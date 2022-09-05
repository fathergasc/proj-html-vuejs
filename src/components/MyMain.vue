<template>
  <main>
    <WelcomeSection />
    <DoctorsSection />
    <ServicesSection />
  </main>
</template>

<script>
import WelcomeSection from './WelcomeSection.vue'
import DoctorsSection from './DoctorsSection.vue'
import ServicesSection from './ServicesSection.vue'

export default {
 name: 'MyMain',
 components:  {
    WelcomeSection,
    DoctorsSection,
    ServicesSection,
 },
 data() {
    return {
        
    }
 },
}
</script>

<style lang="scss">

</style>