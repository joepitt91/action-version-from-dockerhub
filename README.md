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
| greater_equal_version | The minimum version to accept, e.g. 2.0.0. | No | None |
| less_than_version | The version to accept versions less than, e.g. 3.0.0. | No | None |

## Outputs

| Output | Description | Example |
|--------|-------------|---------|
| tag | The image tag for the latest version. | v2.5.3 |
| version | The latest version number. | 2.5.3 |

## Example

```yaml
      - name: Get Latest Nextcloud Version
        id: version
        uses: joepitt91/action-version-from-dockerhub@v2
        with:
          dockerhub_username: ${{ secrets.DOCKERHUB_USERNAME }}
          dockerhub_token: ${{ secrets.DOCKERHUB_TOKEN }}
          repository: nextcloud
```
