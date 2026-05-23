# ClickUp DW MVP v24

Mini sistema interno para cargar Excel de ClickUp, registrar tarifas, calcular horas, costos, facturación y resultado operativo.

## Flujo lógico

1. Cargar Excel ClickUp.
2. El sistema detecta país, cliente, proyecto, hito facturable, persona, rol estimado, rol asignado y horas.
3. Registrar tarifas:
   - Tarifa operaciones: por rol interno.
   - Tarifa comercial: por proyecto + rol asignado.
4. Gerencia General muestra resumen de horas, cumplimiento en horas, resumen de costos, tablas y gráficos.
5. Gerencia de Servicios muestra enfoque operativo sin tarifa comercial/hora.

## Cambios v24

- El gráfico de hitos facturables ahora se agrupa por proyecto.
- Se agregó selector de proyecto para ver todos los proyectos o uno específico.
- El gráfico usa barras horizontales para que los nombres de hitos se lean mejor.
- Si se muestran varios proyectos, cada proyecto aparece como un panel separado.
- Las barras mantienen etiquetas numéricas y tooltip con proyecto, hito, tipo de horas y valor.

## Ejecutar

```powershell
python -m venv .venv
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
streamlit run app.py
```


## v28
- Resumen de horas presentado solo con cards y título de sección.
- Se retiraron subtítulos internos de las cards de horas.
