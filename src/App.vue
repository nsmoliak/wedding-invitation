<template>
  <div id="promise">
    <HeroSection />
    <EventDetails />
    <DaySchedule />
    <DressCode />
    <RsvpForm />
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
import RsvpForm from './components/RsvpForm.vue'
import CounterSection from './components/CounterSection.vue'
import FooterSection from './components/FooterSection.vue'
import DetailsSection from "./components/DetailsSection.vue";
import TransferSection from "./components/TransferSection.vue";
</script>

<style>
#promise {
  min-height: 100vh;
  overflow-x: hidden;
  background-color: var(--accent);
}
</style>
