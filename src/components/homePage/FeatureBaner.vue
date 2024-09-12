<template>
  <div class="text-center feature-box">
    <div class="component-header">
      <h1 class="heading">What's inside?</h1>
      <p class="paragraph">
        Explore the key features that make ChartFlow the ultimate choice<br />for
        healthcare education.
      </p>
    </div>
    <div class="container">
      <div class="box pink">
        <div class="logo"><q-img src="/assets/homePage/internet.png" /></div>
        <h3>Global Accessibility</h3>
        <p>
          ChartFlow's servers span the globe to ensure fast and reliable access
          for educators and students across diverse geographic locations.
        </p>
      </div>
      <div class="box blue">
        <div class="logo"><q-img src="/assets/homePage/clinic.png" /></div>
        <h3>Realistic EHR Simulation</h3>
        <p>
          Immerse students in authentic clinical scenarios through ChartFlow's
          Inpatient and Outpatient EHR simulations for enhanced practice
          readiness.
        </p>
      </div>
      <div class="box yellow">
        <div class="logo">
          <q-img src="/assets/homePage/online-learning-01.png" />
        </div>
        <h3>Learning Management</h3>
        <p>
          ChartFlow's user-friendly interface allows quick setup for small
          groups and advanced functionalities for larger cohorts.
        </p>
      </div>
    </div>
  </div>
</template>

<script setup>
defineOptions({
  name: "FeatureBanner",
});
</script>
<style scoped>
.feature-box {
  padding-bottom: 8rem;
}
.container {
  display: flex; /* Align divs horizontally */
  justify-content: space-between; /* Space out the boxes */
  gap: 3rem; /* Add space between the boxes */
  padding: 1rem;
  width: 80vw;
}

.box {
  background-color: #f0f0f0; /* Light gray background for visibility */
  border: 1px solid #ccc; /* Light border */
  border-radius: 60px; /* Rounded corners */
  padding: 4rem 2rem; /* Padding inside the box */
  flex: 1; /* Make all boxes equal width */
}

.pink {
  background-color: #fffafb;
  border: 2px solid #fdb9c8;
}

.blue {
  background-color: #f8fafc;
  border: 2px solid #bcd1f0;
}

.yellow {
  background-color: #fffef9;
  border: 2px solid #feedb0;
}

.logo {
  display: flex; /* Use flexbox for centering */
  justify-content: center; /* Center the image horizontally */
  align-items: center; /* Center the image vertically */
  margin-bottom: 1rem; /* Add space between the logo and heading */
  width: 100px;
  margin: 0 auto;
}

h3 {
  margin-bottom: 0.5rem; /* Space between h3 and p */
  font-size: 24px;
  line-height: 36px;
}

p {
  margin-top: 0; /* Remove default top margin */
  line-height: 26px; /* Adjust line height for readability */
  font-size: 16px;
}
</style>
