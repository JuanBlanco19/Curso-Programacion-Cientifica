# Retroalimentación — Taller evaluativo 03 (NumPy)

**Estudiante:** Juan Camilo Blanco Parra · **Taller:** Taller evaluativo 03 — NumPy
**Fecha límite:** 2026-10-26 23:59 · **Versión revisada:** commit `4eaf46f`

Excelente trabajo: todos los resultados coinciden con los esperados.

## Nota

| Criterio | Puntos |
|---|---|
| Creación y atributos de arreglos (Ej. 1) | 10 / 10 |
| Indexación y slicing (Ej. 2) | 10 / 10 |
| Máscaras booleanas (Ej. 3) | 15 / 15 |
| Vectorización y broadcasting (Ej. 4) | 15 / 15 |
| Estadística por eje y funciones universales (Ej. 5 y 6) | 20 / 20 |
| Integración (Ej. 7) | 10 / 10 |
| Ejecución sin errores | 10 / 10 |
| Documentación | 4 / 5 |
| Entrega correcta | 2 / 5 |
| **Total** | **96 / 100** |
| **Nota (0–5)** | **4.80** |

Este taller aporta **14.4 %** de los 15 % del momento evaluativo.

## 1. Creación y atributos de arreglos (10 / 10)
**Lo que hizo bien:**
- Creó `lecturas_crudas` con `np.array` a partir de una lista de listas y leyó forma, dimensiones, total y tipo desde sus atributos.
- `dias`, `pendientes` e `interceptos` son correctos.

## 2. Indexación y slicing (10 / 10)
**Lo que hizo bien:**
- Cada resultado sale de una sola expresión, con el índice negativo donde se pedía.
- El bloque tiene la forma `(3, 4)` correcta.

## 3. Máscaras booleanas (15 / 15)
**Lo que hizo bien:**
- Unió las dos comparaciones con `&` y paréntesis, sin usar `and`.
- Obtuvo 2 lecturas faltantes, 5 útiles y promedio 27.0.

## 4. Vectorización y broadcasting (15 / 15)
**Lo que hizo bien:**
- Convirtió pendientes e interceptos en columnas y calibró toda la red sin bucles.
- Explicó bien por qué fallaba la multiplicación con formas distintas.
- El promedio calibrado de SBC-A da 31.9.

## 5. Estadística por eje y funciones universales (20 / 20)
**Lo que hizo bien:**
- Los promedios por sensor y por día, los máximos y la media sobre el límite (43.275) son correctos.
- Usó `np.maximum`, `np.abs` y `np.round`, y `en_alerta` sale de una copia, dejando `calibradas` intacto (8 celdas en alerta).

## 6. Integración (10 / 10)
**Lo que hizo bien:**
- Los conteos 9, 18, 7 y 1 suman 35, y el día pico es el 5.
- Las dos líneas de salida coinciden con lo pedido.

## 7. Ejecución sin errores (10 / 10)
**Lo que hizo bien:**
- El notebook corre completo sin errores y la celda de verificación imprime el mensaje final.

## 8. Documentación (4 / 5)
**Lo que hizo bien:**
- Los siete ejercicios tienen su celda de texto previa y los nombres siguen `snake_case`.

**Lo que puede mejorar:**
- La celda inicial tiene el título y su nombre, pero le falta la fecha.

**Cómo corregirlo:**
- En la primera celda de texto, junto al título y su nombre, escriba una línea con la fecha de entrega (por ejemplo, "Fecha: 26 de octubre de 2026").

## 9. Entrega correcta (2 / 5)
**Lo que hizo bien:**
- El notebook está en la carpeta `ejercicios/` de la rama `main`, antes del plazo.

**Lo que puede mejorar:**
- No siguió la estructura acordada: el archivo se llama `taller_evaluativo_03_numpy.ipynb` y el nombre exacto debía ser `taller-evaluativo-03-numpy.ipynb` (con guiones).

**Cómo corregirlo:**
- Cambie el nombre del archivo a `taller-evaluativo-03-numpy.ipynb`, usando guiones en lugar de guiones bajos, y déjelo dentro de la carpeta `ejercicios/` de la rama `main`.
- Después de renombrarlo, confirme en GitHub que el archivo nuevo aparece con ese nombre y que el anterior ya no está, para que no queden dos copias.

## ¿El notebook funciona?
Sí. Corre completo sin errores, la celda de verificación imprime "Verificación completada sin errores." y todos los resultados coinciden con los esperados.

## Para el próximo taller
- Use exactamente el nombre de archivo que indica la guía.
- Incluya título, nombre completo y fecha en la primera celda.
- Siga ejecutando "Reiniciar y ejecutar todas" antes de entregar.
