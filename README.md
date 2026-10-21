# nt548-manifest-repo

Config Repo (GitOps) cua Nhom 8 – NT548. ArgoCD dong bo repo nay xuong cum GKE `nt548-cluster`.

| Thu muc | Noi dung | Phu trach |
| --- | --- | --- |
| `platform/namespaces/` | ResourceQuota, LimitRange cho `staging`, `prod` | An |
| `platform/gateway/` | Gateway `boutique-gw` (IP `boutique-ip`, TLS Cloudflare Origin) | An |
| `platform/kyverno/` | Chinh sach registry: Audit o staging, Enforce o prod (buoc 7.1) | An |
| `base/`, `overlays/staging`, `overlays/prod` | Manifest Online Boutique (Kustomize) | Nhat |

Ten mien: `nhom8.hocmang.io.vn` (prod), `nhom8-staging.hocmang.io.vn` (staging).
Image: `asia-southeast1-docker.pkg.dev/project-d833ce9b-518c-4957-bad/app/<service>`.

Secret `cloudflare-origin-cert` (namespace `gateway-infra`) tao bang tay, KHONG nam trong repo.
