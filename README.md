# `replayio/action-wait-for-ghcr-image`

Poll ghcr.io for a container image to be available, and optional pull the container image for use by later steps in a workflow.

## Usage

```yaml
- uses: replayio/action-wait-for-ghcr-image@latest
  with:
    github-token: ${{ secrets.GITHUB_TOKEN }}
    github-username: ${{ secrets.GITHUB_ACTOR }}
    image-name: replayio/image-name:latest
```

## Arguments

| Required           | Name                | Description                                                                                | Default |
| ------------------ | ------------------- | ------------------------------------------------------------------------------------------ | ------- |
| :white_check_mark: | `github-token`      | GitHub personal access token for accessing ghcr.                                           |         |
| :white_check_mark: | `github-username`   | Owner of `github-token`                                                                    |         |
| :white_check_mark: | `image-name`        | The container image name to wait for and optionally pull.                                  |         |
| &nbsp;             | `timeout`           | The total amount of time (in minutes) alloted to both waiting and pulling                  | 15      |
| &nbsp;             | `sleep-time`        | The amount of time (in seconds) to sleep between attempts                                  | 30      |
| &nbsp;             | `cache-image`       | When true, the image will be pulled and cached for later use in the calling workflow       | false   |
