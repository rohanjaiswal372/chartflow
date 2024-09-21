<template>
  <div class="text-center">
    <div class="component-header">
      <h1 class="heading">
        Build your Future with Innovative
        <span class="text-blue">EHR Solutions</span>
      </h1>
      <q-img src="/assets/homePage/Path.png" class="path-image" />
      <p class="paragraph">
        ChartFlow is a realistic EHR platform tailored for nursing, allied
        health, and medical programs. Experience the future of learning in
        healthcare.
      </p>
    </div>
    <div class="button-container">
      <q-btn class="start-free-trial" label="Start Free Trial" />
      <q-btn
        class="watch-demo"
        label="Watch a Demo"
        icon="play_circle_outline"
      />
    </div>
    <div class="icon-container">
      <q-icon v-for="n in 4" :key="n" name="star" />
      <q-icon name="star_half" />
      <p>5,000+ success stories</p>
    </div>
    <div class="dashboad-container">
      <q-img src="/assets/dashboad.png" class="dashboad-image" />
      <div class="fade-overlay"></div>
    </div>
    <div class="logo-container">
      <div class="logo"><q-img src="/assets/image 10.png" /></div>
      <div class="logo"><q-img src="/assets/image 15.png" /></div>
      <div class="logo"><q-img src="/assets/image 16.png" /></div>
      <div class="logo"><q-img src="/assets/image 10.png" /></div>
      <div class="logo"><q-img src="/assets/image 17.png" /></div>
    </div>
  </div>
</template>

<script setup>
defineOptions({
  name: "BannerComponent",
});
</script>
<style scoped>
.button-container {
  display: flex;
  justify-content: center;
  gap: 1rem;
  margin-top: 2rem;
}

.start-free-trial {
  background-color: #2f76d3;
  color: white;
  border-radius: 30px;
  padding: 8px 6px;
  width: 180px;
  height: 45px;
}
.watch-demo {
  background-color: white;
  border: 1px solid #2f76d3;
  color: #2f76d3;
  border-radius: 30px;
  padding: 8px 6px;
  width: 180px;
  height: 45px;
}
.icon-container {
  padding: 10px 0;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 0.5rem;
  color: #f5c308;
}
.icon-container p {
  color: black;
  padding-top: 15px;
  padding-left: 15px;
}
.dashboad-container {
  position: relative;
  display: flex;
  width: 80vw;
  justify-content: center;
  margin: 0 auto;
  background: linear-gradient(to bottom, transparent, rgba(255, 255, 255, 0.2));
}
.dashboard-image {
  display: block; /* Ensure the image is block-level for proper positioning */
}
.fade-overlay {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 30%; /* Adjust height for the fade effect */
  background: linear-gradient(
    to bottom,
    transparent,
    rgba(255, 255, 255, 1) /* Fade to white */
  );
  pointer-events: none; /* Ensure the gradient overlay does not block interactions */
}
.logo-container {
  display: flex;
  justify-content: center;
  gap: 8rem;
  border-top: 1px solid #e7e7ea; /* Top border */
  border-bottom: 1px solid #e7e7ea; /* Bottom border */
  padding: 5px 0;
  width: 100vw;
}
.logo {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 150px;
  height: auto;
  padding: 0 15px;
}

.path-image {
  position: absolute;
  left: 0;
  width: 150px;
}
</style>
