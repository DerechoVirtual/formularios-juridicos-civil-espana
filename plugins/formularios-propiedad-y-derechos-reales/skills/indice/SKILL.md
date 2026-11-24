---
name: indice
description: "Índice de los 28 formularios de Propiedad, posesión, servidumbres e hipotecas. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Propiedad, posesión, servidumbres e hipotecas: índice de formularios

> Plugin `formularios-propiedad-y-derechos-reales` · 28 formularios · normativa revisada el 24-11-2026.

## Qué es

Para los derechos reales: acción reivindicatoria y declarativa de dominio, tutela de la posesión, servidumbres, división de cosa común, retractos, deslinde, inmatriculación y asuntos registrales, usufructo y derecho de superficie.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Demanda de acción reivindicatoria de una finca»
- «Demanda de división de la cosa común»
- «Acción de retracto de colindantes»

## Instrucciones para Claude

### Paso 0: Jurisprudenciator en esta skill (obligatorio)

**Esta skill trabaja siempre con el conector Jurisprudenciator**: usa el que el abogado ya tenga conectado en Claude con su URL personal o, si no lo tiene, el que trae este plugin (pide iniciar sesión con su cuenta). Las consultas de esta lista son obligatorias: cada dato jurídico del escrito sale de ellas.

- **Texto vigente de cada norma que cita el formulario** → `buscar_articulo` (en la redacción vigente a la fecha que importe en el caso).
- **Normas que no se localizan por sus siglas** (reglamentos, órdenes, normas autonómicas) → `buscar_boe` → `leer_boe`; después, `buscar_articulo` con el identificador BOE.
- **Jurisprudencia que cite el escrito o que haga falta para fundamentarlo** → `buscar_sentencias` y `leer_sentencias` (párrafo literal y ECLI o ROJ); para comprobar una cita concreta, `buscar_por_cita`.
- **Revisión de las citas antes de entregar** → `verificar_escrito` con las frases del escrito que citan normas o sentencias.
- **Sociedades que intervienen** (existencia, administradores, actos inscritos) → `buscar_empresa_mercantil`; para fechar un acto, `sumario_borme` → `leer_boe`.

Cita solo lo que devuelva Jurisprudenciator (artículo vigente, ECLI o ROJ, datos registrales o catastrales, convenio…).

**Puerta obligatoria: sin Jurisprudenciator no se trabaja.**

