# Bodega de Lingotes - Almacenamiento y Gestión de Inventario

## Descripción

La bodega de lingotes es el sistema de almacenamiento de Goliat-Orbital. Su función es recibir los lingotes producidos (compactados o fundidos), mantener un inventario actualizado en tiempo real, y preparar los lotes para su reingreso a Tierra o transferencia a otras naves en órbita. Es el último eslabón del proceso antes de la venta.

---

## Especificaciones Técnicas

| Parámetro | Valor | Observación |
|:---|:---|:---|
| Capacidad total | 10-20 toneladas | Depende de la misión |
| Número de estantes | 100-200 | Distribuidos en estanterías rotativas |
| Dimensiones por estante | 30×20×15 cm | Ajustable según formato del lingote |
| Material | Aluminio reforzado | Ligero, resistente |
| Control de temperatura | 15-25°C | Evita condensación y corrosión |
| Sistema de acceso | Brazos robóticos | Manipulación autónoma |

---

## Componentes

| Componente | Función | Tecnología |
|:---|:---|:---|
| **Estanterías rotativas** | Almacenan lingotes por tipo y fecha | Diseño compacto, acceso rápido |
| **Brazo robótico** | Coloca y retira lingotes | Control por visión computacional |
| **Sistema de identificación** | Registra cada lingote | Códigos QR o RFID |
| **Inventario digital** | Base de datos en tiempo real | Integrada con el cerebro de Goliat |
| **Contenedores de reingreso** | Prepara lotes para enviar a Tierra | Cápsulas reutilizables con escudo térmico |
| **Sistema de acoplamiento** | Transferencia a otras naves | Interfaz estándar (NASA/ESA) |

---

## Ciclo de Operación

| Fase | Acción | Duración |
|:---|:---|:---|
| **1. Recepción** | Brazo recibe lingote del molde o compactador | 30 s |
| **2. Registro** | Código QR leído, peso y tipo registrados | 5 s |
| **3. Almacenamiento** | Brazo coloca lingote en estante asignado | 30 s |
| **4. Preparación de lote** | Cerebro selecciona lingotes para reingreso o venta | Automático |
| **5. Carga** | Brazo retira lingotes y los coloca en contenedor | 1-2 min por lote |

---

## Tipos de Almacenamiento

| Tipo | Formato | Ubicación | Destino |
|:---|:---|:---|:---|
| **Chatarra compactada** | Bloques de 10-20 kg | Estantes específicos | Reingreso a Tierra (venta como material reciclado) |
| **Lingotes de aluminio** | 5-10 kg | Estantes de alta rotación | Venta en órbita o reingreso |
| **Lingotes de cobre** | 5-10 kg | Estantes con control de humedad | Venta en órbita (prioridad) |
| **Lingotes de Fe-W** | 5-10 kg | Estantes de alta seguridad | Venta estratégica (blindaje, contrapesos) |
| **Plata** | Pequeñas barras | Estantes de alta seguridad | Venta de alto valor |

---

## Inventario Digital

| Campo | Descripción |
|:---|:---|
| ID único | Identificador de cada lingote |
| Tipo de metal | Al, Cu, Fe-W, Ag, etc. |
| Masa | Peso exacto (gramos) |
| Pureza | Porcentaje estimado (en fase de fundición) |
| Fecha de producción | Timestamp de fabricación |
| Ubicación | Estante y posición en la bodega |
| Destino | Pendiente, asignado a reingreso, vendido en órbita |

El inventario es accesible desde Tierra en tiempo real.

---

## Logística de Salida

### Reingreso a Tierra

| Fase | Acción |
|:---|:---|
| 1 | Cerebro selecciona lote de lingotes (ej: 500 kg de aluminio) |
| 2 | Brazo carga los lingotes en un contenedor de reingreso |
| 3 | Contenedor se sella y se acopla a la nave de reingreso (o se expulsa con su propio escudo térmico) |
| 4 | Contenedor reingresa controladamente y es recuperado en Tierra |

### Venta en Órbita

| Fase | Acción |
|:---|:---|
| 1 | Cliente (fabricante de satélites) acuerda compra |
| 2 | Cerebro prepara lote de lingotes |
| 3 | Nave cliente se acopla a Goliat (o Goliat envía lingotes en cápsula pequeña) |
| 4 | Transferencia de propiedad registrada en inventario |

---

## Redundancia y Seguridad

| Aspecto | Estrategia |
|:---|:---|
| **Fallo del brazo robótico** | Brazo secundario de respaldo, o acceso manual remoto (control desde Tierra) |
| **Pérdida de inventario** | Registro local redundante, copia en Tierra cada 24 h |
| **Contenedor de reingreso falla** | Diseño probado (SpaceX, NASA), sistema de respaldo con paracaídas |
| **Robo o pérdida** | Cada lingote tiene código QR único, trazabilidad completa |

---

## Ventajas del Diseño

| Ventaja | Implicación |
|:---|:---|
| **Inventario en tiempo real** | Los clientes pueden saber cuánto hay disponible sin consultar |
| **Logística flexible** | Se puede vender en órbita o reingresar según mejor oferta |
| **Trazabilidad** | Cada lingote tiene registro completo de origen, procesamiento y destino |
| **Escalable** | Capacidad de almacenamiento ajustable según misión |

---

## Próximos Pasos

1. Diseño de estanterías rotativas (compactación, acceso rápido)
2. Selección de sistema de identificación (QR o RFID)
3. Integración con el cerebro de Goliat (inventario digital)
4. Definición de contenedores de reingreso (tamaño, peso, sistema de frenado)

---

*Documento v1.0 - Marzo 2026*
*Goliat-Orbital - Mackiber Labs*
