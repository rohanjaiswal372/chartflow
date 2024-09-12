<template>
  <q-page-container>
    <q-layout style="min-height: 100px">
      <q-row class="footer-banner-columns">
        <q-col cols="6" class="footer-chartflow">
          <div>
            <h3 class="footer-banner-header">Ready for The Next Revolution?</h3>
          </div>
        </q-col>

        <q-col cols="1">
          <div class="footer-banner-img">
            <q-img src="/assets/homePage/Path43.png" class="white-img" />
          </div>
        </q-col>

        <q-col cols="3">
          <div class="footer-banner-button">
            <q-btn
              class="start-free-trial"
              label="Start my 30-day free trial"
            />
          </div>
        </q-col>
      </q-row>
    </q-layout>
  </q-page-container>
  <q-page class="footer-layout" style="min-height: 300px">
    <q-page-container>
      <q-layout style="min-height: 300px">
        <q-row class="footer-columns">
          <q-col cols="2" class="footer-chartflow">
            <div class="footer-img-container">
              <q-img src="/assets/homePage/chartflow.png" />
            </div>
            <div class="footer-caption">
              <p>
                Shape the future healthcare professionals seamlessly and
                transform the way you teach and learn.
              </p>
            </div>
          </q-col>

          <q-col
            v-for="(link, index) in footerLinks"
            :key="index"
            cols="2"
            class="column-item"
          >
            <div class="content-box">
              <h4 class="content-title">{{ link.title }}</h4>
              <router-link
                v-for="(menu, idx) in link.options"
                :key="idx"
                :to="menu.path"
                class="content-link"
              >
                {{ menu.name }}
              </router-link>
            </div>
          </q-col>

          <q-col cols="2" class="footer-icons">
            <div class="footer-icons-container">
              <div class="footer-icons-img">
                <router-link to="linkedin.com">
                  <q-img src="/assets/homePage/linkedin.png" />
                </router-link>
              </div>
              <div class="footer-icons-img">
                <router-link to="facebook.com">
                  <q-img src="/assets/homePage/facebook.png" />
                </router-link>
              </div>
            </div>
            <div class="footer-icons-container">
              <div class="footer-icons-img">
                <router-link to="instagram.com">
                  <q-img src="/assets/homePage/instagram.png" />
                </router-link>
              </div>
              <div class="footer-icons-img">
                <router-link to="twitter.com">
                  <q-img src="/assets/homePage/twitter.png" />
                </router-link>
              </div>
            </div>
          </q-col>
        </q-row>
      </q-layout>
    </q-page-container>
  </q-page>
</template>

<script setup>
defineOptions({
  name: "FooterComponent",
});

const footerLinks = [
  {
    title: "Menu",
    options: [
      {
        name: "Benefits",
        path: "/benefits",
      },
      {
        name: "Pricing",
        path: "/pricing",
      },
      {
        name: "Testimonials",
        path: "/testimonials",
      },
    ],
  },
  {
    title: "Resources",
    options: [
      {
        name: "Privacy Policyits",
        path: "/privacypolicy",
      },
      {
        name: "Terms of Service",
        path: "/tos",
      },
      {
        name: "Blog",
        path: "/blog",
      },
    ],
  },
  {
    title: "Support",
    options: [
      {
        name: "Contact Us",
        path: "/contactus",
      },
      {
        name: "Help Center",
        path: "/pricing",
      },
      {
        name: "FAQ",
        path: "/faq",
      },
    ],
  },
];
</script>

<style scoped>
.footer-layout {
  background-color: #dfe9f8;
}
/* Ensure all columns stay in one row */
.footer-columns {
  display: flex;
  justify-content: space-between;
  gap: 2rem; /* Set gap between columns */
  width: 80vw;
  margin: 0 auto;
}

.footer-img-container {
  width: 10rem;
}

.footer-caption {
  width: 18rem;
  font-size: 16px;
  font-weight: 400;
  line-height: 26px;
  padding: 15px 0;
  color: #868789;
}

.column-item {
  text-align: left;
  flex: 1;
}

.content-box {
  display: flex;
  flex-flow: column;
  padding: 0 30px;
}

.content-title {
  margin: 0;
  font-size: 18px;
  font-weight: 500;
  line-height: 21px;
  padding-bottom: 2rem;
}

.content-link {
  font-size: 16px;
  font-weight: 400;
  line-height: 19px;
  color: #868789;
  text-decoration: none;
  padding: 0.2rem 0;
}

.content-link:hover {
  color: black;
}

.footer-icons-container {
  display: flex;
  flex-flow: row;
}

.footer-icons-img {
  width: 2rem;
  margin: 0.5rem;
}

.footer-banner-columns {
  position: relative;
  display: flex;
  justify-content: space-between;
  gap: 2rem; /* Set gap between columns */
  width: 70vw;
  margin: 0 auto;
  background-color: #2f76d3;
  border-radius: 100px;
  padding: 0 3rem;
  top: 20px;
  z-index: 999;
}

.start-free-trial {
  background-color: white;
  color: #2f76d3;
  border-radius: 30px;
  padding: 8px 6px;
  width: 220px;
  height: 45px;
}

.footer-banner-header {
  color: #fff;
  font-size: 36px;
  font-weight: 600;
  padding-left: 4rem;
  padding-right: 0;
}

.footer-banner-button {
  display: flex;
  justify-content: center;
  padding: 2.4rem 0;
  padding-right: 1.5rem;
}

.footer-banner-img {
  display: flex;
  justify-content: left;
  width: 9rem;
  padding: 1rem 0;
}
</style>
