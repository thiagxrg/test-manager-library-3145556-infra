# test-manager-library-3145556-infra

Infraestructura de *Manager Library* (base de datos vacía + API).

## Uso

```bash
docker compose up --build
```

La base de datos inicia sin tablas hasta que se corran las migraciones:

```bash
docker compose exec api php artisan migrate --seed
```

Puntos de acceso:
- API: `http://localhost:8000/api/v1`
- PostgreSQL: `localhost:5432` (`library` / `library`)

> `ADMIN_PASSWORD` por defecto es `change-me` (override con variable de entorno). No dejar vacía.

## Estado

- T-17 parcial: API + Postgres funcionan con `docker compose up`.
- El servicio `app` se agrega cuando el frontend React exista (T-19).