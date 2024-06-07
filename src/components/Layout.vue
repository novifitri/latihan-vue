<template>
  <Sidebar>
    <Navbar />
    <slot />
  </Sidebar>
</template>

<script>
import Navbar from './Navbar.vue'
import Sidebar from './Sidebar.vue'

export default {
  components: {
    Sidebar,
    Navbar,
  },
  setup() {
    return
  },
}
</script>
