# Ejecución de sentencias y embargos

> Plugin de Claude Code `formularios-ejecucion-y-embargos` · **193 formularios** · Civil · normativa revisada el 25-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Para ejecutar lo ganado: demanda ejecutiva (título judicial, no judicial, laudo, acuerdo de mediación), ejecución provisional, embargo y mejora de embargo, averiguación patrimonial, subasta, lanzamiento, ejecución hipotecaria, tercerías, oposición del ejecutado y liquidación de intereses y costas.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva; el formulario seco, listo para rellenar, está en `assets/formulario.md` dentro de la carpeta de la skill.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 193 está al final):

- **Demandas, peticiones y solicitudes iniciales** (62). Por ejemplo: Demanda ejecutiva de sentencia extranjera conforme al Reglamento (UE) nº 1215-2012; Demanda ejecutiva de sentencia firme que anula la cláusula suelo y ordena devolver cantidades; Demanda ejecutiva basada en auto que homologa una transacción judicial.
- **Contestaciones, oposiciones y alegaciones** (5). Por ejemplo: Alegaciones del ejecutante en el incidente de abusividad apreciada de oficio; Alegaciones del ejecutante sobre la limitación de los intereses de demora; Alegaciones de las partes sobre la formación de lotes en la ejecución.
- **Recursos** (1). Por ejemplo: Apelación contra el auto que deniega ejecutar un laudo arbitral en materia de arrendamientos.
- **Contratos, pactos y cláusulas** (1). Por ejemplo: Acuerdo de mediación alcanzado durante la ejecución de una sentencia.
- **Estatutos, actas, certificaciones y escrituras** (5). Por ejemplo: Certificado de título ejecutivo europeo para transacción judicial aprobada; Certificado de título ejecutivo europeo para resolución judicial; Certificado de falta o limitación de ejecutoriedad del título ejecutivo europeo.
- **Comunicaciones, requerimientos y cartas** (17). Por ejemplo: Solicitud conjunta de suspender el proceso de ejecución para intentar una mediación; Solicitud del ejecutante de autorización para publicar la sentencia en medios a costa del ejecutado; Declaración de gasto extraordinario previa a la ejecución por el carné de ciclomotor del hijo.
- **Escritos de trámite y otros** (102). Por ejemplo: Declinatoria por falta de competencia territorial en la ejecución de un acuerdo de mediación; Escrito de allanamiento en un juicio ejecutivo sobre un automóvil; Escrito del ejecutante pidiendo nuevas averiguaciones sobre el patrimonio del ejecutado.

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
4. Aplica las notas de actualización de la revisión del 25-11-2026 (reformas legales, órganos judiciales de la LO 1/2025, plazos).
5. Comprueba en el BOE, con Jurisprudenciator, cada norma que cita el documento; si alguna ha cambiado, usa la redacción vigente y te lo dice.
6. Te entrega el documento en Word **tal cual es el formulario**: empieza por su primera línea, sin títulos, notas ni explicaciones añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. En el chat te dice lo que queda pendiente y, si es un escrito, el plazo y ante quién se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.

## Antes de empezar

