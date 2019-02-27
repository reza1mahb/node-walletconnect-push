# WalletConnect Push Server

Push Server for triggering WalletConnect notifications

## Environment Variables

The following environment variables should be set for the container:

* `LOG_FILE` - Log file path, does not log to file by default.
* `LOG_LEVEL` - Log level for console and file, default: `info`. Supports `fatal`, `error`, `warn`, `info`, `debug`, `trace` or `silent`.
* `REDIS_URL` - Redis connection URL, default `redis://localhost:6379/0`
* `REDIS_PREFIX` - Redis key prefix, default `wc-push`
* `FCM_API_URL` - Firebase Cloud Messaging API URL, default `https://fcm.googleapis.com/fcm/send`
* `FCM_API_KEY` - Firebase Cloud Messaging API server key

## Development

```bash
yarn dev
```

## Production

### Using NPM

1. Build

```bash
yarn build
```

2. Production

```bash
yarn start
```

3. Server accessible from host:

```bash
http://localhost:5000/
```

### Using Docker

1. Build the container with:

```bash
make build-docker
```

2. Run the container with:

```bash
docker run -p 5000:5000 -e REDIS_URL=redis://192.168.1.53:6379/0 walletconnect/node-walletconnect-push
```

3. Server accessible from host:

```bash
http://localhost:5000/
```

