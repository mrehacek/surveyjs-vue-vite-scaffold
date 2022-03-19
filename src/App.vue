<template>
  <Survey :survey="survey" />
</template>

<script>
import "survey-vue/modern.min.css";
import { StylesManager, Model, Survey } from "survey-vue";

StylesManager.applyTheme("modern");

const surveyJson = {
  elements: [
    {
      name: "FirstName",
      title: "Enter your first name:",
      type: "text",
    },
    {
      name: "LastName",
      title: "Enter your last name:",
      type: "text",
    },
  ],
};

export default {
    components: {
    Survey
  },
  data() {
    const survey = new Model(surveyJson);
    return {
      survey,
    };
  },
};
</script>
