<template>
  <main>
    <WelcomeSection />
    <DoctorsSection />
    <ServicesSection />
    <TourSection />
  </main>
</template>

<script>
import WelcomeSection from './WelcomeSection.vue'
import DoctorsSection from './DoctorsSection.vue'
import ServicesSection from './ServicesSection.vue'
import TourSection from './TourSection.vue'

export default {
 name: 'MyMain',
 components:  {
    WelcomeSection,
    DoctorsSection,
    ServicesSection,
    TourSection,
 },
 data() {
    return {
        
    }
 },
}
</script>

<style lang="scss">

</style>