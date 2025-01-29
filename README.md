# Concourse Local

## Prerequisites

- Docker
- Running on MacOS

## Getting started 

### Start concourse

```bash
docker compose up -d
```

#### Set up spring boot build pipeline

```bash
fly -t tutorial set-pipeline -p springboot-starter-ci -c springboot-starter-ci.yml -v github-ssh-key="$(cat location/of/ssh/key)"
```

#### Set up spring boot pr pipeline

```bash
fly -t tutorial set-pipeline -p springboot-starter-pr -c springboot-starter-pr.yml -v webhook-token="$(cat location/of/webhook/token)" -v github-access-token="$(cat location/of/gh/access/token)"
```