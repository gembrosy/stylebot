<template>
  <b-dropdown-item :disabled="disabled" @click="$emit('click')">
    {{ t('delete_style') }}
  </b-dropdown-item>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'TheDeleteStyleDropdownItem',

  computed: {
    disabled(): boolean {
      return this.$store.state.selectors.length === 0;
    },
  },
});
</script>
