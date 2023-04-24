# Usage
This is a little guide to use `@model-w/Toast` inside a Nuxt3 component.
This guide is going to assume that you have followed the guide inside the [installation](installation.md).

## Usage in template
We can use Toast with the previous implementation, the example above show how to do it with a button.

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

Also, we can use `nextTick` from `@vue/runtime-core` 
to launch a Toast event to show helpful information, as the example above shows.
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
