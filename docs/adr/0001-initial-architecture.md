# ADR-0001: Initial VPS Deployment Architecture

## Status
Accepted

## Context
VM Azure Standard B2ats v2 dengan RAM 1 GiB, Ubuntu Server 24.04, public IPv4.

## Decision
- Flask sebagai aplikasi web
- Gunicorn dengan 1 worker dan 2 thread sebagai application server
- systemd untuk mengelola proses
- Caddy sebagai reverse proxy
- UFW dan NSG Azure sebagai firewall
- GitHub sebagai repository

## Alternatives
1. Node.js + PM2
2. NGINX + Gunicorn
3. Docker
4. PHP-FPM

## Rationale
- Python 3.12 sudah tersedia di Ubuntu 24.04.
- Konfigurasi Caddy singkat dan siap dikembangkan ke HTTPS otomatis.
- Satu worker menjaga memori tetap lega pada RAM 1 GiB.
- Docker belum dipakai karena containerization dibahas pada pertemuan berikutnya.

## Consequences
### Positive
- Stack ringan dan mudah dipahami.
- Backend tidak terekspos langsung ke internet.
### Negative
- Hanya satu VM, tanpa redundansi.
- Deployment masih manual.

## Review Trigger
Tinjau ulang pada M06 dan M07.
