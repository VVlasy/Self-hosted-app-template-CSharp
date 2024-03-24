# Self-hosted-app-template-CSharp

## Docker Configuration

This application can be run in a Docker container. Here are the environment variables that need to be set for the Docker container:

- `DOCKER_REGISTRY`: This environment variable is used to specify the Docker registry that should be used for pulling the Docker images. For example, if you are using Docker Hub, you would set this to `docker.io/`.

- `DOCKER_REGISTRY_SUFFIX`: This environment variable is used in conjunction with `DOCKER_REGISTRY` to specify the tag of the Docker image. For example, if you want to use the latest version of the image, you would set this to `:latest`. If you want to use the main version, you would set this to `:main`.

- `NETWORK`: This environment variable is used to specify the Docker network that the containers should connect to. If you are running multiple containers that need to communicate with each other, they should be connected to the same Docker network.

You can set these environment variables in a `.env` file and use Docker's `--env-file` option to pass them to the container, like so:

```bash
docker run --env-file .env your-image-name