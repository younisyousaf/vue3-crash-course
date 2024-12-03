<script setup>
import { ref } from "vue";
import Hero from "@/components/Hero.vue";
import HomeCards from "@/components/HomeCards.vue";
import JobListing from "@/components/JobListing.vue";

const text = ref("");

const onChange = (event) => {
  text.value = event.target.value;
  console.log(text.value);
};
</script>

<template>
  <Hero
    title="Become a Vue Dev"
    subtitle="Find the Vue Job that fits your skills and needs"
  />

  <div>
    <label for=""> Name: </label>
    <input class="border" :value="text" @input="onChange" />
  </div>

  <HomeCards />
  <JobListing :job-limit="3" :show-button="true" />
</template>
