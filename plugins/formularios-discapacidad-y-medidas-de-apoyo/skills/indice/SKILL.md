---
name: indice
description: "Índice de los 46 formularios de Discapacidad y medidas de apoyo (Ley 8/2021). Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Discapacidad y medidas de apoyo (Ley 8/2021): índice de formularios

> Plugin `formularios-discapacidad-y-medidas-de-apoyo` · 46 formularios · normativa revisada el 25-11-2026.

## Qué es

Para las personas con discapacidad tras la Ley 8/2021: provisión de medidas de apoyo, curatela, defensor judicial, guarda de hecho, autocuratela, revisión de medidas, internamientos no voluntarios y rendición de cuentas.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Solicitud de provisión de medidas de apoyo para una persona mayor»
- «Nombramiento de defensor judicial»
- «Revisión de las medidas de apoyo»

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

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-discapacidad-y-medidas-de-apoyo:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario que se rellena está en `../<skill>/assets/formulario.md` y la guía del tema es el `marco.md` de esta carpeta.

### Demandas, peticiones y solicitudes iniciales (4)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0382 | Solicitud de nombramiento de defensor judicial para el tutelado | `solicitud-nombramiento-defensor-judicial-tutelado-civ-0382` |
| CIV-0387 | Demanda de constitución de curatela o asistencia y nombramiento de curador (Derecho foral aragonés) | `demanda-constitucion-curatela-asistencia-nombramiento-civ-0387` |
| CIV-0390 | Demanda de curatela o asistencia y nombramiento de curador o asistente (Derecho civil catalán) | `demanda-curatela-asistencia-nombramiento-curador-civ-0390` |
| CIV-0398 | Demanda contenciosa de revisión de las medidas judiciales de apoyo a persona con discapacidad | `demanda-contenciosa-revision-medidas-judiciales-apoyo-civ-0398` |

### Contestaciones, oposiciones y alegaciones (3)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0394 | Contestación a la demanda de medidas judiciales de apoyo a persona con discapacidad | `contestacion-demanda-medidas-judiciales-apoyo-persona-civ-0394` |
| CIV-2326 | Escrito de oposición a la apelación en el proceso de medidas judiciales de apoyo a la discapacidad | `escrito-oposicion-apelacion-proceso-medidas-judiciales-civ-2326` |
| CIV-2330 | Contestación que se opone a la demanda de medidas de apoyo y propone un curador si se estima | `contestacion-opone-demanda-medidas-apoyo-propone-civ-2330` |

### Recursos (5)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0391 | Recurso de apelación contra el auto que acuerda el internamiento | `recurso-apelacion-contra-auto-acuerda-internamiento-civ-0391` |
| CIV-0395 | Recurso de apelación contra la sentencia sobre medidas de apoyo a persona con discapacidad | `recurso-apelacion-contra-sentencia-sobre-medidas-apoyo-civ-0395` |
| CIV-2322 | Recurso de apelación con prueba en segunda instancia contra la denegación de medidas de apoyo | `recurso-apelacion-prueba-segunda-instancia-contra-civ-2322` |
| CIV-2327 | Recurso de apelación contra la sentencia dictada en el proceso de medidas judiciales de apoyo | `recurso-apelacion-contra-sentencia-dictada-proceso-civ-2327` |
| CIV-2329 | Recurso de reposición contra el auto que deniega prueba en apelación sobre medidas de apoyo | `recurso-reposicion-contra-auto-deniega-prueba-civ-2329` |

### Contratos, pactos y cláusulas (1)

| Código | Formulario | Skill |
|---|---|---|
| CIV-2320 | Contrato de compraventa de bienes de menores o de personas con discapacidad | `contrato-compraventa-bienes-menores-personas-civ-2320` |

### Comunicaciones, requerimientos y cartas (7)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0384 | Solicitud de jurisdicción voluntaria para nombrar asistente (Derecho civil catalán) | `solicitud-jurisdiccion-voluntaria-nombrar-asistente-civ-0384` |
| CIV-0385 | Solicitud de autorización de internamiento no voluntario en un centro geriátrico | `solicitud-autorizacion-internamiento-no-voluntario-civ-0385` |
| CIV-0392 | Solicitud del tutelado de revisar la tutela y remover al tutor | `solicitud-tutelado-revisar-tutela-remover-tutor-civ-0392` |
| CIV-0393 | Solicitud en jurisdicción voluntaria de curatela para persona con ludopatía grave | `solicitud-jurisdiccion-voluntaria-curatela-persona-civ-0393` |
| CIV-0397 | Solicitud de administrador de bienes como medida cautelar junto con la demanda de medidas de apoyo | `solicitud-administrador-bienes-como-medida-cautelar-civ-0397` |
| CIV-0400 | Solicitud de revisión en jurisdicción voluntaria de las medidas de apoyo a persona con discapacidad | `solicitud-revision-jurisdiccion-voluntaria-medidas-civ-0400` |
| CIV-2318 | Comunicación del hospital al tribunal de un internamiento psiquiátrico urgente de un adulto | `comunicacion-hospital-tribunal-internamiento-civ-2318` |

