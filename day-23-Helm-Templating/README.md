# Helm Templating with values.yaml

This project demonstrates Helm templating and environment-specific configuration
using multiple values.yaml files.

## Environments
- Default
- Development
- Production

## Features
- Helm templates
- values.yaml overrides
- Conditional resources
- Environment-based deployments

## Usage
```bash
helm install dev . -f values-dev.yaml
helm install prod . -f values-prod.yaml
