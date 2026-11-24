---
name: indice
description: "Índice de los 94 formularios de Herencias, testamentos y donaciones. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre."
---

# Herencias, testamentos y donaciones: índice de formularios

> Plugin `formularios-herencias-y-donaciones` · 94 formularios · normativa revisada el 24-11-2026.

## Qué es

Para las sucesiones: testamentos (también forales), aceptación y renuncia de la herencia, declaración de herederos, partición y división judicial, legítimas, colación, desheredación, albaceas y contadores-partidores, y donaciones.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Testamento abierto con legado de usufructo al cónyuge»
- «Solicitud de división judicial de la herencia»
- «Escritura de aceptación y partición de herencia»

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

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-herencias-y-donaciones:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado, con su `formulario.md` y su `marco.md`.

### Demandas, peticiones y solicitudes iniciales (18)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0401 | Solicitud de división judicial de herencia y liquidación de la sociedad de gananciales | `solicitud-division-judicial-herencia-liquidacion-civ-0401` |
| CIV-0409 | Demanda para completar o adicionar la partición de la herencia | `demanda-completar-adicionar-particion-herencia-civ-0409` |
| CIV-0436 | Demanda de nulidad de testamento por incapacidad del testador y falta de formalidades | `demanda-nulidad-testamento-incapacidad-testador-falta-civ-0436` |
| CIV-0440 | Demanda de nulidad de testamento por falta de capacidad del testador (Derecho civil catalán) | `demanda-nulidad-testamento-falta-capacidad-testador-civ-0440` |
| CIV-0445 | Demanda de nulidad de la institución de heredero por preterición no intencional | `demanda-nulidad-institucion-heredero-pretericion-no-civ-0445` |
| CIV-0466 | Demanda de reclamación de un legado específico de cosa propia del testador | `demanda-reclamacion-legado-especifico-cosa-propia-civ-0466` |
| CIV-0467 | Demanda sucesoria con conflicto de aplicación de derechos civiles forales o especiales | `demanda-sucesoria-conflicto-aplicacion-derechos-civ-0467` |
| CIV-0473 | Demanda de juicio ordinario de petición de herencia | `demanda-juicio-ordinario-peticion-herencia-civ-0473` |
| CIV-0476 | Demanda de juicio ordinario que impugna la desheredación en el testamento | `demanda-juicio-ordinario-impugna-desheredacion-civ-0476` |
| CIV-0477 | Demanda ordinaria de rescisión de partición hereditaria por lesión en la valoración de bienes | `demanda-ordinaria-rescision-particion-hereditaria-civ-0477` |
| CIV-0478 | Demanda de juicio ordinario de reducción de la cuota hereditaria por donación inoficiosa | `demanda-juicio-ordinario-reduccion-cuota-hereditaria-civ-0478` |
| CIV-0479 | Demanda de juicio ordinario de complemento de legítima según el Derecho civil de Cataluña | `demanda-juicio-ordinario-complemento-legitima-segun-civ-0479` |
| CIV-0480 | Demanda de juicio ordinario de nulidad del acta notarial de notoriedad de declaración de herederos | `demanda-juicio-ordinario-nulidad-acta-notarial-civ-0480` |
| CIV-0481 | Demanda de juicio ordinario que impugna la partición por no incluir bienes en el inventario | `demanda-juicio-ordinario-impugna-particion-no-incluir-civ-0481` |
| CIV-0482 | Demanda de juicio ordinario de reclamación de legítima por nulidad de la desheredación | `demanda-juicio-ordinario-reclamacion-legitima-nulidad-civ-0482` |
| CIV-0483 | Demanda de juicio ordinario de reclamación de legítima en derecho común por preterición intencional | `demanda-juicio-ordinario-reclamacion-legitima-derecho-civ-0483` |
| CIV-0491 | Demanda para que los hijos obtengan la posesión de los bienes de la herencia | `demanda-hijos-obtengan-posesion-bienes-herencia-civ-0491` |
| CIV-0494 | Demanda de reserva del cónyuge binubo y de simulación en la transmisión de un inmueble reservable | `demanda-reserva-conyuge-binubo-simulacion-transmision-civ-0494` |