- **Dónde funciona:** en Claude Code y en Claude (web, escritorio y Cowork). Se instala desde este repositorio de GitHub o subiendo el ZIP del plugin.
- **Jurisprudenciator es imprescindible:** el plugin trae el conector y cada skill trabaja siempre con él. Sin una cuenta de Jurisprudenciator conectada, las skills se paran y no redactan nada. La primera vez hay que iniciar sesión (en Claude Code, con `/mcp`; o con tu URL personal: https://jurisprudenciator.lexiaipro.org/instalacion). Si ya tienes Jurisprudenciator conectado en Claude, las skills usan ese.
- **Espacio que ocupa:** unos 11.868 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-ejecucion-y-embargos@formularios-juridicos-civil-espana`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-civil-espana
/plugin install formularios-ejecucion-y-embargos@formularios-juridicos-civil-espana
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-civil-espana`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-ejecucion-y-embargos.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (193)

| Código | Formulario | Skill |
|---|---|---|
| CIV-1394 | Demanda ejecutiva de sentencia extranjera conforme al Reglamento (UE) nº 1215-2012 | `demanda-ejecutiva-sentencia-extranjera-conforme-civ-1394` |
| CIV-1396 | Demanda ejecutiva de sentencia firme que anula la cláusula suelo y ordena devolver cantidades | `demanda-ejecutiva-sentencia-firme-anula-clausula-suelo-civ-1396` |
| CIV-1397 | Demanda ejecutiva basada en auto que homologa una transacción judicial | `demanda-ejecutiva-basada-auto-homologa-transaccion-civ-1397` |
| CIV-1400 | Demanda ejecutiva de sentencia firme contra los herederos del condenado fallecido | `demanda-ejecutiva-sentencia-firme-contra-herederos-civ-1400` |
| CIV-1401 | Demanda ejecutiva basada en una póliza de contrato mercantil por cuotas impagadas | `demanda-ejecutiva-basada-poliza-contrato-mercantil-civ-1401` |
| CIV-1402 | Acuerdo de mediación alcanzado durante la ejecución de una sentencia | `acuerdo-mediacion-alcanzado-durante-ejecucion-sentencia-civ-1402` |
| CIV-1406 | Solicitud conjunta de suspender el proceso de ejecución para intentar una mediación | `solicitud-conjunta-suspender-proceso-ejecucion-civ-1406` |
| CIV-1407 | Declinatoria por falta de competencia territorial en la ejecución de un acuerdo de mediación | `declinatoria-falta-competencia-territorial-ejecucion-civ-1407` |
| CIV-1408 | Escrito de allanamiento en un juicio ejecutivo sobre un automóvil | `escrito-allanamiento-juicio-ejecutivo-sobre-automovil-civ-1408` |
| CIV-1410 | Escrito del ejecutante pidiendo nuevas averiguaciones sobre el patrimonio del ejecutado | `escrito-ejecutante-pidiendo-nuevas-averiguaciones-civ-1410` |
| CIV-1411 | Escrito del ejecutado manifestando los bienes de su titularidad que pueden embargarse | `escrito-ejecutado-manifestando-bienes-titularidad-civ-1411` |
| CIV-1418 | Demanda ejecutiva de título judicial con condena dineraria y de hacer no personalísimo | `demanda-ejecutiva-titulo-judicial-condena-dineraria-civ-1418` |
| CIV-1422 | Alegaciones del ejecutante en el incidente de abusividad apreciada de oficio | `alegaciones-ejecutante-incidente-abusividad-apreciada-civ-1422` |
| CIV-1424 | Escrito del ejecutado pidiendo recalcular los intereses de demora (Disp Trans 2ª Ley 1-2013) | `escrito-ejecutado-pidiendo-recalcular-intereses-demora-civ-1424` |
| CIV-1430 | Alegaciones del ejecutante sobre la limitación de los intereses de demora | `alegaciones-ejecutante-sobre-limitacion-intereses-civ-1430` |
| CIV-1439 | Solicitud del ejecutante de autorización para publicar la sentencia en medios a costa del ejecutado | `solicitud-ejecutante-autorizacion-publicar-sentencia-civ-1439` |
| CIV-1440 | Demanda ejecutiva basada en un acuerdo de mediación elevado a escritura pública | `demanda-ejecutiva-basada-acuerdo-mediacion-elevado-civ-1440` |
| CIV-1441 | Demanda ejecutiva para ejecutar la condena a publicar la sentencia | `demanda-ejecutiva-ejecutar-condena-publicar-sentencia-civ-1441` |
| CIV-1442 | Escrito de petición de embargo de bienes del ejecutado tras la averiguación patrimonial | `escrito-peticion-embargo-bienes-ejecutado-tras-civ-1442` |
| CIV-1443 | Escrito de tasación de costas del abogado que se defiende a sí mismo como parte demandante | `escrito-tasacion-costas-abogado-defiende-si-mismo-como-civ-1443` |
| CIV-1445 | Escrito de solicitud de ejecución provisional de sentencia | `escrito-solicitud-ejecucion-provisional-sentencia-civ-1445` |
| CIV-1448 | Escrito de tercero para evitar el embargo de su vivienda habitual | `escrito-tercero-evitar-embargo-vivienda-habitual-civ-1448` |
| CIV-1449 | Escrito del ejecutante que acepta no embargar un bien privativo del cónyuge del ejecutado | `escrito-ejecutante-acepta-no-embargar-bien-privativo-civ-1449` |
| CIV-1450 | Demanda ejecutiva para actualizar la pensión de alimentos | `demanda-ejecutiva-actualizar-pension-alimentos-civ-1450` |
| CIV-1451 | Demanda de ejecución provisional para cobrar la pensión compensatoria fijada en sentencia | `demanda-ejecucion-provisional-cobrar-pension-civ-1451` |
| CIV-1453 | Escrito de ampliación de la demanda ejecutiva por incumplimiento reiterado del régimen de visitas | `escrito-ampliacion-demanda-ejecutiva-incumplimiento-civ-1453` |
| CIV-1455 | Escrito para notificar al cónyuge del deudor el embargo ganancial y anotarlo en el Registro | `escrito-notificar-conyuge-deudor-embargo-ganancial-civ-1455` |
| CIV-1457 | Escrito del cónyuge que ejercita la opción disolutoria ante el embargo de bienes agermanados | `escrito-conyuge-ejercita-opcion-disolutoria-ante-civ-1457` |
| CIV-1459 | Escrito para notificar al cónyuge el embargo de posible vivienda familiar y anotarlo en el Registro | `escrito-notificar-conyuge-embargo-posible-vivienda-civ-1459` |
| CIV-1460 | Demanda de ejecución forzosa del auto de medidas provisionales previas | `demanda-ejecucion-forzosa-auto-medidas-provisionales-civ-1460` |
| CIV-1461 | Demanda ejecutiva para que el cónyuge sin uso de la vivienda familiar arrendada la abandone | `demanda-ejecutiva-conyuge-sin-uso-vivienda-familiar-civ-1461` |
| CIV-1462 | Demanda de ejecución por impago de la compensación económica (art. 232.5 CCCat) | `demanda-ejecucion-impago-compensacion-economica-art-civ-1462` |
| CIV-1463 | Declaración de gasto extraordinario previa a la ejecución por el carné de ciclomotor del hijo | `declaracion-gasto-extraordinario-previa-ejecucion-civ-1463` |
| CIV-1464 | Demanda ejecutiva basada en el auto que homologa un acuerdo de mediación | `demanda-ejecutiva-basada-auto-homologa-acuerdo-civ-1464` |
| CIV-1465 | Declinatoria por falta de competencia territorial en la ejecución de un acuerdo de media - variante 2 | `declinatoria-falta-competencia-territorial-ejecucion-civ-1465` |
| CIV-1466 | Demanda ejecutiva basada en aval bancario de la Ley 57 de 1968 sobre cantidades anticipadas | `demanda-ejecutiva-basada-aval-bancario-ley-57-1968-civ-1466` |
| CIV-1469 | Demanda ejecutiva de un acuerdo de mediación sobre alimentos del hijo mayor de edad (Ley 5 de 2012) | `demanda-ejecutiva-acuerdo-mediacion-sobre-alimentos-civ-1469` |
| CIV-1470 | Escrito pidiendo certificación de dominio y cargas en el procedimiento ejecutivo | `escrito-pidiendo-certificacion-dominio-cargas-civ-1470` |
| CIV-1471 | Escrito del ejecutante pidiendo mejorar el embargo por pensiones alimenticias o compensatorias | `escrito-ejecutante-pidiendo-mejorar-embargo-pensiones-civ-1471` |
| CIV-1472 | Escrito del ejecutante pidiendo el nombramiento de perito tasador | `escrito-ejecutante-pidiendo-nombramiento-perito-tasador-civ-1472` |
| CIV-1474 | Escrito de manifestación de bienes del ejecutado | `escrito-manifestacion-bienes-ejecutado-civ-1474` |
| CIV-1475 | Demanda de ejecución provisional de una medida definitiva sobre régimen de visitas | `demanda-ejecucion-provisional-medida-definitiva-sobre-civ-1475` |
| CIV-1477 | Demanda ejecutiva por rentas y cantidades fijadas en sentencia de juicio verbal de desahucio | `demanda-ejecutiva-rentas-cantidades-fijadas-sentencia-civ-1477` |
| CIV-1478 | Solicitud de que se despache ejecución tras el decreto que termina el juicio de desahucio | `solicitud-despache-ejecucion-tras-decreto-termina-civ-1478` |
| CIV-1483 | Escrito del procurador pidiendo ser facultado para obtener la certificación de dominio y cargas | `escrito-procurador-pidiendo-ser-facultado-obtener-civ-1483` |
| CIV-1486 | Demanda de ejecución de un laudo arbitral de consumo | `demanda-ejecucion-laudo-arbitral-consumo-civ-1486` |
| CIV-1488 | Escrito del ejecutante pidiendo el cambio de depositario | `escrito-ejecutante-pidiendo-cambio-depositario-civ-1488` |
| CIV-1490 | Demanda ejecutiva no dineraria de sentencia firme de desahucio | `demanda-ejecutiva-no-dineraria-sentencia-firme-civ-1490` |
| CIV-1494 | Demanda ejecutiva de sentencia que condena a emitir una declaración de voluntad | `demanda-ejecutiva-sentencia-condena-emitir-declaracion-civ-1494` |
| CIV-1495 | Demanda ejecutiva basada en escritura pública de préstamo | `demanda-ejecutiva-basada-escritura-publica-prestamo-civ-1495` |
| CIV-1496 | Solicitud de ejecución de la sentencia dictada en un juicio de desahucio | `solicitud-ejecucion-sentencia-dictada-juicio-desahucio-civ-1496` |
| CIV-1498 | Demanda ejecutiva de laudo arbitral de desahucio | `demanda-ejecutiva-laudo-arbitral-desahucio-civ-1498` |
| CIV-1503 | Demanda ejecutiva dineraria de un laudo arbitral | `demanda-ejecutiva-dineraria-laudo-arbitral-civ-1503` |
| CIV-1504 | Apelación contra el auto que deniega ejecutar un laudo arbitral en materia de arrendamientos | `apelacion-contra-auto-deniega-ejecutar-laudo-arbitral-civ-1504` |
| CIV-1508 | Demanda ejecutiva para cumplir la condena de otorgar escritura pública | `demanda-ejecutiva-cumplir-condena-otorgar-escritura-civ-1508` |
| CIV-1511 | Ejecución forzosa con multas coercitivas al progenitor custodio que incumple las visitas | `ejecucion-forzosa-multas-coercitivas-progenitor-civ-1511` |
| CIV-1512 | Demanda de ejecución de póliza de crédito garantizada con prenda de acciones cotizadas | `demanda-ejecucion-poliza-credito-garantizada-prenda-civ-1512` |
| CIV-1513 | Escrito pidiendo el embargo del sueldo del deudor | `escrito-pidiendo-embargo-sueldo-deudor-civ-1513` |
| CIV-1515 | Solicitud de multas coercitivas por incumplimiento de una medida de un proceso matrimonial | `solicitud-multas-coercitivas-incumplimiento-medida-civ-1515` |
| CIV-1516 | Escrito para declarar extraordinario un gasto no previsto en las medidas a efectos de ejecución | `escrito-declarar-extraordinario-gasto-no-previsto-civ-1516` |
| CIV-1517 | Demanda ejecutiva de gastos extraordinarios no previstos en la resolución judicial | `demanda-ejecutiva-gastos-extraordinarios-no-previstos-civ-1517` |
| CIV-1518 | Consignación del deudor por vencimiento anticipado en ejecución sobre la vivienda familiar | `consignacion-deudor-vencimiento-anticipado-ejecucion-civ-1518` |
| CIV-1519 | Escrito del ejecutado pidiendo suspender la ejecución provisional de una condena dineraria | `escrito-ejecutado-pidiendo-suspender-ejecucion-civ-1519` |
| CIV-1522 | Escrito del ejecutado pidiendo suspender la ejecución por encontrarse en situación concursal | `escrito-ejecutado-pidiendo-suspender-ejecucion-civ-1522` |
| CIV-1523 | Escrito del ejecutante pidiendo el reembargo de un bien | `escrito-ejecutante-pidiendo-reembargo-bien-civ-1523` |
| CIV-1525 | Escrito del ejecutante pidiendo nombrar depositario de un bien embargado | `escrito-ejecutante-pidiendo-nombrar-depositario-bien-civ-1525` |
| CIV-1531 | Demanda ejecutiva para reclamar deudas garantizadas con prenda | `demanda-ejecutiva-reclamar-deudas-garantizadas-prenda-civ-1531` |
| CIV-1533 | Escrito del ejecutado que pide el cese de la administración judicial por mala gestión del ejecutante | `escrito-ejecutado-pide-cese-administracion-judicial-civ-1533` |
| CIV-1537 | Escrito del ejecutado que pide anular el embargo de un bien inembargable | `escrito-ejecutado-pide-anular-embargo-bien-inembargable-civ-1537` |
| CIV-1538 | Alegaciones de las partes sobre la formación de lotes en la ejecución | `alegaciones-partes-sobre-formacion-lotes-ejecucion-civ-1538` |
| CIV-1540 | Escrito del ejecutante que pide liquidar detalladamente daños y perjuicios (arts. 713 y ss. LEC) | `escrito-ejecutante-pide-liquidar-detalladamente-danos-civ-1540` |
| CIV-1543 | Solicitud del acreedor para que se fije la cantidad debida en concepto de frutos y rentas | `solicitud-acreedor-fije-cantidad-debida-concepto-civ-1543` |
| CIV-1545 | Solicitud del ejecutante de auto que tenga por emitida la declaración de voluntad del ejecutado | `solicitud-ejecutante-auto-tenga-emitida-declaracion-civ-1545` |
| CIV-1548 | Recusación por el ejecutado del perito nombrado durante la ejecución | `recusacion-ejecutado-perito-nombrado-durante-ejecucion-civ-1548` |
| CIV-1549 | Escrito conjunto de ejecutante y ejecutado que acuerdan la valoración del bien embargado | `escrito-conjunto-ejecutante-ejecutado-acuerdan-civ-1549` |
| CIV-1556 | Acumulación de ejecuciones de títulos judiciales contra el mismo deudor ante distintos tribunales | `acumulacion-ejecuciones-titulos-judiciales-contra-civ-1556` |
| CIV-1557 | Demanda ejecutiva basada en título extrajudicial | `demanda-ejecutiva-basada-titulo-extrajudicial-civ-1557` |
| CIV-1559 | Demanda ejecutiva basada en título judicial | `demanda-ejecutiva-basada-titulo-judicial-civ-1559` |
| CIV-1566 | Solicitud del demandado rebelde de suspender la ejecución si se estima la rescisión de la sentencia | `solicitud-demandado-rebelde-suspender-ejecucion-si-civ-1566` |
| CIV-1568 | Demanda de ejecución provisional de sentencia de condena al pago de cantidad líquida | `demanda-ejecucion-provisional-sentencia-condena-pago-civ-1568` |
| CIV-1569 | Solicitud del ejecutado de suspender la ejecución por prejudicialidad penal | `solicitud-ejecutado-suspender-ejecucion-civ-1569` |
| CIV-1570 | Solicitud del ejecutado de suspender la ejecución por rescisión de sentencia dictada en rebeldía | `solicitud-ejecutado-suspender-ejecucion-rescision-civ-1570` |
| CIV-1571 | Escrito genérico que pide una actuación del tribunal en la ejecución | `escrito-generico-pide-actuacion-tribunal-ejecucion-civ-1571` |
| CIV-1575 | Demanda de ejecución provisional de sentencia en materia de arrendamientos | `demanda-ejecucion-provisional-sentencia-materia-civ-1575` |
| CIV-1576 | Solicitud de ejecución provisional de sentencia apelada | `solicitud-ejecucion-provisional-sentencia-apelada-civ-1576` |
| CIV-1577 | Personación ante la Audiencia en apelación pidiendo testimonio para la ejecución provisional | `personacion-ante-audiencia-apelacion-pidiendo-civ-1577` |
| CIV-1578 | Solicitud del ejecutante de embargo de garantías en ejecución no dineraria | `solicitud-ejecutante-embargo-garantias-ejecucion-no-civ-1578` |
| CIV-1579 | Demanda ejecutiva de sentencia firme de división de cosa común sobre finca rústica | `demanda-ejecutiva-sentencia-firme-division-cosa-comun-civ-1579` |
| CIV-1580 | Demanda ejecutiva de condena en sentencia con liquidación de intereses moratorios vencidos | `demanda-ejecutiva-condena-sentencia-liquidacion-civ-1580` |
| CIV-1585 | Solicitud de medidas para hacer efectivo el embargo acordado | `solicitud-medidas-hacer-efectivo-embargo-acordado-civ-1585` |
| CIV-1586 | Solicitud de suspender la ejecución de laudo arbitral no firme por acción de anulación | `solicitud-suspender-ejecucion-laudo-arbitral-no-firme-civ-1586` |
| CIV-1588 | Demanda ejecutiva de auto de cuantía máxima por seguro obligatorio, con bienes a embargar | `demanda-ejecutiva-auto-cuantia-maxima-seguro-civ-1588` |
| CIV-1590 | Declinatoria por falta de competencia territorial en la ejecución forzosa | `declinatoria-falta-competencia-territorial-ejecucion-civ-1590` |
| CIV-1591 | Solicitud de sobreseer la ejecución por estimarse la demanda de revisión de sentencia firme | `solicitud-sobreseer-ejecucion-estimarse-demanda-civ-1591` |
| CIV-1593 | Dictamen favorable del Fiscal a suspender la ejecución de la sentencia sometida a revisión | `dictamen-favorable-fiscal-suspender-ejecucion-civ-1593` |
| CIV-1595 | Dictamen contrario del Fiscal a suspender la ejecución de la sentencia sometida a revisión | `dictamen-contrario-fiscal-suspender-ejecucion-civ-1595` |
| CIV-1596 | Demanda de reconocimiento y ejecución en España de resolución extranjera con convenio | `demanda-reconocimiento-ejecucion-espana-resolucion-civ-1596` |
| CIV-1597 | Certificado de título ejecutivo europeo para transacción judicial aprobada | `certificado-titulo-ejecutivo-europeo-transaccion-civ-1597` |
| CIV-1599 | Solicitud de rectificar o revocar el certificado de título ejecutivo europeo | `solicitud-rectificar-revocar-certificado-titulo-civ-1599` |
| CIV-1600 | Certificado de título ejecutivo europeo para resolución judicial | `certificado-titulo-ejecutivo-europeo-resolucion-civ-1600` |
| CIV-1601 | Certificado de falta o limitación de ejecutoriedad del título ejecutivo europeo | `certificado-falta-limitacion-ejecutoriedad-titulo-civ-1601` |
| CIV-1602 | Certificado de título ejecutivo europeo para instrumento auténtico | `certificado-titulo-ejecutivo-europeo-instrumento-civ-1602` |
| CIV-1603 | Alegaciones a la liquidación presentada por el titular de un crédito posterior | `alegaciones-liquidacion-presentada-titular-credito-civ-1603` |
| CIV-1604 | Demanda ejecutiva de costas tras sentencias absolutorias conformes en instancia y apelación | `demanda-ejecutiva-costas-tras-sentencias-absolutorias-civ-1604` |
| CIV-1605 | Demanda de ejecución de título judicial extranjero conforme al Reglamento (CE) 44 2001 | `demanda-ejecucion-titulo-judicial-extranjero-conforme-civ-1605` |
| CIV-1607 | Solicitud de liquidar intereses al confirmarse en apelación la condena consignada por la aseguradora | `solicitud-liquidar-intereses-confirmarse-apelacion-civ-1607` |
| CIV-1610 | Escrito del deudor que consigna principal e intereses para liberar el bien | `escrito-deudor-consigna-principal-e-intereses-liberar-civ-1610` |
| CIV-1615 | Acta de la diligencia de embargo de bienes del ejecutado por la comisión judicial | `acta-diligencia-embargo-bienes-ejecutado-comision-civ-1615` |
| CIV-1618 | Demanda ejecutiva basada en auto de cuantía máxima por el seguro obligatorio de vehículos de motor | `demanda-ejecutiva-basada-auto-cuantia-maxima-seguro-civ-1618` |
| CIV-1619 | Escrito del ejecutado pidiendo reducir el embargo | `escrito-ejecutado-pidiendo-reducir-embargo-civ-1619` |
| CIV-1624 | Escrito pidiendo ejecutar lo convenido en la conciliación (general) | `escrito-pidiendo-ejecutar-lo-convenido-conciliacion-civ-1624` |
| CIV-1625 | Demanda de ejecución provisional con indicación de los bienes sobre los que trabar embargo | `demanda-ejecucion-provisional-indicacion-bienes-sobre-civ-1625` |
| CIV-1626 | Demanda de ejecución provisional sin conocer bienes sobre los que trabar embargo | `demanda-ejecucion-provisional-sin-conocer-bienes-sobre-civ-1626` |
| CIV-1628 | Escrito impugnando la cuenta final justificada del administrador judicial en la ejecución | `escrito-impugnando-cuenta-final-justificada-civ-1628` |
| CIV-1629 | Escrito del reembargante pidiendo la realización forzosa de los bienes si se alza el embargo previo | `escrito-reembargante-pidiendo-realizacion-forzosa-civ-1629` |
| CIV-1630 | Escrito pidiendo el embargo del sobrante de la realización de bienes en otro procedimiento | `escrito-pidiendo-embargo-sobrante-realizacion-bienes-civ-1630` |
| CIV-1631 | Escrito del reembargante pidiendo la realización forzosa aunque subsista el embargo anterior | `escrito-reembargante-pidiendo-realizacion-forzosa-civ-1631` |
| CIV-1635 | Escrito del ejecutante pidiendo apremiar al ejecutado para que aporte los títulos de propiedad | `escrito-ejecutante-pidiendo-apremiar-ejecutado-aporte-civ-1635` |
| CIV-1640 | Escrito pidiendo deshacer lo hecho e indemnizar al ejecutado tras sentencia revocatoria | `escrito-pidiendo-deshacer-lo-hecho-e-indemnizar-civ-1640` |
| CIV-1641 | Escrito del ejecutado pidiendo la restitución del bien entregado tras sentencia revocatoria | `escrito-ejecutado-pidiendo-restitucion-bien-entregado-civ-1641` |
| CIV-1643 | Escrito del ejecutante conforme con no trabar un bien que pertenece a un tercero | `escrito-ejecutante-conforme-no-trabar-bien-pertenece-civ-1643` |
| CIV-1644 | Escrito de un tercero que se opone al embargo de bienes de su propiedad | `escrito-tercero-opone-embargo-bienes-propiedad-civ-1644` |
| CIV-1645 | Escrito del ejecutante pidiendo mejora de embargo por insuficiencia de los bienes trabados | `escrito-ejecutante-pidiendo-mejora-embargo-civ-1645` |
| CIV-1646 | Escrito pidiendo investigar el patrimonio del ejecutado mediante oficio a una entidad | `escrito-pidiendo-investigar-patrimonio-ejecutado-civ-1646` |
| CIV-1647 | Escrito pidiendo suspender la ejecución por haberse admitido la rescisión de sentencia firme | `escrito-pidiendo-suspender-ejecucion-haberse-admitido-civ-1647` |
| CIV-1654 | Demanda ejecutiva basada en sentencia firme ante el tribunal competente para la ejecución | `demanda-ejecutiva-basada-sentencia-firme-ante-tribunal-civ-1654` |
| CIV-1655 | Demanda ejecutiva por reclamación de cantidad basada en sentencia de condena firme | `demanda-ejecutiva-reclamacion-cantidad-basada-civ-1655` |
| CIV-1656 | Demanda ejecutiva por cantidad con responsabilidad de bienes gananciales | `demanda-ejecutiva-cantidad-responsabilidad-bienes-civ-1656` |
| CIV-1660 | Escrito del ejecutante pidiendo mandamiento al Registro de la Propiedad para anotar el embargo | `escrito-ejecutante-pidiendo-mandamiento-registro-civ-1660` |
| CIV-1661 | Demanda ejecutiva basada en título que obliga a no hacer (art. 711 LEC) | `demanda-ejecutiva-basada-titulo-obliga-no-hacer-art-civ-1661` |
| CIV-1662 | Escrito del ejecutado que expone por qué se niega a hacer lo que dispone el título | `escrito-ejecutado-expone-niega-hacer-lo-dispone-titulo-civ-1662` |
| CIV-1663 | Escrito del ejecutante pidiendo apremiar con multas al ejecutado | `escrito-ejecutante-pidiendo-apremiar-multas-ejecutado-civ-1663` |
| CIV-1664 | Demanda ejecutiva basada en título que obliga a un hacer personalísimo (art. 709 LEC) | `demanda-ejecutiva-basada-titulo-obliga-hacer-civ-1664` |
| CIV-1665 | Escrito pidiendo requerir a los titulares de créditos posteriores que acrediten su subsistencia | `escrito-pidiendo-requerir-titulares-creditos-civ-1665` |
| CIV-1667 | Escrito del ejecutante pidiendo la posesión de los bienes embargados para administrarlos | `escrito-ejecutante-pidiendo-posesion-bienes-embargados-civ-1667` |
| CIV-1668 | Demanda ejecutiva basada en título que obliga a entregar bienes inmuebles (art. 703 LEC) | `demanda-ejecutiva-basada-titulo-obliga-entregar-bienes-civ-1668` |
| CIV-1669 | Demanda ejecutiva basada en título que obliga a un hacer no personalísimo (art. 705 LEC) | `demanda-ejecutiva-basada-titulo-obliga-hacer-no-civ-1669` |
| CIV-1670 | Escrito del ejecutante que opta por la indemnización de daños en lugar del hacer no personalísimo | `escrito-ejecutante-opta-indemnizacion-danos-lugar-civ-1670` |
| CIV-1671 | Demanda ejecutiva basada en título que obliga a entregar una cosa mueble cierta y determinada | `demanda-ejecutiva-basada-titulo-obliga-entregar-cosa-civ-1671` |
| CIV-1672 | Demanda ejecutiva basada en título que obliga a entregar cosas genéricas o indeterminadas | `demanda-ejecutiva-basada-titulo-obliga-entregar-cosas-civ-1672` |
| CIV-1675 | Solicitud de embargo de gananciales contra un cónyuge por deuda consorcial extracontractual | `solicitud-embargo-gananciales-contra-conyuge-deuda-civ-1675` |
| CIV-1676 | Solicitud de embargo de gananciales contra un cónyuge por deuda privativa anterior al matrimonio | `solicitud-embargo-gananciales-contra-conyuge-deuda-civ-1676` |
| CIV-1677 | Escrito del cónyuge no ejecutado oponiéndose al embargo de ganancial por ser privativa la deuda | `escrito-conyuge-no-ejecutado-oponiendose-embargo-civ-1677` |
| CIV-1678 | Escrito pidiendo ampliar la ejecución a nuevos plazos vencidos | `escrito-pidiendo-ampliar-ejecucion-nuevos-plazos-civ-1678` |
| CIV-1679 | Escrito pidiendo acumular ejecuciones de sentencias contra un mismo deudor ante distintos tribunales | `escrito-pidiendo-acumular-ejecuciones-sentencias-civ-1679` |
| CIV-1680 | Escrito pidiendo acumular ejecuciones de títulos extrajudiciales entre las mismas partes | `escrito-pidiendo-acumular-ejecuciones-titulos-civ-1680` |
| CIV-1681 | Escrito pidiendo fijar el equivalente pecuniario de una prestación no dineraria | `escrito-pidiendo-fijar-equivalente-pecuniario-civ-1681` |
| CIV-1682 | Escrito pidiendo acumular ejecuciones de monitorios entre las mismas partes ante el mismo tribunal | `escrito-pidiendo-acumular-ejecuciones-monitorios-entre-civ-1682` |
| CIV-1683 | Escrito del cónyuge no deudor que ejerce la opción ante el embargo de gananciales (art. 541.3 LEC) | `escrito-conyuge-no-deudor-ejerce-opcion-ante-embargo-civ-1683` |
| CIV-1685 | Escrito del ejecutante provisional oponiéndose a la liquidación de daños tras revocarse la sentencia | `escrito-ejecutante-provisional-oponiendose-liquidacion-civ-1685` |
| CIV-1686 | Escrito del ejecutado pidiendo sobreseer la ejecución provisional, devolución de lo cobrado y daños | `escrito-ejecutado-pidiendo-sobreseer-ejecucion-civ-1686` |
| CIV-1689 | Demanda de ejecución provisional de sentencia dictada en segunda instancia (arts. 535 a 537 LEC) | `demanda-ejecucion-provisional-sentencia-dictada-civ-1689` |
| CIV-1690 | Demanda de ejecución provisional de sentencia de condena no dineraria | `demanda-ejecucion-provisional-sentencia-condena-no-civ-1690` |
| CIV-1692 | Escrito del deudor que presenta la liquidación de frutos y rentas | `escrito-deudor-presenta-liquidacion-frutos-rentas-civ-1692` |
| CIV-1693 | Escrito pidiendo fijar la cantidad debida por frutos, rentas, utilidades o productos | `escrito-pidiendo-fijar-cantidad-debida-frutos-rentas-civ-1693` |
| CIV-1694 | Escrito del deudor conforme con la relación de daños y perjuicios | `escrito-deudor-conforme-relacion-danos-perjuicios-civ-1694` |
| CIV-1698 | Escrito del ejecutante pidiendo ser facultado para adquirir la cosa debida a costa del ejecutado | `escrito-ejecutante-pidiendo-ser-facultado-adquirir-civ-1698` |
| CIV-1699 | Escrito designando bienes a embargar y pidiendo despacho de ejecución tras el monitorio | `escrito-designando-bienes-embargar-pidiendo-despacho-civ-1699` |
| CIV-1701 | Escrito pidiendo suspender la ejecución provisional tras consignar judicialmente lo reclamado | `escrito-pidiendo-suspender-ejecucion-provisional-tras-civ-1701` |
| CIV-2823 | Escrito del perito tasador que presenta la valoración de los bienes embargados | `escrito-perito-tasador-presenta-valoracion-bienes-civ-2823` |
| CIV-2825 | Escrito que pide nombrar perito para tasar los bienes embargados e iniciar el apremio | `escrito-pide-nombrar-perito-tasar-bienes-embargados-e-civ-2825` |
| CIV-2827 | Escrito del ejecutante que pide oficiar a los acreedores preferentes anteriores sobre sus créditos | `escrito-ejecutante-pide-oficiar-acreedores-preferentes-civ-2827` |
| CIV-2828 | Escrito del ejecutante sobre si bastan los títulos de propiedad aportados por el ejecutado | `escrito-ejecutante-sobre-si-bastan-titulos-propiedad-civ-2828` |
| CIV-2830 | Escrito que pide la vía de apremio para cobrar los honorarios del abogado no pagados | `escrito-pide-via-apremio-cobrar-honorarios-abogado-no-civ-2830` |
| CIV-2832 | Solicitud de ejecución contra una empresa integrante de la UTE deudora según el título | `solicitud-ejecucion-contra-empresa-integrante-ute-civ-2832` |
| CIV-2836 | Petición de embargo del fondo de reserva de la comunidad ejecutada por sentencia de condena | `peticion-embargo-fondo-reserva-comunidad-ejecutada-civ-2836` |
| CIV-2837 | Escrito del ejecutante que pide exigir caución al tercerista de dominio para admitir su demanda | `escrito-ejecutante-pide-exigir-caucion-tercerista-civ-2837` |
| CIV-2839 | Petición del ejecutado de suspender la ejecución provisional consignando, sin entrega al ejecutante | `peticion-ejecutado-suspender-ejecucion-provisional-civ-2839` |
| CIV-2840 | Demanda de exequátur de sentencia extranjera del Convenio de Bruselas con averiguación de bienes | `demanda-exequatur-sentencia-extranjera-convenio-civ-2840` |
| CIV-2841 | Otrosí de la demanda ejecutiva que advierte que el embargo de gananciales responde a deuda privativa | `otrosi-demanda-ejecutiva-advierte-embargo-gananciales-civ-2841` |
| CIV-2844 | Escrito del rematante que pide mandamiento al Registro para cancelar las cargas | `escrito-rematante-pide-mandamiento-registro-cancelar-civ-2844` |
| CIV-2845 | Escrito de un acreedor posterior que acredita la subsistencia y exigibilidad de su crédito | `escrito-acreedor-posterior-acredita-subsistencia-civ-2845` |
| CIV-2852 | Escrito de las partes que se oponen a liberar del embargo el bien que reclama un tercero | `escrito-partes-oponen-liberar-embargo-bien-reclama-civ-2852` |
| CIV-2855 | Escrito del ejecutante que pide encargar el hacer a un tercero a costa del ejecutado | `escrito-ejecutante-pide-encargar-hacer-tercero-costa-civ-2855` |
| CIV-2857 | Escrito del obligado a desalojar la finca que reclama la titularidad de cosas no separables | `escrito-obligado-desalojar-finca-reclama-titularidad-civ-2857` |
| CIV-2858 | Escrito del ejecutante que declara que la entrega tardía ya no satisface su interés legítimo | `escrito-ejecutante-declara-entrega-tardia-ya-no-civ-2858` |
| CIV-2859 | Petición del ejecutante de mandamiento de anotación o inscripción en el registro correspondiente | `peticion-ejecutante-mandamiento-anotacion-inscripcion-civ-2859` |
| CIV-2860 | Escrito del ejecutante que pide seguir la ejecución por el equivalente en dinero del hacer | `escrito-ejecutante-pide-seguir-ejecucion-equivalente-civ-2860` |
| CIV-2863 | Alegaciones del abogado que no acepta rebajar sus honorarios incluidos en las costas | `alegaciones-abogado-no-acepta-rebajar-honorarios-civ-2863` |
| CIV-2868 | Petición de oficio al pagador para que retenga y consigne el sueldo del ejecutado | `peticion-oficio-pagador-retenga-consigne-sueldo-civ-2868` |
| CIV-2869 | Petición de anotación preventiva de embargo y retención de bienes en ejecución dineraria | `peticion-anotacion-preventiva-embargo-retencion-bienes-civ-2869` |
| CIV-2870 | Escrito del ejecutante que designa la cuenta para el ingreso de las cantidades retenidas | `escrito-ejecutante-designa-cuenta-ingreso-cantidades-civ-2870` |
| CIV-2871 | Declinatoria en la ejecución de sentencia matrimonial por falta de competencia objetiva y funcional | `declinatoria-ejecucion-sentencia-matrimonial-falta-civ-2871` |
| CIV-2872 | Petición de entrega de la cantidad retenida y consignada en el tribunal tras la vía de apremio | `peticion-entrega-cantidad-retenida-consignada-tribunal-civ-2872` |
| CIV-2873 | Escrito del cónyuge que nombra abogado y procurador propios ante la ejecución instada por el otro | `escrito-conyuge-nombra-abogado-procurador-propios-ante-civ-2873` |
| CIV-2874 | Demanda de ejecución para que el otro progenitor entregue al hijo conforme a la custodia fijada | `demanda-ejecucion-otro-progenitor-entregue-hijo-civ-2874` |
| CIV-2875 | Escrito que aporta copia del oficio entregado al banco del ejecutado para el embargo del sueldo | `escrito-aporta-copia-oficio-entregado-banco-ejecutado-civ-2875` |
| CIV-2876 | Solicitud de ejecución dineraria de sentencia matrimonial con aseguramiento de los bienes embargados | `solicitud-ejecucion-dineraria-sentencia-matrimonial-civ-2876` |
| CIV-2877 | Escrito que recuerda la petición pendiente de oficio para garantizar el embargo del sueldo | `escrito-recuerda-peticion-pendiente-oficio-garantizar-civ-2877` |
| CIV-2878 | Demanda de ejecución provisional de medidas patrimoniales antes de elevar los autos en apelación | `demanda-ejecucion-provisional-medidas-patrimoniales-civ-2878` |
| CIV-2879 | Demanda de ejecución dineraria de sentencia matrimonial para cobrar las cantidades impagadas | `demanda-ejecucion-dineraria-sentencia-matrimonial-civ-2879` |
| CIV-2881 | Escrito impugnando la tasación de costas en un proceso civil | `escrito-impugnando-tasacion-costas-proceso-civil-civ-2881` |
| CIV-2882 | Demanda para ejecutar la sentencia de un juicio declarativo por accidente de tráfico | `demanda-ejecutar-sentencia-juicio-declarativo-civ-2882` |

## Privacidad

Ver `PRIVACY.md`.
