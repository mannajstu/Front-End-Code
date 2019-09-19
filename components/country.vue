<template>
  <div class="container">
<nuxt-link to="/" ><b-button variant="success">Home</b-button></nuxt-link>

<b-table striped hover :items="country" :fields="fields"></b-table>


</div>
</template>

<script>


export default {
  components: {

  },
  data () {
    return {
country:[],
fields: [
{ key: '0', label: 'Options' },
{ key: '1', label: 'Data' },
        ],

    }
  },
  methods: {
  async countryData() {
    const countrydata = await this.$axios.$get('https://countriesnode.herokuapp.com/v1/countries/' + this.$route.params.code )
const resultArray = Object.keys(countrydata).map(function(key) {
  return [key, countrydata[key]];
});
this.country=resultArray
  }
},

mounted() {

    this.countryData()
  },

}
</script>

<style>

</style>
