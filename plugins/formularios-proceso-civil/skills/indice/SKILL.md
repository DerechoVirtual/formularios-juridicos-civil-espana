---
name: indice
description: "Índice de los 289 formularios de Proceso civil: demandas, contestaciones, prueba y vista. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Proceso civil: demandas, contestaciones, prueba y vista: índice de formularios

> Plugin `formularios-proceso-civil` · 289 formularios · normativa revisada el 24-11-2026.

## Qué es

Para tramitar un pleito civil de principio a fin: demandas y contestaciones (ordinario y verbal), reconvención, excepciones procesales, declinatoria, audiencia previa, proposición y práctica de prueba, conclusiones, acumulación, desistimiento, allanamiento y escritos de trámite.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Contestación a la demanda de juicio ordinario con reconvención»
- «Escrito de proposición de prueba en el juicio verbal»
- «Declinatoria por falta de competencia territorial»

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

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-proceso-civil:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario está al final de ese fichero y la guía del tema es el `marco.md` de esta carpeta.

### Demandas, peticiones y solicitudes iniciales (18)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0862 | Demanda de juicio ordinario por intromisión ilegítima en el derecho al honor | `demanda-juicio-ordinario-intromision-ilegitima-derecho-civ-0862` |
| CIV-0863 | Demanda de juicio ordinario para reivindicar un título nobiliario | `demanda-juicio-ordinario-reivindicar-titulo-nobiliario-civ-0863` |
| CIV-0864 | Demanda de juicio verbal para rectificar hechos difundidos en un medio de comunicación | `demanda-juicio-verbal-rectificar-hechos-difundidos-civ-0864` |
| CIV-0865 | Demanda de juicio verbal para reivindicar la devolución de un bien mueble (ordenador personal) | `demanda-juicio-verbal-reivindicar-devolucion-bien-civ-0865` |
| CIV-0875 | Demanda de juicio verbal para reclamar los gastos del sepelio | `demanda-juicio-verbal-reclamar-gastos-sepelio-civ-0875` |
| CIV-0898 | Solicitud de reconocimiento en España de una sentencia marroquí (Convenio de 1997) | `solicitud-reconocimiento-espana-sentencia-marroqui-civ-0898` |
| CIV-0923 | Demanda de juicio verbal de rectificación de hechos con domicilios para notificaciones | `demanda-juicio-verbal-rectificacion-hechos-domicilios-civ-0923` |
| CIV-0950 | Demanda de juicio ordinario de tutela del derecho fundamental al secreto de las comunicaciones | `demanda-juicio-ordinario-tutela-derecho-fundamental-civ-0950` |
| CIV-0983 | Demanda ordinaria de beneficiario de justicia gratuita que anuncia prueba pericial (art. 339.1 LEC) | `demanda-ordinaria-beneficiario-justicia-gratuita-civ-0983` |
| CIV-0992 | Demanda con acumulación de acciones | `demanda-acumulacion-acciones-civ-0992` |
| CIV-1002 | Demanda general de juicio verbal por razón de la cuantía | `demanda-general-juicio-verbal-razon-cuantia-civ-1002` |
| CIV-1007 | Demanda de declaración de error judicial (art. 293 LOPJ) | `demanda-declaracion-error-judicial-art-293-lopj-civ-1007` |
| CIV-1019 | Demanda de juicio ordinario con acumulación subjetiva de acciones por daños de circulación | `demanda-juicio-ordinario-acumulacion-subjetiva-civ-1019` |
| CIV-1020 | Demanda de juicio verbal de desahucio por falta de pago con acumulación de reclamación de cantidades | `demanda-juicio-verbal-desahucio-falta-pago-acumulacion-civ-1020` |
| CIV-1021 | Demanda de juicio ordinario que acumula reclamación de cantidad y de daños y perjuicios | `demanda-juicio-ordinario-acumula-reclamacion-cantidad-civ-1021` |
| CIV-1042 | Demanda de juicio ordinario con acumulación de pretensiones incompatibles | `demanda-juicio-ordinario-acumulacion-pretensiones-civ-1042` |
| CIV-1105 | Demanda del procurador contra su poderdante para reclamar provisión de fondos | `demanda-procurador-contra-poderdante-reclamar-civ-1105` |
| CIV-1121 | Demanda genérica de juicio ordinario | `demanda-generica-juicio-ordinario-civ-1121` |

