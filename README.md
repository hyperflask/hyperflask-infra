# Hyperflask-Deploy

**⚠️ This is a work in progress project which is not functionnal yet**

The infrastructure needed to independently host your Hyperflask projects.

This repository contains resources and scripts to create and manage servers to run containerized Hyperflask apps. The infrastructure is kept as simple and straighforward as possible with minimal operations needed.

This setup is meant to deploy apps on a single server. This stack can be run on cheap machines or VMs from any server/cloud providers.

 - Fully Open-Source stack that is 100% self-hostable if desired
 - Provision Ubuntu servers using [OpenTofu](https://opentofu.org/)
 - Configure them using [Ansible](https://www.ansible.com/)
 - [Docker](https://www.docker.com/)-based containers
 - [Traefik](https://traefik.io/) load balancer with HTTPS support using [Let's Encrypt](https://letsencrypt.org)
 - [Blue-green deployments](https://en.wikipedia.org/wiki/Blue%E2%80%93green_deployment)
 - Hardened host machines
 - Full monitoring & observability using [OpenTelemetry Collector](https://opentelemetry.io/docs/collector/)
 - [Litestream](https://litestream.io/) for realtime replication of SQLite
 - [Valkey](https://valkey.io/) for in-memory storage and queues
 - Privacy minded (GDPR compliant)

Note: Hyperflask-Deploy is pre-installed and configured when using the [Hyperflask-Start template](https://github.com/hyperflask/hyperflask-start).

## Usage

Add to your hyperflask projects:

    pip install hyperflask-deploy

This will add the `provision` and `deploy` command:

    hyperflask deploy