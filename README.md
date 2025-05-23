<!--
SPDX-FileCopyrightText: 2025 Joe Pitt

SPDX-License-Identifier: GPL-3.0-only
-->
# GitHub Action - Get Latest Version from DockerHub Image Tags

Get the latest semantic version number from a Docker Hub repository's tagged images

## Inputs

| Input | Description | Required | Default |
|-------|-------------|----------|---------|
| dockerhub_username | The user to authenticate to the Docker Hub API as. | Yes |  |
| dockerhub_token | The token to authenticate to the Docker Hub API with (must have read access). | Yes |  |
| namespace | The namespace the repository is in. | No | library |
| repository | The repository to search tags for. | Yes |  |
| minimum_version | The minimum version number to accept, e.g. 2.0.0. | No | None |
| maximum_version | The maximum version number to accept, e.g. 2.99.99. | No | None |

## Outputs

`version` containing the image tag representing the latest version.
