<template>
  <div class="home">

    <LandingHero />
    <WhyStream />
    <CallToAction />
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import LandingHero from "@/components/LandingPage/LandingHero.vue"
import WhyStream from '@/components/LandingPage/WhyStream.vue';
import CallToAction from '@/components/LandingPage/CallToAction.vue';

@Options({
  components: {

    LandingHero,
    WhyStream,
    CallToAction,

  },
})
export default class HomeView extends Vue { }
</script>
