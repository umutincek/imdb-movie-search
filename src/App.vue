<template>
  <div id="app">
    <Navbar />
    <Loading v-if="$store.state.isLoading" />
    <router-view/>
  </div>
</template>

<script>
  import Vue from 'vue';
  import Navbar from "./components/Navbar";
  import Loading from "./components/Loading";

  export default {
    components: { Navbar, Loading },
    created() {
      window.vueInstance = this;
    }
  }
</script>
