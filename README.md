# 🎬 MovieTrack - React Movie Discovery App

Una aplicación interactiva desarrollada en React para buscar películas, ver detalles en tiempo real y gestionar una lista personal de películas vistas con calificaciones.

![Project Screenshot](ruta-a-tu-screenshot.png) 
*(Nota: ¡Sube una captura de pantalla de tu app y pon la ruta aquí!)*

## 🚀 Descripción

Este proyecto fue construido para demostrar el dominio de los fundamentos de **React**, el manejo de **efectos secundarios complejos** y la persistencia de datos en el navegador. La aplicación consume la API de OMDb para obtener datos en tiempo real y ofrece una experiencia de usuario fluida y persistente.

## 🛠 Tech Stack & Herramientas

* **Core:** React (Hooks, Component Architecture)
* **Estilos:** CSS3
* **API:** OMDb API (Asynchronous Data Fetching)
* **Persistencia:** LocalStorage API

## 💡 Habilidades Técnicas Demostradas

Este proyecto no es solo una interfaz bonita; implementa patrones de diseño y optimizaciones clave:

### 1. Gestión Avanzada de Estado (State Management)
* Uso de **Controlled Components** para formularios y búsqueda.
* Levantamiento de estado (Lifting State Up) para compartir datos entre componentes hermanos.

### 2. Ciclo de Vida y Efectos (`useEffect`)
* Sincronización de datos con la API externa.
* **Limpieza de Efectos (Cleanup Functions):** Implementación de `AbortController` para cancelar peticiones HTTP obsoletas cuando el usuario escribe rápido (evita *Race Conditions*).
* Manejo de listeners del DOM (ej. cerrar modales con la tecla `Escape`) y su correcta eliminación para evitar fugas de memoria.

### 3. Persistencia de Datos y Optimización
* **LocalStorage con Lazy Initial State:**
    * Implementación de persistencia para mantener la lista de "Vistas" tras recargar.
    * Optimización de rendimiento pasando una *función callback* al `useState` para leer del disco solo en el renderizado inicial (Lazy Initialization), evitando lecturas costosas en cada re-render.

### 4. Custom Hooks
* Creación de hooks personalizados (ej. `useFetchMovies`) para abstraer la lógica de negocio y mantener los componentes de UI limpios y reutilizables.

## ⚙️ Instalación y Uso

1.  **Clonar el repositorio**
    ```bash
    git clone [https://github.com/TU_USUARIO/nombre-repo.git](https://github.com/TU_USUARIO/nombre-repo.git)
    ```

2.  **Instalar dependencias**
    ```bash
    npm install
    ```

3.  **Configuración**
    Obtén una API Key gratuita en [OMDb API](http://www.omdbapi.com/) y agrégala a tu archivo de constantes o variables de entorno.

4.  **Correr el proyecto**
    ```bash
    npm run dev
    ```

## 🔮 Futuras Mejoras

* Implementación de `useReducer` para estados más complejos.
* Migración a TypeScript para mayor seguridad de tipos.
* Tests unitarios con React Testing Library.

---
