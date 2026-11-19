# Informe Ejecutivo — Consultoría de IA para Taranis Black
**Programa:** Oracle Next Education (ONE) + Alura | **Challenge:** AI Builder  
**Título sugerido en Google Docs:** `[Reto Taranis Black] — Ruta 4 (Finanzas y Operaciones) — [Tu Nombre Completo]`  
**Vertical principal declarada:** Ruta 4 · Finanzas y Operaciones *(con anexos opcionales de Rutas 1, 2 y 3)*

> **Cómo usar este archivo:** Copia y pega estas secciones directamente en tu copia de la plantilla oficial de Google Docs e inserta los pantallazos ubicados en `04_evidencias_hitl/capturas/`.

---

## 1. Resumen Ejecutivo
Taranis Black cerró el ejercicio con ingresos netos de **USD 39,02 M** (apenas −1,9 % frente a los USD 39,78 M presupuestados), pero sufrió una caída del **−41,4 % en su EBITDA** (**USD 5,77 M reales vs USD 9,85 M presupuestados**), acelerada en el segundo semestre (T4: −65,3 %). El análisis del kit financiero y operativo demuestra que el problema no es falta de demanda, sino **USD 3.890.000/año en pérdidas por fricción operativa** (homologación manual de crédito de 48 h, inadimplencia > 90 días, fletes de emergencia, boletos divergentes y cierre contable tardío) junto con una rotación de **22,86 %** (38,5 % en Atención al Cliente y 30,9 % en Comercial B2B).

Esta consultoría diseña una arquitectura práctica de **IA con Humano en el Bucle (HITL)** y cumplimiento **LGPD**, capaz de capturar un ahorro base estimado de **USD 1.819.000/año** (ROI Año 1 de **2.015 %** sobre una inversión estimada de **USD 86.000**, con *payback* < 1 mes).

---

## 2. Ruta 0 · Base Estratégica (Obligatorio)

### 2.1 Etapa 1 — Oportunidades: AI Canvas y 3 Casos de Uso Prioritarios
*(Insertar captura estilo Canva: `04_evidencias_hitl/capturas/vista_canva_ai_canvas_estrategico.png`)*
- **Objetivo de negocio:** Recuperar margen y EBITDA, reducir el ciclo pedido→cobro de 48 h a ≤ 4 h y mitigar la rotación temprana.
- **Datos disponibles (sintéticos):** Catálogo oficial (`01`), 20 prospectos CRM por USD 4,69 M (`02`), artículo NR-17 y guía de tono (`03`), base de 280 colaboradores y clima (`04`), P&L trimestral (`05`) y mapeo SIPOC (`06`).
- **Supervisión humana (HITL):** Toda aprobación de crédito, excepción de precio/descuento, publicación externa y decisión de personas requiere validación humana explícita.

**Los 3 Casos de Uso Seleccionados:**
1. **CU-1 · Copiloto Order-to-Cash (Finanzas/Ops):** Extracción OCR/IA de propuestas PDF + pre-análisis crediticio Serasa con matriz de alzada. Ataca **USD 2,60 M/año** en cancelaciones por crédito lento, fletes duplicados y errores de NF-e.
2. **CU-2 · Asistente Consultivo de Objeciones B2B (Ventas):** Respuestas basadas en TCO, NR-17, ABERGO, 30/60/90 y piloto sin rebajar margen sobre **USD 4,69 M** de pipeline.
3. **CU-3 · Simulador de Feedback 1:1 (SBI) + People Analytics Agregado (RR. HH.):** Entrenamiento interactivo para líderes de Atención y Comercial (ataca el **40,6 %** de salidas por liderazgo/claridad y **31,2 %** por sobrecarga manual).

### 2.2 Etapa 2 — Prioridad y Cambio: Matriz Esfuerzo × Impacto y ROI
*(Insertar captura: `04_evidencias_hitl/capturas/ruta0_matriz_esfuerzo_impacto_roi.png`)*

- **Quick Wins (0–30 días):** CU-1 Objeciones (Impacto 4, Esfuerzo 1), Gem Marca (Impacto 3, Esfuerzo 1), Simulador Feedback 1:1 (Impacto 4, Esfuerzo 2).
- **Proyectos Estratégicos Prioridad 1 (30–90 días):** Extracción PDF→Orden y Pre-análisis de Crédito (Impacto 5, Esfuerzo 3).
- **Análisis de ROI Año 1 (sobre inversión estimada de USD 86.000):**
  - *Escenario Conservador:* Ahorro USD 1.095.000 → **ROI 1.173 %** · Payback 0,94 meses.
  - *Escenario Base (Plan):* Ahorro **USD 1.819.000** → **ROI 2.015 %** · Payback 0,57 meses (EBITDA proyectado sube de USD 5,77 M a ≈ USD 7,59 M).
  - *Escenario Optimista:* Ahorro USD 2.450.500 → **ROI 2.749 %** · Payback 0,42 meses.
- **Gestión del cambio:** Patrocinio directivo (*"la IA elimina digitación; la persona decide"*), red de 1 campeón por área, capacitación práctica de 90 min y regla de pivote a los 60 días.

### 2.3 Etapa 3 — IA Responsable: Política, Riesgos y Gobernanza LGPD
*(Insertar captura: `04_evidencias_hitl/capturas/ruta0_gobernanza_lgpd.png`)*

