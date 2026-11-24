# Ejecución de sentencias y embargos

> Plugin de Claude Code `formularios-ejecucion-y-embargos` · **311 formularios** · Civil · normativa revisada el 24-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Para ejecutar lo ganado: demanda ejecutiva (título judicial, no judicial, laudo, acuerdo de mediación), ejecución provisional, embargo y mejora de embargo, averiguación patrimonial, subasta, lanzamiento, ejecución hipotecaria, tercerías, oposición del ejecutado y liquidación de intereses y costas.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 311 está al final):

- **Demandas, peticiones y solicitudes iniciales** (73). Por ejemplo: Demanda ejecutiva de sentencia extranjera conforme al Reglamento (UE) nº 1215-2012; Demanda ejecutiva de sentencia firme que anula la cláusula suelo y ordena devolver cantidades; Demanda ejecutiva basada en auto que homologa una transacción judicial.
- **Contestaciones, oposiciones y alegaciones** (59). Por ejemplo: Escrito de oposición a la ejecución del fiador solidario o avalista; Escrito de oposición a la ejecución de un auto que homologa un acuerdo de mediación; Oposición a la ejecución de un acuerdo de mediación por motivos procesales o de fondo.
- **Recursos** (11). Por ejemplo: Recurso de apelación contra el auto que estima la oposición por abusividad en ejecución hipotecaria; Apelación del ejecutado contra el auto que desestima la oposición (auto de cuantía máxima); Apelación del ejecutante contra el auto que estima la oposición (auto de cuantía máxima).
- **Contratos, pactos y cláusulas** (1). Por ejemplo: Acuerdo de mediación alcanzado durante la ejecución de una sentencia.
- **Estatutos, actas, certificaciones y escrituras** (6). Por ejemplo: Certificado de título ejecutivo europeo para transacción judicial aprobada; Certificado sustitutivo de título ejecutivo europeo emitido tras un recurso (art. 6.3); Certificado de título ejecutivo europeo para resolución judicial.
- **Comunicaciones, requerimientos y cartas** (29). Por ejemplo: Declaración responsable del deudor sobre requisitos de la Ley 1-2013 para paralizar el lanzamiento; Solicitud conjunta de suspender el proceso de ejecución para intentar una mediación; Solicitud de un interesado en la subasta para inspeccionar el inmueble.
- **Escritos de trámite y otros** (132). Por ejemplo: Escrito de suspensión del lanzamiento de vivienda habitual de colectivos especialmente vulnerables; Escrito del ejecutante impugnando la oposición a la ejecución de un acuerdo de mediación; Declinatoria por falta de competencia territorial en la ejecución de un acuerdo de mediación.

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Demanda de ejecución de una sentencia de condena dineraria»
   - «Oposición a la ejecución hipotecaria por cláusulas abusivas»
   - «Solicitud de mejora de embargo»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-ejecucion-y-embargos:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-ejecucion-y-embargos:demanda-ejecutiva-sentencia-extranjera-conforme-civ-1394`. Los nombres están en la lista de formularios de abajo.

## Qué hace Claude cuando usas un formulario

1. Comprueba que Jurisprudenciator está conectado. Si no lo está, se para y te dice cómo conectarlo: no redacta nada sin él. Todos los datos jurídicos del documento (artículos vigentes, sentencias con su ECLI, datos registrales) salen de Jurisprudenciator; nunca de memoria.
2. Te pide en una sola tanda los datos del caso (partes, órgano, fechas, importes…). Lo que no sepas queda como hueco visible.
3. Resuelve contigo las opciones que el formulario deja abiertas y decide qué párrafos opcionales entran según los hechos.
4. Aplica las notas de actualización de la revisión del 24-11-2026 (reformas legales, órganos judiciales de la LO 1/2025, plazos).
5. Comprueba en el BOE, con Jurisprudenciator, cada norma que cita el documento; si alguna ha cambiado, usa la redacción vigente y te lo dice.
6. Te entrega el documento en Word **tal cual es el formulario**: empieza por su primera línea, sin títulos, notas ni explicaciones añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. En el chat te dice lo que queda pendiente y, si es un escrito, el plazo y ante quién se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.

## Antes de empezar

- **Dónde funciona:** en Claude Code y en Claude (web, escritorio y Cowork). Se instala desde este repositorio de GitHub o subiendo el ZIP del plugin.
- **Jurisprudenciator es imprescindible:** el plugin trae el conector y cada skill trabaja siempre con él. Sin una cuenta de Jurisprudenciator conectada, las skills se paran y no redactan nada. La primera vez hay que iniciar sesión (en Claude Code, con `/mcp`; o con tu URL personal: https://jurisprudenciator.lexiaipro.org/instalacion). Si ya tienes Jurisprudenciator conectado en Claude, las skills usan ese.
- **Espacio que ocupa:** unos 19.066 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-ejecucion-y-embargos@formularios-juridicos-civil-espana`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-civil-espana
/plugin install formularios-ejecucion-y-embargos@formularios-juridicos-civil-espana
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-civil-espana`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-ejecucion-y-embargos.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (311)

| Código | Formulario | Skill |
|---|---|---|
| CIV-1394 | Demanda ejecutiva de sentencia extranjera conforme al Reglamento (UE) nº 1215-2012 | `demanda-ejecutiva-sentencia-extranjera-conforme-civ-1394` |
| CIV-1395 | Escrito de oposición a la ejecución del fiador solidario o avalista | `escrito-oposicion-ejecucion-fiador-solidario-avalista-civ-1395` |
| CIV-1396 | Demanda ejecutiva de sentencia firme que anula la cláusula suelo y ordena devolver cantidades | `demanda-ejecutiva-sentencia-firme-anula-clausula-suelo-civ-1396` |
| CIV-1397 | Demanda ejecutiva basada en auto que homologa una transacción judicial | `demanda-ejecutiva-basada-auto-homologa-transaccion-civ-1397` |
| CIV-1398 | Escrito de suspensión del lanzamiento de vivienda habitual de colectivos especialmente vulnerables | `escrito-suspension-lanzamiento-vivienda-habitual-civ-1398` |
| CIV-1399 | Declaración responsable del deudor sobre requisitos de la Ley 1-2013 para paralizar el lanzamiento | `declaracion-responsable-deudor-sobre-requisitos-ley-1-civ-1399` |
| CIV-1400 | Demanda ejecutiva de sentencia firme contra los herederos del condenado fallecido | `demanda-ejecutiva-sentencia-firme-contra-herederos-civ-1400` |
| CIV-1401 | Demanda ejecutiva basada en una póliza de contrato mercantil por cuotas impagadas | `demanda-ejecutiva-basada-poliza-contrato-mercantil-civ-1401` |
| CIV-1402 | Acuerdo de mediación alcanzado durante la ejecución de una sentencia | `acuerdo-mediacion-alcanzado-durante-ejecucion-sentencia-civ-1402` |
| CIV-1403 | Escrito de oposición a la ejecución de un auto que homologa un acuerdo de mediación | `escrito-oposicion-ejecucion-auto-homologa-acuerdo-civ-1403` |
| CIV-1404 | Oposición a la ejecución de un acuerdo de mediación por motivos procesales o de fondo | `oposicion-ejecucion-acuerdo-mediacion-motivos-civ-1404` |
| CIV-1405 | Escrito del ejecutante impugnando la oposición a la ejecución de un acuerdo de mediación | `escrito-ejecutante-impugnando-oposicion-ejecucion-civ-1405` |
| CIV-1406 | Solicitud conjunta de suspender el proceso de ejecución para intentar una mediación | `solicitud-conjunta-suspender-proceso-ejecucion-civ-1406` |
| CIV-1407 | Declinatoria por falta de competencia territorial en la ejecución de un acuerdo de mediación | `declinatoria-falta-competencia-territorial-ejecucion-civ-1407` |
| CIV-1408 | Escrito de allanamiento en un juicio ejecutivo sobre un automóvil | `escrito-allanamiento-juicio-ejecutivo-sobre-automovil-civ-1408` |
| CIV-1409 | Escrito de oposición a la ejecución dineraria por cláusulas abusivas | `escrito-oposicion-ejecucion-dineraria-clausulas-civ-1409` |
| CIV-1410 | Escrito del ejecutante pidiendo nuevas averiguaciones sobre el patrimonio del ejecutado | `escrito-ejecutante-pidiendo-nuevas-averiguaciones-civ-1410` |
| CIV-1411 | Escrito del ejecutado manifestando los bienes de su titularidad que pueden embargarse | `escrito-ejecutado-manifestando-bienes-titularidad-civ-1411` |
| CIV-1412 | Escrito de personación del arrendatario en la ejecución hipotecaria pidiendo intervenir | `escrito-personacion-arrendatario-ejecucion-hipotecaria-civ-1412` |
| CIV-1413 | Escrito del arrendatario de inmueble hipotecado subastado para que se declare su derecho a quedarse | `escrito-arrendatario-inmueble-hipotecado-subastado-civ-1413` |
| CIV-1414 | Escrito del ejecutado que acepta la inspección del inmueble hipotecado | `escrito-ejecutado-acepta-inspeccion-inmueble-hipotecado-civ-1414` |
| CIV-1415 | Escrito del ejecutante pidiendo convocar la subasta del bien hipotecado y la inspección del inmueble | `escrito-ejecutante-pidiendo-convocar-subasta-bien-civ-1415` |
| CIV-1416 | Alegaciones del ejecutante sobre reducir la deuda hipotecaria por colaboración del ejecutado | `alegaciones-ejecutante-sobre-reducir-deuda-hipotecaria-civ-1416` |
| CIV-1417 | Escrito del ejecutado pidiendo reducir la deuda hipotecaria por colaborar en la subasta | `escrito-ejecutado-pidiendo-reducir-deuda-hipotecaria-civ-1417` |
| CIV-1418 | Demanda ejecutiva de título judicial con condena dineraria y de hacer no personalísimo | `demanda-ejecutiva-titulo-judicial-condena-dineraria-civ-1418` |
| CIV-1419 | Escrito de oposición por motivos de fondo a la ejecución con auto de cuantía máxima | `escrito-oposicion-motivos-fondo-ejecucion-auto-cuantia-civ-1419` |
| CIV-1420 | Escrito del ejecutante oponiéndose a suspender el lanzamiento pedido por el ejecutado | `escrito-ejecutante-oponiendose-suspender-lanzamiento-civ-1420` |
| CIV-1421 | Alegaciones del ejecutado en el incidente de abusividad apreciada de oficio | `alegaciones-ejecutado-incidente-abusividad-apreciada-civ-1421` |
| CIV-1422 | Alegaciones del ejecutante en el incidente de abusividad apreciada de oficio | `alegaciones-ejecutante-incidente-abusividad-apreciada-civ-1422` |
| CIV-1423 | Oposición extraordinaria a la ejecución hipotecaria por abusividad de la cláusula que la fundamenta | `oposicion-extraordinaria-ejecucion-hipotecaria-civ-1423` |
| CIV-1424 | Escrito del ejecutado pidiendo recalcular los intereses de demora (Disp Trans 2ª Ley 1-2013) | `escrito-ejecutado-pidiendo-recalcular-intereses-demora-civ-1424` |
| CIV-1425 | Demanda de ejecución hipotecaria con aplicación de la cláusula de vencimiento anticipado | `demanda-ejecucion-hipotecaria-aplicacion-clausula-civ-1425` |
| CIV-1426 | Demanda de ejecución hipotecaria sobre la vivienda habitual del deudor | `demanda-ejecucion-hipotecaria-sobre-vivienda-habitual-civ-1426` |
| CIV-1427 | Recurso de apelación contra el auto que estima la oposición por abusividad en ejecución hipotecaria | `recurso-apelacion-contra-auto-estima-oposicion-civ-1427` |
| CIV-1428 | Solicitud de un interesado en la subasta para inspeccionar el inmueble | `solicitud-interesado-subasta-inspeccionar-inmueble-civ-1428` |
| CIV-1429 | Escrito del ejecutante en la ejecución ordinaria impugnando la oposición por abusividad | `escrito-ejecutante-ejecucion-ordinaria-impugnando-civ-1429` |
| CIV-1430 | Alegaciones del ejecutante sobre la limitación de los intereses de demora | `alegaciones-ejecutante-sobre-limitacion-intereses-civ-1430` |
| CIV-1431 | Demanda ejecutiva por la deuda que queda tras una ejecución hipotecaria | `demanda-ejecutiva-deuda-queda-tras-ejecucion-civ-1431` |
| CIV-1432 | Oposición extraordinaria a ejecución hipotecaria por abusividad de la cláusula de cantidad exigible | `oposicion-extraordinaria-ejecucion-hipotecaria-civ-1432` |
| CIV-1433 | Oposición a la ejecución hipotecaria por despacharse por una cantidad derivada de cláusula abusiva | `oposicion-ejecucion-hipotecaria-despacharse-cantidad-civ-1433` |
| CIV-1434 | Oposición a la ejecución hipotecaria por abusividad de la cláusula que fundamenta el despacho | `oposicion-ejecucion-hipotecaria-abusividad-clausula-civ-1434` |
| CIV-1435 | Escrito del ejecutado ante notario para suspender la ejecución hipotecaria extrajudicial por abusiva | `escrito-ejecutado-ante-notario-suspender-ejecucion-civ-1435` |
| CIV-1436 | Escrito del ejecutado pidiendo declarar abusiva y nula una cláusula en la ejecución hipotecaria | `escrito-ejecutado-pidiendo-declarar-abusiva-nula-civ-1436` |
| CIV-1437 | Escrito del ejecutado pidiendo suspender la ejecución hipotecaria por cláusulas abusivas | `escrito-ejecutado-pidiendo-suspender-ejecucion-civ-1437` |
| CIV-1438 | Oposición a la ejecución por pluspetición derivada de cláusula abusiva | `oposicion-ejecucion-pluspeticion-derivada-clausula-civ-1438` |
| CIV-1439 | Solicitud del ejecutante de autorización para publicar la sentencia en medios a costa del ejecutado | `solicitud-ejecutante-autorizacion-publicar-sentencia-civ-1439` |
| CIV-1440 | Demanda ejecutiva basada en un acuerdo de mediación elevado a escritura pública | `demanda-ejecutiva-basada-acuerdo-mediacion-elevado-civ-1440` |
| CIV-1441 | Demanda ejecutiva para ejecutar la condena a publicar la sentencia | `demanda-ejecutiva-ejecutar-condena-publicar-sentencia-civ-1441` |
| CIV-1442 | Escrito de petición de embargo de bienes del ejecutado tras la averiguación patrimonial | `escrito-peticion-embargo-bienes-ejecutado-tras-civ-1442` |
| CIV-1443 | Escrito de tasación de costas del abogado que se defiende a sí mismo como parte demandante | `escrito-tasacion-costas-abogado-defiende-si-mismo-como-civ-1443` |
| CIV-1444 | Escrito para paralizar la ejecución hipotecaria y el desahucio de la vivienda habitual | `escrito-paralizar-ejecucion-hipotecaria-desahucio-civ-1444` |
| CIV-1445 | Escrito de solicitud de ejecución provisional de sentencia | `escrito-solicitud-ejecucion-provisional-sentencia-civ-1445` |
| CIV-1446 | Demanda de tercería de dominio del cónyuge del deudor por bien privativo embargado | `demanda-terceria-dominio-conyuge-deudor-bien-privativo-civ-1446` |
| CIV-1447 | Demanda de tercería de dominio sobre un bien confesado como privativo | `demanda-terceria-dominio-sobre-bien-confesado-como-civ-1447` |
| CIV-1448 | Escrito de tercero para evitar el embargo de su vivienda habitual | `escrito-tercero-evitar-embargo-vivienda-habitual-civ-1448` |
| CIV-1449 | Escrito del ejecutante que acepta no embargar un bien privativo del cónyuge del ejecutado | `escrito-ejecutante-acepta-no-embargar-bien-privativo-civ-1449` |
| CIV-1450 | Demanda ejecutiva para actualizar la pensión de alimentos | `demanda-ejecutiva-actualizar-pension-alimentos-civ-1450` |
| CIV-1451 | Demanda de ejecución provisional para cobrar la pensión compensatoria fijada en sentencia | `demanda-ejecucion-provisional-cobrar-pension-civ-1451` |
| CIV-1452 | Oposición a la ejecución provisional que pide reducir la pensión compensatoria | `oposicion-ejecucion-provisional-pide-reducir-pension-civ-1452` |
| CIV-1453 | Escrito de ampliación de la demanda ejecutiva por incumplimiento reiterado del régimen de visitas | `escrito-ampliacion-demanda-ejecutiva-incumplimiento-civ-1453` |
| CIV-1454 | Oposición del cónyuge al embargo de bienes gananciales por deudas del consorte (art. 541.2 LEC) | `oposicion-conyuge-embargo-bienes-gananciales-deudas-civ-1454` |
| CIV-1455 | Escrito para notificar al cónyuge del deudor el embargo ganancial y anotarlo en el Registro | `escrito-notificar-conyuge-deudor-embargo-ganancial-civ-1455` |
| CIV-1456 | Oposición del cónyuge del ejecutado al embargo de bienes agermanados seguido como deuda consorcial | `oposicion-conyuge-ejecutado-embargo-bienes-agermanados-civ-1456` |
| CIV-1457 | Escrito del cónyuge que ejercita la opción disolutoria ante el embargo de bienes agermanados | `escrito-conyuge-ejercita-opcion-disolutoria-ante-civ-1457` |
| CIV-1458 | Oposición del cónyuge al embargo de bienes agermanados por haber bienes privativos suficientes | `oposicion-conyuge-embargo-bienes-agermanados-haber-civ-1458` |
| CIV-1459 | Escrito para notificar al cónyuge el embargo de posible vivienda familiar y anotarlo en el Registro | `escrito-notificar-conyuge-embargo-posible-vivienda-civ-1459` |
| CIV-1460 | Demanda de ejecución forzosa del auto de medidas provisionales previas | `demanda-ejecucion-forzosa-auto-medidas-provisionales-civ-1460` |
| CIV-1461 | Demanda ejecutiva para que el cónyuge sin uso de la vivienda familiar arrendada la abandone | `demanda-ejecutiva-conyuge-sin-uso-vivienda-familiar-civ-1461` |
| CIV-1462 | Demanda de ejecución por impago de la compensación económica (art. 232.5 CCCat) | `demanda-ejecucion-impago-compensacion-economica-art-civ-1462` |
| CIV-1463 | Declaración de gasto extraordinario previa a la ejecución por el carné de ciclomotor del hijo | `declaracion-gasto-extraordinario-previa-ejecucion-civ-1463` |
| CIV-1464 | Demanda ejecutiva basada en el auto que homologa un acuerdo de mediación | `demanda-ejecutiva-basada-auto-homologa-acuerdo-civ-1464` |
| CIV-1465 | Declinatoria por falta de competencia territorial en la ejecución de un acuerdo de media - variante 2 | `declinatoria-falta-competencia-territorial-ejecucion-civ-1465` |
| CIV-1466 | Demanda ejecutiva basada en aval bancario de la Ley 57 de 1968 sobre cantidades anticipadas | `demanda-ejecutiva-basada-aval-bancario-ley-57-1968-civ-1466` |
| CIV-1467 | Oposición a la ejecución de sentencia por impago de pensiones alegando el pago de lo reclamado | `oposicion-ejecucion-sentencia-impago-pensiones-civ-1467` |
| CIV-1468 | Oposición a ejecutar un acuerdo de mediación sobre alimentos del hijo mayor de edad (Ley 5 de 2012) | `oposicion-ejecutar-acuerdo-mediacion-sobre-alimentos-civ-1468` |
| CIV-1469 | Demanda ejecutiva de un acuerdo de mediación sobre alimentos del hijo mayor de edad (Ley 5 de 2012) | `demanda-ejecutiva-acuerdo-mediacion-sobre-alimentos-civ-1469` |
| CIV-1470 | Escrito pidiendo certificación de dominio y cargas en el procedimiento ejecutivo | `escrito-pidiendo-certificacion-dominio-cargas-civ-1470` |
| CIV-1471 | Escrito del ejecutante pidiendo mejorar el embargo por pensiones alimenticias o compensatorias | `escrito-ejecutante-pidiendo-mejorar-embargo-pensiones-civ-1471` |
| CIV-1472 | Escrito del ejecutante pidiendo el nombramiento de perito tasador | `escrito-ejecutante-pidiendo-nombramiento-perito-tasador-civ-1472` |
| CIV-1473 | Escrito del ejecutante pidiendo que se celebre la subasta | `escrito-ejecutante-pidiendo-celebre-subasta-civ-1473` |
| CIV-1474 | Escrito de manifestación de bienes del ejecutado | `escrito-manifestacion-bienes-ejecutado-civ-1474` |
| CIV-1475 | Demanda de ejecución provisional de una medida definitiva sobre régimen de visitas | `demanda-ejecucion-provisional-medida-definitiva-sobre-civ-1475` |
| CIV-1476 | Oposición por motivos de fondo a la ejecución de sentencia matrimonial por impago de pensiones | `oposicion-motivos-fondo-ejecucion-sentencia-civ-1476` |
| CIV-1477 | Demanda ejecutiva por rentas y cantidades fijadas en sentencia de juicio verbal de desahucio | `demanda-ejecutiva-rentas-cantidades-fijadas-sentencia-civ-1477` |
| CIV-1478 | Solicitud de que se despache ejecución tras el decreto que termina el juicio de desahucio | `solicitud-despache-ejecucion-tras-decreto-termina-civ-1478` |
| CIV-1479 | Solicitud de ejecución del decreto que anula el lanzamiento pero reconoce la cantidad reclamada | `solicitud-ejecucion-decreto-anula-lanzamiento-pero-civ-1479` |
| CIV-1480 | Apelación del ejecutado contra el auto que desestima la oposición (auto de cuantía máxima) | `apelacion-ejecutado-contra-auto-desestima-oposicion-civ-1480` |
| CIV-1481 | Apelación del ejecutante contra el auto que estima la oposición (auto de cuantía máxima) | `apelacion-ejecutante-contra-auto-estima-oposicion-auto-civ-1481` |
| CIV-1482 | Oposición por motivos procesales y de fondo a la ejecución de un auto de cuantía máxima | `oposicion-motivos-procesales-fondo-ejecucion-auto-civ-1482` |
| CIV-1483 | Escrito del procurador pidiendo ser facultado para obtener la certificación de dominio y cargas | `escrito-procurador-pidiendo-ser-facultado-obtener-civ-1483` |
| CIV-1484 | Demanda de ejecución hipotecaria sobre un inmueble | `demanda-ejecucion-hipotecaria-sobre-inmueble-civ-1484` |
| CIV-1485 | Oposición del ejecutado en la ejecución hipotecaria por extinción de la obligación garantizada | `oposicion-ejecutado-ejecucion-hipotecaria-extincion-civ-1485` |
| CIV-1486 | Demanda de ejecución de un laudo arbitral de consumo | `demanda-ejecucion-laudo-arbitral-consumo-civ-1486` |
| CIV-1487 | Oposición a la ejecución provisional de una condena no dineraria | `oposicion-ejecucion-provisional-condena-no-dineraria-civ-1487` |
| CIV-1488 | Escrito del ejecutante pidiendo el cambio de depositario | `escrito-ejecutante-pidiendo-cambio-depositario-civ-1488` |
| CIV-1489 | Escrito del ejecutante que impugna la oposición a la ejecución | `escrito-ejecutante-impugna-oposicion-ejecucion-civ-1489` |
| CIV-1490 | Demanda ejecutiva no dineraria de sentencia firme de desahucio | `demanda-ejecutiva-no-dineraria-sentencia-firme-civ-1490` |
| CIV-1491 | Escrito del ejecutado pidiendo la devolución del sobrante de la subasta | `escrito-ejecutado-pidiendo-devolucion-sobrante-subasta-civ-1491` |
| CIV-1492 | Oposición a la ejecución por no notificar el saldo deudor de una póliza mercantil | `oposicion-ejecucion-no-notificar-saldo-deudor-poliza-civ-1492` |
| CIV-1493 | Demanda de tercería de dominio sobre bien embargado en apremio de la Agencia Tributaria | `demanda-terceria-dominio-sobre-bien-embargado-apremio-civ-1493` |
| CIV-1494 | Demanda ejecutiva de sentencia que condena a emitir una declaración de voluntad | `demanda-ejecutiva-sentencia-condena-emitir-declaracion-civ-1494` |
| CIV-1495 | Demanda ejecutiva basada en escritura pública de préstamo | `demanda-ejecutiva-basada-escritura-publica-prestamo-civ-1495` |
| CIV-1496 | Solicitud de ejecución de la sentencia dictada en un juicio de desahucio | `solicitud-ejecucion-sentencia-dictada-juicio-desahucio-civ-1496` |
| CIV-1497 | Demanda ejecutiva por deuda garantizada con hipoteca de máximo | `demanda-ejecutiva-deuda-garantizada-hipoteca-maximo-civ-1497` |
| CIV-1498 | Demanda ejecutiva de laudo arbitral de desahucio | `demanda-ejecutiva-laudo-arbitral-desahucio-civ-1498` |
| CIV-1499 | Solicitud de suspensión de la ejecución de un laudo por haberse ejercitado la acción de anulación | `solicitud-suspension-ejecucion-laudo-haberse-civ-1499` |
| CIV-1500 | Impugnación de la oposición a la ejecución forzosa de un laudo arbitral | `impugnacion-oposicion-ejecucion-forzosa-laudo-arbitral-civ-1500` |
| CIV-1501 | Recurso de reposición contra el auto que deniega despachar ejecución de un laudo arbitral | `recurso-reposicion-contra-auto-deniega-despachar-civ-1501` |
| CIV-1502 | Oposición al despacho de ejecución de un laudo arbitral por defectos procesales | `oposicion-despacho-ejecucion-laudo-arbitral-defectos-civ-1502` |
| CIV-1503 | Demanda ejecutiva dineraria de un laudo arbitral | `demanda-ejecutiva-dineraria-laudo-arbitral-civ-1503` |
| CIV-1504 | Apelación contra el auto que deniega ejecutar un laudo arbitral en materia de arrendamientos | `apelacion-contra-auto-deniega-ejecutar-laudo-arbitral-civ-1504` |
| CIV-1505 | Escrito del ejecutante que impugna la oposición de fondo a la ejecución por impago de pensiones | `escrito-ejecutante-impugna-oposicion-fondo-ejecucion-civ-1505` |
| CIV-1506 | Oposición a ejecutar el impago de pensiones alegando la mayoría de edad e independencia del hijo | `oposicion-ejecutar-impago-pensiones-alegando-mayoria-civ-1506` |
| CIV-1507 | Oposición a la ejecución de medidas familiares por incumplimiento del régimen de visitas | `oposicion-ejecucion-medidas-familiares-incumplimiento-civ-1507` |
| CIV-1508 | Demanda ejecutiva para cumplir la condena de otorgar escritura pública | `demanda-ejecutiva-cumplir-condena-otorgar-escritura-civ-1508` |
| CIV-1509 | Oposición a la ejecución por impago de pensiones en proceso matrimonial alegando compensación | `oposicion-ejecucion-impago-pensiones-proceso-civ-1509` |
| CIV-1510 | Oposición a la ejecución forzosa de medidas de un proceso matrimonial | `oposicion-ejecucion-forzosa-medidas-proceso-matrimonial-civ-1510` |
| CIV-1511 | Ejecución forzosa con multas coercitivas al progenitor custodio que incumple las visitas | `ejecucion-forzosa-multas-coercitivas-progenitor-civ-1511` |
| CIV-1512 | Demanda de ejecución de póliza de crédito garantizada con prenda de acciones cotizadas | `demanda-ejecucion-poliza-credito-garantizada-prenda-civ-1512` |
| CIV-1513 | Escrito pidiendo el embargo del sueldo del deudor | `escrito-pidiendo-embargo-sueldo-deudor-civ-1513` |
| CIV-1514 | Demanda ejecutiva contra los herederos del beneficiario de una hipoteca inversa | `demanda-ejecutiva-contra-herederos-beneficiario-civ-1514` |
| CIV-1515 | Solicitud de multas coercitivas por incumplimiento de una medida de un proceso matrimonial | `solicitud-multas-coercitivas-incumplimiento-medida-civ-1515` |
| CIV-1516 | Escrito para declarar extraordinario un gasto no previsto en las medidas a efectos de ejecución | `escrito-declarar-extraordinario-gasto-no-previsto-civ-1516` |
| CIV-1517 | Demanda ejecutiva de gastos extraordinarios no previstos en la resolución judicial | `demanda-ejecutiva-gastos-extraordinarios-no-previstos-civ-1517` |
| CIV-1518 | Consignación del deudor por vencimiento anticipado en ejecución sobre la vivienda familiar | `consignacion-deudor-vencimiento-anticipado-ejecucion-civ-1518` |
| CIV-1519 | Escrito del ejecutado pidiendo suspender la ejecución provisional de una condena dineraria | `escrito-ejecutado-pidiendo-suspender-ejecucion-civ-1519` |
| CIV-1520 | Recurso directo de revisión contra la resolución del LAJ contraria al título ejecutivo | `recurso-directo-revision-contra-resolucion-laj-civ-1520` |
| CIV-1521 | Recurso directo de revisión contra el decreto del LAJ que declara terminada la ejecución | `recurso-directo-revision-contra-decreto-laj-declara-civ-1521` |
| CIV-1522 | Escrito del ejecutado pidiendo suspender la ejecución por encontrarse en situación concursal | `escrito-ejecutado-pidiendo-suspender-ejecucion-civ-1522` |
| CIV-1523 | Escrito del ejecutante pidiendo el reembargo de un bien | `escrito-ejecutante-pidiendo-reembargo-bien-civ-1523` |
| CIV-1524 | Escrito del ejecutante para terminar la administración para pago y realizar el bien embargado | `escrito-ejecutante-terminar-administracion-pago-civ-1524` |
| CIV-1525 | Escrito del ejecutante pidiendo nombrar depositario de un bien embargado | `escrito-ejecutante-pidiendo-nombrar-depositario-bien-civ-1525` |
| CIV-1526 | Recurso directo de revisión contra el decreto del LAJ que deniega la mejora de embargo | `recurso-directo-revision-contra-decreto-laj-deniega-civ-1526` |
| CIV-1527 | Escrito del ejecutado pidiendo aplazar el lanzamiento | `escrito-ejecutado-pidiendo-aplazar-lanzamiento-civ-1527` |
| CIV-1528 | Demanda de tercería de dominio en un proceso de ejecución hipotecaria | `demanda-terceria-dominio-proceso-ejecucion-hipotecaria-civ-1528` |
| CIV-1529 | Escrito del ejecutado pidiendo suspender la ejecución hipotecaria por prejudicialidad penal | `escrito-ejecutado-pidiendo-suspender-ejecucion-civ-1529` |
| CIV-1530 | Demanda ordinaria de nulidad del título de ejecución hipotecaria con retención de lo obtenido | `demanda-ordinaria-nulidad-titulo-ejecucion-hipotecaria-civ-1530` |
| CIV-1531 | Demanda ejecutiva para reclamar deudas garantizadas con prenda | `demanda-ejecutiva-reclamar-deudas-garantizadas-prenda-civ-1531` |
| CIV-1532 | Alegaciones del ejecutado a la tasación pericial aportando dictamen contradictorio | `alegaciones-ejecutado-tasacion-pericial-aportando-civ-1532` |
| CIV-1533 | Escrito del ejecutado que pide el cese de la administración judicial por mala gestión del ejecutante | `escrito-ejecutado-pide-cese-administracion-judicial-civ-1533` |
| CIV-1534 | Demanda de tercería de dominio frente al ejecutante | `demanda-terceria-dominio-frente-ejecutante-civ-1534` |
| CIV-1535 | Solicitud del ejecutante de ampliar el embargo tras admitirse una tercería de dominio | `solicitud-ejecutante-ampliar-embargo-tras-admitirse-civ-1535` |
| CIV-1536 | Escrito de contestación a una demanda de tercería de mejor derecho | `escrito-contestacion-demanda-terceria-mejor-derecho-civ-1536` |
| CIV-1537 | Escrito del ejecutado que pide anular el embargo de un bien inembargable | `escrito-ejecutado-pide-anular-embargo-bien-inembargable-civ-1537` |
| CIV-1538 | Alegaciones de las partes sobre la formación de lotes en la ejecución | `alegaciones-partes-sobre-formacion-lotes-ejecucion-civ-1538` |
| CIV-1539 | Oposición del acreedor a la liquidación de frutos y rentas presentada por el deudor (modelo) | `oposicion-acreedor-liquidacion-frutos-rentas-civ-1539` |
| CIV-1540 | Escrito del ejecutante que pide liquidar detalladamente daños y perjuicios (arts. 713 y ss. LEC) | `escrito-ejecutante-pide-liquidar-detalladamente-danos-civ-1540` |
| CIV-1541 | Oposición del deudor a la reclamación de daños y perjuicios en la ejecución | `oposicion-deudor-reclamacion-danos-perjuicios-ejecucion-civ-1541` |
| CIV-1542 | Solicitud del acreedor de administración o posesión interina de la finca hipotecada | `solicitud-acreedor-administracion-posesion-interina-civ-1542` |
| CIV-1543 | Solicitud del acreedor para que se fije la cantidad debida en concepto de frutos y rentas | `solicitud-acreedor-fije-cantidad-debida-concepto-civ-1543` |
| CIV-1544 | Escrito del ejecutante que pide notificar el lanzamiento a los ocupantes del inmueble | `escrito-ejecutante-pide-notificar-lanzamiento-civ-1544` |
| CIV-1545 | Solicitud del ejecutante de auto que tenga por emitida la declaración de voluntad del ejecutado | `solicitud-ejecutante-auto-tenga-emitida-declaracion-civ-1545` |
| CIV-1546 | Impugnación de la tasación de costas por indebidas (procurador) y por excesivas (abogado) | `impugnacion-tasacion-costas-indebidas-procurador-civ-1546` |
| CIV-1547 | Oposición a la impugnación de la tasación de costas por excesivas en el orden civil | `oposicion-impugnacion-tasacion-costas-excesivas-orden-civ-1547` |
| CIV-1548 | Recusación por el ejecutado del perito nombrado durante la ejecución | `recusacion-ejecutado-perito-nombrado-durante-ejecucion-civ-1548` |
| CIV-1549 | Escrito conjunto de ejecutante y ejecutado que acuerdan la valoración del bien embargado | `escrito-conjunto-ejecutante-ejecutado-acuerdan-civ-1549` |
| CIV-1550 | Solicitud del adquirente del inmueble subastado de lanzar a los ocupantes | `solicitud-adquirente-inmueble-subastado-lanzar-civ-1550` |
| CIV-1551 | Escrito del licitador que pide que se reserve la cantidad consignada en la subasta | `escrito-licitador-pide-reserve-cantidad-consignada-civ-1551` |
| CIV-1552 | Oposición del ocupante del inmueble subastado al lanzamiento | `oposicion-ocupante-inmueble-subastado-lanzamiento-civ-1552` |
| CIV-1553 | Solicitud del ejecutante de subasta del inmueble embargado | `solicitud-ejecutante-subasta-inmueble-embargado-civ-1553` |
| CIV-1554 | Oposición a la ejecución de título extrajudicial por compensación | `oposicion-ejecucion-titulo-extrajudicial-compensacion-civ-1554` |
| CIV-1555 | Recurso de reposición genérico contra resolución dictada en la ejecución | `recurso-reposicion-generico-contra-resolucion-dictada-civ-1555` |
| CIV-1556 | Acumulación de ejecuciones de títulos judiciales contra el mismo deudor ante distintos tribunales | `acumulacion-ejecuciones-titulos-judiciales-contra-civ-1556` |
| CIV-1557 | Demanda ejecutiva basada en título extrajudicial | `demanda-ejecutiva-basada-titulo-extrajudicial-civ-1557` |
| CIV-1558 | Oposición a la ejecución de título extrajudicial por defectos procesales (nulidad del despacho) | `oposicion-ejecucion-titulo-extrajudicial-defectos-civ-1558` |
| CIV-1559 | Demanda ejecutiva basada en título judicial | `demanda-ejecutiva-basada-titulo-judicial-civ-1559` |
| CIV-1560 | Oposición a ejecución de título extrajudicial por falta de capacidad o representación del ejecutante | `oposicion-ejecucion-titulo-extrajudicial-falta-civ-1560` |
| CIV-1561 | Impugnación del ejecutante a la oposición por motivos de fondo en ejecución de título judicial | `impugnacion-ejecutante-oposicion-motivos-fondo-civ-1561` |
| CIV-1562 | Oposición a la ejecución de resolución judicial por caducidad de la acción ejecutiva | `oposicion-ejecucion-resolucion-judicial-caducidad-civ-1562` |
| CIV-1563 | Oposición a la ejecución de resolución judicial por motivos de fondo (pago) | `oposicion-ejecucion-resolucion-judicial-motivos-fondo-civ-1563` |
| CIV-1564 | Recurso de apelación contra el auto que estima la oposición a la ejecución | `recurso-apelacion-contra-auto-estima-oposicion-civ-1564` |
| CIV-1565 | Oposición a actuaciones ejecutivas concretas por infracción de la ley | `oposicion-actuaciones-ejecutivas-concretas-infraccion-civ-1565` |
| CIV-1566 | Solicitud del demandado rebelde de suspender la ejecución si se estima la rescisión de la sentencia | `solicitud-demandado-rebelde-suspender-ejecucion-si-civ-1566` |
| CIV-1567 | Solicitud del demandado rebelde de suspensión de la ejecución | `solicitud-demandado-rebelde-suspension-ejecucion-civ-1567` |
| CIV-1568 | Demanda de ejecución provisional de sentencia de condena al pago de cantidad líquida | `demanda-ejecucion-provisional-sentencia-condena-pago-civ-1568` |
| CIV-1569 | Solicitud del ejecutado de suspender la ejecución por prejudicialidad penal | `solicitud-ejecutado-suspender-ejecucion-civ-1569` |
| CIV-1570 | Solicitud del ejecutado de suspender la ejecución por rescisión de sentencia dictada en rebeldía | `solicitud-ejecutado-suspender-ejecucion-rescision-civ-1570` |
| CIV-1571 | Escrito genérico que pide una actuación del tribunal en la ejecución | `escrito-generico-pide-actuacion-tribunal-ejecucion-civ-1571` |
| CIV-1572 | Recurso de reposición contra resolución de ejecución que contradice el título ejecutivo | `recurso-reposicion-contra-resolucion-ejecucion-civ-1572` |
| CIV-1573 | Impugnación de la oposición por el ejecutante ofreciendo caución | `impugnacion-oposicion-ejecutante-ofreciendo-caucion-civ-1573` |
| CIV-1574 | Oposición a la ejecución provisional de sentencia en materia de arrendamientos urbanos | `oposicion-ejecucion-provisional-sentencia-materia-civ-1574` |
| CIV-1575 | Demanda de ejecución provisional de sentencia en materia de arrendamientos | `demanda-ejecucion-provisional-sentencia-materia-civ-1575` |
| CIV-1576 | Solicitud de ejecución provisional de sentencia apelada | `solicitud-ejecucion-provisional-sentencia-apelada-civ-1576` |
| CIV-1577 | Personación ante la Audiencia en apelación pidiendo testimonio para la ejecución provisional | `personacion-ante-audiencia-apelacion-pidiendo-civ-1577` |
| CIV-1578 | Solicitud del ejecutante de embargo de garantías en ejecución no dineraria | `solicitud-ejecutante-embargo-garantias-ejecucion-no-civ-1578` |
| CIV-1579 | Demanda ejecutiva de sentencia firme de división de cosa común sobre finca rústica | `demanda-ejecutiva-sentencia-firme-division-cosa-comun-civ-1579` |
| CIV-1580 | Demanda ejecutiva de condena en sentencia con liquidación de intereses moratorios vencidos | `demanda-ejecutiva-condena-sentencia-liquidacion-civ-1580` |
| CIV-1581 | Impugnación por el demandado del cálculo de intereses del acreedor demandante | `impugnacion-demandado-calculo-intereses-acreedor-civ-1581` |
| CIV-1582 | Oposición a la demanda ejecutiva de condena en sentencia por indebido tipo de interés moratorio | `oposicion-demanda-ejecutiva-condena-sentencia-indebido-civ-1582` |
| CIV-1583 | Impugnación del ejecutante a la liquidación de intereses del ejecutado opuesto a la ejecución | `impugnacion-ejecutante-liquidacion-intereses-ejecutado-civ-1583` |
| CIV-1584 | Solicitud del acreedor de depósito del vehículo hipotecado tras despacharse ejecución | `solicitud-acreedor-deposito-vehiculo-hipotecado-tras-civ-1584` |
| CIV-1585 | Solicitud de medidas para hacer efectivo el embargo acordado | `solicitud-medidas-hacer-efectivo-embargo-acordado-civ-1585` |
| CIV-1586 | Solicitud de suspender la ejecución de laudo arbitral no firme por acción de anulación | `solicitud-suspender-ejecucion-laudo-arbitral-no-firme-civ-1586` |
| CIV-1587 | Escrito de oposición a la ejecución por pluspetición | `escrito-oposicion-ejecucion-pluspeticion-civ-1587` |
| CIV-1588 | Demanda ejecutiva de auto de cuantía máxima por seguro obligatorio, con bienes a embargar | `demanda-ejecutiva-auto-cuantia-maxima-seguro-civ-1588` |
| CIV-1589 | Oposición de la aseguradora obligatoria a la ejecución de auto de cuantía máxima por accidente | `oposicion-aseguradora-obligatoria-ejecucion-auto-civ-1589` |
| CIV-1590 | Declinatoria por falta de competencia territorial en la ejecución forzosa | `declinatoria-falta-competencia-territorial-ejecucion-civ-1590` |
| CIV-1591 | Solicitud de sobreseer la ejecución por estimarse la demanda de revisión de sentencia firme | `solicitud-sobreseer-ejecucion-estimarse-demanda-civ-1591` |
| CIV-1592 | Solicitud de suspensión de la ejecución por admisión de demanda de revisión de sentencia firme | `solicitud-suspension-ejecucion-admision-demanda-civ-1592` |
| CIV-1593 | Dictamen favorable del Fiscal a suspender la ejecución de la sentencia sometida a revisión | `dictamen-favorable-fiscal-suspender-ejecucion-civ-1593` |
| CIV-1594 | Solicitud de levantar la suspensión de la ejecución por desestimación de la demanda de revisión | `solicitud-levantar-suspension-ejecucion-desestimacion-civ-1594` |
| CIV-1595 | Dictamen contrario del Fiscal a suspender la ejecución de la sentencia sometida a revisión | `dictamen-contrario-fiscal-suspender-ejecucion-civ-1595` |
| CIV-1596 | Demanda de reconocimiento y ejecución en España de resolución extranjera con convenio | `demanda-reconocimiento-ejecucion-espana-resolucion-civ-1596` |
| CIV-1597 | Certificado de título ejecutivo europeo para transacción judicial aprobada | `certificado-titulo-ejecutivo-europeo-transaccion-civ-1597` |
| CIV-1598 | Certificado sustitutivo de título ejecutivo europeo emitido tras un recurso (art. 6.3) | `certificado-sustitutivo-titulo-ejecutivo-europeo-civ-1598` |
| CIV-1599 | Solicitud de rectificar o revocar el certificado de título ejecutivo europeo | `solicitud-rectificar-revocar-certificado-titulo-civ-1599` |
| CIV-1600 | Certificado de título ejecutivo europeo para resolución judicial | `certificado-titulo-ejecutivo-europeo-resolucion-civ-1600` |
| CIV-1601 | Certificado de falta o limitación de ejecutoriedad del título ejecutivo europeo | `certificado-falta-limitacion-ejecutoriedad-titulo-civ-1601` |
| CIV-1602 | Certificado de título ejecutivo europeo para instrumento auténtico | `certificado-titulo-ejecutivo-europeo-instrumento-civ-1602` |
| CIV-1603 | Alegaciones a la liquidación presentada por el titular de un crédito posterior | `alegaciones-liquidacion-presentada-titular-credito-civ-1603` |
| CIV-1604 | Demanda ejecutiva de costas tras sentencias absolutorias conformes en instancia y apelación | `demanda-ejecutiva-costas-tras-sentencias-absolutorias-civ-1604` |
| CIV-1605 | Demanda de ejecución de título judicial extranjero conforme al Reglamento (CE) 44 2001 | `demanda-ejecucion-titulo-judicial-extranjero-conforme-civ-1605` |
| CIV-1606 | Solicitud del ejecutante de mandamiento conforme al artículo 144 de la Ley Hipotecaria | `solicitud-ejecutante-mandamiento-conforme-articulo-144-civ-1606` |
| CIV-1607 | Solicitud de liquidar intereses al confirmarse en apelación la condena consignada por la aseguradora | `solicitud-liquidar-intereses-confirmarse-apelacion-civ-1607` |
| CIV-1608 | Escrito del tercer poseedor pidiendo que se le exhiban los autos de ejecución | `escrito-tercer-poseedor-pidiendo-le-exhiban-autos-civ-1608` |
| CIV-1609 | Escrito del ejecutado que se opone a la ejecución hipotecaria y pide su suspensión | `escrito-ejecutado-opone-ejecucion-hipotecaria-pide-civ-1609` |
| CIV-1610 | Escrito del deudor que consigna principal e intereses para liberar el bien | `escrito-deudor-consigna-principal-e-intereses-liberar-civ-1610` |
| CIV-1611 | Demanda de ejecución hipotecaria sobre la vivienda habitual del deudor - variante 2 | `demanda-ejecucion-hipotecaria-sobre-vivienda-habitual-civ-1611` |
| CIV-1612 | Escrito pidiendo notificar la ejecución hipotecaria al último titular registral de dominio | `escrito-pidiendo-notificar-ejecucion-hipotecaria-civ-1612` |
| CIV-1613 | Escrito del ejecutante hipotecario pidiendo declarar que el ocupante de la finca no puede permanecer | `escrito-ejecutante-hipotecario-pidiendo-declarar-civ-1613` |
| CIV-1614 | Escrito que identifica a un ocupante distinto del ejecutado y pide declarar que no puede permanecer | `escrito-identifica-ocupante-distinto-ejecutado-pide-civ-1614` |
| CIV-1615 | Acta de la diligencia de embargo de bienes del ejecutado por la comisión judicial | `acta-diligencia-embargo-bienes-ejecutado-comision-civ-1615` |
| CIV-1616 | Escrito del demandante pidiendo mantener el lanzamiento pese al desalojo voluntario del ocupante | `escrito-demandante-pidiendo-mantener-lanzamiento-pese-civ-1616` |
| CIV-1617 | Escrito de impugnación de la tasación de costas por honorarios indebidos | `escrito-impugnacion-tasacion-costas-honorarios-civ-1617` |
| CIV-1618 | Demanda ejecutiva basada en auto de cuantía máxima por el seguro obligatorio de vehículos de motor | `demanda-ejecutiva-basada-auto-cuantia-maxima-seguro-civ-1618` |
| CIV-1619 | Escrito del ejecutado pidiendo reducir el embargo | `escrito-ejecutado-pidiendo-reducir-embargo-civ-1619` |
| CIV-1620 | Escrito del ejecutante mercantil que impugna la oposición al embargo en ejecución provisional | `escrito-ejecutante-mercantil-impugna-oposicion-embargo-civ-1620` |
| CIV-1621 | Oposición al embargo en ejecución provisional por inactividad real de la empresa ejecutante | `oposicion-embargo-ejecucion-provisional-inactividad-civ-1621` |
| CIV-1622 | Contestación a tercería de dominio alegando abuso de personalidad jurídica y fraude de acreedores | `contestacion-terceria-dominio-alegando-abuso-civ-1622` |
| CIV-1623 | Demanda de tercería de mejor derecho de acreedores laborales frente a la Seguridad Social en apremio | `demanda-terceria-mejor-derecho-acreedores-laborales-civ-1623` |
| CIV-1624 | Escrito pidiendo ejecutar lo convenido en la conciliación (general) | `escrito-pidiendo-ejecutar-lo-convenido-conciliacion-civ-1624` |
| CIV-1625 | Demanda de ejecución provisional con indicación de los bienes sobre los que trabar embargo | `demanda-ejecucion-provisional-indicacion-bienes-sobre-civ-1625` |
| CIV-1626 | Demanda de ejecución provisional sin conocer bienes sobre los que trabar embargo | `demanda-ejecucion-provisional-sin-conocer-bienes-sobre-civ-1626` |
| CIV-1627 | Escrito del ejecutado que presenta a un tercero para mejorar la postura de la subasta ya celebrada | `escrito-ejecutado-presenta-tercero-mejorar-postura-civ-1627` |
| CIV-1628 | Escrito impugnando la cuenta final justificada del administrador judicial en la ejecución | `escrito-impugnando-cuenta-final-justificada-civ-1628` |
| CIV-1629 | Escrito del reembargante pidiendo la realización forzosa de los bienes si se alza el embargo previo | `escrito-reembargante-pidiendo-realizacion-forzosa-civ-1629` |
| CIV-1630 | Escrito pidiendo el embargo del sobrante de la realización de bienes en otro procedimiento | `escrito-pidiendo-embargo-sobrante-realizacion-bienes-civ-1630` |
| CIV-1631 | Escrito del reembargante pidiendo la realización forzosa aunque subsista el embargo anterior | `escrito-reembargante-pidiendo-realizacion-forzosa-civ-1631` |
| CIV-1632 | Escrito del ejecutado que aporta un tercero dispuesto a mejorar la postura | `escrito-ejecutado-aporta-tercero-dispuesto-mejorar-civ-1632` |
| CIV-1633 | Escrito del ejecutante pidiendo alzar la suspensión y sacar los bienes a subasta | `escrito-ejecutante-pidiendo-alzar-suspension-sacar-civ-1633` |
| CIV-1634 | Escrito pidiendo mayor publicidad de la subasta de bienes inmuebles | `escrito-pidiendo-mayor-publicidad-subasta-bienes-civ-1634` |
| CIV-1635 | Escrito del ejecutante pidiendo apremiar al ejecutado para que aporte los títulos de propiedad | `escrito-ejecutante-pidiendo-apremiar-ejecutado-aporte-civ-1635` |
| CIV-1636 | Escrito del ejecutante pidiendo subasta sin suplir previamente la falta de títulos de propiedad | `escrito-ejecutante-pidiendo-subasta-sin-suplir-civ-1636` |
| CIV-1637 | Escrito pidiendo declarar que los ocupantes no tienen derecho a permanecer en el inmueble enajenado | `escrito-pidiendo-declarar-ocupantes-no-tienen-derecho-civ-1637` |
| CIV-1638 | Escrito del ejecutante pidiendo señalar subasta de bienes muebles embargados | `escrito-ejecutante-pidiendo-senalar-subasta-bienes-civ-1638` |
| CIV-1639 | Escrito pidiendo mayor publicidad de la subasta de bienes muebles | `escrito-pidiendo-mayor-publicidad-subasta-bienes-civ-1639` |
| CIV-1640 | Escrito pidiendo deshacer lo hecho e indemnizar al ejecutado tras sentencia revocatoria | `escrito-pidiendo-deshacer-lo-hecho-e-indemnizar-civ-1640` |
| CIV-1641 | Escrito del ejecutado pidiendo la restitución del bien entregado tras sentencia revocatoria | `escrito-ejecutado-pidiendo-restitucion-bien-entregado-civ-1641` |
| CIV-1642 | Demanda de tercería de mejor derecho en el orden civil | `demanda-terceria-mejor-derecho-orden-civil-civ-1642` |
| CIV-1643 | Escrito del ejecutante conforme con no trabar un bien que pertenece a un tercero | `escrito-ejecutante-conforme-no-trabar-bien-pertenece-civ-1643` |
| CIV-1644 | Escrito de un tercero que se opone al embargo de bienes de su propiedad | `escrito-tercero-opone-embargo-bienes-propiedad-civ-1644` |
| CIV-1645 | Escrito del ejecutante pidiendo mejora de embargo por insuficiencia de los bienes trabados | `escrito-ejecutante-pidiendo-mejora-embargo-civ-1645` |
| CIV-1646 | Escrito pidiendo investigar el patrimonio del ejecutado mediante oficio a una entidad | `escrito-pidiendo-investigar-patrimonio-ejecutado-civ-1646` |
| CIV-1647 | Escrito pidiendo suspender la ejecución por haberse admitido la rescisión de sentencia firme | `escrito-pidiendo-suspender-ejecucion-haberse-admitido-civ-1647` |
| CIV-1648 | Escrito de oposición por motivos de fondo a la ejecución de sentencia firme de condena | `escrito-oposicion-motivos-fondo-ejecucion-sentencia-civ-1648` |
| CIV-1649 | Escrito de oposición por motivos de fondo a la ejecución de una póliza de contrato mercantil | `escrito-oposicion-motivos-fondo-ejecucion-poliza-civ-1649` |
| CIV-1650 | Escrito impugnando la oposición a la ejecución por motivos de fondo | `escrito-impugnando-oposicion-ejecucion-motivos-fondo-civ-1650` |
| CIV-1651 | Escrito de oposición por defecto procesal a la ejecución de sentencia firme de condena | `escrito-oposicion-defecto-procesal-ejecucion-sentencia-civ-1651` |
| CIV-1652 | Escrito de oposición por defecto procesal a la ejecución de póliza de contrato mercantil | `escrito-oposicion-defecto-procesal-ejecucion-poliza-civ-1652` |
| CIV-1653 | Escrito del ejecutante que contesta a la oposición basada en defecto procesal | `escrito-ejecutante-contesta-oposicion-basada-defecto-civ-1653` |
| CIV-1654 | Demanda ejecutiva basada en sentencia firme ante el tribunal competente para la ejecución | `demanda-ejecutiva-basada-sentencia-firme-ante-tribunal-civ-1654` |
| CIV-1655 | Demanda ejecutiva por reclamación de cantidad basada en sentencia de condena firme | `demanda-ejecutiva-reclamacion-cantidad-basada-civ-1655` |
| CIV-1656 | Demanda ejecutiva por cantidad con responsabilidad de bienes gananciales | `demanda-ejecutiva-cantidad-responsabilidad-bienes-civ-1656` |
| CIV-1657 | Escrito del ejecutante contestando a la oposición a la ejecución provisional por infracción procesal | `escrito-ejecutante-contestando-oposicion-ejecucion-civ-1657` |
| CIV-1658 | Oposición a la ejecución provisional no dineraria por difícil restauración si se revoca la sentencia | `oposicion-ejecucion-provisional-no-dineraria-dificil-civ-1658` |
| CIV-1659 | Escrito de oposición a la ejecución provisional solicitada tras remitirse los autos a la Audiencia | `escrito-oposicion-ejecucion-provisional-solicitada-civ-1659` |
| CIV-1660 | Escrito del ejecutante pidiendo mandamiento al Registro de la Propiedad para anotar el embargo | `escrito-ejecutante-pidiendo-mandamiento-registro-civ-1660` |
| CIV-1661 | Demanda ejecutiva basada en título que obliga a no hacer (art. 711 LEC) | `demanda-ejecutiva-basada-titulo-obliga-no-hacer-art-civ-1661` |
| CIV-1662 | Escrito del ejecutado que expone por qué se niega a hacer lo que dispone el título | `escrito-ejecutado-expone-niega-hacer-lo-dispone-titulo-civ-1662` |
| CIV-1663 | Escrito del ejecutante pidiendo apremiar con multas al ejecutado | `escrito-ejecutante-pidiendo-apremiar-multas-ejecutado-civ-1663` |
| CIV-1664 | Demanda ejecutiva basada en título que obliga a un hacer personalísimo (art. 709 LEC) | `demanda-ejecutiva-basada-titulo-obliga-hacer-civ-1664` |
| CIV-1665 | Escrito pidiendo requerir a los titulares de créditos posteriores que acrediten su subsistencia | `escrito-pidiendo-requerir-titulares-creditos-civ-1665` |
| CIV-1666 | Escrito del ocupante del inmueble embargado que comunica al tribunal la existencia de ocupantes | `escrito-ocupante-inmueble-embargado-comunica-tribunal-civ-1666` |
| CIV-1667 | Escrito del ejecutante pidiendo la posesión de los bienes embargados para administrarlos | `escrito-ejecutante-pidiendo-posesion-bienes-embargados-civ-1667` |
| CIV-1668 | Demanda ejecutiva basada en título que obliga a entregar bienes inmuebles (art. 703 LEC) | `demanda-ejecutiva-basada-titulo-obliga-entregar-bienes-civ-1668` |
| CIV-1669 | Demanda ejecutiva basada en título que obliga a un hacer no personalísimo (art. 705 LEC) | `demanda-ejecutiva-basada-titulo-obliga-hacer-no-civ-1669` |
| CIV-1670 | Escrito del ejecutante que opta por la indemnización de daños en lugar del hacer no personalísimo | `escrito-ejecutante-opta-indemnizacion-danos-lugar-civ-1670` |
| CIV-1671 | Demanda ejecutiva basada en título que obliga a entregar una cosa mueble cierta y determinada | `demanda-ejecutiva-basada-titulo-obliga-entregar-cosa-civ-1671` |
| CIV-1672 | Demanda ejecutiva basada en título que obliga a entregar cosas genéricas o indeterminadas | `demanda-ejecutiva-basada-titulo-obliga-entregar-cosas-civ-1672` |
| CIV-1673 | Escrito del ejecutante que contesta a las alegaciones del ejecutado y pide aprobar las cuentas | `escrito-ejecutante-contesta-alegaciones-ejecutado-pide-civ-1673` |
| CIV-1674 | Escrito pidiendo multas coercitivas al ejecutado que obstaculiza la administración para pago | `escrito-pidiendo-multas-coercitivas-ejecutado-civ-1674` |
| CIV-1675 | Solicitud de embargo de gananciales contra un cónyuge por deuda consorcial extracontractual | `solicitud-embargo-gananciales-contra-conyuge-deuda-civ-1675` |
| CIV-1676 | Solicitud de embargo de gananciales contra un cónyuge por deuda privativa anterior al matrimonio | `solicitud-embargo-gananciales-contra-conyuge-deuda-civ-1676` |
| CIV-1677 | Escrito del cónyuge no ejecutado oponiéndose al embargo de ganancial por ser privativa la deuda | `escrito-conyuge-no-ejecutado-oponiendose-embargo-civ-1677` |
| CIV-1678 | Escrito pidiendo ampliar la ejecución a nuevos plazos vencidos | `escrito-pidiendo-ampliar-ejecucion-nuevos-plazos-civ-1678` |
| CIV-1679 | Escrito pidiendo acumular ejecuciones de sentencias contra un mismo deudor ante distintos tribunales | `escrito-pidiendo-acumular-ejecuciones-sentencias-civ-1679` |
| CIV-1680 | Escrito pidiendo acumular ejecuciones de títulos extrajudiciales entre las mismas partes | `escrito-pidiendo-acumular-ejecuciones-titulos-civ-1680` |
| CIV-1681 | Escrito pidiendo fijar el equivalente pecuniario de una prestación no dineraria | `escrito-pidiendo-fijar-equivalente-pecuniario-civ-1681` |
| CIV-1682 | Escrito pidiendo acumular ejecuciones de monitorios entre las mismas partes ante el mismo tribunal | `escrito-pidiendo-acumular-ejecuciones-monitorios-entre-civ-1682` |
| CIV-1683 | Escrito del cónyuge no deudor que ejerce la opción ante el embargo de gananciales (art. 541.3 LEC) | `escrito-conyuge-no-deudor-ejerce-opcion-ante-embargo-civ-1683` |
| CIV-1684 | Oposición del cónyuge no ejecutado al embargo de gananciales por existir bienes privativos | `oposicion-conyuge-no-ejecutado-embargo-gananciales-civ-1684` |
| CIV-1685 | Escrito del ejecutante provisional oponiéndose a la liquidación de daños tras revocarse la sentencia | `escrito-ejecutante-provisional-oponiendose-liquidacion-civ-1685` |
| CIV-1686 | Escrito del ejecutado pidiendo sobreseer la ejecución provisional, devolución de lo cobrado y daños | `escrito-ejecutado-pidiendo-sobreseer-ejecucion-civ-1686` |
| CIV-1687 | Escrito del adquirente en subasta pidiendo posesión de inmueble con ocupante declarado sin derecho | `escrito-adquirente-subasta-pidiendo-posesion-inmueble-civ-1687` |
| CIV-1688 | Escrito del ejecutante adjudicatario pidiendo el lanzamiento de un ocupante no declarado sin derecho | `escrito-ejecutante-adjudicatario-pidiendo-lanzamiento-civ-1688` |
| CIV-1689 | Demanda de ejecución provisional de sentencia dictada en segunda instancia (arts. 535 a 537 LEC) | `demanda-ejecucion-provisional-sentencia-dictada-civ-1689` |
| CIV-1690 | Demanda de ejecución provisional de sentencia de condena no dineraria | `demanda-ejecucion-provisional-sentencia-condena-no-civ-1690` |
| CIV-1691 | Demanda de tercería de dominio sobre inmueble aportado a una sociedad sin inscribir en el Registro | `demanda-terceria-dominio-sobre-inmueble-aportado-civ-1691` |
| CIV-1692 | Escrito del deudor que presenta la liquidación de frutos y rentas | `escrito-deudor-presenta-liquidacion-frutos-rentas-civ-1692` |
| CIV-1693 | Escrito pidiendo fijar la cantidad debida por frutos, rentas, utilidades o productos | `escrito-pidiendo-fijar-cantidad-debida-frutos-rentas-civ-1693` |
| CIV-1694 | Escrito del deudor conforme con la relación de daños y perjuicios | `escrito-deudor-conforme-relacion-danos-perjuicios-civ-1694` |
| CIV-1695 | Demanda de tercería de dominio contra embargo preventivo de finca recibida en dación sin escritura | `demanda-terceria-dominio-contra-embargo-preventivo-civ-1695` |
| CIV-1696 | Escrito pidiendo que los bienes embargados los realice una persona o entidad especializada | `escrito-pidiendo-bienes-embargados-realice-persona-civ-1696` |
| CIV-1697 | Escrito del rematante pidiendo lanzar a los ocupantes del inmueble subastado | `escrito-rematante-pidiendo-lanzar-ocupantes-inmueble-civ-1697` |
| CIV-1698 | Escrito del ejecutante pidiendo ser facultado para adquirir la cosa debida a costa del ejecutado | `escrito-ejecutante-pidiendo-ser-facultado-adquirir-civ-1698` |
| CIV-1699 | Escrito designando bienes a embargar y pidiendo despacho de ejecución tras el monitorio | `escrito-designando-bienes-embargar-pidiendo-despacho-civ-1699` |
| CIV-1700 | Escrito del ejecutado que se opone al allanamiento del ejecutante a la tercería | `escrito-ejecutado-opone-allanamiento-ejecutante-civ-1700` |
| CIV-1701 | Escrito pidiendo suspender la ejecución provisional tras consignar judicialmente lo reclamado | `escrito-pidiendo-suspender-ejecucion-provisional-tras-civ-1701` |
| CIV-1702 | Escrito del ejecutante contestando a la oposición a ejecución provisional por difícil restauración | `escrito-ejecutante-contestando-oposicion-ejecucion-civ-1702` |
| CIV-1703 | Escrito de oposición a una actuación concreta de la ejecución provisional dineraria | `escrito-oposicion-actuacion-concreta-ejecucion-civ-1703` |
| CIV-1704 | Escrito del ejecutante contestando a la oposición a una actuación concreta en ejecución provisional | `escrito-ejecutante-contestando-oposicion-actuacion-civ-1704` |

## Privacidad

Ver `PRIVACY.md`.
