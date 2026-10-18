# Backend – Sistema de Incidencias UCV Chiclayo

FastAPI + Python en capas (Controller → Service → Repository → Model) sobre SQL Server.

## Requisitos
- Python 3.11+
- ODBC Driver 17 (o 18) for SQL Server instalado en el sistema (solo si usarás SQL Server)

## Instalación y arranque
```bash
cd backend
python -m venv .venv
# Windows: .venv\Scripts\activate    |  Linux/Mac: source .venv/bin/activate
pip install -r requirements.txt
cp .env.example .env        # Windows: copy .env.example .env   (luego edítalo)
uvicorn app.main:app --reload --port 8000
```
- API: http://localhost:8000  ·  Documentación: http://localhost:8000/docs
- Si en `.env` no defines `DB_USER`/`DB_PASSWORD`/`DB_NAME`, el backend funciona con un almacén en memoria (los datos se pierden al reiniciar).

## Pruebas
```bash
python -m pytest tests/unit
```
