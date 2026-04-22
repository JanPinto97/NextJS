## Desplegament local amb Docker (Next.js)

Aquest projecte es pot executar localment dins d'un contenidor Docker.

### Requisits previs

- Docker instal·lat (Docker Desktop o Docker Engine).

### 1) Construir la imatge i executar el contenidor

```bash
docker build -t prova-nextjs .
docker run --rm prova-nextjs
```

Aquesta prova valida que la imatge es construeix correctament i que l'aplicació arrenca dins del contenidor.

### 2) Accedir des del navegador a `http://localhost:3000`

Per exposar el port del contenidor a la màquina local, executa:

```bash
docker run --rm -p 3000:3000 prova-nextjs
```

Després, obre:

- http://localhost:3000

### Variables d'entorn

L'aplicació pot necessitar variables d'entorn per a funcionalitats d'autenticació i base de dades.
Pots veure un exemple a `.env.example`.
