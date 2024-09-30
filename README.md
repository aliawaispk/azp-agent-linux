This project for creating docker image of Azure Pipelines Agent has been created using instructions available on [Microsoft Learn](https://learn.microsoft.com) article [Run a self-hosted agent in Docker](https://learn.microsoft.com/en-us/azure/devops/pipelines/agents/docker?view=azure-devops) specific to [Linux (Ubuntu)](https://learn.microsoft.com/en-us/azure/devops/pipelines/agents/docker?view=azure-devops#linux). The same instructions list down the steps to create the dockerfile.

Tags
---
- `latest`: Refers to the most recent docker image
- `2024-Apr-05_vuln_fixes`: To address vulnerabilities in the `2024-Apr-05` docker image, the docker file was updated to reflect the following changes:

<strike>

```docker
FROM ubuntu:22.04
```

</strike>

```docker
FROM ubuntu:24.10
```

<strike>

```docker
RUN apt install -y curl git jq libicu70
```

</strike>

```docker
RUN apt install -y curl git jq libicu74
```

- `2024-Apr-05`: Docker image of Azure Pipelines Agent corresponding to the instructions available in section [Linux](https://learn.microsoft.com/en-us/azure/devops/pipelines/agents/docker?view=azure-devops#linux) of the article revision dated 2024-Apr-05


Usage
---

To use the docker image generated using this project, follow the instructions available on the article section [Run a self-hosted agent in Docker](https://learn.microsoft.com/en-us/azure/devops/pipelines/agents/docker?view=azure-devops#start-the-image-1).
