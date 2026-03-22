# Propulsores de Hidracina - Respaldo de Emergencia

## Descripción

Los propulsores de hidracina son el sistema de propulsión de respaldo de Goliat-Orbital. Se utilizan solo en emergencias o maniobras que requieren alto empuje: cambio rápido de órbita, evasión de colisión, o corrección si falla el motor de respiración atmosférica. No son el sistema principal. Son el seguro.

---

## Especificaciones Técnicas

| Parámetro | Valor | Observación |
|:---|:---|:---|
| Tipo | Propulsores químicos monopropelente (hidracina) | Tecnología madura, usada en miles de satélites |
| Número de unidades | 12 | Distribuidos en pares alrededor de la nave |
| Empuje por unidad | 10-100 N | Alto, para maniobras rápidas |
| Impulso específico (Isp) | 200-250 s | Eficiencia moderada, suficiente para emergencias |
| Combustible | Hidracina (N₂H₄) | Almacenada en tanques presurizados |
| Capacidad total | 500-1.000 kg | Depende de la misión |
| Vida útil | 10+ años | El combustible no se degrada significativamente |

---

## Configuración

Los 12 propulsores están distribuidos en:

| Ubicación | Cantidad | Función |
|:---|:---|:---|
| **Proa** | 4 | Frenado, reducción de velocidad orbital |
| **Popa** | 4 | Aceleración, aumento de velocidad orbital |
| **Lateral (cada lado)** | 2 por lado | Control de inclinación y maniobras laterales |

Cada propulsor puede girar (gimbaling) para orientar el empuje en diferentes direcciones, aumentando la capacidad de maniobra.

---

## Ciclo de Operación

| Modo | Descripción | Consumo de combustible |
|:---|:---|:---|
| **Emergencia** | Evasión de colisión, requiere empuje máximo | Alto |
| **Cambio de órbita** | Ascenso rápido a mayor altitud (ej: 300 km → 600 km) | Alto |
| **Respaldo** | Si falla el motor de respiración, se usa para mantener órbita | Bajo, mantenimiento |
| **Prueba** | Encendido periódico para verificar funcionamiento | Muy bajo |

---

## Almacenamiento de Combustible

| Componente | Función | Tecnología |
|:---|:---|:---|
| **Tanques** | Almacenan hidracina a presión | Titanio o acero inoxidable, recubrimiento interno |
| **Válvulas** | Controlan el flujo hacia los propulsores | Electromecánicas, redundantes |
| **Presurización** | Mantiene la presión del tanque | Gas helio (almacenado en tanques separados) |
| **Sensores** | Miden presión, temperatura, nivel de combustible | Redundantes |

---

## Integración con el Sistema Principal

| Situación | Acción |
|:---|:---|
| **Motor de respiración operativo** | Propulsores de hidracina apagados. Solo se usan en emergencia o cambio de órbita. |
| **Fallo del motor de respiración** | Propulsores de hidracina mantienen la órbita hasta que se repare o se decida el reingreso. |
| **Cambio de órbita programado** | Se usan los propulsores para el impulso inicial; el motor de respiración corrige después. |
| **Evasión de colisión** | Propulsores de hidracina se activan inmediatamente para cambiar la trayectoria. |

---

## Redundancia y Seguridad

| Aspecto | Estrategia |
|:---|:---|:---|
| **Fallo de un propulsor** | 12 unidades independientes. Si falla uno, los otros compensan. |
| **Fuga de combustible** | Tanques de doble pared, sensores de presión, válvulas de cierre automático. |
| **Sobrecalentamiento** | Refrigeración pasiva, materiales resistentes, control de duración de encendido. |
| **Fallo de válvulas** | Válvulas redundantes en serie y paralelo. |

---

## Ventajas del Diseño

| Ventaja | Implicación |
|:---|:---|:---|
| **Tecnología probada** | Los propulsores de hidracina se usan en satélites desde hace décadas. Riesgo bajo. |
| **Alto empuje** | Permite maniobras rápidas que el motor de respiración no puede hacer. |
| **Independencia** | Funciona aunque falle el sistema principal de energía o captura de gas. |
| **Escalable** | La cantidad de combustible se ajusta según la duración de la misión. |

---

## Consumo Estimado

| Maniobra | Delta-V requerido | Combustible necesario (kg) | Observación |
|:---|:---|:---|:---|
| Evasión de colisión | 10-50 m/s | 10-50 | Por evento |
| Cambio de órbita (300→600 km) | 200-300 m/s | 200-300 | Eventual (1-2 veces por misión) |
| Mantenimiento de órbita (respaldo) | 1-2 m/s por mes | 1-2 por mes | Solo si falla el motor de respiración |

Con 500 kg de hidracina, Goliat tiene suficiente para varias emergencias y al menos un cambio de órbita.

---

## Próximos Pasos

1. Selección de propulsores comerciales (Aerojet Rocketdyne, Moog, etc.)
2. Diseño de tanques y sistema de presurización
3. Integración con el cerebro de Goliat (control de emergencia autónomo)
4. Pruebas de encendido en vacío

---

*Documento v1.0 - Marzo 2026*
*Goliat-Orbital - Mackiber Labs*
