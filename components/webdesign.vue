<template>
  <div class="back-banner">
    <div class="web-nav pt-4">
      <b-navbar toggleable="lg" type="dark">
        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav>
            <b-nav-item href="#">
              <b-navbar-brand to="/" class="text-uppercase">Smart Simple</b-navbar-brand>
            </b-nav-item>
          </b-navbar-nav>

          <!-- Right aligned nav items -->
          <b-navbar-nav class="ml-auto">
            <b-nav-item>
              <b-navbar-brand to="/" class="text-uppercase">Home</b-navbar-brand>
            </b-nav-item>
            <b-nav-item>
              <b-navbar-brand href="#" class="text-uppercase">Work</b-navbar-brand>
            </b-nav-item>
            <b-nav-item>
              <b-navbar-brand href="#" class="text-uppercase">Contact</b-navbar-brand>
            </b-nav-item>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
    </div>
    <!-- end of nav -->
    <div class="web-body mt-5">
      <div class="container-fluid">
        <h1 class="text-uppercase light">
          Start landing page
          <br />for you product &
          <br />services
        </h1>
        <p
          class="pt-4"
        >Perfect landing page to showcase your product or service. Built with Bootstrap 4</p>
        <p class="pt-2">
          <b class="text-uppercase">Try for free</b> . Just leave your e-mail below and get in touch
        </p>
        <div class="web-form pt-2">
          <form class="form-inline">
            <input
              type="text"
              class="form-control mr-2 mb-2 mt-2"
              id="inputPassword2"
              placeholder="*Your Email Addres"
            />

            <button type="submit" class="btn btn-danger pl-5 pr-5 pt-2 pb-2">Request Free Trail</button>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {};
  },
  methods: {},

  mounted() {}
};
</script>

<style>
.back-banner {
  background-image: url("/markup-1.png");

  background-size: cover;

  height: 625px;

  background-repeat: no-repeat;
  padding: 10px;
}
.web-body {
  color: white;
}
.navbar-dark .navbar-brand:hover {
  color: aqua;
  transition: 0.3s;
}
</style>
