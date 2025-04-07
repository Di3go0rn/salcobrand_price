# Documentación del Extractor de Precios Salcobrand

## Descripción General

El Extractor de Precios Salcobrand es una aplicación web desarrollada para extraer y analizar los precios de productos de la página web de Salcobrand. La aplicación captura correctamente los tres tipos de precios que existen en el sitio:

1. **Precio Internet**: El precio de venta en la web
2. **Precio Tienda/Old**: El precio en tienda física
3. **Precio SBPay**: El precio con descuento usando SBPay (cuando está disponible)

Además de los precios, la aplicación extrae información detallada como SKU, nombre del producto, marca, laboratorio y otras características relevantes.

## Características Principales

- **Extracción Individual**: Permite extraer información detallada de un producto específico
- **Extracción Masiva**: Permite extraer información de múltiples productos simultáneamente
- **Explorador de Sitemap**: Permite navegar por el sitemap de Salcobrand para encontrar productos
- **Exportación de Datos**: Permite exportar los datos extraídos en formatos CSV y Excel
- **Sistema de Caché**: Mejora el rendimiento almacenando temporalmente los datos extraídos
- **Interfaz Responsiva**: Funciona en dispositivos móviles y de escritorio

## Estructura del Proyecto

```
salcobrand-extractor/
├── src/
│   ├── app/
│   │   ├── api/
│   │   │   ├── extract/
│   │   │   │   └── [url]/
│   │   │   │       └── route.ts
│   │   │   ├── sitemap/
│   │   │   │   └── route.ts
│   │   │   └── export/
│   │   │       ├── csv/
│   │   │       │   └── route.ts
│   │   │       └── excel/
│   │   │           └── route.ts
│   │   ├── extract/
│   │   │   ├── single/
│   │   │   │   └── page.tsx
│   │   │   └── batch/
│   │   │       └── page.tsx
│   │   ├── sitemap/
│   │   │   └── page.tsx
│   │   ├── layout.tsx
│   │   └── page.tsx
│   ├── components/
│   │   └── ui/
│   ├── lib/
│   │   ├── extraction/
│   │   │   └── extractor.ts
│   │   └── cache.ts
├── tests/
│   ├── app.spec.ts
│   ├── api.spec.ts
│   └── integration.spec.ts
├── public/
├── package.json
├── README.md
└── DEPLOYMENT.md
```

## Tecnologías Utilizadas

- **Frontend**: Next.js, React, Tailwind CSS
- **Backend**: Next.js API Routes
- **Extracción de Datos**: Axios, Cheerio
- **Exportación**: XLSX
- **Pruebas**: Playwright
- **Despliegue**: Vercel, Netlify, Cloudflare Pages (opciones)

## Flujo de Trabajo

1. **Extracción Individual**:
   - El usuario ingresa la URL de un producto de Salcobrand
   - La aplicación extrae los datos del producto
   - Se muestran los resultados con los tres tipos de precios
   - El usuario puede exportar los datos en CSV o Excel

2. **Extracción Masiva**:
   - El usuario ingresa múltiples URLs o las obtiene desde el sitemap
   - La aplicación extrae los datos de todos los productos
   - Se muestran los resultados en una tabla
   - El usuario puede exportar todos los datos en CSV o Excel

3. **Explorador de Sitemap**:
   - La aplicación obtiene las URLs de productos desde el sitemap de Salcobrand
   - El usuario puede seleccionar qué productos desea analizar
   - La aplicación extrae los datos de los productos seleccionados
   - Se muestran los resultados y se pueden exportar

## Mejoras Implementadas

La aplicación web es una evolución del script original con las siguientes mejoras:

1. **Interfaz Gráfica**: Facilita la interacción y visualización de datos
2. **Extracción Precisa**: Captura correctamente los tres tipos de precios
3. **Procesamiento Masivo**: Permite extraer datos de múltiples productos
4. **Sistema de Caché**: Mejora el rendimiento y reduce la carga en el sitio de Salcobrand
5. **Exportación Flexible**: Permite exportar datos en diferentes formatos
6. **Pruebas Automatizadas**: Garantiza el correcto funcionamiento de la aplicación

## Limitaciones y Consideraciones

- La aplicación depende de la estructura actual del sitio web de Salcobrand. Si el sitio cambia significativamente, podría requerir actualizaciones.
- Se recomienda usar la aplicación con moderación para evitar sobrecargar el servidor de Salcobrand.
- El precio SBPay no está disponible para todos los productos, por lo que puede aparecer como "No disponible" en algunos casos.

## Próximos Pasos y Posibles Mejoras

- Implementar un sistema de monitoreo de precios a lo largo del tiempo
- Añadir gráficos para visualizar tendencias de precios
- Integrar con otras farmacias para comparación de precios
- Implementar notificaciones cuando los precios cambien

Para instrucciones detalladas sobre cómo desplegar la aplicación, consulta el archivo DEPLOYMENT.md.
