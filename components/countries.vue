<template>
  <div class="container">

<b-table id="my-table"
:per-page="perPage"
      :current-page="currentPage"
      striped hover :items="countries"
      :fields="fields">

      <template v-slot:cell(code)="data">
        <nuxt-link :to="`/country/${data.value.toUpperCase()}`"><b-button variant="success">{{ data.value }}</b-button></nuxt-link>

      </template>

      </b-table>
<b-pagination
      v-model="currentPage"
      :total-rows="rows"
      :per-page="perPage"
      aria-controls="my-table"
    ></b-pagination>
</div>
</template>

<script>


export default {
  components: {

  },
  data () {
    return {
      perPage: 8,
        currentPage: 1,
      countries: [],
fields: [
          {
            key: 'name',
            sortable: true
          },
          {
            key: 'languages',
            sortable: false
          },
          {
            key: 'continent',

            sortable: true,

          },
          {
            key: 'code',

            sortable: true,

          }
        ],
    }
  },
  methods: {
  async fetchSomething() {
    const countries = await this.$axios.$get('https://countriesnode.herokuapp.com/v1/countries/')
    this.countries=countries
  }
},
mounted() {
    this.fetchSomething()
  },
  computed: {
      rows() {
        return this.countries.length
      }
}
}
</script>

<style>

</style>
