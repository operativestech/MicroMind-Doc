---
description: Learn how to set up app-level access control for your aimicromindinstances
---

# App Level

***

App level authorization protects your aimicromindinstance by username and password. This protects your apps from being accessible by anyone when deployed online.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

## How to Set Username & Password

### Npm

1. Install AiMicromind     

```bash
npm install -g aimicromind     
```

2. Start aimicromindwith username & password

```bash
npx aimicromind start --AIMICROMIND_USERNAME=user --AIMICROMIND_PASSWORD=1234
```

3. Open [http://localhost:3000](http://localhost:3000)

### Docker

1. Navigate to `docker` folder

```
cd docker
```

2. Create `.env` file and specify the `PORT`, `AIMICROMIND     _USERNAME`, and `AIMICROMIND     _PASSWORD`

```sh
PORT=3000
AIMICROMIND_USERNAME=user
AIMICROMIND_PASSWORD=1234
```

3. Pass `AIMICROMIND     _USERNAME` and `AIMICROMIND     _PASSWORD` to the `docker-compose.yml` file:

```
environment:
    - PORT=${PORT}
    - AIMICROMIND_USERNAME=${AIMICROMIND_USERNAME}
    - AIMICROMIND_PASSWORD=${AIMICROMIND_PASSWORD}
```

4. `docker compose up -d`
5. Open [http://localhost:3000](http://localhost:3000)
6. You can bring the containers down by `docker compose stop`

### Git clone

To enable app level authentication, add `AIMICROMIND     _USERNAME` and `AIMICROMIND     _PASSWORD` to the `.env` file in `packages/server`:

```
AIMICROMIND_USERNAME=user
AIMICROMIND_PASSWORD=1234
```
