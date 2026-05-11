# 🤖 Claude Context — TTN Company / Proyectos & Diseño 2026

Carga este archivo al inicio de cada conversación para que Claude tenga todo el contexto necesario sin necesidad de repetirlo.

---

## ⚙️ Mi configuración — edita esto antes de usar

- **Mi nombre:** TU NOMBRE AQUÍ ← reemplaza con tu nombre
- **Mi Account ID Jira:** TU ACCOUNT ID AQUÍ ← reemplaza con el tuyo (ver tabla de equipo abajo)

---

## 👤 Identidad de empresa

- **Empresa:** TTN Company
- **Idioma de respuesta:** Español siempre

---

## 🗂️ Jira

| Campo         | Valor                                         |
|---------------|-----------------------------------------------|
| URL           | https://ttncompany.atlassian.net              |
| Cloud ID      | `42430057-8c3c-4ab5-ab8e-dda7830841fe`        |
| Proyecto      | `PROYECTOS` (Tablero Proyectos & Diseño 2026) |
| Sprint activo | Sprint Mayo 2026 — ID: `5271`                 |

### Estados disponibles
- POR HACER _(estado inicial por defecto)_
- EN CURSO
- EN REVISIÓN
- FINALIZADA

### Reglas generales de creación de tareas
- Asignar al **usuario configurado arriba** por defecto, salvo indicación contraria.
- Sprint: usar siempre el **ID numérico** en `customfield_10020`.
- Labels: pasarlos en `additional_fields` como `{"labels": ["Label1", "Label2"]}`.
- Confirmar antes de crear o modificar si hay dudas.

### 🏷️ Labels por defecto según assignee

Las labels por defecto se determinan por el **assignee de la tarea** (identificado por su Account ID de Jira), **no por quien escribe el mensaje**. Si la tarea se asigna a Luis Steffens, siempre llevará `Diseño` — sin importar quién la haya solicitado.

Las tags adicionales que se pasen en el comando **se suman** a las labels por defecto. Nunca se reemplazan.

| Rol | Miembros | Labels por defecto |
|---|---|---|
| Diseñadores | Luis Steffens, Maria Alejandra, disenouiux02 | `Diseño` |
| Desarrollo | Deiner Acosta | `Desarrollo`, `Proyectos` |
| Proyectos | Emerson, Maremys, Nelson, Yeison, Yhan | `Proyectos` |

> **Ejemplo:** Si Luis crea una tarea con `tags: RRHH`, las labels finales serán `Diseño` + `RRHH`.  
> **Ejemplo:** Si alguien asigna una tarea a Deiner con `tags: Compras`, las labels finales serán `Desarrollo` + `Proyectos` + `Compras`.

### ⚠️ Regla de borrador — aplica a TODOS los comandos sin excepción
Antes de ejecutar cualquier acción en Jira, Google Drive o cualquier otra plataforma, Claude **siempre** debe:
1. Generar un borrador completo con todo lo que va a crear: título, descripción, campos, tablero destino, asignado, sprint y labels.
2. Mostrar el borrador al usuario y **esperar confirmación explícita** ("ok", "confirmar", "sí" o similar).
3. Solo después de recibir la confirmación, ejecutar las acciones.

Esto aplica a: `/nueva-tarea`, `/nuevo-wireframe`, `/nuevo-proyecto-drive`, `/nuevo-proyecto-wireframe`, `/tarea-dev`, `/tarea-netcare`, `/historia-usuario` y `/backlog`.

---

## 👥 Equipo

| Nombre              | Rol                  | Account ID                                      |
|---------------------|----------------------|-------------------------------------------------|
| Luis Steffens       | Diseño               | `712020:9ee1cabd-b560-41a0-a386-2d052b36aff7`  |
| Maria Alejandra     | Diseño               | `62e446eda855c695587acb4e`                      |
| disenouiux02        | Diseño               | `712020:13564995-e1fc-447d-8eb9-d267fed0da9a`  |
| Deiner Acosta       | Desarrollo           | `712020:913339c3-9cbe-4115-8ccf-4ff767a097c2`  |
| Emerson Turizo      | Proyectos            | `712020:2d5032df-3f53-40dd-bb42-6564663c984a`  |
| Maremys Galindo S.  | Proyectos            | `70121:96fc9f97-4509-4274-90b9-4b6614c48aec`   |
| Nelson Caraballo    | Proyectos            | `620fb1a507f51e00694504fa`                      |
| Yeison Corpas       | Proyectos            | `712020:6dbd7aae-8c8e-4d28-be0e-07027ea852cb`  |
| Yhan Arrieta        | Proyectos            | `712020:04de5f52-2c05-4457-b4b8-950ae69259d0`  |

