# Conductor Release

This repository is used to build and publish a Docker image from the [Conductor](https://github.com/conductor-oss/conductor) repository. 

## Purpose

The Conductor project does not provide a public Docker image, so this repository automates the process of building and publishing the Docker image to GitHub Container Registry.

## Workflow

The GitHub Actions workflow defined in this repository performs the following steps:
1. Logs in to the GitHub Container Registry.
2. Extracts metadata for the Docker image.
3. Finds the latest tag from the Conductor repository.
4. Checks out the Conductor repository at the latest tag.
5. Builds and pushes the Docker image to the GitHub Container Registry.

## Usage

To trigger the workflow manually, navigate to the Actions tab in GitHub and select the "Create and publish a Docker image" workflow, then click "Run workflow".

## Docker Image

The Docker image is published to the GitHub Container Registry and can be pulled using the following command:

```sh
docker pull ghcr.io/bacon-factory/conductor-oss:latest
```