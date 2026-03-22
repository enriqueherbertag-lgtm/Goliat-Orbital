# Módulo Rotatorio - Gravedad Artificial para Fundición

## Descripción

El módulo rotatorio es un segmento de Goliat-Orbital que se acopla al cuerpo principal después de la fase de compactación. Su función es generar gravedad artificial por centrifugación (0.1-0.3 g), permitiendo el uso de un horno convencional con crisol y moldeo por inyección, eliminando la necesidad de tecnologías complejas de fundición en microgravedad.

---

## Especificaciones Técnicas

| Parámetro | Valor | Observación |
|:---|:---|:---|
| Tipo | Segmento rotatorio acoplado al cuerpo principal | Se lanza por separado y se acopla en órbita |
| Radio | 5-10 m | Desde el eje de rotación hasta la cámara de fundición |
| Velocidad de rotación | 4-6 rpm | Suficiente para 0.1-0.3 g |
| Gravedad generada | 0.1-0.3 g | Permite operar horno y molde como en Tierra |
| Accionamiento | Válvulas de alivio (presión del proceso) + respaldo eléctrico | Energía gratuita del proceso |
| Material | Estructura de aluminio reforzado, recubrimiento anti-desgaste | Ligera, resistente |

---

## Componentes

| Componente | Función | Tecnología |
|:---|:---|:---|
| **Eje de rotación** | Conexión con el cuerpo principal, transferencia de energía y datos | Cojinetes de baja fricción, anillos deslizantes |
| **Brazo estructural** | Sostiene la cámara de fundición | Aluminio reforzado, diseño aerodinámico |
| **Cámara de fundición** | Contiene horno, crisol, molde | Acero reforzado, aislamiento térmico |
| **Válvulas de alivio** | Generan par de rotación usando presión del proceso | Toberas tangenciales |
| **Motores de respaldo** | Rotación auxiliar para arranque o emergencia | Motores eléctricos de bajo consumo |

---

## Ciclo de Operación

| Fase | Acción | Fuente de energía |
|:---|:---|:---|
| **1. Arranque** | Motores de respaldo inician la rotación (hasta 1 rpm) | Baterías / paneles solares |
| **2. Estabilización** | Válvulas de alivio toman el control, aceleran hasta 4-6 rpm | Presión del proceso (vapor, gases calientes) |
| **3. Fundición** | Horno se activa, metal fundido en crisol | Energía eléctrica (paneles solares) |
| **4. Moldeo** | Metal se vierte en molde por inyección | Gravedad artificial + presión |
| **5. Frenado** | Válvulas de alivio se orientan para reducir rotación | Presión residual |
| **6. Detención** | Motores de respaldo frenan el módulo | Baterías |

---

## Generación de Rotación por Válvulas de Alivio

| Fuente de presión | Uso | Par generado |
|:---|:---|:---|
| Vapor de enfriamiento | Durante la fundición | Bajo, continuo |
| Gases calientes del horno | Al abrir la cámara | Alto, pulsos |
| Exceso de presión en el molde | Al inyectar metal | Medio, variable |

Las válvulas están orientadas tangencialmente al eje de rotación. El chorro de gas o vapor genera un par que acelera o frena el módulo sin consumir combustible adicional.

---

## Integración con el Procesamiento

```
[COMPACTADOR] → [MÓDULO ROTATORIO] → [HORNO] → [MOLDE] → [BODEGA]
        ↓               ↓               ↓          ↓
[FRAGMENTO]      [GRAVEDAD]       [FUNDICIÓN] [LINGOTE]
```

---

## Redundancia y Seguridad

| Aspecto | Estrategia |
|:---|:---|
| **Fallo de rotación** | Motores de respaldo pueden mantener la rotación o frenar el módulo. |
| **Desbalance** | Sensores de vibración; si se detecta desbalance, se reduce velocidad o se detiene. |
| **Fuga de gases** | Compuertas de aislamiento entre módulo rotatorio y cuerpo principal. |
| **Sobrecalentamiento** | Radiadores pasivos, corte térmico automático. |

---

## Ventajas del Diseño

| Ventaja | Implicación |
|:---|:---|
| **Energía gratuita** | La rotación se genera con presión del proceso, no con motores adicionales. |
| **Tecnología simple** | Horno convencional con crisol, en lugar de levitación electromagnética. |
| **Escalable** | El radio y la velocidad se pueden ajustar según la gravedad deseada. |
| **Desacoplable** | El módulo se puede lanzar después, cuando Goliat ya esté operando. |

---

## Próximos Pasos

1. Diseño estructural del brazo y la cámara de fundición
2. Selección de cojinetes y anillos deslizantes (transferencia de energía/datos)
3. Simulación de rotación con válvulas de alivio
4. Integración con horno convencional y molde por inyección

---

*Documento v1.0 - Marzo 2026*
*Goliat-Orbital - Mackiber Labs*