---

## 🏷️ Labels del tablero (por frecuencia de uso)

| Label                    | Tareas | Uso                              |
|--------------------------|--------|----------------------------------|
| `Diseño`                 | 58     | Tareas de UI/UX y diseño visual  |
| `Proyectos`              | 41     | Gestión general de proyectos     |
| `Central_Esterilización` | 29     | Módulo central de esterilización |
| `Desarrollo`             | 24     | Tareas de desarrollo             |
| `Compras`                | 23     | Módulo de compras                |
| `RRHH`                   | 12     | Recursos humanos y nómina        |
| `Nomina`                 | 9      | Módulo de nómina en Biowel       |
| `Óptica`                 | 9      | Módulo de óptica                 |
| `Netcare`                | 7      | Proyecto Netcare — Afiliaciones  |
| `Contabilidad`           | 3      | Módulo de contabilidad           |
| `Historia_Clinica`       | 3      | Módulo de historia clínica       |
| `Convocatorias`          | 2      | Tareas de convocatorias          |
| `Activos_Fijos`          | 1      | Módulo Activos Fijos 2.0         |

---

## 🗃️ Contexto de proyectos

### Biowel — HR & Payroll
- **Cliente:** FOCA (Fundación Oftalmológica del Caribe)
- Módulos activos: Módulo de Nómina, Dotaciones, Activos Fijos 2.0, Central de Esterilización, Compras, Óptica, Contabilidad, Historia Clínica
- Paleta corporativa: `#005DBF`, `#01A0F6`
- Tipografía: PT Sans Caption

### Netcare — Afiliaciones
- Paleta corporativa: `#750BBE` (morado), `#14B8B0` (turquesa), `#3B4043` (texto)
- Tipografía: Graphik, Gotham

---

## 🎨 ROL: Diseñador

### Archivos de Figma
| Archivo                | File Key                   |
|------------------------|----------------------------|
| Módulo de Nómina       | `65jP25pXHN6tU0yUOrD979`   |
| Activos Fijos 2.0      | `wo1yWzgzrLrQa4vy8hJeEu`   |
| Netcare – Afiliaciones | `YVsc4JqgUhhwjwFrmTLFCw`   |

- Node IDs en formato con guión: `6874-51272`
- Herramienta: `Figma:get_design_context` con `fileKey` + `nodeId`

### Comando `/nueva-tarea`

**Formato:**
```
/nueva-tarea — [link de Figma] — [descripción breve del cambio] — tags: X, Y — vence: DD de mes — Sprint: nombre
```

**Flujo que debe seguir Claude:**
1. Leer el frame en Figma con `get_design_context` para entender el contexto visual.
2. Combinar lo visto en Figma con la descripción proporcionada.
3. Generar descripción profesional con las secciones:
   - **Objetivo**
   - **Contexto**
   - **Referencia de diseño** _(link al frame de Figma)_
   - **Alcance del cambio**
   - **Criterios de aceptación** _(en formato checklist)_
4. Crear la tarea en Jira con: descripción, labels, fecha de vencimiento y sprint.
5. Asignar al usuario configurado arriba por defecto.
6. Estado inicial: **POR HACER**.
7. Confirmar la creación con un resumen en tabla.

---

## 📐 ROL: Wireframer

### Contexto
Los wireframes se crean como hojas de cálculo en Google Drive, organizados en carpetas por proyecto y subcarpetas por tipo de contenido (Wireframes, Documentación, Grabaciones, Demos, etc.). Una vez listos, se crea una tarea en Jira para notificar al equipo de diseño con el link correspondiente.

