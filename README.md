[Ondrej Sika (sika.io)](https://sika.io) | <ondrej@sika.io>

# kcd2026-kargo-workshop

## What is Kargo?

[Kargo](https://kargo.io) is an open-source continuous promotion framework for Kubernetes, built by Akuity. It models your software delivery pipeline as a sequence of **Stages** (e.g. dev → staging → production), each pinned to specific artifact versions called **Freights**. Kargo tracks where each Freight is, automates its promotion through the pipeline, and enforces approval gates — giving teams safe, auditable, GitOps-native progressive delivery without hand-rolled shell scripts.

- <https://kargo.io>
- <https://github.com/akuity/kargo>
- <https://docs.kargo.io/>

## Kargo Components

<https://docs.kargo.io/user-guide/core-concepts>

### Project

Top-level namespace that groups all Kargo resources for a single application or team.

### Warehouse

Watches artifact sources (container registries, Helm chart repos, Git repos) and packages new versions as Freight.

### Freight

An immutable, versioned bundle of artifact references (image tag, chart version, Git commit) ready to be promoted.

### Stage

A deployment target (e.g. dev, staging, prod) that tracks which Freight is current and defines promotion criteria.

### Promotion

A record of moving a specific Freight into a Stage; Kargo creates one automatically or on manual approval.
