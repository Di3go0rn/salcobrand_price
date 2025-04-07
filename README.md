# README - Extractor de Precios Salcobrand

## Descripción

Esta aplicación web permite extraer y analizar los precios de productos de Salcobrand, capturando correctamente los tres tipos de precios que existen en su sitio web:

- **Precio Internet**: El precio de venta en la web
- **Precio Tienda/Old**: El precio en tienda física
- **Precio SBPay**: El precio con descuento usando SBPay (cuando está disponible)

## Características Principales

- Extracción individual de productos
- Extracción masiva de múltiples productos
- Explorador de sitemap para encontrar productos
- Exportación de datos en formatos CSV y Excel
- Interfaz responsiva para dispositivos móviles y de escritorio
- Sistema de caché para mejorar el rendimiento

## Instalación Rápida

```bash
# Clonar el repositorio o descomprimir el archivo ZIP
cd salcobrand-extractor

# Instalar dependencias
npm install

# Iniciar servidor de desarrollo
npm run dev
```

Visita `http://localhost:3000` para ver la aplicación en funcionamiento.

## Documentación

Para información detallada sobre la aplicación, consulta los siguientes archivos:

- [DOCUMENTATION.md](./DOCUMENTATION.md) - Documentación completa de la aplicación
- [DEPLOYMENT.md](./DEPLOYMENT.md) - Guía de despliegue en diferentes entornos

## Pruebas

Para ejecutar las pruebas automatizadas:

```bash
npm test
```

## Licencia

Este proyecto es de uso privado y no está licenciado para distribución pública.
