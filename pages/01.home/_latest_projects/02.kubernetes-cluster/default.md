---
title: "Kubernetes Cluster"
summary: "Migrated all companies web properties and software from Microsoft Server to Kubernetes cluster."
---

#### Workflow
* Migrated all sites to their own Docker container to minimize capability of cross site contamination, allow for individual site scaling, individual site php profiles & versions that match the software.
* Used NFS server & Volume Claims to allow multi-container read-write to shared directories.
* Used Fastcgi caching to allow for acceleration of site delivery and minimize the need for scaling.
* Used PageSpeed to minimize the site footprint and improve site's speed score.
* Used Let's Encrypt for quick multisite SSL generation and renewal.
* NGINX ingress load balancer across all web properties and SSL termination.
* Kubernetes cron jobs that do periodic API queries and data updates.
* Used node selectors to run low priority jobs and development to happen on "preemptable" low cost nodes.
* Used NGINX to mask administration portals with 404 pages outside of authorized IP ranges.

#### Skills used
NFS Implementation, Bash Scripting, YAML, Let's Encrypt, NGINX, Docker, Kubernetes, Google Cloud Platform