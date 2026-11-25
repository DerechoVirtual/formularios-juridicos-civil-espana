# Decretos y providencias del proceso civil

> Plugin de Claude Code `formularios-decretos-y-providencias-civiles` · **153 formularios** · Civil · normativa revisada el 25-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Modelos de los decretos del Letrado de la Administración de Justicia (admisión, embargo, subasta, aprobación del remate, tasación de costas, terminación del proceso) y de las providencias del juez en el proceso civil.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva; el formulario seco, listo para rellenar, está en `assets/formulario.md` dentro de la carpeta de la skill.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 153 está al final):

- **Resoluciones judiciales (autos, decretos, providencias, diligencias)** (153). Por ejemplo: Decreto que acuerda ampliar el embargo por insuficiencia de los bienes embargados; Decreto que acuerda reducir el embargo por exceder el valor de lo embargado a la cantidad reclamada; Decreto de adjudicación de los bienes inmuebles embargados.

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Decreto que admite a trámite la demanda»
   - «Decreto que aprueba el remate en la subasta»
   - «Providencia que acuerda oír a las partes sobre la suspensión»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-decretos-y-providencias-civiles:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-decretos-y-providencias-civiles:decreto-acuerda-ampliar-embargo-insuficiencia-bienes-civ-1801`. Los nombres están en la lista de formularios de abajo.

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
- **Espacio que ocupa:** unos 9.479 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-decretos-y-providencias-civiles@formularios-juridicos-civil-espana`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-civil-espana
/plugin install formularios-decretos-y-providencias-civiles@formularios-juridicos-civil-espana
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-civil-espana`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-decretos-y-providencias-civiles.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (153)

| Código | Formulario | Skill |
|---|---|---|
| CIV-1801 | Decreto que acuerda ampliar el embargo por insuficiencia de los bienes embargados | `decreto-acuerda-ampliar-embargo-insuficiencia-bienes-civ-1801` |
| CIV-1804 | Decreto que acuerda reducir el embargo por exceder el valor de lo embargado a la cantidad reclamada | `decreto-acuerda-reducir-embargo-exceder-valor-lo-civ-1804` |
| CIV-1805 | Decreto de adjudicación de los bienes inmuebles embargados | `decreto-adjudicacion-bienes-inmuebles-embargados-civ-1805` |
| CIV-1806 | Decreto de adjudicación de los bienes muebles embargados | `decreto-adjudicacion-bienes-muebles-embargados-civ-1806` |
| CIV-1811 | Providencia que suspende el proceso para comprobar la competencia internacional (Reglamento 2201) | `providencia-suspende-proceso-comprobar-competencia-civ-1811` |
| CIV-1812 | Providencia que suspende el proceso para comprobar competencia internacional y emplazamiento UE | `providencia-suspende-proceso-comprobar-competencia-civ-1812` |
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
| CIV-1845 | Decreto que admite la demanda de separación contenciosa con medidas provisionales coetáneas | `decreto-admite-demanda-separacion-contenciosa-medidas-civ-1845` |
| CIV-1847 | Decreto que admite demanda de separación contenciosa con medidas previas de otro tribunal | `decreto-admite-demanda-separacion-contenciosa-medidas-civ-1847` |
| CIV-1849 | Decreto de archivo por falta de ratificación de la solicitud de separación de mutuo acuerdo | `decreto-archivo-falta-ratificacion-solicitud-civ-1849` |
| CIV-1851 | Providencia que da plazo para aportar capitulaciones matrimoniales en separación de mutuo acuerdo | `providencia-da-plazo-aportar-capitulaciones-civ-1851` |
| CIV-1853 | Decreto que admite a trámite las medidas provisionales previas a la demanda y cita a los cónyuges | `decreto-admite-tramite-medidas-provisionales-previas-civ-1853` |
| CIV-1854 | Providencia que acuerda practicar la prueba no practicada en el acto de la vista | `providencia-acuerda-practicar-prueba-no-practicada-civ-1854` |
| CIV-1856 | Decreto que admite la demanda y la reconvención y emplaza para contestar | `decreto-admite-demanda-reconvencion-emplaza-contestar-civ-1856` |
| CIV-1858 | Providencia que da plazo a las partes para proponer la modificación del convenio regulador | `providencia-da-plazo-partes-proponer-modificacion-civ-1858` |
| CIV-1862 | Decreto que admite a trámite la solicitud de divorcio de mutuo acuerdo | `decreto-admite-tramite-solicitud-divorcio-mutuo-acuerdo-civ-1862` |
| CIV-1864 | Decreto que nombra depositario al tercero que ya posee el bien embargado | `decreto-nombra-depositario-tercero-ya-posee-bien-civ-1864` |
| CIV-1866 | Decreto que admite a trámite la demanda de revisión de sentencia firme | `decreto-admite-tramite-demanda-revision-sentencia-firme-civ-1866` |
| CIV-1867 | Providencia que confirma casi todas las medidas previas de otro tribunal y cita a los cónyuges | `providencia-confirma-casi-todas-medidas-previas-otro-civ-1867` |
| CIV-1874 | Decreto que admite la solicitud de eficacia civil de resolución canónica con petición de medidas | `decreto-admite-solicitud-eficacia-civil-resolucion-civ-1874` |
| CIV-1875 | Providencia que cita a partes y Fiscal por posible violencia de género sin procedimiento penal | `providencia-cita-partes-fiscal-posible-violencia-civ-1875` |
| CIV-1876 | Providencia con plazo extraordinario para pedir divorcio en procesos contenciosos (Ley 15 2005) | `providencia-plazo-extraordinario-pedir-divorcio-civ-1876` |
| CIV-1877 | Providencia con plazo extraordinario para pedir divorcio en procesos pendientes de sentencia | `providencia-plazo-extraordinario-pedir-divorcio-civ-1877` |
| CIV-1879 | Providencia que acuerda prestar asistencia judicial a los árbitros practicando prueba ante el juez | `providencia-acuerda-prestar-asistencia-judicial-civ-1879` |
| CIV-1885 | Providencia que amplía la responsabilidad del embargo por pensiones impagadas en proceso matrimonial | `providencia-amplia-responsabilidad-embargo-pensiones-civ-1885` |
| CIV-1889 | Decreto que admite a trámite la designación judicial de árbitro único | `decreto-admite-tramite-designacion-judicial-arbitro-civ-1889` |
| CIV-1891 | Providencia con plazo extraordinario para pedir divorcio en procesos de mutuo acuerdo en trámite | `providencia-plazo-extraordinario-pedir-divorcio-civ-1891` |
| CIV-1892 | Providencia con plazo extraordinario para pedir divorcio en mutuo acuerdo pendiente de sentencia | `providencia-plazo-extraordinario-pedir-divorcio-mutuo-civ-1892` |
| CIV-1895 | Decreto que declara la caducidad de la instancia en primera instancia | `decreto-declara-caducidad-instancia-primera-instancia-civ-1895` |
| CIV-1909 | Providencia que rechaza la recusación del juez por interés indirecto | `providencia-rechaza-recusacion-juez-interes-indirecto-civ-1909` |
| CIV-1916 | Decreto que declara en rebeldía a los sucesores desconocidos o ilocalizables del litigante fallecido | `decreto-declara-rebeldia-sucesores-desconocidos-civ-1916` |
| CIV-1930 | Decreto de cese del procurador por revocación del poder impugnada por él | `decreto-cese-procurador-revocacion-poder-impugnada-civ-1930` |
| CIV-1932 | Providencia que abre expediente gubernativo y da audiencia sobre sanción por mala fe procesal | `providencia-abre-expediente-gubernativo-da-audiencia-civ-1932` |
| CIV-1938 | Decreto que tiene por desistido al acreedor en el proceso monitorio | `decreto-tiene-desistido-acreedor-proceso-monitorio-civ-1938` |
| CIV-1947 | Decreto que desestima la impugnación de la tasación de costas por honorarios excesivos | `decreto-desestima-impugnacion-tasacion-costas-civ-1947` |
| CIV-1948 | Decreto que aprueba nueva tasación de costas con honorarios reducidos por excesivos | `decreto-aprueba-nueva-tasacion-costas-honorarios-civ-1948` |
| CIV-1951 | Decreto que estima la impugnación de la tasación de costas por exclusiones indebidas | `decreto-estima-impugnacion-tasacion-costas-exclusiones-civ-1951` |
| CIV-1952 | Decreto que deniega acumular ejecuciones de sentencias seguidas ante distintos tribunales | `decreto-deniega-acumular-ejecuciones-sentencias-civ-1952` |
| CIV-1953 | Decreto que acuerda acumular ejecuciones de títulos extrajudiciales entre las mismas partes | `decreto-acuerda-acumular-ejecuciones-titulos-civ-1953` |
| CIV-1956 | Decreto que aprueba la liquidación de frutos y rentas sin oposición del acreedor | `decreto-aprueba-liquidacion-frutos-rentas-sin-civ-1956` |
| CIV-1960 | Providencia que nombra el perito solicitado por la parte | `providencia-nombra-perito-solicitado-parte-civ-1960` |
| CIV-1962 | Decreto que aprueba la relación de daños y perjuicios por conformidad del deudor | `decreto-aprueba-relacion-danos-perjuicios-conformidad-civ-1962` |
| CIV-1964 | Decreto que aprueba la relación de daños y perjuicios por no contestar el deudor en plazo | `decreto-aprueba-relacion-danos-perjuicios-no-contestar-civ-1964` |
| CIV-1973 | Decreto que embarga bienes del ejecutado para contratar publicidad a su costa | `decreto-embarga-bienes-ejecutado-contratar-publicidad-civ-1973` |
| CIV-1976 | Decreto que aprueba la valoración del coste de contratar la publicidad y requiere el depósito | `decreto-aprueba-valoracion-coste-contratar-publicidad-civ-1976` |
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
| CIV-2000 | Decreto que pone fin a la ejecución por desistimiento del ejecutante tras tercería de mejor derecho | `decreto-pone-fin-ejecucion-desistimiento-ejecutante-civ-2000` |
| CIV-2001 | Decreto que acuerda depositar los bienes embargados en un establecimiento público o privado | `decreto-acuerda-depositar-bienes-embargados-civ-2001` |
| CIV-2006 | Decreto que impone al ejecutado una multa coercitiva | `decreto-impone-ejecutado-multa-coercitiva-civ-2006` |
| CIV-2007 | Providencia que impone multa coercitiva a entidades financieras, organismos y particulares | `providencia-impone-multa-coercitiva-entidades-civ-2007` |
| CIV-2008 | Decreto que manda trabar los bienes por falta de alegaciones del tercero | `decreto-manda-trabar-bienes-falta-alegaciones-tercero-civ-2008` |
| CIV-2010 | Decreto que admite a trámite la demanda de tercería de dominio | `decreto-admite-tramite-demanda-terceria-dominio-civ-2010` |
| CIV-2013 | Decreto que admite a trámite la demanda de tercería de mejor derecho | `decreto-admite-tramite-demanda-terceria-mejor-derecho-civ-2013` |
| CIV-2017 | Decreto que embarga bienes del ejecutado para encargar el hacer a un tercero a su costa | `decreto-embarga-bienes-ejecutado-encargar-hacer-civ-2017` |
| CIV-2019 | Decreto que aprueba la valoración del coste del hacer no personalísimo y exige su depósito | `decreto-aprueba-valoracion-coste-hacer-no-civ-2019` |
| CIV-2022 | Decreto que tiene por desistido al ejecutante y sigue la ejecución a favor del tercerista con título | `decreto-tiene-desistido-ejecutante-sigue-ejecucion-civ-2022` |
| CIV-2025 | Decreto que acuerda el lanzamiento del ejecutado y de los ocupantes del inmueble | `decreto-acuerda-lanzamiento-ejecutado-ocupantes-civ-2025` |
| CIV-2026 | Decreto que resuelve sobre el abono del valor de las cosas no separables | `decreto-resuelve-sobre-abono-valor-cosas-no-separables-civ-2026` |
| CIV-2028 | Decreto que resuelve sobre el reparto de las sumas recaudadas en la ejecución | `decreto-resuelve-sobre-reparto-sumas-recaudadas-civ-2028` |
| CIV-2029 | Decreto que impone multas coercitivas a quien impida o dificulte la administración | `decreto-impone-multas-coercitivas-quien-impida-civ-2029` |
| CIV-2030 | Decreto que rectifica las cuentas anuales presentadas por el ejecutante | `decreto-rectifica-cuentas-anuales-presentadas-civ-2030` |
| CIV-2031 | Decreto que aprueba las cuentas anuales presentadas por el ejecutante | `decreto-aprueba-cuentas-anuales-presentadas-ejecutante-civ-2031` |
| CIV-2032 | Decreto que entrega los bienes embargados en administración para pago al ejecutante | `decreto-entrega-bienes-embargados-administracion-pago-civ-2032` |
| CIV-2033 | Decreto que acepta a un tercero que mejora la postura en la subasta de inmuebles | `decreto-acepta-tercero-mejora-postura-subasta-inmuebles-civ-2033` |
| CIV-2034 | Decreto que acepta a un tercero que mejora la postura en la subasta de bienes muebles | `decreto-acepta-tercero-mejora-postura-subasta-bienes-civ-2034` |
| CIV-2035 | Decreto que alza la suspensión de la ejecución y saca a subasta los bienes | `decreto-alza-suspension-ejecucion-saca-subasta-bienes-civ-2035` |
| CIV-2036 | Decreto que admite el desistimiento y sigue la ejecución a favor del tercerista sin título ejecutivo | `decreto-admite-desistimiento-sigue-ejecucion-favor-civ-2036` |
| CIV-2038 | Providencia que sustituye la entrega de la cosa por una compensación pecuniaria justa | `providencia-sustituye-entrega-cosa-compensacion-civ-2038` |
| CIV-2040 | Decreto que faculta al ejecutante a adquirir cosas genéricas a costa del ejecutado y embarga bienes | `decreto-faculta-ejecutante-adquirir-cosas-genericas-civ-2040` |
| CIV-2052 | Decreto que suspende la ejecución por declaración de concurso | `decreto-suspende-ejecucion-declaracion-concurso-civ-2052` |
| CIV-2053 | Decreto que sobresee la ejecución tras rescindirse la sentencia firme | `decreto-sobresee-ejecucion-tras-rescindirse-sentencia-civ-2053` |
| CIV-2054 | Decreto que aprueba el remate de inmuebles por postura inferior al 70 y superior al 50 por 100 | `decreto-aprueba-remate-inmuebles-postura-inferior-70-civ-2054` |
| CIV-2055 | Decreto que aprueba el remate de los bienes muebles embargados | `decreto-aprueba-remate-bienes-muebles-embargados-civ-2055` |
| CIV-2056 | Decreto que alza el embargo de bienes subastados sin éxito al transcurrir el plazo del acreedor | `decreto-alza-embargo-bienes-subastados-sin-exito-civ-2056` |
| CIV-2057 | Decreto que alza el embargo por constar el bien inscrito a nombre de persona distinta del ejecutado | `decreto-alza-embargo-constar-bien-inscrito-nombre-civ-2057` |
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
| CIV-2093 | Decreto que sobresee la ejecución provisional y ordena devolver lo cobrado tras revocarse la condena | `decreto-sobresee-ejecucion-provisional-ordena-devolver-civ-2093` |
| CIV-2101 | Providencia que aprueba la caución y ejecuta la medida cautelar | `providencia-aprueba-caucion-ejecuta-medida-cautelar-civ-2101` |
| CIV-2108 | Decreto que sobresee el monitorio por no formalizar el peticionario la demanda de juicio ordinario | `decreto-sobresee-monitorio-no-formalizar-peticionario-civ-2108` |
| CIV-2120 | Decreto que da por terminado el monitorio e invita al acreedor a pedir el despacho de ejecución | `decreto-da-terminado-monitorio-e-invita-acreedor-pedir-civ-2120` |
| CIV-2122 | Providencia que declara infundada la tacha de un perito de parte y da audiencia sobre multa | `providencia-declara-infundada-tacha-perito-parte-da-civ-2122` |
| CIV-2125 | Decreto que embarga bienes gananciales en ejecución contra un solo cónyuge por deuda consorcial | `decreto-embarga-bienes-gananciales-ejecucion-contra-civ-2125` |
| CIV-2135 | Decreto que termina el monitorio de 2.000 a 15.000 euros y da traslado al actor sobre la oposición | `decreto-termina-monitorio-2-000-15-000-euros-da-civ-2135` |
| CIV-2136 | Decreto que archiva el monitorio por acreditarse el pago del deudor | `decreto-archiva-monitorio-acreditarse-pago-deudor-civ-2136` |
| CIV-2137 | Decreto que termina el monitorio de hasta 2.000 euros y da traslado al actor sobre la oposición | `decreto-termina-monitorio-hasta-2-000-euros-da-civ-2137` |
| CIV-2140 | Decreto que admite la demanda de filiación presentada por la madre del hijo menor | `decreto-admite-demanda-filiacion-presentada-madre-hijo-civ-2140` |
| CIV-2146 | Providencia con medidas urgentes ante un fallecimiento comunicado desde diligencias penales | `providencia-medidas-urgentes-ante-fallecimiento-civ-2146` |
| CIV-2160 | Decreto que admite a trámite la declinatoria por falta de competencia territorial | `decreto-admite-tramite-declinatoria-falta-competencia-civ-2160` |
| CIV-2162 | Decreto que tiene por anunciada la declinatoria territorial y suspende el cómputo de plazos | `decreto-tiene-anunciada-declinatoria-territorial-civ-2162` |
| CIV-2163 | Decreto que remite el escrito de declinatoria de competencia territorial en juicio verbal | `decreto-remite-escrito-declinatoria-competencia-civ-2163` |
| CIV-2164 | Decreto que estima en parte la reposición sobre devolver lo cobrado en ejecución provisional | `decreto-estima-parte-reposicion-sobre-devolver-lo-civ-2164` |
| CIV-2179 | Providencia que da plazo al ejecutante para subsanar la demanda de ejecución | `providencia-da-plazo-ejecutante-subsanar-demanda-civ-2179` |
| CIV-2182 | Providencia que acuerda reducir el embargo | `providencia-acuerda-reducir-embargo-civ-2182` |
| CIV-2183 | Providencia que acuerda mejorar el embargo | `providencia-acuerda-mejorar-embargo-civ-2183` |
| CIV-2190 | Providencia que señala vista en la ejecución conforme al juicio verbal | `providencia-senala-vista-ejecucion-conforme-juicio-civ-2190` |
| CIV-2194 | Providencia que inadmite la oposición a ejecución provisional sin medidas alternativas ni caución | `providencia-inadmite-oposicion-ejecucion-provisional-civ-2194` |
| CIV-2900 | Decreto que estima en parte la impugnación de honorarios del abogado y fija lo debido | `decreto-estima-parte-impugnacion-honorarios-abogado-civ-2900` |
| CIV-2901 | Decreto que inadmite la reclamación de honorarios presentada por el abogado | `decreto-inadmite-reclamacion-honorarios-presentada-civ-2901` |
| CIV-2911 | Providencia que admite la impugnación de la tasación de costas por honorarios indebidos y excesivos | `providencia-admite-impugnacion-tasacion-costas-civ-2911` |
| CIV-2912 | Providencia que admite la impugnación de la tasación de costas por honorarios excesivos | `providencia-admite-impugnacion-tasacion-costas-civ-2912` |
| CIV-2923 | Providencia que multa al testigo incomparecido y fija fecha para continuar la vista | `providencia-multa-testigo-incomparecido-fija-fecha-civ-2923` |
| CIV-2924 | Providencia que acuerda de oficio la práctica de pruebas en un proceso matrimonial | `providencia-acuerda-oficio-practica-pruebas-proceso-civ-2924` |
| CIV-2943 | Decreto que admite la separación o divorcio de mutuo acuerdo y cita a los cónyuges a ratificarse | `decreto-admite-separacion-divorcio-mutuo-acuerdo-cita-civ-2943` |
| CIV-2946 | Decreto que admite a trámite las medidas provisionales previas a la demanda de separación | `decreto-admite-tramite-medidas-provisionales-previas-civ-2946` |
| CIV-2948 | Decreto de admisión de medidas provisionales pedidas antes de la demanda matrimonial | `decreto-admision-medidas-provisionales-pedidas-antes-civ-2948` |
| CIV-2949 | Providencia que admite la contestación y deja las medidas provisionales para la vista principal | `providencia-admite-contestacion-deja-medidas-civ-2949` |
| CIV-2950 | Providencia que admite la contestación y cita a comparecencia sobre las medidas provisionales | `providencia-admite-contestacion-cita-comparecencia-civ-2950` |
| CIV-2951 | Providencia que pide a las partes un nuevo convenio sobre los puntos no aprobados | `providencia-pide-partes-nuevo-convenio-sobre-puntos-no-civ-2951` |
| CIV-2953 | Decreto que archiva la separación de mutuo acuerdo por falta de ratificación de un cónyuge | `decreto-archiva-separacion-mutuo-acuerdo-falta-civ-2953` |
| CIV-2954 | Providencia que pide informe al Fiscal sobre el convenio relativo a los hijos y acuerda oírlos | `providencia-pide-informe-fiscal-sobre-convenio-civ-2954` |
| CIV-2955 | Providencia que da plazo para subsanar la documentación en un proceso matrimonial de mutuo acuerdo | `providencia-da-plazo-subsanar-documentacion-proceso-civ-2955` |
| CIV-2969 | Decreto que admite la demanda matrimonial y une las medidas provisionales previas del mismo tribunal | `decreto-admite-demanda-matrimonial-une-medidas-civ-2969` |
| CIV-3018 | Providencia que da plazo para subsanar la documentación de la conversión a mutuo acuerdo | `providencia-da-plazo-subsanar-documentacion-conversion-civ-3018` |
| CIV-3019 | Providencia que rechaza por extemporánea la reposición contra el auto que inadmite la reconvención | `providencia-rechaza-extemporanea-reposicion-contra-civ-3019` |

## Privacidad

Ver `PRIVACY.md`.
