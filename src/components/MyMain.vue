<template>
  <main>
    <WelcomeSection />
    <DoctorsSection />
    <ServicesSection />
    <TourSection />
    <LearnMoreSection />
  </main>
</template>

<script>
import WelcomeSection from './WelcomeSection.vue'
import DoctorsSection from './DoctorsSection.vue'
import ServicesSection from './ServicesSection.vue'
import TourSection from './TourSection.vue'
import LearnMoreSection from './LearnMoreSection.vue'

export default {
 name: 'MyMain',
 components:  {
    WelcomeSection,
    DoctorsSection,
    ServicesSection,
    TourSection,
    LearnMoreSection,
 },
 data() {
    return {
        
    }
 },
}
</script>

<style lang="scss">

</style>