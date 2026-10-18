# Base de datos – SQL Server

Ejecuta los scripts **en orden** con SQL Server Management Studio (conectado como `sa` o un usuario con permiso para crear bases de datos):

| Orden | Script | Qué hace |
|---|---|---|
| 1 | `01_schema.sql` | Crea la base `sistema_incidencias_ucv` y las tablas (**borra las tablas si ya existen**) |
| 2 | `02_seed.sql` | Datos iniciales: administrador, un laboratorio y un equipo |
| 3 | `03_migracion.sql` | Ajustes idempotentes (SOFTWARE, subcategoría, calificaciones). Seguro de re-ejecutar |
| – | `04_limpiar_datos_prueba.sql` | Opcional: elimina datos de prueba |

Usuario inicial: `admin@ucv.edu.pe` / `Admin123` (**cámbiala** después del primer ingreso).

Estrategia de copias de respaldo: ver `README_respaldos.md`.
