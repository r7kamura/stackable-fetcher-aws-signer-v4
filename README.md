# stackable-fetcher-aws-signer-v4
A [stackable-fetcher](https://github.com/r7kamura/stackable-fetcher) middleware
for signing requests with AWS Signature v4.

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
