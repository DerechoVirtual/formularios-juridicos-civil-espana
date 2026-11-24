---
name: indice
description: "Índice de los 399 formularios de Resoluciones judiciales civiles: autos, decretos y diligencias. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Resoluciones judiciales civiles: autos, decretos y diligencias: índice de formularios

> Plugin `formularios-resoluciones-judiciales-civiles` · 399 formularios · normativa revisada el 24-11-2026.

## Qué es

Modelos de las resoluciones que dicta el órgano judicial en el proceso civil: autos, sentencias, providencias, decretos y diligencias de ordenación del Letrado de la Administración de Justicia (admisión, ejecución, embargo, subasta, medidas cautelares, suspensión…). Útil para jueces, LAJ, opositores y para anticipar o revisar lo que dicta el juzgado.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Auto que despacha ejecución por título judicial»
- «Decreto que aprueba el remate en la subasta»
- «Diligencia de ordenación que convoca a las partes a la vista»

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

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-resoluciones-judiciales-civiles:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario está al final de ese fichero y la guía del tema es el `marco.md` de esta carpeta.

### Resoluciones judiciales (autos, decretos, providencias, diligencias) (267)

| Código | Formulario | Skill |
|---|---|---|
| CIV-1797 | Auto que acuerda una medida cautelar sin oír antes al demandado | `auto-acuerda-medida-cautelar-sin-oir-antes-demandado-civ-1797` |
| CIV-1799 | Auto que suspende la ejecución por oposición basada solo en motivos de fondo | `auto-suspende-ejecucion-oposicion-basada-solo-motivos-civ-1799` |
| CIV-1800 | Auto que acuerda suspender la ejecución por admitirse la revisión o rescisión de una sentencia firme | `auto-acuerda-suspender-ejecucion-admitirse-revision-civ-1800` |
| CIV-1801 | Decreto que acuerda ampliar el embargo por insuficiencia de los bienes embargados | `decreto-acuerda-ampliar-embargo-insuficiencia-bienes-civ-1801` |
| CIV-1802 | Auto de medidas inmediatas sobre custodia de los hijos y uso de la vivienda familiar | `auto-medidas-inmediatas-sobre-custodia-hijos-uso-civ-1802` |
| CIV-1803 | Auto que admite a trámite la solicitud de divorcio de mutuo acuerdo | `auto-admite-tramite-solicitud-divorcio-mutuo-acuerdo-civ-1803` |
| CIV-1804 | Decreto que acuerda reducir el embargo por exceder el valor de lo embargado a la cantidad reclamada | `decreto-acuerda-reducir-embargo-exceder-valor-lo-civ-1804` |
| CIV-1805 | Decreto de adjudicación de los bienes inmuebles embargados | `decreto-adjudicacion-bienes-inmuebles-embargados-civ-1805` |
| CIV-1806 | Decreto de adjudicación de los bienes muebles embargados | `decreto-adjudicacion-bienes-muebles-embargados-civ-1806` |
| CIV-1807 | Auto que admite la demanda contenciosa de separación con medidas provisionales simultáneas | `auto-admite-demanda-contenciosa-separacion-medidas-civ-1807` |
| CIV-1808 | Auto que admite demanda de separación contenciosa con medidas provisionales previas de otro órgano | `auto-admite-demanda-separacion-contenciosa-medidas-civ-1808` |
| CIV-1809 | Auto que admite a trámite la petición de designación judicial de un árbitro único | `auto-admite-tramite-peticion-designacion-judicial-civ-1809` |
| CIV-1810 | Auto que admite a trámite la demanda de determinación de la filiación de un menor | `auto-admite-tramite-demanda-determinacion-filiacion-civ-1810` |
| CIV-1811 | Providencia que suspende el proceso para comprobar la competencia internacional (Reglamento 2201) | `providencia-suspende-proceso-comprobar-competencia-civ-1811` |
| CIV-1812 | Providencia que suspende el proceso para comprobar competencia internacional y emplazamiento UE | `providencia-suspende-proceso-comprobar-competencia-civ-1812` |
| CIV-1813 | Auto que desestima la excepción de inmunidad de jurisdicción alegada por una parte | `auto-desestima-excepcion-inmunidad-jurisdiccion-civ-1813` |
| CIV-1814 | Providencia que acuerda proseguir el proceso conforme al artículo 15 del Convenio de La Haya de 1965 | `providencia-acuerda-proseguir-proceso-conforme-civ-1814` |
| CIV-1817 | Decreto que concreta medidas ejecutivas tras despachar la ejecución de medidas de separación | `decreto-concreta-medidas-ejecutivas-tras-despachar-civ-1817` |
| CIV-1818 | Decreto que aprueba la tasación de costas no impugnada | `decreto-aprueba-tasacion-costas-no-impugnada-civ-1818` |
| CIV-1819 | Decreto que rectifica un error material en una resolución del Letrado de la AJ | `decreto-rectifica-error-material-resolucion-letrado-aj-civ-1819` |
| CIV-1820 | Decreto que concreta las medidas ejecutivas tras despachar ejecución de una obligación de no hacer | `decreto-concreta-medidas-ejecutivas-tras-despachar-civ-1820` |
| CIV-1821 | Decreto que requiere al ejecutado para que contrate la publicidad de la sentencia | `decreto-requiere-ejecutado-contrate-publicidad-civ-1821` |
| CIV-1823 | Decreto que concreta medidas ejecutivas tras despachar ejecución sin oposición en juicio cambiario | `decreto-concreta-medidas-ejecutivas-tras-despachar-civ-1823` |
| CIV-1824 | Decreto que da por terminado el monitorio y tiene por presentada la demanda de juicio ordinario | `decreto-da-terminado-monitorio-tiene-presentada-civ-1824` |
| CIV-1825 | Decreto que concreta medidas ejecutivas tras despachar la ejecución de sentencia firme de condena | `decreto-concreta-medidas-ejecutivas-tras-despachar-civ-1825` |
| CIV-1830 | Decreto que acuerda celebrar a puerta cerrada la comparecencia para formar inventario de gananciales | `decreto-acuerda-celebrar-puerta-cerrada-comparecencia-civ-1830` |
| CIV-1833 | Decreto que inadmite el incidente de acumulación pedido ante el tribunal del proceso más moderno | `decreto-inadmite-incidente-acumulacion-pedido-ante-civ-1833` |
| CIV-1834 | Decreto que levanta la suspensión por prejudicialidad penal al terminar el juicio criminal | `decreto-levanta-suspension-prejudicialidad-penal-civ-1834` |
| CIV-1835 | Decreto que concreta las medidas ejecutivas tras despachar la ejecución de un laudo arbitral | `decreto-concreta-medidas-ejecutivas-tras-despachar-civ-1835` |
| CIV-1838 | Providencia que ordena examinar a parientes, amigos o vecinos del fallecido sin testamento | `providencia-ordena-examinar-parientes-amigos-vecinos-civ-1838` |
| CIV-1839 | Providencia que fija las condiciones de administración del caudal hereditario en el juicio divisorio | `providencia-fija-condiciones-administracion-caudal-civ-1839` |
| CIV-1840 | Decreto que acuerda la interrupción del procedimiento por fuerza mayor | `decreto-acuerda-interrupcion-procedimiento-fuerza-mayor-civ-1840` |
| CIV-1843 | Auto de inhibición del juez civil a favor del Juzgado de Violencia sobre la Mujer | `auto-inhibicion-juez-civil-favor-juzgado-violencia-civ-1843` |
| CIV-1844 | Auto de la Sección de Violencia sobre la Mujer que requiere de inhibición a la Sección de Familia | `auto-seccion-violencia-sobre-mujer-requiere-inhibicion-civ-1844` |
| CIV-1845 | Decreto que admite la demanda de separación contenciosa con medidas provisionales coetáneas | `decreto-admite-demanda-separacion-contenciosa-medidas-civ-1845` |
| CIV-1846 | Auto de requerimiento de inhibición de Violencia sobre la Mujer a Familia tras denuncia del Fiscal | `auto-requerimiento-inhibicion-violencia-sobre-mujer-civ-1846` |
| CIV-1847 | Decreto que admite demanda de separación contenciosa con medidas previas de otro tribunal | `decreto-admite-demanda-separacion-contenciosa-medidas-civ-1847` |
| CIV-1848 | Sentencia de separación contenciosa con reconvención, medidas previas de otro tribunal y Fiscal | `sentencia-separacion-contenciosa-reconvencion-medidas-civ-1848` |
| CIV-1849 | Decreto de archivo por falta de ratificación de la solicitud de separación de mutuo acuerdo | `decreto-archivo-falta-ratificacion-solicitud-civ-1849` |
| CIV-1850 | Auto que acuerda cambiar el procedimiento contencioso por uno de mutuo acuerdo | `auto-acuerda-cambiar-procedimiento-contencioso-uno-civ-1850` |
| CIV-1851 | Providencia que da plazo para aportar capitulaciones matrimoniales en separación de mutuo acuerdo | `providencia-da-plazo-aportar-capitulaciones-civ-1851` |
| CIV-1852 | Auto que declara caducadas las medidas provisionales previas a la demanda | `auto-declara-caducadas-medidas-provisionales-previas-civ-1852` |
| CIV-1853 | Decreto que admite a trámite las medidas provisionales previas a la demanda y cita a los cónyuges | `decreto-admite-tramite-medidas-provisionales-previas-civ-1853` |
| CIV-1854 | Providencia que acuerda practicar la prueba no practicada en el acto de la vista | `providencia-acuerda-practicar-prueba-no-practicada-civ-1854` |
| CIV-1856 | Decreto que admite la demanda y la reconvención y emplaza para contestar | `decreto-admite-demanda-reconvencion-emplaza-contestar-civ-1856` |
| CIV-1858 | Providencia que da plazo a las partes para proponer la modificación del convenio regulador | `providencia-da-plazo-partes-proponer-modificacion-civ-1858` |
| CIV-1861 | Sentencia que estima el divorcio de mutuo acuerdo | `sentencia-estima-divorcio-mutuo-acuerdo-civ-1861` |
| CIV-1862 | Decreto que admite a trámite la solicitud de divorcio de mutuo acuerdo | `decreto-admite-tramite-solicitud-divorcio-mutuo-acuerdo-civ-1862` |
| CIV-1864 | Decreto que nombra depositario al tercero que ya posee el bien embargado | `decreto-nombra-depositario-tercero-ya-posee-bien-civ-1864` |
| CIV-1865 | Auto que despacha ejecución para entregar cosas genéricas o indeterminadas | `auto-despacha-ejecucion-entregar-cosas-genericas-civ-1865` |
| CIV-1866 | Decreto que admite a trámite la demanda de revisión de sentencia firme | `decreto-admite-tramite-demanda-revision-sentencia-firme-civ-1866` |
| CIV-1867 | Providencia que confirma casi todas las medidas previas de otro tribunal y cita a los cónyuges | `providencia-confirma-casi-todas-medidas-previas-otro-civ-1867` |
| CIV-1869 | Auto en ejecutoria penal que fija lo debido por pensiones impagadas fijadas en proceso civil | `auto-ejecutoria-penal-fija-lo-debido-pensiones-civ-1869` |
| CIV-1871 | Auto que despacha ejecución de las medidas de separación matrimonial | `auto-despacha-ejecucion-medidas-separacion-matrimonial-civ-1871` |
| CIV-1873 | Auto que estima la eficacia civil de sentencia canónica de nulidad matrimonial | `auto-estima-eficacia-civil-sentencia-canonica-nulidad-civ-1873` |
| CIV-1874 | Decreto que admite la solicitud de eficacia civil de resolución canónica con petición de medidas | `decreto-admite-solicitud-eficacia-civil-resolucion-civ-1874` |
| CIV-1875 | Providencia que cita a partes y Fiscal por posible violencia de género sin procedimiento penal | `providencia-cita-partes-fiscal-posible-violencia-civ-1875` |
| CIV-1876 | Providencia con plazo extraordinario para pedir divorcio en procesos contenciosos (Ley 15 2005) | `providencia-plazo-extraordinario-pedir-divorcio-civ-1876` |
| CIV-1877 | Providencia con plazo extraordinario para pedir divorcio en procesos pendientes de sentencia | `providencia-plazo-extraordinario-pedir-divorcio-civ-1877` |
| CIV-1878 | Auto que suspende la ejecución del laudo arbitral previa prestación de caución | `auto-suspende-ejecucion-laudo-arbitral-previa-civ-1878` |
| CIV-1879 | Providencia que acuerda prestar asistencia judicial a los árbitros practicando prueba ante el juez | `providencia-acuerda-prestar-asistencia-judicial-civ-1879` |
| CIV-1880 | Auto que designa árbitros conforme a los criterios legales | `auto-designa-arbitros-conforme-criterios-legales-civ-1880` |
| CIV-1881 | Auto que despacha ejecución de laudo arbitral y decreta el embargo de bienes | `auto-despacha-ejecucion-laudo-arbitral-decreta-embargo-civ-1881` |
| CIV-1882 | Auto de medidas provisionales previas a la separación sin hijos y sin acuerdo entre las partes | `auto-medidas-provisionales-previas-separacion-sin-civ-1882` |
| CIV-1883 | Auto que aprueba el nuevo convenio regulador de divorcio con la estipulación modificada | `auto-aprueba-nuevo-convenio-regulador-divorcio-civ-1883` |
| CIV-1885 | Providencia que amplía la responsabilidad del embargo por pensiones impagadas en proceso matrimonial | `providencia-amplia-responsabilidad-embargo-pensiones-civ-1885` |
| CIV-1886 | Sentencia de divorcio de mutuo acuerdo tras transformar el contencioso, sin aprobar una cláusula | `sentencia-divorcio-mutuo-acuerdo-tras-transformar-civ-1886` |
| CIV-1887 | Sentencia que estima la separación de mutuo acuerdo y aprueba el convenio regulador | `sentencia-estima-separacion-mutuo-acuerdo-aprueba-civ-1887` |
| CIV-1889 | Decreto que admite a trámite la designación judicial de árbitro único | `decreto-admite-tramite-designacion-judicial-arbitro-civ-1889` |
| CIV-1891 | Providencia con plazo extraordinario para pedir divorcio en procesos de mutuo acuerdo en trámite | `providencia-plazo-extraordinario-pedir-divorcio-civ-1891` |
| CIV-1892 | Providencia con plazo extraordinario para pedir divorcio en mutuo acuerdo pendiente de sentencia | `providencia-plazo-extraordinario-pedir-divorcio-mutuo-civ-1892` |
| CIV-1893 | Oficio que recaba informe sobre las cláusulas del convenio regulador relativas a los hijos menores | `oficio-recaba-informe-sobre-clausulas-convenio-civ-1893` |
| CIV-1895 | Decreto que declara la caducidad de la instancia en primera instancia | `decreto-declara-caducidad-instancia-primera-instancia-civ-1895` |
| CIV-1896 | Auto de archivo por acumulación objetiva de acciones indebida no subsanada | `auto-archivo-acumulacion-objetiva-acciones-indebida-no-civ-1896` |
| CIV-1900 | Auto de sobreseimiento del proceso por repudiación de la herencia por los sucesores del demandado | `auto-sobreseimiento-proceso-repudiacion-herencia-civ-1900` |
| CIV-1902 | Auto que rectifica un error material en el fallo de la sentencia | `auto-rectifica-error-material-fallo-sentencia-civ-1902` |
| CIV-1904 | Oficio que remite por duplicado comisión rogatoria para emplazar a demandado en el extranjero | `oficio-remite-duplicado-comision-rogatoria-emplazar-civ-1904` |
| CIV-1905 | Auto que declara reservadas las actuaciones | `auto-declara-reservadas-actuaciones-civ-1905` |
| CIV-1906 | Auto que aparta definitivamente al juez del asunto por interés indirecto | `auto-aparta-definitivamente-juez-asunto-interes-civ-1906` |
| CIV-1907 | Auto del juez civil que se abstiene por enemistad manifiesta | `auto-juez-civil-abstiene-enemistad-manifiesta-civ-1907` |
| CIV-1909 | Providencia que rechaza la recusación del juez por interés indirecto | `providencia-rechaza-recusacion-juez-interes-indirecto-civ-1909` |
| CIV-1912 | Auto que acuerda la sucesión procesal por subrogación o cesión del crédito ejecutivo | `auto-acuerda-sucesion-procesal-subrogacion-cesion-civ-1912` |
| CIV-1916 | Decreto que declara en rebeldía a los sucesores desconocidos o ilocalizables del litigante fallecido | `decreto-declara-rebeldia-sucesores-desconocidos-civ-1916` |
| CIV-1918 | Auto que continúa el proceso pese a la incomparecencia de los sucesores | `auto-continua-proceso-pese-incomparecencia-sucesores-civ-1918` |
| CIV-1919 | Sentencia que tiene por renunciada la acción por incomparecencia de los sucesores del actor | `sentencia-tiene-renunciada-accion-incomparecencia-civ-1919` |
| CIV-1924 | Auto que declara improcedente la pretensión acumulada y sigue el proceso respecto de la otra | `auto-declara-improcedente-pretension-acumulada-sigue-civ-1924` |
| CIV-1930 | Decreto de cese del procurador por revocación del poder impugnada por él | `decreto-cese-procurador-revocacion-poder-impugnada-civ-1930` |
| CIV-1931 | Auto de sobreseimiento y archivo tras requerir a la parte para que nombre nuevo procurador | `auto-sobreseimiento-archivo-tras-requerir-parte-nombre-civ-1931` |
| CIV-1932 | Providencia que abre expediente gubernativo y da audiencia sobre sanción por mala fe procesal | `providencia-abre-expediente-gubernativo-da-audiencia-civ-1932` |
| CIV-1934 | Auto que acuerda celebrar la vista a puerta cerrada | `auto-acuerda-celebrar-vista-puerta-cerrada-civ-1934` |
| CIV-1937 | Cédula de citación a las partes para la vista del juicio verbal | `cedula-citacion-partes-vista-juicio-verbal-civ-1937` |
| CIV-1938 | Decreto que tiene por desistido al acreedor en el proceso monitorio | `decreto-tiene-desistido-acreedor-proceso-monitorio-civ-1938` |
| CIV-1946 | Auto que inadmite la impugnación de la tasación de costas | `auto-inadmite-impugnacion-tasacion-costas-civ-1946` |
| CIV-1947 | Decreto que desestima la impugnación de la tasación de costas por honorarios excesivos | `decreto-desestima-impugnacion-tasacion-costas-civ-1947` |
| CIV-1948 | Decreto que aprueba nueva tasación de costas con honorarios reducidos por excesivos | `decreto-aprueba-nueva-tasacion-costas-honorarios-civ-1948` |
| CIV-1949 | Auto que suspende el juicio cambiario por prejudicialidad penal | `auto-suspende-juicio-cambiario-prejudicialidad-penal-civ-1949` |
| CIV-1951 | Decreto que estima la impugnación de la tasación de costas por exclusiones indebidas | `decreto-estima-impugnacion-tasacion-costas-exclusiones-civ-1951` |
| CIV-1952 | Decreto que deniega acumular ejecuciones de sentencias seguidas ante distintos tribunales | `decreto-deniega-acumular-ejecuciones-sentencias-civ-1952` |
| CIV-1953 | Decreto que acuerda acumular ejecuciones de títulos extrajudiciales entre las mismas partes | `decreto-acuerda-acumular-ejecuciones-titulos-civ-1953` |
| CIV-1956 | Decreto que aprueba la liquidación de frutos y rentas sin oposición del acreedor | `decreto-aprueba-liquidacion-frutos-rentas-sin-civ-1956` |
| CIV-1960 | Providencia que nombra el perito solicitado por la parte | `providencia-nombra-perito-solicitado-parte-civ-1960` |
| CIV-1962 | Decreto que aprueba la relación de daños y perjuicios por conformidad del deudor | `decreto-aprueba-relacion-danos-perjuicios-conformidad-civ-1962` |
| CIV-1963 | Auto que resuelve sobre la liquidación de daños y perjuicios | `auto-resuelve-sobre-liquidacion-danos-perjuicios-civ-1963` |
| CIV-1964 | Decreto que aprueba la relación de daños y perjuicios por no contestar el deudor en plazo | `decreto-aprueba-relacion-danos-perjuicios-no-contestar-civ-1964` |
| CIV-1966 | Auto que deniega despachar ejecución de un hacer no personalísimo | `auto-deniega-despachar-ejecucion-hacer-no-personalisimo-civ-1966` |
| CIV-1967 | Auto que deniega despachar ejecución para la entrega de bienes inmuebles | `auto-deniega-despachar-ejecucion-entrega-bienes-civ-1967` |
| CIV-1968 | Auto que deniega despachar ejecución para la entrega de cosa mueble cierta y determinada | `auto-deniega-despachar-ejecucion-entrega-cosa-mueble-civ-1968` |
| CIV-1969 | Auto que declara personalísimo el hacer y sigue la ejecución por su equivalente con multa única | `auto-declara-personalisimo-hacer-sigue-ejecucion-civ-1969` |
| CIV-1970 | Auto que deniega despachar ejecución de una condena de no hacer | `auto-deniega-despachar-ejecucion-condena-no-hacer-civ-1970` |
| CIV-1971 | Auto que declara no personalísimo el hacer de la sentencia | `auto-declara-no-personalisimo-hacer-sentencia-civ-1971` |
| CIV-1972 | Auto que apremia con multas al ejecutado tras declarar personalísimo el hacer | `auto-apremia-multas-ejecutado-tras-declarar-civ-1972` |
| CIV-1973 | Decreto que embarga bienes del ejecutado para contratar publicidad a su costa | `decreto-embarga-bienes-ejecutado-contratar-publicidad-civ-1973` |
| CIV-1974 | Auto que deniega despachar ejecución de un hacer personalísimo | `auto-deniega-despachar-ejecucion-hacer-personalisimo-civ-1974` |
| CIV-1975 | Auto que tiene por emitida la declaración de voluntad y fija los elementos no esenciales del negocio | `auto-tiene-emitida-declaracion-voluntad-fija-elementos-civ-1975` |
| CIV-1976 | Decreto que aprueba la valoración del coste de contratar la publicidad y requiere el depósito | `decreto-aprueba-valoracion-coste-contratar-publicidad-civ-1976` |
| CIV-1977 | Auto que tiene por emitida la declaración de voluntad a la que fue condenado el ejecutado | `auto-tiene-emitida-declaracion-voluntad-fue-condenado-civ-1977` |
| CIV-1980 | Auto que manda seguir la ejecución por allanamiento del ejecutante a la tercería de mejor derecho | `auto-manda-seguir-ejecucion-allanamiento-ejecutante-civ-1980` |
| CIV-1981 | Sentencia que desestima la tercería de mejor derecho | `sentencia-desestima-terceria-mejor-derecho-civ-1981` |
| CIV-1982 | Auto que declara que el ocupante no tiene derecho a permanecer en el inmueble enajenado | `auto-declara-ocupante-no-tiene-derecho-permanecer-civ-1982` |
| CIV-1984 | Decreto que nombra depositario al ejecutante | `decreto-nombra-depositario-ejecutante-civ-1984` |
| CIV-1987 | Decreto que acuerda la administración judicial en garantía del embargo de frutos y rentas | `decreto-acuerda-administracion-judicial-garantia-civ-1987` |
| CIV-1988 | Decreto que nombra depositario a un tercero que no posee el bien embargado | `decreto-nombra-depositario-tercero-no-posee-bien-civ-1988` |
| CIV-1989 | Decreto que remueve al depositario por incumplir sus obligaciones | `decreto-remueve-depositario-incumplir-obligaciones-civ-1989` |
| CIV-1990 | Decreto que libra mandamiento al Registro de la Propiedad para anotar el embargo de inmuebles | `decreto-libra-mandamiento-registro-propiedad-anotar-civ-1990` |
| CIV-1992 | Decreto que resuelve la discrepancia con los actos del administrador judicial | `decreto-resuelve-discrepancia-actos-administrador-civ-1992` |
| CIV-1993 | Decreto que resuelve la impugnación de la cuenta final del administrador judicial | `decreto-resuelve-impugnacion-cuenta-final-civ-1993` |
| CIV-1994 | Decreto que aprueba el remate de inmuebles a favor de otro postor por no consignar el rematante | `decreto-aprueba-remate-inmuebles-favor-otro-postor-no-civ-1994` |
| CIV-1995 | Decreto que aprueba el remate de inmuebles a favor de la persona designada por el rematante | `decreto-aprueba-remate-inmuebles-favor-persona-civ-1995` |
| CIV-1996 | Decreto que aprueba el remate de inmuebles por postura inferior al 50 por 100 de la tasación | `decreto-aprueba-remate-inmuebles-postura-inferior-50-civ-1996` |
| CIV-1997 | Decreto que nombra depositario al propio ejecutado | `decreto-nombra-depositario-propio-ejecutado-civ-1997` |
| CIV-1999 | Sentencia que estima la tercería de mejor derecho | `sentencia-estima-terceria-mejor-derecho-civ-1999` |
| CIV-2000 | Decreto que pone fin a la ejecución por desistimiento del ejecutante tras tercería de mejor derecho | `decreto-pone-fin-ejecucion-desistimiento-ejecutante-civ-2000` |
| CIV-2001 | Decreto que acuerda depositar los bienes embargados en un establecimiento público o privado | `decreto-acuerda-depositar-bienes-embargados-civ-2001` |
| CIV-2002 | Auto que tiene por allanado al ejecutante en la tercería y la sigue contra el ejecutado | `auto-tiene-allanado-ejecutante-terceria-sigue-contra-civ-2002` |
| CIV-2006 | Decreto que impone al ejecutado una multa coercitiva | `decreto-impone-ejecutado-multa-coercitiva-civ-2006` |
| CIV-2007 | Providencia que impone multa coercitiva a entidades financieras, organismos y particulares | `providencia-impone-multa-coercitiva-entidades-civ-2007` |
| CIV-2008 | Decreto que manda trabar los bienes por falta de alegaciones del tercero | `decreto-manda-trabar-bienes-falta-alegaciones-tercero-civ-2008` |
| CIV-2010 | Decreto que admite a trámite la demanda de tercería de dominio | `decreto-admite-tramite-demanda-terceria-dominio-civ-2010` |
| CIV-2011 | Auto que inadmite la demanda de tercería de dominio | `auto-inadmite-demanda-terceria-dominio-civ-2011` |
| CIV-2012 | Auto que estima la tercería de dominio | `auto-estima-terceria-dominio-civ-2012` |
| CIV-2013 | Decreto que admite a trámite la demanda de tercería de mejor derecho | `decreto-admite-tramite-demanda-terceria-mejor-derecho-civ-2013` |
| CIV-2014 | Auto que inadmite la demanda de tercería de mejor derecho | `auto-inadmite-demanda-terceria-mejor-derecho-civ-2014` |
| CIV-2015 | Auto que desestima la tercería de dominio | `auto-desestima-terceria-dominio-civ-2015` |
| CIV-2017 | Decreto que embarga bienes del ejecutado para encargar el hacer a un tercero a su costa | `decreto-embarga-bienes-ejecutado-encargar-hacer-civ-2017` |
| CIV-2019 | Decreto que aprueba la valoración del coste del hacer no personalísimo y exige su depósito | `decreto-aprueba-valoracion-coste-hacer-no-civ-2019` |
| CIV-2020 | Auto que rechaza la oposición de un tercero al embargo y decreta la traba | `auto-rechaza-oposicion-tercero-embargo-decreta-traba-civ-2020` |
| CIV-2021 | Auto que deniega el embargo de bienes por pertenecer a un tercero | `auto-deniega-embargo-bienes-pertenecer-tercero-civ-2021` |
| CIV-2022 | Decreto que tiene por desistido al ejecutante y sigue la ejecución a favor del tercerista con título | `decreto-tiene-desistido-ejecutante-sigue-ejecucion-civ-2022` |
| CIV-2023 | Auto que admite el allanamiento del ejecutante si el crédito del tercerista no consta en título | `auto-admite-allanamiento-ejecutante-si-credito-civ-2023` |
| CIV-2024 | Auto que deniega abonar el valor de las cosas no separables | `auto-deniega-abonar-valor-cosas-no-separables-civ-2024` |
| CIV-2025 | Decreto que acuerda el lanzamiento del ejecutado y de los ocupantes del inmueble | `decreto-acuerda-lanzamiento-ejecutado-ocupantes-civ-2025` |
| CIV-2026 | Decreto que resuelve sobre el abono del valor de las cosas no separables | `decreto-resuelve-sobre-abono-valor-cosas-no-separables-civ-2026` |
| CIV-2027 | Auto que despacha ejecución para la entrega de bienes inmuebles | `auto-despacha-ejecucion-entrega-bienes-inmuebles-civ-2027` |
| CIV-2028 | Decreto que resuelve sobre el reparto de las sumas recaudadas en la ejecución | `decreto-resuelve-sobre-reparto-sumas-recaudadas-civ-2028` |
| CIV-2029 | Decreto que impone multas coercitivas a quien impida o dificulte la administración | `decreto-impone-multas-coercitivas-quien-impida-civ-2029` |
| CIV-2030 | Decreto que rectifica las cuentas anuales presentadas por el ejecutante | `decreto-rectifica-cuentas-anuales-presentadas-civ-2030` |
| CIV-2031 | Decreto que aprueba las cuentas anuales presentadas por el ejecutante | `decreto-aprueba-cuentas-anuales-presentadas-ejecutante-civ-2031` |
| CIV-2032 | Decreto que entrega los bienes embargados en administración para pago al ejecutante | `decreto-entrega-bienes-embargados-administracion-pago-civ-2032` |
| CIV-2033 | Decreto que acepta a un tercero que mejora la postura en la subasta de inmuebles | `decreto-acepta-tercero-mejora-postura-subasta-inmuebles-civ-2033` |
| CIV-2034 | Decreto que acepta a un tercero que mejora la postura en la subasta de bienes muebles | `decreto-acepta-tercero-mejora-postura-subasta-bienes-civ-2034` |
| CIV-2035 | Decreto que alza la suspensión de la ejecución y saca a subasta los bienes | `decreto-alza-suspension-ejecucion-saca-subasta-bienes-civ-2035` |
| CIV-2036 | Decreto que admite el desistimiento y sigue la ejecución a favor del tercerista sin título ejecutivo | `decreto-admite-desistimiento-sigue-ejecucion-favor-civ-2036` |
| CIV-2037 | Auto que autoriza la entrada en lugar cerrado para entregar la cosa al ejecutante | `auto-autoriza-entrada-lugar-cerrado-entregar-cosa-civ-2037` |
| CIV-2038 | Providencia que sustituye la entrega de la cosa por una compensación pecuniaria justa | `providencia-sustituye-entrega-cosa-compensacion-civ-2038` |
| CIV-2039 | Auto que deniega despachar ejecución para la entrega de cosas genéricas o indeterminadas | `auto-deniega-despachar-ejecucion-entrega-cosas-civ-2039` |
| CIV-2040 | Decreto que faculta al ejecutante a adquirir cosas genéricas a costa del ejecutado y embarga bienes | `decreto-faculta-ejecutante-adquirir-cosas-genericas-civ-2040` |
| CIV-2048 | Auto que desestima la oposición a la ejecución por motivos de fondo | `auto-desestima-oposicion-ejecucion-motivos-fondo-civ-2048` |
| CIV-2050 | Auto que estima la oposición a la ejecución por motivos de fondo | `auto-estima-oposicion-ejecucion-motivos-fondo-civ-2050` |
| CIV-2051 | Auto que alza la suspensión de la ejecución tras desestimarse la revisión o rescisión de sentencia | `auto-alza-suspension-ejecucion-tras-desestimarse-civ-2051` |
| CIV-2052 | Decreto que suspende la ejecución por declaración de concurso | `decreto-suspende-ejecucion-declaracion-concurso-civ-2052` |
| CIV-2053 | Decreto que sobresee la ejecución tras rescindirse la sentencia firme | `decreto-sobresee-ejecucion-tras-rescindirse-sentencia-civ-2053` |
| CIV-2054 | Decreto que aprueba el remate de inmuebles por postura inferior al 70 y superior al 50 por 100 | `decreto-aprueba-remate-inmuebles-postura-inferior-70-civ-2054` |
| CIV-2055 | Decreto que aprueba el remate de los bienes muebles embargados | `decreto-aprueba-remate-bienes-muebles-embargados-civ-2055` |
| CIV-2056 | Decreto que alza el embargo de bienes subastados sin éxito al transcurrir el plazo del acreedor | `decreto-alza-embargo-bienes-subastados-sin-exito-civ-2056` |
| CIV-2057 | Decreto que alza el embargo por constar el bien inscrito a nombre de persona distinta del ejecutado | `decreto-alza-embargo-constar-bien-inscrito-nombre-civ-2057` |
| CIV-2059 | Mandamiento al Registro de la Propiedad para que expida certificación de cargas | `mandamiento-registro-propiedad-expida-certificacion-civ-2059` |
| CIV-2061 | Decreto que aprueba el remate de muebles a favor de otro postor por no consignar el rematante | `decreto-aprueba-remate-muebles-favor-otro-postor-no-civ-2061` |
| CIV-2062 | Decreto que aprueba el remate por postura inferior al 40 por 100 del valor de tasación | `decreto-aprueba-remate-postura-inferior-40-100-valor-civ-2062` |
| CIV-2063 | Decreto que aprueba el remate de muebles a favor de la persona designada por el rematante | `decreto-aprueba-remate-muebles-favor-persona-designada-civ-2063` |
| CIV-2064 | Decreto que aprueba el remate por postura entre el 50 y el 70 por 100 del valor de tasación | `decreto-aprueba-remate-postura-entre-50-70-100-valor-civ-2064` |
| CIV-2065 | Decreto que deniega aprobar el remate en la subasta de muebles por postura inferior al 30 por 100 | `decreto-deniega-aprobar-remate-subasta-muebles-postura-civ-2065` |
| CIV-2067 | Decreto que determina la valoración definitiva del bien embargado | `decreto-determina-valoracion-definitiva-bien-embargado-civ-2067` |
| CIV-2068 | Decreto que sobresee la ejecución por cumplimiento del convenio entre ejecutante y ejecutado | `decreto-sobresee-ejecucion-cumplimiento-convenio-entre-civ-2068` |
| CIV-2069 | Decreto que aprueba el acuerdo de realización de los bienes embargados y suspende la ejecución | `decreto-aprueba-acuerdo-realizacion-bienes-embargados-civ-2069` |
| CIV-2075 | Decreto que aprueba el remate de inmuebles por postura igual o superior al 70 por 100 del avalúo | `decreto-aprueba-remate-inmuebles-postura-igual-civ-2075` |
| CIV-2076 | Decreto que alza el embargo de los bienes subastados sin éxito | `decreto-alza-embargo-bienes-subastados-sin-exito-civ-2076` |
| CIV-2077 | Decreto que aprueba la enajenación de un bien por persona o entidad especializada | `decreto-aprueba-enajenacion-bien-persona-entidad-civ-2077` |
| CIV-2078 | Decreto que designa persona o entidad especializada y fija condiciones para realizar los inmuebles | `decreto-designa-persona-entidad-especializada-fija-civ-2078` |
| CIV-2079 | Decreto que revoca el encargo de realización por transcurso del segundo plazo concedido | `decreto-revoca-encargo-realizacion-transcurso-segundo-civ-2079` |
| CIV-2080 | Decreto que revoca el encargo a persona o entidad especializada por transcurso del plazo | `decreto-revoca-encargo-persona-entidad-especializada-civ-2080` |
| CIV-2083 | Decreto que amplía el plazo para presentar la valoración pericial | `decreto-amplia-plazo-presentar-valoracion-pericial-civ-2083` |
| CIV-2085 | Auto que despacha provisionalmente la vía de apremio solicitada por el ejecutante | `auto-despacha-provisionalmente-via-apremio-solicitada-civ-2085` |
| CIV-2086 | Auto de sobreseimiento de la ejecución provisional cuando es imposible devolver el bien | `auto-sobreseimiento-ejecucion-provisional-cuando-es-civ-2086` |
| CIV-2087 | Auto que despacha ejecución fundada en auto de cuantía máxima del seguro obligatorio de automóviles | `auto-despacha-ejecucion-fundada-auto-cuantia-maxima-civ-2087` |
| CIV-2088 | Auto que estima la oposición por defectos procesales insubsanables | `auto-estima-oposicion-defectos-procesales-insubsanables-civ-2088` |
| CIV-2089 | Auto que deniega despachar ejecución de póliza de contrato mercantil por falta de firma del corredor | `auto-deniega-despachar-ejecucion-poliza-contrato-civ-2089` |
| CIV-2090 | Auto que deniega despachar ejecución de una sentencia de condena que no es firme | `auto-deniega-despachar-ejecucion-sentencia-condena-no-civ-2090` |
| CIV-2091 | Auto que despacha ejecución fundada en póliza de contrato mercantil | `auto-despacha-ejecucion-fundada-poliza-contrato-civ-2091` |
| CIV-2092 | Auto que despacha ejecución de sentencia firme de condena al pago de cantidad | `auto-despacha-ejecucion-sentencia-firme-condena-pago-civ-2092` |
| CIV-2093 | Decreto que sobresee la ejecución provisional y ordena devolver lo cobrado tras revocarse la condena | `decreto-sobresee-ejecucion-provisional-ordena-devolver-civ-2093` |
| CIV-2094 | Auto que rechaza la medida cautelar anterior al juicio por no concurrir urgencia ni necesidad | `auto-rechaza-medida-cautelar-anterior-juicio-no-civ-2094` |
| CIV-2097 | Auto que adopta medida cautelar sustitutoria pese a sentencia íntegramente desestimatoria apelada | `auto-adopta-medida-cautelar-sustitutoria-pese-civ-2097` |
| CIV-2099 | Auto que resuelve la oposición a una medida cautelar acordada sin audiencia previa | `auto-resuelve-oposicion-medida-cautelar-acordada-sin-civ-2099` |
| CIV-2101 | Providencia que aprueba la caución y ejecuta la medida cautelar | `providencia-aprueba-caucion-ejecuta-medida-cautelar-civ-2101` |
| CIV-2102 | Auto que adopta una medida cautelar solicitada junto con la demanda | `auto-adopta-medida-cautelar-solicitada-junto-demanda-civ-2102` |
| CIV-2104 | Auto que despacha ejecución en un juicio cambiario | `auto-despacha-ejecucion-juicio-cambiario-civ-2104` |
| CIV-2105 | Auto que da por terminado el juicio cambiario y despacha ejecución con embargo ya practicado | `auto-da-terminado-juicio-cambiario-despacha-ejecucion-civ-2105` |
| CIV-2106 | Auto de desistimiento en proceso monitorio con oposición del demandado | `auto-desistimiento-proceso-monitorio-oposicion-civ-2106` |
| CIV-2107 | Auto de allanamiento parcial y ejecución por lo reconocido en monitorio de más de 2.000 euros | `auto-allanamiento-parcial-ejecucion-lo-reconocido-civ-2107` |
| CIV-2108 | Decreto que sobresee el monitorio por no formalizar el peticionario la demanda de juicio ordinario | `decreto-sobresee-monitorio-no-formalizar-peticionario-civ-2108` |
| CIV-2109 | Auto que despacha ejecución en monitorio de más de 2.000 euros por incomparecencia del deudor | `auto-despacha-ejecucion-monitorio-mas-2-000-euros-civ-2109` |
| CIV-2110 | Auto de ejecución con embargo de bienes concretos en monitorio de más de 2.000 euros | `auto-ejecucion-embargo-bienes-concretos-monitorio-mas-civ-2110` |
| CIV-2111 | Auto que deniega el monitorio de una comunidad contra varios deudores por acumulación indebida | `auto-deniega-monitorio-comunidad-contra-varios-civ-2111` |
| CIV-2112 | Auto que despacha ejecución provisional con bienes para la traba designados por el ejecutante | `auto-despacha-ejecucion-provisional-bienes-traba-civ-2112` |
| CIV-2113 | Auto que deniega la ejecución provisional por no ser la sentencia provisionalmente ejecutable | `auto-deniega-ejecucion-provisional-no-ser-sentencia-civ-2113` |
| CIV-2114 | Auto que despacha ejecución provisional sin que el ejecutante haya designado bienes para la traba | `auto-despacha-ejecucion-provisional-sin-ejecutante-civ-2114` |
| CIV-2115 | Auto que desestima la oposición a la ejecución provisional por infracción de requisitos procesales | `auto-desestima-oposicion-ejecucion-provisional-civ-2115` |
| CIV-2116 | Auto que estima la oposición a la ejecución provisional si fuera muy difícil restaurar la situación | `auto-estima-oposicion-ejecucion-provisional-si-fuera-civ-2116` |
| CIV-2117 | Auto que desestima la oposición a la ejecución provisional basada en la imposible restauración | `auto-desestima-oposicion-ejecucion-provisional-basada-civ-2117` |
| CIV-2118 | Auto que rechaza plantear la cuestión incidental | `auto-rechaza-plantear-cuestion-incidental-civ-2118` |
| CIV-2119 | Auto que acuerda una diligencia final extraordinaria de ampliación del dictamen pericial económico | `auto-acuerda-diligencia-final-extraordinaria-civ-2119` |
| CIV-2120 | Decreto que da por terminado el monitorio e invita al acreedor a pedir el despacho de ejecución | `decreto-da-terminado-monitorio-e-invita-acreedor-pedir-civ-2120` |
| CIV-2122 | Providencia que declara infundada la tacha de un perito de parte y da audiencia sobre multa | `providencia-declara-infundada-tacha-perito-parte-da-civ-2122` |
| CIV-2124 | Auto que ratifica el embargo de gananciales por deuda no privativa derivada de accidente de tráfico | `auto-ratifica-embargo-gananciales-deuda-no-privativa-civ-2124` |
| CIV-2125 | Decreto que embarga bienes gananciales en ejecución contra un solo cónyuge por deuda consorcial | `decreto-embarga-bienes-gananciales-ejecucion-contra-civ-2125` |
| CIV-2127 | Auto que declara privativa la deuda y da al cónyuge no deudor la opción de disolver los gananciales | `auto-declara-privativa-deuda-da-conyuge-no-deudor-civ-2127` |
| CIV-2135 | Decreto que termina el monitorio de 2.000 a 15.000 euros y da traslado al actor sobre la oposición | `decreto-termina-monitorio-2-000-15-000-euros-da-civ-2135` |
| CIV-2136 | Decreto que archiva el monitorio por acreditarse el pago del deudor | `decreto-archiva-monitorio-acreditarse-pago-deudor-civ-2136` |
| CIV-2137 | Decreto que termina el monitorio de hasta 2.000 euros y da traslado al actor sobre la oposición | `decreto-termina-monitorio-hasta-2-000-euros-da-civ-2137` |
| CIV-2139 | Auto que concede alimentos provisionales como medida cautelar en un proceso de filiación | `auto-concede-alimentos-provisionales-como-medida-civ-2139` |
| CIV-2140 | Decreto que admite la demanda de filiación presentada por la madre del hijo menor | `decreto-admite-demanda-filiacion-presentada-madre-hijo-civ-2140` |
| CIV-2143 | Decreto que sobresee el aseguramiento de bienes hereditarios por aparecer heredero | `decreto-sobresee-aseguramiento-bienes-hereditarios-civ-2143` |
| CIV-2145 | Auto que acuerda de oficio intervenir el caudal hereditario | `auto-acuerda-oficio-intervenir-caudal-hereditario-civ-2145` |
| CIV-2146 | Providencia con medidas urgentes ante un fallecimiento comunicado desde diligencias penales | `providencia-medidas-urgentes-ante-fallecimiento-civ-2146` |
| CIV-2147 | Auto que resuelve sobre la administración, custodia y conservación del caudal hereditario | `auto-resuelve-sobre-administracion-custodia-civ-2147` |
| CIV-2148 | Auto que admite el juicio de división de herencia y la intervención del caudal hereditario | `auto-admite-juicio-division-herencia-intervencion-civ-2148` |
| CIV-2152 | Auto que acepta el requerimiento de otro tribunal para acumular los autos | `auto-acepta-requerimiento-otro-tribunal-acumular-autos-civ-2152` |
| CIV-2154 | Auto que declara procedente acumular autos de otro tribunal tras la impugnación de la contraparte | `auto-declara-procedente-acumular-autos-otro-tribunal-civ-2154` |
| CIV-2155 | Auto del tribunal requerido que deniega la acumulación y remite los autos al tribunal superior | `auto-tribunal-requerido-deniega-acumulacion-remite-civ-2155` |
| CIV-2156 | Auto que deniega inicialmente la acumulación de autos de otro tribunal (art. 78 LEC) | `auto-deniega-inicialmente-acumulacion-autos-otro-civ-2156` |
| CIV-2157 | Auto que acumula el juicio de divorcio al de modificación de medidas de separación | `auto-acumula-juicio-divorcio-modificacion-medidas-civ-2157` |
| CIV-2159 | Auto que suspende el proceso por prejudicialidad penal genérica | `auto-suspende-proceso-prejudicialidad-penal-generica-civ-2159` |
| CIV-2160 | Decreto que admite a trámite la declinatoria por falta de competencia territorial | `decreto-admite-tramite-declinatoria-falta-competencia-civ-2160` |
| CIV-2161 | Auto que deniega suspender el procedimiento por prejudicialidad civil | `auto-deniega-suspender-procedimiento-prejudicialidad-civ-2161` |
| CIV-2162 | Decreto que tiene por anunciada la declinatoria territorial y suspende el cómputo de plazos | `decreto-tiene-anunciada-declinatoria-territorial-civ-2162` |
| CIV-2163 | Decreto que remite el escrito de declinatoria de competencia territorial en juicio verbal | `decreto-remite-escrito-declinatoria-competencia-civ-2163` |
| CIV-2164 | Decreto que estima en parte la reposición sobre devolver lo cobrado en ejecución provisional | `decreto-estima-parte-reposicion-sobre-devolver-lo-civ-2164` |
| CIV-2165 | Auto que deniega el requerimiento por edictos en monitorios ajenos a cuotas de propiedad horizontal | `auto-deniega-requerimiento-edictos-monitorios-ajenos-civ-2165` |
| CIV-2169 | Auto que despacha ejecución en monitorio de menos de 2.000 euros por incomparecencia del deudor | `auto-despacha-ejecucion-monitorio-menos-2-000-euros-civ-2169` |
| CIV-2170 | Auto que sobresee la ejecución provisional de condena dineraria por revocación total de la sentencia | `auto-sobresee-ejecucion-provisional-condena-dineraria-civ-2170` |
| CIV-2171 | Auto de sobreseimiento de ejecución provisional tras revocación total de condena de hacer | `auto-sobreseimiento-ejecucion-provisional-tras-civ-2171` |
| CIV-2172 | Auto que acuerda continuar la ejecución provisional | `auto-acuerda-continuar-ejecucion-provisional-civ-2172` |
| CIV-2173 | Auto que sobresee la ejecución provisional al revocarse la entrega de un bien determinado | `auto-sobresee-ejecucion-provisional-revocarse-entrega-civ-2173` |
| CIV-2175 | Auto que ordena devolver parte de lo cobrado cuando la condena dineraria se revoca en parte | `auto-ordena-devolver-parte-lo-cobrado-cuando-condena-civ-2175` |
| CIV-2177 | Auto que estima la oposición por defectos procesales no subsanados por el ejecutante | `auto-estima-oposicion-defectos-procesales-no-civ-2177` |
| CIV-2179 | Providencia que da plazo al ejecutante para subsanar la demanda de ejecución | `providencia-da-plazo-ejecutante-subsanar-demanda-civ-2179` |
| CIV-2182 | Providencia que acuerda reducir el embargo | `providencia-acuerda-reducir-embargo-civ-2182` |
| CIV-2183 | Providencia que acuerda mejorar el embargo | `providencia-acuerda-mejorar-embargo-civ-2183` |
| CIV-2184 | Auto que archiva la ejecución provisional al poner el ejecutado la suma a disposición del tribunal | `auto-archiva-ejecucion-provisional-poner-ejecutado-civ-2184` |
| CIV-2185 | Auto que estima la oposición a una actuación concreta de la ejecución provisional dineraria | `auto-estima-oposicion-actuacion-concreta-ejecucion-civ-2185` |
| CIV-2186 | Auto que suspende la ejecución provisional por consignación de la condena | `auto-suspende-ejecucion-provisional-consignacion-civ-2186` |
| CIV-2187 | Auto que estima la oposición a la ejecución provisional por infracción de requisitos procesales | `auto-estima-oposicion-ejecucion-provisional-infraccion-civ-2187` |
| CIV-2189 | Auto que desestima la oposición a una actuación concreta de la ejecución provisional dineraria | `auto-desestima-oposicion-actuacion-concreta-ejecucion-civ-2189` |
| CIV-2190 | Providencia que señala vista en la ejecución conforme al juicio verbal | `providencia-senala-vista-ejecucion-conforme-juicio-civ-2190` |
| CIV-2191 | Auto que desestima la oposición por defectos procesales y sigue por motivos de fondo | `auto-desestima-oposicion-defectos-procesales-sigue-civ-2191` |
| CIV-2193 | Auto que desestima la oposición fundada solo en defectos procesales | `auto-desestima-oposicion-fundada-solo-defectos-civ-2193` |
| CIV-2194 | Providencia que inadmite la oposición a ejecución provisional sin medidas alternativas ni caución | `providencia-inadmite-oposicion-ejecucion-provisional-civ-2194` |

