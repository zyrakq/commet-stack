# Commet Custom Image

Custom Docker image for Commet with dynamic configuration generation based on environment variables.

## Quick Start

Build the custom Commet image:

```bash
cd src/commet/image
docker build --build-arg RELEASE=v0.3.1+hotfix.1 -t commet .
docker tag commet localhost/commet
```
