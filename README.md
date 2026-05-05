# Trident Protect Helm Test Charts

Test Helm repository for Trident Protect upgrade testing.

## Usage

```bash
helm repo add trident-protect-test https://sachinrai28.github.io/trident-protect-helm-test/charts
helm repo update
helm search repo trident-protect-test --versions
```

## Available Charts

| Chart | Version | App Version |
|-------|---------|-------------|
| trident-protect | 100.2605.0 | 26.05.0 |
| trident-protect | 100.2604.0 | 26.04.0 |

## Test Upgrade

```bash
# Install old version first
helm install trident-protect trident-protect-test/trident-protect --version 100.2604.0 -n trident-protect --create-namespace

# Upgrade to new version
helm upgrade trident-protect trident-protect-test/trident-protect --version 100.2605.0 -n trident-protect
```
