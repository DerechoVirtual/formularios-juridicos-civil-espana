---
name: indice
description: "Índice de los 114 formularios de Alquileres y desahucios. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Alquileres y desahucios: índice de formularios

> Plugin `formularios-alquileres-y-desahucios` · 114 formularios · normativa revisada el 24-11-2026.

## Qué es

Para los arrendamientos urbanos y rústicos: contratos de vivienda y de local, cesión y subarriendo, actualización de renta, obras, fianza, requerimientos y burofaxes, desahucio por impago, por expiración del plazo y por precario, y reclamación de rentas.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Contrato de alquiler de vivienda habitual conforme a la LAU»
- «Demanda de desahucio por falta de pago y reclamación de rentas»
- «Requerimiento de pago al inquilino antes del desahucio»

---

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

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado, con su `formulario.md` y su `marco.md`.

### Demandas, peticiones y solicitudes iniciales (43)

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
| CIV-0578 | Demanda de juicio verbal de desahucio de finca urbana por vencimiento del plazo del contrato | `demanda-juicio-verbal-desahucio-finca-urbana-civ-0578` |
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
| CIV-0608 | Demanda de recuperación de finca rústica adquirida por el arrendatario histórico (LAR 1980) | `demanda-recuperacion-finca-rustica-adquirida-civ-0608` |

### Contestaciones, oposiciones y alegaciones (4)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0540 | Escrito de oposición del demandado a la demanda de desahucio por falta de pago | `escrito-oposicion-demandado-demanda-desahucio-falta-civ-0540` |
| CIV-0557 | Contestación a la demanda arrendaticia con reconvención para que el arrendador pague las obras | `contestacion-demanda-arrendaticia-reconvencion-civ-0557` |
| CIV-0597 | Contestación a demanda de resolución de alquiler de vivienda por necesidad (contrato previo a 1985) | `contestacion-demanda-resolucion-alquiler-vivienda-civ-0597` |
| CIV-0600 | Contestación a la demanda de resolución por subarriendo y falta de ocupación (vivienda, LAU 1994) | `contestacion-demanda-resolucion-subarriendo-falta-civ-0600` |

### Contratos, pactos y cláusulas (36)

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

### Comunicaciones, requerimientos y cartas (18)

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

### Escritos de trámite y otros (13)

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
