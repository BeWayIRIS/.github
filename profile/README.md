<div align="center">

<img src="assets/omnissiah_phi.svg" alt="BeWay · Cogitator Phi" width="180"/>

# SCRIPT-IRIS

**Repositorio maestro del programa IRIS — Gobierno del Dato en BeWay**

*Ex datis, scientia · Ex scientia, dominium*

</div>

<div align="center">

![Estructura](https://img.shields.io/badge/estructura-v2.0-1f6feb?style=flat-square)
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
| **Última reorganización** | 2026‑05‑28 |
| **Versión de estructura** | v2.0 |
| **GitHub** | [github.com/BeWayIRIS](https://github.com/BeWayIRIS) |

---

## Índice

1. [Modelo](#modelo)
2. [Mapa de carpetas](#mapa-de-carpetas)
3. [Áreas cliente](#áreas-cliente-del-programa-iris)
4. [Convenciones](#convenciones)
5. [Cómo navegar](#cómo-navegar-guía-rápida)
6. [Para futuras sesiones de Claude](#para-futuras-sesiones-de-claude)
7. [Estado del programa](#estado-del-programa-mayo-2026)
8. [Historial de cambios](#historial-de-cambios)

---

## Modelo

El programa IRIS se estructura en tres capas:

1. **Gobierno (`00_governance`)** — marco normativo y de referencia: DAMA, ISO 27001, glosario corporativo, bibliografía. Es el cuerpo doctrinal que aplica a toda la org.
2. **Programa (`01_iris`)** — el propio programa IRIS: documento fundacional, fases, embajadores. Cómo se opera el gobierno del dato dentro de BeWay.
3. **Áreas cliente (`02_…` → `10_…`)** — las 9 áreas de la organización a las que IRIS presta servicio. Cada una tiene su propio espacio + repo en GitHub.

Las carpetas finales (`11_herramientas`, `12_entregables`, `assets`, `_archivo`) son utilidades transversales.

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
├── 01_iris/                Programa IRIS — fundacional + embajadores
│   ├── fase0-fundacional/  Documento fundacional, base v1/v3, FASE0
│   └── embajadores/        Kit, manual, bases y plantillas de embajadores
│
├── 02_Ops/                 Área Operaciones (consumidora de IRIS) ←─ era 02_operaciones
├── 03_DN/                  Área Desarrollo de Negocio              ←─ era 04_DN
├── 04_CE_Data/             Centro de Excelencia de Datos          [NUEVA]
├── 05_BAIT/                Área BAIT — IA para cliente            (sin cambios)
├── 06_Formacion/           Área Formación                          ←─ era 03_formacion
├── 07_Diseno/              Área Diseño                            [NUEVA]
├── 08_Legal/               Área Legal                             [NUEVA]
├── 09_Administracion/      Área Administración                    [NUEVA]
├── 10_PyG/                 Área P&G (People & Growth)             [NUEVA]
│
├── 11_herramientas/        Código, automatizaciones y skills      ←─ era 06_herramientas
├── 12_entregables/         Salidas finales publicables            ←─ era 07_entregables
│
├── assets/                 Activos visuales del repositorio
└── _archivo/               Material deprecated / histórico (no se sube a GitHub)
```

---

## Áreas cliente del programa IRIS

Cada área tiene carpeta local **y** repo privado en GitHub. La estructura interna se está homogeneizando — por defecto se propone `fuentes/`, `procesos/`, `entregables/`.

| # | Área | Carpeta local | Repo GitHub | Estado |
|---|---|---|---|---|
| 02 | **Ops** — Operaciones | `02_Ops/` | [BeWayIRIS/ops](https://github.com/BeWayIRIS/ops) | Activo |
| 03 | **DN** — Desarrollo de Negocio | `03_DN/` | [BeWayIRIS/dn](https://github.com/BeWayIRIS/dn) | Activo (Data Native) |
| 04 | **CE_Data** — Centro de Excelencia de Datos | `04_CE_Data/` | [BeWayIRIS/ce_data](https://github.com/BeWayIRIS/ce_data) | Pendiente de poblar |
| 05 | **BAIT** — IA para cliente | `05_BAIT/` | [BeWayIRIS/bait](https://github.com/BeWayIRIS/bait) | Activo |
| 06 | **Formación** | `06_Formacion/` | [BeWayIRIS/formacion](https://github.com/BeWayIRIS/formacion) | En construcción |
| 07 | **Diseño** | `07_Diseno/` | [BeWayIRIS/diseno](https://github.com/BeWayIRIS/diseno) | Pendiente de poblar |
| 08 | **Legal** | `08_Legal/` | [BeWayIRIS/legal](https://github.com/BeWayIRIS/legal) | Pendiente de poblar |
| 09 | **Administración** | `09_Administracion/` | [BeWayIRIS/administracion](https://github.com/BeWayIRIS/administracion) | Pendiente de poblar |
| 10 | **P&G** — People & Growth | `10_PyG/` | [BeWayIRIS/pyg](https://github.com/BeWayIRIS/pyg) | Pendiente de poblar |

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

- Todos los repos viven en **[BeWayIRIS](https://github.com/BeWayIRIS)**.
- Nombre del