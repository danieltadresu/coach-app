<template>
  <section>
    FILTER
  </section>
  <section>
    <div class="controls">
      <button>Refresh</button>
      <router-link to="/register">Register as Coach</router-link>
    </div>
    <ul>
      <li v-for="coach in filteredCoaches" v-bind:key="coach.id">
        {{ coach.firstName }}
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  computed: {
    filteredCoaches() {
      return this.$store.getters['coaches/coaches'];
    }
  }
}
</script>
