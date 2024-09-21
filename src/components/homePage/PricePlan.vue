<template>
  <div class="text-center price-plan">
    <div class="component-header">
      <h1 class="heading">
        <spam class="text-blue">Affordable,</spam> The Best Price
      </h1>
      <p class="paragraph">
        Choose a plan that fits your path to success and transform your
        healthcare education experience.
      </p>
    </div>
    <div class="container">
      <div class="box green">
        <p class="plan-title green-text green-btn">Basic</p>
        <h3 class="plan-price green-text">
          $15 <span class="plan-title-sub">/ student</span>
        </h3>
        <p class="plan-duration">6 months</p>
        <p class="plan-description">
          Affordable and packed with features. Elevate your learning journey
          with a 6-month membership.
        </p>
        <div class="bullet-points text-left">
          <p>
            <q-icon name="check_circle_outline" color="green" size="20px" />
            Perfect for CNA & emergency mdcn
          </p>
          <p>
            <q-icon name="check_circle_outline" color="green" size="20px" />
            Use the system just once or twice
          </p>
          <p>
            <q-icon name="check_circle_outline" color="green" size="20px" />
            Renew or extend license with any plan
          </p>
        </div>
        <div class="plan-button">
          <q-btn
            class="plan-button-get-started green-text green-bg"
            label="Get Started"
          />
        </div>
      </div>
      <div class="box blue">
        <p class="plan-floating-text">MOST POPULAR</p>
        <div class="blue-container">
          <p class="plan-title blue-text blue-btn">Plus</p>
          <h3 class="plan-price blue-text">
            $25 <span class="plan-title-sub">/ student</span>
          </h3>
          <p class="plan-duration">12 months</p>
          <p class="plan-description">
            A year of learning opportunity. Dive deep into healthcare education
            with a 12-month membership.
          </p>
          <div class="bullet-points text-left">
            <p>
              <q-icon name="check_circle_outline" color="blue" size="20px" />
              Ideal for practical nursing and more
            </p>
            <p>
              <q-icon name="check_circle_outline" color="blue" size="20px" />
              Renew or extend license with any plan
            </p>
            <p>
              <q-icon name="check_circle_outline" color="blue" size="20px" />
              Additional 1 month FREE access
            </p>
          </div>
          <div class="plan-button">
            <q-btn
              class="plan-button-get-started text-white blue-bg"
              label="Get Started"
            />
          </div>
        </div>
      </div>
      <div class="box red">
        <p class="plan-title red-text red-btn">Pro</p>
        <h3 class="plan-price red-text">
          $45 <span class="plan-title-sub">/ student</span>
        </h3>
        <p class="plan-duration">24 months</p>
        <p class="plan-description">
          Maximize your educational journey with a 2-year membership. More time,
          more benefits.
        </p>
        <div class="bullet-points text-left">
          <p>
            <q-icon name="check_circle_outline" color="red" size="20px" />
            Designed for ADN and BSN
          </p>
          <p>
            <q-icon name="check_circle_outline" color="red" size="20px" />
            Most affordable EHR on the market
          </p>
          <p>
            <q-icon name="check_circle_outline" color="red" size="20px" />
            Work directly with our Product team
          </p>
        </div>
        <div class="plan-button">
          <q-btn
            class="plan-button-get-started red-text red-bg"
            label="Contact Sales"
          />
        </div>
      </div>
      <div class="box green">
        <p class="plan-title green-text green-btn">Basic</p>
        <h3 class="plan-price green-text">
          $15 <span class="plan-title-sub">/ student</span>
        </h3>
        <p class="plan-duration">6 months</p>
        <p class="plan-description">
          Affordable and packed with features. Elevate your learning journey
          with a 6-month membership.
        </p>
        <div class="bullet-points text-left">
          <p>
            <q-icon name="check_circle_outline" color="green" size="20px" />
            Perfect for CNA & emergency mdcn
          </p>
          <p>
            <q-icon name="check_circle_outline" color="green" size="20px" />
            Use the system just once or twice
          </p>
          <p>
            <q-icon name="check_circle_outline" color="green" size="20px" />
            Renew or extend license with any plan
          </p>
        </div>
        <div class="plan-button">
          <q-btn
            class="plan-button-get-started green-text green-bg"
            label="Get Started"
          />
        </div>
      </div>
    </div>
    <div class="sub-header">
      <h1 class="heading">Free for Educators to Try</h1>
      <p class="paragraph">
        Get a taste of ChartFlow's capabilities with our free 30-day trial for
        instructors and faculty.
      </p>
      <div class="button-container">
        <q-btn class="get-started-free" label="Start my 30-day free trial" />
      </div>
      <p class="footnote">Cancel anytime. No credit card required.</p>
    </div>
  </div>
