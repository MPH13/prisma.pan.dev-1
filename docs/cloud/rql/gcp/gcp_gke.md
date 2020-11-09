---
id: gcp_gke
title: Kubernetes Engine
sidebar_label: GKE
description: GCP Kubernetes Engine Queries
---

# Sample RQL Queries

:::note
The following guide will walk you through GCP Kubernetes Engine RQL Examples
:::

## List Kubernetes Clusters which have "Automatic node repair" disabled 

```bash
config where api.name = 'gcloud-container-describe-clusters' AND json.rule = 'nodePools[*].management.autoRepair does not exist or nodePools[*].management.autoRepair any equal false'
```