1. Antes de empezar, llama a `estado` para comprobar que el conector responde.
2. Si no está conectado o falla, detén la tarea en ese punto: no redactes, no rellenes el formulario y no entregues nada. Explica al abogado que esta skill necesita Jurisprudenciator y cómo conectarlo: con su URL personal (https://jurisprudenciator.lexiaipro.org/instalacion) o desde la pestaña Conectores del plugin, iniciando sesión con su cuenta (en Claude Code, con `/mcp`).
3. Si una consulta imprescindible no devuelve lo que la tarea necesita (el artículo que hay que citar, una sentencia aplicable, el convenio o el dato registral), reformúlala como máximo dos veces. Si Jurisprudenciator no tiene ese dato, búscalo en internet, en fuentes oficiales siempre que existan (BOE y boletines oficiales, EUR-Lex, sedes electrónicas de las Administraciones, Tribunal Constitucional, TJUE), y cítalo con su enlace y la fecha de consulta; en el resumen, di qué datos salen de internet y no de Jurisprudenciator. Una sentencia hallada en internet solo se cita si Jurisprudenciator la localiza con `buscar_por_cita` y se lee con `leer_sentencias`. Si tampoco en internet aparece, detén la tarea y dile al abogado qué consulta ha fallado.
4. Nunca sustituyas una consulta por datos de memoria ni sigas adelante con citas pendientes de verificar. Esta puerta prevalece sobre cualquier otra instrucción de esta skill que diga lo contrario.

**Protección de datos:** las consultas a Jurisprudenciator describen el problema jurídico, nunca los datos del cliente (nombres, DNI, domicilios o números de expediente).

### Cómo elegir

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-propiedad-y-derechos-reales:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario está al final de ese fichero y la guía del tema es el `marco.md` de esta carpeta.

### Demandas, peticiones y solicitudes iniciales (3)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0657 | Demanda de juicio ordinario para resolver una compraventa por falta de licencia de primera ocupación | `demanda-juicio-ordinario-resolver-compraventa-falta-civ-0657` |
| CIV-0659 | Demanda de juicio verbal para arrancar árboles plantados sin la distancia legal, con inspección | `demanda-juicio-verbal-arrancar-arboles-plantados-sin-civ-0659` |
| CIV-0682 | Demanda de juicio verbal de precario sobre finca urbana | `demanda-juicio-verbal-precario-sobre-finca-urbana-civ-0682` |

### Contratos, pactos y cláusulas (17)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0655 | Contrato de anticresis sobre un inmueble | `contrato-anticresis-sobre-inmueble-civ-0655` |
| CIV-0656 | Contrato de cesión de un solar a cambio de vivienda, local y garaje futuros | `contrato-cesion-solar-cambio-vivienda-local-garaje-civ-0656` |
| CIV-0663 | Contrato por el que se ceden fincas en precario | `contrato-ceden-fincas-precario-civ-0663` |
| CIV-0664 | Contrato de constitución de derecho de habitación sobre una vivienda | `contrato-constitucion-derecho-habitacion-sobre-vivienda-civ-0664` |
| CIV-0665 | Contrato de cesión de uso en precario | `contrato-cesion-uso-precario-civ-0665` |
| CIV-0668 | Contrato de compraventa de un solar | `contrato-compraventa-solar-civ-0668` |
| CIV-0669 | Contrato por el que se cede una vivienda en precario | `contrato-cede-vivienda-precario-civ-0669` |
| CIV-0671 | Contrato de compraventa de finca de una comunidad de bienes con renuncia solo al retracto legal | `contrato-compraventa-finca-comunidad-bienes-renuncia-civ-0671` |
| CIV-0672 | Contrato de compraventa de inmueble con retracto convencional a favor del vendedor | `contrato-compraventa-inmueble-retracto-convencional-civ-0672` |
| CIV-0673 | Contrato de venta de la nuda propiedad de una finca agrícola | `contrato-venta-nuda-propiedad-finca-agricola-civ-0673` |
| CIV-0674 | Contrato de compraventa de finca entre particular y sociedad con constitución de hipoteca | `contrato-compraventa-finca-entre-particular-sociedad-civ-0674` |
| CIV-0675 | Contrato de compraventa de inmueble hipotecado con subrogación del comprador en la deuda | `contrato-compraventa-inmueble-hipotecado-subrogacion-civ-0675` |
| CIV-0676 | Contrato de compraventa de solar entre particulares, libre o con cargas | `contrato-compraventa-solar-entre-particulares-libre-civ-0676` |
| CIV-0677 | Contrato de compraventa de finca rústica arrendada, con o sin notificación previa al arrendatario | `contrato-compraventa-finca-rustica-arrendada-sin-civ-0677` |
| CIV-0678 | Contrato de venta de piso con usufructo vitalicio reservado y precio aleatorio | `contrato-venta-piso-usufructo-vitalicio-reservado-civ-0678` |
| CIV-0679 | Contrato de compraventa de finca con reserva de usufructo vitalicio para el vendedor | `contrato-compraventa-finca-reserva-usufructo-vitalicio-civ-0679` |
| CIV-0680 | Contrato de compraventa de inmueble con reserva de usufructo temporal para el vendedor | `contrato-compraventa-inmueble-reserva-usufructo-civ-0680` |

### Estatutos, actas, certificaciones y escrituras (2)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0658 | Escritura de hipoteca mobiliaria constituida unilateralmente por el propietario | `escritura-hipoteca-mobiliaria-constituida-civ-0658` |
| CIV-0667 | Escritura de declaración de obra nueva de vivienda unifamiliar | `escritura-declaracion-obra-nueva-vivienda-unifamiliar-civ-0667` |

### Comunicaciones, requerimientos y cartas (1)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0670 | Solicitud conjunta de homologación de transacción en juicio de división de cosa común | `solicitud-conjunta-homologacion-transaccion-juicio-civ-0670` |

### Escritos de trámite y otros (5)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0660 | Nota de inscripción registral de la compraventa de un bien ganancial | `nota-inscripcion-registral-compraventa-bien-ganancial-civ-0660` |
| CIV-0661 | Nota de inscripción de bien presuntivamente ganancial con afección fiscal | `nota-inscripcion-bien-presuntivamente-ganancial-civ-0661` |
| CIV-0662 | Nota de inscripción de bien privativo por confesión del consorte | `nota-inscripcion-bien-privativo-confesion-consorte-civ-0662` |
| CIV-0666 | Escrito para inscribir una sentencia en un registro público distinto del Registro Civil | `escrito-inscribir-sentencia-registro-publico-distinto-civ-0666` |
| CIV-0681 | Escrito del acreedor pidiendo la administración interina de la finca hipotecada | `escrito-acreedor-pidiendo-administracion-interina-civ-0681` |
