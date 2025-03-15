# Tarea4CasosdeUso
Tarea 4.- Documento de Requerimientos y Casos de Uso

El sistema tiene como objetivo proporcionar una plataforma integral de búsqueda y recomendación multimodal de contenido enfocado en libros, series, videojuegos y anime. Utilizando APIs públicas externas como Open Library, TVMaze, IGDB o MyAnimeList, el sistema permitirá a los usuarios explorar contenido, guardar favoritos, mantener un historial de búsquedas y recibir recomendaciones personalizadas. Además, contará con funciones avanzadas de procesamiento de datos aplicando diseños ETL y análisis basados en algoritmos de IA para enriquecer la experiencia del usuario.

#Diagrama de Casos de Uso


![Image](https://github.com/user-attachments/assets/2ea509da-a66a-4b9d-b732-0596c06a969f)


# Documentación de Casos de Uso

## 1. Buscar contenido

**Descripción:**
El usuario busca contenido específico (libros, series, videojuegos, anime) utilizando el sistema.

**Actores:**
- Usuario
- Sistema

**Precondiciones:**
- El usuario debe estar autenticado en el sistema.

**Flujo principal:**
1. El usuario ingresa el término de búsqueda.
2. El sistema consulta las APIs públicas (Open Library, TVMaze, etc.).
3. El sistema muestra los resultados de la búsqueda al usuario.

**Flujos alternativos:**
- Flujo alternativo 1: Si no se encuentran resultados, el sistema sugiere alternativas relacionadas.
  1. El sistema busca patrones predefinidos.
  2. El sistema sugiere alternativas basadas en los patrones encontrados.

**Postcondiciones:**
- El usuario ve los resultados de la búsqueda o las sugerencias alternativas.

## 2. Recomendar contenido

**Descripción:**
El sistema recomienda contenido relacionado basado en las preferencias del usuario y el análisis de datos.

**Actores:**
- Usuario
- Sistema

**Precondiciones:**
- El usuario debe haber buscado o visto contenido previamente.

**Flujo principal:**
1. El usuario solicita recomendaciones.
2. El sistema analiza el historial y preferencias del usuario.
3. El sistema recomienda contenido relacionado.

**Flujos alternativos:**
- Ninguno

**Postcondiciones:**
- El usuario recibe recomendaciones de contenido.

## 3. Sugerir alternativas

**Descripción:**
El sistema sugiere alternativas si el contenido buscado no está disponible.

**Actores:**
- Usuario
- Sistema

**Precondiciones:**
- El usuario debe haber realizado una búsqueda de contenido.

**Flujo principal:**
1. El sistema no encuentra el contenido solicitado.
2. El sistema busca alternativas basadas en patrones predefinidos.
3. El sistema sugiere alternativas al usuario.

**Flujos alternativos:**
- Ninguno

**Postcondiciones:**
- El usuario recibe sugerencias alternativas.

## 4. Procesar datos (ETL)

**Descripción:**
El sistema procesa datos utilizando funciones ETL (Extract, Transform, Load).

**Actores:**
- Sistema

**Precondiciones:**
- Datos disponibles para procesar.

**Flujo principal:**
1. El sistema extrae datos de diversas fuentes.
2. El sistema transforma los datos según las necesidades del análisis.
3. El sistema carga los datos en el almacén de datos.

**Flujos alternativos:**
- Ninguno

**Postcondiciones:**
- Los datos están disponibles en el almacén de datos para análisis.

## 5. Generar recomendaciones basadas en análisis avanzados

**Descripción:**
El sistema genera recomendaciones utilizando análisis avanzados de datos.

**Actores:**
- Sistema

**Precondiciones:**
- Datos disponibles en el almacén de datos.

**Flujo principal:**
1. El sistema analiza los datos en el almacén.
2. El sistema genera recomendaciones basadas en el análisis.

**Flujos alternativos:**
- Ninguno

**Postcondiciones:**
- Las recomendaciones están disponibles para el usuario.

## 6. Configurar el sistema

**Descripción:**
El administrador configura el sistema para incorporar almacenes de datos y funciones ETL.

**Actores:**
- Administrador
- Sistema

**Precondiciones:**
- El administrador debe tener permisos de configuración.

**Flujo principal:**
1. El administrador accede a la configuración del sistema.
2. El administrador configura los parámetros del almacén de datos y funciones ETL.
3. El sistema guarda la configuración.

**Flujos alternativos:**
- Ninguno

**Postcondiciones:**
- El sistema está configurado según las necesidades del administrador.
