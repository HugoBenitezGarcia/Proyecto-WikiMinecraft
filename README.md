# Proyecto-WikiMinecraft

---
- Imagenes generadas con ia
- json he tenido que usar la ia para hacerlo
- Documentacion del Readme generado por IA
---

# MineWiki · Proyecto 1: De la API a la página

## 1. Sobre la API utilizada
- **Nombre de la API:** Minecraft Data API (PrismarineJS / Minecraft API)
- **Categoría en el repositorio Public APIs:** Games & Comics
- **Quién la mantiene:** Comunidad Open Source de PrismarineJS (`github.com/PrismarineJS/minecraft-data`)
- **Documentación oficial:** `https://prismarinejs.github.io/minecraft-data/`
- **Condiciones de uso y seguridad:** Acceso público sin necesidad de clave (`Auth: No`), conexión segura cifrada (`HTTPS: Yes`) y licencia MIT para los esquemas de datos. Los nombres y recursos gráficos pertenecen a Mojang Studios.
- **Peticiones realizadas:** Extracción y consolidación de elementos clave (armas, herramientas, armaduras y criaturas) reflejados en el diseño del sitio.

## 2. Tabla de correspondencia de campos del JSON

| Campo del JSON | Tipo | Qué es para el lector |
| :--- | :--- | :--- |
| `name` | texto | El título principal en la ficha individual y el texto del enlace en el catálogo |
| `id` | texto | El identificador interno del juego que sirve de referencia técnica |
| `image` | URL / ruta | La ilustración del objeto o mob, acompañada de su pie descriptivo |
| `category` | texto | La familia del elemento; sirve para agrupar las secciones del catálogo |
| `durability`, `power`, `enchantability` | números | Estadísticas que se leen como «nombre: valor» en las fichas y columnas numéricas en la tabla comparativa |
| `description` | texto | El resumen explicativo del funcionamiento del objeto o criatura |

## 3. Estructura de páginas del sitio
- `index.html`: Portada de bienvenida que explica el propósito del sitio, presenta tres elementos destacados enlazados a sus fichas y un tráiler incrustado.
- `catalogo.html`: Listado de doce elementos reales clasificados en tres categorías semánticas (`Armas y Herramientas`, `Armaduras` y `Mobs`).
- `fichas/`: Tres páginas detalladas (`espada-diamante.html`, `pechera-netherita.html` y `creeper.html`) construidas bajo una misma plantilla estructural.
- `comparativa.html`: Tabla comparativa de ocho elementos evaluados en diversos atributos técnicos, estructurada con cabeceras y fila resumen (`<tfoot>`) con la media del conjunto.
- `sobre-los-datos.html`: Documentación sobre la procedencia de los datos, licencias y un ejemplo visual de transformación de un bloque JSON a HTML5 semántico.
- `propuesta.html`: Formulario con controles agrupados por bloques temáticos y validados de forma nativa por el navegador.

## 4. Decisiones de marcado HTML5
1. **Listas de descripción (`<dl>`, `<dt>`, `<dd>`):** Se han empleado para las estadísticas técnicas de los elementos en lugar de párrafos o listas desordenadas, ya que representan estrictamente pares de «propiedad: valor».
2. **Estructura semántica de fichas y catálogo:** Se ha priorizado el uso de `<article>` para cada tarjeta o ficha individual debido a que su contenido tiene entidad propia y podría sindicarse por separado.