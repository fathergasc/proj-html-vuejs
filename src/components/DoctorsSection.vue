<template>
  <section id="doctors">
    <SectionHeader :header="sectionHeaderData"/>
  </section>
</template>

<script>
import SectionHeader from './SectionHeader.vue'

export default {
    name: 'DoctorsSection',
    components: {
        SectionHeader,
    },
    data() {
        return {
            sectionHeaderData: {
                icon: 'icon-5.png',
                title: 'meet our doctors',
                text: 'lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation',
            }
        
        }
    },
}

</script>

<style lang="scss">
@import '../styles/variables.scss';

#doctors {
    background-color: $grey_light;
}

</style>