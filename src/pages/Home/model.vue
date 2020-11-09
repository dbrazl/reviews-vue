<script>
import reviews from "../../assets/reviews.js";
import View from "./view.vue";

export default {
  name: "Home",
  components: {
    View,
  },
  data: function() {
    return {
      reviews,
    };
  },
};
</script>

<template>
  <View :reviews="reviews" />
</template>
