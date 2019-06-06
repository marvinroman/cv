---
title: "Company API"
---

Built a custom company API for lead generation companies and the companies web-site to push new leads into companies CRM.
#### Built with the following technologies
* Slim Framework API Endpoint w/Api-Key authentication
* Slim Framework administration panel to create new authorized API consumers.
* Google Pub/Sub for dispatching to to CRM api workers.
* Google Pub/Sub monitoring to ensure that stale staff are notified of stale queue's.
* Google Logging with hash fingerprints from submission to worker import verification.
* CRM worker that does final import into the customer's CRM through XML API.
* API endpoint, API administration portal, CRM worker all run on dockers in Kubernetes cluster.