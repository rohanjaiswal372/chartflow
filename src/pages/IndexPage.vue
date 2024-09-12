<template>
  <q-page class="flex flex-center">
    <BannerComponent />
    <FeatureBaner />
    <FreeTrial />
    <ExploreBanner />
    <TestimonialComponent />
    <PricePlan />
    <QuestionsBanner />
  </q-page>
</template>

<script setup>
import BannerComponent from "components/homePage/Banner.vue";
import FeatureBaner from "components/homePage/FeatureBaner.vue";
import FreeTrial from "components/homePage/FreeTrial.vue";
import ExploreBanner from "components/homePage/ExploreBanner.vue";
import TestimonialComponent from "components/homePage/TestimonialComponent.vue";
import PricePlan from "components/homePage/PricePlan.vue";
import QuestionsBanner from "components/homePage/QuestionsBanner.vue";

defineOptions({
  name: "IndexPage",
});
</script>
<style >
@import "../css/homePage.scss";
</style>
