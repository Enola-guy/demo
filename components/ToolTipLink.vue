<template>
  <span>
    <NuxtLink
      v-for="node in path"
      :key="node.name"
      :to="{name: 'plop', params: { id: node.id } }"
      v-text="node.name"
    />
  </span>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({

  props: {
    path: {
      type: Array,
      required: true,
    },
  },
});
</script>