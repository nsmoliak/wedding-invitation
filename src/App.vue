<template>
  <div id="promise">
    <HeroSection />
    <EventDetails />
    <DaySchedule />
    <DressCode />
    <RsvpForm />
    <CounterSection />
    <FooterSection />
  </div>
</template>

<script setup>
import HeroSection from './components/HeroSection.vue'
import EventDetails from './components/EventDetails.vue'
import DaySchedule from './components/DaySchedule.vue'
import DressCode from './components/DressCode.vue'
import RsvpForm from './components/RsvpForm.vue'
import CounterSection from './components/CounterSection.vue'
import FooterSection from './components/FooterSection.vue'
</script>

<style>
#promise {
  min-height: 100vh;
  overflow-x: hidden;
}
</style>
