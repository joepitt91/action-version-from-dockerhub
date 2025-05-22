<!--
SPDX-FileCopyrightText: 2025 Joe Pitt

SPDX-License-Identifier: GPL-3.0-only
-->
# GitHub Action - Get Latest Version from DockerHub Image Tags

Get the latest semantic version number from a Docker Hub repository's tagged images

## Inputs

| Input | Description | Required | Default |
|-------|-------------|----------|---------|
| dockerhub_username | DockerHub username | Yes |  |
| dockerhub_token | Personal Access Token with read access to target repository | Yes |  |
| repository | The repository to look within. | Yes |  |
| namespace | The namespace containing the repository | No | library |
| minimum_version | The minimum version number to accept e.g. 2.0.0 | No |  |
| maximum_version | The maximum version number to accept e.g. 2.99.99 | No |  |

## Outputs

`version` containing the image tag representing the latest version.
