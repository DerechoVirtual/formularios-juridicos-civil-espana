# Familia: divorcio, custodia, pensiones y parejas

> Plugin de Claude Code `formularios-familia-y-divorcio` · **372 formularios** · Civil · normativa revisada el 24-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Para el Derecho de familia: separación y divorcio de mutuo acuerdo o contencioso, convenio regulador, medidas provisionales y su modificación, custodia, visitas y pensiones, filiación, adopción, parejas de hecho, regímenes económicos y liquidación de gananciales, con especialidades forales.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 372 está al final):

- **Demandas, peticiones y solicitudes iniciales** (145). Por ejemplo: Solicitud de mediación familiar por una parte en cumplimiento de un pacto previo de mediación; Demanda contenciosa de modificación de medidas para reducir la pensión de alimentos de un hijo menor; Demanda de modificación de medidas por incumplimiento reiterado del régimen de visitas.
- **Contestaciones, oposiciones y alegaciones** (47). Por ejemplo: Contestación a demanda de divorcio reconviniendo por la prestación compensatoria del Derecho catalán; Contestación a la demanda de modificación de medidas por cambio de domicilio del progenitor custodio; Contestación a la reconvención que pide alimentos para un hijo mayor de edad.
- **Contratos, pactos y cláusulas** (18). Por ejemplo: Convenio regulador que recoge un acuerdo alcanzado en mediación; Convenio regulador tras la ruptura de la unión de hecho (Derecho civil catalán); Convenio regulador de mutuo acuerdo sobre hijos fuera de matrimonio y de pareja estable (Cataluña).
- **Estatutos, actas, certificaciones y escrituras** (48). Por ejemplo: Acta de inicio de un procedimiento de mediación familiar; Acta final de mediación con acuerdo en la ejecución de medidas definitivas de un proceso matrimonial; Acta final de mediación familiar con acuerdo de una pareja de hecho con hijos menores.
- **Comunicaciones, requerimientos y cartas** (44). Por ejemplo: Solicitud conjunta de mediación familiar presentada por ambas partes; Solicitud de aprobación judicial de un acuerdo de mediación sobre visitas de los abuelos; Burofax comunicando un cambio de domicilio.
- **Escritos de trámite y otros** (70). Por ejemplo: Escrito conjunto para transformar el proceso matrimonial tras alcanzar un acuerdo en mediación; Escrito conjunto para homologar un acuerdo de mediación familiar en ejecución de medidas definitivas; Escrito conjunto para homologar un acuerdo de mediación familiar en un proceso de filiación.

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Demanda de divorcio de mutuo acuerdo con hijos menores»
   - «Modificación de medidas para pasar a custodia compartida»
   - «Liquidación de la sociedad de gananciales»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-familia-y-divorcio:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-familia-y-divorcio:contestacion-demanda-divorcio-reconviniendo-prestacion-civ-0001`. Los nombres están en la lista de formularios de abajo.

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
- **Espacio que ocupa:** unos 21.023 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-familia-y-divorcio@formularios-juridicos-civil-espana`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-civil-espana
/plugin install formularios-familia-y-divorcio@formularios-juridicos-civil-espana
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-civil-espana`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-familia-y-divorcio.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (372)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0001 | Contestación a demanda de divorcio reconviniendo por la prestación compensatoria del Derecho catalán | `contestacion-demanda-divorcio-reconviniendo-prestacion-civ-0001` |
| CIV-0002 | Solicitud conjunta de mediación familiar presentada por ambas partes | `solicitud-conjunta-mediacion-familiar-presentada-ambas-civ-0002` |
| CIV-0003 | Acta de inicio de un procedimiento de mediación familiar | `acta-inicio-procedimiento-mediacion-familiar-civ-0003` |
| CIV-0004 | Escrito conjunto para transformar el proceso matrimonial tras alcanzar un acuerdo en mediación | `escrito-conjunto-transformar-proceso-matrimonial-tras-civ-0004` |
| CIV-0005 | Escrito conjunto para homologar un acuerdo de mediación familiar en ejecución de medidas definitivas | `escrito-conjunto-homologar-acuerdo-mediacion-familiar-civ-0005` |
| CIV-0006 | Escrito conjunto para homologar un acuerdo de mediación familiar en un proceso de filiación | `escrito-conjunto-homologar-acuerdo-mediacion-familiar-civ-0006` |
| CIV-0007 | Solicitud de mediación familiar por una parte en cumplimiento de un pacto previo de mediación | `solicitud-mediacion-familiar-parte-cumplimiento-pacto-civ-0007` |
| CIV-0008 | Escrito pidiendo levantar la suspensión del proceso porque la mediación familiar terminó sin acuerdo | `escrito-pidiendo-levantar-suspension-proceso-porque-civ-0008` |
| CIV-0009 | Solicitud de aprobación judicial de un acuerdo de mediación sobre visitas de los abuelos | `solicitud-aprobacion-judicial-acuerdo-mediacion-sobre-civ-0009` |
| CIV-0010 | Acta final de mediación con acuerdo en la ejecución de medidas definitivas de un proceso matrimonial | `acta-final-mediacion-acuerdo-ejecucion-medidas-civ-0010` |
| CIV-0011 | Convenio regulador que recoge un acuerdo alcanzado en mediación | `convenio-regulador-recoge-acuerdo-alcanzado-mediacion-civ-0011` |
| CIV-0012 | Acta final de mediación familiar con acuerdo de una pareja de hecho con hijos menores | `acta-final-mediacion-familiar-acuerdo-pareja-hecho-civ-0012` |
| CIV-0013 | Demanda contenciosa de modificación de medidas para reducir la pensión de alimentos de un hijo menor | `demanda-contenciosa-modificacion-medidas-reducir-civ-0013` |
| CIV-0014 | Demanda de modificación de medidas por incumplimiento reiterado del régimen de visitas | `demanda-modificacion-medidas-incumplimiento-reiterado-civ-0014` |
| CIV-0015 | Acta inicial o contrato de mediación familiar según la normativa aragonesa | `acta-inicial-contrato-mediacion-familiar-segun-civ-0015` |
| CIV-0016 | Acta final de mediación familiar sin acuerdos según la normativa andaluza | `acta-final-mediacion-familiar-sin-acuerdos-segun-civ-0016` |
| CIV-0017 | Acta final de mediación familiar con acuerdos según la normativa aragonesa | `acta-final-mediacion-familiar-acuerdos-segun-normativa-civ-0017` |
| CIV-0018 | Acta inicial o contrato de mediación familiar según la normativa andaluza | `acta-inicial-contrato-mediacion-familiar-segun-civ-0018` |
| CIV-0019 | Acta final de mediación familiar sin acuerdos según la normativa aragonesa | `acta-final-mediacion-familiar-sin-acuerdos-segun-civ-0019` |
| CIV-0020 | Acta final de mediación familiar con acuerdos según la normativa andaluza | `acta-final-mediacion-familiar-acuerdos-segun-normativa-civ-0020` |
| CIV-0021 | Solicitud de reconocimiento en España de una sentencia de divorcio colombiana (Convenio de 1908) | `solicitud-reconocimiento-espana-sentencia-divorcio-civ-0021` |
| CIV-0022 | Acta final de mediación familiar que concluye por posturas irreconciliables de las partes | `acta-final-mediacion-familiar-concluye-posturas-civ-0022` |
| CIV-0023 | Acta final de mediación familiar que termina sin acuerdo | `acta-final-mediacion-familiar-termina-sin-acuerdo-civ-0023` |
| CIV-0024 | Demanda de modificación de medidas definitivas porque el progenitor custodio cambia de domicilio | `demanda-modificacion-medidas-definitivas-porque-civ-0024` |
| CIV-0025 | Contestación a la demanda de modificación de medidas por cambio de domicilio del progenitor custodio | `contestacion-demanda-modificacion-medidas-cambio-civ-0025` |
| CIV-0026 | Burofax comunicando un cambio de domicilio | `burofax-comunicando-cambio-domicilio-civ-0026` |
| CIV-0027 | Acta inicial o contrato de mediación familiar sobre alimentos de un hijo mayor de edad | `acta-inicial-contrato-mediacion-familiar-sobre-civ-0027` |
| CIV-0028 | Acta final de mediación familiar con acuerdo sobre la pensión de alimentos | `acta-final-mediacion-familiar-acuerdo-sobre-pension-civ-0028` |
| CIV-0029 | Acta final de mediación familiar con acuerdo sobre la pensión compensatoria | `acta-final-mediacion-familiar-acuerdo-sobre-pension-civ-0029` |
| CIV-0030 | Contestación a la reconvención que pide alimentos para un hijo mayor de edad | `contestacion-reconvencion-pide-alimentos-hijo-mayor-civ-0030` |
| CIV-0031 | Contestación a la reconvención que pide indemnización por el artículo 98 del Código Civil | `contestacion-reconvencion-pide-indemnizacion-articulo-civ-0031` |
| CIV-0032 | Contestación a la reconvención que pide prestación compensatoria según el Derecho catalán | `contestacion-reconvencion-pide-prestacion-civ-0032` |
| CIV-0033 | Contestación a la reconvención de alimentos para un hijo mayor de edad según el Derecho catalán | `contestacion-reconvencion-alimentos-hijo-mayor-edad-civ-0033` |
| CIV-0034 | Contestación a divorcio con medidas y reconvención de alimentos a hijo mayor, Derecho catalán | `contestacion-divorcio-medidas-reconvencion-alimentos-civ-0034` |
| CIV-0035 | Contestación a la reconvención de pensión compensatoria alegando que no hay desequilibrio económico | `contestacion-reconvencion-pension-compensatoria-civ-0035` |
| CIV-0036 | Contestación a la reconvención de pensión compensatoria por larga separación de hecho sin ayuda | `contestacion-reconvencion-pension-compensatoria-larga-civ-0036` |
| CIV-0037 | Contestación a divorcio contencioso con reconvención de pensión compensatoria, Derecho catalán | `contestacion-divorcio-contencioso-reconvencion-pension-civ-0037` |
| CIV-0038 | Demanda de nulidad canónica por grave defecto de discreción de juicio y prórroga de competencia | `demanda-nulidad-canonica-grave-defecto-discrecion-civ-0038` |
| CIV-0039 | Contestación a divorcio contencioso con medidas propuestas y reconvención de alimentos a hijo mayor | `contestacion-divorcio-contencioso-medidas-propuestas-civ-0039` |
| CIV-0040 | Contestación a demanda contenciosa de separación con reconvención de divorcio y medidas definitivas | `contestacion-demanda-contenciosa-separacion-civ-0040` |
| CIV-0041 | Contestación a divorcio contencioso con medidas propuestas y reconvención de pensión compensatoria | `contestacion-divorcio-contencioso-medidas-propuestas-civ-0041` |
| CIV-0042 | Demanda de divorcio contencioso entre cónyuge español en España y cónyuge extracomunitario fuera | `demanda-divorcio-contencioso-entre-conyuge-espanol-civ-0042` |
| CIV-0043 | Demanda contenciosa de divorcio con petición de modificar la pensión de alimentos | `demanda-contenciosa-divorcio-peticion-modificar-civ-0043` |
| CIV-0044 | Solicitud de decisión judicial ante el desacuerdo de los padres sobre patria potestad (art 156 CC) | `solicitud-decision-judicial-ante-desacuerdo-padres-civ-0044` |
| CIV-0045 | Solicitud de jurisdicción voluntaria para que los abuelos asuman la guarda y custodia de los menores | `solicitud-jurisdiccion-voluntaria-abuelos-asuman-civ-0045` |
| CIV-0046 | Demanda de divorcio contencioso con alimentos y vivienda para hijo mayor sin ingresos conviviente | `demanda-divorcio-contencioso-alimentos-vivienda-hijo-civ-0046` |
| CIV-0047 | Escrito de conclusiones en un proceso de nulidad matrimonial ante el Tribunal Eclesiástico | `escrito-conclusiones-proceso-nulidad-matrimonial-ante-civ-0047` |
| CIV-0048 | Demanda de desahucio por precario contra quien usa la vivienda familiar por sentencia matrimonial | `demanda-desahucio-precario-contra-quien-usa-vivienda-civ-0048` |
| CIV-0049 | Oposición oral al desahucio por precario de la vivienda familiar alegando fraude de ley | `oposicion-oral-desahucio-precario-vivienda-familiar-civ-0049` |
| CIV-0050 | Solicitud de lanzamiento del ocupante en precario de la vivienda familiar tras separación o divorcio | `solicitud-lanzamiento-ocupante-precario-vivienda-civ-0050` |
| CIV-0051 | Oposición a la solicitud de declarar un gasto extraordinario no previsto en las medidas | `oposicion-solicitud-declarar-gasto-extraordinario-no-civ-0051` |
| CIV-0052 | Demanda de liquidación de gananciales y partición de herencia de un hijo adoptivo del fallecido | `demanda-liquidacion-gananciales-particion-herencia-civ-0052` |
| CIV-0053 | Demanda de divorcio o separación de mutuo acuerdo con convenio que recoge una mediación previa | `demanda-divorcio-separacion-mutuo-acuerdo-convenio-civ-0053` |
| CIV-0054 | Resolución consular que deniega la inscripción de un matrimonio | `resolucion-consular-deniega-inscripcion-matrimonio-civ-0054` |
| CIV-0055 | Demanda de nulidad matrimonial ante el Tribunal Eclesiástico | `demanda-nulidad-matrimonial-ante-tribunal-eclesiastico-civ-0055` |
| CIV-0056 | Otrosíes pidiendo comisión canónica para representar a la actora y reducción de costas en la nulidad | `otrosies-pidiendo-comision-canonica-representar-actora-civ-0056` |
| CIV-0057 | Lista de testigos para la prueba en un proceso de nulidad matrimonial canónica | `lista-testigos-prueba-proceso-nulidad-matrimonial-civ-0057` |
| CIV-0058 | Solicitud de dispensa pontificia de matrimonio rato y no consumado | `solicitud-dispensa-pontificia-matrimonio-rato-no-civ-0058` |
| CIV-0059 | Interrogatorio de testigos en un proceso de nulidad canónica por el canon 1095.2 | `interrogatorio-testigos-proceso-nulidad-canonica-canon-civ-0059` |
| CIV-0060 | Solicitud de patrocinio gratuito en un proceso de nulidad matrimonial | `solicitud-patrocinio-gratuito-proceso-nulidad-civ-0060` |
| CIV-0061 | Escrito de proposición de prueba en un proceso de nulidad canónica | `escrito-proposicion-prueba-proceso-nulidad-canonica-civ-0061` |
| CIV-0062 | Pliego de preguntas para el examen judicial de la parte en una nulidad canónica por el canon 1095.2 | `pliego-preguntas-examen-judicial-parte-nulidad-civ-0062` |
| CIV-0063 | Solicitud de dispensa in favorem fidei para disolver un matrimonio canónico con persona no bautizada | `solicitud-dispensa-in-favorem-fidei-disolver-civ-0063` |
| CIV-0064 | Demanda de divorcio contencioso según el Derecho civil catalán pidiendo la custodia compartida | `demanda-divorcio-contencioso-segun-derecho-civil-civ-0064` |
| CIV-0065 | Escritura de capitulaciones posteriores al matrimonio que adoptan la sociedad de gananciales | `escritura-capitulaciones-posteriores-matrimonio-civ-0065` |
| CIV-0066 | Solicitud de declaración de gasto extraordinario por tratamiento del hijo común antes de ejecutar | `solicitud-declaracion-gasto-extraordinario-tratamiento-civ-0066` |
| CIV-0067 | Demanda de modificación de medidas para pedir custodia compartida (ley valenciana de 2011) | `demanda-modificacion-medidas-pedir-custodia-compartida-civ-0067` |
| CIV-0068 | Contestación a la demanda de modificación de medidas que pide la custodia compartida | `contestacion-demanda-modificacion-medidas-pide-civ-0068` |
| CIV-0069 | Otrosí de medidas provisionales sobre guarda y custodia en demanda de modificación de medidas | `otrosi-medidas-provisionales-sobre-guarda-custodia-civ-0069` |
| CIV-0070 | Demanda de modificación de medidas de mutuo acuerdo para establecer la custodia compartida | `demanda-modificacion-medidas-mutuo-acuerdo-establecer-civ-0070` |
| CIV-0071 | Otrosí pidiendo la audiencia del menor en demanda de modificación de medidas sobre custodia | `otrosi-pidiendo-audiencia-menor-demanda-modificacion-civ-0071` |
| CIV-0072 | Escrito pidiendo alzar el embargo por extinción de la obligación de pagar alimentos | `escrito-pidiendo-alzar-embargo-extincion-obligacion-civ-0072` |
| CIV-0073 | Escrito inicial para hacer valer el asentimiento exigido en la adopción | `escrito-inicial-hacer-valer-asentimiento-exigido-civ-0073` |
| CIV-0074 | Contestación a la demanda de divorcio que pide modificar las medidas fijadas en la separación previa | `contestacion-demanda-divorcio-pide-modificar-medidas-civ-0074` |
| CIV-0075 | Demanda de divorcio de mutuo acuerdo que modifica las medidas acordadas en la separación previa | `demanda-divorcio-mutuo-acuerdo-modifica-medidas-civ-0075` |
| CIV-0076 | Solicitud de inventario en la liquidación del régimen económico matrimonial (Derecho catalán) | `solicitud-inventario-liquidacion-regimen-economico-civ-0076` |
| CIV-0077 | Demanda de oposición a la declaración administrativa de desamparo de un menor (Derecho catalán) | `demanda-oposicion-declaracion-administrativa-desamparo-civ-0077` |
| CIV-0078 | Escrito inicial de oposición a la resolución de desamparo de un menor (Derecho catalán) | `escrito-inicial-oposicion-resolucion-desamparo-menor-civ-0078` |
| CIV-0079 | Demanda de juicio ordinario para recuperar la patria potestad | `demanda-juicio-ordinario-recuperar-patria-potestad-civ-0079` |
| CIV-0080 | Propuesta de medidas por separación o divorcio contencioso (Derecho catalán) | `propuesta-medidas-separacion-divorcio-contencioso-civ-0080` |
| CIV-0081 | Acta notarial de notificación de ruptura y requerimiento para dejar sin efecto la escritura de unión | `acta-notarial-notificacion-ruptura-requerimiento-dejar-civ-0081` |
| CIV-0082 | Demanda de juicio ordinario para reclamar derechos sobre bienes adjudicados como privativos | `demanda-juicio-ordinario-reclamar-derechos-sobre-civ-0082` |
| CIV-0083 | Demanda de mutuo acuerdo de parejas de hecho con hijos menores | `demanda-mutuo-acuerdo-parejas-hecho-hijos-menores-civ-0083` |
| CIV-0084 | Solicitud de medidas sobre hijos menores ante la Sección de Violencia sobre la Mujer | `solicitud-medidas-sobre-hijos-menores-ante-seccion-civ-0084` |
| CIV-0085 | Contestación a la demanda de nulidad matrimonial con oposición | `contestacion-demanda-nulidad-matrimonial-oposicion-civ-0085` |
| CIV-0086 | Contestación a la demanda de nulidad matrimonial con allanamiento | `contestacion-demanda-nulidad-matrimonial-allanamiento-civ-0086` |
| CIV-0087 | Liquidación del régimen económico-matrimonial de mutuo acuerdo (solicitud) | `liquidacion-regimen-economico-matrimonial-mutuo-civ-0087` |
| CIV-0088 | Demanda de nulidad del matrimonio cuando no hay hijos menores | `demanda-nulidad-matrimonio-cuando-no-hay-hijos-menores-civ-0088` |
| CIV-0089 | Demanda de extinción de convivencia con alimentos y pensión compensatoria (convivientes en Cataluña) | `demanda-extincion-convivencia-alimentos-pension-civ-0089` |
| CIV-0090 | Solicitud de derecho de visita de un menor a través de la Autoridad Central | `solicitud-derecho-visita-menor-traves-autoridad-central-civ-0090` |
| CIV-0091 | Escrito de ejecución de sentencia por impago de pensión y su actualización | `escrito-ejecucion-sentencia-impago-pension-civ-0091` |
| CIV-0092 | Escrito del condenado que se opone a la actualización de la pensión y a los impagos reclamados | `escrito-condenado-opone-actualizacion-pension-impagos-civ-0092` |
| CIV-0093 | Escrito de oposición a la ejecución de medidas definitivas de familia | `escrito-oposicion-ejecucion-medidas-definitivas-familia-civ-0093` |
| CIV-0094 | Escrito con nueva propuesta de convenio regulador de separación o divorcio | `escrito-nueva-propuesta-convenio-regulador-separacion-civ-0094` |
| CIV-0095 | Demanda para exigir el cumplimiento del régimen de visitas de los nietos con sus abuelos | `demanda-exigir-cumplimiento-regimen-visitas-nietos-civ-0095` |
| CIV-0096 | Demanda de divorcio contencioso con hijos menores y mayores dependientes y petición de medidas | `demanda-divorcio-contencioso-hijos-menores-mayores-civ-0096` |
| CIV-0097 | Demanda de separación presentada por un cónyuge sin el consentimiento del otro | `demanda-separacion-presentada-conyuge-sin-civ-0097` |
| CIV-0098 | Demanda de separación contenciosa con hijos menores y mayores dependientes y petición de medidas | `demanda-separacion-contenciosa-hijos-menores-mayores-civ-0098` |
| CIV-0099 | Demanda de separación contenciosa sin hijos con petición de medidas | `demanda-separacion-contenciosa-sin-hijos-peticion-civ-0099` |
| CIV-0100 | Solicitud de conversión del proceso de separación en divorcio tras la Ley 15 de 2005 | `solicitud-conversion-proceso-separacion-divorcio-tras-civ-0100` |
| CIV-0101 | Demanda de divorcio de un cónyuge con el consentimiento del otro y convenio regulador | `demanda-divorcio-conyuge-consentimiento-otro-convenio-civ-0101` |
| CIV-0102 | Escrito para alzar las medidas provisionales previas por no presentar la demanda en plazo | `escrito-alzar-medidas-provisionales-previas-no-civ-0102` |
| CIV-0103 | Demanda de restitución de menores según el Convenio hispano-marroquí de 1997 | `demanda-restitucion-menores-segun-convenio-hispano-civ-0103` |
| CIV-0104 | Solicitud de devolución de un menor a través de la Autoridad Central | `solicitud-devolucion-menor-traves-autoridad-central-civ-0104` |
| CIV-0105 | Solicitud a la Autoridad Central de restitución de menores (Convenio hispano-marroquí de 1997) | `solicitud-autoridad-central-restitucion-menores-civ-0105` |
| CIV-0106 | Solicitud de liquidación del régimen de participación y propuesta de liquidación (Derecho catalán) | `solicitud-liquidacion-regimen-participacion-propuesta-civ-0106` |
| CIV-0107 | Propuesta de inventario para reclamar la compensación por razón de trabajo (Derecho catalán) | `propuesta-inventario-reclamar-compensacion-razon-civ-0107` |
| CIV-0108 | Contestación a la demanda de modificación de medidas de un proceso matrimonial (Derecho catalán) | `contestacion-demanda-modificacion-medidas-proceso-civ-0108` |
| CIV-0109 | Escrito para recuperar la posesión de la vivienda familiar por extinción del uso (Derecho catalán) | `escrito-recuperar-posesion-vivienda-familiar-extincion-civ-0109` |
| CIV-0110 | Contestación a la demanda de extinción de pareja estable (Derecho catalán) | `contestacion-demanda-extincion-pareja-estable-derecho-civ-0110` |
| CIV-0111 | Contestación del Ministerio Fiscal a la demanda de reclamación de filiación no matrimonial | `contestacion-ministerio-fiscal-demanda-reclamacion-civ-0111` |
| CIV-0112 | Contestación a la reclamación de filiación de la madre con impugnación de la contradictoria | `contestacion-reclamacion-filiacion-madre-impugnacion-civ-0112` |
| CIV-0113 | Demanda de reclamación de filiación no matrimonial del hijo con impugnación de la contradictoria | `demanda-reclamacion-filiacion-no-matrimonial-hijo-civ-0113` |
| CIV-0114 | Demanda del presunto padre de reclamación de filiación con medidas de protección del menor | `demanda-presunto-padre-reclamacion-filiacion-medidas-civ-0114` |
| CIV-0115 | Contestación a la reclamación de filiación del presunto padre con impugnación de la contradictoria | `contestacion-reclamacion-filiacion-presunto-padre-civ-0115` |
| CIV-0116 | Contestación a la reclamación de filiación no matrimonial del hijo mayor de edad | `contestacion-reclamacion-filiacion-no-matrimonial-hijo-civ-0116` |
| CIV-0117 | Contestación a la reclamación de filiación del hijo con impugnación de la contradictoria | `contestacion-reclamacion-filiacion-hijo-impugnacion-civ-0117` |
| CIV-0118 | Contestación del Ministerio Fiscal a la demanda de impugnación de filiación matrimonial | `contestacion-ministerio-fiscal-demanda-impugnacion-civ-0118` |
| CIV-0119 | Demanda de la madre de reclamación de filiación no matrimonial con prueba biológica | `demanda-madre-reclamacion-filiacion-no-matrimonial-civ-0119` |
| CIV-0120 | Demanda del hijo mayor de edad de reclamación de filiación no matrimonial | `demanda-hijo-mayor-edad-reclamacion-filiacion-no-civ-0120` |
| CIV-0121 | Demanda de medidas paterno-filiales tras la sentencia que declara la filiación | `demanda-medidas-paterno-filiales-tras-sentencia-civ-0121` |
| CIV-0122 | Demanda del presunto padre de reclamación de filiación no matrimonial | `demanda-presunto-padre-reclamacion-filiacion-no-civ-0122` |
| CIV-0123 | Demanda de impugnación de filiación matrimonial | `demanda-impugnacion-filiacion-matrimonial-civ-0123` |
| CIV-0124 | Demanda de modificación de las medidas definitivas de un proceso matrimonial (Derecho catalán) | `demanda-modificacion-medidas-definitivas-proceso-civ-0124` |
| CIV-0125 | Demanda de alimentos de un hijo contra sus padres | `demanda-alimentos-hijo-contra-padres-civ-0125` |
| CIV-0126 | Demanda de alimentos entre hermanos (Derecho civil catalán) | `demanda-alimentos-entre-hermanos-derecho-civil-catalan-civ-0126` |
| CIV-0127 | Contestación a la reclamación de filiación de la madre que pide prueba biológica | `contestacion-reclamacion-filiacion-madre-pide-prueba-civ-0127` |
| CIV-0128 | Demanda del presunto padre de reclamación de filiación con régimen de visitas provisional | `demanda-presunto-padre-reclamacion-filiacion-regimen-civ-0128` |
| CIV-0129 | Solicitud de informe del equipo psicosocial en el divorcio | `solicitud-informe-equipo-psicosocial-divorcio-civ-0129` |
| CIV-0130 | Escritura de poder especial entre cónyuges para vender un bien ganancial | `escritura-poder-especial-entre-conyuges-vender-bien-civ-0130` |
| CIV-0131 | Escrito para continuar el procedimiento de filiación contra los herederos del demandado fallecido | `escrito-continuar-procedimiento-filiacion-contra-civ-0131` |
| CIV-0132 | Nota de inscripción registral de la compraventa para la sociedad de gananciales | `nota-inscripcion-registral-compraventa-sociedad-civ-0132` |
| CIV-0133 | Escritura de aportación de un bien a la sociedad de gananciales | `escritura-aportacion-bien-sociedad-gananciales-civ-0133` |
| CIV-0134 | Escritura de cese de proindivisión y adjudicación entre cónyuges en separación de bienes | `escritura-cese-proindivision-adjudicacion-entre-civ-0134` |
| CIV-0135 | Demanda de separación o divorcio que modifica las medidas dictadas por Violencia sobre la Mujer | `demanda-separacion-divorcio-modifica-medidas-dictadas-civ-0135` |
| CIV-0136 | Solicitud de la familia acogedora a la entidad pública para cesar el acogimiento | `solicitud-familia-acogedora-entidad-publica-cesar-civ-0136` |
| CIV-0137 | Demanda contra la declaración de no idoneidad para adoptar | `demanda-contra-declaracion-no-idoneidad-adoptar-civ-0137` |
| CIV-0138 | Petición de reanudar divorcio o separación contenciosos suspendidos y convertirlos en mutuo acuerdo | `peticion-reanudar-divorcio-separacion-contenciosos-civ-0138` |
| CIV-0139 | Escrito sucinto inicial de oposición a la declaración de no idoneidad para adoptar | `escrito-sucinto-inicial-oposicion-declaracion-no-civ-0139` |
| CIV-0140 | Escrito para recuperar la guarda del menor asumida temporalmente por la entidad pública | `escrito-recuperar-guarda-menor-asumida-temporalmente-civ-0140` |
| CIV-0141 | Convenio regulador tras la ruptura de la unión de hecho (Derecho civil catalán) | `convenio-regulador-tras-ruptura-union-hecho-derecho-civ-0141` |
| CIV-0142 | Demanda de mutuo acuerdo sobre guarda y custodia compartida tras ruptura de pareja (Derecho catalán) | `demanda-mutuo-acuerdo-sobre-guarda-custodia-compartida-civ-0142` |
| CIV-0143 | Contestación a la demanda de guarda, visitas y alimentos de menores presentada por un progenitor | `contestacion-demanda-guarda-visitas-alimentos-menores-civ-0143` |
| CIV-0144 | Plan de parentalidad conforme al Derecho civil catalán | `plan-parentalidad-conforme-derecho-civil-catalan-civ-0144` |
| CIV-0145 | Demanda de extinción de la prestación compensatoria (Derecho civil catalán) | `demanda-extincion-prestacion-compensatoria-derecho-civ-0145` |
| CIV-0146 | Demanda de extinción de la pensión alimenticia del hijo mayor por su matrimonio | `demanda-extincion-pension-alimenticia-hijo-mayor-civ-0146` |
| CIV-0147 | Demanda para sustituir la cláusula de gastos extraordinarios por mayor pensión alimenticia | `demanda-sustituir-clausula-gastos-extraordinarios-civ-0147` |
| CIV-0148 | Demanda de reducción de la pensión alimenticia por el nacimiento de un nuevo hijo | `demanda-reduccion-pension-alimenticia-nacimiento-nuevo-civ-0148` |
| CIV-0149 | Demanda de suspensión temporal del pago de la pensión alimenticia | `demanda-suspension-temporal-pago-pension-alimenticia-civ-0149` |
| CIV-0150 | Demanda de reducción de la pensión alimenticia por el aumento de ingresos del progenitor custodio | `demanda-reduccion-pension-alimenticia-aumento-ingresos-civ-0150` |
| CIV-0151 | Demanda para suspender en verano el pago de la pensión alimenticia | `demanda-suspender-verano-pago-pension-alimenticia-civ-0151` |
| CIV-0152 | Demanda para sustituir la pensión fijada como porcentaje de ingresos por una cantidad fija | `demanda-sustituir-pension-fijada-como-porcentaje-civ-0152` |
| CIV-0153 | Solicitud de medidas judiciales por desacuerdo en la potestad parental (Derecho catalán) | `solicitud-medidas-judiciales-desacuerdo-potestad-civ-0153` |
| CIV-0154 | Demanda de divorcio contencioso con alimentos para hijos mayores de edad (Derecho catalán) | `demanda-divorcio-contencioso-alimentos-hijos-mayores-civ-0154` |
| CIV-0155 | Demanda de separación contenciosa con privación de la potestad parental (Derecho catalán) | `demanda-separacion-contenciosa-privacion-potestad-civ-0155` |
| CIV-0156 | Medidas provisionales previas a la demanda de nulidad, separación o divorcio (Derecho catalán) | `medidas-provisionales-previas-demanda-nulidad-civ-0156` |
| CIV-0157 | Convenio regulador de mutuo acuerdo sobre hijos fuera de matrimonio y de pareja estable (Cataluña) | `convenio-regulador-mutuo-acuerdo-sobre-hijos-fuera-civ-0157` |
| CIV-0158 | Escrito para promover la adopción del menor acogido durante más de un año | `escrito-promover-adopcion-menor-acogido-durante-mas-ano-civ-0158` |
| CIV-0159 | Escrito para promover la adopción por el tutor | `escrito-promover-adopcion-tutor-civ-0159` |
| CIV-0160 | Escrito para promover la adopción de un pariente en tercer o ulterior grado colateral | `escrito-promover-adopcion-pariente-tercer-ulterior-civ-0160` |
| CIV-0161 | Plan de parentalidad de mutuo acuerdo con custodia compartida | `plan-parentalidad-mutuo-acuerdo-custodia-compartida-civ-0161` |
| CIV-0162 | Plan de parentalidad de mutuo acuerdo con guarda individual | `plan-parentalidad-mutuo-acuerdo-guarda-individual-civ-0162` |
| CIV-0163 | Propuesta de plan de parentalidad presentada por uno de los cónyuges | `propuesta-plan-parentalidad-presentada-uno-conyuges-civ-0163` |
| CIV-0164 | Demanda de extinción o reducción de la pensión alimenticia por disminución de ingresos del obligado | `demanda-extincion-reduccion-pension-alimenticia-civ-0164` |
| CIV-0165 | Demanda de aumento de la pensión alimenticia por incremento de los gastos de los hijos | `demanda-aumento-pension-alimenticia-incremento-gastos-civ-0165` |
| CIV-0166 | Demanda de divorcio de mutuo acuerdo tras una separación de mutuo acuerdo previa | `demanda-divorcio-mutuo-acuerdo-tras-separacion-mutuo-civ-0166` |
| CIV-0167 | Demanda de separación presentada con medidas provisionales previas vigentes | `demanda-separacion-presentada-medidas-provisionales-civ-0167` |
| CIV-0168 | Escrito pidiendo prohibir la salida de un menor al extranjero | `escrito-pidiendo-prohibir-salida-menor-extranjero-civ-0168` |
| CIV-0169 | Escrito de proposición de prueba en el procedimiento de separación contenciosa | `escrito-proposicion-prueba-procedimiento-separacion-civ-0169` |
| CIV-0170 | Escrito pidiendo testimonio de la sentencia y del convenio regulador en separación de mutuo acuerdo | `escrito-pidiendo-testimonio-sentencia-convenio-civ-0170` |
| CIV-0171 | Demanda de modificación del régimen de visitas con suspensión provisional | `demanda-modificacion-regimen-visitas-suspension-civ-0171` |
| CIV-0172 | Demanda de modificación de medidas con modificación provisional y supresión de alimentos (Cataluña) | `demanda-modificacion-medidas-modificacion-provisional-civ-0172` |
| CIV-0173 | Demanda de divorcio de mutuo acuerdo tras pacto en la comparecencia de medidas previas (Cataluña) | `demanda-divorcio-mutuo-acuerdo-tras-pacto-civ-0173` |
| CIV-0174 | Demanda contra la declaración de desamparo por razones de fondo | `demanda-contra-declaracion-desamparo-razones-fondo-civ-0174` |
| CIV-0175 | Demanda contra la declaración de desamparo por defectos formales | `demanda-contra-declaracion-desamparo-defectos-formales-civ-0175` |
| CIV-0176 | Escrito inicial de oposición al desamparo presentado por el guardador de hecho | `escrito-inicial-oposicion-desamparo-presentado-civ-0176` |
| CIV-0177 | Demanda para rectificar un error en la inscripción de nacimiento en el Registro Civil | `demanda-rectificar-error-inscripcion-nacimiento-civ-0177` |
| CIV-0178 | Escrito de familiares pidiendo que se les entregue al menor desamparado en acogimiento | `escrito-familiares-pidiendo-les-entregue-menor-civ-0178` |
| CIV-0179 | Pacto de convivencia de una unión de hecho según el Derecho valenciano | `pacto-convivencia-union-hecho-segun-derecho-valenciano-civ-0179` |
| CIV-0180 | Escritura de poder especial para contraer matrimonio | `escritura-poder-especial-contraer-matrimonio-civ-0180` |
| CIV-0181 | Demanda de juicio verbal de alimentos del hijo mayor de edad | `demanda-juicio-verbal-alimentos-hijo-mayor-edad-civ-0181` |
| CIV-0182 | Escritura de revocación de poder especial para contraer matrimonio | `escritura-revocacion-poder-especial-contraer-matrimonio-civ-0182` |
| CIV-0183 | Escrito del progenitor pidiendo a la entidad pública que asuma temporalmente la guarda del menor | `escrito-progenitor-pidiendo-entidad-publica-asuma-civ-0183` |
| CIV-0184 | Contrato de mediación con acuerdos sobre los efectos del divorcio | `contrato-mediacion-acuerdos-sobre-efectos-divorcio-civ-0184` |
| CIV-0185 | Solicitud de medidas judiciales por desacuerdo en el ejercicio de la patria potestad | `solicitud-medidas-judiciales-desacuerdo-ejercicio-civ-0185` |
| CIV-0186 | Demanda contenciosa de medidas parentales, alimentos y vivienda tras ruptura de pareja (Cataluña) | `demanda-contenciosa-medidas-parentales-alimentos-civ-0186` |
| CIV-0187 | Demanda de disolución de la sociedad de gananciales por discapacidad de un cónyuge con liquidación | `demanda-disolucion-sociedad-gananciales-discapacidad-civ-0187` |
| CIV-0188 | Demanda consensual de medidas parentales y económicas tras ruptura de pareja de hecho (Cataluña) | `demanda-consensual-medidas-parentales-economicas-tras-civ-0188` |
| CIV-0189 | Solicitud de autorización judicial para vender bienes de hijos menores (Derecho civil catalán) | `solicitud-autorizacion-judicial-vender-bienes-hijos-civ-0189` |
| CIV-0190 | Escrito pidiendo plazo para formular demanda en el procedimiento de asentimiento a la adopción | `escrito-pidiendo-plazo-formular-demanda-procedimiento-civ-0190` |
| CIV-0191 | Solicitud de medidas cautelares en un proceso de filiación | `solicitud-medidas-cautelares-proceso-filiacion-civ-0191` |
| CIV-0192 | Escrito de declaración de gastos extraordinarios en un proceso matrimonial | `escrito-declaracion-gastos-extraordinarios-proceso-civ-0192` |
| CIV-0193 | Escrito de contestación a la demanda en proceso sobre menores | `escrito-contestacion-demanda-proceso-sobre-menores-civ-0193` |
| CIV-0194 | Demanda para añadir bienes a una liquidación previa de la sociedad de gananciales | `demanda-anadir-bienes-liquidacion-previa-sociedad-civ-0194` |
| CIV-0195 | Demanda de juicio ordinario para anular el convenio regulador por vicio del consentimiento | `demanda-juicio-ordinario-anular-convenio-regulador-civ-0195` |
| CIV-0196 | Demanda contenciosa de modificación del convenio regulador para extinguir la pensión compensatoria | `demanda-contenciosa-modificacion-convenio-regulador-civ-0196` |
| CIV-0197 | Escritura de extinción de pareja de hecho según el Derecho vasco | `escritura-extincion-pareja-hecho-segun-derecho-vasco-civ-0197` |
| CIV-0198 | Escritura de constitución de pareja de hecho según el Derecho vasco | `escritura-constitucion-pareja-hecho-segun-derecho-vasco-civ-0198` |
| CIV-0199 | Escritura de constitución de unión de hecho según el Derecho de Madrid | `escritura-constitucion-union-hecho-segun-derecho-madrid-civ-0199` |
| CIV-0200 | Escritura de constitución de pareja de hecho según el Derecho de Extremadura | `escritura-constitucion-pareja-hecho-segun-derecho-civ-0200` |
| CIV-0201 | Escritura de constitución de pareja de hecho según el Derecho de Canarias | `escritura-constitucion-pareja-hecho-segun-derecho-civ-0201` |
| CIV-0202 | Escritura de constitución de pareja estable según el Derecho de Asturias | `escritura-constitucion-pareja-estable-segun-derecho-civ-0202` |
| CIV-0203 | Escritura de constitución de pareja de hecho según el Derecho de Andalucía | `escritura-constitucion-pareja-hecho-segun-derecho-civ-0203` |
| CIV-0204 | Escritura de constitución de pareja estable no casada según el Derecho aragonés | `escritura-constitucion-pareja-estable-no-casada-segun-civ-0204` |
| CIV-0205 | Escritura de constitución de unión de hecho según el Derecho valenciano | `escritura-constitucion-union-hecho-segun-derecho-civ-0205` |
| CIV-0206 | Escritura de extinción de pareja estable según el Derecho catalán | `escritura-extincion-pareja-estable-segun-derecho-civ-0206` |
| CIV-0207 | Escritura de constitución de pareja estable según el Derecho catalán | `escritura-constitucion-pareja-estable-segun-derecho-civ-0207` |
| CIV-0208 | Escritura de capítulos matrimoniales según el Derecho catalán | `escritura-capitulos-matrimoniales-segun-derecho-catalan-civ-0208` |
| CIV-0209 | Escritura de capítulos matrimoniales según el Derecho aragonés | `escritura-capitulos-matrimoniales-segun-derecho-civ-0209` |
| CIV-0210 | Escritura de reconocimiento de filiación de un hijo mayor de edad | `escritura-reconocimiento-filiacion-hijo-mayor-edad-civ-0210` |
| CIV-0211 | Convenio regulador de divorcio sin hijos con régimen de separación de bienes | `convenio-regulador-divorcio-sin-hijos-regimen-civ-0211` |
| CIV-0212 | Escritura de capitulaciones matrimoniales con régimen de participación | `escritura-capitulaciones-matrimoniales-regimen-civ-0212` |
| CIV-0213 | Acta notarial sobre la vivienda a efectos de reagrupación familiar | `acta-notarial-sobre-vivienda-efectos-reagrupacion-civ-0213` |
| CIV-0214 | Autorización notarial de viaje de un menor | `autorizacion-notarial-viaje-menor-civ-0214` |
| CIV-0215 | Convenio regulador de un matrimonio mixto entre español y extranjero | `convenio-regulador-matrimonio-mixto-entre-espanol-civ-0215` |
| CIV-0216 | Escritura de capitulaciones matrimoniales con reconciliación de los cónyuges | `escritura-capitulaciones-matrimoniales-reconciliacion-civ-0216` |
| CIV-0217 | Escritura de consentimiento para el ejercicio de la patria potestad | `escritura-consentimiento-ejercicio-patria-potestad-civ-0217` |
| CIV-0218 | Escritura por la que se revoca la emancipación | `escritura-revoca-emancipacion-civ-0218` |
| CIV-0219 | Escritura de emancipación de un menor | `escritura-emancipacion-menor-civ-0219` |
| CIV-0220 | Escritura de poder y consentimiento recíprocos entre cónyuges | `escritura-poder-consentimiento-reciprocos-entre-civ-0220` |
| CIV-0221 | Escritura de poder para vender bienes gananciales | `escritura-poder-vender-bienes-gananciales-civ-0221` |
| CIV-0222 | Escritura de poder para contraer matrimonio por representante | `escritura-poder-contraer-matrimonio-representante-civ-0222` |
| CIV-0223 | Convenio regulador de divorcio con custodia compartida y liquidación del régimen económico | `convenio-regulador-divorcio-custodia-compartida-civ-0223` |
| CIV-0224 | Convenio regulador de divorcio con hijos menores y liquidación del régimen económico matrimonial | `convenio-regulador-divorcio-hijos-menores-liquidacion-civ-0224` |
| CIV-0225 | Escritura de ratificación de la venta de bienes gananciales | `escritura-ratificacion-venta-bienes-gananciales-civ-0225` |
| CIV-0226 | Escritura de disposición de la vivienda privativa que es la habitual del matrimonio | `escritura-disposicion-vivienda-privativa-es-habitual-civ-0226` |
| CIV-0227 | Escritura de emancipación por concesión de quienes ejercen la patria potestad | `escritura-emancipacion-concesion-quienes-ejercen-civ-0227` |
| CIV-0228 | Otrosí de medidas provisionales coetáneas contenciosas en demanda de nulidad, separación o divorcio | `otrosi-medidas-provisionales-coetaneas-contenciosas-civ-0228` |
| CIV-0229 | Otrosí de medidas provisionales coetáneas convenidas en demanda de nulidad, separación o divorcio | `otrosi-medidas-provisionales-coetaneas-convenidas-civ-0229` |
| CIV-0230 | Contestación a la demanda de extinción de pareja de hecho sin hijos comunes | `contestacion-demanda-extincion-pareja-hecho-sin-hijos-civ-0230` |
| CIV-0231 | Contestación a la demanda de extinción de pareja de hecho sin hijos comunes en Cataluña | `contestacion-demanda-extincion-pareja-hecho-sin-hijos-civ-0231` |
| CIV-0232 | Demanda para hacer efectivo el derecho de relación con abuelos, hermanos y allegados (Cataluña) | `demanda-hacer-efectivo-derecho-relacion-abuelos-civ-0232` |
| CIV-0233 | Demanda del conviviente supérstite de pareja estable contra el heredero (Cataluña) | `demanda-conviviente-superstite-pareja-estable-contra-civ-0233` |
| CIV-0234 | Demanda por cese de convivencia de pareja estable de hecho con medidas cautelares (Derecho común) | `demanda-cese-convivencia-pareja-estable-hecho-medidas-civ-0234` |
| CIV-0235 | Demanda de extinción de pareja estable según el Derecho civil catalán | `demanda-extincion-pareja-estable-segun-derecho-civil-civ-0235` |
| CIV-0236 | Demanda por cese de la convivencia de pareja de hecho según el Derecho vasco | `demanda-cese-convivencia-pareja-hecho-segun-derecho-civ-0236` |
| CIV-0237 | Contestación a la demanda de extinción de pareja de hecho | `contestacion-demanda-extincion-pareja-hecho-civ-0237` |
| CIV-0238 | Solicitud de inventario en la liquidación del régimen matrimonial (comunicación foral vasca) | `solicitud-inventario-liquidacion-regimen-matrimonial-civ-0238` |
| CIV-0239 | Demanda de divorcio contencioso con compensación por razón de trabajo (Derecho civil catalán) | `demanda-divorcio-contencioso-compensacion-razon-civ-0239` |
| CIV-0240 | Demanda de guarda y custodia y alimentos de hijos menores (Derecho civil catalán) | `demanda-guarda-custodia-alimentos-hijos-menores-civ-0240` |
| CIV-0241 | Demanda de separación contenciosa con prestación compensatoria (Derecho civil catalán) | `demanda-separacion-contenciosa-prestacion-civ-0241` |
| CIV-0242 | Solicitud y propuesta de liquidación del régimen matrimonial por un cónyuge (foral vasca) | `solicitud-propuesta-liquidacion-regimen-matrimonial-civ-0242` |
| CIV-0243 | Solicitud de inventario en la liquidación de la sociedad de conquistas (Derecho foral navarro) | `solicitud-inventario-liquidacion-sociedad-conquistas-civ-0243` |
| CIV-0244 | Solicitud y propuesta de liquidación del régimen matrimonial por un cónyuge (conquistas, Navarra) | `solicitud-propuesta-liquidacion-regimen-matrimonial-civ-0244` |
| CIV-0245 | Solicitud y propuesta de liquidación del régimen matrimonial por un cónyuge (Derecho foral aragonés) | `solicitud-propuesta-liquidacion-regimen-matrimonial-civ-0245` |
| CIV-0246 | Contestación a la demanda de disolución del régimen matrimonial que impugna su determinación | `contestacion-demanda-disolucion-regimen-matrimonial-civ-0246` |
| CIV-0247 | Convenio de los cónyuges para liquidar la sociedad de gananciales | `convenio-conyuges-liquidar-sociedad-gananciales-civ-0247` |
| CIV-0248 | Solicitud de dispensa del impedimento matrimonial de parentesco | `solicitud-dispensa-impedimento-matrimonial-parentesco-civ-0248` |
| CIV-0249 | Solicitud de dispensa de impedimento una vez celebrado el matrimonio | `solicitud-dispensa-impedimento-vez-celebrado-matrimonio-civ-0249` |
| CIV-0250 | Demanda de mutuo acuerdo de medidas paternofiliales | `demanda-mutuo-acuerdo-medidas-paternofiliales-civ-0250` |
| CIV-0251 | Solicitud de modificar el régimen de visitas por incumplimiento del otro progenitor | `solicitud-modificar-regimen-visitas-incumplimiento-civ-0251` |
| CIV-0252 | Otrosí de demanda matrimonial que pide modificar las medidas provisionales previas | `otrosi-demanda-matrimonial-pide-modificar-medidas-civ-0252` |
| CIV-0253 | Solicitud de medidas provisionales previas a la demanda en un proceso de menores | `solicitud-medidas-provisionales-previas-demanda-civ-0253` |
| CIV-0254 | Expediente de jurisdicción voluntaria de medidas provisionales sobre menores (art. 158 CC) | `expediente-jurisdiccion-voluntaria-medidas-civ-0254` |
| CIV-0255 | Solicitud del representante legal del menor a la entidad pública para cesar el acogimiento | `solicitud-representante-legal-menor-entidad-publica-civ-0255` |
| CIV-0256 | Propuesta de liquidación del régimen económico matrimonial de participación | `propuesta-liquidacion-regimen-economico-matrimonial-civ-0256` |
| CIV-0257 | Demanda de guarda y custodia y alimentos de hijos menores | `demanda-guarda-custodia-alimentos-hijos-menores-civ-0257` |
| CIV-0258 | Demanda de divorcio contencioso sin acuerdo entre los cónyuges | `demanda-divorcio-contencioso-sin-acuerdo-entre-conyuges-civ-0258` |
| CIV-0259 | Solicitud de liquidación del régimen económico matrimonial por uno de los cónyuges | `solicitud-liquidacion-regimen-economico-matrimonial-civ-0259` |
| CIV-0260 | Demanda de eficacia civil de resolución pontificia de matrimonio rato y no consumado con medidas | `demanda-eficacia-civil-resolucion-pontificia-civ-0260` |
| CIV-0261 | Escrito para exigir el asentimiento necesario en la adopción | `escrito-exigir-asentimiento-necesario-adopcion-civ-0261` |
| CIV-0262 | Escrito que plantea la competencia de Violencia sobre la Mujer en un proceso matrimonial | `escrito-plantea-competencia-violencia-sobre-mujer-civ-0262` |
| CIV-0263 | Demanda de divorcio de mutuo acuerdo con hijos menores no emancipados | `demanda-divorcio-mutuo-acuerdo-hijos-menores-no-civ-0263` |
| CIV-0264 | Demanda de reclamación de filiación paterna | `demanda-reclamacion-filiacion-paterna-civ-0264` |
| CIV-0265 | Demanda de impugnación de la filiación paterna | `demanda-impugnacion-filiacion-paterna-civ-0265` |
| CIV-0266 | Escrito de contestación a la demanda de reclamación o impugnación de paternidad | `escrito-contestacion-demanda-reclamacion-impugnacion-civ-0266` |
| CIV-0267 | Escrito del tercero titular no registral de la vivienda familiar que se opone a su embargo | `escrito-tercero-titular-no-registral-vivienda-familiar-civ-0267` |
| CIV-0268 | Contestación a la demanda sobre los derechos del artículo 160 del Código Civil | `contestacion-demanda-sobre-derechos-articulo-160-civ-0268` |
| CIV-0269 | Convenio regulador de divorcio según el Derecho civil de Cataluña | `convenio-regulador-divorcio-segun-derecho-civil-civ-0269` |
| CIV-0270 | Demanda de divorcio contencioso según el Derecho civil catalán tras separación judicial previa | `demanda-divorcio-contencioso-segun-derecho-civil-civ-0270` |
| CIV-0271 | Solicitud de extender la inscripción marginal de sentencia de divorcio de otro Estado de la UE | `solicitud-extender-inscripcion-marginal-sentencia-civ-0271` |
| CIV-0272 | Demanda de divorcio de mutuo acuerdo de cónyuges extranjeros no comunitarios | `demanda-divorcio-mutuo-acuerdo-conyuges-extranjeros-no-civ-0272` |
| CIV-0273 | Demanda de separación contenciosa según el Derecho civil de Cataluña | `demanda-separacion-contenciosa-segun-derecho-civil-civ-0273` |
| CIV-0274 | Demanda de divorcio de mutuo acuerdo según el Derecho civil de Cataluña | `demanda-divorcio-mutuo-acuerdo-segun-derecho-civil-civ-0274` |
| CIV-0275 | Demanda de separación de mutuo acuerdo según el Derecho civil de Cataluña | `demanda-separacion-mutuo-acuerdo-segun-derecho-civil-civ-0275` |
| CIV-0276 | Demanda de divorcio contencioso según el Derecho civil catalán sin separación judicial previa | `demanda-divorcio-contencioso-segun-derecho-civil-civ-0276` |
| CIV-0277 | Convenio regulador con hijos menores y guarda y custodia exclusiva (propuesta) | `convenio-regulador-hijos-menores-guarda-custodia-civ-0277` |
| CIV-0278 | Demanda de juicio ordinario de privación de la patria potestad | `demanda-juicio-ordinario-privacion-patria-potestad-civ-0278` |
| CIV-0279 | Encabezamiento de demanda con procurador y padres como representantes de hijo menor | `encabezamiento-demanda-procurador-padres-como-civ-0279` |
| CIV-0280 | Demanda de alimentos de un progenitor contra el otro en nombre de hijos menores | `demanda-alimentos-progenitor-contra-otro-nombre-hijos-civ-0280` |
| CIV-0281 | Contestación del Fiscal a demanda de oposición a resolución administrativa de protección de menores | `contestacion-fiscal-demanda-oposicion-resolucion-civ-0281` |
| CIV-0282 | Cuaderno particional de la sociedad de gananciales disuelta, elaborado por el contador-partidor | `cuaderno-particional-sociedad-gananciales-disuelta-civ-0282` |
| CIV-0283 | Convenio regulador de separación según el Derecho civil de Cataluña | `convenio-regulador-separacion-segun-derecho-civil-civ-0283` |
| CIV-0284 | Divorcio contencioso sin separación judicial previa (demanda) | `divorcio-contencioso-sin-separacion-judicial-previa-civ-0284` |
| CIV-0285 | Solicitud de actualización de las pensiones fijadas judicialmente | `solicitud-actualizacion-pensiones-fijadas-judicialmente-civ-0285` |
| CIV-0286 | Oposición a la reclamación de actualización de pensiones fijadas judicialmente | `oposicion-reclamacion-actualizacion-pensiones-fijadas-civ-0286` |
| CIV-0287 | Contestación a la demanda de alimentos de un progenitor contra el otro para hijos menores | `contestacion-demanda-alimentos-progenitor-contra-otro-civ-0287` |
| CIV-0288 | Solicitud de autorización para retirar de la vivienda familiar bienes de uso personal | `solicitud-autorizacion-retirar-vivienda-familiar-civ-0288` |
| CIV-0289 | Solicitud de cumplimiento del régimen de visitas fijado en la sentencia de separación | `solicitud-cumplimiento-regimen-visitas-fijado-civ-0289` |
| CIV-0290 | Demanda de modificación de medidas por incumplimiento reiterado de visitas por el custodio | `demanda-modificacion-medidas-incumplimiento-reiterado-civ-0290` |
| CIV-0291 | Solicitud del cónyuge que dejó la vivienda por orden judicial de recuperar sus bienes personales | `solicitud-conyuge-dejo-vivienda-orden-judicial-civ-0291` |
| CIV-0292 | Solicitud de actualizar pensiones pidiendo oficio a la entidad pagadora para certificar los ingresos | `solicitud-actualizar-pensiones-pidiendo-oficio-entidad-civ-0292` |
| CIV-0293 | Solicitud de lanzamiento de la vivienda familiar en proceso matrimonial | `solicitud-lanzamiento-vivienda-familiar-proceso-civ-0293` |
| CIV-0294 | Ejecución de sentencia firme de separación, nulidad o divorcio (solicitud) | `ejecucion-sentencia-firme-separacion-nulidad-divorcio-civ-0294` |
| CIV-0295 | Solicitud de pago de lo embargado, con ampliación automática a nuevos vencimientos de pensiones | `solicitud-pago-lo-embargado-ampliacion-automatica-civ-0295` |
| CIV-0296 | Divorcio contencioso de cónyuges extranjeros comunitarios (demanda) | `divorcio-contencioso-conyuges-extranjeros-comunitarios-civ-0296` |
| CIV-0297 | Demanda de separación con hijos menores que sustituye por definitivas las medidas previas | `demanda-separacion-hijos-menores-sustituye-definitivas-civ-0297` |
| CIV-0298 | Demanda de reconocimiento de necesidad de asentimiento en la adopción, con suspensión del expediente | `demanda-reconocimiento-necesidad-asentimiento-adopcion-civ-0298` |
| CIV-0299 | Contestación a la demanda de modificación de medidas sobre aumento de gastos de los hijos | `contestacion-demanda-modificacion-medidas-sobre-civ-0299` |
| CIV-0300 | Solicitud conjunta de los cónyuges de suspender el proceso para acudir a mediación | `solicitud-conjunta-conyuges-suspender-proceso-acudir-civ-0300` |
| CIV-0301 | Demanda de separación o divorcio que pide ratificar medidas del Juzgado de Violencia sobre la Mujer | `demanda-separacion-divorcio-pide-ratificar-medidas-civ-0301` |
| CIV-0302 | Demanda de divorcio contencioso según el Derecho catalán con acción de división de cosa común | `demanda-divorcio-contencioso-segun-derecho-catalan-civ-0302` |
| CIV-0303 | Medidas provisionales previas a la demanda de separación con hijos menores y salida del otro cónyuge | `medidas-provisionales-previas-demanda-separacion-hijos-civ-0303` |
| CIV-0304 | Medidas provisionales previas a la separación con hijo mayor conviviente sin independencia económica | `medidas-provisionales-previas-separacion-hijo-mayor-civ-0304` |
| CIV-0305 | Medidas provisionales previas a la demanda de separación de matrimonio sin hijos (solicitud) | `medidas-provisionales-previas-demanda-separacion-civ-0305` |
| CIV-0306 | Solicitud al tribunal civil de remitir al eclesiástico certificación del auto de medidas | `solicitud-tribunal-civil-remitir-eclesiastico-civ-0306` |
| CIV-0307 | Testimonio para formar pieza separada de medidas provisionales pedidas en la demanda de separación | `testimonio-formar-pieza-separada-medidas-provisionales-civ-0307` |
| CIV-0308 | Solicitud de liquidación del régimen económico matrimonial de participación | `solicitud-liquidacion-regimen-economico-matrimonial-civ-0308` |
| CIV-0309 | Demanda contenciosa sobre relaciones paternofiliales tras ruptura de pareja de hecho | `demanda-contenciosa-sobre-relaciones-paternofiliales-civ-0309` |
| CIV-0310 | Demanda de divorcio contencioso de extranjeros no comunitarios residentes en España | `demanda-divorcio-contencioso-extranjeros-no-civ-0310` |
| CIV-0311 | Demanda de guarda y custodia de hijos menores no matrimoniales con medidas provisionales | `demanda-guarda-custodia-hijos-menores-no-matrimoniales-civ-0311` |
| CIV-0312 | Solicitud de liquidación de la sociedad de gananciales con propuesta de liquidación | `solicitud-liquidacion-sociedad-gananciales-propuesta-civ-0312` |
| CIV-0313 | Demanda de reconocimiento y ejecución de sentencia suiza de divorcio (tratado de 1896) | `demanda-reconocimiento-ejecucion-sentencia-suiza-civ-0313` |
| CIV-0314 | Solicitud de formar inventario para liquidar el régimen económico matrimonial | `solicitud-formar-inventario-liquidar-regimen-economico-civ-0314` |
| CIV-0315 | Formación de inventario sin controversia (acta) | `formacion-inventario-sin-controversia-acta-civ-0315` |
| CIV-0316 | Demanda de separación con hijos menores y solicitud simultánea de medidas provisionales | `demanda-separacion-hijos-menores-solicitud-simultanea-civ-0316` |
| CIV-0317 | Demanda de separación o divorcio que pide modificar medidas del Juzgado de Violencia sobre la Mujer | `demanda-separacion-divorcio-pide-modificar-medidas-civ-0317` |
| CIV-0318 | Demanda de divorcio de mutuo acuerdo de cónyuges extranjeros comunitarios | `demanda-divorcio-mutuo-acuerdo-conyuges-extranjeros-civ-0318` |
| CIV-0319 | Demanda conjunta de separación o divorcio de mutuo acuerdo con distintas opciones legales | `demanda-conjunta-separacion-divorcio-mutuo-acuerdo-civ-0319` |
| CIV-0320 | Demanda de divorcio contencioso de cónyuges extranjeros no comunitarios por fuero de los demandantes | `demanda-divorcio-contencioso-conyuges-extranjeros-no-civ-0320` |
| CIV-0321 | Escrito de contestación a la demanda de divorcio | `escrito-contestacion-demanda-divorcio-civ-0321` |
| CIV-0322 | Contestación a la demanda sobre comunicación y visitas de los abuelos con su nieto | `contestacion-demanda-sobre-comunicacion-visitas-civ-0322` |
| CIV-0323 | Contestación del Ministerio Fiscal a la demanda de separación matrimonial contenciosa | `contestacion-ministerio-fiscal-demanda-separacion-civ-0323` |
| CIV-0324 | Contestación a la reconvención del cónyuge demandado en separación matrimonial contenciosa | `contestacion-reconvencion-conyuge-demandado-separacion-civ-0324` |
| CIV-0325 | Demanda de mutuo acuerdo sobre guarda, custodia y alimentos de hijos tras ruptura de unión de hecho | `demanda-mutuo-acuerdo-sobre-guarda-custodia-alimentos-civ-0325` |
| CIV-0326 | Demanda de mutuo acuerdo de modificación de medidas definitivas sobre guarda y custodia | `demanda-mutuo-acuerdo-modificacion-medidas-definitivas-civ-0326` |
| CIV-0327 | Escrito que comunica al tribunal la reconciliación de los cónyuges | `escrito-comunica-tribunal-reconciliacion-conyuges-civ-0327` |
| CIV-0328 | Contestación a demanda de separación con hijo menor y mayor conviviente, y reconvención de divorcio | `contestacion-demanda-separacion-hijo-menor-mayor-civ-0328` |
| CIV-0329 | Demanda de oposición a resolución administrativa de protección de menores tras recabar el expediente | `demanda-oposicion-resolucion-administrativa-proteccion-civ-0329` |
| CIV-0330 | Demanda de nulidad matrimonial por defecto de forma con indemnización al cónyuge de buena fe | `demanda-nulidad-matrimonial-defecto-forma-civ-0330` |
| CIV-0331 | Demanda de nulidad matrimonial por error en la identidad o cualidades del cónyuge, con indemnización | `demanda-nulidad-matrimonial-error-identidad-cualidades-civ-0331` |
| CIV-0332 | Demanda de eficacia civil de sentencia eclesiástica de nulidad matrimonial con petición de medidas | `demanda-eficacia-civil-sentencia-eclesiastica-nulidad-civ-0332` |
| CIV-0333 | Oposición a la eficacia civil de sentencia canónica de nulidad sin petición de medidas | `oposicion-eficacia-civil-sentencia-canonica-nulidad-civ-0333` |
| CIV-0334 | Solicitud de actualizar la pensión de alimentos según el IPC con reclamación de atrasos | `solicitud-actualizar-pension-alimentos-segun-ipc-civ-0334` |
| CIV-0335 | Solicitud de ampliar las medidas de garantía del embargo a nuevos vencimientos de pensiones | `solicitud-ampliar-medidas-garantia-embargo-nuevos-civ-0335` |
| CIV-0336 | Medidas provisionales previas a la demanda de divorcio con hijo menor y riesgo para el solicitante | `medidas-provisionales-previas-demanda-divorcio-hijo-civ-0336` |
| CIV-0337 | Solicitud de ejecución del pronunciamiento sobre atribución del uso de la vivienda familiar | `solicitud-ejecucion-pronunciamiento-sobre-atribucion-civ-0337` |
| CIV-0338 | Solicitud de ejecución para que el ejecutado entregue los hijos a la madre custodia | `solicitud-ejecucion-ejecutado-entregue-hijos-madre-civ-0338` |
| CIV-0339 | Solicitud conjunta de pasar la separación o divorcio contencioso a procedimiento de mutuo acuerdo | `solicitud-conjunta-pasar-separacion-divorcio-civ-0339` |
| CIV-0340 | Demanda contenciosa de modificación de medidas sobre guarda y custodia con modificación provisional | `demanda-contenciosa-modificacion-medidas-sobre-guarda-civ-0340` |
| CIV-0341 | Demanda contenciosa de modificación de medidas para aumentar la pensión de alimentos del hijo menor | `demanda-contenciosa-modificacion-medidas-aumentar-civ-0341` |
| CIV-0342 | Demanda contenciosa de modificación de medidas para reducir la pensión compensatoria | `demanda-contenciosa-modificacion-medidas-reducir-civ-0342` |
| CIV-0343 | Demanda contenciosa de modificación de medidas para extinguir la pensión compensatoria | `demanda-contenciosa-modificacion-medidas-extinguir-civ-0343` |
| CIV-0344 | Demanda de divorcio contencioso sin separación previa, con solicitud de medidas provisionales | `demanda-divorcio-contencioso-sin-separacion-previa-civ-0344` |
| CIV-0345 | Demanda de divorcio contencioso con separación previa y modificación provisional de las medidas | `demanda-divorcio-contencioso-separacion-previa-civ-0345` |
| CIV-0346 | Demanda de divorcio contencioso tras separación judicial previa | `demanda-divorcio-contencioso-tras-separacion-judicial-civ-0346` |
| CIV-0347 | Escrito inicial de oposición a resolución administrativa de protección de menores | `escrito-inicial-oposicion-resolucion-administrativa-civ-0347` |
| CIV-0348 | Contestación que pide seguir el divorcio por mutuo acuerdo aportando convenio regulador | `contestacion-pide-seguir-divorcio-mutuo-acuerdo-civ-0348` |
| CIV-0349 | Demanda de modificación del convenio regulador pedida por ambos cónyuges o uno con el otro | `demanda-modificacion-convenio-regulador-pedida-ambos-civ-0349` |
| CIV-0350 | Solicitud de ejecución de resolución de proceso matrimonial por impago de pensiones | `solicitud-ejecucion-resolucion-proceso-matrimonial-civ-0350` |
| CIV-0351 | Solicitud de ejecución de prestaciones periódicas de la sentencia de separación y las provisionales | `solicitud-ejecucion-prestaciones-periodicas-sentencia-civ-0351` |
| CIV-0352 | Reconocimiento y ejecución en España de sentencia extranjera de alimentos (demanda) | `reconocimiento-ejecucion-espana-sentencia-extranjera-civ-0352` |
| CIV-0353 | Demanda de mutuo acuerdo sobre guarda y custodia de hijos menores tras ruptura de unión de hecho | `demanda-mutuo-acuerdo-sobre-guarda-custodia-hijos-civ-0353` |
| CIV-0354 | Certificación de la sentencia de nulidad dictada por el tribunal eclesiástico | `certificacion-sentencia-nulidad-dictada-tribunal-civ-0354` |
| CIV-0355 | Convenio regulador de la ruptura de pareja de hecho con hijos menores | `convenio-regulador-ruptura-pareja-hecho-hijos-menores-civ-0355` |
| CIV-0356 | Propuesta de modificación del convenio regulador de divorcio no aprobado en la sentencia | `propuesta-modificacion-convenio-regulador-divorcio-no-civ-0356` |
| CIV-0357 | Convenio regulador de separación de hecho en escritura con hijos menores y custodia exclusiva | `convenio-regulador-separacion-hecho-escritura-hijos-civ-0357` |
| CIV-0358 | Contrato de alimentos a favor de hijo con patria potestad prorrogada | `contrato-alimentos-favor-hijo-patria-potestad-civ-0358` |
| CIV-0359 | Demanda de juicio verbal sobre comunicación y visitas de los abuelos con su nieto menor | `demanda-juicio-verbal-sobre-comunicacion-visitas-civ-0359` |
| CIV-0360 | Demanda de juicio verbal sobre régimen de visitas con un hijo menor extramatrimonial | `demanda-juicio-verbal-sobre-regimen-visitas-hijo-menor-civ-0360` |
| CIV-0361 | Demanda de juicio ordinario para extinguir una adopción | `demanda-juicio-ordinario-extinguir-adopcion-civ-0361` |
| CIV-0362 | Convenio regulador de separación con régimen de comunicación de los hijos con los abuelos | `convenio-regulador-separacion-regimen-comunicacion-civ-0362` |
| CIV-0363 | Contrato de resarcimiento de gastos por incumplimiento de promesa de matrimonio | `contrato-resarcimiento-gastos-incumplimiento-promesa-civ-0363` |
| CIV-0364 | Contestación a demanda de juicio ordinario que pide rescindir la liquidación de gananciales | `contestacion-demanda-juicio-ordinario-pide-rescindir-civ-0364` |
| CIV-0365 | Capitulaciones matrimoniales posteriores al matrimonio que modifican el régimen económico (Bizkaia) | `capitulaciones-matrimoniales-posteriores-matrimonio-civ-0365` |
| CIV-0366 | Capitulaciones matrimoniales otorgadas ante notario antes del matrimonio | `capitulaciones-matrimoniales-otorgadas-ante-notario-civ-0366` |
| CIV-0367 | Demanda de juicio verbal para que el progenitor pague alimentos al hijo | `demanda-juicio-verbal-progenitor-pague-alimentos-hijo-civ-0367` |
| CIV-0368 | Demanda de la madre reclamando filiación no matrimonial del hijo menor sin posesión de estado | `demanda-madre-reclamando-filiacion-no-matrimonial-hijo-civ-0368` |
| CIV-0369 | Demanda del fiscal impugnando un reconocimiento de paternidad que encubre una adopción ilícita | `demanda-fiscal-impugnando-reconocimiento-paternidad-civ-0369` |
| CIV-0370 | Contestación del demandado como padre a la demanda de filiación no matrimonial | `contestacion-demandado-como-padre-demanda-filiacion-no-civ-0370` |
| CIV-0371 | Demanda del padre reclamando filiación de hijo menor difunto e impugnando otra filiación | `demanda-padre-reclamando-filiacion-hijo-menor-difunto-civ-0371` |
| CIV-0372 | Demanda para rescindir la liquidación de la sociedad conyugal por lesión en más de la cuarta parte | `demanda-rescindir-liquidacion-sociedad-conyugal-lesion-civ-0372` |

## Privacidad

Ver `PRIVACY.md`.
