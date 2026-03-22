# Arquitectura del Sistema - Goliat-Orbital

## Capas Funcionales

Goliat-Orbital está organizado en siete capas funcionales, cada una con componentes específicos y un flujo claro de materiales, energía e información.

---

## 1. Protección

| Componente | Función | Tecnología |
|:---|:---|:---|
| **Casco estructural** | Sostén de toda la nave | Cilindro con seis branquias, ancho en el centro |
| **Space Armor** | Protección contra micrometeoritos | Paneles de 2.54 cm, resiste impactos de 3 mm a 7 km/s |
| **Blindaje en zonas críticas** | Doble capa en tolva, cámara de procesamiento, depósitos | Integración de Space Armor |

---

## 2. Captura

| Componente | Función | Tecnología |
|:---|:---|:---|
| **Seis branquias** | Entrada de fragmentos | Aberturas longitudinales, cada una con compresor independiente |
| **Sensores de proximidad** | Detección de fragmentos a cientos de metros | Radar / lidar / ópticos |
| **Compresores** | Generan flujo de gas para arrastrar fragmentos | Unidad por branquia (6 total) |
| **Tobera saxofón** | Concentra y dirige el flujo hacia el interior | Geometría convergente |
| **Compuerta** | Abre cuando el fragmento está en la zona de influencia | Diseño hermético |

---

## 3. Procesamiento (Fase 1: Compactación)

| Componente | Función | Tecnología |
|:---|:---|:---|
| **Tolva de recepción** | Almacenamiento temporal | Contenedor reforzado con amortiguadores |
| **Compactador** | Reduce volumen de fragmentos | Prensas hidráulicas |
| **Bodega de material compactado** | Almacenamiento para reingreso | Contenedores estandarizados |

---

## 4. Procesamiento (Fase 2: Fundición)

| Componente | Función | Tecnología |
|:---|:---|:---|
| **Módulo rotatorio** | Genera gravedad artificial (0.1-0.3 g) | Giratorio, acoplado al cuerpo principal |
| **Válvulas de alivio** | Usan presión del proceso para generar rotación | Toberas tangenciales |
| **Horno convencional** | Funde metales | Resistencia o inducción con crisol |
| **Molde por inyección** | Forma lingotes | Inyección a presión en moldes de dos mitades |
| **Bodega de lingotes** | Almacenamiento para venta | Estanterías rotativas, inventario digital |

---

## 5. Propulsión y Mantenimiento Orbital

| Componente | Función | Tecnología |
|:---|:---|:---|
| **Motor de respiración atmosférica** | Corrección fina de órbita | Toma de gas atmosférico + ionización |
| **Aerobraking** | Descenso de órbita sin combustible | Uso de la atmósfera residual como freno |
| **Propulsores de hidracina** | Respaldo para emergencias o cambios de órbita | Tecnología estándar |

---

## 6. Navegación y Control

| Componente | Función | Tecnología |
|:---|:---|:---|
| **GPS / GNSS** | Posicionamiento absoluto | Tecnología madura |
| **Sensores estelares** | Orientación de la nave | Tecnología madura |
| **Giroscopios y acelerómetros** | Movimiento relativo | MEMS de alta precisión |
| **Ruedas de reacción** | Control de actitud | Tecnología estándar |
| **Antena banda X** | Enlace principal de datos | Alta velocidad, direccional |
| **Antena banda S** | Enlace de respaldo y emergencia | Omnidireccional, bajo consumo |
| **Estaciones terrestres** | Comunicación con Tierra | Red DSN / ESA / comercial |

---

## 7. Automatización y Control Remoto

| Nivel | Descripción | Tecnología |
|:---|:---|:---|
| **Autónomo** | La nave opera sola. Solo reporta estado. | IA a bordo, algoritmos de control predictivo |
| **Supervisado** | La nave opera sola, pero envía datos en tiempo real. Tierra puede intervenir. | Enlace continuo, supervisión humana |
| **Remoto** | Tierra toma el control total. La nave solo ejecuta comandos. | Interfaz de control remoto |
| **Modo seguro** | Ante una anomalía, la nave apaga todo, activa el enlace de emergencia y espera instrucciones. | Protocolo failsafe |

---

## Flujo Integrado

```
[PROTECCIÓN] Space Armor
        ↓
[CAPTURA] Sensores → compresores → tobera → compuerta → fragmento entra
        ↓
[PROCESAMIENTO] Tolva → compactador (fase 1) → módulo rotatorio → horno → molde (fase 2)
        ↓
[PRODUCTO] Lingotes de Al, Cu, Fe-W, Ag
        ↓
[ALMACENAMIENTO] Bodega rotativa → inventario digital
        ↓
[LOGÍSTICA] Reingreso controlado o transferencia en órbita
```

---

## Redundancia y Seguridad

| Sistema | Redundancia |
|:---|:---|
| Captura | Seis branquias independientes. Si falla una, las otras cinco siguen. |
| Propulsión | Motor de respiración + propulsores de hidracina. Si falla uno, el otro puede mantener la órbita. |
| Comunicaciones | Antenas banda X y banda S. Si falla una, la otra permite control remoto. |
| Energía | Paneles solares + baterías. Si falla la generación, las baterías dan tiempo para entrar en modo seguro. |
| Computadores | Unidad principal + respaldo. Si falla uno, el otro toma el control. |

---

*Documento v1.0 - Marzo 2026*
*Goliat-Orbital - Mackiber Labs*
