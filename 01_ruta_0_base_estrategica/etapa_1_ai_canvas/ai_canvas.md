# Ruta 0 · Etapa 1 — AI Canvas y casos de uso

> Fuente: kit de datos Taranis Black (archivos 01–06). Cifras en USD.

## 1. Contexto del negocio
Taranis Black fabrica mobiliario corporativo ergonómico (ErgoPro, SmartDesk, Silence y periféricos) con foco B2B, alineado a la NR-17. Ingresos reales del ejercicio: **USD 39,0 M** (presupuesto 39,8 M) y **EBITDA 5,77 M vs 9,85 M presupuestado (−41 %)**. Plantilla: 280 personas, rotación 22,8 %.

## 2. Problemas medibles detectados (dolores)
| # | Dolor | Evidencia | Impacto anual |
|---|---|---|---|
| 1 | Homologación de crédito lenta | 48 h vs meta 4 h | USD 1.250.000 en pedidos cancelados |
| 2 | Fletes de emergencia y reentregas | 2,8 % vs 0,8 % de la facturación | USD 960.000 |
| 3 | Inadimplencia B2B > 90 días | 3,4 % vs 1,2 % | USD 1.110.000 |
| 4 | Boletos/NF-e con divergencias | 6,8 % vs < 0,5 % | USD 390.000 |
| 5 | Cierre contable tardío | 7 vs 2 días hábiles | USD 180.000 |
| 6 | Rotación en Atención (38,5 %) y Comercial (30,9 %) | Salidas por falta de claridad, sobrecarga manual | Costo de reposición no cuantificado en el kit |
| 7 | Ciclo de venta largo y objeciones recurrentes | 20 prospectos, USD 4,69 M en pipeline | Ventas perdidas/retrasadas |
| **Total cuantificado (1–5)** | | | **≈ USD 3,89 M** |

## 3. AI Canvas
| Bloque | Contenido |
|---|---|
| **Objetivo de negocio** | Recuperar margen y EBITDA, acelerar el ciclo pedido→cobro y retener talento, con IA supervisada por humanos. |
| **Usuarios / beneficiarios** | Ventas B2B, Marketing, RR. HH., Finanzas/Operaciones, dirección. |
| **Datos disponibles** | CRM de prospectos, catálogo, guía de tono, base de colaboradores y encuesta de clima, P&L presupuesto vs real, SIPOC. Todos sintéticos. |
| **Tareas de IA** | Clasificar, resumir, redactar, extraer datos de PDF, analizar sentimiento, detectar anomalías, proyectar. |
| **Modelo / herramientas** | LLM generalista (ChatGPT / Gemini / Claude) con instrucciones de sistema y Skills versionadas en este repo. |
| **Supervisión humana (HITL)** | Toda salida se revisa antes de uso externo; decisiones de crédito, salida de personal y precios requieren aprobación humana. |
| **Riesgos** | Alucinaciones, sesgo en RR. HH., fuga de datos personales (LGPD), decisiones de crédito automatizadas. |
| **Métricas de éxito** | Ver sección 5. |

## 4. Casos de uso candidatos
| ID | Ruta | Caso de uso |
|---|---|---|
| CU-1 | Ventas | Asistente de respuesta a objeciones + propuestas personalizadas por prospecto |
| CU-2 | Marketing | Gem/GPT de marca que adapta el artículo NR-17 a LinkedIn, Instagram y e-mail |
| CU-3 | RR. HH. | Análisis de rotación y sentimiento de la encuesta de clima |
| CU-4 | Finanzas/Ops | Extracción con OCR/IA de propuestas PDF → orden de venta/expedición, y panel de seguimiento SLA |
| CU-5 | Finanzas | Pre-análisis de crédito con matriz de alzada (la aprobación final es humana) |
| CU-6 | Finanzas | Recordatorios de cobranza automáticos y proyección de flujo |
| CU-7 | Transversal | Asistente interno de políticas y onboarding |

## 5. KPIs objetivo (a validar)
Homologación de crédito 48 h → ≤ 4 h · Cierre contable 7 → 2–3 días · Divergencia en boletos 6,8 % → < 1,5 % · Fletes de emergencia 2,8 % → ≤ 1,5 % · Rotación primeros 90 días −30 %.