### Contestaciones, oposiciones y alegaciones (26)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0872 | Alegaciones frente a la solicitud de complemento de una resolución procesal | `alegaciones-frente-solicitud-complemento-resolucion-civ-0872` |
| CIV-0882 | Contestación a la demanda alegando litispendencia internacional (artículo 29 Bruselas I bis) | `contestacion-demanda-alegando-litispendencia-civ-0882` |
| CIV-0904 | Oposición a la acumulación de procesos ante el mismo tribunal | `oposicion-acumulacion-procesos-ante-mismo-tribunal-civ-0904` |
| CIV-0905 | Oposición a la acumulación de procesos que se tramitan ante tribunales distintos | `oposicion-acumulacion-procesos-tramitan-ante-civ-0905` |
| CIV-0928 | Contestación a la cuestión incidental de previo pronunciamiento por falta de capacidad del actor | `contestacion-cuestion-incidental-previo-civ-0928` |
| CIV-0938 | Oposición a la tacha de testigo en el juicio ordinario | `oposicion-tacha-testigo-juicio-ordinario-civ-0938` |
| CIV-0948 | Contestación a la demanda de juicio ordinario con oposición por disconformidad en los hechos | `contestacion-demanda-juicio-ordinario-oposicion-civ-0948` |
| CIV-0949 | Contestación a la demanda ordinaria conforme en los hechos y opuesta en los fundamentos de derecho | `contestacion-demanda-ordinaria-conforme-hechos-opuesta-civ-0949` |
| CIV-0964 | Oposición del demandante a la excepción de litispendencia o cosa juzgada, con resolución y protesta | `oposicion-demandante-excepcion-litispendencia-cosa-civ-0964` |
| CIV-0967 | Oposición del demandante a la excepción de falta de litisconsorcio pasivo necesario | `oposicion-demandante-excepcion-falta-litisconsorcio-civ-0967` |
| CIV-0969 | Alegación en la audiencia previa de falta de capacidad del actor por carecer de personalidad | `alegacion-audiencia-previa-falta-capacidad-actor-civ-0969` |
| CIV-0970 | Alegaciones complementarias del demandante en la audiencia previa, oposición y resolución | `alegaciones-complementarias-demandante-audiencia-civ-0970` |
| CIV-0977 | Alegación del demandante de un hecho de nueva noticia en la audiencia previa, y oposición | `alegacion-demandante-hecho-nueva-noticia-audiencia-civ-0977` |
| CIV-0985 | Contestación a la reconvención formulada por quien no es demandante, oponiendo falta de legitimación | `contestacion-reconvencion-formulada-quien-no-es-civ-0985` |
| CIV-0986 | Contestación del demandante a la reconvención oponiendo excepciones procesales | `contestacion-demandante-reconvencion-oponiendo-civ-0986` |
| CIV-0987 | Contestación del demandante a la reconvención oponiendo excepciones de fondo | `contestacion-demandante-reconvencion-oponiendo-civ-0987` |
| CIV-0991 | Contestación del demandante a la declinatoria aportando documentos | `contestacion-demandante-declinatoria-aportando-civ-0991` |
| CIV-1026 | Oposición del demandado al desistimiento por incomparecencia de los sucesores del actor fallecido | `oposicion-demandado-desistimiento-incomparecencia-civ-1026` |
| CIV-1028 | Oposición de los coejecutados a que el deudor solidario suceda como ejecutante en el proceso | `oposicion-coejecutados-deudor-solidario-suceda-como-civ-1028` |
| CIV-1046 | Oposición a la causa de recusación del LAJ propuesta por la parte contraria | `oposicion-causa-recusacion-laj-propuesta-parte-civ-1046` |
| CIV-1075 | Oposición del demandado al desistimiento con petición de costas, antes de contestar a la demanda | `oposicion-demandado-desistimiento-peticion-costas-civ-1075` |
| CIV-1114 | Contestación a la demanda con oposición a la acumulación de acciones hecha en la ampliación | `contestacion-demanda-oposicion-acumulacion-acciones-civ-1114` |
| CIV-1126 | Alegaciones de la contraparte sobre una sentencia aportada tras las conclusiones (art. 271.2 LEC) | `alegaciones-contraparte-sobre-sentencia-aportada-tras-civ-1126` |
| CIV-1133 | Contestación a la demanda con oposición a la acumulación de acciones planteada en la propia demanda | `contestacion-demanda-oposicion-acumulacion-acciones-civ-1133` |
| CIV-1137 | Contestación a la demanda alegando compensación de deudas en una compraventa de mercancías | `contestacion-demanda-alegando-compensacion-deudas-civ-1137` |
| CIV-1144 | Escrito de oposición a la tacha de un testigo (art. 379.2 LEC) | `escrito-oposicion-tacha-testigo-art-379-2-lec-civ-1144` |

### Estatutos, actas, certificaciones y escrituras (7)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0861 | Poder notarial general para pleitos y especial para otras facultades | `poder-notarial-general-pleitos-especial-otras-civ-0861` |
| CIV-0883 | Acta de audiencia al Ministerio Fiscal y a las partes sobre la falta de jurisdicción por inmunidad | `acta-audiencia-ministerio-fiscal-partes-sobre-falta-civ-0883` |
| CIV-0886 | Acta de otorgamiento de poder apud acta (artículo 23.3 LEC) | `acta-otorgamiento-poder-apud-acta-articulo-23-3-lec-civ-0886` |
| CIV-0910 | Escritura de poder para pleitos | `escritura-poder-pleitos-civ-0910` |
| CIV-0911 | Escritura de poder de miseria | `escritura-poder-miseria-civ-0911` |
| CIV-0912 | Escritura de revocación de poder para pleitos y otorgamiento de uno nuevo | `escritura-revocacion-poder-pleitos-otorgamiento-uno-civ-0912` |
| CIV-1079 | Acta de apoderamiento apud acta a procurador antes de presentar la demanda | `acta-apoderamiento-apud-acta-procurador-antes-civ-1079` |

