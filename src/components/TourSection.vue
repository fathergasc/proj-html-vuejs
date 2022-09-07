<template>
  <section id="tour">
    <div class="tour-top">
        <div class="container">
            <SectionHeader :header="tourHeaderData"/>
            <span class="play-button mt-5" @click="showVideo"><i class="fa-solid fa-play"></i></span>
        </div>
        <!-- video wrapper rendered on show == true and hidden on click on .video-wrapper -->
        <div class="video-wrapper" v-if="show == true" @click="closeVideo">
            <iframe width="960" height="540" src="https://www.youtube.com/embed/4LrQ8V6offk?autoplay=1" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
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
            show: false,
            //data for section header
            tourHeaderData: {
                icon: 'icon-7.png',
                title: 'tour our facilities',
                text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation',
            },
        }
    },
    methods: {
        //functions to show overlayed video
        showVideo() {
            this.show = true;
        },
        closeVideo() {
            this.show = false;
        }
    }
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
    position: relative;

    span {
        color: white;

        &:hover {
            color: white; //bootstrap override
            transform: scale(1.1);
            cursor: pointer;
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

.video-wrapper {
    position: fixed;
    top:50%;
    left:50%;
    transform: translate(-50%, -50%);
    height: 100%;
    width: 100%;
    z-index: 999;
    padding: 1rem;
    display: flex;
    justify-content: center;
    align-items: center;
}

.close-video {
    position: absolute;
    top: -10%;
    right: -10%;
    background-color: #081425;
    color: white;
    height: 50px;
    width: 50px;
    font-size: 2rem;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 50%;
}
</style>