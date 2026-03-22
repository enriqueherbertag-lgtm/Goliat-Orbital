# Principio de Captura de Goliat-Orbital

## La Lógica

No se persiguen fragmentos. No se espera a que estén cerca para activar la succión. Se **anticipa**.

La nave orbita en la misma trayectoria que los fragmentos. La velocidad relativa es casi cero. Los sensores detectan un fragmento a cientos de metros. El computador calcula cuándo estará en la zona de influencia de la branquia. Los compresores se encienden con antelación. Cuando el fragmento llega, ya hay un flujo estable de gas arrastrándolo hacia el interior.

## El Ciclo

| Fase | Acción | Efecto |
|:---|:---|:---|
| **Detección** | Sensores identifican fragmento a 500 m | Se calcula trayectoria y tiempo de llegada |
| **Preparación** | Compresores se encienden con antelación (T-10 s) | Se genera un flujo continuo de gas hacia la branquia |
| **Aproximación** | Fragmento entra en la zona de influencia | El flujo ya está estable, arrastra el fragmento |
| **Entrada** | Fragmento es conducido hacia la branquia | Entra sin impacto, sin turbulencias |
| **Procesamiento** | Fragmento dentro de la nave | Listo para compactar o fundir |

## Ventajas

| Aspecto | Beneficio |
|:---|:---|
| **Velocidad relativa** | Casi cero (nave en misma órbita) |
| **Consumo energético** | Compresores en régimen estable, no en picos |
| **Riesgo de impacto** | Nulo (el fragmento es arrastrado, no choca) |
| **Precisión** | No se necesita apuntar, solo anticipar |
| **Redundancia** | Seis branquias independientes, cada una con sus sensores y compresores |

## Implementación

Cada branquia tiene:

- **Sensores de proximidad** (radar/lidar/ópticos) con alcance de hasta 500 m
- **Compresor independiente** (uno por branquia)
- **Tobera saxofón** (dirige el flujo hacia el interior)
- **Compuerta** (se abre cuando el fragmento está en la zona de influencia)

La nave orbita con las branquias cerradas. Cuando los sensores detectan un fragmento, se abre la compuerta correspondiente y se activa su compresor. El flujo se establece antes de que el fragmento llegue. Cuando entra, es arrastrado suavemente hacia el interior.
