<template>
  <div id="promise">
    <HeroSection />
    <EventDetails />
    <DaySchedule />
    <DressCode />
    <RsvpSection />
    <TransferSection />
    <DetailsSection />
    <CounterSection />
    <FooterSection />
  </div>
</template>

<script setup>
import HeroSection from './components/HeroSection.vue'
import EventDetails from './components/EventDetails.vue'
import DaySchedule from './components/DaySchedule.vue'
import DressCode from './components/DressCode.vue'
import RsvpSection from './components/RsvpSection.vue'
import CounterSection from './components/CounterSection.vue'
import FooterSection from './components/FooterSection.vue'
import DetailsSection from "./components/DetailsSection.vue";
import TransferSection from "./components/TransferSection.vue";
</script>

<style>
#promise {
  min-height: 100vh;
  overflow-x: hidden;
}
</style>
