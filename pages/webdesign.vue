<template>
  <div>
    <Webdesign />
  </div>
</template>

<script>
import Webdesign from "../components/webdesign";

export default {
  components: {
    Webdesign
  },
  data() {
    return {
      code: "Web design"
    };
  },
  head() {
    return {
      title: this.code
    };
  }
};
</script>

<style>
</style>
