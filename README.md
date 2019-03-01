# WalletConnect Push Server

## Environment Variables

The following environment variables should be set for the container:

* `LOG_FILE` - Log file path, does not log to file by default.
* `LOG_LEVEL` - Log level for console and file, default: `info`. Supports `fatal`, `error`, `warn`, `info`, `debug`, `trace` or `silent`.
* `REDIS_URL` - Redis connection URL, default `redis://localhost:6379/0`
* `REDIS_PREFIX` - Redis key prefix, default `wc-push`
* `FCM_API_URL` - Firebase Cloud Messaging API URL, default `https://fcm.googleapis.com/fcm/send`
* `FCM_API_KEY` - Firebase Cloud Messaging API server key

## Develop

```bash
yarn dev
```

## Test

```bash
yarn test
```

## Build

```bash
yarn build
```

## Run

```bash
yarn start
```
