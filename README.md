# ModelW Toast

This module is intended to enable the Toast notifications in Nuxt3, showing them inside the pages.

### Installation
To install this module we need to get it from npm with the following command:
```commandline
npm install @model-w/toast
```
### Setup


After we need to add to the `nuxt.config.ts` file, the following param:
```typescript
    runtimeConfig: {
        public:
            {
                sentryDSN: process.env.SENTRY_DSN
            }
        }
```

With all these done the sentry must start to track the errors you have
