---
name: indice
description: "Índice de los 46 formularios de Comunidades de propietarios. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Comunidades de propietarios: índice de formularios

> Plugin `formularios-comunidades-de-propietarios` · 46 formularios · normativa revisada el 24-11-2026.

## Qué es

Para la propiedad horizontal: convocatorias y actas de junta, estatutos, impugnación de acuerdos, reclamación de cuotas a morosos, obras en elementos comunes y privativos, actividades molestas y relaciones con el administrador.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Impugnación de un acuerdo de la junta de propietarios»
- «Reclamación de cuotas de comunidad impagadas»
- «Acción de cesación por actividad molesta en un piso»

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

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-comunidades-de-propietarios:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario está al final de ese fichero y la guía del tema es el `marco.md` de esta carpeta.

### Demandas, peticiones y solicitudes iniciales (16)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0612 | Demanda de un propietario para suspender una obra nueva hecha sin consentimiento de la comunidad | `demanda-propietario-suspender-obra-nueva-hecha-sin-civ-0612` |
| CIV-0616 | Demanda de la comunidad contra el secretario-administrador cesado para que entregue la documentación | `demanda-comunidad-contra-secretario-administrador-civ-0616` |
| CIV-0617 | Demanda de reclamación de gastos extraordinarios a un propietario de una comunidad | `demanda-reclamacion-gastos-extraordinarios-propietario-civ-0617` |
| CIV-0618 | Demanda de juicio de equidad en propiedad horizontal sobre instalar contadores individuales de agua | `demanda-juicio-equidad-propiedad-horizontal-sobre-civ-0618` |
| CIV-0620 | Demanda de la comunidad de propietarios contra el administrador por rendición de cuentas y daños | `demanda-comunidad-propietarios-contra-administrador-civ-0620` |
| CIV-0621 | Demanda de juicio verbal para reclamar cuotas de la comunidad de propietarios | `demanda-juicio-verbal-reclamar-cuotas-comunidad-civ-0621` |
| CIV-0628 | Demanda para declarar ilegales las cuotas de participación en elementos comunes y redistribuirlas | `demanda-declarar-ilegales-cuotas-participacion-civ-0628` |
| CIV-0630 | Demanda de la comunidad contra un propietario por obras en su elemento privativo (Cataluña) | `demanda-comunidad-contra-propietario-obras-elemento-civ-0630` |
| CIV-0631 | Demanda de impugnación de un acuerdo de la junta de propietarios por abuso de derecho (Cataluña) | `demanda-impugnacion-acuerdo-junta-propietarios-abuso-civ-0631` |
| CIV-0639 | Demanda de juicio ordinario de impugnación de acuerdos de la junta de propietarios | `demanda-juicio-ordinario-impugnacion-acuerdos-junta-civ-0639` |
| CIV-0647 | Demanda de juicio ordinario de un propietario contra la comunidad por daños de elementos comunes | `demanda-juicio-ordinario-propietario-contra-comunidad-civ-0647` |
| CIV-0648 | Demanda de juicio de equidad en propiedad horizontal para nombrar presidente de la comunidad | `demanda-juicio-equidad-propiedad-horizontal-nombrar-civ-0648` |
| CIV-0649 | Demanda de juicio de equidad en propiedad horizontal para adoptar acuerdo sin mayorías legales | `demanda-juicio-equidad-propiedad-horizontal-adoptar-civ-0649` |
| CIV-0652 | Demanda de impugnación de acuerdos de la comunidad por falta de citación a la junta | `demanda-impugnacion-acuerdos-comunidad-falta-citacion-civ-0652` |
| CIV-0653 | Demanda de privación del uso de vivienda por actividades dañosas o prohibidas en la comunidad | `demanda-privacion-uso-vivienda-actividades-danosas-civ-0653` |
| CIV-0654 | Demanda por alteración no consentida de elementos privativos que afecta a elementos comunes | `demanda-alteracion-no-consentida-elementos-privativos-civ-0654` |

### Contestaciones, oposiciones y alegaciones (4)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0613 | Oposición al monitorio por gastos comunes de comunidad de propietarios de menos de 2.000 euros | `oposicion-monitorio-gastos-comunes-comunidad-civ-0613` |
| CIV-0614 | Oposición al monitorio por gastos comunes de comunidad de propietarios de entre 2.000 y 15.000 euros | `oposicion-monitorio-gastos-comunes-comunidad-civ-0614` |
| CIV-0615 | Oposición al monitorio por gastos comunes de comunidad de propietarios de más de 15.000 euros | `oposicion-monitorio-gastos-comunes-comunidad-civ-0615` |
| CIV-0640 | Contestación en propiedad horizontal con reconvención de reclamación de cantidades al propietario | `contestacion-propiedad-horizontal-reconvencion-civ-0640` |