---

### Comando `/crear-wireframe`
Crea la estructura de carpetas en Google Drive y una Google Sheet en blanco dentro de la subcarpeta indicada.

**Formato:**
```
/crear-wireframe — [nombre del proyecto] — subcarpetas: X, Y, Z — sheet en: [nombre de subcarpeta] — [nombre de la Sheet]
```

**Ejemplo:**
```
/crear-wireframe — Módulo de Compras FOCA — subcarpetas: Wireframes, Documentación, Grabaciones, Demos — sheet en: Wireframes — Flujo de aprobación de órdenes
```

**Flujo que debe seguir Claude:**
1. Crear la carpeta raíz en Google Drive con el nombre indicado.
2. Crear cada subcarpeta dentro de la carpeta raíz.
3. Crear una Google Sheet en blanco dentro de la subcarpeta especificada en `sheet en:`, con el nombre indicado.
4. Devolver un resumen con los links de cada carpeta creada y el link directo a la Sheet.

---

### Comando `/nuevo-wireframe`
Documenta un wireframe ya existente en Google Drive creando la tarea correspondiente en Jira.

**Formato:**
```
/nuevo-wireframe — [link del Google Sheets] — [módulo o funcionalidad] — [descripción breve] — etiquetar: [nombre] — tags: X, Y — vence: DD de mes — Sprint: nombre
```

**Ejemplo:**
```
/nuevo-wireframe — https://docs.google.com/spreadsheets/d/1A2B3C4D5E — Módulo de Compras: flujo de aprobación de órdenes — Wireframe de 3 pantallas: listado de órdenes, detalle de orden y modal de aprobación — etiquetar: Luis Steffens — tags: Compras — vence: 20 de mayo — Sprint: Mayo 2026
```

**Flujo que debe seguir Claude:**
1. Leer el contenido de la hoja de cálculo desde el link de Google Drive.
2. Entender qué pantallas o flujos cubre el wireframe.
3. Generar descripción profesional con las secciones:
   - **Objetivo** _(qué funcionalidad cubre el wireframe)_
   - **Contexto** _(por qué se necesita)_
   - **Referencia** _(link al Google Sheets)_
   - **Alcance** _(qué pantallas o flujos incluye)_
   - **Notas para el diseñador** _(indicaciones o restricciones relevantes)_
4. Crear la tarea en Jira con: descripción, labels, fecha de vencimiento y sprint.
5. Asignar al usuario configurado por defecto.
6. Estado inicial: **POR HACER**.
7. Dejar un comentario en la tarea recién creada etiquetando a la persona indicada en `etiquetar:`, usando su Account ID de la tabla del equipo. Mensaje: _"@[nombre] el wireframe de [módulo] está listo para revisar: [link al Sheet]"_
8. Confirmar la creación con un resumen en tabla que incluya el link a la tarea y la persona etiquetada.

---

## 🛠️ ROL: Analista Técnico

### Contexto
Los analistas técnicos formulan tareas para el equipo de desarrollo. Hay dos flujos según el proyecto:
- **Netcare** → las tareas van al tablero `NET` con Historia principal + Dev-Tasks de frontend y backend, y una tarea espejo en `PROYECTOS`.
- **Otros proyectos** → las tareas se añaden al backlog en Google Sheets que maneja el Product Owner.

### Datos de Netcare
| Campo | Valor |
|---|---|
| Project key | `NET` |
| Sprint activo | Consultar sprint activo del tablero NET antes de crear |
| Tipo de issue principal | `Historia` |
| Tipo de subtarea | `Dev-Task` |
| Sin labels | No se usan labels en el tablero NET |

### Épicas disponibles en Netcare
El usuario no necesita saber el key — solo menciona el área. Claude mapea automáticamente:

| Área | Épica | Key |
|---|---|---|
| Mejoras generales | Mejoras | `NET-49` |
| Módulo administración | Administración | `NET-103` |
| Módulo aliados | Aliados | `NET-105` |
| Landing page | LANDING | `NET-217` |

> Si no queda claro a qué épica pertenece la tarea, Claude pregunta antes de generar el borrador.

