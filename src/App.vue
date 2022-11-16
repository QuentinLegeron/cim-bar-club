<script lang="ts">
import Index from './components/pages/Index.vue'
import DevWeb from './components/pages/DevWeb.vue'
import CreaDesign from './components/pages/CreaDesign.vue'
import Communication from './components/pages/Communication.vue'

const routes = {
  '/': Index,
  '/devweb': DevWeb,
  '/creadesign': CreaDesign,
  '/communication': Communication
}

export default {
  data() {
    return {
      currentPath: window.location.hash
    }
  },
  computed: {
    currentView() {
      return routes[this.currentPath.slice(1) || '/']
    }
  },
  methods: {
    MusiqueInClub() {
      var audio = new Audio('https://www.youtube.com/watch?v=QH2-TGUlwu4');
      audio.play();
    },
  },
  mounted() {
    this.MusiqueInClub()
    window.addEventListener('hashchange', () => {
		  this.currentPath = window.location.hash
		})
  }
}
</script>

<template>
  <main>
    <component :is="currentView" />
  </main>
</template>

<style>
  * {
    overflow: hidden;
  }
</style>