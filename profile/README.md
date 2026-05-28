<div align="center">

<img src="assets/omnissiah_phi.svg" alt="BeWay · Cogitator Phi" width="180"/>

# SCRIPT-IRIS

**Repositorio maestro de Gobierno del Dato — BeWay**

*Ex datis, scientia · Ex scientia, dominium*

</div>

<div align="center">

![Estructura](https://img.shields.io/badge/estructura-v1.1-1f6feb?style=flat-square)
![Marco](https://img.shields.io/badge/marco-DAMA--DMBOK2-0a7d3f?style=flat-square)
![Norma](https://img.shields.io/badge/norma-ISO%2027001-555?style=flat-square)
![Estado](https://img.shields.io/badge/estado-vivo-success?style=flat-square)

</div>

---

> Workspace unificado para los proyectos de gobierno, arquitectura y operación del dato en **BeWay**.
> Estructura inspirada en **DAMA‑DMBOK2** (knowledge areas + ciclo de vida del dato) y en buenas prácticas de gestión documental.

| | |
|---|---|
| **Propietario** | Francisco C. Ceballos |
| **Contacto** | <franciscoceballos@beway.com> |
| **Última reorganización** | 2026‑05‑28 |
| **Versión de estructura** | v1.1 |

---

## Índice

1. [Mapa de carpetas](#mapa-de-carpetas)
2. [Convenciones](#convenciones)
3. [Cómo navegar](#cómo-navegar-guía-rápida)
4. [Para futuras sesiones de Claude](#para-futuras-sesiones-de-claude)
5. [Estado de los proyectos](#estado-de-los-proyectos-mayo-2026)
6. [Historial de cambios](#historial-de-cambios)

---

## Mapa de carpetas

```text
SCRIPT-IRIS/
│
├── 00_governance/          Marco normativo y de gobierno (DAMA, ISO, glosario, bibliografía)
│   ├── dama-dmbok/         Knowledge areas DAMA en .qmd / .html (EN/ES) · repo BeWayIRIS/DM
│   ├── iso-27001/          Normativa ISO 27001 y ofertas de securización
│   ├── glosario/           Glosario corporativo único (fuente de verdad)
│   └── bibliografia/       Libros y manuales de referencia (DAMA-DMBOK, Labyrinth, ISO)
│
├── 01_iris/                Plan IRIS — programa fundacional de gobierno del dato
│   ├── fase0-fundacional/  Documento fundacional, base v1/v3, FASE0 · repo BeWayIRIS/Plan_IRIS
│   └── embajadores/        Kit pre-entrevista, manual embajador, bases, plantillas
│
├── 02_operaciones/         Proyecto OPERACIONES — modelo operativo del dato
│   ├── procesos/           OPS_anexo_DAMA, OPS_recomendaciones, Proceso Ops 2.0
│   ├── context-diagrams/   Diagramas SIPOC (E1–E4, M0) + payloads JSON
│   ├── inventarios/        Inventario descriptivo y documental
│   └── fuentes/            Documentos originales que alimentan operaciones
│
├── 03_formacion/           Formación y bases de conocimiento operativas
│   ├── mcp-base/           MCP formación base · repo BeWayIRIS/Manuales-Formacion
│   └── bemate-kb/          Base de conocimiento BeMate
│
├── 04_DN/                  Proyecto Data Native — blueprint operativo del dato
│   ├── blueprint/          DN_DataManagement y derivados
│   ├── ceremonias/         Definición de ceremonias y rituales del dato
│   ├── transcripciones/    Transcripciones de audios fuente
│   └── fuentes/            Blueprint original, audios .ogg, informes
│
├── 05_BAIT/                Proyecto BAIT — experimentación con datos
│   └── Be-Truth/           Material completo Be-Truth (00_proyecto → 05_conexion_M2)
│
├── 06_herramientas/        Código, automatizaciones y skills
│   ├── slack-downloader/   Herramienta Python para descarga de Slack
│   ├── power-automate/     Flujos Power Automate (reservado)
│   └── skills/             Skills de Claude (skill-context-diagram, …)
│
├── 07_entregables/         Salidas finales publicables (.docx, .pdf, .html versionados)
│
├── assets/                 Activos visuales del repositorio (logos, marcas de agua)
│
└── _archivo/               Material deprecated o histórico
    ├── old/                Estructura ad-hoc previa (ex BeWayData/IRIS)
    └── _backup_pre_migracion_20260528.tar.gz   Snapshot pre-reorganización
```

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
| `_drafts/` | Borradores y versiones de trabajo. |
| `_archivo/` | Material deprecated dentro de un proyecto. |
| `metadata/` | **DEPRECATED** — sustituido por `fuentes/` para mayor claridad. |

### Versionado

- Cambios menores: editar en sitio.
- Cambios mayores: nuevo archivo con sufijo `_vN`.
- Archivos abandonados: mover a `_archivo/` del proyecto, no borrar.

### Git

Cada proyecto con repo propio mantiene su `.git/` interno. Remotos actuales (verificar antes de renombrar en GitHub):

| Carpeta local | Remoto |
|---|---|
| `00_governance/dama-dmbok/` | `BeWayIRIS/DM` |
| `01_iris/fase0-fundacional/` | `BeWayIRIS/Plan_IRIS` |
| `03_formacion/mcp-base/` | `BeWayIRIS/Manuales-Formacion` |
| `_archivo/old/` | `BeWayData/IRIS` |

---

## Cómo navegar (guía rápida)

| Si buscas… | Ve a |
|---|---|
| Definir un término del negocio | `00_governance/glosario/` |
| Consultar un knowledge area DAMA | `00_governance/dama-dmbok/` |
| Saber qué pide ISO 27001 | `00_governance/iso-27001/` |
| El documento fundacional de IRIS | `01_iris/fase0-fundacional/` |
| Material para embajadores IRIS | `01_iris/embajadores/` |
| Diagrama SIPOC de un proceso | `02_operaciones/context-diagrams/` |
| Inventario documental | `02_operaciones/inventarios/` |
| Material de formación | `03_formacion/` |
| Blueprint Data Native | `04_DN/blueprint/` |
| Material Be-Truth | `05_BAIT/Be-Truth/` |
| Script o automatización | `06_herramientas/` |
| Una versión publicada y estable | `07_entregables/` |
| Algo antiguo o deprecated | `_archivo/` |

---

## Para futuras sesiones de Claude

> Esta sección sirve como *system prompt* implícito del repositorio.
> Si una sesión de Claude entra aquí sin contexto previo, debe leer este README primero.

**Reglas operativas:**

1. **Antes de crear un archivo nuevo**, comprobar que no existe ya algo equivalente en su carpeta correspondiente.
2. **Nunca duplicar contenido entre carpetas raíz** — si un activo es transversal, vive en `00_governance/`.
3. **Las fuentes originales (insumos) van en `fuentes/`**, los entregables publicados en `07_e