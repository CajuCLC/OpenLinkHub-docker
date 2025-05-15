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
  docker pull ghcr.io/cajuclc/openlinkhub-docker:v0.0.2
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

## Future Work

### To Do

- **GitHub Workflow/Action**: Set up a GitHub Action to automate Docker builds with the following command:
  ```bash
  docker build --build-arg GIT_TAG=0.1.3-beta -t openlinkhub .
  ```

This setup will ensure your Docker image is up-to-date with the latest OpenLinkHub releases and streamlines the management and deployment of the software.