### Escritos de trámite y otros (26)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0373 | Escrito del tutor pidiendo autorización para internar al tutelado en centro de educación especial | `escrito-tutor-pidiendo-autorizacion-internar-tutelado-civ-0373` |
| CIV-0374 | Escrito del curador pidiendo prórroga del plazo para inventariar los bienes del curatelado | `escrito-curador-pidiendo-prorroga-plazo-inventariar-civ-0374` |
| CIV-0375 | Escrito del tutor pidiendo autorización judicial para demandar en nombre del tutelado | `escrito-tutor-pidiendo-autorizacion-judicial-demandar-civ-0375` |
| CIV-0376 | Escrito pidiendo excluir del cargo de tutor a una persona inhábil | `escrito-pidiendo-excluir-cargo-tutor-persona-inhabil-civ-0376` |
| CIV-0377 | Escrito de excusa sobrevenida para seguir en el cargo de tutor o curador | `escrito-excusa-sobrevenida-seguir-cargo-tutor-curador-civ-0377` |
| CIV-0378 | Escrito de excusa para no aceptar el cargo de tutor | `escrito-excusa-no-aceptar-cargo-tutor-civ-0378` |
| CIV-0379 | Escrito del tutor con informe de la situación del tutelado y rendición anual de cuentas | `escrito-tutor-informe-situacion-tutelado-rendicion-civ-0379` |
| CIV-0380 | Escrito alegando excusa sobrevenida para seguir como curador | `escrito-alegando-excusa-sobrevenida-seguir-como-curador-civ-0380` |
| CIV-0381 | Escrito que comunica al tribunal el fallecimiento del tutelado | `escrito-comunica-tribunal-fallecimiento-tutelado-civ-0381` |
| CIV-0383 | Escrito del tutor pidiendo retribución por el ejercicio de la tutela | `escrito-tutor-pidiendo-retribucion-ejercicio-tutela-civ-0383` |
| CIV-0386 | Documento de voluntades anticipadas o testamento vital | `documento-voluntades-anticipadas-testamento-vital-civ-0386` |
| CIV-0388 | Expediente de jurisdicción voluntaria para constituir curatela de menor emancipado (Cataluña) | `expediente-jurisdiccion-voluntaria-constituir-curatela-civ-0388` |
| CIV-0389 | Expediente de jurisdicción voluntaria para constituir tutela y nombrar tutor (Aragón) | `expediente-jurisdiccion-voluntaria-constituir-tutela-civ-0389` |
| CIV-0396 | Escrito solicitando el internamiento no voluntario por trastorno psíquico de una persona adulta | `escrito-solicitando-internamiento-no-voluntario-civ-0396` |
| CIV-0399 | Escrito de medidas cautelares previas a la demanda de apoyos judiciales a persona con discapacidad | `escrito-medidas-cautelares-previas-demanda-apoyos-civ-0399` |
| CIV-2316 | Escrito que pone en conocimiento del Fiscal hechos que pueden requerir medidas de apoyo | `escrito-pone-conocimiento-fiscal-hechos-pueden-civ-2316` |
| CIV-2317 | Escrito que pide comunicar al Registro de la Propiedad la sentencia de medidas de apoyo | `escrito-pide-comunicar-registro-propiedad-sentencia-civ-2317` |
| CIV-2319 | Escrito del defensor de la persona con discapacidad conforme con la demanda del Fiscal | `escrito-defensor-persona-discapacidad-conforme-demanda-civ-2319` |
| CIV-2321 | Otrosí en demanda de medidas de apoyo para nombrar un curador de la persona y otro de los bienes | `otrosi-demanda-medidas-apoyo-nombrar-curador-persona-civ-2321` |
| CIV-2323 | Escrito que pide cautelares sobre el patrimonio tras presentar la demanda de medidas de apoyo | `escrito-pide-cautelares-sobre-patrimonio-tras-civ-2323` |
| CIV-2324 | Escrito entre dos sesiones de la vista de medidas de apoyo que alega hechos y pide prueba | `escrito-entre-dos-sesiones-vista-medidas-apoyo-alega-civ-2324` |
| CIV-2325 | Impugnación de la reposición contra el auto que deniega prueba en apelación sobre medidas de apoyo | `impugnacion-reposicion-contra-auto-deniega-prueba-civ-2325` |
| CIV-2328 | Petición de subsanación de la sentencia que omitió fijar el régimen de medidas de apoyo | `peticion-subsanacion-sentencia-omitio-fijar-regimen-civ-2328` |
| CIV-2331 | Escrito en segunda instancia del proceso de medidas de apoyo que alega hechos nuevos y pide prueba | `escrito-segunda-instancia-proceso-medidas-apoyo-alega-civ-2331` |
| CIV-2332 | Desistimiento del proceso de medidas de apoyo antes de que se persone la persona afectada | `desistimiento-proceso-medidas-apoyo-antes-persone-civ-2332` |
| CIV-2333 | Otrosí de la demanda de medidas de apoyo que pide designar quién representará a la persona afectada | `otrosi-demanda-medidas-apoyo-pide-designar-quien-civ-2333` |
