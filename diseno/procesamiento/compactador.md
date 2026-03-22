# Compactador - Procesamiento de Fragmentos (Fase 1)

## Descripción

El compactador es el sistema de procesamiento primario de Goliat-Orbital en su primera fase de operación. Su función es reducir el volumen de los fragmentos capturados mediante presión hidráulica, transformándolos en bloques compactos de chatarra listos para almacenar y eventualmente reingresar a Tierra.

Es la opción de menor riesgo y mayor velocidad de implementación. No requiere fundición, no requiere gravedad artificial, y puede operar en microgravedad con tecnología existente.

---

## Especificaciones Técnicas

| Parámetro | Valor | Observación |
|:---|:---|:---|
| Tipo | Prensa hidráulica de doble efecto | Compactación en ambas direcciones |
| Fuerza máxima | 1000 toneladas | Suficiente para fragmentos metálicos de hasta 2.5 m |
| Ciclo por fragmento | 30-60 segundos | Depende del tamaño y material |
| Consumo energético | 10-50 kW por ciclo | Picos durante la compactación |
| Dimensiones | 3 m × 2 m × 2 m | Integrado en la tolva de recepción |
| Material | Acero reforzado, revestimiento anti-desgaste | Alta resistencia al impacto |

---

## Componentes

| Componente | Función | Tecnología |
|:---|:---|:---|
| **Tolva de recepción** | Almacena fragmentos antes de compactar | Contenedor reforzado, amortiguadores |
| **Prensa hidráulica** | Aplica presión para reducir volumen | Cilindros hidráulicos de alta fuerza |
| **Matriz** | Molde donde se compacta el fragmento | Acero templado, geometría estandarizada |
| **Sistema de eyección** | Expulsa el bloque compactado | Pistón hidráulico secundario |
| **Bodega de compactados** | Almacena bloques para reingreso | Estanterías con sujeción automática |

---

## Ciclo de Operación

| Fase | Acción | Duración |
|:---|:---|:---|
| **1. Recepción** | Fragmento cae en la tolva | Automático |
| **2. Posicionamiento** | Brazo robótico (o gravedad) coloca el fragmento en la matriz | 5-10 s |
| **3. Compactación** | Prensa hidráulica aplica presión | 10-30 s |
| **4. Eyección** | Bloque compactado es expulsado | 5 s |
| **5. Almacenamiento** | Brazo robótico lleva el bloque a la bodega | 10-15 s |

---

## Redundancia y Seguridad

| Aspecto | Estrategia |
|:---|:---|
| **Atasco** | Sensores de presión detectan bloqueo. Se invierte el ciclo para liberar. |
| **Fallo hidráulico** | Sistema de válvulas redundantes. Respaldo manual desde Tierra. |
| **Sobrecalentamiento** | Refrigeración por radiadores, corte térmico automático. |
| **Fragmento no compactable** | (ej: material no metálico) Se expulsa a un contenedor separado o se devuelve al espacio. |

---

## Integración con la Nave

```
[CAPTURA] → [TOLVA] → [COMPACTADOR] → [BODEGA] → [REINGRESO]
                ↓
         [BRAZO ROBÓTICO]
```

---

## Ventajas del Diseño

| Ventaja | Implicación |
|:---|:---|
| **Tecnología probada** | Las prensas hidráulicas existen desde hace siglos. No hay riesgo de desarrollo. |
| **Bajo consumo** | Solo picos durante la compactación. El resto del tiempo, consumo cero. |
| **Operación en microgravedad** | La presión hidráulica no depende de la gravedad. Funciona igual en el espacio. |
| **Genera ingresos rápido** | Los bloques compactados se pueden vender como chatarra desde la fase 1. |

---

## Materiales Procesados

| Material | Compactabilidad | Valor comercial |
|:---|:---|:---|
| Aluminio | Alta | Medio |
| Cobre | Alta | Alto |
| Hierro | Alta | Bajo-medio |
| Titanio | Media | Alto |
| Materiales compuestos | Baja | Bajo (se separan) |

Los bloques compactados mantienen la pureza del material original. No hay mezcla ni contaminación.

---

## Capacidad Estimada

| Período | Fragmentos procesados | Masa compactada |
|:---|:---|:---|
| Por día | 10-50 fragmentos | 100-500 kg |
| Por año | 3.600-18.000 fragmentos | 36-180 toneladas |

Depende de la densidad de basura en la órbita seleccionada.

---

## Próximos Pasos

1. Selección de prensa hidráulica comercial (o diseño propio)
2. Simulación de compactación en microgravedad
3. Integración con brazo robótico para posicionamiento
4. Pruebas en Tierra con fragmentos reales

---

*Documento v1.0 - Marzo 2026*
*Goliat-Orbital - Mackiber Labs*
