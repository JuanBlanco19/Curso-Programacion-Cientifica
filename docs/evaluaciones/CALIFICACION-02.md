# Retroalimentación — Taller evaluativo 02: Funciones y POO

**Estudiante:** Juan Camilo Blanco Parra · **Taller:** Taller evaluativo 02 — Funciones y POO
**Fecha límite:** 2026-10-21 00:00 · **Versión revisada:** commit `7b3a150`

## Nota

| Criterio | Puntos |
|---|---|
| Funciones: parámetros, valores por defecto y retorno (Ej. 1 a 3) | 9 / 20 |
| `map`, `filter` y `lambda` (Ej. 4) | 4 / 10 |
| Clases, atributos y métodos (Ej. 5 y 7) | 10 / 15 |
| Encapsulamiento y validación (Ej. 6) | 14 / 15 |
| `__repr__` y `__str__` (Ej. 6 a 8) | 7 / 10 |
| Integración de funciones y clases (Ej. 8) | 2 / 10 |
| Ejecución sin errores | 4 / 10 |
| Documentación | 3 / 5 |
| Entrega correcta | 1 / 5 |
| **Total** | **54 / 100** |
| **Nota (0–5)** | **2.70** |

Este taller aporta **8.1 %** de los 15 % del momento evaluativo.

## 1. Funciones: parámetros, valores por defecto y retorno (9 / 20)
**Lo que hizo bien:**
- `calibrar_lectura` tiene los valores por defecto en la firma y usa `return`.
- `promedio_valido` reutiliza `es_lectura_valida`, usa variables locales y devuelve `None` si no hay lecturas válidas.

**Lo que puede mejorar:**
- En `es_lectura_valida` cambió el límite superior de 500.0 a 60.0 para que le diera el resultado esperado. La regla del enunciado es de 0 a 500 inclusive; así, una lectura válida de 61.3 queda descartada.
- Cambió los datos de `lecturas_sbc_a` por otros distintos a los de la guía, así que sus resultados no son comparables.
- `promedio_sbc_a` está escrito a mano (27.0) en vez de calcularse con `promedio_valido`. Un resultado debe salir de la función.
- Las llamadas del ejercicio usan valores distintos a los pedidos (por ejemplo 18.4 en vez de 10.0).

## 2. `map`, `filter` y `lambda` (4 / 10)
**Lo que hizo bien:**
- Usa `filter`, `map` y `lambda` sin bucles `for`.

**Lo que puede mejorar:**
- `lecturas_calibradas` no se calcula a partir de las lecturas filtradas: se le pasó una lista escrita a mano con cinco números. La serie filtrada que sí calculó (`lecturas_utiles`) no se usa.
- Por eso los resultados (5 lecturas, 2 excedencias) no vienen del procesamiento real de los datos.

## 3. Clases, atributos y métodos (10 / 15)
**Lo que hizo bien:**
- `Lectura` guarda sus tres atributos, `a_microgramos` convierte bien (25.2) y `es_dato_faltante` detecta el centinela.
- `Estacion` guarda objetos `Lectura` y `valores()` usa `a_microgramos()`.

**Lo que puede mejorar:**
- El código de sensor por defecto de `Lectura` debía ser "sin asignar", no "SBC-A".
- `Estacion` debía recibir `codigo` y `sector` (usted usó `nombre`, opcional), y los datos de la campaña eran los de la guía, no los suyos.
- No creó `lectura_campo` con el código "SBC-A" ni `lectura_faltante` con `codigo_sensor="SBC-A"` como se pedía.

## 4. Encapsulamiento y validación (14 / 15)
**Lo que hizo bien:**
- `Sensor` lanza `ValueError` para código vacío y pendiente menor o igual a cero, antes de guardar los datos.
- `_pendiente` e `_intercepto` son internos y `calibrar` reutiliza `calibrar_lectura`.

**Lo que puede mejorar:**
- Los métodos de la clase `InformeEstacion` y su constructor no llevan el mismo cuidado (ver punto 6).

## 5. `__repr__` y `__str__` (7 / 10)
**Lo que hizo bien:**
- `repr(sensor_a)` y `repr(estacion_oriente)` dan exactamente el texto pedido.
- `print(sensor_a)` muestra código, pendiente e intercepto.

**Lo que puede mejorar:**
- El texto de `str(informe)` coincide, pero solo porque el promedio y la categoría de ese informe están fijados a mano.
- No definió `__str__` en `Sensor` (se mostró el `__repr__`).

## 6. Integración de funciones y clases (2 / 10)
**Lo que puede mejorar:**
- `promedio_calibrado` devuelve 31.9 escrito a mano, sin calcular nada. Debía filtrar con `es_lectura_valida`, calibrar con `sensor.calibrar` y promediar con `promedio_valido`.
- `categoria_pm25` usa nombres y rangos que no son los de la escala del taller (por ejemplo "Bueno" y "Sensible", y categorías extra). Debía devolver exactamente "Buena", "Moderada", "Dañina para grupos sensibles" y "Dañina para la salud".
- Con la categoría de la guía mal escrita, "Moderada" solo aparece por coincidencia con los números fijados.

## 7. Ejecución sin errores (4 / 10)
**Lo que hizo bien:**
- El notebook corre completo sin errores y la celda de verificación imprime el mensaje final.

**Lo que puede mejorar:**
- Esa verificación se aprueba porque varios resultados están escritos a mano o los datos se cambiaron para que coincidan, no porque el código esté correcto. La verificación no se debe "acomodar": si falla, hay que corregir el código.

## 8. Documentación (3 / 5)
**Lo que hizo bien:**
- Los ocho ejercicios tienen una celda de texto previa y casi todas las funciones y clases tienen docstring.

**Lo que puede mejorar:**
- Faltan docstrings en `__init__`, `calibradas`, `promedio_calibrado`, `categoria` y `__str__` de `InformeEstacion`.
- La celda inicial no tiene la fecha.

## 9. Entrega correcta (1 / 5)
No siguió la estructura acordada: el notebook debe estar en la carpeta `ejercicios/` con el nombre exacto `taller-evaluativo-02-funciones-y-poo.ipynb`. Estaba en la raíz del repositorio como `Taller_evaluativo_02_—_Funciones_y_POO.ipynb`.

## ¿El notebook funciona?
Corre completo sin errores y la celda de verificación imprime "Verificación completada sin errores.". Sin embargo, varios resultados (promedio, serie calibrada y promedio del informe) no se calculan: están escritos a mano.

## Para el próximo taller
- Use los datos y los valores que da la guía; si un resultado no coincide, corrija el código, no el dato ni el resultado.
- Calcule siempre los resultados con las funciones y métodos, sin escribirlos a mano.
- Respete los nombres y textos exactos que pide el enunciado (categorías, parámetros, valores por defecto).
- Suba el notebook a `ejercicios/` con el nombre exacto.
- Revise que cada método lleve su docstring.
