# Ruta 1 · Ventas y gestión comercial — Etapa 1 (obligatoria)

**Insumo:** `02_Prospectos_B2B_Comercial.xlsx` (20 prospectos, **USD 4,69 M** en pipeline) + catálogo.

## Diagnóstico
Las 5 objeciones del CRM frenan los negocios: precio, presupuesto congelado, proveedor actual, plazo de entrega y customización. Ejemplos: Vanguarda Softwares (USD 801.900, CAPEX congelado), Studio Alfa (USD 635.500, tejido Pantone), LogiMax (USD 65.880, pide 25 % de descuento).

## Solución: asistente consultivo de objeciones
| Objeción | Enfoque con IA (no rebajar precio) | Evidencia a citar |
|---|---|---|
| Precio | Pasar de precio a **TCO** y riesgo NR-17 | Garantía 5 años, informe ABERGO |
| Presupuesto | Reencuadrar como mitigación de riesgo; **pago 30/60/90** o modelo "as a service" | Ahorro por menos certificados médicos |
| Proveedor actual | **Piloto sin compromiso** (2 puestos × 15 días) en lugar de reemplazo | Soporte ergonomista |
| Plazo | Stock regulador del CD de Santa Catarina, entrega escalonada | Plazos y política CIF/FOB del catálogo |
| Customización | Ingeniería de aplicación, biblioteca BIM/Revit, tejidos a medida | Catálogo, equipo de proyectos |

## Flujo con humano en el bucle
1. El CRM exporta el prospecto → la IA clasifica la objeción y redacta e-mail/propuesta.
2. El ejecutivo revisa datos (precios, plazos) contra el catálogo.
3. Descuentos y condiciones especiales: aprobación del coordinador.
4. Se registra el resultado en el CRM y en el log HITL.

## Priorización del pipeline (propuesta)
Puntaje = valor × probabilidad (estado en el embudo) ÷ complejidad. Primero: Vanguarda (plan 12× / as-a-service), Studio Alfa (customización), Atlas (plazo de 30 días para informe ABERGO).

## KPIs
Tasa de respuesta a objeciones < 24 h · conversión de propuestas enviadas · ciclo de venta (−20 %) · descuento medio.

**Prompt:** [prompt_ventas_objeciones.md](../../03_prompts_y_skills/prompt_ventas_objeciones.md)
