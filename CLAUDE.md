# 🤖 Claude Context — TTN Company / Biowel & Netcare

Carga este archivo al inicio de cada conversación para que Claude tenga todo el contexto necesario sin necesidad de repetirlo.

---

## 👤 Identidad

- **Usuario:** Luis Steffens
- **Empresa:** TTN Company
- **Account ID Jira:** `712020:9ee1cabd-b560-41a0-a386-2d052b36aff7`
- **Idioma de respuesta:** Español siempre

---

## 🗂️ Jira

| Campo       | Valor                                        |
|-------------|----------------------------------------------|
| URL         | https://ttncompany.atlassian.net             |
| Cloud ID    | `42430057-8c3c-4ab5-ab8e-dda7830841fe`       |
| Proyecto    | `PROYECTOS` (Tablero Proyectos & Diseño 2026)|
| Sprint activo | Sprint Mayo 2026 — ID: `5271`              |

### Estados disponibles
- POR HACER _(estado inicial por defecto)_
- EN CURSO
- EN REVISIÓN
- FINALIZADA

### Reglas de creación de tareas
- Asignar a **Luis Steffens** por defecto salvo indicación contraria.
- Sprint: usar siempre el **ID numérico** en `customfield_10020`.
- Labels: pasarlos en `additional_fields` como `{"labels": ["Label1", "Label2"]}`.
- Confirmar con Luis antes de crear o modificar si hay dudas.

---

## 👥 Equipo

| Nombre              | Account ID                                        |
|---------------------|---------------------------------------------------|
| Luis Steffens       | `712020:9ee1cabd-b560-41a0-a386-2d052b36aff7`    |
| Emerson Turizo      | `712020:2d5032df-3f53-40dd-bb42-6564663c984a`    |
| Deiner Acosta       | `712020:913339c3-9cbe-4115-8ccf-4ff767a097c2`    |
| Maria Alejandra     | `62e446eda855c695587acb4e`                        |
| Maremys Galindo S.  | `70121:96fc9f97-4509-4274-90b9-4b6614c48aec`     |
| Nelson Caraballo    | `620fb1a507f51e00694504fa`                        |
| Yeison Corpas       | `712020:6dbd7aae-8c8e-4d28-be0e-07027ea852cb`    |
| disenouiux02        | `712020:13564995-e1fc-447d-8eb9-d267fed0da9a`    |

---

## 🎨 Figma

| Archivo              | File Key                        |
|----------------------|---------------------------------|
| Módulo de Nómina     | `65jP25pXHN6tU0yUOrD979`        |
| Activos Fijos 2.0    | `wo1yWzgzrLrQa4vy8hJeEu`        |
| Netcare – Afiliaciones | `YVsc4JqgUhhwjwFrmTLFCw`      |

- Node IDs en formato con guión: `6874-51272`
- Herramienta: `Figma:get_design_context` con `fileKey` + `nodeId`

---

## 🏷️ Labels frecuentes

`Diseño` · `RRHH` · `Activos_Fijos` · `Netcare` · `Nómina` · `Dotaciones`

---

## ⚡ Comando `/nueva-tarea`

### Formato
```
/nueva-tarea — [link de Figma] — [descripción breve del cambio] — tags: X, Y — vence: DD de mes — Sprint: nombre
```

### Flujo que debe seguir Claude
1. Leer el frame en Figma con `get_design_context` para entender el contexto visual.
2. Combinar lo visto en Figma con la descripción de Luis.
3. Generar descripción profesional con las secciones:
   - **Objetivo**
   - **Contexto**
   - **Referencia de diseño** _(link al frame de Figma)_
   - **Alcance del cambio**
   - **Criterios de aceptación** _(en formato checklist)_
4. Crear la tarea en Jira con: descripción, labels, fecha de vencimiento y sprint.
5. Asignar a Luis Steffens por defecto.
6. Estado inicial: **POR HACER**.
7. Confirmar la creación con un resumen en tabla.

---

## 🗃️ Contexto de proyectos

### Biowel — HR & Payroll
- **Cliente:** FOCA (Fundación Oftalmológica del Caribe)
- Módulos activos: Módulo de Nómina, Dotaciones, Activos Fijos 2.0
- Paleta corporativa: `#005DBF`, `#01A0F6`
- Tipografía: PT Sans Caption

### Netcare — Afiliaciones
- Paleta corporativa: `#750BBE` (morado), `#14B8B0` (turquesa), `#3B4043` (texto)
- Tipografía: Graphik, Gotham

---

## 📁 Archivos de referencia

| Archivo             | Descripción                                      |
|---------------------|--------------------------------------------------|
| `sprint-tracker.md` | Historial y datos del sprint activo              |
| `claude.md`         | Este archivo — contexto general para Claude      |
