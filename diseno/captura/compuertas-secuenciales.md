# Compuertas Secuenciales - Aislamiento y Control de Flujo

## Descripción

Cada branquia de Goliat-Orbital tiene un sistema de dos compuertas: una externa (en la entrada) y una interna (antes de la cámara de procesamiento). Su función no es desacelerar fragmentos (no hay velocidad relativa), sino **aislar secciones**, mantener presión diferencial y evitar pérdidas de gas durante la captura.

---

## Especificaciones Técnicas

| Parámetro | Valor |
|:---|:---|
| Número por branquia | 2 (externa e interna) |
| Material | Acero reforzado, bordes con sello hermético |
| Accionamiento | Electromecánico (motor + reductora) |
| Tiempo de apertura/cierre | < 1 segundo |
| Control | Digital (desde computador de a bordo) |
| Respaldo | Manual desde Tierra (enlace banda S) |

---

## Ubicación

```
[BRANQUIA] → [COMPUERTA EXTERNA] → [TOBERA SAXOFÓN] → [COMPUERTA INTERNA] → [CÁMARA DE PROCESAMIENTO]
```

---

## Ciclo de Operación

| Fase | Compuerta Externa | Compuerta Interna | Acción |
|:---|:---|:---|:---|
| **1. Espera** | Cerrada | Cerrada | Protección contra impactos, sin pérdida de gas |
| **2. Detección** | Se abre | Cerrada | Preparación para entrada de fragmento |
| **3. Arrastre** | Abierta | Cerrada | El fragmento entra, flujo activo |
| **4. Paso** | Abierta | Se abre | El fragmento pasa a la cámara de procesamiento |
| **5. Cierre** | Se cierra | Se cierra | Aislamiento, fin del ciclo |

---

## Funciones Principales

| Función | Cómo se logra |
|:---|:---|
| **Aislamiento** | Las dos compuertas crean una cámara intermedia que se puede presurizar o evacuar sin afectar el resto de la nave |
| **Control de flujo** | Abriendo o cerrando en secuencia, se regula la cantidad de gas que entra y se evita la pérdida de presión |
| **Seguridad** | En caso de impacto inesperado, la compuerta externa absorbe el golpe y protege el interior |
| **Mantenimiento** | Aislando secciones, se puede reparar o limpiar una branquia sin detener la operación de las otras |

---

## Redundancia y Seguridad

| Aspecto | Estrategia |
|:---|:---|
| **Fallo de compuerta** | Cada compuerta tiene actuador independiente. Si una falla, la otra puede cerrarse para aislar la branquia. |
| **Pérdida de presión** | Sensores de presión detectan fugas; las compuertas se cierran automáticamente. |
| **Atasco** | Sensores de posición detectan obstrucción; se activa contraflujo o se abre otra branquia para aliviar presión. |
| **Energía** | Accionamiento electromecánico con respaldo de batería local. |

---

## Ventajas del Diseño

| Ventaja | Implicación |
|:---|:---|
| **Aislamiento** | Permite operar branquias independientemente. Si una falla, las otras siguen. |
| **Control de presión** | Evita pérdida de gas, mejora eficiencia de los compresores. |
| **Seguridad** | Protege el interior de la nave en caso de impacto o mal funcionamiento. |
| **Mantenimiento** | Permite reparar una branquia sin detener toda la operación. |

---

## Próximos Pasos

1. Selección de actuadores electromecánicos (tiempo de respuesta, consumo)
2. Diseño de sellos herméticos para vacío
3. Simulación de flujo con compuertas abiertas/cerradas
4. Integración con sistema de sensores de presión y posición

---

*Documento v1.0 - Marzo 2026*
*Goliat-Orbital - Mackiber Labs*
