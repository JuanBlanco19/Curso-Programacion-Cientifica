# Retroalimentación — Taller evaluativo 02: Funciones y POO

**Estudiante:** Juan Camilo Blanco Parra · **Taller:** Taller evaluativo 02 — Funciones y POO
**Fecha límite:** 2026-10-26 23:59 · **Versión revisada:** commit `c23fe25`

Excelente trabajo: un taller casi perfecto, limpio y bien organizado.

## Nota

| Criterio | Puntos |
|---|---|
| Funciones: parámetros, valores por defecto y retorno (Ej. 1 a 3) | 20 / 20 |
| `map`, `filter` y `lambda` (Ej. 4) | 10 / 10 |
| Clases, atributos y métodos (Ej. 5 y 7) | 15 / 15 |
| Encapsulamiento y validación (Ej. 6) | 15 / 15 |
| `__repr__` y `__str__` (Ej. 6 a 8) | 10 / 10 |
| Integración de funciones y clases (Ej. 8) | 10 / 10 |
| Ejecución sin errores | 10 / 10 |
| Documentación | 4 / 5 |
| Entrega correcta | 5 / 5 |
| **Total** | **99 / 100** |
| **Nota (0–5)** | **4.95** |

Este taller aporta **14.9 %** de los 15 % del momento evaluativo.

## 1. Funciones: parámetros, valores por defecto y retorno (20 / 20)
**Lo que hizo bien:**
- `calibrar_lectura` tiene los valores por defecto en la firma, usa `return` y da 11.5 y 12.0 como se esperaba.
- `es_lectura_valida` responde bien para 25.0, -999.0, 600.0 y 0.0.
- `promedio_valido` reutiliza `es_lectura_valida`, usa solo variables locales, da 27.0 y devuelve `None` cuando no hay datos válidos.

## 2. `map`, `filter` y `lambda` (10 / 10)
**Lo que hizo bien:**
- Obtuvo las 5 lecturas calibradas (de 11.5 a 61.9) y las 2 excedencias, sin bucles ni comprensiones.

## 3. Clases, atributos y métodos (15 / 15)
**Lo que hizo bien:**
- `Lectura` guarda sus tres datos con valores por defecto y convierte 0.0252 mg/m3 a 25.2 ug/m3.
- `Estacion` guarda objetos `Lectura` y `valores()` entrega los ocho valores usando `a_microgramos()`.

## 4. Encapsulamiento y validación (15 / 15)
**Lo que hizo bien:**
- `Sensor` rechaza el código vacío y la pendiente menor o igual a cero antes de guardar nada.
- La pendiente y el intercepto quedan como `_pendiente` e `_intercepto`, y `calibrar` reutiliza `calibrar_lectura`.
- No dejó celdas de prueba que fallen.

## 5. `__repr__` y `__str__` (10 / 10)
**Lo que hizo bien:**
- Los textos de `Sensor`, `Estacion` e `InformeEstacion` coinciden exactamente con lo pedido, y `print(sensor_a)` es claro.

## 6. Integración de funciones y clases (10 / 10)
**Lo que hizo bien:**
- `InformeEstacion` da 31.9 y "Moderada" reutilizando las funciones y el método `calibrar` del sensor.
- `categoria_pm25` usa una sola cadena `if` / `elif` / `else` y cubre las cuatro categorías.

## 7. Ejecución sin errores (10 / 10)
**Lo que hizo bien:**
- Todo corre de principio a fin sin errores y la verificación final imprime el mensaje esperado.

## 8. Documentación (4 / 5)
**Lo que hizo bien:**
- Cada ejercicio tiene su celda de texto y todas las funciones, clases y métodos tienen docstring.
- Los nombres siguen `snake_case` y `PascalCase`.

**Lo que puede mejorar:**
- En la celda inicial falta la fecha: quedó el campo "Fecha:" vacío.

## 9. Entrega correcta (5 / 5)
**Lo que hizo bien:**
- El notebook está en `ejercicios/` con el nombre exacto, antes del plazo.

## ¿El notebook funciona?
Sí. Corre completo sin errores, la celda de verificación imprime "Verificación completada sin errores." y todos los resultados coinciden con los esperados.

## Para el próximo taller
- Complete siempre la celda inicial con título, nombre y fecha.
- Revise las celdas de texto y deje solo la explicación del ejercicio.
- Siga con el mismo hábito de ejecutar todo desde cero antes de entregar.