---

### Comando `/tarea-netcare`
Crea la Historia principal con sus Dev-Tasks en el tablero NET y una tarea de seguimiento automática en PROYECTOS.

**Formato:**
```
/tarea-netcare — [área: Administración / Aliados / Landing / Mejoras] — [título de la historia] — [descripción detallada pantalla por pantalla] — [link de Figma] — vence: DD de mes
```

**Flujo que debe seguir Claude:**
1. Leer el frame en Figma con `get_design_context` para entender el contexto visual.
2. Consultar el sprint activo del tablero NET.
3. Generar borrador completo y esperar confirmación antes de crear nada.
4. Tras confirmación, crear en el tablero `NET`:
   - **Historia principal** bajo la épica indicada con descripción narrativa pantalla por pantalla e imágenes de referencia de Figma
   - **Dev-Task frontend** como subtarea: maquetado visual según Figma con checklist de cambios
   - **Dev-Task backend** como subtarea: endpoints necesarios con checklist técnico
5. Crear en el tablero `PROYECTOS` una tarea de seguimiento con:
   - **Título:** `[Netcare] [título de la historia]`
   - **Descripción:** link a la Historia NET creada, épica padre, sprint de Netcare, resumen del cambio, checklist de seguimiento (Historia completada, Dev-Tasks finalizadas)
   - **Labels:** `Netcare`
   - **Asignado:** usuario configurado (Emerson Turizo por defecto en este caso)
   - **Sprint:** sprint activo de PROYECTOS
   - **Estado inicial:** POR HACER
6. Devolver resumen con tabla de todo lo creado: Historia, Dev-Tasks y tarea espejo.

---

### Comando `/tarea-dev`
Para convertir el backlog de una épica en Google Sheets a una tarea base con subtareas en Jira. El parámetro `tarea:` es opcional — si se omite, Claude procesa todas las filas de la épica; si se indica, Claude toca únicamente esa fila.

**Formato:**
```
/tarea-dev — [link del Google Sheets] — épica: [nombre de la épica]
/tarea-dev — [link del Google Sheets] — épica: [nombre de la épica] — tarea: [nombre de la tarea]
```

**Flujo sin `tarea:` (épica completa):**
1. Leer el Google Sheets y filtrar todas las filas de la épica indicada.
2. Identificar cada fila como una subtarea distinta.
3. Generar borrador completo con tarea base + todas las subtareas y esperar confirmación.
4. Tras confirmación:
   - **Si la tarea base no existe** → crearla con todas sus subtareas.
   - **Si existe y NO está `FINALIZADA`** → actualizarla y crear/actualizar sus subtareas.
   - **Si existe y está `FINALIZADA`** → crear nueva tarea base con todas las subtareas (nueva iteración).

**Flujo con `tarea:` (fila específica):**
1. Leer el Google Sheets y localizar únicamente la fila indicada dentro de la épica.
2. Generar borrador solo de esa subtarea y esperar confirmación.
3. Tras confirmación:
   - **Si la subtarea no existe** → crearla dentro de la tarea base existente.
   - **Si la subtarea existe y NO está `FINALIZADA`** → actualizarla sin tocar las demás subtareas.
   - **Si la subtarea existe y está `FINALIZADA`** → crear una subtarea nueva (iteración) dentro de la misma tarea base.
   - **Si la tarea base también está `FINALIZADA`** → crear una tarea base nueva con solo esa subtarea como iteración.

**Aplica a ambos flujos:**
- Asignar al **usuario configurado en `Mi configuración`** — sin etiquetar en comentarios, salvo que se incluya `asignar: [nombre]`.
- Labels por defecto según assignee + las que apliquen al módulo.
- Sprint activo de PROYECTOS.
- Estado inicial: **POR HACER**.
- Confirmar con resumen en tabla indicando qué se creó o actualizó.

---

## 📁 Archivos de referencia

| Archivo             | Descripción                                 |
|---------------------|---------------------------------------------|
| `sprint-tracker.md` | Historial y datos del sprint activo         |
| `CLAUDE.md`         | Este archivo — contexto general para Claude |
