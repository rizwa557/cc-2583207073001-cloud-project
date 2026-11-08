# Requirements

## Problem Statement
Warga kesulitan menukar atau menjual makanan dan barang berlebih kepada tetangga sekitar.
Sistem menyediakan daftar penawaran jual, beli, dan tukar sehingga barang yang tidak terpakai dapat berpindah dengan mudah.

## Target Users
- Warga penawar: ingin menjual atau menukar makanan dan barang yang tidak terpakai.
- Warga pencari: ingin membeli atau menukar kebutuhan dari tetangga sekitar.

## Functional Requirements
- FR-01 Sistem menampilkan halaman utama.
- FR-02 Sistem menyediakan health endpoint.
- FR-03 Sistem menampilkan metadata aplikasi.
- FR-04 Sistem menampilkan daftar penawaran jual, beli, dan tukar (direncanakan setelah data persisten, M05).

## Non-Functional Requirements
- NFR-01 Backend hanya listen pada loopback.
- NFR-02 Aplikasi dikelola systemd.
- NFR-03 Request publik masuk melalui reverse proxy.
- NFR-04 Secret tidak disimpan pada Git repository.
- NFR-05 Health endpoint mengembalikan HTTP 200 saat sehat.
- NFR-06 Deployment dapat direproduksi dari repository.
- NFR-07 Arsitektur sesuai VM dengan RAM 1 GiB.

## Scope
In scope M03: repository, requirements, architecture, ADR, aplikasi Flask dasar, hardening SSH, Gunicorn, systemd, Caddy, deployment HTTP publik.
Out of scope M03: database, Docker, Infrastructure as Code, CI/CD, domain dan HTTPS, monitoring penuh.

## Constraints
- Microsoft Azure VM Standard B2ats v2 (RAM 1 GiB)
- Ubuntu Server 24.04
- Public IPv4 static

## Acceptance Criteria M03
- [ ] Aplikasi dapat dibuka dari internet lewat http://4.217.184.141/
- [ ] Endpoint /health mengembalikan HTTP 200
