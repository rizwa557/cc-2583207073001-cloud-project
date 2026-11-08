# Architecture v0.1 - Barterin

## Deployment View

    Internet
       |
       v
    NSG Azure (port 22 dan 80)
       |
       v
    UFW (port 22 dan 80)
       |
       v
    Caddy :80
       |
       v
    Gunicorn 127.0.0.1:8000
       |
       v
    Flask

## Resource Constraints
- RAM 1 GiB (Azure Standard B2ats v2)
- Ubuntu Server 24.04

## Security Decisions
- administrasi memakai user non-root
- SSH hanya dengan key
- login password SSH dimatikan
- UFW aktif
- backend hanya listen pada loopback

## Current Limitations
- HTTP saja, belum HTTPS
- satu VM
- belum ada database
- belum ada container
- belum ada CI/CD

## Planned Evolution
- M04 DNS dan HTTPS
- M05 data persisten
- M06 container
- M07 Infrastructure as Code
- M09 CI/CD
