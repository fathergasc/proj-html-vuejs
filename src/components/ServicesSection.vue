<template>
  <section id="services">
    <div class="container">
        <SectionHeader :header="servicesHeaderData"/>
        <div class="services-cards pt-4">
            <SmallCard v-for="(card, index) in servicesCards" :key="index" :card="card"/>
        </div>
    </div>
    
  </section>
</template>

<script>
import SectionHeader from './SectionHeader.vue'
import SmallCard from './SmallCard.vue'

export default {
    name: 'ServicesSection',
    components: {
        SectionHeader,
        SmallCard,
    },
    data() {
        return {
            //data for section header
            servicesHeaderData: {
                icon: 'icon-6.png',
                title: 'our health services',
                text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation',
            },
            //data for services cards v-for
            servicesCards: [
            {
                image: 'icon-14.png',
                title: 'rehabilitation center',
                text: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium totam rem aperiam eaque ipsa',
            },
            {
                image: 'icon-15.png',
                title: 'dental implants',
                text: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium totam rem aperiam eaque ipsa',
            },
            {
                image: 'icon-16.png',
                title: 'medicine research',
                text: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium totam rem aperiam eaque ipsa',
            },
            {
                image: 'icon-11.png',
                title: 'blood bank',
                text: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium totam rem aperiam eaque ipsa',
            },
            {
                image: 'icon-12.png',
                title: 'pharmaceutical advice',
                text: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium totam rem aperiam eaque ipsa',
            },
            {
                image: 'icon-13.png',
                title: 'medical counseling',
                text: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium totam rem aperiam eaque ipsa',
            },
            ]
        }
    }
}
</script>

<style lang="scss">
@import '../styles/variables.scss';

.services-cards {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;

    .small-card {
        width: calc(100% / 3 - 2rem);
        margin: 1rem;

        &:hover > h5 {
            color: $blue_light;
        }
    }
}

</style>