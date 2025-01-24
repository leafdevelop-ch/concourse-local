# Concourse Local

## Prerequisites

- Docker
- Running on MacOS

## Getting started 

### Start concourse

```bash
docker compose up -d
```

#### Set up spring boot pipeline

```bash
fly -t tutorial set-pipeline -p springboot-starter-ci -c springboot-starter-ci.yml -v github-ssh-key="$(cat location/of/ssh/key)"
```
