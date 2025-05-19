---
description: Aprende cómo configurar el control de acceso a nivel de aplicación para tus instancias de AiMicromind
---

# App Level

***

La app level authorization protege tu instancia de aimicromind mediante username y password. Esto protege tus apps de ser accesibles por cualquier persona cuando están deployed online.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

## How to Set Username & Password

### NPM

1. Install AiMicromind

```bash
npm install -g aimicromind
```

2. Start aimicromind con username y password

```bash
npx aimicromindstart --AIMICROMIND_USERNAME=user --AIMICROMIND_PASSWORD=1234
```

3. Open [http://localhost:3000](http://localhost:3000)

### Docker

1. Navigate a la carpeta `docker`

```
cd docker
```

2. Create un archivo `.env` y especifica el `PORT`, `AIMICROMIND_USERNAME`, y `AIMICROMIND_PASSWORD`

```sh
PORT=3000
AIMICROMIND_USERNAME=user
AIMICROMIND_PASSWORD=1234
```

3. Pass `AIMICROMIND_USERNAME` y `AIMICROMIND_PASSWORD` al archivo `docker-compose.yml`:

```
environment:
    - PORT=${PORT}
    - AIMICROMIND_USERNAME=${AIMICROMIND_USERNAME}
    - AIMICROMIND_PASSWORD=$AIMICROMIND_PASSWORD}
```

4. `docker compose up -d`
5. Open [http://localhost:3000](http://localhost:3000)
6. Puedes detener los containers usando `docker compose stop`

### Git clone

Para habilitar la app level authentication, add `AIMICROMIND_USERNAME` y `AIMICROMIND_PASSWORD` al archivo `.env` en `packages/server`:

```
AIMICROMIND_USERNAME=user
AIMICROMIND_PASSWORD=1234
```
