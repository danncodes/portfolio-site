<template>
  <Navbar />
  <router-view />
</template>

<script>
import Navbar from "./components/Navbar.vue"
import Home from "./views/Home.vue"
export default {
  components: { Navbar, Home },
  data(){
    return {
    }
  },
  methods: {
  }
}
</script>