### Estatutos, actas, certificaciones y escrituras (5)

| Código | Formulario | Skill |
|---|---|---|
| CIV-1888 | Acta de la vista principal en juicio de separación matrimonial | `acta-vista-principal-juicio-separacion-matrimonial-civ-1888` |
| CIV-1890 | Acta de audiencia del menor sobre el régimen de visitas | `acta-audiencia-menor-sobre-regimen-visitas-civ-1890` |
| CIV-1894 | Acta de ratificación de la petición de divorcio y del convenio regulador | `acta-ratificacion-peticion-divorcio-convenio-regulador-civ-1894` |
| CIV-1933 | Acta de la vista de apelación con recusación oral de un magistrado | `acta-vista-apelacion-recusacion-oral-magistrado-civ-1933` |
| CIV-2151 | Acta de la vista sobre medidas de protección y alimentos provisionales en reclamación de filiación | `acta-vista-sobre-medidas-proteccion-alimentos-civ-2151` |

### Escritos de trámite y otros (127)

| Código | Formulario | Skill |
|---|---|---|
| CIV-1798 | Pronunciamientos de la sentencia definitiva sobre las medidas cautelares | `pronunciamientos-sentencia-definitiva-sobre-medidas-civ-1798` |
| CIV-1815 | Resolución que admite la declinatoria por inmunidad de jurisdicción alegada por el demandado | `resolucion-admite-declinatoria-inmunidad-jurisdiccion-civ-1815` |
| CIV-1816 | Resolución que declara la falta de jurisdicción por inmunidad apreciada de oficio | `resolucion-declara-falta-jurisdiccion-inmunidad-civ-1816` |
| CIV-1822 | Diligencia de ordenación que acuerda el embargo y libra el mandamiento | `diligencia-ordenacion-acuerda-embargo-libra-mandamiento-civ-1822` |
| CIV-1826 | Diligencia de ordenación que alza la medida cautelar tras ser firme la sentencia absolutoria | `diligencia-ordenacion-alza-medida-cautelar-tras-ser-civ-1826` |
| CIV-1827 | Diligencia de ordenación que da cuenta al tribunal de una posible causa de inadmisión de la demanda | `diligencia-ordenacion-da-cuenta-tribunal-posible-causa-civ-1827` |
| CIV-1828 | Diligencia de ordenación que suspende el proceso acumulado más avanzado | `diligencia-ordenacion-suspende-proceso-acumulado-mas-civ-1828` |
| CIV-1829 | Diligencia de ordenación que cita a las partes ante el instructor | `diligencia-ordenacion-cita-partes-ante-instructor-civ-1829` |
| CIV-1831 | Diligencia de ordenación que suspende el proceso tras la abstención del juez | `diligencia-ordenacion-suspende-proceso-tras-abstencion-civ-1831` |
| CIV-1832 | Diligencia de ordenación que comunica a otro tribunal la petición de acumulación de autos | `diligencia-ordenacion-comunica-otro-tribunal-peticion-civ-1832` |
| CIV-1836 | Diligencia de ordenación que fija la remuneración de los gastos del depósito | `diligencia-ordenacion-fija-remuneracion-gastos-deposito-civ-1836` |
| CIV-1837 | Diligencia de ordenación que cita a las partes al juicio divisorio | `diligencia-ordenacion-cita-partes-juicio-divisorio-civ-1837` |
| CIV-1841 | Diligencia de ordenación que da traslado de la oposición a intereses moratorios para fijar el tipo | `diligencia-ordenacion-da-traslado-oposicion-intereses-civ-1841` |
| CIV-1842 | Diligencia de ordenación que convoca a las partes a vista de juicio verbal para liquidar intereses | `diligencia-ordenacion-convoca-partes-vista-juicio-civ-1842` |
| CIV-1855 | Diligencia de ordenación que tiene por contestada la reconvención en separación y cita a vista | `diligencia-ordenacion-tiene-contestada-reconvencion-civ-1855` |
| CIV-1857 | Diligencia de ordenación que recibe propuesta de modificar el convenio y la traslada al Fiscal | `diligencia-ordenacion-recibe-propuesta-modificar-civ-1857` |
| CIV-1859 | Diligencia de ordenación que sigue la solicitud de divorcio por el cauce de mutuo acuerdo | `diligencia-ordenacion-sigue-solicitud-divorcio-cauce-civ-1859` |
| CIV-1860 | Diligencia de ordenación que requiere a las partes para que digan si litigan con defensa propia | `diligencia-ordenacion-requiere-partes-digan-si-litigan-civ-1860` |
| CIV-1863 | Diligencia de ordenación tras la ratificación de la solicitud de divorcio de mutuo acuerdo | `diligencia-ordenacion-tras-ratificacion-solicitud-civ-1863` |
| CIV-1868 | Diligencia de ordenación que cita a los cónyuges para acordar la liquidación del régimen económico | `diligencia-ordenacion-cita-conyuges-acordar-civ-1868` |
| CIV-1870 | Diligencia de ordenación que acuerda pagar al ejecutante las cantidades retenidas al ejecutado | `diligencia-ordenacion-acuerda-pagar-ejecutante-civ-1870` |
| CIV-1872 | Diligencia de ordenación que señala día y hora para formar el inventario | `diligencia-ordenacion-senala-dia-hora-formar-inventario-civ-1872` |
| CIV-1884 | Diligencia de ordenación que cita a comparecencia en la pieza separada de medidas provisionales | `diligencia-ordenacion-cita-comparecencia-pieza-civ-1884` |
| CIV-1897 | Diligencia de ordenación que requiere subsanar la acumulación indebida de acciones | `diligencia-ordenacion-requiere-subsanar-acumulacion-civ-1897` |
| CIV-1898 | Diligencia que requiere instar la reanudación del proceso suspendido, con apercibimiento de archivo | `diligencia-requiere-instar-reanudacion-proceso-civ-1898` |
| CIV-1899 | Diligencia de ordenación que archiva provisionalmente los autos al acabar el plazo de suspensión | `diligencia-ordenacion-archiva-provisionalmente-autos-civ-1899` |
| CIV-1901 | Diligencia que requiere ratificar la revocación del poder para pleitos y nombrar nuevo procurador | `diligencia-requiere-ratificar-revocacion-poder-pleitos-civ-1901` |
| CIV-1903 | Diligencia de ordenación que da curso a la liquidación de intereses sin demanda ejecutiva previa | `diligencia-ordenacion-da-curso-liquidacion-intereses-civ-1903` |
| CIV-1908 | Diligencia de ordenación que alza la suspensión del proceso civil por no aceptarse la abstención | `diligencia-ordenacion-alza-suspension-proceso-civil-no-civ-1908` |
| CIV-1910 | Diligencia de ordenación que remite los autos al juez sustituto y la recusación a la Audiencia | `diligencia-ordenacion-remite-autos-juez-sustituto-civ-1910` |
| CIV-1911 | Diligencia de ordenación que forma pieza separada con la recusación del juez | `diligencia-ordenacion-forma-pieza-separada-recusacion-civ-1911` |
| CIV-1913 | Diligencia de ordenación que suspende el proceso y oye a la contraparte ante la sucesión ejecutiva | `diligencia-ordenacion-suspende-proceso-oye-contraparte-civ-1913` |
| CIV-1914 | Diligencia de ordenación que da audiencia a la contraparte sobre sucesión procesal por transmisión | `diligencia-ordenacion-da-audiencia-contraparte-sobre-civ-1914` |
| CIV-1915 | Diligencia de ordenación que traslada la falta de localización de sucesores del actor | `diligencia-ordenacion-traslada-falta-localizacion-civ-1915` |
| CIV-1917 | Diligencia de ordenación que acuerda averiguar los sucesores del litigante fallecido | `diligencia-ordenacion-acuerda-averiguar-sucesores-civ-1917` |
| CIV-1920 | Diligencia de ordenación que suspende el proceso para notificarlo a los sucesores del actor | `diligencia-ordenacion-suspende-proceso-notificarlo-civ-1920` |
| CIV-1921 | Diligencia de ordenación que suspende el proceso para dar traslado de la sucesión procesal | `diligencia-ordenacion-suspende-proceso-dar-traslado-civ-1921` |
| CIV-1922 | Diligencia de ordenación que suspende el proceso al conocer el tribunal la muerte del demandado | `diligencia-ordenacion-suspende-proceso-conocer-civ-1922` |
| CIV-1923 | Acuerda la sucesión procesal por causa de muerte (decreto) | `acuerda-sucesion-procesal-causa-muerte-decreto-civ-1923` |
| CIV-1925 | Diligencia de ordenación que comunica al poderdante el fallecimiento de su procurador | `diligencia-ordenacion-comunica-poderdante-civ-1925` |
| CIV-1926 | Diligencia que da al procurador la opción de cesar por renuncia voluntaria en el proceso ejecutivo | `diligencia-da-procurador-opcion-cesar-renuncia-civ-1926` |
| CIV-1927 | Diligencia que ordena oír al demandado sobre el desistimiento bilateral | `diligencia-ordena-oir-demandado-sobre-desistimiento-civ-1927` |
| CIV-1928 | Diligencia que tiene por cesado al procurador y requiere a la parte para nombrar uno nuevo | `diligencia-tiene-cesado-procurador-requiere-parte-civ-1928` |
| CIV-1929 | Diligencia de ordenación que da audiencia a quien otorgó poderes sucesivos sobre la representación | `diligencia-ordenacion-da-audiencia-quien-otorgo-civ-1929` |
| CIV-1935 | Escrito del juez de primera instancia que se abstiene por ser cónyuge del procurador de una parte | `escrito-juez-primera-instancia-abstiene-ser-conyuge-civ-1935` |
| CIV-1936 | Diligencia de ordenación que admite a trámite el monitorio y requiere de pago al deudor | `diligencia-ordenacion-admite-tramite-monitorio-civ-1936` |
| CIV-1939 | Diligencia de ordenación que acuerda continuar el trámite del juicio ordinario | `diligencia-ordenacion-acuerda-continuar-tramite-juicio-civ-1939` |
| CIV-1940 | Diligencia de ordenación que acuerda oficiar a los acreedores anteriores | `diligencia-ordenacion-acuerda-oficiar-acreedores-civ-1940` |
| CIV-1941 | Diligencia de ordenación que acuerda dar vista de los autos al tercer poseedor | `diligencia-ordenacion-acuerda-dar-vista-autos-tercer-civ-1941` |
| CIV-1942 | Diligencia de ordenación que señala la subasta | `diligencia-ordenacion-senala-subasta-civ-1942` |
| CIV-1943 | Diligencia de ordenación que convoca comparecencia para realizar inmuebles por entidad especializada | `diligencia-ordenacion-convoca-comparecencia-realizar-civ-1943` |
| CIV-1944 | Diligencia de actuaciones inmediatas para asegurar los bienes de la herencia | `diligencia-actuaciones-inmediatas-asegurar-bienes-civ-1944` |
| CIV-1945 | Diligencia de ordenación que da representación al fiscal del heredero ausente y cita a inventario | `diligencia-ordenacion-da-representacion-fiscal-civ-1945` |
| CIV-1950 | Diligencia de ordenación que acuerda pedir informe al colegio de abogados | `diligencia-ordenacion-acuerda-pedir-informe-colegio-civ-1950` |
| CIV-1954 | Diligencia de ordenación que da traslado de la solicitud de acumulación de ejecuciones | `diligencia-ordenacion-da-traslado-solicitud-civ-1954` |
| CIV-1955 | Diligencia de ordenación que requiere al acreedor su liquidación por no presentarla el deudor | `diligencia-ordenacion-requiere-acreedor-liquidacion-no-civ-1955` |
| CIV-1957 | Diligencia de ordenación que requiere al deudor la liquidación de frutos y rentas | `diligencia-ordenacion-requiere-deudor-liquidacion-civ-1957` |
| CIV-1958 | Diligencia de ordenación que cita a vista tras el traslado del dictamen del perito | `diligencia-ordenacion-cita-vista-tras-traslado-civ-1958` |
| CIV-1959 | Diligencia de ordenación que cita a vista cuando no se ha nombrado perito | `diligencia-ordenacion-cita-vista-cuando-no-ha-nombrado-civ-1959` |
| CIV-1961 | Diligencia de ordenación que da traslado a las partes del dictamen del perito | `diligencia-ordenacion-da-traslado-partes-dictamen-civ-1961` |
| CIV-1965 | Diligencia de ordenación que da traslado de la relación de daños y perjuicios | `diligencia-ordenacion-da-traslado-relacion-danos-civ-1965` |
| CIV-1978 | Diligencia de ordenación que cita a ocupantes a vista sobre el lanzamiento que pide el ejecutante | `diligencia-ordenacion-cita-ocupantes-vista-sobre-civ-1978` |
| CIV-1979 | Diligencia de ordenación que sustituye la entrega por su equivalente pecuniario con indemnización | `diligencia-ordenacion-sustituye-entrega-equivalente-civ-1979` |
| CIV-1983 | Diligencia de ordenación que retiene sueldos, pensiones o prestaciones periódicas | `diligencia-ordenacion-retiene-sueldos-pensiones-civ-1983` |
| CIV-1985 | Diligencia de ordenación que notifica el embargo de valores u otros instrumentos financieros | `diligencia-ordenacion-notifica-embargo-valores-u-otros-civ-1985` |
| CIV-1986 | Diligencia de ordenación que retiene intereses, frutos o rentas | `diligencia-ordenacion-retiene-intereses-frutos-rentas-civ-1986` |
| CIV-1991 | Diligencia de ordenación que retiene saldos en cuentas bancarias | `diligencia-ordenacion-retiene-saldos-cuentas-bancarias-civ-1991` |
| CIV-1998 | Diligencia de ordenación que da traslado al ejecutado del allanamiento del ejecutante | `diligencia-ordenacion-da-traslado-ejecutado-civ-1998` |
| CIV-2003 | Diligencia de ordenación que acuerda librar los oficios solicitados | `diligencia-ordenacion-acuerda-librar-oficios-civ-2003` |
| CIV-2004 | Diligencia de ordenación que requiere al ejecutado para que manifieste bienes | `diligencia-ordenacion-requiere-ejecutado-manifieste-civ-2004` |
| CIV-2005 | Diligencia de ordenación que avisa a un tercero de la inminente traba de bienes | `diligencia-ordenacion-avisa-tercero-inminente-traba-civ-2005` |
| CIV-2009 | Diligencia de ordenación que da traslado a las partes | `diligencia-ordenacion-da-traslado-partes-civ-2009` |
| CIV-2016 | Diligencia de ordenación que da audiencia sobre la caución del tercerista para admitir su demanda | `diligencia-ordenacion-da-audiencia-sobre-caucion-civ-2016` |
| CIV-2018 | Diligencia de ordenación que nombra perito para valorar la obligación de hacer no personalísimo | `diligencia-ordenacion-nombra-perito-valorar-obligacion-civ-2018` |
| CIV-2041 | Diligencia de ordenación que devuelve los bienes al ejecutado una vez cobrada la deuda | `diligencia-ordenacion-devuelve-bienes-ejecutado-vez-civ-2041` |
| CIV-2042 | Diligencia de ordenación que pone fin a la administración para pago | `diligencia-ordenacion-pone-fin-administracion-pago-civ-2042` |
| CIV-2043 | Diligencia de ordenación que convoca a ejecutante y ejecutado a comparecencia | `diligencia-ordenacion-convoca-ejecutante-ejecutado-civ-2043` |
| CIV-2044 | Diligencia de ordenación que da traslado al ejecutante de las alegaciones del ejecutado | `diligencia-ordenacion-da-traslado-ejecutante-civ-2044` |
| CIV-2045 | Diligencia de ordenación que da vista de la rendición de cuentas al ejecutado | `diligencia-ordenacion-da-vista-rendicion-cuentas-civ-2045` |
| CIV-2046 | Diligencia de ordenación que cita a los ocupantes a vista sobre el lanzamiento que pide el rematante | `diligencia-ordenacion-cita-ocupantes-vista-sobre-civ-2046` |
| CIV-2047 | Diligencia de ordenación que acuerda el lanzamiento de los ocupantes de hecho del inmueble | `diligencia-ordenacion-acuerda-lanzamiento-ocupantes-civ-2047` |
| CIV-2049 | Diligencia de ordenación que pasa las actuaciones al Ministerio Fiscal | `diligencia-ordenacion-pasa-actuaciones-ministerio-civ-2049` |
| CIV-2058 | Diligencia de ordenación que comunica al ejecutante la presentación de títulos por el ejecutado | `diligencia-ordenacion-comunica-ejecutante-presentacion-civ-2058` |
| CIV-2060 | Diligencia de ordenación que libra mandamiento al Registro y requiere la presentación de títulos | `diligencia-ordenacion-libra-mandamiento-registro-civ-2060` |
| CIV-2066 | Diligencia de ordenación que entrega al ejecutante el precio del remate | `diligencia-ordenacion-entrega-ejecutante-precio-remate-civ-2066` |
| CIV-2070 | Diligencia de ordenación que convoca a las partes a comparecencia | `diligencia-ordenacion-convoca-partes-comparecencia-civ-2070` |
| CIV-2071 | Diligencia de ordenación que da traslado de la solicitud de comparecencia | `diligencia-ordenacion-da-traslado-solicitud-civ-2071` |
| CIV-2072 | Diligencia de ordenación que libra mandamiento al notario | `diligencia-ordenacion-libra-mandamiento-notario-civ-2072` |
| CIV-2073 | Diligencia de ordenación que cita a los ocupantes a vista para resolver sobre su ocupación | `diligencia-ordenacion-cita-ocupantes-vista-resolver-civ-2073` |
| CIV-2074 | Diligencia de ordenación que da mayor publicidad a la subasta | `diligencia-ordenacion-da-mayor-publicidad-subasta-civ-2074` |
| CIV-2081 | Diligencia de ordenación que acuerda realizar el bien por persona o entidad especializada | `diligencia-ordenacion-acuerda-realizar-bien-persona-civ-2081` |
| CIV-2082 | Diligencia de ordenación que amplía el plazo para ejecutar el encargo de realización | `diligencia-ordenacion-amplia-plazo-ejecutar-encargo-civ-2082` |
| CIV-2084 | Diligencia de ordenación que designa perito para valorar los bienes embargados | `diligencia-ordenacion-designa-perito-valorar-bienes-civ-2084` |
| CIV-2095 | Diligencia de ordenación que admite la medida cautelar previa pedida por asociación de consumidores | `diligencia-ordenacion-admite-medida-cautelar-previa-civ-2095` |
| CIV-2096 | Diligencia de ordenación que da audiencia al vencedor sobre mantener o sustituir la medida cautelar | `diligencia-ordenacion-da-audiencia-vencedor-sobre-civ-2096` |
| CIV-2098 | Diligencia de ordenación que da audiencia a la parte recurrida sobre la medida cautelar | `diligencia-ordenacion-da-audiencia-parte-recurrida-civ-2098` |
| CIV-2100 | Diligencia de ordenación que convoca vista ante la oposición a cautelar acordada sin audiencia | `diligencia-ordenacion-convoca-vista-ante-oposicion-civ-2100` |
| CIV-2103 | Diligencia de ordenación que convoca vista en el proceso cautelar instado con la demanda | `diligencia-ordenacion-convoca-vista-proceso-cautelar-civ-2103` |
| CIV-2121 | Diligencia de ordenación que admite la alegación de hechos nuevos y da traslado a la contraparte | `diligencia-ordenacion-admite-alegacion-hechos-nuevos-civ-2121` |
| CIV-2123 | Diligencia de ordenación que requiere al ejecutante aclarar por qué pide embargar bienes gananciales | `diligencia-ordenacion-requiere-ejecutante-aclarar-pide-civ-2123` |
| CIV-2126 | Diligencia de ordenación que convoca a audiencia sobre la división tras disolverse los gananciales | `diligencia-ordenacion-convoca-audiencia-sobre-division-civ-2126` |
| CIV-2128 | Diligencia de ordenación que convoca vista de incidente de especial pronunciamiento en juicio verbal | `diligencia-ordenacion-convoca-vista-incidente-especial-civ-2128` |
| CIV-2129 | Diligencia de ordenación que admite la cuestión incidental de previo pronunciamiento | `diligencia-ordenacion-admite-cuestion-incidental-civ-2129` |
| CIV-2130 | Diligencia de ordenación que admite la cuestión incidental de especial pronunciamiento | `diligencia-ordenacion-admite-cuestion-incidental-civ-2130` |
| CIV-2131 | Diligencia de ordenación que convoca a las partes a la vista del incidente | `diligencia-ordenacion-convoca-partes-vista-incidente-civ-2131` |
| CIV-2132 | Diligencia de ordenación que da traslado del escrito de oposición con allanamiento parcial | `diligencia-ordenacion-da-traslado-escrito-oposicion-civ-2132` |
| CIV-2133 | Diligencia de ordenación que tiene por hecha la consignación del deudor y el pago al acreedor | `diligencia-ordenacion-tiene-hecha-consignacion-deudor-civ-2133` |
| CIV-2134 | Diligencia de ordenación que da traslado al requerido de pago del escrito de desistimiento | `diligencia-ordenacion-da-traslado-requerido-pago-civ-2134` |
| CIV-2138 | Diligencia de ordenación que convoca vista sobre medidas protectoras y alimentos en filiación | `diligencia-ordenacion-convoca-vista-sobre-medidas-civ-2138` |
| CIV-2141 | Diligencia de ordenación que convoca a los interesados y al contador a comparecencia | `diligencia-ordenacion-convoca-interesados-contador-civ-2141` |
| CIV-2142 | Diligencia de ordenación que da posesión al contador y le entrega los autos | `diligencia-ordenacion-da-posesion-contador-le-entrega-civ-2142` |
| CIV-2144 | Diligencia de ordenación que manda averiguar si existe abintestato y parientes del causante | `diligencia-ordenacion-manda-averiguar-si-existe-civ-2144` |
| CIV-2149 | Diligencia de ordenación que da posesión de su cargo al administrador | `diligencia-ordenacion-da-posesion-cargo-administrador-civ-2149` |
| CIV-2150 | Diligencia de ordenación que convoca junta para nombrar contador y perito tras el inventario | `diligencia-ordenacion-convoca-junta-nombrar-contador-civ-2150` |
| CIV-2153 | Diligencia de remisión al tribunal superior por el tribunal requirente tras denegarse la acumulación | `diligencia-remision-tribunal-superior-tribunal-civ-2153` |
| CIV-2158 | Diligencia de ordenación que admite a trámite la reclamación de cuenta del procurador | `diligencia-ordenacion-admite-tramite-reclamacion-civ-2158` |
| CIV-2166 | Diligencia de ordenación que forma pieza separada con los autos principales ya en la Audiencia | `diligencia-ordenacion-forma-pieza-separada-autos-civ-2166` |
| CIV-2167 | Diligencia de ordenación que abre pieza separada con los autos principales aún en el tribunal | `diligencia-ordenacion-abre-pieza-separada-autos-civ-2167` |
| CIV-2168 | Diligencia de pago al acreedor mediante mandamiento contra la cuenta de consignaciones | `diligencia-pago-acreedor-mediante-mandamiento-contra-civ-2168` |
| CIV-2174 | Diligencia de ordenación que recibe los autos con resolución totalmente revocatoria | `diligencia-ordenacion-recibe-autos-resolucion-civ-2174` |
| CIV-2176 | Diligencia de ordenación que recibe los autos con resolución confirmatoria | `diligencia-ordenacion-recibe-autos-resolucion-civ-2176` |
| CIV-2178 | Diligencia de ordenación que da traslado de la oposición basada solo en defectos procesales | `diligencia-ordenacion-da-traslado-oposicion-basada-civ-2178` |
| CIV-2180 | Diligencia de ordenación que da traslado de la oposición por defectos procesales y otros motivos | `diligencia-ordenacion-da-traslado-oposicion-defectos-civ-2180` |
| CIV-2181 | Diligencia de ordenación que pasa los autos para resolver tras contestarse la oposición | `diligencia-ordenacion-pasa-autos-resolver-tras-civ-2181` |
| CIV-2188 | Diligencia de ordenación que tiene por evacuado el traslado de la oposición a ejecución provisional | `diligencia-ordenacion-tiene-evacuado-traslado-civ-2188` |
| CIV-2192 | Diligencia de ordenación que da traslado al ejecutante de la oposición solo por motivos de fondo | `diligencia-ordenacion-da-traslado-ejecutante-oposicion-civ-2192` |
| CIV-2195 | Diligencia de ordenación que da traslado de la oposición a la ejecución provisional | `diligencia-ordenacion-da-traslado-oposicion-ejecucion-civ-2195` |
