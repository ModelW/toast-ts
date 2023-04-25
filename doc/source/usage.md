# Usage
This is a little guide to use `@model-w/Toast` inside a Nuxt3 component.
This guide is going to assume that you have followed the guide inside the [installation](installation.md).

## In a Vue template

### Button trigger

In this example, we trigger the Toast notification on button click.

```vue
<script setup lang="ts">
  const notify = () => {
    useNuxtApp().$toast.info("toastify success");
  };
</script>

<template>
  <div>
    <button @click="notify">Notify by click</button>
  </div>
</template>
```

If you want to see it running you 
can click on this [link](https://codesandbox.io/p/sandbox/modelw-toast-nuxt3-dmxmuc?file=%2Fpages%2Findex.vue).

### Auto trigger

In this example, we use `nextTick` from `@vue/runtime-core` to launch a Toast notification on page load.

```vue
<script setup lang="ts">
  import { nextTick } from "@vue/runtime-core";
  nextTick(() => {
    if (process.client) {
      useNuxtApp().$toast('notify after nextTick');
    }
  })
</script>

<template>
  <div>
    <button @click="notify">Notify by click</button>
  </div>
</template>
```
