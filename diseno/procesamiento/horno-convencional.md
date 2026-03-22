# Horno Convencional - Fundición de Metales

## Descripción

El horno convencional es el corazón del sistema de procesamiento de Goliat-Orbital en su segunda fase. Opera dentro del módulo rotatorio, aprovechando la gravedad artificial (0.1-0.3 g) para fundir metales en un crisol, como en una fundición terrestre. Reemplaza la tecnología de levitación electromagnética por un sistema simple, probado y escalable.

---

## Especificaciones Técnicas

| Parámetro | Valor | Observación |
|:---|:---|:---|
| Tipo | Horno de resistencia o inducción con crisol | Tecnología existente, adaptada al espacio |
| Temperatura máxima | 1600°C | Suficiente para fundir cobre (1085°C), hierro (1538°C) |
| Capacidad por carga | 50-100 kg | Escalable según tamaño del crisol |
| Consumo energético | 20-100 kW durante la fusión | Depende del metal y la carga |
| Tiempo de fusión | 30-60 minutos | Según metal y potencia |
| Material del crisol | Grafito, cerámica o refractario | Resistente a altas temperaturas y corrosión |
| Aislamiento | Multicapa cerámica + vacío | Minimiza pérdidas térmicas |

---

## Componentes

| Componente | Función | Tecnología |
|:---|:---|:---|
| **Crisol** | Contiene el metal a fundir | Grafito o cerámica, con recubrimiento antiadherente |
| **Resistencias** | Generan calor por efecto Joule | Elementos de carburo de silicio o molibdeno |
| **Opcional: inducción** | Calentamiento por campos magnéticos alternos | Bobinas de cobre refrigeradas |
| **Aislante térmico** | Reduce pérdidas de calor | Multicapa cerámica + vacío |
| **Sistema de vertido** | Inclina el crisol o abre válvula inferior | Actuadores hidráulicos o eléctricos |
| **Cámara de fusión** | Contiene todo el conjunto | Acero reforzado, con puerta hermética |

---

## Ciclo de Operación

| Fase | Acción | Duración |
|:---|:---|:---|
| **1. Carga** | Brazo robótico introduce fragmentos compactados en el crisol | 2-5 min |
| **2. Sellado** | Cámara de fusión se cierra herméticamente | 30 s |
| **3. Calentamiento** | Resistencias o inducción elevan la temperatura | 30-60 min |
| **4. Fusión** | Metal alcanza estado líquido, se homogeniza | 10-20 min |
| **5. Vertido** | Crisol se inclina, metal fluye al molde | 1-2 min |
| **6. Enfriamiento** | Crisol se limpia, se prepara para siguiente carga | 5-10 min |

---

## Materiales Procesados

| Metal | Punto de fusión (°C) | Energía requerida (kWh/kg) | Valor comercial |
|:---|:---|:---|:---|
| Aluminio | 660 | 0.3-0.4 | Medio |
| Cobre | 1085 | 0.5-0.7 | Alto |
| Hierro | 1538 | 0.8-1.0 | Bajo-medio |
| Titanio | 1668 | 0.9-1.1 | Alto |
| Plata | 961 | 0.4-0.6 | Muy alto |

---

## Integración con el Módulo Rotatorio

```
[MÓDULO ROTATORIO] → [HORNO CONVENCIONAL] → [MOLDE POR INYECCIÓN] → [BODEGA]
        ↓                    ↓                       ↓
   [0.1-0.3 g]        [CRISOL]              [LINGOTE]
```

La gravedad artificial mantiene el metal en el fondo del crisol durante la fusión y facilita el vertido sin necesidad de sistemas complejos de succión o presión.

---

## Redundancia y Seguridad

| Aspecto | Estrategia |
|:---|:---|
| **Sobrecalentamiento** | Control de temperatura con termopares redundantes, corte automático |
| **Fuga de metal fundido** | Cámara de fusión con doble pared, sistema de contención |
| **Fallo de resistencias** | Opción de inducción como respaldo, o resistencias secundarias |
| **Pérdida de vacío** | Sensores de presión, cierre de compuertas de aislamiento |

---

## Ventajas del Diseño

| Ventaja | Implicación |
|:---|:---|
| **Tecnología probada** | Hornos convencionales existen hace siglos. No hay riesgo de desarrollo. |
| **Operación en gravedad artificial** | El metal se comporta como en Tierra. No se requiere levitación. |
| **Escalable** | Tamaño del crisol ajustable según producción deseada. |
| **Materiales versátiles** | Puede procesar aluminio, cobre, hierro, titanio, plata, etc. |

---

## Energía y Consumo

| Fuente de energía | Uso | Porcentaje |
|:---|:---|:---|
| Paneles solares | Calentamiento del horno | 60-80% |
| Baterías | Picos de demanda | 20-40% |
| Calor residual | Precalentamiento de fragmentos (opcional) | 10-20% (ahorro) |

El horno opera en ciclos intermitentes, no continuos. La energía solar se acumula en baterías durante las horas de baja demanda y se usa durante la fusión.

---

## Próximos Pasos

1. Selección de tipo de horno (resistencia vs inducción)
2. Dimensionamiento del crisol según capacidad de captura
3. Integración con sistema de vertido y molde por inyección
4. Pruebas en Tierra con fragmentos reales y gravedad simulada (bancada inclinada o vuelo parabólico)

---

*Documento v1.0 - Marzo 2026*
*Goliat-Orbital - Mackiber Labs*