### Contratos, pactos y cláusulas (2)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0622 | Contrato de servicios de limpieza para una comunidad de propietarios | `contrato-servicios-limpieza-comunidad-propietarios-civ-0622` |
| CIV-0624 | Contrato de arrendamiento de un elemento común para instalar antenas de telefonía | `contrato-arrendamiento-elemento-comun-instalar-antenas-civ-0624` |

### Estatutos, actas, certificaciones y escrituras (8)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0623 | Estatutos de una subcomunidad de plazas de garaje y trasteros | `estatutos-subcomunidad-plazas-garaje-trasteros-civ-0623` |
| CIV-0633 | Estatutos de una comunidad de propietarios | `estatutos-comunidad-propietarios-civ-0633` |
| CIV-0634 | Acta de constitución de una comunidad de propietarios | `acta-constitucion-comunidad-propietarios-civ-0634` |
| CIV-0635 | Estatutos reguladores de una urbanización | `estatutos-reguladores-urbanizacion-civ-0635` |
| CIV-0638 | Escritura de declaración de obra nueva y división horizontal | `escritura-declaracion-obra-nueva-division-horizontal-civ-0638` |
| CIV-0642 | Acta de junta de propietarios que aprueba la liquidación de deuda y la reclamación al moroso | `acta-junta-propietarios-aprueba-liquidacion-deuda-civ-0642` |
| CIV-0646 | Acta de junta de propietarios que acuerda la remoción de cargos electos | `acta-junta-propietarios-acuerda-remocion-cargos-electos-civ-0646` |
| CIV-0651 | Convocatoria de junta ordinaria de propietarios por el presidente de la comunidad | `convocatoria-junta-ordinaria-propietarios-presidente-civ-0651` |

### Comunicaciones, requerimientos y cartas (7)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0609 | Comunicación a la junta de propietarios para dividir materialmente un elemento privativo | `comunicacion-junta-propietarios-dividir-materialmente-civ-0609` |
| CIV-0611 | Comunicación del administrador de la comunidad sobre la necesidad de reparaciones urgentes | `comunicacion-administrador-comunidad-sobre-necesidad-civ-0611` |
| CIV-0625 | Comunicación del propietario disidente que cambia el sentido de su voto | `comunicacion-propietario-disidente-cambia-sentido-voto-civ-0625` |
| CIV-0626 | Comunicación de supresión del servicio de portería o conserjería | `comunicacion-supresion-servicio-porteria-conserjeria-civ-0626` |
| CIV-0627 | Comunicación para encargar un informe técnico sobre una instalación o servicio común | `comunicacion-encargar-informe-tecnico-sobre-civ-0627` |
| CIV-0632 | Solicitud de diligenciado del libro de actas en el Registro por una comunidad recién constituida | `solicitud-diligenciado-libro-actas-registro-comunidad-civ-0632` |
| CIV-0641 | Requerimiento al propietario para que cese en actividades prohibidas en la comunidad | `requerimiento-propietario-cese-actividades-prohibidas-civ-0641` |

### Escritos de trámite y otros (9)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0610 | Escrito del propietario disidente que solicita acceso a servicios o instalaciones comunitarias | `escrito-propietario-disidente-solicita-acceso-civ-0610` |
| CIV-0619 | Diligencia del administrador-secretario que subsana un error en el acta de la junta de propietarios | `diligencia-administrador-secretario-subsana-error-acta-civ-0619` |
| CIV-0629 | División Horizontal (escritura) | `division-horizontal-escritura-civ-0629` |
| CIV-0636 | Reglamento de régimen interior de una comunidad de propietarios | `reglamento-regimen-interior-comunidad-propietarios-civ-0636` |
| CIV-0637 | Normas de régimen interior de una urbanización | `normas-regimen-interior-urbanizacion-civ-0637` |
| CIV-0643 | Instancia al Registro de la Propiedad para diligenciar el libro de actas de la comunidad | `instancia-registro-propiedad-diligenciar-libro-actas-civ-0643` |
| CIV-0644 | Autorización escrita para representar a un propietario en la junta | `autorizacion-escrita-representar-propietario-junta-civ-0644` |
| CIV-0645 | Designación de representante en la junta por los copropietarios proindiviso de un piso o local | `designacion-representante-junta-copropietarios-civ-0645` |
| CIV-0650 | Encabezamiento de demanda monitoria de la comunidad de propietarios presentada por su presidente | `encabezamiento-demanda-monitoria-comunidad-civ-0650` |
