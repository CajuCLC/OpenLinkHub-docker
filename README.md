# OpenLinkHub Docker

This repository provides a Docker image for OpenLinkHub, enabling easy deployment and management.

## Pull the Docker Image

You can pull the Docker image from GitHub Container Registry:

- Latest version:
  ```bash
  docker pull ghcr.io/cajuclc/openlinkhub-docker:latest
  ```

- Specific version:
  ```bash
  docker pull ghcr.io/cajuclc/openlinkhub-docker:0.5.5
  ```

## Running the Docker Container

To run the OpenLinkHub container, you need to mount a configuration file. Make sure to replace `your_path/config.json` with the path to your own configuration file.

```bash
docker run --network host --privileged -v your_path/config.json:/opt/OpenLinkHub/config.json openlinkhub
```

### Important Path Information

Ensure you have created the `config.json` file in the path you provide. For detailed guidance on setting up this configuration file, please refer to the official OpenLinkHub documentation: [Configuration Instructions](https://github.com/jurkovic-nikola/OpenLinkHub/tree/main?tab=readme-ov-file#5-configuration).

## Source of OpenLinkHub

All information and the core application instructions can be found on the official OpenLinkHub repository:  
[OpenLinkHub GitHub Repository](https://github.com/jurkovic-nikola/OpenLinkHub/tree/main)

### Version Matching with GIT_TAG

The Docker build process now incorporates a `GIT_TAG` build argument, which aligns the Docker image version with the OpenLinkHub release version. This ensures consistency between the Docker image and the OpenLinkHub version it is based on. When you tag a new release, the `GIT_TAG` reflects this tag, and the Docker image is built using that specific version of OpenLinkHub, syncing both versions.
