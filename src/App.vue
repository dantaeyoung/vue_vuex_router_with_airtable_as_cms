<template>
  <div id="app">
      <router-view name="nav" />
      <router-view name="view" />
  </div>
</template>

<script>

/* eslint-disable */

const process_api_key = process.env.VUE_APP_AIRTABLE_API_KEY;
const airtable_table = process.env.VUE_APP_AIRTABLE_TABLE;
const airtable_base = process.env.VUE_APP_AIRTABLE_BASE;
const airtable_view = process.env.VUE_APP_AIRTABLE_VIEW ;

export default {
  name: "App",
  components: {
  },
  data() {
    return {
    };
  },
  created() {
    this.$store.dispatch("fetchData");
  },
  methods: {
  }
};
</script>

<style>



body {
  background: no-repeat center center fixed;
  background-color: lightgray;
}

#app {
  color: black;
  margin-top: 60px;
  padding: 1em;
}

@media only screen and (max-width: 1020px) {
  #app {
    display: none;
  }

  #mobile {
    color: green;
    display: block !important;
    font-size: 3em;
  }
}


</style>
