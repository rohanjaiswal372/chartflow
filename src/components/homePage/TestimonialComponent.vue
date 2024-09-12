<template>
  <div class="text-center">
    <div class="component-header">
      <h1 class="heading">
        People Love <span class="text-blue">ChartFlow</span>
      </h1>
      <p class="paragraph">
        Our users share their experiences of ChartFlow, how this is making a
        difference in their teaching and learning journeys.
      </p>
    </div>
    <q-carousel
      v-model="slide"
      height="auto"
      infinite
      animated
      swipeable
      indicators
      navigation
      control-type="dots"
      :autoplay="autoplay"
      ref="carousel"
      class="carousel"
    >
      <q-carousel-slide
        v-for="(testimony, index) in testimonials"
        :key="index"
        :name="index"
      >
        <div class="container">
          <div class="left-block">
            <div class="left-content">
              <div class="text-left">
                <h3 class="name">{{ testimony.name }}</h3>
                <p class="title">— {{ testimony.title }}</p>
                <p class="comment">{{ testimony.comment }}</p>
              </div>
            </div>
          </div>
          <div class="right-block">
            <div class="right-content">
              <div class="img">
                <q-img :src="testimony.img" />
              </div>
            </div>
          </div>
        </div>
      </q-carousel-slide>

      <!-- Custom Arrow Controls -->
      <template v-slot:control>
        <q-carousel-control position="bottom-left" :offset="[30, 40]">
          <q-btn
            class="custom-arrow left-arrow"
            round
            icon="keyboard_arrow_left"
            dense
            @click="prevSlide"
          />
          <q-btn
            class="custom-arrow right-arrow"
            round
            icon="keyboard_arrow_right"
            dense
            @click="nextSlide"
          />
        </q-carousel-control>
      </template>

      <template v-slot:navigation-icon="{ active, btnProps, onClick }">
        <q-btn
          v-if="active"
          size="xs"
          :icon="btnProps.icon"
          color="blue"
          flat
          round
          dense
          @click="onClick"
        ></q-btn>
        <q-btn
          v-else
          size="xs"
          :icon="btnProps.icon"
          color="grey"
          flat
          round
          dense
          @click="onClick"
        ></q-btn>
      </template>
    </q-carousel>
  </div>
</template>

<script setup>
import { ref } from "vue";

defineOptions({
  name: "TestimonialComponent",
});

const slide = ref(0);

const testimonials = [
  {
    name: "Prof. Michael Rodriguez",
    title: "Allied Health Educator",
    comment: `“As an instructor, I appreciate ChartFlow's intuitive design
                  and flexibility. Creating activities and grading student work
                  has never been easier. The platform has become an essential
                  part of our curriculum to help students bridge the gap between
                  theory and practice seamlessly”`,
    img: "/assets/homePage/Group 591.png",
  },
  {
    name: "Prof. Michael Rodriguez 2",
    title: "Allied Health Educator",
    comment: `“As an instructor, I appreciate ChartFlow's intuitive design
                  and flexibility. Creating activities and grading student work
                  has never been easier. The platform has become an essential
                  part of our curriculum to help students bridge the gap between
                  theory and practice seamlessly”`,
    img: "/assets/homePage/Group 591.png",
  },
  {
    name: "Prof. Michael Rodriguez 3",
    title: "Allied Health Educator",
    comment: `“As an instructor, I appreciate ChartFlow's intuitive design
                  and flexibility. Creating activities and grading student work
                  has never been easier. The platform has become an essential
                  part of our curriculum to help students bridge the gap between
                  theory and practice seamlessly”`,
    img: "/assets/homePage/Group 591.png",
  },
];

const nextSlide = () => {
  slide.value = (slide.value + 1) % testimonials.length;
};

const prevSlide = () => {
  slide.value = (slide.value - 1 + testimonials.length) % testimonials.length;
};
</script>

<style scoped>
.component-header {
  padding-bottom: 2rem;
}

.container {
  display: flex;
  justify-content: space-between;
  align-items: stretch;
  gap: 4rem;
  width: 80vw;
}

.left-block,
.right-block {
  flex: 1;
  padding: 10px;
}

.name {
  font-size: 36px;
  font-weight: 600;
  line-height: 43px;
}

.title {
  font-size: 16px;
  font-weight: 400;
  line-height: 19px;
  color: #a3a3a3;
}

.comment {
  font-size: 24px;
  font-weight: 400;
  line-height: 40px;
  color: #a3a3a3;
}

.img {
  display: flex;
  width: 22rem;
  margin: 0 auto;
}

.carousel {
  padding: 3rem 0;
}

/* Custom CSS for arrows */
.custom-arrow {
  position: absolute;
  background-color: #2096f3;
  bottom: 10px;
  z-index: 10;
}

.left-arrow {
  left: 10px;
}

.right-arrow {
  left: 60px;
}

.q-carousel__control--dots {
  bottom: 20px; /* Adjust positioning */
}

.q-carousel__navigation-icon .q-btn {
  width: 14px; /* Custom size for the dots */
  height: 14px;
  border-radius: 50%;
  background-color: black; /* Default color */
  opacity: 0.6; /* Set transparency for non-active dots */
  transition: background-color 0.3s ease, opacity 0.3s ease;
}

.q-carousel__navigation-icon--active {
  width: 16px; /* Slightly larger for the active dot */
  height: 16px;
  background-color: #00cc66; /* Custom color for active indicator */
  opacity: 1; /* Fully opaque for active dot */
}
</style>
