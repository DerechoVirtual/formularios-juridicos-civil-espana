---
name: indice
description: "Índice de los 219 formularios de Alquileres y desahucios. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Alquileres y desahucios: índice de formularios

> Plugin `formularios-alquileres-y-desahucios` · 219 formularios · normativa revisada el 25-11-2026.

## Qué es

Para los arrendamientos urbanos y rústicos: contratos de vivienda y de local, cesión y subarriendo, actualización de renta, obras, fianza, requerimientos y burofaxes, desahucio por impago, por expiración del plazo y por precario, y reclamación de rentas.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Contrato de alquiler de vivienda habitual conforme a la LAU»
- «Demanda de desahucio por falta de pago y reclamación de rentas»
- «Requerimiento de pago al inquilino antes del desahucio»

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

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-alquileres-y-desahucios:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario que se rellena está en `../<skill>/assets/formulario.md` y la guía del tema es el `marco.md` de esta carpeta.

### Demandas, peticiones y solicitudes iniciales (66)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0502 | Demanda del inquilino para que el arrendador haga las obras de conservación de la vivienda (LAU 94) | `demanda-inquilino-arrendador-haga-obras-conservacion-civ-0502` |
| CIV-0509 | Demanda de desahucio por impago y reclamación de rentas contra el inquilino y su fiador solidario | `demanda-desahucio-impago-reclamacion-rentas-contra-civ-0509` |
| CIV-0510 | Demanda de juicio verbal de desahucio de vivienda por impago de la renta | `demanda-juicio-verbal-desahucio-vivienda-impago-renta-civ-0510` |
| CIV-0520 | Demanda de indemnización por resolución unilateral del arrendamiento de local por el inquilino | `demanda-indemnizacion-resolucion-unilateral-civ-0520` |
| CIV-0521 | Demanda de resolución de arrendamiento anterior a 1995 por cierre del local o desocupación sin causa | `demanda-resolucion-arrendamiento-anterior-1995-cierre-civ-0521` |
| CIV-0522 | Demanda de juicio verbal del inquilino para recuperar la fianza de vivienda (LAU 1994) | `demanda-juicio-verbal-inquilino-recuperar-fianza-civ-0522` |
| CIV-0524 | Demanda de juicio ordinario para resolver el arrendamiento de industria y recuperar el local | `demanda-juicio-ordinario-resolver-arrendamiento-civ-0524` |
| CIV-0530 | Demanda para extinguir el arrendamiento de local de negocio (LAU 1964) por necesidad del hijo | `demanda-extinguir-arrendamiento-local-negocio-lau-1964-civ-0530` |
| CIV-0534 | Demanda de resolución de arrendamiento de vivienda por necesidad del arrendador (posterior a 1995) | `demanda-resolucion-arrendamiento-vivienda-necesidad-civ-0534` |
| CIV-0535 | Demanda de resolución del arrendamiento por ocupar el inquilino varias viviendas (anterior a 1995) | `demanda-resolucion-arrendamiento-ocupar-inquilino-civ-0535` |
| CIV-0541 | Demanda sucinta de desahucio por falta de pago de las rentas | `demanda-sucinta-desahucio-falta-pago-rentas-civ-0541` |
| CIV-0542 | Demanda sucinta de desahucio por falta de pago con acumulación de la reclamación de rentas | `demanda-sucinta-desahucio-falta-pago-acumulacion-civ-0542` |
| CIV-0552 | Demanda de desahucio por impago y reclamación de rentas, sin enervación y con condonación de deuda | `demanda-desahucio-impago-reclamacion-rentas-sin-civ-0552` |
| CIV-0554 | Demanda de desahucio de local de negocio por expiración del plazo del contrato | `demanda-desahucio-local-negocio-expiracion-plazo-civ-0554` |
| CIV-0556 | Demanda de desahucio por precario de local trastero | `demanda-desahucio-precario-local-trastero-civ-0556` |
| CIV-0558 | Demanda de juicio verbal de reclamación de rentas impagadas | `demanda-juicio-verbal-reclamacion-rentas-impagadas-civ-0558` |
| CIV-0559 | Demanda de juicio verbal de desahucio de finca rústica por expiración del plazo del contrato | `demanda-juicio-verbal-desahucio-finca-rustica-civ-0559` |
| CIV-0562 | Demanda de resolución de arrendamiento de vivienda por subarriendo inconsentido (anterior a 1995) | `demanda-resolucion-arrendamiento-vivienda-subarriendo-civ-0562` |
| CIV-0563 | Demanda de resolución de arrendamiento de vivienda por cesión inconsentida (posterior a 1995) | `demanda-resolucion-arrendamiento-vivienda-cesion-civ-0563` |
| CIV-0564 | Demanda de desahucio de finca rústica por impago, con enervación y lanzamiento anticipado | `demanda-desahucio-finca-rustica-impago-enervacion-civ-0564` |
| CIV-0565 | Demanda de resolución de arrendamiento de uso distinto de vivienda por subarriendo (LAU 1994) | `demanda-resolucion-arrendamiento-uso-distinto-vivienda-civ-0565` |
| CIV-0566 | Demanda de resolución de arrendamiento de vivienda por subarriendo inconsentido (posterior a 1995) | `demanda-resolucion-arrendamiento-vivienda-subarriendo-civ-0566` |
| CIV-0567 | Demanda de resolución de arrendamiento de local por subarriendo o traspaso no autorizado (LAU 1964) | `demanda-resolucion-arrendamiento-local-subarriendo-civ-0567` |
| CIV-0568 | Demanda de extinción de arrendamiento de vivienda por no notificar la subrogación mortis causa | `demanda-extincion-arrendamiento-vivienda-no-notificar-civ-0568` |
| CIV-0569 | Demanda verbal de rentas debidas tras extinguirse el arrendamiento hasta recuperar la posesión | `demanda-verbal-rentas-debidas-tras-extinguirse-civ-0569` |
| CIV-0577 | Demanda de desahucio de vivienda por impago de rentas (contrato posterior a 1995), sin enervación | `demanda-desahucio-vivienda-impago-rentas-contrato-civ-0577` |
| CIV-0579 | Demanda de desahucio por impago y rentas de vivienda, sin enervación por requerimiento fehaciente | `demanda-desahucio-impago-rentas-vivienda-sin-civ-0579` |
| CIV-0580 | Demanda de desahucio por impago y reclamación de rentas de vivienda, sin posibilidad de enervación | `demanda-desahucio-impago-reclamacion-rentas-vivienda-civ-0580` |
| CIV-0581 | Demanda de desahucio por impago y reclamación de rentas de vivienda, con posibilidad de enervación | `demanda-desahucio-impago-reclamacion-rentas-vivienda-civ-0581` |
| CIV-0582 | Demanda de desahucio de local por impago, con ofrecimiento de transacción sobre las rentas | `demanda-desahucio-local-impago-ofrecimiento-civ-0582` |
| CIV-0594 | Demanda de resolución de arrendamiento de vivienda por cesión no consentida (contrato previo a 1995) | `demanda-resolucion-arrendamiento-vivienda-cesion-no-civ-0594` |
| CIV-0595 | Demanda de juicio ordinario para reclamar la actualización de rentas, con acumulación subjetiva | `demanda-juicio-ordinario-reclamar-actualizacion-rentas-civ-0595` |
| CIV-0596 | Demanda del arrendatario de finca urbana que ejercita el retracto contra el comprador | `demanda-arrendatario-finca-urbana-ejercita-retracto-civ-0596` |
| CIV-0598 | Demanda de resolución de arrendamiento por falta de reparaciones del arrendador (vivienda, LAU 1994) | `demanda-resolucion-arrendamiento-falta-reparaciones-civ-0598` |
| CIV-0599 | Demanda de resolución de arrendamiento rústico y reclamación de daños por obras no autorizadas | `demanda-resolucion-arrendamiento-rustico-reclamacion-civ-0599` |
| CIV-0601 | Demanda de desahucio de arrendamiento rústico anterior a 2004 por fin del plazo y prórrogas legales | `demanda-desahucio-arrendamiento-rustico-anterior-2004-civ-0601` |
| CIV-0602 | Demanda de reducción o exoneración de renta de finca rústica (arrendamiento sujeto a la LAR 1980) | `demanda-reduccion-exoneracion-renta-finca-rustica-civ-0602` |
| CIV-0603 | Demanda de revisión de renta de finca rústica (arrendamiento sujeto a la LAR 1980) | `demanda-revision-renta-finca-rustica-arrendamiento-civ-0603` |
| CIV-0605 | Demanda de desahucio por impago en arrendamiento de uso distinto de vivienda posterior a 1995 | `demanda-desahucio-impago-arrendamiento-uso-distinto-civ-0605` |
| CIV-0606 | Demanda de resolución de alquiler de vivienda por necesidad del arrendador (anterior a 1985) | `demanda-resolucion-alquiler-vivienda-necesidad-civ-0606` |
| CIV-0607 | Demanda de resolución de arrendamiento de vivienda por obras no consentidas | `demanda-resolucion-arrendamiento-vivienda-obras-no-civ-0607` |
| CIV-2408 | Demanda de desahucio por impago de renta de vivienda en la que el arrendador condona la deuda | `demanda-desahucio-impago-renta-vivienda-arrendador-civ-2408` |
| CIV-2409 | Demanda para resolver el arrendamiento de vivienda por subrogación inter vivos no comunicada | `demanda-resolver-arrendamiento-vivienda-subrogacion-civ-2409` |
| CIV-2419 | Demanda verbal de desahucio por impago con reclamación de rentas y posibilidad de enervación | `demanda-verbal-desahucio-impago-reclamacion-rentas-civ-2419` |
| CIV-2420 | Demanda verbal de desahucio por impago cuando ya no cabe enervar la acción | `demanda-verbal-desahucio-impago-cuando-ya-no-cabe-civ-2420` |
| CIV-2421 | Demanda verbal de desahucio por vencimiento del plazo del arrendamiento | `demanda-verbal-desahucio-vencimiento-plazo-civ-2421` |
| CIV-2422 | Demanda ordinaria para fijar la renta y reclamar las diferencias adeudadas | `demanda-ordinaria-fijar-renta-reclamar-diferencias-civ-2422` |
| CIV-2423 | Demanda ordinaria para extinguir el derecho del arrendatario sobre una vivienda o local | `demanda-ordinaria-extinguir-derecho-arrendatario-sobre-civ-2423` |
| CIV-2425 | Demanda ordinaria de extinción del arrendamiento por pérdida de la finca | `demanda-ordinaria-extincion-arrendamiento-perdida-finca-civ-2425` |
| CIV-2426 | Demanda ordinaria de resolución del arriendo por oposición temeraria del inquilino a las subidas | `demanda-ordinaria-resolucion-arriendo-oposicion-civ-2426` |
| CIV-2427 | Demanda ordinaria para cobrar rentas adeudadas tras extinguirse el arrendamiento | `demanda-ordinaria-cobrar-rentas-adeudadas-tras-civ-2427` |
| CIV-2428 | Demanda ordinaria de extinción del arrendamiento por declaración firme de ruina | `demanda-ordinaria-extincion-arrendamiento-declaracion-civ-2428` |
| CIV-2430 | Demanda verbal de desahucio por precario contra quien ocupa la vivienda sin pagar renta | `demanda-verbal-desahucio-precario-contra-quien-ocupa-civ-2430` |
| CIV-2431 | Demanda ordinaria de resolución porque la vivienda no es la residencia permanente del inquilino | `demanda-ordinaria-resolucion-porque-vivienda-no-es-civ-2431` |
| CIV-2432 | Demanda ordinaria de desahucio tramitada por el cauce del juicio de retracto | `demanda-ordinaria-desahucio-tramitada-cauce-juicio-civ-2432` |
| CIV-2433 | Demanda ordinaria de resolución por cierre del local más de seis meses en un año | `demanda-ordinaria-resolucion-cierre-local-mas-seis-civ-2433` |
| CIV-2434 | Demanda ordinaria de resolución del arriendo de vivienda por denegar la prórroga por necesidad | `demanda-ordinaria-resolucion-arriendo-vivienda-denegar-civ-2434` |
| CIV-2435 | Demanda ordinaria de resolución por no cumplirse los requisitos de subrogación en la vivienda | `demanda-ordinaria-resolucion-no-cumplirse-requisitos-civ-2435` |
| CIV-2436 | Demanda ordinaria del inquilino que ejercita el retracto por la venta de su vivienda | `demanda-ordinaria-inquilino-ejercita-retracto-venta-civ-2436` |
| CIV-2437 | Demanda ordinaria de resolución por desocupación de la vivienda más de seis meses en un año | `demanda-ordinaria-resolucion-desocupacion-vivienda-mas-civ-2437` |
| CIV-2438 | Demanda ordinaria de resolución por no cumplirse los requisitos de subrogación en el local | `demanda-ordinaria-resolucion-no-cumplirse-requisitos-civ-2438` |
| CIV-2439 | Demanda de resolución por actividades molestas, insalubres, nocivas, peligrosas o ilícitas | `demanda-resolucion-actividades-molestas-insalubres-civ-2439` |
| CIV-2440 | Demanda ordinaria de resolución por obras que alteran la configuración de la vivienda arrendada | `demanda-ordinaria-resolucion-obras-alteran-civ-2440` |
| CIV-2441 | Demanda ordinaria de resolución por subarriendo o cesión no consentidos del local | `demanda-ordinaria-resolucion-subarriendo-cesion-no-civ-2441` |
| CIV-2442 | Demanda ordinaria de resolución del arriendo por daños causados dolosamente en la finca | `demanda-ordinaria-resolucion-arriendo-danos-causados-civ-2442` |
| CIV-2443 | Demanda ordinaria de resolución por subarriendo o cesión no consentidos de la vivienda | `demanda-ordinaria-resolucion-subarriendo-cesion-no-civ-2443` |

