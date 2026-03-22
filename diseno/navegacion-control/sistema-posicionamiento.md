# Sistema de Posicionamiento - Saber Dónde Está Goliat

## Descripción

Goliat-Orbital necesita saber en todo momento su posición exacta, su velocidad y su orientación para poder capturar fragmentos, mantener órbita y reportar a Tierra. El sistema de posicionamiento combina tecnologías redundantes que funcionan incluso si alguna falla.

---

## Componentes Principales

| Componente | Función | Precisión | Redundancia |
|:---|:---|:---|:---|
| **GPS / GNSS** | Posición absoluta (órbita baja) | < 10 m | Dos receptores independientes |
| **Sensores estelares** | Orientación (actitud) | < 0.01° | Dos sensores, calibración cruzada |
| **Giroscopios** | Velocidad angular, movimiento relativo | < 0.001°/s | Tres ejes, redundancia |
| **Acelerómetros** | Cambios de velocidad | < 0.01 m/s² | Tres ejes, redundancia |
| **Altímetro láser** | Distancia a la superficie (opcional) | < 1 m | Respaldo para maniobras de reingreso |

---

## Flujo de Datos

```
[GPS] → [POSICIÓN] → [COMPUTADOR DE NAVEGACIÓN]
[SENSORES ESTELARES] → [ORIENTACIÓN] → [COMPUTADOR DE NAVEGACIÓN]
[GIROSCOPIOS] → [MOVIMIENTO] → [COMPUTADOR DE NAVEGACIÓN]
[ACELERÓMETROS] → [CAMBIOS DE VELOCIDAD] → [COMPUTADOR DE NAVEGACIÓN]
        ↓
[FILTRO DE KALMAN] → [ESTADO ESTIMADO] → [CEREBRO DE GOLIAT] → [ACTUADORES]
```

---

## Modos de Operación

| Modo | Descripción | Precisión |
|:---|:---|:---|
| **Nominal** | GPS + sensores estelares + giroscopios | Máxima |
| **GPS degradado** | Solo sensores estelares + giroscopios (integración) | Buena (deriva lenta) |
| **Emergencia** | Solo giroscopios y acelerómetros | Baja (deriva rápida, solo para regresar a modo seguro) |

---

## Integración con el Cerebro

El cerebro de Goliat recibe la posición y orientación estimadas cada segundo. Con esa información:

- Decide si es necesario corregir la órbita.
- Calcula el tiempo de llegada de fragmentos a cada branquia.
- Orienta la nave para maximizar la captura.
- Reporta telemetría a Tierra.

---

## Redundancia y Seguridad

| Aspecto | Estrategia |
|:---|:---|:---|
| **Fallo de GPS** | Dos receptores independientes, con antenas separadas. Si uno falla, el otro sigue. |
| **Fallo de sensores estelares** | Dos unidades, calibración cruzada. Si una falla, la otra puede operar sola. |
| **Fallo de giroscopios** | Giroscopios de fibra óptica (sin partes móviles), tres ejes independientes. |
| **Pérdida total de navegación** | Modo seguro: se apagan sistemas no esenciales, se activa enlace de emergencia, se espera instrucciones. |

---

## Datos de Referencia

| Elemento | Valor | Fuente |
|:---|:---|:---|
| Órbita objetivo | 200-400 km, inclinación según zona de basura | Datos de NASA/ESA |
| Velocidad orbital | 7.8 km/s | Constante |
| Período orbital | 90-120 minutos | Depende de la altitud |

---

## Ventajas del Diseño

| Ventaja | Implicación |
|:---|:---|:---|
| **Redundancia** | Ningún sensor es único. Si uno falla, el sistema sigue funcionando. |
| **Precisión** | Posición conocida con error < 10 m, orientación con error < 0.01°. |
| **Integración** | Los datos se fusionan en un solo estado estimado para el cerebro. |
| **Robustez** | Funciona incluso en condiciones de GPS degradado o fallo de sensores estelares. |

---

## Próximos Pasos

1. Selección de componentes comerciales (receptores GPS, sensores estelares, giroscopios)
2. Diseño del filtro de Kalman (fusión de datos)
3. Integración con el cerebro de Goliat
4. Pruebas en simulador orbital

---

*Documento v1.0 - Marzo 2026*
*Goliat-Orbital - Mackiber Labs*
