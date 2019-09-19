<template>
  <div>
    <Country></Country>
  </div>
</template>

<script>
import Country from "~/components/country";
export default {
  components: {
    Country
  },
  data() {
    return {
      code: null
    };
  },
  head() {
    return {
      title: this.code
    };
  },

  mounted() {
    this.code = this.$route.params.code.toUpperCase();
  }
};
</script>

<style>
</style>
