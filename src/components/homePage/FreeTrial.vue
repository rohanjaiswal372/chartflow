<template>
  <div class="block text-center">
    <div class="container text-center">
      <div class="component-header">
        <h1 class="heading">
          Make a <span class="text-blue">Positive Change</span> in Healthcare
          Education
        </h1>
        <p class="paragraph">
          Dive into a 30-day free trial with ChartFlow and transform your
          teaching into a professional way. Empower your students and unlock a
          future of confident healthcare professionals. Let’s get started
          together! Sign up for your free trial today.
        </p>
      </div>
      <div class="button-container">
        <q-btn class="start-free-trial" label="Start my 30-day free trial" />
      </div>
      <p class="footnote">Cancel anytime. No credit card required.</p>
    </div>
  </div>
</template>

<script setup>
defineOptions({
  name: "FreeTrial",
});
</script>
<style scoped>
.block {
  width: 100vw;
  background-color: #f5f8fd;
  padding: 5rem;
}

.container {
  display: flex;
  flex-direction: column; /* Stack elements vertically */
  justify-content: center;
  align-items: center; /* Center elements horizontally */
  width: 80vw;
  text-align: center; /* Ensure text is centered */
  gap: 1rem; /* Space between elements */
  margin: 0 auto;
}

.footnote {
  font-size: 14px;
  line-height: 16px;
}

.start-free-trial {
  background-color: #2f76d3;
  color: white;
  border-radius: 30px;
  padding: 8px 6px;
  width: 220px;
  height: 45px;
}
</style>
