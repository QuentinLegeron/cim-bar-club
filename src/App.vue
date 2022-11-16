<script lang="ts">
import Index from './components/pages/Index.vue'
import DevWeb from './components/pages/DevWeb.vue'
import CreaDesign from './components/pages/CreaDesign.vue'

const routes = {
  '/': Index,
  '/devweb': DevWeb,
  '/creadesign': CreaDesign,
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
  mounted() {
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