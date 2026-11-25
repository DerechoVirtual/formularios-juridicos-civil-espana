# Familia: separación, divorcio y medidas

> Plugin de Claude Code `formularios-familia-y-divorcio` · **236 formularios** · Civil · normativa revisada el 25-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Para las crisis matrimoniales: separación y divorcio de mutuo acuerdo o contencioso, nulidad matrimonial, convenio regulador, medidas provisionales y definitivas y su modificación, pensión compensatoria, uso de la vivienda familiar y su ejecución, con especialidades forales. Los asuntos de los hijos y la economía familiar tienen sus propios plugins.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva; el formulario seco, listo para rellenar, está en `assets/formulario.md` dentro de la carpeta de la skill.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 236 está al final):

- **Demandas, peticiones y solicitudes iniciales** (98). Por ejemplo: Solicitud de reconocimiento en España de una sentencia de divorcio colombiana (Convenio de 1908); Demanda de modificación de medidas definitivas porque el progenitor custodio cambia de domicilio; Demanda de nulidad canónica por grave defecto de discreción de juicio y prórroga de competencia.
- **Contestaciones, oposiciones y alegaciones** (31). Por ejemplo: Contestación a demanda de divorcio reconviniendo por la prestación compensatoria del Derecho catalán; Contestación a la demanda de modificación de medidas por cambio de domicilio del progenitor custodio; Contestación a la reconvención que pide indemnización por el artículo 98 del Código Civil.
- **Recursos** (6). Por ejemplo: Recurso de apelación contra sentencia que deniega la separación o divorcio, invocando la nueva ley; Recurso de reposición contra el auto que inadmite la reconvención sobre pensión compensatoria; Recurso de apelación para que se suprima la pensión compensatoria fijada en la sentencia.
- **Contratos, pactos y cláusulas** (15). Por ejemplo: Convenio regulador que recoge un acuerdo alcanzado en mediación; Contrato de mediación con acuerdos sobre los efectos del divorcio; Convenio regulador de un matrimonio mixto entre español y extranjero.
- **Estatutos, actas, certificaciones y escrituras** (14). Por ejemplo: Acta final de mediación con acuerdo en la ejecución de medidas definitivas de un proceso matrimonial; Acta final de mediación familiar con acuerdo sobre la pensión compensatoria; Acta notarial de notificación de ruptura y requerimiento para dejar sin efecto la escritura de unión.
- **Comunicaciones, requerimientos y cartas** (22). Por ejemplo: Burofax comunicando un cambio de domicilio; Solicitud de lanzamiento del ocupante en precario de la vivienda familiar tras separación o divorcio; Solicitud de dispensa pontificia de matrimonio rato y no consumado.
- **Escritos de trámite y otros** (50). Por ejemplo: Escrito conjunto para transformar el proceso matrimonial tras alcanzar un acuerdo en mediación; Escrito conjunto para homologar un acuerdo de mediación familiar en ejecución de medidas definitivas; Escrito de conclusiones en un proceso de nulidad matrimonial ante el Tribunal Eclesiástico.

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Demanda de divorcio de mutuo acuerdo con convenio regulador»
   - «Solicitud de medidas provisionales previas a la demanda de divorcio»
   - «Demanda de extinción de la pensión compensatoria»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-familia-y-divorcio:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-familia-y-divorcio:contestacion-demanda-divorcio-reconviniendo-prestacion-civ-0001`. Los nombres están en la lista de formularios de abajo.

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
- **Espacio que ocupa:** unos 14.624 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-familia-y-divorcio@formularios-juridicos-civil-espana`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-civil-espana
/plugin install formularios-familia-y-divorcio@formularios-juridicos-civil-espana
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-civil-espana`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-familia-y-divorcio.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (236)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0001 | Contestación a demanda de divorcio reconviniendo por la prestación compensatoria del Derecho catalán | `contestacion-demanda-divorcio-reconviniendo-prestacion-civ-0001` |
| CIV-0004 | Escrito conjunto para transformar el proceso matrimonial tras alcanzar un acuerdo en mediación | `escrito-conjunto-transformar-proceso-matrimonial-tras-civ-0004` |
| CIV-0005 | Escrito conjunto para homologar un acuerdo de mediación familiar en ejecución de medidas definitivas | `escrito-conjunto-homologar-acuerdo-mediacion-familiar-civ-0005` |
| CIV-0010 | Acta final de mediación con acuerdo en la ejecución de medidas definitivas de un proceso matrimonial | `acta-final-mediacion-acuerdo-ejecucion-medidas-civ-0010` |
| CIV-0011 | Convenio regulador que recoge un acuerdo alcanzado en mediación | `convenio-regulador-recoge-acuerdo-alcanzado-mediacion-civ-0011` |
| CIV-0021 | Solicitud de reconocimiento en España de una sentencia de divorcio colombiana (Convenio de 1908) | `solicitud-reconocimiento-espana-sentencia-divorcio-civ-0021` |
| CIV-0024 | Demanda de modificación de medidas definitivas porque el progenitor custodio cambia de domicilio | `demanda-modificacion-medidas-definitivas-porque-civ-0024` |
| CIV-0025 | Contestación a la demanda de modificación de medidas por cambio de domicilio del progenitor custodio | `contestacion-demanda-modificacion-medidas-cambio-civ-0025` |
| CIV-0026 | Burofax comunicando un cambio de domicilio | `burofax-comunicando-cambio-domicilio-civ-0026` |
| CIV-0029 | Acta final de mediación familiar con acuerdo sobre la pensión compensatoria | `acta-final-mediacion-familiar-acuerdo-sobre-pension-civ-0029` |
| CIV-0031 | Contestación a la reconvención que pide indemnización por el artículo 98 del Código Civil | `contestacion-reconvencion-pide-indemnizacion-articulo-civ-0031` |
| CIV-0032 | Contestación a la reconvención que pide prestación compensatoria según el Derecho catalán | `contestacion-reconvencion-pide-prestacion-civ-0032` |
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
| CIV-0046 | Demanda de divorcio contencioso con alimentos y vivienda para hijo mayor sin ingresos conviviente | `demanda-divorcio-contencioso-alimentos-vivienda-hijo-civ-0046` |
| CIV-0047 | Escrito de conclusiones en un proceso de nulidad matrimonial ante el Tribunal Eclesiástico | `escrito-conclusiones-proceso-nulidad-matrimonial-ante-civ-0047` |
| CIV-0048 | Demanda de desahucio por precario contra quien usa la vivienda familiar por sentencia matrimonial | `demanda-desahucio-precario-contra-quien-usa-vivienda-civ-0048` |
| CIV-0049 | Oposición oral al desahucio por precario de la vivienda familiar alegando fraude de ley | `oposicion-oral-desahucio-precario-vivienda-familiar-civ-0049` |
| CIV-0050 | Solicitud de lanzamiento del ocupante en precario de la vivienda familiar tras separación o divorcio | `solicitud-lanzamiento-ocupante-precario-vivienda-civ-0050` |
| CIV-0051 | Oposición a la solicitud de declarar un gasto extraordinario no previsto en las medidas | `oposicion-solicitud-declarar-gasto-extraordinario-no-civ-0051` |
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
| CIV-0069 | Otrosí de medidas provisionales sobre guarda y custodia en demanda de modificación de medidas | `otrosi-medidas-provisionales-sobre-guarda-custodia-civ-0069` |
| CIV-0074 | Contestación a la demanda de divorcio que pide modificar las medidas fijadas en la separación previa | `contestacion-demanda-divorcio-pide-modificar-medidas-civ-0074` |
| CIV-0075 | Demanda de divorcio de mutuo acuerdo que modifica las medidas acordadas en la separación previa | `demanda-divorcio-mutuo-acuerdo-modifica-medidas-civ-0075` |
| CIV-0080 | Propuesta de medidas por separación o divorcio contencioso (Derecho catalán) | `propuesta-medidas-separacion-divorcio-contencioso-civ-0080` |
| CIV-0081 | Acta notarial de notificación de ruptura y requerimiento para dejar sin efecto la escritura de unión | `acta-notarial-notificacion-ruptura-requerimiento-dejar-civ-0081` |
| CIV-0082 | Demanda de juicio ordinario para reclamar derechos sobre bienes adjudicados como privativos | `demanda-juicio-ordinario-reclamar-derechos-sobre-civ-0082` |
| CIV-0085 | Contestación a la demanda de nulidad matrimonial con oposición | `contestacion-demanda-nulidad-matrimonial-oposicion-civ-0085` |
| CIV-0086 | Contestación a la demanda de nulidad matrimonial con allanamiento | `contestacion-demanda-nulidad-matrimonial-allanamiento-civ-0086` |
| CIV-0088 | Demanda de nulidad del matrimonio cuando no hay hijos menores | `demanda-nulidad-matrimonio-cuando-no-hay-hijos-menores-civ-0088` |
| CIV-0089 | Demanda de extinción de convivencia con alimentos y pensión compensatoria (convivientes en Cataluña) | `demanda-extincion-convivencia-alimentos-pension-civ-0089` |
| CIV-0091 | Escrito de ejecución de sentencia por impago de pensión y su actualización | `escrito-ejecucion-sentencia-impago-pension-civ-0091` |
| CIV-0092 | Escrito del condenado que se opone a la actualización de la pensión y a los impagos reclamados | `escrito-condenado-opone-actualizacion-pension-impagos-civ-0092` |
| CIV-0093 | Escrito de oposición a la ejecución de medidas definitivas de familia | `escrito-oposicion-ejecucion-medidas-definitivas-familia-civ-0093` |
| CIV-0094 | Escrito con nueva propuesta de convenio regulador de separación o divorcio | `escrito-nueva-propuesta-convenio-regulador-separacion-civ-0094` |
| CIV-0096 | Demanda de divorcio contencioso con hijos menores y mayores dependientes y petición de medidas | `demanda-divorcio-contencioso-hijos-menores-mayores-civ-0096` |
| CIV-0097 | Demanda de separación presentada por un cónyuge sin el consentimiento del otro | `demanda-separacion-presentada-conyuge-sin-civ-0097` |
| CIV-0098 | Demanda de separación contenciosa con hijos menores y mayores dependientes y petición de medidas | `demanda-separacion-contenciosa-hijos-menores-mayores-civ-0098` |
| CIV-0099 | Demanda de separación contenciosa sin hijos con petición de medidas | `demanda-separacion-contenciosa-sin-hijos-peticion-civ-0099` |
| CIV-0100 | Solicitud de conversión del proceso de separación en divorcio tras la Ley 15 de 2005 | `solicitud-conversion-proceso-separacion-divorcio-tras-civ-0100` |
| CIV-0101 | Demanda de divorcio de un cónyuge con el consentimiento del otro y convenio regulador | `demanda-divorcio-conyuge-consentimiento-otro-convenio-civ-0101` |
| CIV-0102 | Escrito para alzar las medidas provisionales previas por no presentar la demanda en plazo | `escrito-alzar-medidas-provisionales-previas-no-civ-0102` |
| CIV-0108 | Contestación a la demanda de modificación de medidas de un proceso matrimonial (Derecho catalán) | `contestacion-demanda-modificacion-medidas-proceso-civ-0108` |
| CIV-0109 | Escrito para recuperar la posesión de la vivienda familiar por extinción del uso (Derecho catalán) | `escrito-recuperar-posesion-vivienda-familiar-extincion-civ-0109` |
| CIV-0124 | Demanda de modificación de las medidas definitivas de un proceso matrimonial (Derecho catalán) | `demanda-modificacion-medidas-definitivas-proceso-civ-0124` |
| CIV-0129 | Solicitud de informe del equipo psicosocial en el divorcio | `solicitud-informe-equipo-psicosocial-divorcio-civ-0129` |
| CIV-0130 | Escritura de poder especial entre cónyuges para vender un bien ganancial | `escritura-poder-especial-entre-conyuges-vender-bien-civ-0130` |
| CIV-0135 | Demanda de separación o divorcio que modifica las medidas dictadas por Violencia sobre la Mujer | `demanda-separacion-divorcio-modifica-medidas-dictadas-civ-0135` |
| CIV-0138 | Petición de reanudar divorcio o separación contenciosos suspendidos y convertirlos en mutuo acuerdo | `peticion-reanudar-divorcio-separacion-contenciosos-civ-0138` |
| CIV-0144 | Plan de parentalidad conforme al Derecho civil catalán | `plan-parentalidad-conforme-derecho-civil-catalan-civ-0144` |
| CIV-0145 | Demanda de extinción de la prestación compensatoria (Derecho civil catalán) | `demanda-extincion-prestacion-compensatoria-derecho-civ-0145` |
| CIV-0147 | Demanda para sustituir la cláusula de gastos extraordinarios por mayor pensión alimenticia | `demanda-sustituir-clausula-gastos-extraordinarios-civ-0147` |
| CIV-0149 | Demanda de suspensión temporal del pago de la pensión alimenticia | `demanda-suspension-temporal-pago-pension-alimenticia-civ-0149` |
| CIV-0150 | Demanda de reducción de la pensión alimenticia por el aumento de ingresos del progenitor custodio | `demanda-reduccion-pension-alimenticia-aumento-ingresos-civ-0150` |
| CIV-0151 | Demanda para suspender en verano el pago de la pensión alimenticia | `demanda-suspender-verano-pago-pension-alimenticia-civ-0151` |
| CIV-0152 | Demanda para sustituir la pensión fijada como porcentaje de ingresos por una cantidad fija | `demanda-sustituir-pension-fijada-como-porcentaje-civ-0152` |
| CIV-0153 | Solicitud de medidas judiciales por desacuerdo en la potestad parental (Derecho catalán) | `solicitud-medidas-judiciales-desacuerdo-potestad-civ-0153` |
| CIV-0154 | Demanda de divorcio contencioso con alimentos para hijos mayores de edad (Derecho catalán) | `demanda-divorcio-contencioso-alimentos-hijos-mayores-civ-0154` |
| CIV-0155 | Demanda de separación contenciosa con privación de la potestad parental (Derecho catalán) | `demanda-separacion-contenciosa-privacion-potestad-civ-0155` |
| CIV-0156 | Medidas provisionales previas a la demanda de nulidad, separación o divorcio (Derecho catalán) | `medidas-provisionales-previas-demanda-nulidad-civ-0156` |
| CIV-0163 | Propuesta de plan de parentalidad presentada por uno de los cónyuges | `propuesta-plan-parentalidad-presentada-uno-conyuges-civ-0163` |
| CIV-0164 | Demanda de extinción o reducción de la pensión alimenticia por disminución de ingresos del obligado | `demanda-extincion-reduccion-pension-alimenticia-civ-0164` |
| CIV-0166 | Demanda de divorcio de mutuo acuerdo tras una separación de mutuo acuerdo previa | `demanda-divorcio-mutuo-acuerdo-tras-separacion-mutuo-civ-0166` |
| CIV-0167 | Demanda de separación presentada con medidas provisionales previas vigentes | `demanda-separacion-presentada-medidas-provisionales-civ-0167` |
| CIV-0169 | Escrito de proposición de prueba en el procedimiento de separación contenciosa | `escrito-proposicion-prueba-procedimiento-separacion-civ-0169` |
| CIV-0170 | Escrito pidiendo testimonio de la sentencia y del convenio regulador en separación de mutuo acuerdo | `escrito-pidiendo-testimonio-sentencia-convenio-civ-0170` |
| CIV-0173 | Demanda de divorcio de mutuo acuerdo tras pacto en la comparecencia de medidas previas (Cataluña) | `demanda-divorcio-mutuo-acuerdo-tras-pacto-civ-0173` |
| CIV-0180 | Escritura de poder especial para contraer matrimonio | `escritura-poder-especial-contraer-matrimonio-civ-0180` |
| CIV-0182 | Escritura de revocación de poder especial para contraer matrimonio | `escritura-revocacion-poder-especial-contraer-matrimonio-civ-0182` |
| CIV-0184 | Contrato de mediación con acuerdos sobre los efectos del divorcio | `contrato-mediacion-acuerdos-sobre-efectos-divorcio-civ-0184` |
| CIV-0192 | Escrito de declaración de gastos extraordinarios en un proceso matrimonial | `escrito-declaracion-gastos-extraordinarios-proceso-civ-0192` |
| CIV-0195 | Demanda de juicio ordinario para anular el convenio regulador por vicio del consentimiento | `demanda-juicio-ordinario-anular-convenio-regulador-civ-0195` |
| CIV-0196 | Demanda contenciosa de modificación del convenio regulador para extinguir la pensión compensatoria | `demanda-contenciosa-modificacion-convenio-regulador-civ-0196` |
| CIV-0213 | Acta notarial sobre la vivienda a efectos de reagrupación familiar | `acta-notarial-sobre-vivienda-efectos-reagrupacion-civ-0213` |
| CIV-0215 | Convenio regulador de un matrimonio mixto entre español y extranjero | `convenio-regulador-matrimonio-mixto-entre-espanol-civ-0215` |
| CIV-0220 | Escritura de poder y consentimiento recíprocos entre cónyuges | `escritura-poder-consentimiento-reciprocos-entre-civ-0220` |
| CIV-0222 | Escritura de poder para contraer matrimonio por representante | `escritura-poder-contraer-matrimonio-representante-civ-0222` |
| CIV-0226 | Escritura de disposición de la vivienda privativa que es la habitual del matrimonio | `escritura-disposicion-vivienda-privativa-es-habitual-civ-0226` |
| CIV-0228 | Otrosí de medidas provisionales coetáneas contenciosas en demanda de nulidad, separación o divorcio | `otrosi-medidas-provisionales-coetaneas-contenciosas-civ-0228` |
| CIV-0229 | Otrosí de medidas provisionales coetáneas convenidas en demanda de nulidad, separación o divorcio | `otrosi-medidas-provisionales-coetaneas-convenidas-civ-0229` |
| CIV-0232 | Demanda para hacer efectivo el derecho de relación con abuelos, hermanos y allegados (Cataluña) | `demanda-hacer-efectivo-derecho-relacion-abuelos-civ-0232` |
| CIV-0239 | Demanda de divorcio contencioso con compensación por razón de trabajo (Derecho civil catalán) | `demanda-divorcio-contencioso-compensacion-razon-civ-0239` |
| CIV-0241 | Demanda de separación contenciosa con prestación compensatoria (Derecho civil catalán) | `demanda-separacion-contenciosa-prestacion-civ-0241` |
| CIV-0246 | Contestación a la demanda de disolución del régimen matrimonial que impugna su determinación | `contestacion-demanda-disolucion-regimen-matrimonial-civ-0246` |
| CIV-0248 | Solicitud de dispensa del impedimento matrimonial de parentesco | `solicitud-dispensa-impedimento-matrimonial-parentesco-civ-0248` |
| CIV-0249 | Solicitud de dispensa de impedimento una vez celebrado el matrimonio | `solicitud-dispensa-impedimento-vez-celebrado-matrimonio-civ-0249` |
| CIV-0250 | Demanda de mutuo acuerdo de medidas paternofiliales | `demanda-mutuo-acuerdo-medidas-paternofiliales-civ-0250` |
| CIV-0252 | Otrosí de demanda matrimonial que pide modificar las medidas provisionales previas | `otrosi-demanda-matrimonial-pide-modificar-medidas-civ-0252` |
| CIV-0253 | Solicitud de medidas provisionales previas a la demanda en un proceso de menores | `solicitud-medidas-provisionales-previas-demanda-civ-0253` |
| CIV-0254 | Expediente de jurisdicción voluntaria de medidas provisionales sobre menores (art. 158 CC) | `expediente-jurisdiccion-voluntaria-medidas-civ-0254` |
| CIV-0258 | Demanda de divorcio contencioso sin acuerdo entre los cónyuges | `demanda-divorcio-contencioso-sin-acuerdo-entre-conyuges-civ-0258` |
| CIV-0260 | Demanda de eficacia civil de resolución pontificia de matrimonio rato y no consumado con medidas | `demanda-eficacia-civil-resolucion-pontificia-civ-0260` |
| CIV-0262 | Escrito que plantea la competencia de Violencia sobre la Mujer en un proceso matrimonial | `escrito-plantea-competencia-violencia-sobre-mujer-civ-0262` |
| CIV-0263 | Demanda de divorcio de mutuo acuerdo con hijos menores no emancipados | `demanda-divorcio-mutuo-acuerdo-hijos-menores-no-civ-0263` |
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
| CIV-0283 | Convenio regulador de separación según el Derecho civil de Cataluña | `convenio-regulador-separacion-segun-derecho-civil-civ-0283` |
| CIV-0284 | Divorcio contencioso sin separación judicial previa (demanda) | `divorcio-contencioso-sin-separacion-judicial-previa-civ-0284` |
| CIV-0285 | Solicitud de actualización de las pensiones fijadas judicialmente | `solicitud-actualizacion-pensiones-fijadas-judicialmente-civ-0285` |
| CIV-0286 | Oposición a la reclamación de actualización de pensiones fijadas judicialmente | `oposicion-reclamacion-actualizacion-pensiones-fijadas-civ-0286` |
| CIV-0288 | Solicitud de autorización para retirar de la vivienda familiar bienes de uso personal | `solicitud-autorizacion-retirar-vivienda-familiar-civ-0288` |
| CIV-0291 | Solicitud del cónyuge que dejó la vivienda por orden judicial de recuperar sus bienes personales | `solicitud-conyuge-dejo-vivienda-orden-judicial-civ-0291` |
| CIV-0292 | Solicitud de actualizar pensiones pidiendo oficio a la entidad pagadora para certificar los ingresos | `solicitud-actualizar-pensiones-pidiendo-oficio-entidad-civ-0292` |
| CIV-0293 | Solicitud de lanzamiento de la vivienda familiar en proceso matrimonial | `solicitud-lanzamiento-vivienda-familiar-proceso-civ-0293` |
| CIV-0294 | Ejecución de sentencia firme de separación, nulidad o divorcio (solicitud) | `ejecucion-sentencia-firme-separacion-nulidad-divorcio-civ-0294` |
| CIV-0295 | Solicitud de pago de lo embargado, con ampliación automática a nuevos vencimientos de pensiones | `solicitud-pago-lo-embargado-ampliacion-automatica-civ-0295` |
| CIV-0296 | Divorcio contencioso de cónyuges extranjeros comunitarios (demanda) | `divorcio-contencioso-conyuges-extranjeros-comunitarios-civ-0296` |
| CIV-0297 | Demanda de separación con hijos menores que sustituye por definitivas las medidas previas | `demanda-separacion-hijos-menores-sustituye-definitivas-civ-0297` |
| CIV-0300 | Solicitud conjunta de los cónyuges de suspender el proceso para acudir a mediación | `solicitud-conjunta-conyuges-suspender-proceso-acudir-civ-0300` |
| CIV-0301 | Demanda de separación o divorcio que pide ratificar medidas del Juzgado de Violencia sobre la Mujer | `demanda-separacion-divorcio-pide-ratificar-medidas-civ-0301` |
| CIV-0302 | Demanda de divorcio contencioso según el Derecho catalán con acción de división de cosa común | `demanda-divorcio-contencioso-segun-derecho-catalan-civ-0302` |
| CIV-0303 | Medidas provisionales previas a la demanda de separación con hijos menores y salida del otro cónyuge | `medidas-provisionales-previas-demanda-separacion-hijos-civ-0303` |
| CIV-0304 | Medidas provisionales previas a la separación con hijo mayor conviviente sin independencia económica | `medidas-provisionales-previas-separacion-hijo-mayor-civ-0304` |
| CIV-0305 | Medidas provisionales previas a la demanda de separación de matrimonio sin hijos (solicitud) | `medidas-provisionales-previas-demanda-separacion-civ-0305` |
| CIV-0306 | Solicitud al tribunal civil de remitir al eclesiástico certificación del auto de medidas | `solicitud-tribunal-civil-remitir-eclesiastico-civ-0306` |
| CIV-0307 | Testimonio para formar pieza separada de medidas provisionales pedidas en la demanda de separación | `testimonio-formar-pieza-separada-medidas-provisionales-civ-0307` |
| CIV-0310 | Demanda de divorcio contencioso de extranjeros no comunitarios residentes en España | `demanda-divorcio-contencioso-extranjeros-no-civ-0310` |
| CIV-0311 | Demanda de guarda y custodia de hijos menores no matrimoniales con medidas provisionales | `demanda-guarda-custodia-hijos-menores-no-matrimoniales-civ-0311` |
| CIV-0313 | Demanda de reconocimiento y ejecución de sentencia suiza de divorcio (tratado de 1896) | `demanda-reconocimiento-ejecucion-sentencia-suiza-civ-0313` |
| CIV-0316 | Demanda de separación con hijos menores y solicitud simultánea de medidas provisionales | `demanda-separacion-hijos-menores-solicitud-simultanea-civ-0316` |
| CIV-0317 | Demanda de separación o divorcio que pide modificar medidas del Juzgado de Violencia sobre la Mujer | `demanda-separacion-divorcio-pide-modificar-medidas-civ-0317` |
| CIV-0318 | Demanda de divorcio de mutuo acuerdo de cónyuges extranjeros comunitarios | `demanda-divorcio-mutuo-acuerdo-conyuges-extranjeros-civ-0318` |
| CIV-0319 | Demanda conjunta de separación o divorcio de mutuo acuerdo con distintas opciones legales | `demanda-conjunta-separacion-divorcio-mutuo-acuerdo-civ-0319` |
| CIV-0320 | Demanda de divorcio contencioso de cónyuges extranjeros no comunitarios por fuero de los demandantes | `demanda-divorcio-contencioso-conyuges-extranjeros-no-civ-0320` |
| CIV-0321 | Escrito de contestación a la demanda de divorcio | `escrito-contestacion-demanda-divorcio-civ-0321` |
| CIV-0323 | Contestación del Ministerio Fiscal a la demanda de separación matrimonial contenciosa | `contestacion-ministerio-fiscal-demanda-separacion-civ-0323` |
| CIV-0324 | Contestación a la reconvención del cónyuge demandado en separación matrimonial contenciosa | `contestacion-reconvencion-conyuge-demandado-separacion-civ-0324` |
| CIV-0326 | Demanda de mutuo acuerdo de modificación de medidas definitivas sobre guarda y custodia | `demanda-mutuo-acuerdo-modificacion-medidas-definitivas-civ-0326` |
| CIV-0327 | Escrito que comunica al tribunal la reconciliación de los cónyuges | `escrito-comunica-tribunal-reconciliacion-conyuges-civ-0327` |
| CIV-0328 | Contestación a demanda de separación con hijo menor y mayor conviviente, y reconvención de divorcio | `contestacion-demanda-separacion-hijo-menor-mayor-civ-0328` |
| CIV-0330 | Demanda de nulidad matrimonial por defecto de forma con indemnización al cónyuge de buena fe | `demanda-nulidad-matrimonial-defecto-forma-civ-0330` |
| CIV-0331 | Demanda de nulidad matrimonial por error en la identidad o cualidades del cónyuge, con indemnización | `demanda-nulidad-matrimonial-error-identidad-cualidades-civ-0331` |
| CIV-0332 | Demanda de eficacia civil de sentencia eclesiástica de nulidad matrimonial con petición de medidas | `demanda-eficacia-civil-sentencia-eclesiastica-nulidad-civ-0332` |
| CIV-0333 | Oposición a la eficacia civil de sentencia canónica de nulidad sin petición de medidas | `oposicion-eficacia-civil-sentencia-canonica-nulidad-civ-0333` |
| CIV-0335 | Solicitud de ampliar las medidas de garantía del embargo a nuevos vencimientos de pensiones | `solicitud-ampliar-medidas-garantia-embargo-nuevos-civ-0335` |
| CIV-0336 | Medidas provisionales previas a la demanda de divorcio con hijo menor y riesgo para el solicitante | `medidas-provisionales-previas-demanda-divorcio-hijo-civ-0336` |
| CIV-0337 | Solicitud de ejecución del pronunciamiento sobre atribución del uso de la vivienda familiar | `solicitud-ejecucion-pronunciamiento-sobre-atribucion-civ-0337` |
| CIV-0339 | Solicitud conjunta de pasar la separación o divorcio contencioso a procedimiento de mutuo acuerdo | `solicitud-conjunta-pasar-separacion-divorcio-civ-0339` |
| CIV-0342 | Demanda contenciosa de modificación de medidas para reducir la pensión compensatoria | `demanda-contenciosa-modificacion-medidas-reducir-civ-0342` |
| CIV-0343 | Demanda contenciosa de modificación de medidas para extinguir la pensión compensatoria | `demanda-contenciosa-modificacion-medidas-extinguir-civ-0343` |
| CIV-0344 | Demanda de divorcio contencioso sin separación previa, con solicitud de medidas provisionales | `demanda-divorcio-contencioso-sin-separacion-previa-civ-0344` |
| CIV-0345 | Demanda de divorcio contencioso con separación previa y modificación provisional de las medidas | `demanda-divorcio-contencioso-separacion-previa-civ-0345` |
| CIV-0346 | Demanda de divorcio contencioso tras separación judicial previa | `demanda-divorcio-contencioso-tras-separacion-judicial-civ-0346` |
| CIV-0348 | Contestación que pide seguir el divorcio por mutuo acuerdo aportando convenio regulador | `contestacion-pide-seguir-divorcio-mutuo-acuerdo-civ-0348` |
| CIV-0349 | Demanda de modificación del convenio regulador pedida por ambos cónyuges o uno con el otro | `demanda-modificacion-convenio-regulador-pedida-ambos-civ-0349` |
| CIV-0350 | Solicitud de ejecución de resolución de proceso matrimonial por impago de pensiones | `solicitud-ejecucion-resolucion-proceso-matrimonial-civ-0350` |
| CIV-0351 | Solicitud de ejecución de prestaciones periódicas de la sentencia de separación y las provisionales | `solicitud-ejecucion-prestaciones-periodicas-sentencia-civ-0351` |
| CIV-0354 | Certificación de la sentencia de nulidad dictada por el tribunal eclesiástico | `certificacion-sentencia-nulidad-dictada-tribunal-civ-0354` |
| CIV-0356 | Propuesta de modificación del convenio regulador de divorcio no aprobado en la sentencia | `propuesta-modificacion-convenio-regulador-divorcio-no-civ-0356` |
| CIV-0357 | Convenio regulador de separación de hecho en escritura con hijos menores y custodia exclusiva | `convenio-regulador-separacion-hecho-escritura-hijos-civ-0357` |
| CIV-0362 | Convenio regulador de separación con régimen de comunicación de los hijos con los abuelos | `convenio-regulador-separacion-regimen-comunicacion-civ-0362` |
| CIV-0363 | Contrato de resarcimiento de gastos por incumplimiento de promesa de matrimonio | `contrato-resarcimiento-gastos-incumplimiento-promesa-civ-0363` |
| CIV-2199 | Convenio regulador de separación con custodia exclusiva y régimen de visitas | `convenio-regulador-separacion-custodia-exclusiva-civ-2199` |
| CIV-2200 | Convenio regulador de divorcio tras una separación matrimonial previa | `convenio-regulador-divorcio-tras-separacion-civ-2200` |
| CIV-2201 | Convenio regulador de las medidas sobre un hijo no matrimonial | `convenio-regulador-medidas-sobre-hijo-no-matrimonial-civ-2201` |
| CIV-2202 | Convenio regulador para la separación de los cónyuges | `convenio-regulador-separacion-conyuges-civ-2202` |
| CIV-2203 | Escritura por la que un cónyuge vende al otro un bien ganancial o privativo | `escritura-conyuge-vende-otro-bien-ganancial-privativo-civ-2203` |
| CIV-2205 | Escrito conjunto de los cónyuges que comunican su reconciliación tras concluir la separación | `escrito-conjunto-conyuges-comunican-reconciliacion-civ-2205` |
| CIV-2206 | Escrito conjunto de los cónyuges que comunican su reconciliación durante el proceso de separación | `escrito-conjunto-conyuges-comunican-reconciliacion-civ-2206` |
| CIV-2207 | Escrito conjunto de los cónyuges que comunican su reconciliación durante el proceso de divorcio | `escrito-conjunto-conyuges-comunican-reconciliacion-civ-2207` |
| CIV-2208 | Recurso de apelación contra sentencia que deniega la separación o divorcio, invocando la nueva ley | `recurso-apelacion-contra-sentencia-deniega-separacion-civ-2208` |
| CIV-2209 | Contestación con reconvención a la demanda de divorcio y petición de medidas provisionales | `contestacion-reconvencion-demanda-divorcio-peticion-civ-2209` |
| CIV-2210 | Contestación a la demanda de separación con reconvención que pide el divorcio | `contestacion-demanda-separacion-reconvencion-pide-civ-2210` |
| CIV-2211 | Demanda de separación con medidas provisionales y pensión compensatoria temporal | `demanda-separacion-medidas-provisionales-pension-civ-2211` |
| CIV-2212 | Demanda de separación con pensión compensatoria en una prestación única | `demanda-separacion-pension-compensatoria-prestacion-civ-2212` |
| CIV-2213 | Demanda de separación de uno de los cónyuges pasados tres meses desde la boda | `demanda-separacion-uno-conyuges-pasados-tres-meses-civ-2213` |
| CIV-2214 | Demanda de divorcio con medidas provisionales y pensión compensatoria temporal | `demanda-divorcio-medidas-provisionales-pension-civ-2214` |
| CIV-2215 | Demanda de separación por riesgo para la integridad física, con pensión y medidas provisionales | `demanda-separacion-riesgo-integridad-fisica-pension-civ-2215` |
| CIV-2216 | Demanda de separación con medidas provisionales y pensión compensatoria indefinida | `demanda-separacion-medidas-provisionales-pension-civ-2216` |
| CIV-2217 | Demanda de separación presentada por el tutor de uno de los cónyuges | `demanda-separacion-presentada-tutor-uno-conyuges-civ-2217` |
| CIV-2218 | Demanda de divorcio por riesgo para la integridad física, con pensión y medidas provisionales | `demanda-divorcio-riesgo-integridad-fisica-pension-civ-2218` |
| CIV-2219 | Demanda de divorcio de uno de los cónyuges pasados tres meses desde la boda | `demanda-divorcio-uno-conyuges-pasados-tres-meses-desde-civ-2219` |
| CIV-2220 | Demanda de divorcio presentada por el tutor de uno de los cónyuges | `demanda-divorcio-presentada-tutor-uno-conyuges-civ-2220` |
| CIV-2221 | Demanda de divorcio con medidas provisionales y pensión compensatoria en una prestación única | `demanda-divorcio-medidas-provisionales-pension-civ-2221` |
| CIV-2222 | Demanda de divorcio con medidas provisionales y pensión compensatoria indefinida | `demanda-divorcio-medidas-provisionales-pension-civ-2222` |
| CIV-2223 | Otrosí que pide oír al hijo menor en el proceso de modificación de medidas definitivas | `otrosi-pide-oir-hijo-menor-proceso-modificacion-civ-2223` |
| CIV-2224 | Contestación oponiendo justa causa a la demanda de los abuelos para relacionarse con los nietos | `contestacion-oponiendo-justa-causa-demanda-abuelos-civ-2224` |
| CIV-2226 | Contestación que pide un régimen de relación con los abuelos más limitado que el solicitado | `contestacion-pide-regimen-relacion-abuelos-mas-civ-2226` |
| CIV-2232 | Contestación a la demanda que reclama la mitad de los bienes adquiridos durante la convivencia | `contestacion-demanda-reclama-mitad-bienes-adquiridos-civ-2232` |
| CIV-2234 | Demanda de desahucio por precario contra el conviviente que ocupa la vivienda tras morir su pareja | `demanda-desahucio-precario-contra-conviviente-ocupa-civ-2234` |
| CIV-2235 | Carta al arrendador que comunica la subrogación del cónyuge al que se atribuyó la vivienda familiar | `carta-arrendador-comunica-subrogacion-conyuge-atribuyo-civ-2235` |
| CIV-2238 | Solicitud sin abogado ni procurador de medidas previas a la nulidad, separación o divorcio | `solicitud-sin-abogado-ni-procurador-medidas-previas-civ-2238` |
| CIV-2243 | Demanda para que se reconozca eficacia civil a la sentencia canónica de nulidad matrimonial | `demanda-reconozca-eficacia-civil-sentencia-canonica-civ-2243` |
| CIV-2245 | Recurso de reposición contra el auto que inadmite la reconvención sobre pensión compensatoria | `recurso-reposicion-contra-auto-inadmite-reconvencion-civ-2245` |
| CIV-2246 | Recurso de apelación para que se suprima la pensión compensatoria fijada en la sentencia | `recurso-apelacion-suprima-pension-compensatoria-fijada-civ-2246` |
| CIV-2247 | Recurso de apelación contra las medidas acordadas en la sentencia de separación o divorcio | `recurso-apelacion-contra-medidas-acordadas-sentencia-civ-2247` |
| CIV-2251 | Demanda de juicio verbal del hijo mayor de edad que reclama alimentos a sus padres divorciados | `demanda-juicio-verbal-hijo-mayor-edad-reclama-civ-2251` |
| CIV-2252 | Solicitud de medidas provisionales previas a la nulidad, separación o divorcio con hijos menores | `solicitud-medidas-provisionales-previas-nulidad-civ-2252` |
| CIV-2253 | Demanda de medidas provisionales coetáneas a la separación, nulidad o divorcio con hijos menores | `demanda-medidas-provisionales-coetaneas-separacion-civ-2253` |
| CIV-2259 | Demanda de medidas provisionales coetáneas a la separación o divorcio con alimentos a hijos mayores | `demanda-medidas-provisionales-coetaneas-separacion-civ-2259` |
| CIV-2260 | Otrosí de la contestación a la demanda matrimonial que pide medidas provisionales sobre la custodia | `otrosi-contestacion-demanda-matrimonial-pide-medidas-civ-2260` |
| CIV-2263 | Demanda de nulidad matrimonial por error en las cualidades personales del otro contrayente | `demanda-nulidad-matrimonial-error-cualidades-civ-2263` |
| CIV-2269 | Demanda de divorcio tras una separación previa en matrimonio sin hijos | `demanda-divorcio-tras-separacion-previa-matrimonio-sin-civ-2269` |
| CIV-2270 | Demanda de ejecución de la entrega del uso de la vivienda familiar y su anotación registral | `demanda-ejecucion-entrega-uso-vivienda-familiar-civ-2270` |
| CIV-2271 | Petición de que se anote la sentencia matrimonial en el Registro de la Propiedad y en el Mercantil | `peticion-anote-sentencia-matrimonial-registro-civ-2271` |
| CIV-2280 | Demanda de eficacia civil de la nulidad canónica pidiendo adoptar o modificar medidas provisionales | `demanda-eficacia-civil-nulidad-canonica-pidiendo-civ-2280` |
| CIV-2281 | Otrosí de la demanda matrimonial que pide aprobar las medidas provisionales pactadas | `otrosi-demanda-matrimonial-pide-aprobar-medidas-civ-2281` |
| CIV-2282 | Otrosí de la demanda matrimonial que solicita medidas provisionales cuando hay hijos menores | `otrosi-demanda-matrimonial-solicita-medidas-civ-2282` |
| CIV-2283 | Otrosí de la demanda de nulidad, separación o divorcio que solicita medidas provisionales | `otrosi-demanda-nulidad-separacion-divorcio-solicita-civ-2283` |
| CIV-2284 | Petición de anotar al margen en el Registro Civil la sentencia de nulidad, separación o divorcio | `peticion-anotar-margen-registro-civil-sentencia-civ-2284` |
| CIV-2286 | Demanda de ejecución del uso de la vivienda familiar alquilada con anotación y aviso al arrendador | `demanda-ejecucion-uso-vivienda-familiar-alquilada-civ-2286` |
| CIV-2289 | Demanda de medidas provisionales con hijos menores y petición de litisexpensas | `demanda-medidas-provisionales-hijos-menores-peticion-civ-2289` |
| CIV-2293 | Convenio regulador de divorcio con hijo muy pequeño y custodia prevista si enferma el custodio | `convenio-regulador-divorcio-hijo-muy-pequeno-custodia-civ-2293` |
| CIV-2296 | Escritura de compraventa entre cónyuges de vivienda privativa y ganancial tras la liquidación | `escritura-compraventa-entre-conyuges-vivienda-civ-2296` |
| CIV-2298 | Convenio regulador de separación con hijos menores que fija una pensión compensatoria | `convenio-regulador-separacion-hijos-menores-fija-civ-2298` |
| CIV-2305 | Escritura por la que un cónyuge revoca al otro el poder general de administración y disposición | `escritura-conyuge-revoca-otro-poder-general-civ-2305` |
| CIV-2311 | Recurso ante la Dirección General de los Registros contra la resolución de un Consulado | `recurso-ante-direccion-general-registros-contra-civ-2311` |
| CIV-2313 | Recurso ante la DGRN contra la denegación de inscribir la nacionalidad por opción | `recurso-ante-dgrn-contra-denegacion-inscribir-civ-2313` |

## Privacidad

Ver `PRIVACY.md`.
