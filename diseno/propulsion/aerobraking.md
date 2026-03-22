# Aerobraking - Frenado Atmosférico sin Combustible

## Descripción

El aerobraking es una técnica de maniobra orbital que utiliza la fricción de la atmósfera residual para reducir la velocidad de la nave sin consumir combustible. Consiste en realizar pasadas rasantes a la atmósfera terrestre (en órbitas elípticas con perigeo bajo) que, en cada vuelta, disminuyen la energía orbital de la nave.

En Goliat-Orbital, el aerobraking se usa para:
- Descender de órbita cuando se termina la misión.
- Cambiar a una órbita con mayor densidad de basura.
- Ajustar la altitud sin gastar combustible de respaldo.

---

## Principio de Funcionamiento

1. La nave se coloca en una órbita elíptica con el perigeo (punto más bajo) dentro de la atmósfera residual (80-120 km).
2. En cada pasada, la fricción con las moléculas de gas reduce la velocidad de la nave.
3. El apogeo (punto más alto) disminuye gradualmente.
4. Después de varias pasadas, la órbita se vuelve circular a menor altitud.

Todo el proceso se realiza sin encender motores. Solo se requiere un pequeño impulso inicial para bajar el perigeo (que puede darse con el motor de respiración atmosférica o con los propulsores de hidracina).

---

## Especificaciones Técnicas

| Parámetro | Valor | Observación |
|:---|:---|:---|
| Altitud de perigeo | 80-120 km | Suficiente para sentir fricción atmosférica |
| Reducción de velocidad por pasada | 10-100 m/s | Depende de la densidad atmosférica |
| Número de pasadas | 10-100 | Según el cambio de altitud deseado |
| Duración total | Días a semanas | Depende del cambio orbital |
| Protección térmica | Space Armor (zona de fricción) | Resiste temperaturas de reentrada parcial |

---

## Ciclo de Operación

| Fase | Acción | Duración |
|:---|:---|:---|
| **1. Preparación** | La nave se orienta para proteger zonas sensibles (branquias cerradas, módulo rotatorio alineado) | Minutos |
| **2. Descenso inicial** | Motor de respiración o hidracina baja el perigeo a 100 km | Pulsos cortos |
| **3. Pasadas sucesivas** | La nave orbita, fricción reduce velocidad gradualmente | Días |
| **4. Verificación** | Sensores miden la nueva altitud; se repite hasta alcanzar la órbita deseada | Cada pasada |
| **5. Estabilización** | Una vez alcanzada la órbita, se usa el motor de respiración para circularizar | Horas |

---

## Integración con la Nave

| Componente | Función |
|:---|:---|
| **Space Armor** | Protege la nave durante las pasadas de alta fricción |
| **Sensores de altitud** | Miden la posición orbital en tiempo real |
| **Sistema de control de actitud** | Orienta la nave para minimizar resistencia o proteger zonas sensibles |
| **Cerebro de Goliat** | Calcula el número de pasadas necesarias y ejecuta la maniobra |

---

## Protección Térmica

| Zona | Protección | Justificación |
|:---|:---|:---|
| **Casco frontal** | Space Armor (doble capa) | Mayor fricción durante el descenso |
| **Branquias** | Cerradas, selladas | Evitar entrada de gas caliente |
| **Módulo rotatorio** | Alineado con la dirección de vuelo | Minimizar área expuesta |
| **Zonas sensibles** (computadores, depósitos) | Blindaje adicional | Protección extra |

---

## Ventajas del Aerobraking

| Ventaja | Implicación |
|:---|:---|
| **Cero combustible** | No consume hidracina ni metal fundido. Solo usa fricción atmosférica. |
| **Sin partes móviles** | No requiere activación de motores. Solo orientación de la nave. |
| **Precisión** | Se puede controlar el descenso con gran exactitud (metros por pasada). |
| **Seguridad** | Si algo falla, la nave no se estrella; sigue en órbita elíptica. |

---

## Riesgos y Mitigación

| Riesgo | Mitigación |
|:---|:---|
| **Sobrecalentamiento** | Space Armor resiste temperaturas de reentrada parcial |
| **Pérdida de control** | Sistema de actitud redundante; si falla, se aborta la maniobra |
| **Fricción imprevista** | Sensores de temperatura; si se excede el límite, se eleva el perigeo |

---

## Aplicaciones en Goliat-Orbital

| Escenario | Uso del aerobraking |
|:---|:---|
| **Fin de misión** | Descenso controlado para reingreso de la nave (o desintegración segura) |
| **Cambio de órbita** | Pasar de 400 km a 300 km para acceder a mayor densidad de basura |
| **Respaldo** | Si fallan los motores de respiración, se puede usar aerobraking para bajar y luego usar hidracina para circularizar |

---

## Próximos Pasos

1. Simulación de trayectorias de aerobraking con software orbital (STK, GMAT)
2. Cálculo del número de pasadas necesarias para cada cambio de altitud
3. Diseño de protocolo de seguridad (límites de temperatura, aborto de maniobra)
4. Integración con el sistema de navegación y el cerebro de Goliat

---

*Documento v1.0 - Marzo 2026*
*Goliat-Orbital - Mackiber Labs*
