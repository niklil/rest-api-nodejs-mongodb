# Container quickstart

This pull request adds a ready-to-build container scaffold.

* **Base image**: `public.ecr.aws/docker/library/node:20-alpine`
* **Expose port**: `3000`
* **Start command**: `["npm", "start"]`

Update the Dockerfile to reflect the real application entrypoint and runtime dependencies, then run:

```bash
docker compose -f container/docker-compose.yml up --build
```

Push images to ECR with the Terraform outputs after deployment.
