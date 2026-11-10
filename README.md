# ChemicAI

Aplikasi web berbasis AI untuk menghasilkan dan menganalisis molekul kimia. Proyek capstone tim.

**Demo live:** https://chemic-ai.vercel.app

## Struktur

| Folder | Isi |
|---|---|
| `Frontend/` | Antarmuka web: React 19, Vite, Tailwind CSS, tsParticles |
| `Backend/backendChem/` | REST API: FastAPI, PostgreSQL, Alembic, autentikasi JWT |
| `machine-learning/` | Layanan generasi molekul dengan NVIDIA API |

## Menjalankan front-end

```bash
cd Frontend
npm install
npm run dev
```

Secara default front-end memakai backend di `https://backend-chem.vercel.app`. Untuk memakai backend lain, isi `VITE_API_BASE_URL` di `Frontend/.env`.

## Menjalankan backend

Backend membaca konfigurasi dari environment variable: `JWT_SECRET_KEY`, `POSTGRESQL_*`, `NVIDIA_API_KEY`, dan `BACKEND_CORS_ORIGINS`. Lihat `Backend/backendChem/core/config.py` dan `docker-compose.yml`.