- **Clasificación en 4 niveles:** Público (catálogo/NR-17), Interno (P&L/SIPOC solo en cuentas enterprise con retención cero), Personal Art. 5 (anonimizado previo) y Sensible/Alto Riesgo (certificados médicos/entrevistas prohibidos en IA pública; solo agregados).
- **LGPD Art. 20:** Prohibido que la IA tome decisiones automatizadas de crédito, contratación o desvinculación.
- **Roles:** Comité de IA, DPO (ROPA y derechos de titulares), Dueño de Proceso (firma HITL) y TI/Seguridad (DLP y control de retención).

---

## 3. Especialización Declarada: Ruta 4 · Finanzas y Operaciones

### 3.1 Entregable Obligatorio: SIPOC + Ishikawa (6M) + Proceso To-Be
*(Insertar capturas: `04_evidencias_hitl/capturas/ruta4_finanzas_sipoc_ishikawa.png` y flujo n8n `04_evidencias_hitl/capturas/vista_n8n_workflow_order_to_cash.png`)*

- **Cuello de botella As-Is (SIPOC):** Cada uno de los 180–220 pedidos B2B/mes pasa por correo informal, consulta manual de 40 min a Serasa, espera de hasta 48 h por aprobación gerencial sin matriz de alzada, re-digitación en ERP legado para NF-e/boletos y envío manual al CD de Joinville (SC).
- **Causa raíz Ishikawa (6M):**
  - *Método:* Sin POP ni matriz de alzada ni verificación CIF/FOB.
  - *Máquina:* ERP sin API, cero OCR, 3 Excels desconectados.
  - *Mano de obra:* Burnout por digitación y centralización gerencial.
  - *Material:* Propuestas incompletas y SKUs/precios desactualizados.
  - *Medición:* Sin SLA en tiempo real; errores detectados al cierre de mes.
  - *Medio ambiente:* Fricción entre Comercial (São Paulo) y CD (Joinville).
- **Solución To-Be Lean + IA:** OCR/LLM extrae y valida datos del PDF contra catálogo → consulta automática a Serasa (< 5 min) → **Matriz de alzada** (bajo riesgo sigue flujo; alto monto/alerta pasa con ficha resumida al Gerente Financiero) → emisión sin re-digitación y orden automática al CD Joinville con chequeo CIF/FOB.

### 3.2 Entregable Opcional: Panel Financiero Presupuesto vs. Real
*(Insertar capturas: `04_evidencias_hitl/capturas/ruta4_finanzas_panel_ejecutivo.png` y tablero Magnus BI `04_evidencias_hitl/capturas/vista_magnus_tablero_ejecutivo.png`)*

- **EBITDA T1–T4:** T1 −15,7 % → T2 −18,4 % → T3 −55,6 % → **T4 −65,3 %**.
- **Sobrecostos críticos:** Fletes CD (+57,1 %), Reentregas y multas (+245,2 %), Cancelaciones (+120,5 %) y PDD Inadimplencia (+152,3 %).
- **Auditoría HITL de datos:** Se detectó diferencia entre Hoja 2 (*Ingresos por producto*: USD 47,40 M reales) y Hoja 1 (*P&L*: USD 48,50 M brutos / 39,02 M netos), documentada para conciliación contable.

---

## 4. Tabla de Evidencias, Validación HITL y Capturas (Obligatorio)
*(Insertar captura: `04_evidencias_hitl/capturas/evidencias_hitl_pruebas_prompts.png` y las capturas de las rutas incluidas)*

| Ruta | Prompt / Artefacto | Validación Humana (HITL) Aplicada | Archivo de Evidencia |
|---|---|---|---|
| Ruta 0 | AI Canvas, Matriz + ROI, LGPD | Supuestos de captura/inversión marcados para aprobación financiera; reglas Art. 20 | `ruta0_matriz_esfuerzo_impacto_roi.png`, `ruta0_gobernanza_lgpd.png` |
| Ruta 4 (Principal) | `prompt_finanzas_operaciones.md` | Detección de brecha 47,4 M vs 39,02 M; aprobación de crédito 100 % humana | `ruta4_finanzas_sipoc_ishikawa.png`, `ruta4_finanzas_panel_ejecutivo.png` |
| Anexo · Ruta 1 Ventas | `prompt_ventas_objeciones.md` | Precios contrastados vs catálogo en `#1045 Vanguarda` ($801.900 exacto) | `ruta1_ventas_pipeline_objeciones.png`, `vista_trello_kanban_comercial_ops.png` |
| Anexo · Ruta 2 Mkt | `prompt_marketing_voz_marca.md` | Citas exactas (23m 15s, 32 dB); cero promesas médicas | `ruta2_marketing_gem_campana.png` |
| Anexo · Ruta 3 RRHH | `prompt_rrhh_simulador_feedback.md` | Simulador ficticio sin PII; corrección de cálculo real 64/280 = 22,86 % | `ruta3_rrhh_simulador_people_analytics.png` |

---

## 5. Conclusiones y Próximos Pasos
1. **Desbloquear el núcleo Order-to-Cash en 90 días** permite atacar USD 2,60 M de pérdidas inmediatas sin esperar el reemplazo completo del ERP legado.
2. **Desplegar los Quick Wins en 30 días** (Manual de Objeciones, Gem de Marca y Simulador de Feedback 1:1) alivia el *burnout* de Atención y Comercial y protege el pipeline de USD 4,69 M.
3. **Repositorio completo y trazable en GitHub:** `[Insertar URL de tu repo]` · **Enlace de evidencias:** `04_evidencias_hitl/`.
