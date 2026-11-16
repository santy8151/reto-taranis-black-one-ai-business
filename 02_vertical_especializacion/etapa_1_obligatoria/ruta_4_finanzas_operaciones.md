# Ruta 4 · Finanzas y operaciones — Etapa 1 (obligatoria)

**Insumo:** `05_Finanzas_Presupuesto_vs_Real.xlsx` + `06_Descripcion_del_proceso_operativo_SIPOC`.

## Diagnóstico financiero
| Concepto | Presupuesto | Real | Variación |
|---|---|---|---|
| Ingresos netos | 39,78 M | 39,02 M | −1,9 % |
| Lucro bruto | 19,70 M | 18,43 M | −6,4 % |
| Fletes y logística | 2,38 M | 3,74 M | **+57 %** |
| Reentregas y multas | 0,21 M | 0,73 M | **+245 %** |
| Provisión incobrables | 0,44 M | 1,11 M | +152 % |
| **EBITDA** | 9,85 M | 5,77 M | **−41 %** |
| **Lucro líquido** | 5,97 M | 3,11 M | −48 % |

El deterioro se acelera trimestre a trimestre (EBITDA T4: −65 % vs presupuesto).
*Calidad de datos:* la hoja de líneas de producto suma USD 47,4 M reales vs 39,0 M de ingresos netos del estado de resultados; verificar si uno es bruto y otro neto.

## Proceso As-Is (SIPOC)
Propuesta PDF → consulta manual a Serasa (40 min) → aprobación por e-mail del gerente → emisión NF-e/boletos en ERP legado (re-digitación) → e-mail manual al CD Joinville. Sin SOP, sin matriz de alzada, 3 hojas de cálculo desconectadas, sin SLA.

## Ishikawa (6M) — problema: cierre con 5 días de atraso y ciclo de facturación de 5 días
- **Método:** sin POP, aprobación gerencial para cualquier monto, sin verificación CIF/FOB.
- **Máquina:** ERP sin API, sin OCR, 3 planillas no sincronizadas.
- **Mano de obra:** sobrecarga y burnout, líder que centraliza aprobaciones.
- **Material:** propuestas incompletas, códigos de producto discordantes con el ERP.
- **Medición:** sin SLA en tiempo real; los retrasos se detectan a fin de mes.
- **Medio ambiente:** distancia comercial (São Paulo) ↔ CD (Joinville), cultura reactiva.

## Proceso To-Be (Lean + IA, con humano en el bucle)
| Paso | Mejora | Antes → Después |
|---|---|---|
| 1 | IA/OCR extrae datos de la propuesta y valida CNPJ, IE y códigos contra tabla de precios | digitación manual → validación automática |
| 2 | Consulta Serasa por API/lote; IA arma ficha de crédito | 40 min → < 5 min |
| 3 | **Matriz de alzada**: montos bajos aprobación automática bajo reglas; altos al gerente | 48 h → ≤ 4 h |
| 4 | Generación de NF-e/boleto desde datos validados (revisión humana por muestreo) | divergencia 6,8 % → < 1,5 % |
| 5 | Orden de expedición generada del mismo dato; chequeo CIF/FOB | fletes de emergencia 2,8 % → ≤ 1,5 % |
| 6 | Panel SLA y alertas de cobranza automática | detección a fin de mes → tiempo real |

## Valor estimado (hipótesis a validar)
| Palanca | Costo actual | Captura supuesta | Ahorro |
|---|---|---|---|
| Crédito rápido | 1.250.000 | 50 % | 625.000 |
| Fletes/reentregas | 960.000 | 50 % | 480.000 |
| Incobrables | 1.110.000 | 30 % | 333.000 |
| Boletos | 390.000 | 70 % | 273.000 |
| Cierre | 180.000 | 60 % | 108.000 |
| **Total** | **3.890.000** | | **≈ 1.819.000/año** |

Los porcentajes de captura son supuestos del autor, no datos del kit.

**Prompt:** [prompt_finanzas_operaciones.md](../../03_prompts_y_skills/prompt_finanzas_operaciones.md)
