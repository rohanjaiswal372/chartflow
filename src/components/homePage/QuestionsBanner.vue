<template>
  <div class="text-center">
    <div class="component-header">
      <h1 class="heading">Still have questions?</h1>
      <p class="paragraph">
        Answers to your top questions on enhancing your healthcare education
        experience.
      </p>
    </div>

    <div class="q-pa-md expansion-card">
      <q-list padding class="expansion-card-list">
        <q-expansion-item
          v-for="(question, index) in questions"
          :key="index"
          :name="index"
          :label="question.label"
          class="expansion-card-item"
          expand-icon="add"
          expanded-icon="remove"
        >
          <q-card>
            <q-card-section class="custom-card-section">
              {{ question.description }}
            </q-card-section>
          </q-card>
        </q-expansion-item>
      </q-list>
    </div>
  </div>
</template>

<script setup>
defineOptions({
  name: "QuestionsBanner",
});

const questions = [
  {
    id: 1,
    label: "What support is available for technical issues?",
    description:
      "ChartFlow offers comprehensive customer support. If you encounter any technical issues, you can reach out to our support team through the Contact Us form, and we'll assist you promptly.",
  },
  {
    id: 2,
    label: "Can students customize their learning experience with ChartFlow?",
    description:
      "ChartFlow offers comprehensive customer support. If you encounter any technical issues, you can reach out to our support team through the Contact Us form, and we'll assist you promptly.",
  },
  {
    id: 3,
    label:
      "Are there custom pricing options for organizations or international users?",
    description:
      "ChartFlow offers comprehensive customer support. If you encounter any technical issues, you can reach out to our support team through the Contact Us form, and we'll assist you promptly.",
  },
  {
    id: 4,
    label: "What are the benefits of becoming a member?",
    description:
      "ChartFlow offers comprehensive customer support. If you encounter any technical issues, you can reach out to our support team through the Contact Us form, and we'll assist you promptly.",
  },
  {
    id: 5,
    label: "What features are included in the free trial for instructors?",
    description:
      "ChartFlow offers comprehensive customer support. If you encounter any technical issues, you can reach out to our support team through the Contact Us form, and we'll assist you promptly.",
  },
];
</script>
<style scoped>
.expansion-card {
  display: flex;
  justify-content: center;
  width: 80vw;
}
.expansion-card-list {
  width: 100%;
  text-align: left;
}

.expansion-card-item {
  font-size: 24px;
  font-weight: 600;
  padding: 15px 0;
}

.expansion-card-item:not(:last-child) {
  border-bottom: 1px solid #e7e7ea;
}

.expansion-card-item:hover {
  background-color: unset;
}

.custom-card-section {
  font-size: 16px;
  line-height: 16px;
  font-weight: 400;
  padding: 20px;
  color: #939393;
}
</style>
