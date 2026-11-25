# Herencias, testamentos y donaciones

> Plugin de Claude Code `formularios-herencias-y-donaciones` · **163 formularios** · Civil · normativa revisada el 25-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Para las sucesiones: testamentos (también forales), aceptación y renuncia de la herencia, declaración de herederos, partición y división judicial, legítimas, colación, desheredación, albaceas y contadores-partidores, y donaciones.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva; el formulario seco, listo para rellenar, está en `assets/formulario.md` dentro de la carpeta de la skill.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 163 está al final):

- **Demandas, peticiones y solicitudes iniciales** (26). Por ejemplo: Solicitud de división judicial de herencia y liquidación de la sociedad de gananciales; Demanda para completar o adicionar la partición de la herencia; Demanda de nulidad de testamento por incapacidad del testador y falta de formalidades.
- **Contestaciones, oposiciones y alegaciones** (11). Por ejemplo: Escrito de oposición a las operaciones particionales del contador; Oposición del acreedor de la herencia al reparto mientras no se pague o garantice su crédito; Contestación a la demanda de nulidad de la institución de heredero por desheredación injusta.
- **Recursos** (1). Por ejemplo: Recurso de reposición contra la admisión de la partición pedida por un legatario de parte alícuota.
- **Contratos, pactos y cláusulas** (5). Por ejemplo: Cláusula testamentaria de legado de pensión de alimentos; Contrato por el que se ceden derechos hereditarios; Contrato de compromiso de venta de un tercio indiviso de una herencia.
- **Estatutos, actas, certificaciones y escrituras** (61). Por ejemplo: Testamento con usufructo poderoso según el Derecho civil vasco; Testamento con poder testatorio según el Derecho civil vasco; Testamento otorgado por el comisario según el Derecho civil vasco.
- **Comunicaciones, requerimientos y cartas** (8). Por ejemplo: Solicitud al notario de testamento abierto de una persona judicialmente incapacitada; Solicitud notarial de requerimiento para aceptar o repudiar la herencia (Derecho civil catalán); Solicitud notarial de adveración, apertura y protocolización de testamento cerrado.
- **Escritos de trámite y otros** (51). Por ejemplo: Escrito a la notaría del heredero que delibera sin tener los bienes de la herencia; Escrito a la notaría aceptando a beneficio de inventario con los bienes en poder del heredero; Escrito a la notaría del heredero que delibera teniendo los bienes de la herencia.

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Testamento abierto con legado de usufructo al cónyuge»
   - «Solicitud de división judicial de la herencia»
   - «Escritura de aceptación y partición de herencia»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-herencias-y-donaciones:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-herencias-y-donaciones:solicitud-division-judicial-herencia-liquidacion-civ-0401`. Los nombres están en la lista de formularios de abajo.

## Qué hace Claude cuando usas un formulario

1. Comprueba que Jurisprudenciator está conectado. Si no lo está, se para y te dice cómo conectarlo: no redacta nada sin él. Todos los datos jurídicos del documento (artículos vigentes, sentencias con su ECLI, datos registrales) salen de Jurisprudenciator; nunca de memoria.
2. Te pide en una sola tanda los datos del caso (partes, órgano, fechas, importes…). Lo que no sepas queda como hueco visible.
3. Resuelve contigo las opciones que el formulario deja abiertas y decide qué párrafos opcionales entran según los hechos.
4. Aplica las notas de actualización de la revisión del 25-11-2026 (reformas legales, órganos judiciales de la LO 1/2025, plazos).
5. Comprueba en el BOE, con Jurisprudenciator, cada norma que cita el documento; si alguna ha cambiado, usa la redacción vigente y te lo dice.
6. Te entrega el documento en Word **tal cual es el formulario**: empieza por su primera línea, sin títulos, notas ni explicaciones añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. En el chat te dice lo que queda pendiente y, si es un escrito, el plazo y ante quién se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.

## Antes de empezar

- **Dónde funciona:** en Claude Code y en Claude (web, escritorio y Cowork). Se instala desde este repositorio de GitHub o subiendo el ZIP del plugin.
- **Jurisprudenciator es imprescindible:** el plugin trae el conector y cada skill trabaja siempre con él. Sin una cuenta de Jurisprudenciator conectada, las skills se paran y no redactan nada. La primera vez hay que iniciar sesión (en Claude Code, con `/mcp`; o con tu URL personal: https://jurisprudenciator.lexiaipro.org/instalacion). Si ya tienes Jurisprudenciator conectado en Claude, las skills usan ese.
- **Espacio que ocupa:** unos 9.783 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-herencias-y-donaciones@formularios-juridicos-civil-espana`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-civil-espana
/plugin install formularios-herencias-y-donaciones@formularios-juridicos-civil-espana
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-civil-espana`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-herencias-y-donaciones.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (163)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0401 | Solicitud de división judicial de herencia y liquidación de la sociedad de gananciales | `solicitud-division-judicial-herencia-liquidacion-civ-0401` |
| CIV-0402 | Testamento con usufructo poderoso según el Derecho civil vasco | `testamento-usufructo-poderoso-segun-derecho-civil-vasco-civ-0402` |
| CIV-0403 | Testamento con poder testatorio según el Derecho civil vasco | `testamento-poder-testatorio-segun-derecho-civil-vasco-civ-0403` |
| CIV-0404 | Testamento otorgado por el comisario según el Derecho civil vasco | `testamento-otorgado-comisario-segun-derecho-civil-vasco-civ-0404` |
| CIV-0405 | Testamento hil buruko según el Derecho civil vasco | `testamento-hil-buruko-segun-derecho-civil-vasco-civ-0405` |
| CIV-0406 | Escritura de adjudicación de la herencia de confianza según el Derecho civil catalán | `escritura-adjudicacion-herencia-confianza-segun-civ-0406` |
| CIV-0407 | Escritura de fiducia colectiva según el Derecho civil aragonés | `escritura-fiducia-colectiva-segun-derecho-civil-civ-0407` |
| CIV-0408 | Escritura de fiducia sucesoria otorgada por un cónyuge según el Derecho civil aragonés | `escritura-fiducia-sucesoria-otorgada-conyuge-segun-civ-0408` |
| CIV-0409 | Demanda para completar o adicionar la partición de la herencia | `demanda-completar-adicionar-particion-herencia-civ-0409` |
| CIV-0410 | Escrito a la notaría del heredero que delibera sin tener los bienes de la herencia | `escrito-notaria-heredero-delibera-sin-tener-bienes-civ-0410` |
| CIV-0411 | Escrito a la notaría aceptando a beneficio de inventario con los bienes en poder del heredero | `escrito-notaria-aceptando-beneficio-inventario-bienes-civ-0411` |
| CIV-0412 | Escrito a la notaría del heredero que delibera teniendo los bienes de la herencia | `escrito-notaria-heredero-delibera-teniendo-bienes-civ-0412` |
| CIV-0413 | Escrito al tribunal aceptando la herencia a beneficio de inventario sin tener los bienes el heredero | `escrito-tribunal-aceptando-herencia-beneficio-civ-0413` |
| CIV-0414 | Escritura de poder especial entre cónyuges para otorgar la partición de herencia | `escritura-poder-especial-entre-conyuges-otorgar-civ-0414` |
| CIV-0415 | Manifestación de herencia testada por el hijo del causante como heredero único | `manifestacion-herencia-testada-hijo-causante-como-civ-0415` |
| CIV-0416 | Manifestación de herencia intestada por el cónyuge como heredero único | `manifestacion-herencia-intestada-conyuge-como-heredero-civ-0416` |
| CIV-0417 | Testamento con legado para la educación de un beneficiario | `testamento-legado-educacion-beneficiario-civ-0417` |
| CIV-0418 | Cláusula testamentaria de legado de pensión de alimentos | `clausula-testamentaria-legado-pension-alimentos-civ-0418` |
| CIV-0420 | Testamento que delega en otro la facultad de mejorar | `testamento-delega-otro-facultad-mejorar-civ-0420` |
| CIV-0421 | Testamento que autoriza al tutor a hacer suyos los frutos de los bienes del tutelado | `testamento-autoriza-tutor-hacer-suyos-frutos-bienes-civ-0421` |
| CIV-0422 | Testamento que excluye a una persona del cargo de tutor | `testamento-excluye-persona-cargo-tutor-civ-0422` |
| CIV-0423 | Solicitud al notario de testamento abierto de una persona judicialmente incapacitada | `solicitud-notario-testamento-abierto-persona-civ-0423` |
| CIV-0424 | Testamento con reconocimiento de hijo extramatrimonial | `testamento-reconocimiento-hijo-extramatrimonial-civ-0424` |
| CIV-0425 | Testamento con sustitución fideicomisaria a favor de un hijo o descendiente incapacitado | `testamento-sustitucion-fideicomisaria-favor-hijo-civ-0425` |
| CIV-0426 | Testamento abierto según el Derecho civil navarro | `testamento-abierto-segun-derecho-civil-navarro-civ-0426` |
| CIV-0427 | Acta de depósito de testamento según el Derecho navarro | `acta-deposito-testamento-segun-derecho-navarro-civ-0427` |
| CIV-0428 | Acta de notificación del pago de la legítima en metálico según el Derecho gallego | `acta-notificacion-pago-legitima-metalico-segun-derecho-civ-0428` |
| CIV-0429 | Testamento mancomunado según el Derecho civil gallego | `testamento-mancomunado-segun-derecho-civil-gallego-civ-0429` |
| CIV-0430 | Testamento por comisario según el Derecho civil gallego | `testamento-comisario-segun-derecho-civil-gallego-civ-0430` |
| CIV-0431 | Renuncia al usufructo de fidelidad según el Derecho navarro | `renuncia-usufructo-fidelidad-segun-derecho-navarro-civ-0431` |
| CIV-0432 | Testamento con mejora de labrar y poseer según el Derecho gallego | `testamento-mejora-labrar-poseer-segun-derecho-gallego-civ-0432` |
| CIV-0433 | Testamento en ejercicio del poder testatorio según el Derecho gallego | `testamento-ejercicio-poder-testatorio-segun-derecho-civ-0433` |
| CIV-0434 | Acta de depósito de pacto de hermandad según el Derecho navarro | `acta-deposito-pacto-hermandad-segun-derecho-navarro-civ-0434` |
| CIV-0435 | Testamento con heredero de confianza según el Derecho navarro | `testamento-heredero-confianza-segun-derecho-navarro-civ-0435` |
| CIV-0436 | Demanda de nulidad de testamento por incapacidad del testador y falta de formalidades | `demanda-nulidad-testamento-incapacidad-testador-falta-civ-0436` |
| CIV-0437 | Solicitud notarial de requerimiento para aceptar o repudiar la herencia (Derecho civil catalán) | `solicitud-notarial-requerimiento-aceptar-repudiar-civ-0437` |
| CIV-0438 | Acta de protocolización de testamento cerrado según el Derecho catalán | `acta-protocolizacion-testamento-cerrado-segun-derecho-civ-0438` |
| CIV-0439 | Testamento abierto con fiducia a favor del cónyuge según el Derecho catalán | `testamento-abierto-fiducia-favor-conyuge-segun-derecho-civ-0439` |
| CIV-0440 | Demanda de nulidad de testamento por falta de capacidad del testador (Derecho civil catalán) | `demanda-nulidad-testamento-falta-capacidad-testador-civ-0440` |
| CIV-0441 | Escritura de heredamiento simple según el Derecho catalán | `escritura-heredamiento-simple-segun-derecho-catalan-civ-0441` |
| CIV-0442 | Acta de protocolización instada por el párroco según el Derecho catalán | `acta-protocolizacion-instada-parroco-segun-derecho-civ-0442` |
| CIV-0443 | Capítulos matrimoniales con heredamiento cumulativo según el Derecho catalán | `capitulos-matrimoniales-heredamiento-cumulativo-segun-civ-0443` |
| CIV-0444 | Codicilo según el Derecho civil de Baleares (Mallorca y Menorca) | `codicilo-segun-derecho-civil-baleares-mallorca-menorca-civ-0444` |
| CIV-0445 | Demanda de nulidad de la institución de heredero por preterición no intencional | `demanda-nulidad-institucion-heredero-pretericion-no-civ-0445` |
| CIV-0446 | Testamento mancomunado abierto según el Derecho aragonés | `testamento-mancomunado-abierto-segun-derecho-aragones-civ-0446` |
| CIV-0447 | Escritura de institución de heredero a favor de un tercero según el Derecho aragonés | `escritura-institucion-heredero-favor-tercero-segun-civ-0447` |
| CIV-0448 | Escritura de institución recíproca de heredero según el Derecho aragonés | `escritura-institucion-reciproca-heredero-segun-derecho-civ-0448` |
| CIV-0449 | Escritura de revocación de pacto sucesorio según el Derecho aragonés | `escritura-revocacion-pacto-sucesorio-segun-derecho-civ-0449` |
| CIV-0450 | Escritura de institución de heredero de presente según el Derecho aragonés | `escritura-institucion-heredero-presente-segun-derecho-civ-0450` |
| CIV-0451 | Sucesión paccionada con institución de heredero para después de los días según el Derecho aragonés | `sucesion-paccionada-institucion-heredero-despues-dias-civ-0451` |
| CIV-0452 | Testamento abierto otorgado por quien no tiene legitimarios | `testamento-abierto-otorgado-quien-no-tiene-legitimarios-civ-0452` |
| CIV-0453 | Testamento abierto con usufructo universal y cláusula de sustitución | `testamento-abierto-usufructo-universal-clausula-civ-0453` |
| CIV-0454 | Escritura de poder a un abogado para aceptar una herencia | `escritura-poder-abogado-aceptar-herencia-civ-0454` |
| CIV-0455 | Contrato por el que se ceden derechos hereditarios | `contrato-ceden-derechos-hereditarios-civ-0455` |
| CIV-0456 | Acta notarial de notoriedad para declarar herederos abintestato | `acta-notarial-notoriedad-declarar-herederos-abintestato-civ-0456` |
| CIV-0457 | Escritura de poder especial para actuaciones sucesorias | `escritura-poder-especial-actuaciones-sucesorias-civ-0457` |
| CIV-0458 | Cuaderno particional de herencia testada con viuda e hijos y liquidación de gananciales | `cuaderno-particional-herencia-testada-viuda-e-hijos-civ-0458` |
| CIV-0459 | Escritura de renuncia a la herencia por legitimario preterido | `escritura-renuncia-herencia-legitimario-preterido-civ-0459` |
| CIV-0460 | Compromiso de venta de bienes de la herencia | `compromiso-venta-bienes-herencia-civ-0460` |
| CIV-0461 | Escritura de entrega del legado al legatario | `escritura-entrega-legado-legatario-civ-0461` |
| CIV-0462 | Testamento con legado, usufructo universal y contador partidor | `testamento-legado-usufructo-universal-contador-partidor-civ-0462` |
| CIV-0463 | Testamento con cláusula de desheredación | `testamento-clausula-desheredacion-civ-0463` |
| CIV-0464 | Cuaderno particional de herencia testada con viuda e hijos, gananciales y conmutación de usufructo | `cuaderno-particional-herencia-testada-viuda-e-hijos-civ-0464` |
| CIV-0465 | Testamento abierto con usufructo universal según el Derecho de Baleares | `testamento-abierto-usufructo-universal-segun-derecho-civ-0465` |
| CIV-0466 | Demanda de reclamación de un legado específico de cosa propia del testador | `demanda-reclamacion-legado-especifico-cosa-propia-civ-0466` |
| CIV-0467 | Demanda sucesoria con conflicto de aplicación de derechos civiles forales o especiales | `demanda-sucesoria-conflicto-aplicacion-derechos-civ-0467` |
| CIV-0468 | Solicitud notarial de adveración, apertura y protocolización de testamento cerrado | `solicitud-notarial-adveracion-apertura-protocolizacion-civ-0468` |
| CIV-0469 | Solicitud notarial de adveración y protocolización de testamento ológrafo | `solicitud-notarial-adveracion-protocolizacion-civ-0469` |
| CIV-0470 | Requerimiento inicial ante notario para la declaración de herederos abintestato | `requerimiento-inicial-ante-notario-declaracion-civ-0470` |
| CIV-0471 | Requerimiento notarial para que el heredero acepte o repudie la herencia (interrogatio in iure) | `requerimiento-notarial-heredero-acepte-repudie-civ-0471` |
| CIV-0472 | Escritura de poder para aceptar herencias | `escritura-poder-aceptar-herencias-civ-0472` |
| CIV-0473 | Demanda de juicio ordinario de petición de herencia | `demanda-juicio-ordinario-peticion-herencia-civ-0473` |
| CIV-0474 | Otrosí de demanda de división de herencia sobre intervención del Fiscal hasta nombrar defensor | `otrosi-demanda-division-herencia-sobre-intervencion-civ-0474` |
| CIV-0475 | Solicitud de hacer definitiva la posesión interina de bienes hereditarios sin reclamación en 40 días | `solicitud-hacer-definitiva-posesion-interina-bienes-civ-0475` |
| CIV-0476 | Demanda de juicio ordinario que impugna la desheredación en el testamento | `demanda-juicio-ordinario-impugna-desheredacion-civ-0476` |
| CIV-0477 | Demanda ordinaria de rescisión de partición hereditaria por lesión en la valoración de bienes | `demanda-ordinaria-rescision-particion-hereditaria-civ-0477` |
| CIV-0478 | Demanda de juicio ordinario de reducción de la cuota hereditaria por donación inoficiosa | `demanda-juicio-ordinario-reduccion-cuota-hereditaria-civ-0478` |
| CIV-0479 | Demanda de juicio ordinario de complemento de legítima según el Derecho civil de Cataluña | `demanda-juicio-ordinario-complemento-legitima-segun-civ-0479` |
| CIV-0480 | Demanda de juicio ordinario de nulidad del acta notarial de notoriedad de declaración de herederos | `demanda-juicio-ordinario-nulidad-acta-notarial-civ-0480` |
| CIV-0481 | Demanda de juicio ordinario que impugna la partición por no incluir bienes en el inventario | `demanda-juicio-ordinario-impugna-particion-no-incluir-civ-0481` |
| CIV-0482 | Demanda de juicio ordinario de reclamación de legítima por nulidad de la desheredación | `demanda-juicio-ordinario-reclamacion-legitima-nulidad-civ-0482` |
| CIV-0483 | Demanda de juicio ordinario de reclamación de legítima en derecho común por preterición intencional | `demanda-juicio-ordinario-reclamacion-legitima-derecho-civ-0483` |
| CIV-0484 | Escrito de los contadores que devuelve los autos y presenta el cuaderno particional | `escrito-contadores-devuelve-autos-presenta-cuaderno-civ-0484` |
| CIV-0485 | Cuaderno particional presentado por el contador | `cuaderno-particional-presentado-contador-civ-0485` |
| CIV-0486 | Cuenta final complementaria del administrador de la herencia | `cuenta-final-complementaria-administrador-herencia-civ-0486` |
| CIV-0487 | Contrato de compromiso de venta de un tercio indiviso de una herencia | `contrato-compromiso-venta-tercio-indiviso-herencia-civ-0487` |
| CIV-0488 | Acta de comparecencia del contador y de las partes (art. 787.3 LEC) | `acta-comparecencia-contador-partes-art-787-3-lec-civ-0488` |
| CIV-0489 | Cuenta final justificada del administrador de la herencia | `cuenta-final-justificada-administrador-herencia-civ-0489` |
| CIV-0490 | Escrito de oposición a las operaciones particionales del contador | `escrito-oposicion-operaciones-particionales-contador-civ-0490` |
| CIV-0491 | Demanda para que los hijos obtengan la posesión de los bienes de la herencia | `demanda-hijos-obtengan-posesion-bienes-herencia-civ-0491` |
| CIV-0492 | Escrito pidiendo alzar la suspensión del juicio divisorio por prejudicialidad penal | `escrito-pidiendo-alzar-suspension-juicio-divisorio-civ-0492` |
| CIV-0494 | Demanda de reserva del cónyuge binubo y de simulación en la transmisión de un inmueble reservable | `demanda-reserva-conyuge-binubo-simulacion-transmision-civ-0494` |
| CIV-2334 | Demanda de nulidad del testamento por captación de la voluntad de un testador sin capacidad | `demanda-nulidad-testamento-captacion-voluntad-testador-civ-2334` |
| CIV-2335 | Demanda de nulidad de la institución de heredero por desheredación injusta en Derecho foral | `demanda-nulidad-institucion-heredero-desheredacion-civ-2335` |
| CIV-2336 | Petición de autorizar reparaciones extraordinarias y vender bienes de la herencia intervenida | `peticion-autorizar-reparaciones-extraordinarias-vender-civ-2336` |
| CIV-2337 | Solicitud de división judicial de la herencia presentada por los hijos y el cónyuge viudo | `solicitud-division-judicial-herencia-presentada-hijos-civ-2337` |
| CIV-2338 | Solicitud de medidas complementarias tras la intervención judicial del caudal hereditario | `solicitud-medidas-complementarias-tras-intervencion-civ-2338` |
| CIV-2339 | Oposición del acreedor de la herencia al reparto mientras no se pague o garantice su crédito | `oposicion-acreedor-herencia-reparto-mientras-no-pague-civ-2339` |
| CIV-2340 | Escrito del Fiscal como defensor de un pariente que pide sobreseer la intervención de la herencia | `escrito-fiscal-como-defensor-pariente-pide-sobreseer-civ-2340` |
| CIV-2341 | Contestación a la demanda de nulidad de la institución de heredero por desheredación injusta | `contestacion-demanda-nulidad-institucion-heredero-civ-2341` |
| CIV-2342 | Escritura de aceptación de la herencia a beneficio de inventario | `escritura-aceptacion-herencia-beneficio-inventario-civ-2342` |
| CIV-2343 | Escritura notarial de aceptación de la herencia | `escritura-notarial-aceptacion-herencia-civ-2343` |
| CIV-2344 | Escritura notarial de renuncia a la herencia | `escritura-notarial-renuncia-herencia-civ-2344` |
| CIV-2345 | Testamento ológrafo escrito y firmado de puño y letra por el testador | `testamento-olografo-escrito-firmado-puno-letra-testador-civ-2345` |
| CIV-2346 | Cuaderno de operaciones particionales de la herencia otorgado por los herederos | `cuaderno-operaciones-particionales-herencia-otorgado-civ-2346` |
| CIV-2347 | Testamento cerrado otorgado ante notario | `testamento-cerrado-otorgado-ante-notario-civ-2347` |
| CIV-2348 | Documento privado de donación remuneratoria | `documento-privado-donacion-remuneratoria-civ-2348` |
| CIV-2349 | Escritura de donación onerosa o con carga para el donatario | `escritura-donacion-onerosa-carga-donatario-civ-2349` |
| CIV-2350 | Contrato de venta de la herencia por los herederos | `contrato-venta-herencia-herederos-civ-2350` |
| CIV-2351 | Solicitud de división judicial de herencia que cuestiona la cláusula testamentaria de arbitraje | `solicitud-division-judicial-herencia-cuestiona-civ-2351` |
| CIV-2352 | Otrosí que pide intervenir el caudal en la declaración de herederos dentro de la división judicial | `otrosi-pide-intervenir-caudal-declaracion-herederos-civ-2352` |
| CIV-2353 | Escrito del contador-partidor que pide al tribunal el nombramiento de un perito | `escrito-contador-partidor-pide-tribunal-nombramiento-civ-2353` |
| CIV-2354 | Escrito del administrador de la herencia que acredita la fianza constituida en metálico | `escrito-administrador-herencia-acredita-fianza-civ-2354` |
| CIV-2355 | Petición de todos los interesados de cesar la intervención de la herencia al pagar a los acreedores | `peticion-todos-interesados-cesar-intervencion-herencia-civ-2355` |
| CIV-2356 | Escrito del contador-partidor que reclama el pago de sus honorarios en la división judicial | `escrito-contador-partidor-reclama-pago-honorarios-civ-2356` |
| CIV-2357 | Escrito del contador-partidor que pide a los herederos la entrega de la documentación de la herencia | `escrito-contador-partidor-pide-herederos-entrega-civ-2357` |
| CIV-2358 | Demanda de juicio verbal para reclamar los alimentos dejados en un legado | `demanda-juicio-verbal-reclamar-alimentos-dejados-legado-civ-2358` |
| CIV-2359 | Solicitud del legatario de parte alícuota para que se divida judicialmente la herencia | `solicitud-legatario-parte-alicuota-divida-civ-2359` |
| CIV-2360 | Oposición del acreedor del causante con título ejecutivo a que se haga la partición de la herencia | `oposicion-acreedor-causante-titulo-ejecutivo-haga-civ-2360` |
| CIV-2361 | Oposición del heredero a la división judicial por existir un testamento ológrafo posterior | `oposicion-heredero-division-judicial-existir-civ-2361` |
| CIV-2362 | Oposición del heredero a las operaciones divisorias del contador por error de cálculo | `oposicion-heredero-operaciones-divisorias-contador-civ-2362` |
| CIV-2363 | Escrito del heredero que se muestra conforme con las operaciones divisorias de la herencia | `escrito-heredero-muestra-conforme-operaciones-civ-2363` |
| CIV-2364 | Oposición del heredero a las operaciones divisorias por no capitalizar el usufructo legal | `oposicion-heredero-operaciones-divisorias-no-civ-2364` |
| CIV-2365 | Petición de entregar a los herederos los bienes adjudicados al constar pagadas las deudas | `peticion-entregar-herederos-bienes-adjudicados-constar-civ-2365` |
| CIV-2366 | Escrito que aporta el avalúo de la herencia y pide reanudar la oposición al cuaderno particional | `escrito-aporta-avaluo-herencia-pide-reanudar-oposicion-civ-2366` |
| CIV-2367 | Declinatoria de los coherederos en la división judicial por haber previsto el testador un arbitraje | `declinatoria-coherederos-division-judicial-haber-civ-2367` |
| CIV-2368 | Solicitud de división judicial de la herencia por muerte del contador-partidor y falta de acuerdo | `solicitud-division-judicial-herencia-muerte-contador-civ-2368` |
| CIV-2369 | Petición del coheredero para suspender la división de herencia por prejudicialidad penal | `peticion-coheredero-suspender-division-herencia-civ-2369` |
| CIV-2370 | Otrosí de la solicitud de división de herencia que pide formar inventario de los bienes | `otrosi-solicitud-division-herencia-pide-formar-civ-2370` |
| CIV-2371 | Recurso de reposición contra la admisión de la partición pedida por un legatario de parte alícuota | `recurso-reposicion-contra-admision-particion-pedida-civ-2371` |
| CIV-2372 | Otrosí de la solicitud de división de herencia que pide intervenir el caudal hereditario | `otrosi-solicitud-division-herencia-pide-intervenir-civ-2372` |
| CIV-2373 | Otrosí de la solicitud de división de herencia sobre la intervención del Ministerio Fiscal | `otrosi-solicitud-division-herencia-sobre-intervencion-civ-2373` |
| CIV-2374 | Petición del acreedor del difunto para que se intervenga judicialmente la herencia | `peticion-acreedor-difunto-intervenga-judicialmente-civ-2374` |
| CIV-2375 | Petición de sustituir al administrador de la herencia por falta de capacidad para el cargo | `peticion-sustituir-administrador-herencia-falta-civ-2375` |
| CIV-2376 | Personación de los representantes del concebido no nacido en la partición, pidiendo inventario | `personacion-representantes-concebido-no-nacido-civ-2376` |
| CIV-2377 | Oposición de los coherederos a la división pedida por un legatario por haber contador designado | `oposicion-coherederos-division-pedida-legatario-haber-civ-2377` |
| CIV-2378 | Oposición del heredero a la división judicial porque el causante nombró un contador-partidor | `oposicion-heredero-division-judicial-porque-causante-civ-2378` |
| CIV-2379 | Escrito de algunos herederos que dispensan al administrador de la herencia de prestar caución | `escrito-algunos-herederos-dispensan-administrador-civ-2379` |
| CIV-2380 | Escrito del coheredero que afianza el crédito del acreedor del causante para evitar su oposición | `escrito-coheredero-afianza-credito-acreedor-causante-civ-2380` |
| CIV-2381 | Personación en la partición judicial de la herencia del representante legal de un coheredero | `personacion-particion-judicial-herencia-representante-civ-2381` |
| CIV-2382 | Escrito de todos los herederos que dispensan de común acuerdo al administrador de prestar caución | `escrito-todos-herederos-dispensan-comun-acuerdo-civ-2382` |
| CIV-2383 | Escrito del administrador de la herencia que acredita la fianza constituida mediante aval bancario | `escrito-administrador-herencia-acredita-fianza-civ-2383` |
| CIV-2384 | Escrito de todos los interesados con un avalúo pactado de la herencia para alzar la suspensión | `escrito-todos-interesados-avaluo-pactado-herencia-civ-2384` |
| CIV-2385 | Escrito de todos los interesados que pide poner fin a la intervención judicial de la herencia | `escrito-todos-interesados-pide-poner-fin-intervencion-civ-2385` |
| CIV-2386 | Petición del cónyuge viudo, administrador de la herencia, para que se le exima de prestar caución | `peticion-conyuge-viudo-administrador-herencia-le-exima-civ-2386` |
| CIV-2387 | Petición del coheredero de un plazo para que el contador presente las operaciones divisorias | `peticion-coheredero-plazo-contador-presente-civ-2387` |
| CIV-2388 | Escrito del acreedor de un coheredero que pide intervenir en la partición judicial de la herencia | `escrito-acreedor-coheredero-pide-intervenir-particion-civ-2388` |
| CIV-2389 | Contestación que se opone a la nulidad de una compraventa simulada y al complemento de la legítima | `contestacion-opone-nulidad-compraventa-simulada-civ-2389` |
| CIV-2390 | Demanda que pide la nulidad de una compraventa simulada y reclama la legítima | `demanda-pide-nulidad-compraventa-simulada-reclama-civ-2390` |
| CIV-2391 | Contestación por falta de representación del administrador de la herencia tras declarar herederos | `contestacion-falta-representacion-administrador-civ-2391` |
| CIV-2392 | Escritura de aceptación de herencia y adjudicación de los bienes a los herederos | `escritura-aceptacion-herencia-adjudicacion-bienes-civ-2392` |
| CIV-2393 | Cuaderno particional de la herencia intestada de un causante sin hijos a favor de sus hermanos | `cuaderno-particional-herencia-intestada-causante-sin-civ-2393` |
| CIV-2394 | Testamento abierto que lega al cónyuge el tercio de libre disposición | `testamento-abierto-lega-conyuge-tercio-libre-civ-2394` |
| CIV-2395 | Testamento abierto con sustituciones vulgar y ejemplar de los herederos | `testamento-abierto-sustituciones-vulgar-ejemplar-civ-2395` |
| CIV-2396 | Testamento abierto de persona sin descendientes con sustitución fideicomisaria de residuo | `testamento-abierto-persona-sin-descendientes-civ-2396` |
| CIV-2397 | Escritura de venta de los derechos hereditarios que corresponden al vendedor | `escritura-venta-derechos-hereditarios-corresponden-civ-2397` |
| CIV-2398 | Escritura de aceptación, renuncia y adjudicación de herencia con un heredero con discapacidad | `escritura-aceptacion-renuncia-adjudicacion-herencia-civ-2398` |
| CIV-2399 | Contrato privado de cesión onerosa de derechos hereditarios | `contrato-privado-cesion-onerosa-derechos-hereditarios-civ-2399` |
| CIV-2400 | Documento privado de venta por los herederos testamentarios antes de adjudicarse la herencia | `documento-privado-venta-herederos-testamentarios-antes-civ-2400` |
| CIV-2401 | Poder especial para aceptar una herencia en nombre del poderdante | `poder-especial-aceptar-herencia-nombre-poderdante-civ-2401` |
| CIV-2402 | Testamento abierto de una persona soltera sin hijos ni legitimarios | `testamento-abierto-persona-soltera-sin-hijos-ni-civ-2402` |
| CIV-2403 | Testamento abierto de matrimonio con hijos menores que nombra contador-partidor y tutor | `testamento-abierto-matrimonio-hijos-menores-nombra-civ-2403` |
| CIV-2404 | Escritura de aceptación y adjudicación de la herencia al viudo y a los hijos | `escritura-aceptacion-adjudicacion-herencia-viudo-hijos-civ-2404` |

## Privacidad

Ver `PRIVACY.md`.