### Contestaciones, oposiciones y alegaciones (2)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0490 | Escrito de oposición a las operaciones particionales del contador | `escrito-oposicion-operaciones-particionales-contador-civ-0490` |
| CIV-0493 | Contestación a la demanda de juicio ordinario sobre nulidad de testamento | `contestacion-demanda-juicio-ordinario-sobre-nulidad-civ-0493` |

### Contratos, pactos y cláusulas (4)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0418 | Cláusula testamentaria de legado de pensión de alimentos | `clausula-testamentaria-legado-pension-alimentos-civ-0418` |
| CIV-0419 | Cláusula testamentaria de legado de uso o habitación a un legitimario con discapacidad (art. 822 CC) | `clausula-testamentaria-legado-uso-habitacion-civ-0419` |
| CIV-0455 | Contrato por el que se ceden derechos hereditarios | `contrato-ceden-derechos-hereditarios-civ-0455` |
| CIV-0487 | Contrato de compromiso de venta de un tercio indiviso de una herencia | `contrato-compromiso-venta-tercio-indiviso-herencia-civ-0487` |

### Estatutos, actas, certificaciones y escrituras (45)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0402 | Testamento con usufructo poderoso según el Derecho civil vasco | `testamento-usufructo-poderoso-segun-derecho-civil-vasco-civ-0402` |
| CIV-0403 | Testamento con poder testatorio según el Derecho civil vasco | `testamento-poder-testatorio-segun-derecho-civil-vasco-civ-0403` |
| CIV-0404 | Testamento otorgado por el comisario según el Derecho civil vasco | `testamento-otorgado-comisario-segun-derecho-civil-vasco-civ-0404` |
| CIV-0405 | Testamento hil buruko según el Derecho civil vasco | `testamento-hil-buruko-segun-derecho-civil-vasco-civ-0405` |
| CIV-0406 | Escritura de adjudicación de la herencia de confianza según el Derecho civil catalán | `escritura-adjudicacion-herencia-confianza-segun-civ-0406` |
| CIV-0407 | Escritura de fiducia colectiva según el Derecho civil aragonés | `escritura-fiducia-colectiva-segun-derecho-civil-civ-0407` |
| CIV-0408 | Escritura de fiducia sucesoria otorgada por un cónyuge según el Derecho civil aragonés | `escritura-fiducia-sucesoria-otorgada-conyuge-segun-civ-0408` |
| CIV-0414 | Escritura de poder especial entre cónyuges para otorgar la partición de herencia | `escritura-poder-especial-entre-conyuges-otorgar-civ-0414` |
| CIV-0417 | Testamento con legado para la educación de un beneficiario | `testamento-legado-educacion-beneficiario-civ-0417` |
| CIV-0420 | Testamento que delega en otro la facultad de mejorar | `testamento-delega-otro-facultad-mejorar-civ-0420` |
| CIV-0421 | Testamento que autoriza al tutor a hacer suyos los frutos de los bienes del tutelado | `testamento-autoriza-tutor-hacer-suyos-frutos-bienes-civ-0421` |
| CIV-0422 | Testamento que excluye a una persona del cargo de tutor | `testamento-excluye-persona-cargo-tutor-civ-0422` |
| CIV-0424 | Testamento con reconocimiento de hijo extramatrimonial | `testamento-reconocimiento-hijo-extramatrimonial-civ-0424` |
| CIV-0425 | Testamento con sustitución fideicomisaria a favor de un hijo o descendiente incapacitado | `testamento-sustitucion-fideicomisaria-favor-hijo-civ-0425` |
| CIV-0426 | Testamento abierto según el Derecho civil navarro | `testamento-abierto-segun-derecho-civil-navarro-civ-0426` |
| CIV-0427 | Acta de depósito de testamento según el Derecho navarro | `acta-deposito-testamento-segun-derecho-navarro-civ-0427` |
| CIV-0428 | Acta de notificación del pago de la legítima en metálico según el Derecho gallego | `acta-notificacion-pago-legitima-metalico-segun-derecho-civ-0428` |
| CIV-0429 | Testamento mancomunado según el Derecho civil gallego | `testamento-mancomunado-segun-derecho-civil-gallego-civ-0429` |
| CIV-0430 | Testamento por comisario según el Derecho civil gallego | `testamento-comisario-segun-derecho-civil-gallego-civ-0430` |
| CIV-0432 | Testamento con mejora de labrar y poseer según el Derecho gallego | `testamento-mejora-labrar-poseer-segun-derecho-gallego-civ-0432` |
| CIV-0433 | Testamento en ejercicio del poder testatorio según el Derecho gallego | `testamento-ejercicio-poder-testatorio-segun-derecho-civ-0433` |
| CIV-0434 | Acta de depósito de pacto de hermandad según el Derecho navarro | `acta-deposito-pacto-hermandad-segun-derecho-navarro-civ-0434` |
| CIV-0435 | Testamento con heredero de confianza según el Derecho navarro | `testamento-heredero-confianza-segun-derecho-navarro-civ-0435` |
| CIV-0438 | Acta de protocolización de testamento cerrado según el Derecho catalán | `acta-protocolizacion-testamento-cerrado-segun-derecho-civ-0438` |
| CIV-0439 | Testamento abierto con fiducia a favor del cónyuge según el Derecho catalán | `testamento-abierto-fiducia-favor-conyuge-segun-derecho-civ-0439` |
| CIV-0441 | Escritura de heredamiento simple según el Derecho catalán | `escritura-heredamiento-simple-segun-derecho-catalan-civ-0441` |
| CIV-0442 | Acta de protocolización instada por el párroco según el Derecho catalán | `acta-protocolizacion-instada-parroco-segun-derecho-civ-0442` |
| CIV-0443 | Capítulos matrimoniales con heredamiento cumulativo según el Derecho catalán | `capitulos-matrimoniales-heredamiento-cumulativo-segun-civ-0443` |
| CIV-0446 | Testamento mancomunado abierto según el Derecho aragonés | `testamento-mancomunado-abierto-segun-derecho-aragones-civ-0446` |
| CIV-0447 | Escritura de institución de heredero a favor de un tercero según el Derecho aragonés | `escritura-institucion-heredero-favor-tercero-segun-civ-0447` |
| CIV-0448 | Escritura de institución recíproca de heredero según el Derecho aragonés | `escritura-institucion-reciproca-heredero-segun-derecho-civ-0448` |
| CIV-0449 | Escritura de revocación de pacto sucesorio según el Derecho aragonés | `escritura-revocacion-pacto-sucesorio-segun-derecho-civ-0449` |
| CIV-0450 | Escritura de institución de heredero de presente según el Derecho aragonés | `escritura-institucion-heredero-presente-segun-derecho-civ-0450` |
| CIV-0452 | Testamento abierto otorgado por quien no tiene legitimarios | `testamento-abierto-otorgado-quien-no-tiene-legitimarios-civ-0452` |
| CIV-0453 | Testamento abierto con usufructo universal y cláusula de sustitución | `testamento-abierto-usufructo-universal-clausula-civ-0453` |
| CIV-0454 | Escritura de poder a un abogado para aceptar una herencia | `escritura-poder-abogado-aceptar-herencia-civ-0454` |
| CIV-0456 | Acta notarial de notoriedad para declarar herederos abintestato | `acta-notarial-notoriedad-declarar-herederos-abintestato-civ-0456` |
| CIV-0457 | Escritura de poder especial para actuaciones sucesorias | `escritura-poder-especial-actuaciones-sucesorias-civ-0457` |
| CIV-0459 | Escritura de renuncia a la herencia por legitimario preterido | `escritura-renuncia-herencia-legitimario-preterido-civ-0459` |
| CIV-0461 | Escritura de entrega del legado al legatario | `escritura-entrega-legado-legatario-civ-0461` |
| CIV-0462 | Testamento con legado, usufructo universal y contador partidor | `testamento-legado-usufructo-universal-contador-partidor-civ-0462` |
| CIV-0463 | Testamento con cláusula de desheredación | `testamento-clausula-desheredacion-civ-0463` |
| CIV-0465 | Testamento abierto con usufructo universal según el Derecho de Baleares | `testamento-abierto-usufructo-universal-segun-derecho-civ-0465` |
| CIV-0472 | Escritura de poder para aceptar herencias | `escritura-poder-aceptar-herencias-civ-0472` |
| CIV-0488 | Acta de comparecencia del contador y de las partes (art. 787.3 LEC) | `acta-comparecencia-contador-partes-art-787-3-lec-civ-0488` |

