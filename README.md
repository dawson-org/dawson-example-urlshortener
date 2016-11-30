# dawson-example-urlshortener
A proof-of-concept of a serverless URL shortener built with [dawson](https://github.com/dawson-org/dawson-cli).

## Deploy

```bash
export AWS_REGION=us-east-1
export AWS_PROFILE=xxx # or AWS_ACCESS_KEY_ID, SECRET_ACCESS_KEY
yarn # or npm install
dawson deploy
```
Since you're deploying a CloudFront distribution, the first deploy will take about 20 minutes. Subsequent deploys will take about 1-2 minutes.


## What's next?

After the first deploy, you can locally run your functions, using the dev proxy with auto reloading:
```bash
dawson dev --port 3000
```

and tail Lambda logs:
```bash
dawson log -f functionName -t
```
