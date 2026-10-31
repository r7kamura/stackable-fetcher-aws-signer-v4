# stackable-fetcher-aws-signer-v4

> [!NOTE]
> This project is archived because I no longer actively use it, and there seems to be no recent activity from other users either. If you are still using it and would like to take over maintenance, please contact me somewhere.

A [stackable-fetcher](https://github.com/r7kamura/stackable-fetcher) middleware
for signing requests with AWS Signature v4.

## Install
```
npm install --save stackable-fetcher-aws-signer-v4
```

## Usage
```js
// Create a new Fetcher instance
var fetcher = new Fetcher();

// Build your middleware stack
fetcher.use(
  require('stackable-fetcher-aws-signer-v4'),
  {
    accessKeyId: '...',
    secretAccessKey: '...'
  }
)

// Send a signed request
fetcher
  .get('https://apigateway.us-east-1.amazonaws.com/restapis')
  .then(function (response) {
    // ... do your task
  });
```