### Comunicaciones, requerimientos y cartas (51)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0869 | Solicitud de citación de testigos a la vista | `solicitud-citacion-testigos-vista-civ-0869` |
| CIV-0877 | Solicitud del demandado de suspender el plazo para contestar y reconvenir | `solicitud-demandado-suspender-plazo-contestar-civ-0877` |
| CIV-0878 | Solicitud ex parte de continuar el proceso sin el demandado (artículo 22.2 Reglamento 2020-1784) | `solicitud-ex-parte-continuar-proceso-sin-demandado-civ-0878` |
| CIV-0880 | Solicitud ex parte de declinatoria por sumisión a tribunales extranjeros (DIPr autónomo) | `solicitud-ex-parte-declinatoria-sumision-tribunales-civ-0880` |
| CIV-0881 | Solicitud ex parte de declinatoria por falta de competencia internacional (Bruselas I refundido) | `solicitud-ex-parte-declinatoria-falta-competencia-civ-0881` |
| CIV-0884 | Solicitud de habilitación ad casum para actuar ante el Tribunal Eclesiástico | `solicitud-habilitacion-ad-casum-actuar-ante-tribunal-civ-0884` |
| CIV-0885 | Declaración jurada para obtener la habilitación ante el Tribunal Eclesiástico | `declaracion-jurada-obtener-habilitacion-ante-tribunal-civ-0885` |
| CIV-0915 | Solicitud del demandado en juicio verbal de intervención de tercero y contestación a esa solicitud | `solicitud-demandado-juicio-verbal-intervencion-tercero-civ-0915` |
| CIV-0929 | Solicitud de nuevo señalamiento del juicio ordinario por enfermedad del abogado (art. 430 LEC) | `solicitud-nuevo-senalamiento-juicio-ordinario-civ-0929` |
| CIV-0942 | Solicitud de la parte para que intervenga en el juicio el perito designado judicialmente | `solicitud-parte-intervenga-juicio-perito-designado-civ-0942` |
| CIV-0944 | Solicitud de citación de testigos para el acto del juicio verbal | `solicitud-citacion-testigos-acto-juicio-verbal-civ-0944` |
| CIV-0980 | Solicitud de alterar el orden de práctica de los medios de prueba | `solicitud-alterar-orden-practica-medios-prueba-civ-0980` |
| CIV-0994 | Solicitud de acumulación de procesos seguidos ante el mismo tribunal | `solicitud-acumulacion-procesos-seguidos-ante-mismo-civ-0994` |
| CIV-0996 | Solicitud del demandante de justicia gratuita ante la comisión de asistencia jurídica gratuita | `solicitud-demandante-justicia-gratuita-ante-comision-civ-0996` |
| CIV-1000 | Comunicación del procurador al tribunal de que cesa en su cargo por terminar el proceso | `comunicacion-procurador-tribunal-cesa-cargo-terminar-civ-1000` |
| CIV-1009 | Notificación y traslado de demanda de juicio ordinario según el Convenio de La Haya de 1965 | `notificacion-traslado-demanda-juicio-ordinario-segun-civ-1009` |
| CIV-1010 | Solicitud de sucesión procesal por fallecimiento del demandante | `solicitud-sucesion-procesal-fallecimiento-demandante-civ-1010` |
| CIV-1011 | Solicitud de notificación personal de la sentencia al demandado condenado en rebeldía (art. 497 LEC) | `solicitud-notificacion-personal-sentencia-demandado-civ-1011` |
| CIV-1012 | Comunicación del procurador al tribunal del fallecimiento de su poderdante | `comunicacion-procurador-tribunal-fallecimiento-civ-1012` |
| CIV-1014 | Solicitud conjunta de suspensión del proceso por estar las partes en vías de acuerdo | `solicitud-conjunta-suspension-proceso-estar-partes-civ-1014` |
| CIV-1015 | Solicitud de intervención de un tercero en juicio ordinario o verbal | `solicitud-intervencion-tercero-juicio-ordinario-verbal-civ-1015` |
| CIV-1017 | Solicitud de tercero con interés legítimo de copia de un documento obrante en el proceso civil | `solicitud-tercero-interes-legitimo-copia-documento-civ-1017` |
| CIV-1018 | Solicitud del ejecutado subrogado de suceder al ejecutante en el proceso contra el codeudor | `solicitud-ejecutado-subrogado-suceder-ejecutante-civ-1018` |
| CIV-1022 | Solicitud de cooperación jurisdiccional internacional fuera de la UE y del Convenio de La Haya | `solicitud-cooperacion-jurisdiccional-internacional-civ-1022` |
| CIV-1023 | Solicitud del demandado de que se comunique el proceso a los sucesores del demandante fallecido | `solicitud-demandado-comunique-proceso-sucesores-civ-1023` |
| CIV-1024 | Comunicación de repudiación de herencia por parientes del demandado contra la sucesión procesal | `comunicacion-repudiacion-herencia-parientes-demandado-civ-1024` |
| CIV-1025 | Solicitud del actor de que se comunique el juicio a los sucesores del demandado fallecido | `solicitud-actor-comunique-juicio-sucesores-demandado-civ-1025` |
| CIV-1027 | Solicitud del adquirente del objeto litigioso por cesión de crédito de suceder al transmitente | `solicitud-adquirente-objeto-litigioso-cesion-credito-civ-1027` |
| CIV-1030 | Solicitud de llamada a tercero con suspensión del plazo para contestar la demanda | `solicitud-llamada-tercero-suspension-plazo-contestar-civ-1030` |
| CIV-1035 | Solicitud de intervención adhesiva de tercero a favor del demandado en juicio ordinario | `solicitud-intervencion-adhesiva-tercero-favor-civ-1035` |
| CIV-1036 | Solicitud de caducidad de la instancia civil con desistimiento del actor | `solicitud-caducidad-instancia-civil-desistimiento-actor-civ-1036` |
| CIV-1037 | Solicitud de habilitación de días inhábiles para practicar una prueba urgente | `solicitud-habilitacion-dias-inhabiles-practicar-prueba-civ-1037` |
| CIV-1038 | Solicitud de que se declare el carácter reservado de las actuaciones | `solicitud-declare-caracter-reservado-actuaciones-civ-1038` |
| CIV-1039 | Solicitud de celebrar determinadas actuaciones a puerta cerrada | `solicitud-celebrar-determinadas-actuaciones-puerta-civ-1039` |
| CIV-1041 | Solicitud de interrumpir un plazo por causa de fuerza mayor | `solicitud-interrumpir-plazo-causa-fuerza-mayor-civ-1041` |
| CIV-1053 | Solicitud del demandado con justicia gratuita de abogado y procurador de oficio en desahucio verbal | `solicitud-demandado-justicia-gratuita-abogado-civ-1053` |
| CIV-1054 | Comunicación del procurador de su cese por carecer de habilitación para actuar en el recurso | `comunicacion-procurador-cese-carecer-habilitacion-civ-1054` |
| CIV-1056 | Comunicación del Colegio de Procuradores al tribunal de la suspensión de un procurador por sanción | `comunicacion-colegio-procuradores-tribunal-suspension-civ-1056` |
| CIV-1057 | Comunicación del procurador al tribunal de una causa de incompatibilidad para representar a la parte | `comunicacion-procurador-tribunal-causa-civ-1057` |
| CIV-1058 | Solicitud de procurador de oficio por parte que alega derecho a justicia gratuita | `solicitud-procurador-oficio-parte-alega-derecho-civ-1058` |
| CIV-1059 | Comunicación del demandado de que comparecerá en juicio verbal con procurador y abogado | `comunicacion-demandado-comparecera-juicio-verbal-civ-1059` |
| CIV-1060 | Solicitud de citación de testigos y peritos para el juicio verbal | `solicitud-citacion-testigos-peritos-juicio-verbal-civ-1060` |
| CIV-1064 | Solicitud del beneficiario de justicia gratuita de abogado y procurador de oficio en verbal | `solicitud-beneficiario-justicia-gratuita-abogado-civ-1064` |
| CIV-1067 | Solicitud del demandante de terminar el proceso por satisfacción extraprocesal (art. 22 LEC) | `solicitud-demandante-terminar-proceso-satisfaccion-civ-1067` |
| CIV-1069 | Solicitud del demandado de terminar el proceso por satisfacción extraprocesal de las pretensiones | `solicitud-demandado-terminar-proceso-satisfaccion-civ-1069` |
| CIV-1070 | Solicitud del actor de que se dicte auto de allanamiento parcial pedido por el demandado | `solicitud-actor-dicte-auto-allanamiento-parcial-pedido-civ-1070` |
| CIV-1073 | Solicitud de reanudar el curso de los autos | `solicitud-reanudar-curso-autos-civ-1073` |
| CIV-1074 | Solicitud conjunta de homologación judicial de la transacción que pone fin al litigio | `solicitud-conjunta-homologacion-judicial-transaccion-civ-1074` |
| CIV-1085 | Solicitud de nuevo señalamiento de vista por imposibilidad de asistir el representante de la actora | `solicitud-nuevo-senalamiento-vista-imposibilidad-civ-1085` |
| CIV-1086 | Solicitud de suspensión de la vista señalada por acuerdo de las partes (art. 188.1.3 LEC) | `solicitud-suspension-vista-senalada-acuerdo-partes-art-civ-1086` |
| CIV-1088 | Solicitud de nuevo señalamiento de vista en juicio verbal por imposibilidad de un testigo citado | `solicitud-nuevo-senalamiento-vista-juicio-verbal-civ-1088` |

