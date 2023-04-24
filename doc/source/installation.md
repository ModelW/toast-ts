# Installation

In order to install the Model W Toast, you need to add it to the `package.json`, for example `"@model-w/toast": "~0.2.4"`,
or use the next command 
```commandline
npm install @model-w/toast
```

Then you can use it in your project modifying the `nuxt.config.ts` file. 
Here is a minimalistic example:

```typescript
export default defineNuxtConfig(
  {
    modules: [
        "@model-W/toast"
    ],
  }
)
```
When you have added it to this configuration, you are ready to use it.
