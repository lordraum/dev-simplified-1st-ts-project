# HOW TO BUILD YOUR FIRST TS PTOJECT - DEV SIMPLIFIED

## Basic setup

```bash
pnpm i typescript -D
pnpm tsc --init (npx) 
```

Esto crea un archivo `tsconfig` con todas las opciones de compilación de ts.

Crear carpeta SRC para detectar cambios en archivo js.

Elegir carpeta diferente --> tsconfig --> `"outDir": "./folder"`

## Setup with bundler (template)

`pnpx create-snowpack-app . --template @snowpack/app-template-blank-typescript`

## DOM Element types

```typescript
const form = document.getElementById('new-task-form') as HTMLFormElement | null
const input = document.querySelector<HTMLInputElement>('#new-task-title') // No funciona con getElementById
```

## 3rd party Modules @types

Muchas librerías tienen la opción de instalar los tipos

`npm i --save-dev @types/uuid`

## Solución error null | string al parsear JSON

```typescript
const loadTasks = (): Task[] => {
  const taskJSON = localStorage.getItem('TASKS')
  if (taskJSON == null) return []
  return JSON.parse(taskJSON) 
}
```




