<template>
  <main>
    <WelcomeSection />
    <DoctorsSection />
  </main>
</template>

<script>
import WelcomeSection from './WelcomeSection.vue'
import DoctorsSection from './DoctorsSection.vue'

export default {
 name: 'MyMain',
 components:  {
    WelcomeSection,
    DoctorsSection,
 },
 data() {
    return {
        
    }
 },
}
</script>

<style lang="scss">

</style>