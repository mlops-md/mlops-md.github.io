---
layout: post
title:  "License To Deploy — from Jupyter to Prod"
date:   2025-10-27 12:00:00 +0200
categories: deployment mlops
---

**Mission brief:** Getting a model from exploration (Jupyter) into production is full of small traps. This mission report lists pragmatic steps and a minimal pipeline you can use tonight.

### TL;DR
- Track experiments (MLflow)
- Containerize the model (Docker)
- Use CI to build artifacts (GitHub Actions)
- Deploy on K8s / serverless depending on latency needs
- Add monitoring & alerts for drift and latency

### Minimal pipeline
1. Experiment tracking — log parameters, metrics, artifacts.
2. Model packaging — a predictable entrypoint (`predict()`), requirements, and a Dockerfile.
3. CI job — run tests, build image, push to registry.
4. Deployment — helm chart or k8s manifest, with readiness & liveness probes.
5. Observability — metrics, logs, and data quality checks.

_More mission reports incoming. Stay tuned, agent._ 😎
