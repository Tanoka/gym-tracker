# Gym Tracker PWA

Esta es una aplicación web progresiva (PWA) diseñada para realizar el seguimiento de sesiones de gimnasio de forma local y eficiente.

## Características Principales

- **Funcionamiento Offline:** Al ser una PWA con Service Worker (`sw.js`), la aplicación puede funcionar sin conexión a internet.
- **Persistencia Local:** Utiliza **Dexie.js** (una envoltura para IndexedDB) para almacenar los datos directamente en el navegador del usuario.
- **Interfaz Adaptable:** Diseño "Mobile First" con soporte para modo oscuro.
- **Historial Detallado:** Permite visualizar y editar sesiones pasadas mediante un calendario integrado (**Flatpickr**).
- **Importación/Exportación:** Soporte para exportar e importar datos en formato CSV.

## Tecnologías Utilizadas

- **Frontend:** HTML5, CSS3 (Vanilla) y JavaScript (ES6+).
- **Base de Datos:** [Dexie.js](https://dexie.org/) para IndexedDB.
- **Calendario:** [Flatpickr](https://flatpickr.js.org/).
- **PWA:** Service Workers y Web App Manifest.

## Estructura del Proyecto

- `index.html`: Contiene toda la lógica de la interfaz, estilos CSS y el código JavaScript principal.
- `sw.js`: Service Worker que gestiona el cacheo de recursos para el modo offline.
- `manifest.json`: Configuración de la PWA (iconos, colores, nombre).
- `icon-192.png`: Icono de la aplicación.

## Convenciones de Desarrollo

- Mantener la lógica en un solo archivo (`index.html`) para simplicidad, a menos que la complejidad requiera modularización.
- Priorizar el uso de CSS nativo (Variables CSS).
- Asegurar que cualquier cambio en los recursos estáticos sea reflejado en la lista de `ASSETS` del `sw.js`.
