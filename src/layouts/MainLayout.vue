<template>
  <q-layout view="lHh Lpr lFf">
    <q-page-container class="chartflow-layout">
      <q-header elevated class="chartflow-header text-black">
        <q-toolbar class="toolbar-centered">
          <q-icon class="logo">
            <img src="/logo.svg" />
          </q-icon>
          <q-tabs v-model="tab" class="navlink">
            <Navbar v-for="link in navLinks" :key="link.title" v-bind="link" />
          </q-tabs>
          <q-btn class="get-started" label="Get Started" />
        </q-toolbar>
      </q-header>
    </q-page-container>

    <q-page-container>
      <router-view />
      <FooterComponent />
    </q-page-container>
  </q-layout>
</template>

<script setup>
import { ref } from "vue";
import Navbar from "src/components/navbar/Navbar.vue";
import FooterComponent from "src/components/Footer.vue";

defineOptions({
  name: "MainLayout",
});

const navLinks = [
  {
    title: "Features",
  },
  {
    title: "Testimonials",
  },
  {
    title: "Pricing",
  },
  {
    title: "Login",
  },
];

const leftDrawerOpen = ref(false);

function toggleLeftDrawer() {
  leftDrawerOpen.value = !leftDrawerOpen.value;
}
</script>
<style lang="scss" scoped>
.chartflow-layout {
  width: 90%;
  max-width: 80vw; /* Ensure it doesn't overflow the viewport width */
  margin: 0 auto;
  overflow-x: hidden; /* Prevent horizontal scrolling */
}
.chartflow-header {
  width: 90%;
  margin: 0 auto;
}
.logo {
  width: 150px;
  height: 70px;
}
.toolbar-centered {
  display: flex;
  justify-content: space-between; /* Spread items across the toolbar */
  align-items: center; /* Vertically center items */
  width: 100%;
}

.navlink {
  flex: 1; /* Take up available space */
  display: flex;
  justify-content: center; /* Center the nav links horizontally */
  align-items: center;
}

.get-started {
  background-color: #2f76d3; /* Set background to blue */
  color: white; /* Set text to white */
  border-radius: 20px; /* Make the button circular */
  padding: 6px 12px;
  width: 140px; /* Set width */
  height: 40px; /* Set height to keep it circular */
}
</style>
