# Barterin

Cloud Computing - PTI 2802
Pertemuan 3 - Project Inception

## Author
Rizwa Rahmatunnisa / 2583207073001 / PTI2A

## Problem
Warga kesulitan menukar atau menjual makanan dan barang berlebih kepada tetangga sekitar.
Sistem menyediakan daftar penawaran jual, beli, dan tukar sehingga barang yang tidak terpakai dapat berpindah dengan mudah.

## Target Users
- Warga penawar: ingin menjual atau menukar makanan dan barang yang tidak terpakai.
- Warga pencari: ingin membeli atau menukar kebutuhan dari tetangga sekitar.

## Features M03
- aplikasi dasar
- health endpoint
- deployment di VM Azure

## Architecture
Lihat docs/architecture.md.

## Infrastructure
- Microsoft Azure VM Standard B2ats v2
- Ubuntu Server 24.04
- Caddy dan Gunicorn

## Public Endpoint
http://4.217.184.141/

## Health Check
GET /health

## Deployment
Lihat docs/deployment.md.

## Security
- SSH hanya dengan key
- login root SSH dimatikan
- UFW aktif
- backend hanya listen pada loopback

## Current Limitations
- HTTP saja
- belum ada database persisten
- belum ada container
- deployment manual

## Roadmap
M04 DNS dan HTTPS, M05 Data, M06 Container, M07 IaC, M09 CI/CD