### Contestaciones, oposiciones y alegaciones (6)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0540 | Escrito de oposición del demandado a la demanda de desahucio por falta de pago | `escrito-oposicion-demandado-demanda-desahucio-falta-civ-0540` |
| CIV-0557 | Contestación a la demanda arrendaticia con reconvención para que el arrendador pague las obras | `contestacion-demanda-arrendaticia-reconvencion-civ-0557` |
| CIV-0597 | Contestación a demanda de resolución de alquiler de vivienda por necesidad (contrato previo a 1985) | `contestacion-demanda-resolucion-alquiler-vivienda-civ-0597` |
| CIV-0600 | Contestación a la demanda de resolución por subarriendo y falta de ocupación (vivienda, LAU 1994) | `contestacion-demanda-resolucion-subarriendo-falta-civ-0600` |
| CIV-2473 | Oposición del inquilino a la actualización de renta por los ingresos de la unidad familiar | `oposicion-inquilino-actualizacion-renta-ingresos-civ-2473` |
| CIV-2513 | Oposición del inquilino a las obras de mejora que pretende el arrendador | `oposicion-inquilino-obras-mejora-pretende-arrendador-civ-2513` |

### Contratos, pactos y cláusulas (43)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0495 | Contrato de arrendamiento de local de negocio, dentro o fuera de centro comercial | `contrato-arrendamiento-local-negocio-dentro-fuera-civ-0495` |
| CIV-0496 | Contrato de traspaso de local de negocio | `contrato-traspaso-local-negocio-civ-0496` |
| CIV-0497 | Acuerdo de resolución del contrato de arrendamiento de local de negocio | `acuerdo-resolucion-contrato-arrendamiento-local-negocio-civ-0497` |
| CIV-0498 | Contrato de alquiler de finca para la celebración de eventos | `contrato-alquiler-finca-celebracion-eventos-civ-0498` |
| CIV-0500 | Contrato de arrendamiento de local para uso distinto del de vivienda | `contrato-arrendamiento-local-uso-distinto-vivienda-civ-0500` |
| CIV-0501 | Contrato de alquiler de maquinaria | `contrato-alquiler-maquinaria-civ-0501` |
| CIV-0504 | Contrato de arrendamiento de local u otro inmueble para uso distinto del de vivienda | `contrato-arrendamiento-local-u-otro-inmueble-uso-civ-0504` |
| CIV-0505 | Contrato de arrendamiento de vivienda sin prórroga por necesidad del arrendador y con indemnización | `contrato-arrendamiento-vivienda-sin-prorroga-necesidad-civ-0505` |
| CIV-0506 | Contrato de arrendamiento de vivienda con avalista o cláusula de garantía del inquilino | `contrato-arrendamiento-vivienda-avalista-clausula-civ-0506` |
| CIV-0507 | Contrato de arrendamiento de vivienda que autoriza el subarriendo parcial | `contrato-arrendamiento-vivienda-autoriza-subarriendo-civ-0507` |
| CIV-0508 | Contrato de arrendamiento de vivienda del usufructuario con consentimiento del nudo propietario | `contrato-arrendamiento-vivienda-usufructuario-civ-0508` |
| CIV-0511 | Contrato privado de arrendamiento rústico según el Derecho civil catalán | `contrato-privado-arrendamiento-rustico-segun-derecho-civ-0511` |
| CIV-0512 | Cláusula de arrendamiento de vivienda que fija indemnización si el inquilino desiste del contrato | `clausula-arrendamiento-vivienda-fija-indemnizacion-si-civ-0512` |
| CIV-0513 | Contrato de arrendamiento de vivienda amueblada con inventario del mobiliario | `contrato-arrendamiento-vivienda-amueblada-inventario-civ-0513` |
| CIV-0514 | Contrato de arrendamiento con resolución por impago previo requerimiento en el domicilio registral | `contrato-arrendamiento-resolucion-impago-previo-civ-0514` |
| CIV-0515 | Contrato de arrendamiento para uso distinto de vivienda de una finca destinada a actividad docente | `contrato-arrendamiento-uso-distinto-vivienda-finca-civ-0515` |
| CIV-0519 | Contrato de arrendamiento de nave industrial con facultad de subarrendar | `contrato-arrendamiento-nave-industrial-facultad-civ-0519` |
| CIV-0528 | Cláusula que excluye la subrogación por fallecimiento del arrendatario en el alquiler de vivienda | `clausula-excluye-subrogacion-fallecimiento-civ-0528` |
| CIV-0531 | Contrato de arrendamiento de la vivienda del portero | `contrato-arrendamiento-vivienda-portero-civ-0531` |
| CIV-0536 | Contrato de arrendamiento de un corner en centro comercial con prohibición de cesión y subarriendo | `contrato-arrendamiento-corner-centro-comercial-civ-0536` |
| CIV-0538 | Contrato de arrendamiento de vivienda habitual | `contrato-arrendamiento-vivienda-habitual-civ-0538` |
| CIV-0544 | Contrato de cesión de un arrendamiento rústico | `contrato-cesion-arrendamiento-rustico-civ-0544` |
| CIV-0545 | Contrato de aparcería de finca rústica | `contrato-aparceria-finca-rustica-civ-0545` |
| CIV-0546 | Contrato de subarriendo de finca rústica | `contrato-subarriendo-finca-rustica-civ-0546` |
| CIV-0547 | Contrato de aparcería de tipo asociativo | `contrato-aparceria-tipo-asociativo-civ-0547` |
| CIV-0548 | Contrato de arrendamiento rústico ad meliorandum | `contrato-arrendamiento-rustico-ad-meliorandum-civ-0548` |
| CIV-0549 | Contrato de arrendamiento de una habitación | `contrato-arrendamiento-habitacion-civ-0549` |
| CIV-0550 | Contrato de cesión de un arrendamiento de vivienda urbana | `contrato-cesion-arrendamiento-vivienda-urbana-civ-0550` |
| CIV-0551 | Contrato por el que se subarrienda una vivienda | `contrato-subarrienda-vivienda-civ-0551` |
| CIV-0573 | Contrato de arrendamiento de plaza de garaje o aparcamiento subterráneo | `contrato-arrendamiento-plaza-garaje-aparcamiento-civ-0573` |
| CIV-0574 | Contrato de arrendamiento de finca rústica para uso agrícola | `contrato-arrendamiento-finca-rustica-uso-agricola-civ-0574` |
| CIV-0575 | Contrato de opción de compra a favor del inquilino sobre el inmueble arrendado | `contrato-opcion-compra-favor-inquilino-sobre-inmueble-civ-0575` |
| CIV-0583 | Contrato de cesión de arrendamiento para uso distinto de vivienda, con o sin existencias | `contrato-cesion-arrendamiento-uso-distinto-vivienda-civ-0583` |
| CIV-0588 | Contrato de arrendamiento de uso distinto de vivienda con pactos sobre cesión y subarriendo | `contrato-arrendamiento-uso-distinto-vivienda-pactos-civ-0588` |
| CIV-0589 | Contrato de arrendamiento de vivienda por temporada | `contrato-arrendamiento-vivienda-temporada-civ-0589` |
| CIV-0592 | Cláusulas de revisión y modificación de la renta en contratos de arrendamiento urbano | `clausulas-revision-modificacion-renta-contratos-civ-0592` |
| CIV-2405 | Contrato de transacción extrajudicial sobre un arrendamiento de vivienda | `contrato-transaccion-extrajudicial-sobre-arrendamiento-civ-2405` |
| CIV-2406 | Contrato de arrendamiento de cosa con duración anual prorrogable | `contrato-arrendamiento-cosa-duracion-anual-prorrogable-civ-2406` |
| CIV-2407 | Contrato de alquiler de plaza de garaje sujeto al Código Civil | `contrato-alquiler-plaza-garaje-sujeto-codigo-civil-civ-2407` |
| CIV-2416 | Contrato de arrendamiento de local para uso distinto de vivienda con opción de compra | `contrato-arrendamiento-local-uso-distinto-vivienda-civ-2416` |
| CIV-2466 | Contrato de subarriendo de un local de negocio | `contrato-subarriendo-local-negocio-civ-2466` |
| CIV-2469 | Contrato de traspaso de un local de negocio, con o sin existencias | `contrato-traspaso-local-negocio-sin-existencias-civ-2469` |
| CIV-2515 | Contrato de subarriendo parcial de vivienda con intervención del propietario | `contrato-subarriendo-parcial-vivienda-intervencion-civ-2515` |

