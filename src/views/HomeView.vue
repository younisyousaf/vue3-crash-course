<script setup>
import Hero from "@/components/Hero.vue";
import HomeCards from "@/components/HomeCards.vue";
import JobListing from "@/components/JobListing.vue";
</script>

<template>
  <Hero
    title="Become a Vue Dev"
    subtitle="Find the Vue Job that fits your skills and needs"
  />

  <HomeCards />
  <JobListing :job-limit="3" :show-button="true" />
</template>
