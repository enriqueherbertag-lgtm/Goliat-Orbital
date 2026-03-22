# Branquias - Sistema de Captura de Goliat-Orbital

## Descripción

Las branquias son las aberturas longitudinales en el casco de Goliat. Son seis, ubicadas en las seis caras del cilindro, cada una con su propio sistema de sensores, compresor, tobera saxofón y compuerta. Son la entrada de fragmentos y gas a la nave.

---

## Especificaciones Técnicas

| Parámetro | Valor |
|:---|:---|
| Número de branquias | 6 |
| Ubicación | Distribución hexagonal en el casco cilíndrico |
| Longitud | 10 m (aproximadamente 1/3 de la nave) |
| Apertura máxima | 2.5 m (para admitir fragmentos de hasta 2.5 m) |
| Apertura en modo espera | Cerrada (protege contra impactos) |
| Apertura en modo captura | Variable según tamaño del fragmento |
| Material | Acero reforzado con recubrimiento anti-impacto (Space Armor en borde) |

---

## Componentes por Branquia

| Componente | Función |
|:---|:---|
| **Sensores de proximidad** | Detectan fragmentos a cientos de metros |
| **Compresor** | Genera flujo de gas para arrastrar fragmentos |
| **Tobera saxofón** | Concentra y acelera el flujo hacia el interior |
| **Compuerta** | Abre cuando el fragmento está en la zona de influencia |
| **Cámara de entrada** | Recibe el fragmento y lo conduce al interior |

---

## Ciclo de Operación

| Fase | Acción |
|:---|:---|
| **1. Detección** | Sensores detectan fragmento a 500 m. Se calcula trayectoria y tiempo de llegada. |
| **2. Preparación** | Compresor se enciende con antelación (T-10 s). Se genera flujo continuo. |
| **3. Apertura** | Compuerta se abre cuando el fragmento está en la zona de influencia. |
| **4. Arrastre** | El flujo de gas arrastra el fragmento hacia la tobera saxofón. |
| **5. Entrada** | El fragmento entra suavemente a la nave, sin impacto. |
| **6. Cierre** | Compuerta se cierra después de la entrada. El ciclo continúa con otro fragmento o se apaga. |

---

## Redundancia y Seguridad

| Aspecto | Estrategia |
|:---|:---|
| **Fallos** | Cada branquia es independiente. Si falla una, las otras cinco siguen operando. |
| **Impacto accidental** | Compuerta cerrada protege la nave en modo espera. |
| **Atascos** | Sensores de obstrucción detectan si un fragmento se traba; se activan contraflujos o se abre otra branquia para aliviar presión. |

---

## Integración con la Nave

| Elemento | Conexión |
|:---|:---|
| **Estructura** | Las branquias son parte integral del casco, reforzado en los bordes con Space Armor. |
| **Sensores** | Conectados al computador de navegación y al sistema de IA a bordo. |
| **Compresores** | Alimentados por la red eléctrica de la nave (paneles solares + baterías). |
| **Compuertas** | Controladas por actuadores electromecánicos, con respaldo manual desde Tierra. |

---

## Ventajas del Diseño

| Ventaja | Implicación |
|:---|:---|
| **Seis branquias** | Redundancia, mayor área de captura, capacidad de procesar múltiples fragmentos simultáneamente |
| **Compresor por branquia** | Flujo independiente, menor consumo energético al activar solo las necesarias |
| **Apertura variable** | Adaptación al tamaño del fragmento, menor pérdida de gas |
| **Flujo anticipado** | El fragmento es arrastrado, no impacta. No necesita desaceleración. |

---

## Próximos Pasos

1. Simulación de flujo de gas en tobera saxofón
2. Selección de compresores (capacidad, consumo, tamaño)
3. Diseño de compuertas (mecanismo, sellado, control)
4. Integración con sistema de sensores (radar/lidar/ópticos)

---

*Documento v1.0 - Marzo 2026*
*Goliat-Orbital - Mackiber Labs*
