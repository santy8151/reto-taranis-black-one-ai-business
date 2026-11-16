# Ruta 3 · RR. HH. y People Analytics — Etapa 1 (obligatoria)

**Insumo:** `04_Base_de_colaboradores_People_Analytics.xlsx` (280 colaboradores, encuesta de clima, indicadores de rotación).

## Hallazgos (calculados sobre la base)
| Área | Plantilla | Salidas | Rotación | eNPS |
|---|---|---|---|---|
| Atención al cliente | 65 | 25 | **38,5 %** | +8 |
| Comercial B2B | 55 | 17 | **30,9 %** | +18 |
| Operaciones y Logística | 60 | 9 | 15,0 % | +34 |
| Marketing | 25 | 4 | 16,0 % | +36 |
| Finanzas | 30 | 4 | 13,3 % | +32 |
| Gente y Cultura | 15 | 2 | 13,3 % | +40 |
| Ingeniería y P&D | 30 | 3 | 10,0 % | +58 |
| **Total** | **280** | **64** | **22,8 %** | **+28** |

- **Motivos de salida (64):** falta de claridad de objetivos y mal liderazgo directo **26 (41 %)**; sobrecarga por tareas manuales y sistemas lentos **20 (31 %)**; oferta salarial de la competencia **11 (17 %)**; otros 7.
- **Ausentismo medio** más alto en Atención (8,8 días) y Comercial (7,2); el más bajo en Ingeniería (5,1).
- La rotación se concentra en áreas con peores notas de liderazgo y herramientas en la encuesta: **la causa dominante es gestión y herramientas, no salario** (solo 17 % por competencia).
- *Nota de calidad de datos:* el kit indica 22,5 % general; el recuento sobre la base da 22,8 % (64/280). Verificar el criterio de cálculo antes de presentar.

## Solución con IA
1. **Análisis de sentimiento** de comentarios abiertos → temas (liderazgo, herramientas, carga, onboarding) por área.
2. **Cruce cuantitativo:** rotación y ausentismo vs eNPS, antigüedad, modelo de trabajo.
3. **Alertas tempranas** agregadas (no individuales) para nuevos ingresos en riesgo en los primeros 90 días.
4. **Plan de acción:** onboarding con playbook, formación de líderes en feedback y objetivos claros, automatizar tareas manuales (vincula con Ruta 4).

## Salvaguardas éticas
- Solo datos **agregados/anonimizados**; salarios y entrevistas de salida no se suben a IA pública.
- La IA no predice ni puntúa a personas individuales ni decide desvinculaciones (LGPD art. 20).
- Revisión de sesgos por género y modelo de trabajo antes de actuar.

## KPIs
Rotación en Atención/Comercial −30 % · eNPS +10 puntos · rotación a 90 días < 15 % · ausentismo −15 %.

**Prompt:** [prompt_rrhh_people_analytics.md](../../03_prompts_y_skills/prompt_rrhh_people_analytics.md)
