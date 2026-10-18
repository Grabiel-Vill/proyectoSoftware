# Sistema de Incidencias de Laboratorio – UCV Chiclayo

Aplicación web para que docentes reporten fallas de laboratorio, los técnicos las atiendan y los administradores supervisen métricas y reportes.

```
├── backend/    API REST (FastAPI + Python)
├── frontend/   Interfaz web (HTML/CSS/JS)
├── database/   Scripts SQL Server
└── docs/       Arquitectura y changelog
```

## Puesta en marcha (3 pasos)

**1. Base de datos** – ejecuta en SQL Server los scripts de `database/` en orden (`01`, `02`, `03`). Ver [database/README.md](database/README.md).

**2. Backend**
```bash
cd backend
python -m venv .venv && .venv\Scripts\activate     # Linux/Mac: source .venv/bin/activate
pip install -r requirements.txt
copy .env.example .env                              # Linux/Mac: cp .env.example .env  -> edita tus credenciales
uvicorn app.main:app --reload --port 8000
```

**3. Frontend** (en otra terminal)
```bash
cd frontend
python -m http.server 5500
```
Abre http://localhost:5500 e ingresa con `admin@ucv.edu.pe` / `Admin123`.

> Sin SQL Server también puedes probar: deja vacías las credenciales de BD en `.env` y el backend usará memoria.

## Roles
- **Docente**: reporta incidencias, sigue su estado, califica la atención, usa el chatbot.
- **Técnico**: bandeja de tickets asignados, notas técnicas y evidencias.
- **Administrador**: dashboard, usuarios, laboratorios, incidencias y reportes.

## Seguridad antes de desplegar
Define un `JWT_SECRET` propio, `HTTPS_OBLIGATORIO=true`, restringe `CORS_ORIGENES_PERMITIDOS` y cambia la contraseña del administrador. **Nunca subas tu `.env`.**
