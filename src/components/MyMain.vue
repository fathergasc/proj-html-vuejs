<template>
  <main>
    <WelcomeSection />
    <DoctorsSection />
    <ServicesSection />
    <TourSection />
    <LearnMoreSection />
    <AppointmentSection />
  </main>
</template>

<script>
import WelcomeSection from './WelcomeSection.vue'
import DoctorsSection from './DoctorsSection.vue'
import ServicesSection from './ServicesSection.vue'
import TourSection from './TourSection.vue'
import LearnMoreSection from './LearnMoreSection.vue'
import AppointmentSection from './AppointmentSection.vue'

export default {
 name: 'MyMain',
 components:  {
    WelcomeSection,
    DoctorsSection,
    ServicesSection,
    TourSection,
    LearnMoreSection,
    AppointmentSection,
 },
 data() {
    return {
        
    }
 },
}
</script>

<style lang="scss">

</style>