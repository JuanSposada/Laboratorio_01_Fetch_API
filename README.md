# 🧪 LABORATORIO 01 - APIS JAVASCRIPT: Uso de Fetch con Promesas

Este proyecto es la solución al primer laboratorio práctico enfocado en el consumo de APIs públicas utilizando la **Fetch API** de JavaScript, manejando las peticiones mediante el flujo de **Promesas** (`.then().catch()`).

El objetivo principal fue consolidar la comprensión del ciclo de vida de una petición HTTP (obtener datos, parsear JSON, manejar la respuesta y capturar errores) en un entorno de desarrollo web.

---

## 🎯 Objetivos de Aprendizaje

* Realizar peticiones **GET** a APIs externas utilizando `fetch()`.
* Manejar la asincronía con **Promesas** (`.then()` y `.catch()`).
* Procesar la respuesta de la API (`response.json()`).
* Implementar la lógica de interfaz de usuario para mostrar estados de **carga** y **error**.
* Manejar peticiones encadenadas y condicionales (ej. búsqueda y filtrado).
* Trabajar con APIs que requieren la construcción dinámica de URLs.

---

## 📂 Estructura del Proyecto

El laboratorio consta de cuatro ejercicios independientes, cada uno en su propio archivo HTML/JavaScript, abordando diferentes niveles de complejidad y APIs.

| Archivo | Nivel | API Utilizada | Descripción |
| :--- | :--- | :--- | :--- |
| `ejercicio1.html` | Básico | **JSONPlaceholder** | Obtiene y lista 10 usuarios. Primer contacto con `fetch` y promesas. |
| `ejercicio1.html` | Básico | **JSONPlaceholder** | Obtiene y lista 10 usuarios. Primer contacto con `fetch` y promesas. |
| `ejercicio2.html` | Básico-Intermedio | **PokéAPI** | Crea un buscador dinámico de Pokémon por nombre o ID, incluyendo la visualización de datos y manejo del error **404**. |
| `ejercicio3.html` | Intermedio | **REST Countries** | Implementa un explorador de países con opciones de **búsqueda por nombre** o **filtrado por región**, y limita los resultados. |
| `ejercicio4.html` | Intermedio-Avanzado | **JSONPlaceholder** | Desarrolla una aplicación de blog que maneja **múltiples peticiones encadenadas** (cargar usuarios, cargar posts, contar comentarios y cargar comentarios al hacer clic). |

---

## ⚙️ APIs Públicas Utilizadas

Para la realización de los ejercicios, se utilizó la siguiente lista de APIs públicas, gratuitas y sin requerimiento de autenticación:

1.  **JSONPlaceholder:** (`https://jsonplaceholder.typicode.com`)
    * Utilizado para datos de prueba (usuarios, posts, comentarios).
2.  **PokéAPI:** (`https://pokeapi.co/api/v2`)
    * Utilizado para obtener información detallada de Pokémon.
3.  **REST Countries:** (`https://restcountries.com/`)
    * Utilizado para obtener datos geográficos y demográficos de países.

---

## ✅ Tareas y Logros Destacados

### Ejercicio 1: Lista de Usuarios

* Implementación completa de la función `cargarUsuarios()` con `fetch()`.
* Manejo de la respuesta para verificar `respuesta.ok`.
* Renderizado dinámico de la lista de usuarios en el DOM.

### Ejercicio 2: Buscador de Pokémon

* Construcción dinámica de la URL de búsqueda (`https://pokeapi.co/api/v2/pokemon/${nombre}`).
* Implementación de la lógica para identificar y manejar el error **404** (Pokémon no encontrado).
* Extracción y visualización de propiedades complejas como la imagen y los tipos de Pokémon.

### Ejercicio 3: Información de Países

* Lógica condicional para construir la URL basándose en filtros de **nombre** o **región**.
* Manejo de la respuesta para limitar el número de resultados a **12** mediante `paises.slice(0, 12)`.
* Extracción de información anidada (capital, idiomas, monedas, etc.).

### Ejercicio 4: Posts y Comentarios

* **Carga inicial de datos:** Se llenó dinámicamente el `select` de usuarios al cargar la página.
* **Peticiones encadenadas (simuladas):** Se implementó una función para **contar comentarios** (`contarComentarios()`) y otra para **cargar comentarios** al hacer clic, demostrando la capacidad de realizar múltiples `fetch` en cascada.
* Uso de JavaScript para manipular la visibilidad de elementos (`comentarios.visible`).