<template>
  <section id="learn-more">
    <LearnMoreCard v-for="(card, index) in learnMoreCards" :key="index" :card="card" :style="card.color"/>
  </section>
</template>

<script>
import LearnMoreCard from './LearnMoreCard.vue'

export default {
    name: 'LearnMoreSection',
    components: {
        LearnMoreCard,
    },
    data() {
        return {
            //data for learn-more cards v-for with color key to change bg-color
            learnMoreCards: [
                {
                    title: 'Emergency Care',
                    text: 'lorem ipsum dolor sit amet, consectetur adipisicing elit. Quisquam, quod.',
                    color: 'background-color: #39afbb',
                },
                {
                    title: 'Expert Diagnostics',
                    text: 'lorem ipsum dolor sit amet, consectetur adipisicing elit. Quisquam, quod.',
                    color: 'background-color: #3597c3',
                },
                {
                    title: 'Superb Rehabilitation',
                    text: 'lorem ipsum dolor sit amet, consectetur adipisicing elit. Quisquam, quod.',
                    color: 'background-color: #327ec7',
                },
            ],
        }
    },
}
</script>

<style lang="scss">
@import '../styles/variables.scss';

#learn-more {
    display: flex;
}

</style>