### Comunicaciones, requerimientos y cartas (81)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0503 | Comunicación del arrendador de local de negocio de que no renovará el contrato al vencer el plazo | `comunicacion-arrendador-local-negocio-no-renovara-civ-0503` |
| CIV-0517 | Solicitud del demandado de abogado y procurador de oficio en un desahucio por impago | `solicitud-demandado-abogado-procurador-oficio-civ-0517` |
| CIV-0518 | Requerimiento de pago al avalista o fiador solidario de las rentas debidas, previo a reclamar | `requerimiento-pago-avalista-fiador-solidario-rentas-civ-0518` |
| CIV-0523 | Carta al inquilino comunicando el cambio de propietario de la vivienda alquilada | `carta-inquilino-comunicando-cambio-propietario-civ-0523` |
| CIV-0525 | Notificación del menor emancipado para poner fin al arrendamiento rústico concertado por sus padres | `notificacion-menor-emancipado-poner-fin-arrendamiento-civ-0525` |
| CIV-0526 | Carta del cónyuge o conviviente del arrendatario fallecido que renuncia a subrogarse | `carta-conyuge-conviviente-arrendatario-fallecido-civ-0526` |
| CIV-0527 | Carta de otros familiares del arrendatario fallecido que renuncian a subrogarse en el arrendamiento | `carta-otros-familiares-arrendatario-fallecido-civ-0527` |
| CIV-0529 | Carta que notifica la subrogación sucesoria en el arrendamiento rústico | `carta-notifica-subrogacion-sucesoria-arrendamiento-civ-0529` |
| CIV-0560 | Notificación del arrendador que da por terminado el arrendamiento y excluye la tácita reconducción | `notificacion-arrendador-da-terminado-arrendamiento-civ-0560` |
| CIV-0561 | Comunicación del arrendador al arrendatario de fin del contrato sin tácita reconducción | `comunicacion-arrendador-arrendatario-fin-contrato-sin-civ-0561` |
| CIV-0571 | Solicitud del demandado de terminar el proceso por enervación de la acción de desahucio | `solicitud-demandado-terminar-proceso-enervacion-accion-civ-0571` |
| CIV-0572 | Notificación del arrendatario de vivienda al arrendador de su desistimiento del contrato | `notificacion-arrendatario-vivienda-arrendador-civ-0572` |
| CIV-0584 | Notificación del arrendador de vivienda de que el contrato concluye al expirar el plazo | `notificacion-arrendador-vivienda-contrato-concluye-civ-0584` |
| CIV-0585 | Notificación del arrendatario de vivienda de que no renovará el contrato | `notificacion-arrendatario-vivienda-no-renovara-contrato-civ-0585` |
| CIV-0586 | Requerimiento notarial al inquilino para cesar actividades molestas, nocivas, peligrosas o ilícitas | `requerimiento-notarial-inquilino-cesar-actividades-civ-0586` |
| CIV-0590 | Reclamación del arrendatario al arrendador para que haga las reparaciones necesarias en la vivienda | `reclamacion-arrendatario-arrendador-haga-reparaciones-civ-0590` |
| CIV-0591 | Reclamación al inquilino de vivienda del pago de las rentas atrasadas | `reclamacion-inquilino-vivienda-pago-rentas-atrasadas-civ-0591` |
| CIV-0593 | Comunicación al inquilino de la actualización de la renta de finca urbana | `comunicacion-inquilino-actualizacion-renta-finca-urbana-civ-0593` |
| CIV-2410 | Aviso de subida de renta en uso no residencial por fusión, escisión o transformación del inquilino | `aviso-subida-renta-uso-no-residencial-fusion-escision-civ-2410` |
| CIV-2412 | Aviso del inquilino que resuelve el contrato por perturbaciones imputables al arrendador | `aviso-inquilino-resuelve-contrato-perturbaciones-civ-2412` |
| CIV-2413 | Aviso de la nueva cuantía de gastos de comunidad en arrendamiento de vivienda | `aviso-nueva-cuantia-gastos-comunidad-arrendamiento-civ-2413` |
| CIV-2414 | Comunicación del inquilino de que necesita obras en la vivienda por discapacidad o edad avanzada | `comunicacion-inquilino-necesita-obras-vivienda-civ-2414` |
| CIV-2415 | Aviso de denegación de la prórroga forzosa del arriendo por pérdida de la vivienda habitual | `aviso-denegacion-prorroga-forzosa-arriendo-perdida-civ-2415` |
| CIV-2417 | Comunicación del nuevo propietario al inquilino de las condiciones esenciales de la compra | `comunicacion-nuevo-propietario-inquilino-condiciones-civ-2417` |
| CIV-2418 | Comunicación del inquilino que ofrece ante notario el pago de las rentas debidas | `comunicacion-inquilino-ofrece-ante-notario-pago-rentas-civ-2418` |
| CIV-2424 | Aviso del arrendador de fin al vencer el plazo en contratos para uso distinto de vivienda | `aviso-arrendador-fin-vencer-plazo-contratos-uso-civ-2424` |
| CIV-2429 | Aviso del arrendador de fin al vencer el plazo en contratos posteriores al 9 de mayo de 1985 | `aviso-arrendador-fin-vencer-plazo-contratos-civ-2429` |
| CIV-2444 | Aviso de denegación de la prórroga forzosa del arriendo porque el hijo quiere vivir independiente | `aviso-denegacion-prorroga-forzosa-arriendo-porque-hijo-civ-2444` |
| CIV-2447 | Aviso de denegación de la prórroga por tener el inquilino vivienda libre en los seis meses previos | `aviso-denegacion-prorroga-tener-inquilino-vivienda-civ-2447` |
| CIV-2448 | Aviso de denegación de la prórroga forzosa del arriendo por derribo de la finca | `aviso-denegacion-prorroga-forzosa-arriendo-derribo-civ-2448` |
| CIV-2449 | Aviso de denegación de la prórroga por ocupar el inquilino dos o más viviendas en la misma población | `aviso-denegacion-prorroga-ocupar-inquilino-dos-mas-civ-2449` |
| CIV-2450 | Aviso de denegación de la prórroga por desocupación o cierre más de seis meses en un año | `aviso-denegacion-prorroga-desocupacion-cierre-mas-seis-civ-2450` |
| CIV-2451 | Aviso de denegación de la prórroga forzosa del arriendo por aumento de las necesidades familiares | `aviso-denegacion-prorroga-forzosa-arriendo-aumento-civ-2451` |
| CIV-2452 | Aviso del cesionario al arrendador poniendo a su disposición la participación en el traspaso | `aviso-cesionario-arrendador-poniendo-disposicion-civ-2452` |
| CIV-2453 | Aviso de denegación de la prórroga forzosa del arriendo por necesidad inexcusable de traslado | `aviso-denegacion-prorroga-forzosa-arriendo-necesidad-civ-2453` |
| CIV-2454 | Aviso del arrendador que ejercita el derecho de tanteo en el traspaso del local | `aviso-arrendador-ejercita-derecho-tanteo-traspaso-local-civ-2454` |
| CIV-2455 | Aviso al arrendador de la intención de traspasar el local de negocio con existencias | `aviso-arrendador-intencion-traspasar-local-negocio-civ-2455` |
| CIV-2456 | Aviso de denegación de la prórroga forzosa del arriendo por matrimonio del hijo del arrendador | `aviso-denegacion-prorroga-forzosa-arriendo-matrimonio-civ-2456` |
| CIV-2457 | Aviso del inquilino al arrendador de que se ha hecho el traspaso y de sus condiciones | `aviso-inquilino-arrendador-ha-hecho-traspaso-civ-2457` |
| CIV-2458 | Comunicación del nuevo propietario al inquilino de las condiciones de la compra según la LAU de 1964 | `comunicacion-nuevo-propietario-inquilino-condiciones-civ-2458` |
| CIV-2461 | Comunicación del inquilino de local que elige la duración del apartado 8 de la DT tercera LAU | `comunicacion-inquilino-local-elige-duracion-apartado-8-civ-2461` |
| CIV-2462 | Aviso de actualización en años sucesivos de renta y conceptos del apartado 10 de la DT segunda | `aviso-actualizacion-anos-sucesivos-renta-conceptos-civ-2462` |
| CIV-2463 | Aviso de actualización de la renta del local de negocio en las anualidades sucesivas | `aviso-actualizacion-renta-local-negocio-anualidades-civ-2463` |
| CIV-2464 | Aviso de actualización de renta del local y conceptos del apartado 10 de la DT segunda LAU | `aviso-actualizacion-renta-local-conceptos-apartado-10-civ-2464` |
| CIV-2465 | Aviso al arrendador de la intención de traspasar el local sin existencias, art. 32 LAU 1964 | `aviso-arrendador-intencion-traspasar-local-sin-civ-2465` |
| CIV-2467 | Aviso al arrendador de la fusión, escisión o transformación de la sociedad inquilina, sin traspaso | `aviso-arrendador-fusion-escision-transformacion-civ-2467` |
| CIV-2470 | Aviso del inquilino que opta por firmar un nuevo contrato de arrendamiento del local de negocio | `aviso-inquilino-opta-firmar-nuevo-contrato-civ-2470` |
| CIV-2471 | Aviso del arrendador que entrega al inquilino copia del nuevo contrato de arrendamiento del local | `aviso-arrendador-entrega-inquilino-copia-nuevo-civ-2471` |
| CIV-2472 | Aviso del arrendador al inquilino de su voluntad de firmar un nuevo contrato del local de negocio | `aviso-arrendador-inquilino-voluntad-firmar-nuevo-civ-2472` |
| CIV-2474 | Aviso de subida de renta por traspaso del local de negocio | `aviso-subida-renta-traspaso-local-negocio-civ-2474` |
| CIV-2475 | Comunicación del inquilino que se acoge al sistema de no actualización de la renta | `comunicacion-inquilino-acoge-sistema-no-actualizacion-civ-2475` |
| CIV-2476 | Aviso de subida de renta por fusión, escisión o transformación de la sociedad arrendataria | `aviso-subida-renta-fusion-escision-transformacion-civ-2476` |
| CIV-2477 | Aviso del arrendador de actualización de renta en las anualidades sucesivas del periodo transitorio | `aviso-arrendador-actualizacion-renta-anualidades-civ-2477` |
| CIV-2478 | Aviso al inquilino de la repercusión en la renta del coste de servicios y suministros | `aviso-inquilino-repercusion-renta-coste-servicios-civ-2478` |
| CIV-2479 | Aviso de actualización de renta de vivienda y conceptos autorizados en las anualidades sucesivas | `aviso-actualizacion-renta-vivienda-conceptos-civ-2479` |
| CIV-2480 | Aviso al arrendador de la muerte del inquilino del local y de la subrogación del cónyuge o familiar | `aviso-arrendador-muerte-inquilino-local-subrogacion-civ-2480` |
| CIV-2481 | Aviso al arrendador de la muerte del inquilino subrogado y de la segunda subrogación de un familiar | `aviso-arrendador-muerte-inquilino-subrogado-segunda-civ-2481` |
| CIV-2483 | Aviso al inquilino de la repercusión de obras de reparación para recuperar la inversión | `aviso-inquilino-repercusion-obras-reparacion-recuperar-civ-2483` |
| CIV-2484 | Aviso al arrendador de la muerte del inquilino de vivienda y subrogación del cónyuge o familiar | `aviso-arrendador-muerte-inquilino-vivienda-subrogacion-civ-2484` |
| CIV-2485 | Aviso de muerte del subrogado y segunda subrogación si la primera fue desde el 1 de enero de 1995 | `aviso-muerte-subrogado-segunda-subrogacion-si-primera-civ-2485` |
| CIV-2486 | Aviso del heredero de la muerte del inquilino y su subrogación en arriendo de uso no residencial | `aviso-heredero-muerte-inquilino-subrogacion-arriendo-civ-2486` |
| CIV-2487 | Aviso al inquilino de obras de mejora en un arriendo de uso distinto de vivienda | `aviso-inquilino-obras-mejora-arriendo-uso-distinto-civ-2487` |
| CIV-2488 | Aviso de subida de renta por la cláusula de actualización en arriendo de uso distinto de vivienda | `aviso-subida-renta-clausula-actualizacion-arriendo-uso-civ-2488` |
| CIV-2489 | Aviso al arrendador de la cesión del contrato de arrendamiento para uso distinto de vivienda | `aviso-arrendador-cesion-contrato-arrendamiento-uso-civ-2489` |
| CIV-2490 | Aviso de subida de renta por obras de mejora en arriendo de uso distinto de vivienda | `aviso-subida-renta-obras-mejora-arriendo-uso-distinto-civ-2490` |
| CIV-2492 | Aviso de la nueva cuantía de gastos de comunidad en arrendamiento para uso distinto de vivienda | `aviso-nueva-cuantia-gastos-comunidad-arrendamiento-uso-civ-2492` |
| CIV-2493 | Aviso del inquilino de que quiere renovar el arriendo de uso distinto de vivienda | `aviso-inquilino-quiere-renovar-arriendo-uso-distinto-civ-2493` |
| CIV-2495 | Aviso del arrendador de fin del contrato al vencer el plazo pactado, LAU 1994 | `aviso-arrendador-fin-contrato-vencer-plazo-pactado-lau-civ-2495` |
| CIV-2496 | Aviso del inquilino que resuelve el contrato porque el arrendador no hace obras de conservación | `aviso-inquilino-resuelve-contrato-porque-arrendador-no-civ-2496` |
| CIV-2497 | Aviso del arrendador al inquilino de que va a realizar obras de mejora | `aviso-arrendador-inquilino-va-realizar-obras-mejora-civ-2497` |
| CIV-2498 | Aviso del arrendador al cónyuge o pareja del inquilino que ha desistido del contrato | `aviso-arrendador-conyuge-pareja-inquilino-ha-desistido-civ-2498` |
| CIV-2499 | Aviso del inquilino que desiste del contrato por obras que hacen inhabitable la vivienda | `aviso-inquilino-desiste-contrato-obras-hacen-civ-2499` |
| CIV-2501 | Aviso de subida de renta por instalar o adaptar infraestructuras comunes de telecomunicaciones | `aviso-subida-renta-instalar-adaptar-infraestructuras-civ-2501` |
| CIV-2502 | Aviso al inquilino de vivienda de la subida de renta por obras de mejora | `aviso-inquilino-vivienda-subida-renta-obras-mejora-civ-2502` |
| CIV-2503 | Aviso al inquilino de que se instalarán infraestructuras comunes de telecomunicaciones | `aviso-inquilino-instalaran-infraestructuras-comunes-civ-2503` |
| CIV-2504 | Aviso al arrendador de que se subrogan descendientes, ascendientes o hermanos del fallecido | `aviso-arrendador-subrogan-descendientes-ascendientes-civ-2504` |
| CIV-2507 | Aviso al inquilino de vivienda de la subida de renta por la cláusula de actualización | `aviso-inquilino-vivienda-subida-renta-clausula-civ-2507` |
| CIV-2508 | Aviso al arrendador de la subrogación del conviviente con ayuda mutua del inquilino fallecido | `aviso-arrendador-subrogacion-conviviente-ayuda-mutua-civ-2508` |
| CIV-2509 | Aviso al arrendador de la subrogación de la pareja more uxorio del inquilino fallecido | `aviso-arrendador-subrogacion-pareja-more-uxorio-civ-2509` |
| CIV-2510 | Aviso del cónyuge o pareja del inquilino de que este ha abandonado la vivienda sin desistir | `aviso-conyuge-pareja-inquilino-este-ha-abandonado-civ-2510` |
| CIV-2511 | Comunicación del inquilino de que necesita obras no estructurales en la finca por discapacidad | `comunicacion-inquilino-necesita-obras-no-estructurales-civ-2511` |

