<template>
  <div>
    <b-form action="/search">
      <b-input-group class="">
        <b-form-input
          placeholder="Buscar..."
          type="search"
          
          name="search"
          id="search"
          ref="search"
          v-model="searchinput"
        >
        </b-form-input>
      </b-input-group>
    </b-form>
  </div>
</template>

<script>
export default {
  name: "SearchForm",
  data() {
    return {
      searchinput: null
    };
  },
  mounted() {
    // set the focus when the component opened
    this.$refs.search.focus();
  },
  props: {
    currentinput: {
      type: String,
      default: null
    }
  },
  created() {
    if (this.currentinput !== null) {
      this.searchinput = this.currentinput;
    }
  }
};
</script>
