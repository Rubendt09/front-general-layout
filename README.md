# Front General Layout

Plantilla general de frontend construida con **React + Vite + Material UI**. Sirve como base para proyectos que requieran un panel administrativo con autenticación, navegación lateral y tema personalizable.

## Stack

- **React 18** + **TypeScript**
- **Vite** (SWC) — bundler y dev server
- **Material UI (MUI)** — componentes y sistema de tema
- **React Router** — enrutamiento
- **ApexCharts** — gráficos
- **ESLint + Prettier** — linting y formato

## Requisitos

- Node.js 18+
- npm o yarn

## Instalación

```bash
npm install
# o
yarn install
```

## Comandos

| Comando           | Descripción                              |
| ----------------- | ---------------------------------------- |
| `npm run dev`     | Levanta el servidor de desarrollo        |
| `npm run build`   | Compila para producción (`tsc` + `vite`) |
| `npm run start`   | Previsualiza el build de producción      |
| `npm run lint`    | Ejecuta ESLint                           |
| `npm run lint:fix`| Corrige errores de lint automáticamente  |
| `npm run fm:check`| Verifica formato con Prettier            |
| `npm run fm:fix`  | Aplica formato con Prettier              |

## Estructura del proyecto

```
src/
├── app.tsx            # Componente raíz
├── main.tsx           # Punto de entrada
├── config-global.ts   # Configuración global
├── routes/            # Definición de rutas y hooks de navegación
├── layouts/           # Layouts (dashboard, auth) y config de navegación
├── pages/             # Páginas (lazy loaded)
├── sections/          # Vistas por sección (auth, dashboard, errores...)
├── components/        # Componentes reutilizables
├── theme/             # Tema de MUI (colores, tipografía, overrides)
├── hooks/             # Hooks personalizados
├── utils/             # Utilidades
└── _mock/             # Datos de prueba
```

## Rutas principales

- `/` — Login (página principal)
- `/dashboard` — Panel principal
- `/user`, `/products`, `/blog` — Secciones de ejemplo
- `/404` — Página no encontrada

## Personalización

- **Tema**: edita `src/theme/` para cambiar paleta, tipografía y estilos de componentes.
- **Navegación**: edita `src/layouts/nav-config-dashboard.tsx` para agregar o quitar ítems del menú lateral.
- **Rutas**: edita `src/routes/sections.tsx` para registrar nuevas páginas.
