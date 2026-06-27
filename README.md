## Hipótesis

| Causa | Fase DT origen (E/D/I) | Insight de empatía | Supuesto central |
|---|---|---|---|
| Presión operativa y normalización de conductas inseguras. | Mapa de empatia (comentarios de los trabajadores) | "Todo se hace con afán y no hay tiempo para parar." | La presión operativa y la necesidad de cumplir tiempos de servicio favorecen la normalización de conductas inseguras, incrementando la probabilidad de accidentes laborales en los trabajadores de cocina. |

## Construcción Analítica

| Pregunta analítica | Variables (nombres exactos) | Tipo (Outcome / Explic / Control / Segmento) | Cálculo / Transformación | Métrica (nombre + fórmula) | Periodo / Segmento | Patrón esperado (si cierta) | Condición refutación |
|---|---|---|---|---|---|---|---|
| ¿Los periodos de mayor presión operativa presentan una mayor ocurrencia de accidentes laborales en comparación con los periodos de menor presión operativa? | accidentes_laborales | Outcome | Agrupar registros por `turno_trabajo`; sumar `accidentes_laborales` por período; calcular promedio de `volumen_pedidos`, `horas_trabajadas` y `cantidad_personal_turno` para cada turno analizado. | **Tasa de accidentalidad operativa.**<br>`(accidentes_laborales / cantidad_personal_turno) × 100` | Mensual | ≤ 10% | **≥ 15%** |
|  | `turno_trabajo` | Segmento |  |  |  |  |  |
|  | `cantidad_personal_turno` | Control |  |  |  |  |  |
|  | `volumen_pedidos` | Explic |  |  |  |  |  |
|  | `horas_trabajadas` | Explic |  |  |  |  |  |

## Decisión y Acción

| Valor esperado para usuario/ciudadano | Riesgo si falsa | Acción si confirma | Acción si refuta | Experimento analítico mínimo (query + visual 1 línea) | Estado (V/A/R) |
|---|---|---|---|---|---|
| Reducción significativa de accidentes laborales, disminución de incapacidades y mejora del bienestar y desempeño operativo de los trabajadores en cocina. | La empresa perdería eficiencia operativa y recursos al mantener estrategias insuficientes, mientras la accidentalidad laboral continuaría afectando la seguridad, productividad y bienestar de los trabajadores. | Implementar capacitaciones prácticas en los próximos dos días enfocadas en los riesgos más frecuentes dentro de cocina, ya que permite intervenir rápidamente el comportamiento preventivo de los trabajadores y generar impacto temprano. | Rediseñar la operación teniendo en cuenta un modelo de intervención integral centrado en el trabajador, incluyendo revisión de cargas laborales, pausas activas, acompañamiento emocional, liderazgo preventivo y participación del personal en decisiones de seguridad operacional. |  |  |
