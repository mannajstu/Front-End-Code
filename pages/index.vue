<template>
  <div class="container">
    <nuxt-link to="/countries">
      <b-button variant="success">Countries</b-button>
    </nuxt-link>
    <nuxt-link to="/webdesign">
      <b-button variant="danger">Web Design</b-button>
    </nuxt-link>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      title: "Home"
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
