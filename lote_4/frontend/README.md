# Frontend – Sistema de Incidencias UCV Chiclayo

HTML + CSS + JavaScript (módulos ES). Sin frameworks ni compilación.

## Ejecutar
Los módulos ES requieren un servidor estático (no abrir con doble clic):

```bash
cd frontend
python -m http.server 5500
```
Abre http://localhost:5500

## Conectar con el backend
La URL de la API está en `js/config.js`:
```js
export const API_BASE_URL = "http://localhost:8000";
```
Cámbiala por la URL pública del backend al desplegar.

## Personalizar el login
- Logo oficial: `assets/logo-ucv.svg` o `assets/logo-ucv.png`
- Foto del laboratorio (panel izquierdo): `assets/fondo-laboratorio.jpg`

Si no existen, se usan un logo y una escena de respaldo.
