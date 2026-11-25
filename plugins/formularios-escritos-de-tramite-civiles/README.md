# Escritos de trámite en el proceso civil

> Plugin de Claude Code `formularios-escritos-de-tramite-civiles` · **110 formularios** · Civil · normativa revisada el 25-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Para los escritos del día a día de un pleito civil: personación y apoderamiento, solicitudes al tribunal, suspensión, acumulación, recusación y abstención, sucesión procesal, subsanación, desistimiento y renuncia, comunicaciones y otrosíes.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva; el formulario seco, listo para rellenar, está en `assets/formulario.md` dentro de la carpeta de la skill.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 110 está al final):

- **Demandas, peticiones y solicitudes iniciales** (1). Por ejemplo: Solicitud de reconocimiento en España de una sentencia marroquí (Convenio de 1997).
- **Contestaciones, oposiciones y alegaciones** (1). Por ejemplo: Escrito de oposición a que se reconozca eficacia civil a la sentencia canónica de nulidad.
- **Estatutos, actas, certificaciones y escrituras** (5). Por ejemplo: Poder notarial general para pleitos y especial para otras facultades; Poder general para pleitos de una persona jurídica a favor de procuradores y abogados; Poder especial para pleitos de una persona jurídica a favor de procuradores y abogados.
- **Comunicaciones, requerimientos y cartas** (22). Por ejemplo: Solicitud de habilitación ad casum para actuar ante el Tribunal Eclesiástico; Solicitud de nuevo señalamiento del juicio ordinario por enfermedad del abogado (art. 430 LEC); Solicitud de acumulación de procesos seguidos ante el mismo tribunal.
- **Escritos de trámite y otros** (81). Por ejemplo: Escrito de proposición de diligencias finales; Escrito de subsanación de errores u omisiones; Escrito de subsanación por no presentar el modelo de autoliquidación de la tasa judicial.

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Escrito de personación en un procedimiento ya iniciado»
   - «Solicitud de suspensión del proceso por acuerdo de las partes»
   - «Escrito de desistimiento del demandante»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-escritos-de-tramite-civiles:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-escritos-de-tramite-civiles:poder-notarial-general-pleitos-especial-otras-civ-0861`. Los nombres están en la lista de formularios de abajo.

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
- **Espacio que ocupa:** unos 6.717 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-escritos-de-tramite-civiles@formularios-juridicos-civil-espana`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-civil-espana
/plugin install formularios-escritos-de-tramite-civiles@formularios-juridicos-civil-espana
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-civil-espana`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-escritos-de-tramite-civiles.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (110)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0861 | Poder notarial general para pleitos y especial para otras facultades | `poder-notarial-general-pleitos-especial-otras-civ-0861` |
| CIV-0867 | Escrito de proposición de diligencias finales | `escrito-proposicion-diligencias-finales-civ-0867` |
| CIV-0874 | Escrito de subsanación de errores u omisiones | `escrito-subsanacion-errores-u-omisiones-civ-0874` |
| CIV-0884 | Solicitud de habilitación ad casum para actuar ante el Tribunal Eclesiástico | `solicitud-habilitacion-ad-casum-actuar-ante-tribunal-civ-0884` |
| CIV-0887 | Escrito de subsanación por no presentar el modelo de autoliquidación de la tasa judicial | `escrito-subsanacion-no-presentar-modelo-civ-0887` |
| CIV-0888 | Escrito pidiendo suspender el proceso porque las partes inician negociaciones | `escrito-pidiendo-suspender-proceso-porque-partes-civ-0888` |
| CIV-0889 | Escrito de conformidad para dar eficacia civil a una resolución | `escrito-conformidad-dar-eficacia-civil-resolucion-civ-0889` |
| CIV-0893 | Escrito de solicitud de auxilio judicial | `escrito-solicitud-auxilio-judicial-civ-0893` |
| CIV-0894 | Otrosí que acompaña el modelo de autoliquidación por exención subjetiva de la tasa (Cataluña) | `otrosi-acompana-modelo-autoliquidacion-exencion-civ-0894` |
| CIV-0895 | Otrosí que anuncia el ingreso de la tasa de servicios de la Administración de Justicia (Cataluña) | `otrosi-anuncia-ingreso-tasa-servicios-administracion-civ-0895` |
| CIV-0896 | Escrito del procurador que aporta el acto de comunicación no entregado a su destinatario | `escrito-procurador-aporta-acto-comunicacion-no-civ-0896` |
| CIV-0898 | Solicitud de reconocimiento en España de una sentencia marroquí (Convenio de 1997) | `solicitud-reconocimiento-espana-sentencia-marroqui-civ-0898` |
| CIV-0900 | Escrito ante Violencia sobre la Mujer pidiendo que se requiera de inhibición a una sección civil | `escrito-ante-violencia-sobre-mujer-pidiendo-requiera-civ-0900` |
| CIV-0902 | Otrosí para que un procurador habilitado practique un acto de comunicación ante órgano exhortado | `otrosi-procurador-habilitado-practique-acto-civ-0902` |
| CIV-0903 | Escrito del actor que contesta al requerimiento por indebida acumulación de acciones | `escrito-actor-contesta-requerimiento-indebida-civ-0903` |
| CIV-0906 | Escrito del procurador que aporta la documentación de un acto de comunicación cumplimentado | `escrito-procurador-aporta-documentacion-acto-civ-0906` |
| CIV-0908 | Escrito que comunica el resultado negativo de un acto de comunicación y pide averiguar domicilio | `escrito-comunica-resultado-negativo-acto-comunicacion-civ-0908` |
| CIV-0909 | Escrito general de desistimiento | `escrito-general-desistimiento-civ-0909` |
| CIV-0929 | Solicitud de nuevo señalamiento del juicio ordinario por enfermedad del abogado (art. 430 LEC) | `solicitud-nuevo-senalamiento-juicio-ordinario-civ-0929` |
| CIV-0939 | Escrito que denuncia el retraso de un exhorto y solicita recordatorio de urgencia | `escrito-denuncia-retraso-exhorto-solicita-recordatorio-civ-0939` |
| CIV-0945 | Escrito de valoración y resumen de las diligencias finales en juicio ordinario | `escrito-valoracion-resumen-diligencias-finales-juicio-civ-0945` |
| CIV-0954 | Intervenciones de las partes y del tribunal para fijar los hechos controvertidos | `intervenciones-partes-tribunal-fijar-hechos-civ-0954` |
| CIV-0994 | Solicitud de acumulación de procesos seguidos ante el mismo tribunal | `solicitud-acumulacion-procesos-seguidos-ante-mismo-civ-0994` |
| CIV-0998 | Escrito que plantea cuestión incidental de especial pronunciamiento en juicio ordinario | `escrito-plantea-cuestion-incidental-especial-civ-0998` |
| CIV-0999 | Suspensión del juicio ordinario por prejudicialidad civil (solicitud) | `suspension-juicio-ordinario-prejudicialidad-civil-civ-0999` |
| CIV-1000 | Comunicación del procurador al tribunal de que cesa en su cargo por terminar el proceso | `comunicacion-procurador-tribunal-cesa-cargo-terminar-civ-1000` |
| CIV-1001 | Escrito de revocación expresa del poder del procurador | `escrito-revocacion-expresa-poder-procurador-civ-1001` |
| CIV-1004 | Escrito que subsana defectos de capacidad o representación (art. 418.1 LEC) | `escrito-subsana-defectos-capacidad-representacion-art-civ-1004` |
| CIV-1012 | Comunicación del procurador al tribunal del fallecimiento de su poderdante | `comunicacion-procurador-tribunal-fallecimiento-civ-1012` |
| CIV-1014 | Solicitud conjunta de suspensión del proceso por estar las partes en vías de acuerdo | `solicitud-conjunta-suspension-proceso-estar-partes-civ-1014` |
| CIV-1015 | Solicitud de intervención de un tercero en juicio ordinario o verbal | `solicitud-intervencion-tercero-juicio-ordinario-verbal-civ-1015` |
| CIV-1017 | Solicitud de tercero con interés legítimo de copia de un documento obrante en el proceso civil | `solicitud-tercero-interes-legitimo-copia-documento-civ-1017` |
| CIV-1018 | Solicitud del ejecutado subrogado de suceder al ejecutante en el proceso contra el codeudor | `solicitud-ejecutado-subrogado-suceder-ejecutante-civ-1018` |
| CIV-1022 | Solicitud de cooperación jurisdiccional internacional fuera de la UE y del Convenio de La Haya | `solicitud-cooperacion-jurisdiccional-internacional-civ-1022` |
| CIV-1027 | Solicitud del adquirente del objeto litigioso por cesión de crédito de suceder al transmitente | `solicitud-adquirente-objeto-litigioso-cesion-credito-civ-1027` |
| CIV-1034 | Escrito que pide rechazar la petición por abuso de derecho o fraude de ley frente al auto ejecutivo | `escrito-pide-rechazar-peticion-abuso-derecho-fraude-civ-1034` |
| CIV-1036 | Solicitud de caducidad de la instancia civil con desistimiento del actor | `solicitud-caducidad-instancia-civil-desistimiento-actor-civ-1036` |
| CIV-1038 | Solicitud de que se declare el carácter reservado de las actuaciones | `solicitud-declare-caracter-reservado-actuaciones-civ-1038` |
| CIV-1039 | Solicitud de celebrar determinadas actuaciones a puerta cerrada | `solicitud-celebrar-determinadas-actuaciones-puerta-civ-1039` |
| CIV-1041 | Solicitud de interrumpir un plazo por causa de fuerza mayor | `solicitud-interrumpir-plazo-causa-fuerza-mayor-civ-1041` |
| CIV-1043 | Escrito que subsana la indebida acumulación de acciones desistiendo de la no acumulable | `escrito-subsana-indebida-acumulacion-acciones-civ-1043` |
| CIV-1044 | Escrito que subsana la indebida acumulación de acciones manteniendo la segunda de forma eventual | `escrito-subsana-indebida-acumulacion-acciones-civ-1044` |
| CIV-1045 | Recusación de juez o magistrado en juicio ordinario por enemistad manifiesta | `recusacion-juez-magistrado-juicio-ordinario-enemistad-civ-1045` |
| CIV-1047 | Recusación de funcionario de la Administración de Justicia | `recusacion-funcionario-administracion-justicia-civ-1047` |
| CIV-1048 | Recusación del LAJ en juicio ordinario por enemistad manifiesta | `recusacion-laj-juicio-ordinario-enemistad-manifiesta-civ-1048` |
| CIV-1049 | Recusación del LAJ en juicio verbal por enemistad manifiesta | `recusacion-laj-juicio-verbal-enemistad-manifiesta-civ-1049` |
| CIV-1052 | Recusación de juez o magistrado en juicio verbal por enemistad manifiesta | `recusacion-juez-magistrado-juicio-verbal-enemistad-civ-1052` |
| CIV-1054 | Comunicación del procurador de su cese por carecer de habilitación para actuar en el recurso | `comunicacion-procurador-cese-carecer-habilitacion-civ-1054` |
| CIV-1055 | Escrito del procurador que cuestiona la existencia y validez de una revocación tácita de su poder | `escrito-procurador-cuestiona-existencia-validez-civ-1055` |
| CIV-1056 | Comunicación del Colegio de Procuradores al tribunal de la suspensión de un procurador por sanción | `comunicacion-colegio-procuradores-tribunal-suspension-civ-1056` |
| CIV-1057 | Comunicación del procurador al tribunal de una causa de incompatibilidad para representar a la parte | `comunicacion-procurador-tribunal-causa-civ-1057` |
| CIV-1058 | Solicitud de procurador de oficio por parte que alega derecho a justicia gratuita | `solicitud-procurador-oficio-parte-alega-derecho-civ-1058` |
| CIV-1061 | Personación de nuevo procurador por revocación tácita del anterior | `personacion-nuevo-procurador-revocacion-tacita-anterior-civ-1061` |
| CIV-1064 | Solicitud del beneficiario de justicia gratuita de abogado y procurador de oficio en verbal | `solicitud-beneficiario-justicia-gratuita-abogado-civ-1064` |
| CIV-1065 | Escrito del actor que niega la satisfacción extraprocesal de sus pretensiones | `escrito-actor-niega-satisfaccion-extraprocesal-civ-1065` |
| CIV-1073 | Solicitud de reanudar el curso de los autos | `solicitud-reanudar-curso-autos-civ-1073` |
| CIV-1074 | Solicitud conjunta de homologación judicial de la transacción que pone fin al litigio | `solicitud-conjunta-homologacion-judicial-transaccion-civ-1074` |
| CIV-1078 | Renuncia del actor a la acción ejercitada con petición de absolución en costas | `renuncia-actor-accion-ejercitada-peticion-absolucion-civ-1078` |
| CIV-1091 | Escrito pidiendo la traducción al castellano de las actuaciones redactadas en lengua cooficial | `escrito-pidiendo-traduccion-castellano-actuaciones-civ-1091` |
| CIV-1093 | Escrito que acompaña la autoliquidación de tasa judicial (modelo 696) presentada telemáticamente | `escrito-acompana-autoliquidacion-tasa-judicial-modelo-civ-1093` |
| CIV-1094 | Escrito pidiendo corregir por error material una resolución judicial | `escrito-pidiendo-corregir-error-material-resolucion-civ-1094` |
| CIV-1095 | Escrito que acompaña la autoliquidación de tasa judicial (modelo 696) | `escrito-acompana-autoliquidacion-tasa-judicial-modelo-civ-1095` |
| CIV-1096 | Escrito pidiendo la reconstrucción parcial de autos | `escrito-pidiendo-reconstruccion-parcial-autos-civ-1096` |
| CIV-1097 | Escrito pidiendo subsanar la omisión de una resolución para poder cumplirla | `escrito-pidiendo-subsanar-omision-resolucion-poder-civ-1097` |
| CIV-1098 | Escrito impugnando por excesivos los honorarios de abogado en un juicio de desahucio | `escrito-impugnando-excesivos-honorarios-abogado-juicio-civ-1098` |
| CIV-1099 | Escrito de minuta de honorarios del abogado | `escrito-minuta-honorarios-abogado-civ-1099` |
| CIV-1106 | Escrito pidiendo suspender el juicio ordinario por prejudicialidad penal genérica | `escrito-pidiendo-suspender-juicio-ordinario-civ-1106` |
| CIV-1108 | Escrito pidiendo comparecencia de las partes para convenir cómo realizar los bienes | `escrito-pidiendo-comparecencia-partes-convenir-como-civ-1108` |
| CIV-1110 | Escrito de resumen y valoración de las diligencias finales | `escrito-resumen-valoracion-diligencias-finales-civ-1110` |
| CIV-1115 | Escrito pidiendo una diligencia final extraordinaria (art. 435.2 LEC) | `escrito-pidiendo-diligencia-final-extraordinaria-art-civ-1115` |
| CIV-1124 | Escrito conjunto de las partes pidiendo la homologación de lo convenido extrajudicialmente | `escrito-conjunto-partes-pidiendo-homologacion-lo-civ-1124` |
| CIV-1128 | Escrito aportando documento anterior que no fue posible obtener con antelación (art. 270.1.3 LEC) | `escrito-aportando-documento-anterior-no-fue-posible-civ-1128` |
| CIV-1129 | Escrito pidiendo diligencia final ordinaria (art. 435.1.2.ª LEC) | `escrito-pidiendo-diligencia-final-ordinaria-art-435-1-civ-1129` |
| CIV-1130 | Escrito de la contraparte que niega el hecho alegado en la ampliación de hechos | `escrito-contraparte-niega-hecho-alegado-ampliacion-civ-1130` |
| CIV-1131 | Escrito de la contraparte que reconoce como cierto el hecho alegado en la ampliación de hechos | `escrito-contraparte-reconoce-como-cierto-hecho-alegado-civ-1131` |
| CIV-1132 | Escrito general de ampliación de hechos en juicio declarativo ordinario (art. 286 LEC) | `escrito-general-ampliacion-hechos-juicio-declarativo-civ-1132` |
| CIV-1136 | Escrito del actor que contesta a la alegación de nulidad del negocio en que funda su pretensión | `escrito-actor-contesta-alegacion-nulidad-negocio-funda-civ-1136` |
| CIV-1140 | Escrito de desistimiento bilateral en juicio ordinario | `escrito-desistimiento-bilateral-juicio-ordinario-civ-1140` |
| CIV-1142 | Escrito pidiendo nuevo señalamiento del juicio (art. 430 LEC) | `escrito-pidiendo-nuevo-senalamiento-juicio-art-430-lec-civ-1142` |
| CIV-2687 | Escrito que pide acumular el divorcio al proceso de modificación de medidas por conexión objetiva | `escrito-pide-acumular-divorcio-proceso-modificacion-civ-2687` |
| CIV-2688 | Escrito del poderdante que impugna la cuenta de derechos y suplidos de su procurador | `escrito-poderdante-impugna-cuenta-derechos-suplidos-civ-2688` |
| CIV-2690 | Escrito del abogado que reclama sus honorarios por el procedimiento de jura de cuentas | `escrito-abogado-reclama-honorarios-procedimiento-jura-civ-2690` |
| CIV-2691 | Escrito que pide acumular autos de distintos tribunales por prejudicialidad civil | `escrito-pide-acumular-autos-distintos-tribunales-civ-2691` |
| CIV-2692 | Escrito que pide acumular a este juicio otro seguido ante un tribunal distinto | `escrito-pide-acumular-este-juicio-otro-seguido-ante-civ-2692` |
| CIV-2693 | Escrito de alegaciones ante el tribunal superior en la discrepancia sobre acumulación | `escrito-alegaciones-ante-tribunal-superior-civ-2693` |
| CIV-2694 | Escrito que se opone a la acumulación de autos seguidos ante distintos tribunales | `escrito-opone-acumulacion-autos-seguidos-ante-civ-2694` |
| CIV-2696 | Escrito que pide sobreseer el juicio cambiario por cosa juzgada penal sobre la falsedad de la letra | `escrito-pide-sobreseer-juicio-cambiario-cosa-juzgada-civ-2696` |
| CIV-2697 | Escrito que pide levantar la suspensión por prejudicialidad penal tras archivarse la causa | `escrito-pide-levantar-suspension-prejudicialidad-penal-civ-2697` |
| CIV-2701 | Escrito que se opone a la cuestión incidental de previo pronunciamiento sobre capacidad procesal | `escrito-opone-cuestion-incidental-previo-civ-2701` |
| CIV-2702 | Escrito que plantea cuestión incidental de previo pronunciamiento suspensiva en juicio verbal | `escrito-plantea-cuestion-incidental-previo-civ-2702` |
| CIV-2706 | Petición de suspender el proceso civil por haberse planteado inhibitoria ante lo contencioso | `peticion-suspender-proceso-civil-haberse-planteado-civ-2706` |
| CIV-2707 | Escrito que comunica actos de violencia de género a la Sección Civil a efectos de inhibición | `escrito-comunica-actos-violencia-genero-seccion-civil-civ-2707` |
| CIV-2712 | Escrito de los cónyuges que aporta los documentos omitidos a requerimiento del tribunal | `escrito-conyuges-aporta-documentos-omitidos-civ-2712` |
| CIV-2713 | Escrito que pide comunicar al Registro Civil la sentencia de separación o divorcio de mutuo acuerdo | `escrito-pide-comunicar-registro-civil-sentencia-civ-2713` |
| CIV-2715 | Escrito que comunica la muerte de una parte del juicio de filiación y pide personar a sus herederos | `escrito-comunica-muerte-parte-juicio-filiacion-pide-civ-2715` |
| CIV-2720 | Escrito que pide examinar en apelación a la persona afectada por el proceso de medidas de apoyo | `escrito-pide-examinar-apelacion-persona-afectada-civ-2720` |
| CIV-2722 | Escrito de oposición a que se reconozca eficacia civil a la sentencia canónica de nulidad | `escrito-oposicion-reconozca-eficacia-civil-sentencia-civ-2722` |
| CIV-2723 | Escrito de los cónyuges con un nuevo convenio sobre los puntos que el juez no aprobó | `escrito-conyuges-nuevo-convenio-sobre-puntos-juez-no-civ-2723` |
| CIV-2727 | Escrito del Ministerio Fiscal que se opone a la transacción de las partes en el juicio de filiación | `escrito-ministerio-fiscal-opone-transaccion-partes-civ-2727` |
| CIV-2742 | Petición de suspender el juicio verbal por prejudicialidad penal al haberse iniciado una causa penal | `peticion-suspender-juicio-verbal-prejudicialidad-penal-civ-2742` |
| CIV-2743 | Petición de suspender el juicio por prejudicialidad penal ante la posible falsedad de un documento | `peticion-suspender-juicio-prejudicialidad-penal-ante-civ-2743` |
| CIV-2744 | Petición conjunta de las partes para suspender el curso del proceso | `peticion-conjunta-partes-suspender-curso-proceso-civ-2744` |
| CIV-2746 | Escrito conjunto que pide terminar el proceso por transacción y homologar el acuerdo | `escrito-conjunto-pide-terminar-proceso-transaccion-civ-2746` |
| CIV-2747 | Escrito que pide terminar el proceso por haberse alcanzado una transacción extrajudicial | `escrito-pide-terminar-proceso-haberse-alcanzado-civ-2747` |
| CIV-2750 | Poder general para pleitos de una persona jurídica a favor de procuradores y abogados | `poder-general-pleitos-persona-juridica-favor-civ-2750` |
| CIV-2751 | Poder especial para pleitos de una persona jurídica a favor de procuradores y abogados | `poder-especial-pleitos-persona-juridica-favor-civ-2751` |
| CIV-2752 | Poder para pleitos con facultad especial de declarar por el representante de una persona jurídica | `poder-pleitos-facultad-especial-declarar-representante-civ-2752` |
| CIV-2753 | Poder general para pleitos otorgado por una persona física a procurador y abogado | `poder-general-pleitos-otorgado-persona-fisica-civ-2753` |
| CIV-2754 | Escrito pidiendo la acumulación de autos en un proceso civil | `escrito-pidiendo-acumulacion-autos-proceso-civil-civ-2754` |
| CIV-2767 | Escrito del lesionado indemnizado tras contestar la aseguradora que renuncia a sus acciones | `escrito-lesionado-indemnizado-tras-contestar-civ-2767` |

## Privacidad

Ver `PRIVACY.md`.