### Comunicaciones, requerimientos y cartas (7)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0423 | Solicitud al notario de testamento abierto de una persona judicialmente incapacitada | `solicitud-notario-testamento-abierto-persona-civ-0423` |
| CIV-0437 | Solicitud notarial de requerimiento para aceptar o repudiar la herencia (Derecho civil catalán) | `solicitud-notarial-requerimiento-aceptar-repudiar-civ-0437` |
| CIV-0468 | Solicitud notarial de adveración, apertura y protocolización de testamento cerrado | `solicitud-notarial-adveracion-apertura-protocolizacion-civ-0468` |
| CIV-0469 | Solicitud notarial de adveración y protocolización de testamento ológrafo | `solicitud-notarial-adveracion-protocolizacion-civ-0469` |
| CIV-0470 | Requerimiento inicial ante notario para la declaración de herederos abintestato | `requerimiento-inicial-ante-notario-declaracion-civ-0470` |
| CIV-0471 | Requerimiento notarial para que el heredero acepte o repudie la herencia (interrogatio in iure) | `requerimiento-notarial-heredero-acepte-repudie-civ-0471` |
| CIV-0475 | Solicitud de hacer definitiva la posesión interina de bienes hereditarios sin reclamación en 40 días | `solicitud-hacer-definitiva-posesion-interina-bienes-civ-0475` |

