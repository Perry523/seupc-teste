<template>
  <b-card
    style="max-width: 768px"
    class="no-border-on-mobile shadow-on-desktop"
  >
    <b-card-title class="h6"
      >{{ client.name }} / {{ client.phone }} / {{ client.email }}</b-card-title
    >
    <b-card-text class="d-flex my-2">
      <b-badge v-for="(tag, j) in client.tags" :key="j" class="mx-1" w pill>{{
        tag
      }}</b-badge>
    </b-card-text>
    <b-card-text v-for="(suggestion, j) in client.suggestions" :key="j" class="mb-1">
      <b>Sugestão {{ j }}</b
      >: {{ suggestion }}
    </b-card-text>
  </b-card>
</template>

<script>
export default {
  props: {
    client: {
      type: Object,
      default: () => {},
    },
  },
}
</script>

<style>
</style>