# Motor de Respiración Atmosférica - Mantenimiento Orbital

## Descripción

El motor de respiración atmosférica es el sistema de propulsión primario de Goliat-Orbital para el mantenimiento de órbita. En lugar de consumir combustible transportado desde Tierra, captura las partículas de gas de la atmósfera residual (presente en órbitas bajas de 200-400 km), las ioniza y las acelera para generar empuje. No requiere combustible externo.

---

## Especificaciones Técnicas

| Parámetro | Valor | Observación |
|:---|:---|:---|
| Tipo | Propulsor de iones con captura de gas atmosférico | Tecnología en desarrollo por ESA / Surrey Space Centre |
| Empuje | 10-100 mN | Suficiente para corregir órbita |
| Impulso específico (Isp) | 1.500-3.000 s | Muy eficiente en consumo de masa |
| Consumo eléctrico | 1-5 kW | Alimentado por energía recuperada del proceso |
| Gas capturado | Hidrógeno atómico (H), oxígeno atómico (O) | Presente en la termosfera (200-400 km) |
| Altitud de operación | 200-400 km | Región donde la atmósfera residual es utilizable |

---

## Principio de Funcionamiento

1. **Captura**: La nave toma gas atmosférico a través de una toma especial (una de las branquias en modo gas).
2. **Ionización**: El gas se convierte en plasma mediante descarga eléctrica o calentamiento por radiofrecuencia.
3. **Aceleración**: El plasma se acelera mediante un campo magnético (propulsor Hall) o una rejilla electrostática.
4. **Expulsión**: El plasma se expulsa a alta velocidad, generando empuje en dirección opuesta.

---

## Energía para el Motor

La energía necesaria para la ionización y aceleración proviene de:

| Fuente | Descripción |
|:---|:---|
| **Generadores termoeléctricos** | Convierten el calor residual del horno en electricidad (efecto Seebeck) |
| **Turbinas de flujo** | Aprovechan la velocidad del gas entrante para generar electricidad |
| **Generador acoplado al módulo rotatorio** | Convierte el movimiento de rotación en electricidad |
| **Baterías de respaldo** | Almacenan energía para picos de demanda o emergencias |

Ninguno de estos sistemas tiene partes expuestas al espacio exterior. Todo está integrado dentro de la estructura de la nave, protegido por Space Armor.

---

## Integración con Goliat

```
[BRANQUIA (modo gas)] → [IONIZADOR] → [ACELERADOR] → [CHORRO DE PLASMA]
        ↓
[TURBINA DE FLUJO] → [ENERGÍA ELÉCTRICA] → [SISTEMAS DE LA NAVE]
```

El sistema utiliza una de las branquias existentes en modo gas. La energía para la ionización viene del propio flujo de gas y del calor del proceso.

---

## Ciclo de Operación

| Modo | Función | Frecuencia |
|:---|:---|:---|
| **Mantenimiento continuo** | Corrección fina de órbita (compensa la fricción atmosférica) | Siempre activo (bajo empuje) |
| **Corrección programada** | Ajuste de órbita después de una captura masiva o impacto | Según necesidad |
| **Cambio de órbita** | Ascenso a mayor altitud (ej: 300 km → 500 km) | Raro, requiere respaldo de hidracina |

---

## Rendimiento por Altitud

| Altitud (km) | Densidad atmosférica (kg/m³) | Empuje disponible (mN) | Potencia requerida (kW) |
|:---|:---|:---|:---|
| 200 | 1 × 10⁻⁷ | 50-100 | 3-5 |
| 300 | 1 × 10⁻¹⁰ | 10-30 | 1-2 |
| 400 | 1 × 10⁻¹² | 1-5 | 0.5-1 |

A 200-300 km, el empuje es suficiente para mantener la órbita indefinidamente. Por encima de 400 km, la densidad es demasiado baja para ser práctica.

---

## Redundancia y Seguridad

| Aspecto | Estrategia |
|:---|:---|
| **Fallo del motor** | Propulsores de hidracina como respaldo para emergencias |
| **Atasco de la toma de gas** | Válvulas de purga, inversión de flujo |
| **Pérdida de plasma** | Cámaras de confinamiento magnético, sensores de presión |
| **Fallo de generación de energía** | Baterías de respaldo, modo de bajo consumo |

---

## Ventajas del Diseño

| Ventaja | Implicación |
|:---|:---|
| **Combustible infinito** | No necesita recarga. Opera mientras haya atmósfera residual. |
| **Sin paneles solares** | No hay partes frágiles expuestas al impacto de fragmentos. |
| **Energía del proceso** | Aprovecha calor residual, flujo de gas y rotación. |
| **Bajo peso** | No requiere tanques de combustible grandes. |

---

## Próximos Pasos

1. Selección del tipo de ionizador (descarga eléctrica vs. radiofrecuencia)
2. Diseño de las turbinas de flujo para aprovechar el gas entrante
3. Integración de generadores termoeléctricos en el horno
4. Pruebas en cámara de vacío con gas de baja densidad

---

*Documento v1.1 - Marzo 2026*
*Goliat-Orbital - Mackiber Labs*
