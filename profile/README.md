<div align="center">

<img src="assets/omnissiah_phi.svg" alt="BeWay · Cogitator Phi" width="180"/>

# SCRIPT-IRIS

**Repositorio maestro del programa IRIS — Gobierno del Dato en BeWay**

*Ex datis, scientia · Ex scientia, dominium*

</div>

<div align="center">

![Estructura](https://img.shields.io/badge/estructura-v3.0-1f6feb?style=flat-square)
![Marco](https://img.shields.io/badge/marco-DAMA--DMBOK2-0a7d3f?style=flat-square)
![Norma](https://img.shields.io/badge/norma-ISO%2027001-555?style=flat-square)
![Estado](https://img.shields.io/badge/estado-vivo-success?style=flat-square)

</div>

---

> SCRIPT-IRIS es el espacio de trabajo del **programa IRIS**, el motor de gobierno del dato de **BeWay**.
> El programa presta servicio transversal a las **9 áreas de la organización** y se apoya en **DAMA‑DMBOK2** como marco de referencia.

| | |
|---|---|
| **Propietario** | Francisco C. Ceballos |
| **Contacto** | <franciscoceballos@beway.com> |
| **Última reorganización** | 2026‑06‑04 |
| **Versión de estructura** | v3.0 |
| **GitHub** | [github.com/BeWayIRIS](https://github.com/BeWayIRIS) |

---

## Índice

1. [Modelo](#modelo)
2. [Mapa de carpetas](#mapa-de-carpetas)
3. [Áreas cliente](#áreas-cliente-del-programa-iris)
4. [Convenciones](#convenciones)
5. [Cómo navegar](#cómo-navegar-guía-rápida)
6. [Para futuras sesiones de Claude](#para-futuras-sesiones-de-claude)
7. [Estado del programa](#estado-del-programa-junio-2026)
8. [Historial de cambios](#historial-de-cambios)

---

## Modelo

El programa IRIS se estructura en cuatro capas:

1. **Gobierno (`00_governance`)** — marco normativo y de referencia: DAMA, ISO 27001, glosario corporativo, bibliografía. Es el cuerpo doctrinal que aplica a toda la org.
2. **Programa (`01_iris`)** — el propio programa IRIS: documento fundacional, velocidades de despliegue, embajadores. Cómo se opera el gobierno del dato dentro de BeWay.
3. **Áreas cliente (`02_…` → `10_…`)** — las 9 áreas de la organización a las que IRIS presta servicio. Cada una tiene su propio espacio + repo en GitHub.
4. **Metodologías y utilidades transversales (`11_…` → `13_…`, `assets`, `_archivo`)** — herramientas, entregables publicables y la metodología **BEMATE** de diseño conductual.

---

## Mapa de carpetas

```text
SCRIPT-IRIS/
│
├── 00_governance/          Marco normativo y de gobierno (DAMA, ISO, glosario, bibliografía)
│   ├── dama-dmbok/         Knowledge areas DAMA (EN/ES)
│   ├── iso-27001/          Normativa ISO 27001 y ofertas de securización
│   ├── glosario/           Glosario corporativo único (fuente de verdad)
│   └── bibliografia/       Libros y manuales de referencia
│
├── 01_iris/                Programa IRIS — fundacional, velocidades y embajadores
│   ├── fundacional/        Documento fundacional, bases v1/v3/v4, política de uso de IA, EDA licencias
│   ├── Velocidad_1/        IRIS FASE0, base Velocidad 1, embajadores, gantt
│   └── fuentes/            Insumos: política IA, IRIS_v2, transcritos de reuniones
│
├── 02_Ops/                 Área Operaciones (consumidora de IRIS)
├── 03_DN/                  Área Desarrollo de Negocio (Data Native)
├── 04_CE_Data/             Centro de Excelencia de Datos          [pendiente de poblar]
├── 05_BAIT/                Área BAIT — IA para cliente (Be-Truth)
├── 06_Formacion/           Área Formación (mcp-base, bemate-kb)
├── 07_Diseno/              Área Diseño                            [pendiente de poblar]
├── 08_Legal/               Área Legal                             [pendiente de poblar]
├── 09_Administracion/      Área Administración                    [pendiente de poblar]
├── 10_PyG/                 Área P&G (People & Growth)             [pendiente de poblar]
│
├── 11_herramientas/        Código, automatizaciones y skills
├── 12_entregables/         Salidas finales publicables
├── 13_BEMATE/              Metodología BeMate — diseño conductual (10 pasos + PreWork, 6 CE)  [NUEVA]
│   ├── fuentes/            Manuales paso 01–09, blueprints CE, modelo CEs, contenidos formativos
│   ├── BeSisSol/           Behavioral Systems Solutions (BSS) — auditoría conductual
│   └── INDICE_BASE_CONOCIMIENTO_BEMATE.md   Índice navegable de la base de conocimiento
│
├── assets/                 Activos visuales del repositorio
└── _archivo/               Material deprecated / histórico (no se sube a GitHub)
```

---

## Áreas cliente del programa IRIS

Cada área tiene carpeta local **y** repo privado en GitHub. La estructura interna se está homogeneizando — por defecto se propone `fuentes/`, `procesos/`, `entregables/`.

| # | Área | Carpeta local | Repo GitHub | Estado |
|---|---|---|---|---|
| 02 | **Ops** — Operaciones | `02_Ops/` | [BeWayIRIS/02_Ops](https://github.com/BeWayIRIS/02_Ops) | Activo |
| 03 | **DN** — Desarrollo de Negocio | `03_DN/` | [BeWayIRIS/03_DN](https://github.com/BeWayIRIS/03_DN) | Activo (Data Native) |
| 04 | **CE_Data** — Centro de Excelencia de Datos | `04_CE_Data/` | [BeWayIRIS/04_CE_Data](https://github.com/BeWayIRIS/04_CE_Data) | Pendiente de poblar |
| 05 | **BAIT** — IA para cliente | `05_BAIT/` | [BeWayIRIS/05_BAIT](https://github.com/BeWayIRIS/05_BAIT) | Activo |
| 06 | **Formación** | `06_Formacion/` | [BeWayIRIS/06_Formacion](https://github.com/BeWayIRIS/06_Formacion) | En construcción |
| 07 | **Diseño** | `07_Diseno/` | [BeWayIRIS/07_Diseno](https://github.com/BeWayIRIS/07_Diseno) | Pendiente de poblar |
| 08 | **Legal** | `08_Legal/` | [BeWayIRIS/08_Legal](https://github.com/BeWayIRIS/08_Legal) | Pendiente de poblar |
| 09 | **Administración** | `09_Administracion/` | [BeWayIRIS/09_Administracion](https://github.com/BeWayIRIS/09_Administracion) | Pendiente de poblar |
| 10 | **P&G** — People & Growth | `10_PyG/` | [BeWayIRIS/10_PyG](https://github.com/BeWayIRIS/10_PyG) | Pendiente de poblar |

> El antiguo nombre de P&G era *Talento y Cultura*.

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

- Todos los repos viven en **[BeWayIRIS](https://github.com/BeWayIRIS)** y son **privados**.
- **Un repo por carpeta raíz numerada** (`00_governance` → `13_BEMATE`). El nombre del repo es **idéntico al de la carpeta local**, prefijo numérico incluido, para preservar el orden visual y el mapeo 1:1 carpeta ↔ repo.
- `assets/` y `_archivo/` **no** se suben a GitHub (activos del repo maestro y material deprecated, respectivamente).

---

## Cómo navegar (guía rápida)

| Si buscas… | Ve a |
|---|---|
| Definir un término del negocio | `00_governance/glosario/` |
| Consultar un knowledge area DAMA | `00_governance/dama-dmbok/` |
| Saber qué pide ISO 27001 | `00_governance/iso-27001/` |
| El documento fundacional de IRIS | `01_iris/fundacional/` |
| Material para embajadores IRIS | `01_iris/Velocidad_1/embajadores/` |
| Diagrama SIPOC de un proceso | `02_Ops/context-diagrams/` |
| Inventario documental | `02_Ops/inventarios/` |
| Blueprint Data Native | `03_DN/blueprint/` |
| Material Be-Truth | `05_BAIT/Be-Truth/` |
| Material de formación | `06_Formacion/` |
| Metodología BeMate (10 pasos, CE) | `13_BEMATE/` |
| Script o automatización | `11_herramientas/` |
| Una versión publicada y estable | `12_entregables/` |
| Algo antiguo o deprecated | `_archivo/` |

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

---

## Estado del programa (junio 2026)

| Capa | Estado | Notas |
|---|---|---|
| `00_governance` | Estable | En mantenimiento. |
| `01_iris` | Activo | Fundacional cerrado; Velocidad 1 en despliegue + selección de embajadores. |
| `02_Ops` | Activo | Modelando procesos 2.0. |
| `03_DN` | Activo | Blueprint v1 entregado (Data Native). |
| `04_CE_Data` | Pendiente | Por arrancar. |
| `05_BAIT` | Activo | Marco conceptual v0; refinando M1‑M2. |
| `06_Formacion` | En construcción | MCP base operativo; BeMate KB en consolidación. |
| `07_Diseno` | Pendiente | Por arrancar. |
| `08_Legal` | Pendiente | Por arrancar. |
| `09_Administracion` | Pendiente | Por arrancar. |
| `10_PyG` | Pendiente | Por arrancar. |
| `11_herramientas` | Mixto | `slack-downloader` operativo; resto en evaluación. |
| `12_entregables` | Pendiente | A poblar desde proyectos individuales. |
| `13_BEMATE` | Activo | Base de conocimiento e índice navegable; BeSisSol (BSS) en Fase 1. |

---

## Historial de cambios

| Fecha | Cambio | Responsable |
|---|---|---|
| 2026‑06‑04 | **v3.0** — alta de `13_BEMATE` (metodología de diseño conductual). Reorganización interna de `01_iris` (`fundacional/`, `Velocidad_1/`, `fuentes/`)