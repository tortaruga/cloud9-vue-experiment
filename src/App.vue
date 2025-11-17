<script setup>
import Navbar from './components/layout/navbar.vue';
import Intro from './components/layout/Intro.vue';
import PhilosophySection from './components/layout/PhilosophySection.vue';
import DestinationsSection from './components/layout/DestinationsSection.vue';
import Disclaimer from './components/layout/Disclaimer.vue';
import ReviewsSection from './components/layout/ReviewsSection.vue'
import Contacts from './components/layout/Contacts.vue';
import EventsSection from './components/layout/EventsSection.vue'

</script>

<template>
  <div>
    <main>
      <Navbar></Navbar>
      <Intro></Intro>
      <PhilosophySection></PhilosophySection>
      <DestinationsSection />  
      <ReviewsSection />
      <EventsSection />
      <Disclaimer />
      <Contacts />      
    </main>

  
  </div>
</template>


<style scoped>
</style>
