<template>
  <main>
    <WelcomeSection />
    <DoctorsSection />
    <ServicesSection />
    <TourSection />
    <LearnMoreSection />
    <AppointmentSection />
    <ClientsSection />
  </main>
</template>

<script>
import WelcomeSection from './WelcomeSection.vue'
import DoctorsSection from './DoctorsSection.vue'
import ServicesSection from './ServicesSection.vue'
import TourSection from './TourSection.vue'
import LearnMoreSection from './LearnMoreSection.vue'
import AppointmentSection from './AppointmentSection.vue'
import ClientsSection from './ClientsSection.vue'

export default {
 name: 'MyMain',
 components:  {
    WelcomeSection,
    DoctorsSection,
    ServicesSection,
    TourSection,
    LearnMoreSection,
    AppointmentSection,
    ClientsSection,
 },
}
</script>

<style lang="scss">

</style>