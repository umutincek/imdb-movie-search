<template>
  <div>
    <b-card class="my-5 mx-5">
      <label>Movie Search</label>
      <b-form-input v-model="searchText" placeholder="Enter your movie name"></b-form-input>
    </b-card>

    <b-card class="my-5 mx-5">
      <TableComponent :data-list="searchMovies" />
    </b-card>
  </div>
</template>

<script>
import debounce from 'lodash/debounce';
import { mapState } from 'vuex';
import TableComponent from "../components/TableComponent";
export default {
  name: 'Home',
  components: {
    TableComponent,
  },
  data() {
    return {
      searchText: '',
    }
  },
  watch: {
    searchText: debounce( function (newVal) {
      this.$store.dispatch('searchMovie', newVal);
    }, 500)
  },
  computed: {
    ...mapState(['searchMovies'])
  }
}
</script>
