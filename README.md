# Epsagon AWS Lambda Extension

This repository contains an example of how to use the new [Epsagon extension for AWS Lambda runtime](https://epsagon.com/development/aws-lambda-extension/).

With the release of the new extension, Epsagon enables developers to reduce the overhead of distributed tracing and improve performance while still gaining full visibility into their serverless application.

## Getting Started

To integrate Epsagon's Lambda extension, follow these steps:
1. [Install Epsagon's SDK](https://docs.epsagon.com/docs/nodejs-aws-lambda). This example installs it using Epsagon's [Serverless Plugin](https://github.com/epsagon/serverless-plugin-epsagon).
2. Include Epsagon's extension layer in your Lambda (see [serverless.yml](./serverless.yml) for an example)
3. Configure the SDK to use the extension. this is done by adding the following code at the top of your handler:
```javascript
const epsagon = require('epsagon')
epsagon.init({ useLocalCollector: true })
```

And that's it! You are good to go with zero latency observability
