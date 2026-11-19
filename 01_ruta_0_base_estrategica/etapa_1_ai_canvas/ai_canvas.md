# Ruta 0 · Etapa 1 — AI Canvas y 3 casos de uso prioritarios

> Fuente: kit de datos Taranis Black (`00_kit_datos_originales/archivos/` 01–06). Cifras en USD.

## 1. Contexto del negocio
Taranis Black fabrica mobiliario corporativo ergonómico (*ErgoPro*, *SmartDesk*, *Silence* y periféricos) con foco B2B (70 % de los ingresos) y D2C (30 %), alineado a la norma NR-17.
- **Ingresos brutos reales:** USD 48,50 M (presupuesto 48,60 M) · **Ingresos netos reales:** USD 39,02 M (presupuesto 39,78 M; −1,9 %).
- **EBITDA real:** **USD 5,77 M vs USD 9,85 M presupuestados (−41,4 %)**, con deterioro acelerado en T3 (−55,6 %) y T4 (−65,3 %).
- **Lucro líquido:** USD 3,11 M vs USD 5,97 M presupuestados (−47,9 %).
- **Talento:** 280 colaboradores, 64 salidas en el último año (**22,86 %** rotación real; 38,5 % en Atención al cliente y 30,9 % en Comercial B2B), eNPS global +28.

## 2. Problemas medibles detectados (dolores)
| # | Dolor | Evidencia en el kit | Impacto anual |
|---|---|---|---|
| 1 | Homologación de crédito lenta | 48 h vs meta 4 h (40 min manuales en Serasa + espera gerencial) | **USD 1.250.000** en pedidos cancelados |
| 2 | Inadimplencia B2B > 90 días | 3,4 % vs meta 1,2 % (cobranza manual por e-mail) | **USD 1.110.000** en PDD |
| 3 | Fletes de emergencia y reentregas | 2,8 % vs meta 0,8 % de la facturación (errores de digitación al CD) | **USD 960.000** |
| 4 | Boletos/NF-e con divergencias | 6,8 % vs meta < 0,5 % (tabla comercial vs ERP desactualizado) | **USD 390.000** |
| 5 | Cierre contable tardío | 7 días hábiles vs meta 2 días (3 Excels desconectados) | **USD 180.000** |
| 6 | Rotación crítica en Atención (38,5 %) y Comercial (30,9 %) | 40,6 % de salidas citan liderazgo/objetivos y 31,2 % sobrecarga manual | Costo de reposición no cuantificado en el kit |
| 7 | Ciclo de venta B2B frenado por 5 objeciones | 20 prospectos activos, **USD 4.693.630** en pipeline | Ventas retrasadas/perdidas |
| **Total cuantificado (1–5)** | | | **USD 3.890.000 / año** |

## 3. AI Canvas Estratégico
| Bloque | Definición para Taranis Black |
|---|---|
| **Objetivo de negocio** | Recuperar margen operativo y EBITDA (−41,4 %), acelerar el ciclo pedido→cobro (48 h → ≤ 4 h) y reducir la rotación en áreas críticas, con IA supervisada por humanos. |
| **Usuarios / beneficiarios** | Finanzas & Operaciones (cierre, crédito y expedición), Ventas B2B, RR. HH. / Líderes, Marketing, Dirección. |
| **Datos disponibles** | `01_Catalogo`, `02_Prospectos_B2B_Comercial.xlsx`, `03_Marketing_Articulo_base`, `04_Base_de_colaboradores_People_Analytics.xlsx`, `05_Finanzas_Presupuesto_vs_Real.xlsx`, `06_SIPOC`. Todos sintéticos. |
| **Tareas de IA** | Extracción OCR/estructurada de PDFs, pre-scoring explicable, redacción consultiva grounded en catálogo, simulación roleplay de feedback 1:1, análisis de sentimiento agregado y detección de anomalías P&L. |
| **Modelo / herramientas** | LLM corporativo con retención cero (Gemini Gem / Custom GPT / Claude Artifacts) + OCR ligero + prompts y Skills versionados en GitHub. |
| **Supervisión humana (HITL)** | **Obligatoria:** decisiones de crédito, precios/descuentos, publicación externa y gestión de personas requieren aprobación humana explícita (LGPD art. 20). |
| **Riesgos** | Alucinaciones en precios o NR-17, fuga de PII, sesgos en People Analytics, automatización indebida de crédito. |
| **Métricas de éxito (KPIs)** | Homologación crédito 48 h → ≤ 4 h · Cierre contable 7 → 2–3 días · Boletos divergentes 6,8 % → < 1,5 % · Fletes emergencia 2,8 % → ≤ 1,5 % · Rotación primeros 90 días −30 % · Respuesta a objeciones < 24 h. |

## 4. Selección de los 3 Casos de Uso Prioritarios (Rúbrica Ruta 0 · Etapa 1)
De los 7 candidatos mapeados en el diagnóstico, se seleccionan **3 casos de uso prioritarios** por su impacto directo sobre EBITDA, pipeline comercial y retención:

| ID | Caso de uso seleccionado | Problema que ataca | Entrada / Datos | Salida de IA + HITL | KPI objetivo |
|---|---|---|---|---|---|
| **CU-1** | **Copiloto Order-to-Cash (OCR PDF + Pre-análisis de Crédito con Matriz de Alzada)** *(Finanzas/Ops)* | Crédito lento (48 h), fletes duplicados y boletos divergentes (**USD 2,60 M/año** combinados) | Propuesta PDF firmada, catálogo oficial, datos Serasa, tabla CIF/FOB | Ficha validada de pedido + dictamen sugerido según alzada; **Gerente Financiero aprueba crédito** | Crédito ≤ 4 h · Boletos < 1,5 % · Fletes ≤ 1,5 % |
| **CU-2** | **Asistente Consultivo de Objeciones y Propuestas B2B** *(Ventas)* | 5 objeciones frenan **USD 4,69 M** en 20 prospectos sin caer en descuentos | Ficha CRM del prospecto + extracto oficial del catálogo | Clasificación de objeción + e-mail ≤ 150 palabras + secuencia 30/60/90 o piloto; **Ejecutivo verifica precios/plazos** | Respuesta < 24 h · Ciclo −20 % · Sin descuentos no autorizados |
| **CU-3** | **Simulador de Feedback 1:1 (SBI) + People Analytics Agregado** *(RR. HH.)* | Rotación de 38,5 % (Atención) y 30,9 % (Comercial); **40,6 %** de salidas citan liderazgo y claridad | Escenarios anónimos de clima + tabla agregada por área (sin PII) | Entrenamiento roleplay con rúbrica 1–5 para líderes + alertas agregadas; **RR. HH. decide acciones (sin score individual)** | Rotación Atención/Comercial −30 % · eNPS +10 pts |

### Backlog secundario (expansión de fase)
| ID | Caso de uso | Rol en la hoja de ruta |
|---|---|---|
| **CU-4** | Gem/GPT "Voz Taranis Black" (adaptación artículo NR-17 a LinkedIn, IG y e-mail) | Quick win de Marketing (Fase 1) |
| **CU-5** | Cobranza automatizada y proyección de flujo de caja | Escala financiera contra inadimplencia USD 1,11 M (Fase 3) |
| **CU-6** | Asistente interno de políticas y playbook de onboarding | Apoyo transversal para reducir salidas tempranas ≤ 90 días (Fase 2–3) |
