<script setup lang="ts">
  import { nextTick } from "@vue/runtime-core";
  import { useNuxtApp } from "#app";

  nextTick(() => {
    if (process.client) {
      useNuxtApp().$toast('notify after nextTick');
    }
  })
  const notify = () => {
    useNuxtApp().$toast.info('toastify success');
  }
</script>

<template>
  <div>
    <button @click="notify">Notify by click</button>
  </div>
</template>
