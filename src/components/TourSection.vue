<template>
  <section id="tour">
    <div class="tour-top">
        <div class="container">
            <SectionHeader :header="tourHeaderData"/>
            <a href="#" class="play-button mt-5"><i class="fa-solid fa-play"></i></a>
        </div>
    </div>
    
    
  </section>
</template>

<script>
import SectionHeader from './SectionHeader.vue'

export default {
    name: 'TourSection',
    components: {
        SectionHeader,
    },
    data() {
        return {
            tourHeaderData: {
                icon: 'icon-7.png',
                title: 'tour our facilities',
                text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation',
            },
        }
    },
}
</script>

<style lang="scss">

@import '../styles/variables.scss';

.tour-top {
    padding: 4rem 0;
    color: white;
    background-image: url(../assets/images/paralax-bg-tour-facilities.jpg);
    background-size: cover;
    background-position: center;

    a {
        color: white;

        &:hover {
            color: white; //bootstrap override
            transform: scale(1.1);
        }

    }
}

.play-button {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 4rem;
    width: 4rem;
    background-image: linear-gradient(45deg, $blue_light, $blue_median, $blue_dark);
    border-radius: 50%;

    i {
        font-size: 1.5rem;
    }
}
</style>