### Escritos de trámite y otros (18)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0410 | Escrito a la notaría del heredero que delibera sin tener los bienes de la herencia | `escrito-notaria-heredero-delibera-sin-tener-bienes-civ-0410` |
| CIV-0411 | Escrito a la notaría aceptando a beneficio de inventario con los bienes en poder del heredero | `escrito-notaria-aceptando-beneficio-inventario-bienes-civ-0411` |
| CIV-0412 | Escrito a la notaría del heredero que delibera teniendo los bienes de la herencia | `escrito-notaria-heredero-delibera-teniendo-bienes-civ-0412` |
| CIV-0413 | Escrito al tribunal aceptando la herencia a beneficio de inventario sin tener los bienes el heredero | `escrito-tribunal-aceptando-herencia-beneficio-civ-0413` |
| CIV-0415 | Manifestación de herencia testada por el hijo del causante como heredero único | `manifestacion-herencia-testada-hijo-causante-como-civ-0415` |
| CIV-0416 | Manifestación de herencia intestada por el cónyuge como heredero único | `manifestacion-herencia-intestada-conyuge-como-heredero-civ-0416` |
| CIV-0431 | Renuncia al usufructo de fidelidad según el Derecho navarro | `renuncia-usufructo-fidelidad-segun-derecho-navarro-civ-0431` |
| CIV-0444 | Codicilo según el Derecho civil de Baleares (Mallorca y Menorca) | `codicilo-segun-derecho-civil-baleares-mallorca-menorca-civ-0444` |
| CIV-0451 | Sucesión paccionada con institución de heredero para después de los días según el Derecho aragonés | `sucesion-paccionada-institucion-heredero-despues-dias-civ-0451` |
| CIV-0458 | Cuaderno particional de herencia testada con viuda e hijos y liquidación de gananciales | `cuaderno-particional-herencia-testada-viuda-e-hijos-civ-0458` |
| CIV-0460 | Compromiso de venta de bienes de la herencia | `compromiso-venta-bienes-herencia-civ-0460` |
| CIV-0464 | Cuaderno particional de herencia testada con viuda e hijos, gananciales y conmutación de usufructo | `cuaderno-particional-herencia-testada-viuda-e-hijos-civ-0464` |
| CIV-0474 | Otrosí de demanda de división de herencia sobre intervención del Fiscal hasta nombrar defensor | `otrosi-demanda-division-herencia-sobre-intervencion-civ-0474` |
| CIV-0484 | Escrito de los contadores que devuelve los autos y presenta el cuaderno particional | `escrito-contadores-devuelve-autos-presenta-cuaderno-civ-0484` |
| CIV-0485 | Cuaderno particional presentado por el contador | `cuaderno-particional-presentado-contador-civ-0485` |
| CIV-0486 | Cuenta final complementaria del administrador de la herencia | `cuenta-final-complementaria-administrador-herencia-civ-0486` |
| CIV-0489 | Cuenta final justificada del administrador de la herencia | `cuenta-final-justificada-administrador-herencia-civ-0489` |
| CIV-0492 | Escrito pidiendo alzar la suspensión del juicio divisorio por prejudicialidad penal | `escrito-pidiendo-alzar-suspension-juicio-divisorio-civ-0492` |
