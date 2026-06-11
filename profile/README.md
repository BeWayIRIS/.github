<div align="center">

<img src="assets/omnissiah_phi.svg" alt="BeWay · Cogitator Phi" width="180"/>

# IRIS

**Integración de Riesgos, IA y Sistemas**

*Ex datis, scientia · Ex scientia, dominium*

</div>

<div align="center">

![Estructura](https://img.shields.io/badge/estructura-v3.3-1f6feb?style=flat-square)
![Marco](https://img.shields.io/badge/marco-DAMA--DMBOK2-0a7d3f?style=flat-square)
![Norma](https://img.shields.io/badge/norma-ISO%2027001-555?style=flat-square)
![Estado](https://img.shields.io/badge/estado-vivo-success?style=flat-square)

</div>

---

> IRIS dirige la adopción de IA en BeWay bajo responsabilidad humana, alineada con los estándares de seguridad y de gestión de IA y con los principios y objetivos de negocio de BeWay. Su principio operativo se podría definir como Hypothesis-driven AI research. Las ideas, los conceptos, parten de un humano; la actividad de la IA se revisa por un humano; la firma y la responsabilidad final son humanas.

| | |
|---|---|
| **Workspace** | `SCRIPT-IRIS` — repositorio maestro del programa IRIS |
| **Propietario** | Francisco C. Ceballos |
| **Contacto** | <franciscoceballos@beway.com> |
| **Última actualización** | 2026‑06‑11 |
| **Versión de estructura** | v3.3 |
| **GitHub** | [github.com/BeWayIRIS](https://github.com/BeWayIRIS) |

---

## Índice

1. [Modelo](#modelo)
2. [Mapa de carpetas](#mapa-de-carpetas)
3. [Áreas del programa](#áreas-del-programa-iris)
4. [Convenciones](#convenciones)
5. [Cómo navegar](#cómo-navegar-guía-rápida)
6. [Skill `/dama` — el marco DAMA consultable](#skill-dama--el-marco-dama-consultable)
7. [Hoja de ruta Data Management](#hoja-de-ruta-data-management-revisión-dama-2026-06-06)
8. [Para futuras sesiones de Claude](#para-futuras-sesiones-de-claude)
9. [Estado del programa](#estado-del-programa-junio-2026)
10. [Historial de cambios](#historial-de-cambios)

---

## Modelo

El programa IRIS se estructura en cuatro capas:

1. **Gobierno (`00_governance`)** — marco normativo y de referencia: DAMA, ISO 27001, glosario corporativo, bibliografía. Es el cuerpo doctrinal que aplica a toda la org.
2. **Programa (`01_iris`)** — el propio programa IRIS: documento fundacional, velocidades de despliegue, embajadores. Cómo se opera el gobierno del dato dentro de BeWay.
3. **Áreas (`02_…` → `10_…`)** — las 9 áreas a las que IRIS presta servicio, clasificadas en tres grupos: **áreas internas** (Ops, DN — Desarrollo de Negocio, Formación, Diseño/IT, Legal, Administración, P&G), **Centros de Excelencia** (CE_Data) y **área de cliente** (BAIT). Cada una tiene su propio espacio + repo en GitHub.
4. **Metodologías, proyectos y utilidades transversales (`11_…` → `15_…`, `assets`, `_archivo`)** — herramientas, entregables publicables, la metodología **BEMATE** de diseño conductual, la **auditoría de seguridad ISO 27001** (PRO26‑023) y el proyecto **IAMA** (IA Maturity Assessment).

---

## Mapa de carpetas

```text
SCRIPT-IRIS/
│
├── 00_governance/          Marco normativo y de gobierno (DAMA, ISO, glosario, bibliografía)
│   ├── dama-dmbok/         Knowledge areas DAMA (EN/ES) + roles de gobierno del dato
│   ├── iso-27001/          Normativa ISO 27001 y ofertas de securización
│   ├── glosario/           Glosario corporativo único (fuente de verdad)
│   ├── bibliografia/       Libros y manuales de referencia
│   └── CDMP/               Preparación del examen CDMP (banco de preguntas, skill /cdmp)
│
├── 01_iris/                Programa IRIS — fundacional, velocidades y embajadores
│   ├── fundacional/        Documento fundacional, documento maestro, bases v1/v3/v4, EDA licencias
│   ├── Velocidad_1/        Presentación Fase 0, doc Velocidad 1, embajadores
│   ├── Velocidad_2/        Segunda velocidad de despliegue (en preparación)
│   └── fuentes/            Insumos: política IA, IRIS_v2, plan general, transcritos de reuniones
│
├── 02_Ops/                 Área interna · Operaciones
├── 03_DN/                  Área interna · Desarrollo de Negocio
├── 04_CE_Data/             Centro de Excelencia · Datos           [pendiente de poblar]
├── 05_BAIT/                Área de cliente · IA para cliente (Be-Truth) + clon de trabajo de trama
├── 06_Formacion/           Área interna · Formación (mcp-base, bemate-kb)
├── 07_Diseno/              Área interna · Diseño/IT               [pendiente de poblar]
├── 08_Legal/               Área interna · Legal — fuentes iniciales (política de uso de IA)
├── 09_Administracion/      Área interna · Administración          [pendiente de poblar]
├── 10_PyG/                 Área interna · P&G (People & Growth)   [pendiente de poblar]
│
├── 11_herramientas/        Código, automatizaciones y skills
├── 12_entregables/         Salidas finales publicables
├── 13_BEMATE/              Repo oficial de la metodología BeMate (BAIT) — corpus markdown + pilotos
│   ├── INDEX.md            Punto de entrada: rutas por perfil, por CE, por capa y por estado
│   ├── Marco/              Doctrina: qué es BeMate, 6 Centros de Excelencia, glosario, roadmap
│   ├── Manuales/           11 manuales rectores (Paso 0 PreWork → Paso 10), uno por paso
│   ├── Artefactos/         ~74 artefactos operativos por paso (plantillas, instructivos, runbooks)
│   ├── Casos/              Best practices de proyectos cerrados (B100-Abanca)
│   ├── Operacion/          Modelo operador IA: manual, escalado, umbrales, decision log, auditoría
│   └── pilotos/            Pilotos del modelo operador IA (e2e-01 preparado, pendiente de cliente)
│
├── 14_ISO-27001/           Auditoría de Seguridad de la Información PRO26-023 (CyS Management)
│   │                       ⚠️ CONFIDENCIAL — NDA · solo local, sin repo en GitHub
│   ├── AUD1.01 .../        Arquitectura Empresarial — buzones de entrega I01–I14
│   ├── AUD1.02 .../        Arquitectura TIC — buzones de entrega I01–I21
│   └── 02 Meeting Records/ Kick-off (2026-05-21) y reuniones de control
│
├── 15_IAMA/                Proyecto IAMA — IA Maturity Assessment de departamentos internos
│                           (reutiliza el motor Patrón de trama; en diseño, sin repo aún)
│
├── assets/                 Activos visuales del repositorio
├── _archivo/               Material deprecated / histórico (no se sube a GitHub)
└── .claude/skills/         Skills de Claude Code del workspace: dama (conocimiento DAMA)
                            y sipoc (context diagrams de procesos con detección de gaps)
                            (copias compartidas del equipo en 00_governance/.claude/skills/)
```

---

## Áreas del programa IRIS

Cada área tiene carpeta local **y** repo privado en GitHub. La estructura interna se está homogeneizando — por defecto se propone `fuentes/`, `procesos/`, `entregables/`. Las áreas se clasifican en **tres grupos** según a quién sirven:

### Áreas internas

Las áreas funcionales de BeWay a las que IRIS presta servicio dentro de la organización.

| # | Área | Carpeta local | Repo GitHub | Estado |
|---|---|---|---|---|
| 02 | **Ops** — Operaciones | `02_Ops/` | [BeWayIRIS/02_Ops](https://github.com/BeWayIRIS/02_Ops) | Activo |
| 03 | **DN** — Desarrollo de Negocio | `03_DN/` | [BeWayIRIS/03_DN](https://github.com/BeWayIRIS/03_DN) | Activo |
| 06 | **Formación** | `06_Formacion/` | [BeWayIRIS/06_Formacion](https://github.com/BeWayIRIS/06_Formacion) | En construcción |
| 07 | **Diseño/IT** | `07_Diseno/` | [BeWayIRIS/07_Diseno](https://github.com/BeWayIRIS/07_Diseno) | Pendiente de poblar |
| 08 | **Legal** | `08_Legal/` | [BeWayIRIS/08_Legal](https://github.com/BeWayIRIS/08_Legal) | Inicializada — primeras fuentes |
| 09 | **Administración** | `09_Administracion/` | [BeWayIRIS/09_Administracion](https://github.com/BeWayIRIS/09_Administracion) | Pendiente de poblar |
| 10 | **P&G** — People & Growth | `10_PyG/` | [BeWayIRIS/10_PyG](https://github.com/BeWayIRIS/10_PyG) | Pendiente de poblar |

> El antiguo nombre de P&G era *Talento y Cultura*. El área Diseño pasa a denominarse **Diseño/IT** (la carpeta y el repo conservan el nombre `07_Diseno`).

### Centros de Excelencia

Capacidades especializadas transversales: ejecutan para todas las áreas (la gobernanza queda en `00`/`01`).

| # | Área | Carpeta local | Repo GitHub | Estado |
|---|---|---|---|---|
| 04 | **CE_Data** — Centro de Excelencia de Datos | `04_CE_Data/` | [BeWayIRIS/04_CE_Data](https://github.com/BeWayIRIS/04_CE_Data) | Pendiente de poblar |

### Área de cliente

IA aplicada a producto/servicio para el cliente final de BeWay.

| # | Área | Carpeta local | Repo GitHub | Estado |
|---|---|---|---|---|
| 05 | **BAIT** — IA para cliente (Be‑Truth) | `05_BAIT/` | [BeWayIRIS/05_BAIT](https://github.com/BeWayIRIS/05_BAIT) | Activo |

---

## Convenciones

### Nomenclatura de archivos

- Minúsculas con guion bajo: `dama_arquitectura_v2.qmd`
- Prefijos numéricos para orden: `00_`, `01_`, `02_`…
- Idioma como sufijo: `_es`, `_en` (no `_SP`, `_EN`)
- Versión al final: `_v1`, `_v2`, `_v1.3`

### Tipos de subcarpetas estándar

| Carpeta | Contiene |
|---|---|
| `fuentes/` | Documentos originales que dieron lugar al entregable (insumos). |
| `transcripciones/` | Texto extraído de audio, vídeo o documentos no editables. |
| `procesos/` | Procesos y procedimientos del área. |
| `entregables/` | Salidas finales versionadas del área. |
| `_drafts/` | Borradores y versiones de trabajo. |
| `_archivo/` | Material deprecated dentro de un proyecto. |
| `metadata/` | **DEPRECATED** — la metadata real vive embebida en los archivos, en `00_governance/glosario/` y en los inventarios. Ver discusión en el README de gobernanza. |

### Versionado

- Cambios menores: editar en sitio.
- Cambios mayores: nuevo archivo con sufijo `_vN`.
- Archivos abandonados: mover a `_archivo/` del proyecto, no borrar.

### GitHub — nomenclatura de repos

- Todos los repos viven en [**BeWayIRIS**](https://github.com/BeWayIRIS) y son **privados**.
- **Un repo por carpeta raíz numerada** (`00_governance` → `12_entregables`). El nombre del repo es **idéntico al de la carpeta local**, prefijo numérico incluido, para preservar el orden visual y el mapeo 1:1 carpeta ↔ repo.
- **Excepciones al mapeo:** `13_BEMATE` es clon del repo oficial [`BeWayBAIT/BeMate`](https://github.com/BeWayBAIT/BeMate) (el `BeWayIRIS/13_BEMATE` original queda obsoleto); `14_ISO-27001` **no tiene repo** (material NDA, solo local); `15_IAMA` aún no tiene repo (en diseño); `05_BAIT/trama/` es un clon de trabajo de [`BeWayBAIT/trama`](https://github.com/BeWayBAIT/trama) y no se versiona dentro de `05_BAIT`.
- `assets/` y `_archivo/` **no** se suben a GitHub (activos del repo maestro y material deprecated, respectivamente).

---

## Cómo navegar (guía rápida)

| Si buscas… | Ve a |
|---|---|
| Definir un término del negocio | `00_governance/glosario/` |
| Consultar un knowledge area DAMA | `00_governance/dama-dmbok/` o skill `/dama` en Claude Code |
| Definición canónica DAMA de un término | `/dama define <término>` (Diccionario DAMA, ~2.000 términos) |
| Saber qué pide ISO 27001 | `00_governance/iso-27001/` |
| El documento fundacional de IRIS | `01_iris/fundacional/` |
| Material para embajadores IRIS | `01_iris/Velocidad_1/embajadores/` |
| Diagrama SIPOC de un proceso | `02_Ops/context-diagrams/` |
| Inventario documental | `02_Ops/inventarios/` |
| Blueprint Data Native | `03_DN/blueprint/` |
| Material Be-Truth | `05_BAIT/Be-Truth/` |
| Material de formación | `06_Formacion/` |
| Metodología BeMate (11 pasos, 6 CE, operador IA) | `13_BEMATE/INDEX.md` ([BeWayBAIT/BeMate](https://github.com/BeWayBAIT/BeMate)) |
| Auditoría de seguridad ISO 27001 (PRO26‑023) | `14_ISO-27001/` (⚠️ NDA, solo local) |
| Madurez IA de un departamento interno (IAMA) | `15_IAMA/iama_base.md` |
| Preparar el examen CDMP | `00_governance/CDMP/` + skill `/cdmp` |
| Script o automatización | `11_herramientas/` |
| Una versión publicada y estable | `12_entregables/` |
| Algo antiguo o deprecated | `_archivo/` |

---

## Skill `/dama` — el marco DAMA consultable

Desde 2026‑06‑06 el marco de referencia del programa es **consultable por IA** mediante la skill `/dama` de Claude Code, generada desde la bibliografía de `00_governance/bibliografia/`:

| Fuente | Contenido |
|---|---|
| **DAMA‑DMBOK2** (2nd Ed. Revised) | ch01–ch17: las 11 knowledge areas, frameworks, patrones, tablas |
| **DAMA Dictionary** (2nd Ed.) | ~2.000 definiciones canónicas A‑Z (`dictionary.md`) |
| **Navigating the Labyrinth** (Sebastian‑Coleman) | ch18–ch29: visión ejecutiva y business case |

**Uso:** `/dama <tema>` · `/dama define <término>` · `/dama ch03` · `/dama cómo vendo esto a dirección`

**Ubicaciones** (mantener sincronizadas):

- Activa en este workspace: `SCRIPT-IRIS/.claude/skills/dama/`
- Compartida con el equipo: `00_governance/.claude/skills/dama/` (instalador: `install_dama.ps1`)

> ⚠️ Contenido con copyright de DAMA International — uso interno, solo repos privados.

---

## Hoja de ruta Data Management (revisión DAMA 2026‑06‑06)

Revisión del workspace contra DAMA‑DMBOK2 (vía `/dama`). Madurez estimada: **programa → L3 (Defined); organización → L1–L2**.

**Fortalezas confirmadas:** separación gobierno/ejecución (ch03) · glosario único (ch12) · SIPOC en Ops (ch01) · despliegue incremental por velocidades y embajadores (ch16) · metadata como producto, no por sí misma (ch12).

**Gaps priorizados:**

| # | Gap | Capítulo DAMA | Acción |
|---|---|---|---|
| 1 | `04_CE_Data` vacío mientras `01_iris` absorbe ejecución | ch16 (modelo Híbrido: CoE) | Charter de CE_Data como brazo *ejecutor* (inventarios, calidad, perfilado); gobernanza queda en 00/01 |
| 2 | Embajadores sin accountability formal | ch03/ch16 (stewardship, RACI) | Matriz RACI embajador ↔ área + ruta de escalado de issues (embajador → IRIS → dirección) |
| 3 | Versionado `_vN` duplica a git | ch09 (ANSI 859) | Dentro de repos versiona git; `_vN` solo para entregables publicados |
| 4 | `12_entregables` vacío — sin "copy of record" | ch09 (records) | Biblioteca de registro con control formal: qué se publicó, versión, fecha, aprobador. Lo publicado no se modifica |
| 5 | 4 áreas vacías sin priorizar | ch29 (evolution not revolution) | Siguiente ola: **08_Legal** (driver regulatorio, ch03). Resto: plantilla mínima hasta tener embajador |

**Plan (ch29):** 1) DMMA ligera por área (radar de dos anillos) → 2) roadmap por dependencias: glosario+inventarios → procesos → analítica (objetivo L2→L3 en 12‑18 meses) → 3) gestión del cambio: Steering Committee formalizado + los 10 factores de éxito (ch16).

---

## Para futuras sesiones de Claude

> Esta sección sirve como *system prompt* implícito del repositorio.
> Si una sesión de Claude entra aquí sin contexto previo, debe leer este README primero.

**Reglas operativas:**

1. **Antes de crear un archivo nuevo**, comprobar que no existe ya algo equivalente en su carpeta correspondiente.
2. **Nunca duplicar contenido entre carpetas raíz** — si un activo es transversal, vive en `00_governance/`.
3. **Las fuentes originales (insumos) van en `fuentes/`**, los entregables publicados en `entregables/` (del área correspondiente o en `12_entregables/` si es publicación final del programa).
4. **Cualquier archivo `.qmd` debe poder renderizar sin dependencias externas** (rutas relativas a su propia carpeta).
5. **No tocar `_archivo/`** salvo para añadir más material deprecated o recuperar algo concreto.
6. **Si reorganizas, actualiza este README** y el README del área afectada. Recuerda que cada carpeta numerada mapea 1:1 con un repo privado del mismo nombre en `BeWayIRIS`.
7. **Para cualquier duda sobre el marco DAMA, usa la skill `/dama`** (definiciones, frameworks, capítulos) en vez de responder de memoria. Si editas la skill, sincroniza las dos copias: `.claude/skills/dama/` (activa) y `00_governance/.claude/skills/dama/` (compartida, commit + push).

---

## Estado del programa (junio 2026)

| Capa | Estado | Notas |
|---|---|---|
| `00_governance` | Estable | En mantenimiento. |
| `01_iris` | Activo | Fundacional cerrado (documento maestro); Velocidad 1 en despliegue + selección de embajadores; Velocidad 2 en preparación. |
| `02_Ops` | Activo | Modelando procesos 2.0. |
| `03_DN` | Activo | Blueprint *Data Native* v1 entregado (proyecto del área). |
| `04_CE_Data` | Pendiente | Por arrancar. |
| `05_BAIT` | Activo | Marco conceptual v0; refinando M1‑M2. Clon de trabajo de `trama` (BeWayBAIT) como referencia. |
| `06_Formacion` | En construcción | MCP base operativo; BeMate KB en consolidación. |
| `07_Diseno` | Pendiente | Por arrancar. |
| `08_Legal` | Inicializada | Primeras fuentes (Política de Uso de IA). |
| `09_Administracion` | Pendiente | Por arrancar. |
| `10_PyG` | Pendiente | Por arrancar. |
| `11_herramientas` | Mixto | `slack-downloader` operativo; resto en evaluación. |
| `12_entregables` | Arrancado | Informe post‑migración + referencia rápida de skills de Claude Code (PDF). |
| `13_BEMATE` | Activo | Corpus v2 migrado (~124 docs md): 11 manuales + 74 artefactos + capa Operación (operador IA). `AGENTS.md` + skill `bemate-operador-ia`; piloto e2e‑01 preparado, pendiente de cliente. Repo oficial: `BeWayBAIT/BeMate`. |
| `14_ISO-27001` | Activo | Auditoría PRO26‑023 en curso (kick‑off 2026‑05‑21, ~9 semanas). 5/35 inputs con datos, 21 en plantilla, 10 vacíos. ⚠️ NDA — solo local. |
| `15_IAMA` | En diseño | Documento base de contexto creado; arquitectura heredada de trama (Patrón). Sin repo aún. |

---

## Historial de cambios

| Fecha | Cambio | Responsable |
|---|---|---|
| 2026‑06‑11 | **v3.3** — alta de `14_ISO-27001/` (auditoría de seguridad PRO26‑023 de CyS Management; ⚠️ NDA, solo local, sin repo) y de `15_IAMA/` (proyecto IA Maturity Assessment sobre el motor Patrón de trama). Alta del clon de trabajo `05_BAIT/trama/` (BeWayBAIT/trama) y de `00_governance/CDMP/` (preparación del examen CDMP). Primeras fuentes en `08_Legal/` (Política de Uso de IA). Limpieza de `01_iris/Velocidad_1` (renombrados Fase 0 / Velocidad 1) y alta de `Velocidad_2/`. | F. Ceballos + Claude |
| 2026‑06‑10 | **Reestructuración de `13_BEMATE`** — pasa de base de conocimiento (fuentes + índice) a **repositorio oficial de la metodología BeMate** (`BeWayBAIT/BeMate`) con corpus markdown migrado (Marco, 11 manuales, ~74 artefactos, Casos, Operación), modelo de **operador IA** (modos copiloto/primario, umbrales, escalado, decision log con JSON Schemas) y primer piloto e2e preparado. `INDEX.md` sustituye a `INDICE_BASE_CONOCIMIENTO_BEMATE.md` como punto de entrada. | F. Ceballos + Claude |
| 2026‑06‑07 | **Corrección DN** — el área 03 es **Desarrollo de Negocio** (área interna); *Data Native* es el nombre del blueprint/proyecto que vive en `03_DN/blueprint/`, no del área. Corregido en README maestro, portal y README del repo `03_DN`. | F. Ceballos + Claude |
| 2026‑06‑07 | **v3.2** — nueva taxonomía de áreas en tres grupos: **áreas internas** (Ops, DN, Formación, Diseño/IT, Legal, Administración, P&G), **Centros de Excelencia** (CE_Data) y **área de cliente** (BAIT). El área Diseño pasa a denominarse **Diseño/IT** (carpeta y repo conservan `07_Diseno`). Trazabilidad DAMA de las skills: README por skill con metadata, linaje e historial en `00_governance`. | F. Ceballos + Claude |
| 2026‑06‑06 | **v3.1** — nueva identidad del programa: **IRIS — Integración de Riesgos, IA y Sistemas** (adopción de IA bajo responsabilidad humana, *hypothesis-driven AI research*). Alta de la skill `/dama` (DMBOK2 + Diccionario DAMA + Navigating the Labyrinth) en `.claude/skills/` y en `00_governance` (compartida vía GitHub con instalador). Primera revisión DM del workspace contra DAMA: nueva sección *Hoja de ruta Data Management* con 5 gaps priorizados y plan en 3 pasos. | F. Ceballos + Claude |
| 2026‑06‑04 | **v3.0** — alta de `13_BEMATE` (metodología de diseño conductual). Reorganización interna de `01_iris` (`fundacional/`, `Velocidad_1/`, `fuentes/`). Nuevo esquema de GitHub: **un repo por carpeta numerada** (`00_governance`→`13_BEMATE`), nombre de repo idéntico al de la carpeta; recreación completa de los repos en `BeWayIRIS`. | F. Ceballos + Claude |
| 2026‑05‑28 | **v2.0** — modelo de áreas cliente: SCRIPT-IRIS pasa a estar organizado por las 9 áreas de BeWay que consumen IRIS. Nuevas: CE_Data, Diseño, Legal, Administración, P&G. Renumeración completa. | F. Ceballos + Claude |
| 2026‑05‑28 | Subida inicial a `github.com/BeWayIRIS` — 1 repo por carpeta raíz, perfil de org en `.github`, repos viejos archivados. | F. Ceballos + Claude |
| 2026‑05‑28 | **v1.1** — refresco estético del README, alta de `assets/`, ajuste del mapa a la estructura real. | F. Ceballos + Claude |
| 2026‑05‑28 | **v1.0** — reorganización completa según DAMA: 10 carpetas raíz, naming unificado, separación gobierno / proyectos / herramientas. | F. Ceballos + Claude |
| < 2026‑05‑28 | Estructura ad‑hoc por proyecto (BEMATE, CEO, DAMA, IRIS‑BAIT, IRIS‑DN, Manuales‑Formacion, OPERACIONES, Plan_IRIS, Power_automate, old). | F. Ceballos |

---

<div align="center">

<sub>BeWay · Programa IRIS — <em>servamus datum, servamus veritatem</em></sub>

</div>
