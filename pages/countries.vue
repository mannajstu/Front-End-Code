<template>
  <div class="container">
    <nuxt-link to="/">
      <b-button variant="success">Home</b-button>
    </nuxt-link>
    <Countries />
  </div>
</template>

<script>
import Countries from "../components/countries";

export default {
  components: {
    Countries
  },
  data() {
    return {
      title: "Countries"
    };
  },
  head() {
    return {
      title: this.title
    };
  }
};
</script>

<style>
</style>
