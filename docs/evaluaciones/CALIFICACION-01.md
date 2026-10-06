# Retroalimentación — Taller evaluativo 01

**Estudiante:** Juan Camilo Blanco Parra · **Taller:** Taller evaluativo 01 — Python y estructuras de datos
**Fecha límite:** 2026-10-06 23:59 · **Versión revisada:** commit `9810939`

Muy buen trabajo: el notebook es claro y casi todos los resultados son correctos.

## Nota

| Criterio | Puntos |
|---|---|
| Variables, tipos y operadores (Ej. 1 a 4) | 16 / 20 |
| Condicionales y clasificación (Ej. 5) | 15 / 15 |
| Bucles, acumuladores y control de flujo (Ej. 6 a 8) | 30 / 30 |
| Estructuras de datos nativas (Ej. 9) | 15 / 15 |
| Ejecución sin errores | 10 / 10 |
| Documentación en celdas de texto | 4 / 5 |
| Entrega correcta | 1 / 5 |
| **Total** | **91 / 100** |
| **Nota (0–5)** | **4.55** |

Este taller aporta **13.7 %** de los 15 % del momento evaluativo.

## 1. Variables, tipos y operadores (16 / 20)
**Lo que hizo bien:**
- Las siete variables del Ejercicio 1 tienen el tipo correcto y los verificó con `type()`.
- La conversión del Ejercicio 2 sale del producto con el factor, no de un valor escrito a mano.
- El Ejercicio 3 usa solo `//` y `%` y da los valores correctos.
- El Ejercicio 4 usa `and` y `not`, sin `if`, y los tres booleanos son correctos.

**Lo que puede mejorar:**
- En el Ejercicio 2 el error absoluto se calculó al revés (valor del patrón menos lectura). Debía ser la lectura convertida menos el patrón; por eso salió -1.8 en lugar de 1.8 y el error relativo quedó con signo contrario.
- El sector quedó escrito como "NORTE" y no como "Norte", como indica la ficha.
- La variable del factor se llamó `factor_coversion` (falta una "n") y no `factor_conversion`.

## 2. Condicionales y clasificación (15 / 15)
**Lo que hizo bien:**
- La cadena `if` / `elif` / `else` va de menor a mayor umbral, cubre las cuatro categorías y clasifica 41.8 como "Dañina para grupos sensibles".

## 3. Bucles, acumuladores y control de flujo (30 / 30)
**Lo que hizo bien:**
- Ejercicio 6: `continue` descarta los dos centinelas antes de acumular; quedan 10 lecturas y el promedio es 22.55.
- Ejercicio 7: máximo 58.3, mínimo 7.5, dos recorridos y sin `max()`, `min()` ni `sum()`.
- Ejercicio 8: el `while` actualiza la concentración dentro del bloque y termina (10 horas).

## 4. Estructuras de datos nativas (15 / 15)
**Lo que hizo bien:**
- Accede a cada dato por su clave, desempaqueta las coordenadas en `latitud` y `longitud` y usa `get` con "no disponible", sin errores.

## 5. Ejecución sin errores (10 / 10)
**Lo que hizo bien:**
- El notebook corre completo sin errores y la celda de verificación imprime el mensaje final.

## 6. Documentación en celdas de texto (4 / 5)
**Lo que hizo bien:**
- Cada ejercicio tiene su celda de texto previa y los nombres están en `snake_case`.

**Lo que puede mejorar:**
- Algunos nombres no coinciden con la guía: `factor_coversion`, `lecturas_por_horas` (debía ser `lecturas_por_hora`) y `dias_completas`.

## 7. Entrega correcta (1 / 5)
**Lo que puede mejorar:**
- No siguió la estructura acordada: el notebook debe estar en la carpeta `ejercicios/` con el nombre exacto `taller-evaluativo-01-calidad-del-aire.ipynb`. Usted lo subió a la raíz del repositorio con el nombre `Taller_Evaluativo_01_Calidad_Del_Aire.ipynb`.
- Sí lo entregó a tiempo y en la rama `main`.

## ¿El notebook funciona?
Sí. Corre de principio a fin sin errores, la celda de verificación da "Verificación completada sin errores." y los resultados coinciden con los esperados.

## Para el próximo taller
- Guarde el notebook en `ejercicios/` con el nombre exacto que pide la guía.
- Copie los nombres de variables tal como aparecen en la guía.
- Revise el sentido de las restas en las fórmulas de error (lectura menos patrón).
- Compare los valores de texto con la ficha (por ejemplo "Norte").
