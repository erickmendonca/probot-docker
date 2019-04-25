# probot-docker
Build and run your [probot-based](https://github.com/probot/probot) GitHub App on a docker container.

## Usage

Copy `Dockerfile` and `.dockerignore` to your repo's root.

### Build your image:

```sh
docker build -t probot-alpine .
```

### Run your container:

```sh
docker run -p 0.0.0.0:3000:3000 probot-alpine
```

### Warning

This script will copy your `.env` file to the image. [This file contains secrets](https://probot.github.io/docs/deployment/#deploy-the-app) that shouldn't be shared.
