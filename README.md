# Base_Node.js
Proyecto educativo basico para node y express

Inicializar el proyecto:

# 1.- Crear package.json:

```bash
npm init -y 
```

# 2.- Instalaciones:

```bash
npm i -D typescript tsx @types/node pkgroll
```
typescript: lenguaje en que se va a trabajar .ts
tsx: Forma moderna para trabajar con typescript
@types/node: node
pkgroll: para llevar este producto a producción.

# 3.- Formato de Directorio de trabajo:

```ts
.
├── dist
├── node_modules
├── src
│   └── index.ts
├── package.json
└── tsconfig.json
└── .gitignore
```
Se pueden crear las carpetas en el directorio o con la terminal:

Crear las carpetas dist y scr 
```bash
mkdir dist
```
```bash
mkdir scr
```
Creacion del archivo index.ts en la carpeta src

```bash
touch scr/index.ts
```

# 4.- Crear archivo tsconfig.json:

Se puede crear como un documento normal 
nombre: "tsconfig.json" o con el siguiente comando en la terminal: 

```bash
touch tsconfig.json
```

# 4.1.- Configuración de tsconfig.json:

```ts
{
    "compilerOptions": {
      "target": "es2022",
      "strict": true,
      "outDir": "./dist",
      "moduleDetection": "force",
      "module": "Preserve",
      "resolveJsonModule": true,
      "allowJs": true,
      "esModuleInterop": true,
      "isolatedModules": true
    }
  }
```

# 5.- Crear archivo .gitignore:

Agrega el archivo .gitignore para evitar subir los módulos de Node.js a tu repositorio.

Se puede crear como un documento normal 
nombre: ".gitignore" o con el siguiente comando en la terminal: 

```bash
touch .gitignore
```

# 5.1- Configuración de .gitignore:

```ts
node_modules
```

# 6.- Configuración en package.json:

package.json: debes agregar los scripts necesarios para compilar y ejecutar el proyecto. Además configurar el exports (donde terminarán los archivos compilados) y el type (para que Node.js pueda reconocer el módulo).

```ts
{
  "exports": "./dist/index.js",
  "type": "module",
  "scripts": {
    "dev": "tsx watch src/index.ts",
    "build": "pkgroll",
    "start": "node dist/index.js"
  },
  "devDependencies": {
    "@types/node": "^22.9.0",
    "pkgroll": "^2.5.1",
    "tsx": "^4.19.2",
    "typescript": "^5.6.3"
  }
}
```

# 7.- Instalacion de Express:

```bash
npm install express
```
no se debe pone -D por que esta dependencia si se necesita en producción.


# Comandos

run dev: ejecuta el proyecto en "developed mode" con el siguiente comando.
```bash
npm run dev
```

run build: compila el proyecto con el siguiente comando.
```bash
npm run build
```

run start: ejecuta el proyecto compilado con el siguiente comando.
```bash
npm run start
```

Con estas configuraciones ya puedes trabajar con Typescript, Node.js y Express.


# Fuentes:

https://nodejs.org/

https://bluuweb.dev/node-ts/tsx.html

https://expressjs.com/en/starter/installing.html