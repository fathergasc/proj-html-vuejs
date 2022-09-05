<template>
  <section id="welcome" class="container">
    <div class="welcome-top">
        <h2>Welcome to Avada Health</h2>
        <p class="py-3">Lorem ipsum dolor sit amet consectetur adipisicing elit. Consectetur eligendi quasi similique eaque esse quod reiciendis perferendis aut nisi repellat.</p>
    </div>
    <div class="welcome-cards pt-3">
        <SmallCard v-for="(card, index) in welcomeCards" :key="index" :welcomeCards="card" />
    </div>
    
  </section>
</template>

<script>
import SmallCard from './SmallCard.vue'


export default {
    name: 'WelcomeSection',
    data() {
        return {
            welcomeCards: [
            {
                image: 'icon-1.png',
                title: 'same day appointments',
                text: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium',
            },
            {
                image: 'icon-2.png',
                title: 'world class facilities',
                text: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium',
            },
            {
                image: 'icon-3.png',
                title: 'expert doctors',
                text: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium',
            },
            {
                image: 'icon-4.png',
                title: 'complementary therapies',
                text: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium',
            },
            ]
        } 
    },
    components: {
        SmallCard,
    },
 }

</script>

<style lang="scss">
.container {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    padding: 4rem 0;

    h2 {
        font-weight: 300;
        font-size: 1.5rem;
    }
}

.welcome-top {
    width: 60%;
    text-align: center;
}

.welcome-cards {
    display: flex;
    justify-content: center;
    align-items: flex-start;
}

</style>