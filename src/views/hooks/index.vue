<template>
  <a-skeleton v-if="loading" />
  <div v-if="error">An Error occured, please try again</div>
  <div v-if="hasData">{{ data.text }}</div>
</template>

<script lang="ts">
import useFetchData from '../../hooks/use-fetch-data'
import { defineComponent } from 'vue'

export default defineComponent({
  setup() {
    return useFetchData()
  },
  created() {
    this.fetchData()
  }
})
</script>
