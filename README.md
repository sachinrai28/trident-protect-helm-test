# Trident Protect Helm Test Charts

Test Helm repository for Trident Protect upgrade testing.

## Usage

```bash
helm repo add --force-update trident-protect-test https://sachinrai28.github.io/trident-protect-helm-test/charts
helm repo update
helm search repo trident-protect-test --versions
```

## Available Charts

| Chart | Version | App Version |
|-------|---------|-------------|
| trident-protect-console | 100.2605.0-console | 26.05.0-console |
| trident-protect-console | 100.2604.0-console | 26.04.0-console |

## Install/Upgrade

```bash
helm upgrade --install trident-protect \
trident-protect-test/trident-protect-console \
--version 100.2605.0-console \
--namespace trident-protect \
--create-namespace \
--set clusterName=<your-cluster-name> \
--set trident-protect.cbs.accountID=<account-id> \
--set trident-protect.cbs.agentID=<agent-id> \
--set trident-protect.cbs.proxySecretName=occmauthcreds \
--set trident-protect.cbs.proxyHostIP=<proxy-host>
```