### Escritos de trámite y otros (187)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0856 | Escrito del perito designado que presenta su dictamen | `escrito-perito-designado-presenta-dictamen-civ-0856` |
| CIV-0857 | Escrito del perito designado que rechaza el cargo por causa justificada | `escrito-perito-designado-rechaza-cargo-causa-civ-0857` |
| CIV-0858 | Escrito de solicitud de nombramiento de un tercer perito | `escrito-solicitud-nombramiento-tercer-perito-civ-0858` |
| CIV-0859 | Escrito del tercer perito que acepta el cargo y pide acceso al expediente | `escrito-tercer-perito-acepta-cargo-pide-acceso-civ-0859` |
| CIV-0860 | Escrito de ampliación objetiva de la demanda | `escrito-ampliacion-objetiva-demanda-civ-0860` |
| CIV-0866 | Escrito de proposición de prueba, modelo general | `escrito-proposicion-prueba-modelo-general-civ-0866` |
| CIV-0867 | Escrito de proposición de diligencias finales | `escrito-proposicion-diligencias-finales-civ-0867` |
| CIV-0868 | Incidente de nulidad de actuaciones por defecto de forma | `incidente-nulidad-actuaciones-defecto-forma-civ-0868` |
| CIV-0870 | Escrito de ampliación o modificación de la prueba propuesta a indicación del tribunal | `escrito-ampliacion-modificacion-prueba-propuesta-civ-0870` |
| CIV-0871 | Escrito del demandado aportando prueba pericial, modelo general | `escrito-demandado-aportando-prueba-pericial-modelo-civ-0871` |
| CIV-0873 | Protesta por la inadmisión de una prueba propia o la admisión de la del contrario | `protesta-inadmision-prueba-propia-admision-contrario-civ-0873` |
| CIV-0874 | Escrito de subsanación de errores u omisiones | `escrito-subsanacion-errores-u-omisiones-civ-0874` |
| CIV-0876 | Impugnación de la resolución que deniega la justicia gratuita, con reconocimiento excepcional | `impugnacion-resolucion-deniega-justicia-gratuita-civ-0876` |
| CIV-0879 | Escrito proponiendo la declinatoria por falta de jurisdicción debida a inmunidad de jurisdicción | `escrito-proponiendo-declinatoria-falta-jurisdiccion-civ-0879` |
| CIV-0887 | Escrito de subsanación por no presentar el modelo de autoliquidación de la tasa judicial | `escrito-subsanacion-no-presentar-modelo-civ-0887` |
| CIV-0888 | Escrito pidiendo suspender el proceso porque las partes inician negociaciones | `escrito-pidiendo-suspender-proceso-porque-partes-civ-0888` |
| CIV-0889 | Escrito de conformidad para dar eficacia civil a una resolución | `escrito-conformidad-dar-eficacia-civil-resolucion-civ-0889` |
| CIV-0890 | Escrito del demandante indicando el tribunal de remisión de los autos ante varios fueros electivos | `escrito-demandante-indicando-tribunal-remision-autos-civ-0890` |
| CIV-0891 | Escrito pidiendo la citación judicial de testigos y peritos para el acto del juicio | `escrito-pidiendo-citacion-judicial-testigos-peritos-civ-0891` |
| CIV-0892 | Escrito de alegaciones a la valoración de bienes hecha por el perito tasador | `escrito-alegaciones-valoracion-bienes-hecha-perito-civ-0892` |
| CIV-0893 | Escrito de solicitud de auxilio judicial | `escrito-solicitud-auxilio-judicial-civ-0893` |
| CIV-0894 | Otrosí que acompaña el modelo de autoliquidación por exención subjetiva de la tasa (Cataluña) | `otrosi-acompana-modelo-autoliquidacion-exencion-civ-0894` |
| CIV-0895 | Otrosí que anuncia el ingreso de la tasa de servicios de la Administración de Justicia (Cataluña) | `otrosi-anuncia-ingreso-tasa-servicios-administracion-civ-0895` |
| CIV-0896 | Escrito del procurador que aporta el acto de comunicación no entregado a su destinatario | `escrito-procurador-aporta-acto-comunicacion-no-civ-0896` |
| CIV-0897 | Escrito del demandado pidiendo abogado y procurador de oficio | `escrito-demandado-pidiendo-abogado-procurador-oficio-civ-0897` |
| CIV-0899 | Proposición de prueba en otros Estados de la UE en la audiencia previa del juicio ordinario | `proposicion-prueba-otros-estados-ue-audiencia-previa-civ-0899` |
| CIV-0900 | Escrito ante Violencia sobre la Mujer pidiendo que se requiera de inhibición a una sección civil | `escrito-ante-violencia-sobre-mujer-pidiendo-requiera-civ-0900` |
| CIV-0901 | Otrosí de demanda pidiendo que el procurador practique los actos de comunicación | `otrosi-demanda-pidiendo-procurador-practique-actos-civ-0901` |
| CIV-0902 | Otrosí para que un procurador habilitado practique un acto de comunicación ante órgano exhortado | `otrosi-procurador-habilitado-practique-acto-civ-0902` |
| CIV-0903 | Escrito del actor que contesta al requerimiento por indebida acumulación de acciones | `escrito-actor-contesta-requerimiento-indebida-civ-0903` |
| CIV-0906 | Escrito del procurador que aporta la documentación de un acto de comunicación cumplimentado | `escrito-procurador-aporta-documentacion-acto-civ-0906` |
| CIV-0907 | Escrito que aporta una resolución dictada o notificada después del trámite de conclusiones | `escrito-aporta-resolucion-dictada-notificada-despues-civ-0907` |
| CIV-0908 | Escrito que comunica el resultado negativo de un acto de comunicación y pide averiguar domicilio | `escrito-comunica-resultado-negativo-acto-comunicacion-civ-0908` |
| CIV-0909 | Escrito general de desistimiento | `escrito-general-desistimiento-civ-0909` |
| CIV-0913 | Minuta del procurador con derechos, gastos y suplidos | `minuta-procurador-derechos-gastos-suplidos-civ-0913` |
| CIV-0914 | Escrito del demandado que comparece y formula reconvención en juicio verbal | `escrito-demandado-comparece-formula-reconvencion-civ-0914` |
| CIV-0916 | Escrito del demandado que opone compensación por relaciones comerciales con el actor en verbal | `escrito-demandado-opone-compensacion-relaciones-civ-0916` |
| CIV-0917 | Protesta por la inadmisión de una pregunta al testigo | `protesta-inadmision-pregunta-testigo-civ-0917` |
| CIV-0918 | Impugnación de la admisibilidad de una pregunta formulada a un testigo | `impugnacion-admisibilidad-pregunta-formulada-testigo-civ-0918` |
| CIV-0919 | Petición de careo entre testigos en el acto del juicio | `peticion-careo-entre-testigos-acto-juicio-civ-0919` |
| CIV-0920 | Declinatoria por falta de competencia territorial propuesta por el demandado en juicio verbal | `declinatoria-falta-competencia-territorial-propuesta-civ-0920` |
| CIV-0921 | Declinatoria del demandado en juicio verbal por falta de competencia territorial del tribunal | `declinatoria-demandado-juicio-verbal-falta-competencia-civ-0921` |
| CIV-0922 | Escrito de la parte no proponente que pide otros extremos en el reconocimiento judicial | `escrito-parte-no-proponente-pide-otros-extremos-civ-0922` |
| CIV-0924 | Petición oral de interrumpir el juicio por incomparecencia de testigo citado judicialmente | `peticion-oral-interrumpir-juicio-incomparecencia-civ-0924` |
| CIV-0925 | Escrito que impugna una prueba admitida por vulnerar derechos fundamentales | `escrito-impugna-prueba-admitida-vulnerar-derechos-civ-0925` |
| CIV-0926 | Escrito de contestación a la ampliación de hechos | `escrito-contestacion-ampliacion-hechos-civ-0926` |
| CIV-0927 | Cuestión incidental de previo pronunciamiento por falta de capacidad del demandante | `cuestion-incidental-previo-pronunciamiento-falta-civ-0927` |
| CIV-0930 | Escrito con lista de preguntas para el interrogatorio de parte por auxilio judicial | `escrito-lista-preguntas-interrogatorio-parte-auxilio-civ-0930` |
| CIV-0931 | Interrogatorio escrito para testigo que declara por exhorto en el orden civil | `interrogatorio-escrito-testigo-declara-exhorto-orden-civ-0931` |
| CIV-0932 | Aportación de dictamen pericial antes del juicio con petición de que comparezca el perito | `aportacion-dictamen-pericial-antes-juicio-peticion-civ-0932` |
| CIV-0933 | Preguntas y aclaraciones de la parte al perito que responde por auxilio judicial | `preguntas-aclaraciones-parte-perito-responde-auxilio-civ-0933` |
| CIV-0934 | Proposición de prueba documental por certificación de entidad prestadora de servicio público | `proposicion-prueba-documental-certificacion-entidad-civ-0934` |
| CIV-0935 | Proposición de reconocimiento judicial junto con testifical e interrogatorio de parte | `proposicion-reconocimiento-judicial-junto-testifical-e-civ-0935` |
| CIV-0936 | Proposición de reproducción de palabra, sonido e imagen con medio instrumental | `proposicion-reproduccion-palabra-sonido-e-imagen-medio-civ-0936` |
| CIV-0937 | Proposición de prueba en la audiencia previa del juicio ordinario | `proposicion-prueba-audiencia-previa-juicio-ordinario-civ-0937` |
| CIV-0939 | Escrito que denuncia el retraso de un exhorto y solicita recordatorio de urgencia | `escrito-denuncia-retraso-exhorto-solicita-recordatorio-civ-0939` |
| CIV-0940 | Escrito de ampliación de hechos nuevos posteriores a la audiencia previa | `escrito-ampliacion-hechos-nuevos-posteriores-audiencia-civ-0940` |
| CIV-0941 | Escrito de tacha de testigo en el juicio ordinario | `escrito-tacha-testigo-juicio-ordinario-civ-0941` |
| CIV-0943 | Recusación del perito designado judicialmente formulada en la audiencia previa | `recusacion-perito-designado-judicialmente-formulada-civ-0943` |
| CIV-0945 | Escrito de valoración y resumen de las diligencias finales en juicio ordinario | `escrito-valoracion-resumen-diligencias-finales-juicio-civ-0945` |
| CIV-0946 | Conclusiones orales de la parte en el juicio ordinario | `conclusiones-orales-parte-juicio-ordinario-civ-0946` |
| CIV-0947 | Petición oral de diligencias finales durante el trámite de conclusiones | `peticion-oral-diligencias-finales-durante-tramite-civ-0947` |
| CIV-0951 | Con reconvención contra el demandante (contestación) | `reconvencion-contra-demandante-contestacion-civ-0951` |
| CIV-0952 | Impugnación en la audiencia previa de un dictamen pericial con petición de ampliación | `impugnacion-audiencia-previa-dictamen-pericial-civ-0952` |
| CIV-0953 | Impugnación del informe elaborado por detective privado | `impugnacion-informe-elaborado-detective-privado-civ-0953` |
| CIV-0954 | Intervenciones de las partes y del tribunal para fijar los hechos controvertidos | `intervenciones-partes-tribunal-fijar-hechos-civ-0954` |
| CIV-0955 | Hechos y fundamentos de la contestación a la demanda ordinaria que opone defectos de capacidad | `hechos-fundamentos-contestacion-demanda-ordinaria-civ-0955` |
| CIV-0956 | Hechos y fundamentos de la contestación a la demanda ordinaria que opone defectos de representación | `hechos-fundamentos-contestacion-demanda-ordinaria-civ-0956` |
| CIV-0957 | Hechos y fundamentos de la contestación a la demanda ordinaria que opone litispendencia | `hechos-fundamentos-contestacion-demanda-ordinaria-civ-0957` |
| CIV-0958 | Hechos y fundamentos de la contestación ordinaria que se opone a la acumulación de acciones | `hechos-fundamentos-contestacion-ordinaria-opone-civ-0958` |
| CIV-0959 | Hechos y fundamentos de la contestación a la demanda ordinaria que opone defectos de la demanda | `hechos-fundamentos-contestacion-demanda-ordinaria-civ-0959` |
| CIV-0960 | Hechos y fundamentos de la contestación ordinaria que opone falta de litisconsorcio necesario | `hechos-fundamentos-contestacion-ordinaria-opone-falta-civ-0960` |
| CIV-0961 | Petición del demandado en la audiencia previa de que el juez revise de oficio su competencia | `peticion-demandado-audiencia-previa-juez-revise-oficio-civ-0961` |
| CIV-0962 | Intervención del actor que integra voluntariamente la litis en la audiencia previa, y resolución | `intervencion-actor-integra-voluntariamente-litis-civ-0962` |
| CIV-0963 | Audiencia previa sobre inadecuación de procedimiento por la cuantía y paso a juicio verbal | `audiencia-previa-sobre-inadecuacion-procedimiento-civ-0963` |
| CIV-0965 | Planteamiento por el actor de la falta de representación del demandado en la audiencia previa | `planteamiento-actor-falta-representacion-demandado-civ-0965` |
| CIV-0966 | Hechos y fundamentos de la contestación ordinaria que opone inadecuación de procedimiento | `hechos-fundamentos-contestacion-ordinaria-opone-civ-0966` |
| CIV-0968 | Hechos y fundamentos de la contestación a la demanda ordinaria que opone cosa juzgada | `hechos-fundamentos-contestacion-demanda-ordinaria-civ-0968` |
| CIV-0971 | Impugnación de dictamen pericial en la audiencia previa pidiendo que el perito actúe en el juicio | `impugnacion-dictamen-pericial-audiencia-previa-civ-0971` |
| CIV-0972 | Impugnación de documento privado en la audiencia previa con prueba sobre su autenticidad | `impugnacion-documento-privado-audiencia-previa-prueba-civ-0972` |
| CIV-0973 | Intervención del demandante que añade una petición en la audiencia previa, con oposición y protesta | `intervencion-demandante-anade-peticion-audiencia-civ-0973` |
| CIV-0974 | Intervención oral que rebate el dictamen pericial de la contestación y propone la tacha del perito | `intervencion-oral-rebate-dictamen-pericial-civ-0974` |
| CIV-0975 | Intervención en la audiencia previa sobre inadecuación de procedimiento por razón de la materia | `intervencion-audiencia-previa-sobre-inadecuacion-civ-0975` |
| CIV-0976 | Impugnación de documento público en la audiencia previa con prueba sobre su autenticidad | `impugnacion-documento-publico-audiencia-previa-prueba-civ-0976` |
| CIV-0978 | Intervención en la audiencia previa sobre defectos de la demanda y aclaraciones | `intervencion-audiencia-previa-sobre-defectos-demanda-civ-0978` |
| CIV-0979 | Proposición de interrogatorio cuando la parte es una persona jurídica | `proposicion-interrogatorio-cuando-parte-es-persona-civ-0979` |
| CIV-0981 | Proposición de prueba documental por exhibición de un documento en poder de un tercero | `proposicion-prueba-documental-exhibicion-documento-civ-0981` |
| CIV-0982 | Otrosí de la demanda de persona jurídica exenta que no aporta justificante de la tasa judicial | `otrosi-demanda-persona-juridica-exenta-no-aporta-civ-0982` |
| CIV-0984 | Otrosí de la demanda que fija la cuantía en la pretensión de condena a entregar un inmueble | `otrosi-demanda-fija-cuantia-pretension-condena-civ-0984` |
| CIV-0988 | Otrosí de la demanda que fija la cuantía en una reclamación de cantidad dineraria | `otrosi-demanda-fija-cuantia-reclamacion-cantidad-civ-0988` |
| CIV-0989 | Comparecencia ante el tribunal competente tras estimarse la declinatoria, sin conocerlo aún | `comparecencia-ante-tribunal-competente-tras-estimarse-civ-0989` |
| CIV-0990 | Declinatoria por corresponder el asunto a los tribunales de otro país | `declinatoria-corresponder-asunto-tribunales-otro-pais-civ-0990` |
| CIV-0993 | Declinatoria por falta de competencia territorial alegando la nulidad de la sumisión expresa | `declinatoria-falta-competencia-territorial-alegando-civ-0993` |
| CIV-0995 | Comparecencia ante el tribunal competente tras estimarse la declinatoria, ya conocido | `comparecencia-ante-tribunal-competente-tras-estimarse-civ-0995` |
| CIV-0997 | Escrito de tacha de perito de parte | `escrito-tacha-perito-parte-civ-0997` |
| CIV-0998 | Escrito que plantea cuestión incidental de especial pronunciamiento en juicio ordinario | `escrito-plantea-cuestion-incidental-especial-civ-0998` |
| CIV-0999 | Suspensión del juicio ordinario por prejudicialidad civil (solicitud) | `suspension-juicio-ordinario-prejudicialidad-civil-civ-0999` |
| CIV-1001 | Escrito de revocación expresa del poder del procurador | `escrito-revocacion-expresa-poder-procurador-civ-1001` |
| CIV-1003 | Escrito que subsana defectos de la demanda en la determinación de la cuantía | `escrito-subsana-defectos-demanda-determinacion-cuantia-civ-1003` |
| CIV-1004 | Escrito que subsana defectos de capacidad o representación (art. 418.1 LEC) | `escrito-subsana-defectos-capacidad-representacion-art-civ-1004` |
| CIV-1005 | Presentación de listas de preguntas para los testigos propuestos (art. 429.5 LEC) | `presentacion-listas-preguntas-testigos-propuestos-art-civ-1005` |
| CIV-1006 | Encabezamiento de demanda con abogado y procurador del turno de oficio en nombre de persona física | `encabezamiento-demanda-abogado-procurador-turno-oficio-civ-1006` |
| CIV-1008 | Intervención en la audiencia previa para pedir prueba de persona con domicilio en el extranjero | `intervencion-audiencia-previa-pedir-prueba-persona-civ-1008` |
| CIV-1013 | Escrito del demandado de oposición al desistimiento (art. 20.3 LEC) | `escrito-demandado-oposicion-desistimiento-art-20-3-lec-civ-1013` |
| CIV-1016 | Impugnación del reparto de la demanda con solicitud de nulidad y remisión al órgano competente | `impugnacion-reparto-demanda-solicitud-nulidad-remision-civ-1016` |
| CIV-1029 | Otrosí de la contestación que pide llamar a un tercero al juicio ordinario | `otrosi-contestacion-pide-llamar-tercero-juicio-civ-1029` |
| CIV-1031 | Escrito del demandante que identifica a un tercero para notificarle la pendencia del juicio verbal | `escrito-demandante-identifica-tercero-notificarle-civ-1031` |
| CIV-1032 | Escrito del actor que manifiesta desconocer a los herederos del demandado fallecido y su paradero | `escrito-actor-manifiesta-desconocer-herederos-civ-1032` |
| CIV-1033 | Otrosí del demandante que pide llamar a un tercero sin la condición de demandado | `otrosi-demandante-pide-llamar-tercero-sin-condicion-civ-1033` |
| CIV-1034 | Escrito que pide rechazar la petición por abuso de derecho o fraude de ley frente al auto ejecutivo | `escrito-pide-rechazar-peticion-abuso-derecho-fraude-civ-1034` |
| CIV-1040 | Recusación del perito designado por sorteo que emitió dictamen extrajudicial sobre el mismo asunto | `recusacion-perito-designado-sorteo-emitio-dictamen-civ-1040` |
| CIV-1043 | Escrito que subsana la indebida acumulación de acciones desistiendo de la no acumulable | `escrito-subsana-indebida-acumulacion-acciones-civ-1043` |
| CIV-1044 | Escrito que subsana la indebida acumulación de acciones manteniendo la segunda de forma eventual | `escrito-subsana-indebida-acumulacion-acciones-civ-1044` |
| CIV-1045 | Recusación de juez o magistrado en juicio ordinario por enemistad manifiesta | `recusacion-juez-magistrado-juicio-ordinario-enemistad-civ-1045` |
| CIV-1047 | Recusación de funcionario de la Administración de Justicia | `recusacion-funcionario-administracion-justicia-civ-1047` |
| CIV-1048 | Recusación del LAJ en juicio ordinario por enemistad manifiesta | `recusacion-laj-juicio-ordinario-enemistad-manifiesta-civ-1048` |
| CIV-1049 | Recusación del LAJ en juicio verbal por enemistad manifiesta | `recusacion-laj-juicio-verbal-enemistad-manifiesta-civ-1049` |
| CIV-1050 | Adhesión a la recusación del LAJ propuesta por la parte contraria | `adhesion-recusacion-laj-propuesta-parte-contraria-civ-1050` |
| CIV-1051 | Adhesión a la causa de recusación propuesta por la contraparte contra el juez | `adhesion-causa-recusacion-propuesta-contraparte-contra-civ-1051` |
| CIV-1052 | Recusación de juez o magistrado en juicio verbal por enemistad manifiesta | `recusacion-juez-magistrado-juicio-verbal-enemistad-civ-1052` |
| CIV-1055 | Escrito del procurador que cuestiona la existencia y validez de una revocación tácita de su poder | `escrito-procurador-cuestiona-existencia-validez-civ-1055` |
| CIV-1061 | Personación de nuevo procurador por revocación tácita del anterior | `personacion-nuevo-procurador-revocacion-tacita-anterior-civ-1061` |
| CIV-1062 | Otrosí de la demanda de juicio verbal que anuncia el uso de abogado y procurador no preceptivos | `otrosi-demanda-juicio-verbal-anuncia-uso-abogado-civ-1062` |
| CIV-1063 | Procurador de su renuncia a la representación del poderdante (comunicación) | `procurador-renuncia-representacion-poderdante-civ-1063` |
| CIV-1065 | Escrito del actor que niega la satisfacción extraprocesal de sus pretensiones | `escrito-actor-niega-satisfaccion-extraprocesal-civ-1065` |
| CIV-1066 | Manifestación del demandante de satisfacción extraprocesal del derecho de reparación civil | `manifestacion-demandante-satisfaccion-extraprocesal-civ-1066` |
| CIV-1068 | Personación y allanamiento total del demandado en juicio ordinario | `personacion-allanamiento-total-demandado-juicio-civ-1068` |
| CIV-1071 | Personación y allanamiento total del demandado en juicio verbal | `personacion-allanamiento-total-demandado-juicio-verbal-civ-1071` |
| CIV-1072 | Desistimiento del actor sin traslado al demandado aún no emplazado | `desistimiento-actor-sin-traslado-demandado-aun-no-civ-1072` |
| CIV-1076 | Desistimiento del actor tras la contestación con traslado al demandado y petición de no pagar costas | `desistimiento-actor-tras-contestacion-traslado-civ-1076` |
| CIV-1077 | Desistimiento del actor con traslado al demandado ya emplazado o citado | `desistimiento-actor-traslado-demandado-ya-emplazado-civ-1077` |
| CIV-1078 | Renuncia del actor a la acción ejercitada con petición de absolución en costas | `renuncia-actor-accion-ejercitada-peticion-absolucion-civ-1078` |
| CIV-1080 | Encabezamiento de demanda con procurador apoderado apud acta en comparecencia | `encabezamiento-demanda-procurador-apoderado-apud-acta-civ-1080` |
| CIV-1081 | Encabezamiento de demanda con procurador en nombre del tutor de un menor | `encabezamiento-demanda-procurador-nombre-tutor-menor-civ-1081` |
| CIV-1082 | Otrosí de demanda que pide emplazar al demandado domiciliado en el extranjero (Convenio de La Haya) | `otrosi-demanda-pide-emplazar-demandado-domiciliado-civ-1082` |
| CIV-1083 | Otrosí de la demanda que pide una medida urgente antes del reparto | `otrosi-demanda-pide-medida-urgente-antes-reparto-civ-1083` |
| CIV-1084 | Vista en segunda instancia con personación de procurador habilitado (solicitud) | `vista-segunda-instancia-personacion-procurador-civ-1084` |
| CIV-1087 | Escrito del actor que desconoce otro domicilio del demandado en el monitorio y pide oficios | `escrito-actor-desconoce-otro-domicilio-demandado-civ-1087` |
| CIV-1089 | Escrito anunciando que se usará una lengua cooficial en la vista oral | `escrito-anunciando-usara-lengua-cooficial-vista-oral-civ-1089` |
| CIV-1090 | Escrito pidiendo copia de las grabaciones originales de la vista | `escrito-pidiendo-copia-grabaciones-originales-vista-civ-1090` |
| CIV-1091 | Escrito pidiendo la traducción al castellano de las actuaciones redactadas en lengua cooficial | `escrito-pidiendo-traduccion-castellano-actuaciones-civ-1091` |
| CIV-1092 | Escrito pidiendo suspender la vista por coincidencia de señalamientos del letrado | `escrito-pidiendo-suspender-vista-coincidencia-civ-1092` |
| CIV-1093 | Escrito que acompaña la autoliquidación de tasa judicial (modelo 696) presentada telemáticamente | `escrito-acompana-autoliquidacion-tasa-judicial-modelo-civ-1093` |
| CIV-1094 | Escrito pidiendo corregir por error material una resolución judicial | `escrito-pidiendo-corregir-error-material-resolucion-civ-1094` |
| CIV-1095 | Escrito que acompaña la autoliquidación de tasa judicial (modelo 696) | `escrito-acompana-autoliquidacion-tasa-judicial-modelo-civ-1095` |
| CIV-1096 | Escrito pidiendo la reconstrucción parcial de autos | `escrito-pidiendo-reconstruccion-parcial-autos-civ-1096` |
| CIV-1097 | Escrito pidiendo subsanar la omisión de una resolución para poder cumplirla | `escrito-pidiendo-subsanar-omision-resolucion-poder-civ-1097` |
| CIV-1098 | Escrito impugnando por excesivos los honorarios de abogado en un juicio de desahucio | `escrito-impugnando-excesivos-honorarios-abogado-juicio-civ-1098` |
| CIV-1099 | Escrito de minuta de honorarios del abogado | `escrito-minuta-honorarios-abogado-civ-1099` |
| CIV-1100 | Escrito del demandado aportando dictamen pericial cinco días antes de la audiencia previa | `escrito-demandado-aportando-dictamen-pericial-cinco-civ-1100` |
| CIV-1101 | Escrito aportando un documento posterior a la demanda, a la contestación o a la audiencia previa | `escrito-aportando-documento-posterior-demanda-civ-1101` |
| CIV-1102 | Escrito de allanamiento total del demandado en juicio ordinario | `escrito-allanamiento-total-demandado-juicio-ordinario-civ-1102` |
| CIV-1103 | Escrito de declinatoria territorial ante el tribunal del domicilio del demandado (juicio verbal) | `escrito-declinatoria-territorial-ante-tribunal-civ-1103` |
| CIV-1104 | Escrito del actor que dirige la demanda contra los litisconsortes señalados por el demandado | `escrito-actor-dirige-demanda-contra-litisconsortes-civ-1104` |
| CIV-1106 | Escrito pidiendo suspender el juicio ordinario por prejudicialidad penal genérica | `escrito-pidiendo-suspender-juicio-ordinario-civ-1106` |
| CIV-1107 | Escrito del actor pidiendo contestar a la alegación de nulidad del negocio hecha por el demandado | `escrito-actor-pidiendo-contestar-alegacion-nulidad-civ-1107` |
| CIV-1108 | Escrito pidiendo comparecencia de las partes para convenir cómo realizar los bienes | `escrito-pidiendo-comparecencia-partes-convenir-como-civ-1108` |
| CIV-1109 | Escrito de declinatoria por falta de competencia internacional en juicio ordinario | `escrito-declinatoria-falta-competencia-internacional-civ-1109` |
| CIV-1110 | Escrito de resumen y valoración de las diligencias finales | `escrito-resumen-valoracion-diligencias-finales-civ-1110` |
| CIV-1111 | Escrito pidiendo presenciar el reconocimiento de lugares, objetos o personas para el peritaje | `escrito-pidiendo-presenciar-reconocimiento-lugares-civ-1111` |
| CIV-1112 | Escrito del demandante que se opone a la nulidad de actuaciones por copia inexacta | `escrito-demandante-opone-nulidad-actuaciones-copia-civ-1112` |
| CIV-1113 | Escrito del demandado que denuncia la inexactitud de la copia del dictamen pericial (art. 280 LEC) | `escrito-demandado-denuncia-inexactitud-copia-dictamen-civ-1113` |
| CIV-1115 | Escrito pidiendo una diligencia final extraordinaria (art. 435.2 LEC) | `escrito-pidiendo-diligencia-final-extraordinaria-art-civ-1115` |
| CIV-1116 | Escrito de ampliación de hechos de la demanda por cambio de liquidador, con documentos | `escrito-ampliacion-hechos-demanda-cambio-liquidador-civ-1116` |
| CIV-1117 | Escrito que contradice la tacha de un perito de parte (agente de la propiedad inmobiliaria) | `escrito-contradice-tacha-perito-parte-agente-propiedad-civ-1117` |
| CIV-1118 | Escrito del perito de parte que defiende su profesionalidad frente a una tacha | `escrito-perito-parte-defiende-profesionalidad-frente-civ-1118` |
| CIV-1119 | Escrito de ampliación subjetiva de la demanda | `escrito-ampliacion-subjetiva-demanda-civ-1119` |
| CIV-1120 | Escrito general de contestación a la demanda y oposición | `escrito-general-contestacion-demanda-oposicion-civ-1120` |
| CIV-1122 | Escrito de cualquiera de las partes aportando dictamen pericial cinco días antes del juicio | `escrito-cualquiera-partes-aportando-dictamen-pericial-civ-1122` |
| CIV-1123 | Escrito aportando sentencia o resolución de fecha no anterior a las conclusiones (art. 271.2 LEC) | `escrito-aportando-sentencia-resolucion-fecha-no-civ-1123` |
| CIV-1124 | Escrito conjunto de las partes pidiendo la homologación de lo convenido extrajudicialmente | `escrito-conjunto-partes-pidiendo-homologacion-lo-civ-1124` |
| CIV-1125 | Escrito del demandante aportando dictamen pericial cinco días antes de la audiencia previa | `escrito-demandante-aportando-dictamen-pericial-cinco-civ-1125` |
| CIV-1127 | Escrito aportando documento anterior a la demanda o contestación del que no se tenía conocimiento | `escrito-aportando-documento-anterior-demanda-civ-1127` |
| CIV-1128 | Escrito aportando documento anterior que no fue posible obtener con antelación (art. 270.1.3 LEC) | `escrito-aportando-documento-anterior-no-fue-posible-civ-1128` |
| CIV-1129 | Escrito pidiendo diligencia final ordinaria (art. 435.1.2.ª LEC) | `escrito-pidiendo-diligencia-final-ordinaria-art-435-1-civ-1129` |
| CIV-1130 | Escrito de la contraparte que niega el hecho alegado en la ampliación de hechos | `escrito-contraparte-niega-hecho-alegado-ampliacion-civ-1130` |
| CIV-1131 | Escrito de la contraparte que reconoce como cierto el hecho alegado en la ampliación de hechos | `escrito-contraparte-reconoce-como-cierto-hecho-alegado-civ-1131` |
| CIV-1132 | Escrito general de ampliación de hechos en juicio declarativo ordinario (art. 286 LEC) | `escrito-general-ampliacion-hechos-juicio-declarativo-civ-1132` |
| CIV-1134 | Escrito general del demandante que contesta a la reconvención | `escrito-general-demandante-contesta-reconvencion-civ-1134` |
| CIV-1135 | Escrito general de contestación a la demanda con reconvención | `escrito-general-contestacion-demanda-reconvencion-civ-1135` |
| CIV-1136 | Escrito del actor que contesta a la alegación de nulidad del negocio en que funda su pretensión | `escrito-actor-contesta-alegacion-nulidad-negocio-funda-civ-1136` |
| CIV-1138 | Escrito de un sujeto no demandante que contesta a la reconvención | `escrito-sujeto-no-demandante-contesta-reconvencion-civ-1138` |
| CIV-1139 | Escrito de contestación a la demanda que se allana parcialmente a las pretensiones del actor | `escrito-contestacion-demanda-allana-parcialmente-civ-1139` |
| CIV-1140 | Escrito de desistimiento bilateral en juicio ordinario | `escrito-desistimiento-bilateral-juicio-ordinario-civ-1140` |
| CIV-1141 | Escrito alegando tacha de testigo (art. 377 LEC) | `escrito-alegando-tacha-testigo-art-377-lec-civ-1141` |
| CIV-1142 | Escrito pidiendo nuevo señalamiento del juicio (art. 430 LEC) | `escrito-pidiendo-nuevo-senalamiento-juicio-art-430-lec-civ-1142` |
| CIV-1143 | Escrito pidiendo que el juicio se celebre en dos meses desde la audiencia previa (art. 429.3 LEC) | `escrito-pidiendo-juicio-celebre-dos-meses-desde-civ-1143` |
