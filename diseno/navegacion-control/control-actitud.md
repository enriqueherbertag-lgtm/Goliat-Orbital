# Control de Actitud - Orientación de Goliat

## Descripción

El control de actitud es el sistema que mantiene la orientación correcta de Goliat-Orbital en el espacio. La nave debe apuntar sus branquias hacia la dirección de llegada de los fragmentos, proteger las zonas sensibles durante las maniobras de aerobraking, y mantener la antena de comunicaciones apuntando a Tierra. El sistema es completamente autónomo, con respaldo manual desde Tierra.

---

## Componentes Principales

| Componente | Función | Tecnología | Redundancia |
|:---|:---|:---|:---|
| **Ruedas de reacción** | Control fino de orientación | 4 ruedas (configuración tetraédrica) | Si una falla, las otras tres compensan |
| **Propulsores de gas frío** | Control grueso y desaturación de ruedas | 8 propulsores, 1-5 N de empuje | Pares redundantes |
| **Sensores estelares** | Referencia absoluta | 2 unidades | Cruzada |
| **Giroscopios** | Velocidad angular | 3 ejes | Redundantes |
| **Magnetómetros** | Referencia del campo magnético terrestre (respaldo) | 3 ejes | Opcional |

---

## Arquitectura de Control

```
[SENSORES ESTELARES] → [ORIENTACIÓN ABSOLUTA] → [CONTROLADOR]
[GIROSCOPIOS] → [VELOCIDAD ANGULAR] → [CONTROLADOR]
        ↓
[COMPARADOR] → [ERROR DE ORIENTACIÓN] → [ALGORITMO DE CONTROL]
        ↓
[RUEDAS DE REACCIÓN] → [TORQUE FINO] → [NAVE]
[PROPULSORES DE GAS FRÍO] → [TORQUE GRUESO] → [NAVE]
```

---

## Modos de Operación

| Modo | Descripción | Actuadores principales |
|:---|:---|:---|
| **Nominal** | Mantiene orientación constante para captura y comunicaciones | Ruedas de reacción |
| **Maniobra** | Cambia rápidamente de orientación (ej: apuntar branquias a un fragmento) | Ruedas de reacción + gas frío |
| **Desaturación** | Descarga el momento angular acumulado en las ruedas | Propulsores de gas frío |
| **Emergencia** | Mantiene orientación mínima (antena apuntando a Tierra, modo seguro) | Gas frío (ruedas apagadas) |

---

## Orientaciones Típicas

| Modo | Orientación | Justificación |
|:---|:---|:---|
| **Captura** | Eje de la nave alineado con la dirección de la basura | Las branquias miran hacia los fragmentos entrantes |
| **Comunicaciones** | Antena de alta ganancia apuntando a Tierra | Enlace de datos continuo |
| **Aerobraking** | Nave orientada para minimizar área expuesta | Proteger zonas sensibles |
| **Modo seguro** | Antena omnidireccional activa, paneles (si los hubiera) al Sol | Máxima supervivencia |

---

## Control en Detalle

### Ruedas de Reacción

| Parámetro | Valor |
|:---|:---|
| Número | 4 (configuración tetraédrica) |
| Momento angular máximo | 50 Nms por rueda |
| Torque máximo | 0.5 Nm por rueda |
| Consumo | 10-50 W por rueda |

### Propulsores de Gas Frío

| Parámetro | Valor |
|:---|:---|
| Número | 8 (pares en cada eje) |
| Empuje | 1-5 N por propulsor |
| Combustible | Nitrógeno (N₂) o xenón (Xe) |
| Capacidad | Suficiente para 100 desaturaciones |

---

## Integración con el Cerebro

El cerebro de Goliat recibe la orientación actual de los sensores y la orientación deseada según la tarea (captura, comunicación, aerobraking). Calcula la diferencia y envía comandos a las ruedas de reacción y propulsores de gas frío.

| Tarea | Orientación deseada | Prioridad |
|:---|:---|:---|
| Captura de fragmento | Branquias hacia el fragmento | Alta |
| Comunicación con Tierra | Antena hacia la estación terrestre | Media (puede esperar) |
| Aerobraking | Perfil aerodinámico mínimo | Alta (durante la maniobra) |
| Modo seguro | Antena omnidireccional activa | Máxima |

---

## Redundancia y Seguridad

| Aspecto | Estrategia |
|:---|:---|:---|
| **Fallo de una rueda de reacción** | 4 ruedas en configuración tetraédrica; si una falla, las otras tres pueden controlar la nave con degradación aceptable. |
| **Fallo de sensores estelares** | Giroscopios integran la orientación; la deriva es lenta (grados por hora). |
| **Fallo de todos los sensores** | Modo seguro: se apagan sistemas no esenciales, se activa el enlace de emergencia, se espera instrucciones. |
| **Fallo de propulsores de gas frío** | Las ruedas de reacción pueden operar sin desaturar por períodos cortos; la deriva se controla con la orientación de la nave. |

---

## Ventajas del Diseño

| Ventaja | Implicación |
|:---|:---|:---|
| **Precisión** | Ruedas de reacción permiten un control fino, esencial para apuntar las branquias. |
| **Redundancia** | Múltiples actuadores y sensores; no hay punto único de fallo. |
| **Eficiencia** | Ruedas de reacción consumen solo electricidad; el gas frío se usa solo para desaturar. |
| **Autonomía** | El cerebro decide la orientación óptima según la tarea, sin intervención de Tierra. |

---

## Próximos Pasos

1. Selección de ruedas de reacción comerciales (Honeywell, Rockwell Collins, etc.)
2. Selección de propulsores de gas frío
3. Diseño del controlador (PID, LQR, etc.)
4. Integración con el cerebro de Goliat
5. Pruebas en simulador de actitud

---

*Documento v1.0 - Marzo 2026*
*Goliat-Orbital - Mackiber Labs*
