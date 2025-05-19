# Primeros Pasos

***

## Cloud

El alojamiento propio requiere más habilidades técnicas para configurar la instancia, respaldar la base de datos y mantener las actualizaciones. Si no tienes experiencia en la gestión de servidores y solo quieres usar la aplicación web, te recomendamos usar [AiMicronindCloud](https://chat.aimicromind.com/join).

## Inicio Rápido

{% hint style="info" %}
Requisito previo: asegúrate de que [NodeJS](https://nodejs.org/en/download) esté instalado en tu máquina. Se admiten las versiones Node `v18.15.0` o `v20` y superiores.
{% endhint %}

Instala aimicromind localmente usando NPM.

1. Instala AiMicromind:

```bash
npm install -g aimicromind
```

2. Inicia AiMicromind:

```bash
npx aimicromind start
```

3. Abre: [http://localhost:3000](http://localhost:3000)

***

## Docker

Hay dos formas de desplegar aimicromind con Docker:

### Docker Compose

1. Ve a la `carpeta docker` en la raíz del proyecto
2. Copia el archivo `.env.example` y pégalo como otro archivo llamado `.env`
3. Ejecuta:

```bash
docker compose up -d
```

4. Abre: [http://localhost:3000](http://localhost:3000)
5. Puedes detener los contenedores ejecutando:

```bash
docker compose stop
```

### Imagen Docker

1. Construye la imagen:

```bash
docker build --no-cache -t aimicromind.
```

2. Ejecuta la imagen:

```bash=
docker run -d --name aimicromind-p 3000:3000 aimicromind
```

3. Detén la imagen:

```bash
docker stop aimicromind
```

***

## Para Desarrolladores

AiMicromind tiene 3 módulos diferentes en un único monorepositorío:

* **Server**: Backend en Node para servir la lógica de la API
* **UI**: Frontend en React
* **Components**: Componentes de integración

### Requisito Previo

Instala [PNPM](https://pnpm.io/installation).

```bash
npm i -g pnpm
```

### Configuración 1

Configuración simple usando PNPM:

1. Clona el repositorio

```bash
git clone https://github.com/operativestech/AiMicroMind_Platform_2025.git
```

2. Ve a la carpeta del repositorio

```bash
cd AiMicromind
```

3. Instala todas las dependencias de todos los módulos:

```bash
pnpm install
```

4. Construye el código:

```bash
pnpm build
```

Inicia la aplicación en [http://localhost:3000](http://localhost:3000)

```bash
pnpm start
```

### Configuración 2

Configuración paso a paso para contribuidores del proyecto:

1. Haz un fork del [Repositorio oficial de aimicromind en Github](https://github.com/operativestech/AiMicroMind_Platform_2025)
2. Clona tu repositorio forkeado
3. Crea una nueva rama, consulta la [guía](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-and-deleting-branches-within-your-repository). Convenciones de nombres:
   * Para rama de funcionalidad: `feature/<Tu Nueva Funcionalidad>`
   * Para rama de corrección de errores: `bugfix/<Tu Nueva Corrección>`.
4. Cambia a la rama que acabas de crear
5. Ve a la carpeta del repositorio:

```bash
cd AiMicromind
```

6. Instala todas las dependencias de todos los módulos:

```bash
pnpm install
```

7. Construye el código:

```bash
pnpm build
```

8. Inicia la aplicación en [http://localhost:3000](http://localhost:3000)

```bash
pnpm start
```

9. Para construcción de desarrollo:

* Crea un archivo `.env` y especifica el `PORT` (consulta `.env.example`) en `packages/ui`
* Crea un archivo `.env` y especifica el `PORT` (consulta `.env.example`) en `packages/server`

```bash
pnpm dev
```

* Cualquier cambio realizado en `packages/ui` o `packages/server` se reflejará en [http://localhost:8080](http://localhost:8080/)
* Para los cambios realizados en `packages/components`, necesitarás construir nuevamente para incorporar los cambios
* Después de realizar todos los cambios, ejecuta:

```bash
pnpm build
```

y

```bash
pnpm start
```

para asegurarte de que todo funcione bien en producción.

***

## Para Empresas

Los planes empresariales tienen un repositorio e imagen de Docker separados.

Una vez concedido el acceso a ambos, la configuración es la misma que en [#configuración-1](./#setup-1 "mention"). Antes de iniciar la aplicación, los usuarios empresariales deben completar los valores de los Parámetros Empresariales en el archivo `.env`. Consulta `.env.example` para los cambios requeridos.

Contacta a support@aimicromind.com para obtener el valor de las siguientes variables de entorno:

```
LICENSE_URL
AIMICROMIND_EE_LICENSE_KEY
```

Para Instalación con Docker:

```bash
cd docker
cd enterprise
docker compose up -d
```

***

## Aprende Más

En este video tutorial, Leon proporciona una introducción a aimicromind y explica cómo configurarlo en tu máquina local.

The video tutorial for that coming soon

## Guía de la Comunidad

* [Introducción a \[Práctica\] Construcción de Aplicaciones LLM con aimicromind/ LangChain](https://volcano-ice-cd6.notion.site/Introduction-to-Practical-Building-LLM-Applications-with-AiMicromind-LangChain-03d6d75bfd20495d96dfdae964bea5a5)
* [aimicromind/ LangChainによるLLMアプリケーション構築\[実践\]入門](https://volcano-ice-cd6.notion.site/AiMicromind-LangChain-LLM-e106bb0f7e2241379aad8fa428ee064a)
