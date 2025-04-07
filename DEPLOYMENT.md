# Guía de Despliegue - Extractor de Precios Salcobrand

Esta guía proporciona instrucciones detalladas para desplegar la aplicación Extractor de Precios Salcobrand en diferentes entornos.

## Requisitos Previos

- Node.js 18.x o superior
- npm 8.x o superior
- Git (opcional, para clonar el repositorio)

## Instalación Local

1. Descomprime el archivo ZIP del proyecto en tu directorio preferido
2. Abre una terminal y navega al directorio del proyecto:
   ```bash
   cd ruta/a/salcobrand-extractor
   ```
3. Instala las dependencias:
   ```bash
   npm install
   ```
4. Inicia el servidor de desarrollo:
   ```bash
   npm run dev
   ```
5. Abre tu navegador y visita `http://localhost:3000`

## Construcción para Producción

Para crear una versión optimizada para producción:

1. Construye la aplicación:
   ```bash
   npm run build
   ```
2. Inicia el servidor de producción:
   ```bash
   npm start
   ```

## Despliegue en Vercel

La forma más sencilla de desplegar esta aplicación es utilizando Vercel:

1. Crea una cuenta en [Vercel](https://vercel.com) si aún no tienes una
2. Instala la CLI de Vercel:
   ```bash
   npm install -g vercel
   ```
3. Inicia sesión en Vercel:
   ```bash
   vercel login
   ```
4. Despliega la aplicación:
   ```bash
   vercel
   ```

## Despliegue en Netlify

También puedes desplegar la aplicación en Netlify:

1. Crea una cuenta en [Netlify](https://netlify.com) si aún no tienes una
2. Instala la CLI de Netlify:
   ```bash
   npm install -g netlify-cli
   ```
3. Inicia sesión en Netlify:
   ```bash
   netlify login
   ```
4. Construye la aplicación:
   ```bash
   npm run build
   ```
5. Despliega la aplicación:
   ```bash
   netlify deploy --prod
   ```

## Despliegue en Cloudflare Pages

Para desplegar en Cloudflare Pages:

1. Crea una cuenta en [Cloudflare](https://cloudflare.com) si aún no tienes una
2. Instala Wrangler:
   ```bash
   npm install -g wrangler
   ```
3. Inicia sesión en Cloudflare:
   ```bash
   wrangler login
   ```
4. Construye la aplicación:
   ```bash
   npm run build
   ```
5. Despliega la aplicación:
   ```bash
   wrangler pages deploy .next
   ```

## Variables de Entorno

Si necesitas configurar variables de entorno, crea un archivo `.env.local` en la raíz del proyecto con el siguiente contenido:

```
# Ejemplo de variables de entorno
NEXT_PUBLIC_API_URL=https://tu-api.com
```

## Solución de Problemas

Si encuentras problemas durante la instalación o el despliegue:

1. Asegúrate de tener las versiones correctas de Node.js y npm
2. Limpia la caché de npm:
   ```bash
   npm cache clean --force
   ```
3. Elimina la carpeta `node_modules` y el archivo `package-lock.json`:
   ```bash
   rm -rf node_modules package-lock.json
   ```
4. Reinstala las dependencias:
   ```bash
   npm install
   ```

## Soporte

Si necesitas ayuda adicional, consulta la documentación o contacta al equipo de soporte.