### Escritos de trámite y otros (23)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0499 | Alquiler de instalaciones deportivas (contrato) | `alquiler-instalaciones-deportivas-contrato-civ-0499` |
| CIV-0516 | Escrito del demandado oponiéndose al desahucio por enervación de la acción | `escrito-demandado-oponiendose-desahucio-enervacion-civ-0516` |
| CIV-0532 | Novación del contrato de arrendamiento de vivienda para reducir la renta | `novacion-contrato-arrendamiento-vivienda-reducir-renta-civ-0532` |
| CIV-0533 | Promesa de arrendar un local de negocio (precontrato) | `promesa-arrendar-local-negocio-precontrato-civ-0533` |
| CIV-0537 | Compromiso de abandonar una vivienda | `compromiso-abandonar-vivienda-civ-0537` |
| CIV-0539 | Escrito del arrendador que se opone a la enervación de la acción de desahucio | `escrito-arrendador-opone-enervacion-accion-desahucio-civ-0539` |
| CIV-0543 | Otrosí de demanda de desahucio que pide la ejecución directa de la sentencia | `otrosi-demanda-desahucio-pide-ejecucion-directa-civ-0543` |
| CIV-0553 | Escrito del demandado que enerva la acción de desahucio por falta de pago | `escrito-demandado-enerva-accion-desahucio-falta-pago-civ-0553` |
| CIV-0555 | Allanamiento del demandado al compromiso ofrecido por el actor en desahucio por falta de pago | `allanamiento-demandado-compromiso-ofrecido-actor-civ-0555` |
| CIV-0570 | Petición oral en la vista de sentencia que declare no haber lugar al desahucio por falta de objeto | `peticion-oral-vista-sentencia-declare-no-haber-lugar-civ-0570` |
| CIV-0576 | Escrito de la viuda del arrendatario subrogándose en el arrendamiento por su fallecimiento | `escrito-viuda-arrendatario-subrogandose-arrendamiento-civ-0576` |
| CIV-0587 | Escrito de entrega de llaves de la vivienda arrendada y devolución de la fianza | `escrito-entrega-llaves-vivienda-arrendada-devolucion-civ-0587` |
| CIV-0604 | Escrito de allanamiento del arrendatario de un local con compromiso de desalojo voluntario | `escrito-allanamiento-arrendatario-local-compromiso-civ-0604` |
| CIV-2459 | Respuesta del inquilino que quiere ejercer el tanteo y comprar la vivienda o local | `respuesta-inquilino-quiere-ejercer-tanteo-comprar-civ-2459` |
| CIV-2468 | Consentimiento del arrendador para que el inquilino subarriende la vivienda | `consentimiento-arrendador-inquilino-subarriende-civ-2468` |
| CIV-2482 | Respuesta del inquilino que rechaza la subida de renta por el tenor de la cláusula invocada | `respuesta-inquilino-rechaza-subida-renta-tenor-civ-2482` |
| CIV-2491 | Rechazo del inquilino a la subida de renta por falta de datos, arriendo de uso distinto de vivienda | `rechazo-inquilino-subida-renta-falta-datos-arriendo-civ-2491` |
| CIV-2494 | Documento de resolución del arrendamiento por mutuo acuerdo de arrendador e inquilino | `documento-resolucion-arrendamiento-mutuo-acuerdo-civ-2494` |
| CIV-2500 | Rechazo del inquilino a la subida de renta notificada por no aportarle los datos necesarios | `rechazo-inquilino-subida-renta-notificada-no-aportarle-civ-2500` |
| CIV-2505 | Respuesta del arrendador que deniega al inquilino el permiso para subarrendar | `respuesta-arrendador-deniega-inquilino-permiso-civ-2505` |
| CIV-2506 | Petición del inquilino al arrendador de permiso para subarrendar parte de la vivienda | `peticion-inquilino-arrendador-permiso-subarrendar-civ-2506` |
| CIV-2512 | Petición de los inquilinos para instalar infraestructuras comunes de telecomunicaciones | `peticion-inquilinos-instalar-infraestructuras-comunes-civ-2512` |
| CIV-2514 | Petición del inquilino al arrendador de permiso para obras del artículo 23 LAU 1994 | `peticion-inquilino-arrendador-permiso-obras-articulo-civ-2514` |
