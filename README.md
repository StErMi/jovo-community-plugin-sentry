# jovo-community-plugin-sentry

[![NPM](https://nodei.co/npm/jovo-community-plugin-sentry.png)](https://nodei.co/npm/jovo-community-plugin-sentry/)

![Node CI](https://github.com/jovo-community/jovo-community-plugin-sentry/workflows/Build/badge.svg)

## Overview
This plugin for the [Jovo Framework](https://github.com/jovotech/jovo-framework) allows you to easily add error monitoring with [Sentry](https://sentry.io) to your voice projects.

## Platforms
The following platforms are supported:
* Amazon Alexa
* Google Assistant
* Samsung Bixby
* Twilio Autopilot

## Install
Install the plugin into your Jovo project:

`npm install jovo-community-plugin-sentry --save`

Use the plugin in:

app.js:
```javascript
const { SentryPlugin } = require('jovo-community-plugin-sentry');


app.use(
    // ... base imports
    new SentryPlugin()
);
```


app.ts:
```typescript
import { SentryPlugin } from 'jovo-community-plugin-sentry';

app.use(
    // ... base imports
    new SentryPlugin()
);
```

## Configuration

Refer to the Sentry documentation on [Configuration](https://docs.sentry.io/error-reporting/configuration/?platform=node).

Supported configuration values:
- dsn
- debug
- release
- environment
- maxBreadcrumbs
- sampleRate
- attachStacktrace
- serverName

config.js or config.ts:
```javascript
    SentryPlugin: {
        dsn: 'https://sample@sentry.io/0000000', // or set SENTRY_DSN
        environment: process.env.STAGE, //or set SENTRY_ENVIRONMENT
        debug: false,
        release: 'voice-app@1.0.0', //or set SENTRY_RELEASE
    },
```

# License

MIT