</template>

<script setup>
defineOptions({
  name: "PricePlan",
});
</script>
<style scoped>
.price-plan {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 1rem;
  background-color: #f5f8fd;
  width: 100vw;
}

.container {
  display: flex;
  justify-content: space-between;
  gap: 1rem;
  padding: 1rem;
  width: 90vw;
}

.box {
  background-color: #ffffff;
  border-radius: 60px;
  padding: 4rem 1rem 0 1rem;
  flex: 1;
}

.plan-title {
  font-size: 14px;
  font-weight: 600;
  line-height: 16px;
}

.plan-price {
  font-size: 64px;
  font-weight: 600;
  line-height: 77px;
}

.plan-title-sub {
  font-size: 16px;
  font-weight: 400;
  line-height: 19px;
}

.plan-duration {
  font-size: 24px;
  font-weight: 600;
  line-height: 29px;
}

.plan-description {
  color: #939393;
  font-size: 16px;
  font-weight: 500;
  line-height: 26px;
}

.bullet-points {
  padding: 20px 0;
}

.bullet-points p {
  font-size: 16px;
  font-weight: 500;
  line-height: 10px;
}

.plan-button-get-started {
  border-radius: 30px;
  padding: 15px 100px;
  font-size: 14px;
  margin: 0;
}

.green-text {
  color: #2dca54;
}
.green-bg {
  background-color: #e9fbee;
}
.green-btn {
  background-color: #e9fbee;
  margin: 0 100px;
  padding: 10px 40px;
  border-radius: 20px;
}

.blue {
  border: 1px solid #2f76d3;
}
.blue-container {
  z-index: 999;
  position: relative;
  padding-top: 60px;
  top: -135px;
  background: white;
  border-radius: 40px;
}

.plan-floating-text {
  position: relative;
  background-color: #2f76d3;
  color: white;
  border-radius: 35px;
  top: -92px;
  margin: 0 40px;
  padding: 5px 30px 40px 30px;
}

.blue-text {
  color: #2f76d3;
}
.blue-bg {
  background-color: #2e76d3;
}
.blue-btn {
  background-color: #eaf1fb;
  margin: 0 100px;
  padding: 10px 40px;
  border-radius: 20px;
}

.red-text {
  color: #fc416a;
}
.red-bg {
  background-color: #ffecf0;
}
.red-btn {
  background-color: #ffecf0;
  margin: 0 100px;
  padding: 10px 40px;
  border-radius: 20px;
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

.sub-header .heading {
  font-size: 36px;
  font-weight: 600;
  line-height: 43px;
}

.sub-header .paragraph {
  font-size: 16px;
  font-weight: 500;
  line-height: 19px;
  color: #a3a3a3;
  padding-bottom: 20px;
}

.sub-header .footnote {
  font-size: 14px;
  font-weight: 400;
  line-height: 16px;
  padding: 10px 0;
  color: #a3a3a3;
}

.get-started-free {
  background-color: #eaf1fb;
  color: #2f76d3;
  border-radius: 30px;
  padding: 10px 30px;
  font-size: 14px;
  margin: 0;
}
</style>
