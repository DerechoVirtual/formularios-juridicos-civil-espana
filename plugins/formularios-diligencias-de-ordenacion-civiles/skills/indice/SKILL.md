---
name: indice
description: "Índice de los 146 formularios de Diligencias de ordenación y de constancia del proceso civil. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Diligencias de ordenación y de constancia del proceso civil: índice de formularios

> Plugin `formularios-diligencias-de-ordenacion-civiles` · 146 formularios · normativa revisada el 25-11-2026.

## Qué es

Modelos de las diligencias que extiende el Letrado de la Administración de Justicia en el proceso civil: de ordenación (traslados, citaciones, señalamientos, impulso del procedimiento) y de constancia, comunicación y ejecución. Útil para LAJ, tramitadores, opositores y para anticipar lo que acuerda el tribunal.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Diligencia de ordenación que convoca a las partes a la vista»
- «Diligencia de ordenación que da traslado del escrito de la otra parte»
- «Diligencia de constancia de la presentación de un escrito»

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

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-diligencias-de-ordenacion-civiles:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario que se rellena está en `../<skill>/assets/formulario.md` y la guía del tema es el `marco.md` de esta carpeta.

### Escritos de trámite y otros (146)

| Código | Formulario | Skill |
|---|---|---|
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
| CIV-1925 | Diligencia de ordenación que comunica al poderdante el fallecimiento de su procurador | `diligencia-ordenacion-comunica-poderdante-civ-1925` |
| CIV-1926 | Diligencia que da al procurador la opción de cesar por renuncia voluntaria en el proceso ejecutivo | `diligencia-da-procurador-opcion-cesar-renuncia-civ-1926` |
| CIV-1927 | Diligencia que ordena oír al demandado sobre el desistimiento bilateral | `diligencia-ordena-oir-demandado-sobre-desistimiento-civ-1927` |
| CIV-1928 | Diligencia que tiene por cesado al procurador y requiere a la parte para nombrar uno nuevo | `diligencia-tiene-cesado-procurador-requiere-parte-civ-1928` |
| CIV-1929 | Diligencia de ordenación que da audiencia a quien otorgó poderes sucesivos sobre la representación | `diligencia-ordenacion-da-audiencia-quien-otorgo-civ-1929` |
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
| CIV-2902 | Diligencia de requerimiento al poderdante para que pague o impugne la cuenta de su procurador | `diligencia-requerimiento-poderdante-pague-impugne-civ-2902` |
| CIV-2915 | Diligencia de embargo por título extrajudicial y deuda privativa, entendida con el cónyuge no deudor | `diligencia-embargo-titulo-extrajudicial-deuda-civ-2915` |
| CIV-2916 | Diligencia de inventario judicial de los bienes de la herencia tras acordarse su intervención | `diligencia-inventario-judicial-bienes-herencia-tras-civ-2916` |
| CIV-2917 | Diligencia de ordenación para formar el inventario de la herencia sin acuerdo de los herederos | `diligencia-ordenacion-formar-inventario-herencia-sin-civ-2917` |
| CIV-2942 | Diligencia de ordenación que pide informe al Fiscal sobre lo pactado respecto a los hijos | `diligencia-ordenacion-pide-informe-fiscal-sobre-lo-civ-2942` |
| CIV-2944 | Diligencia de ordenación que pregunta a las partes si mantienen la misma defensa y representación | `diligencia-ordenacion-pregunta-partes-si-mantienen-civ-2944` |
| CIV-2945 | Diligencia de ordenación que exige nombrar abogado y procurador ante la ejecución del convenio | `diligencia-ordenacion-exige-nombrar-abogado-procurador-civ-2945` |
| CIV-2958 | Diligencia de ordenación que manda oficiar al Registro Civil para anotar el fallo de la sentencia | `diligencia-ordenacion-manda-oficiar-registro-civil-civ-2958` |
| CIV-2960 | Diligencia de ordenación que recibe la oposición a la apelación y la impugnación de la sentencia | `diligencia-ordenacion-recibe-oposicion-apelacion-civ-2960` |
| CIV-2961 | Diligencia de ordenación que admite la reposición contra el auto que rechaza la reconvención | `diligencia-ordenacion-admite-reposicion-contra-auto-civ-2961` |
| CIV-2962 | Diligencia de ordenación que pide a la actora elegir fuero por falta de competencia territorial | `diligencia-ordenacion-pide-actora-elegir-fuero-falta-civ-2962` |
| CIV-2965 | Diligencia de ordenación que requiere a la actora para que la demanda la firmen abogado y procurador | `diligencia-ordenacion-requiere-actora-demanda-firmen-civ-2965` |
| CIV-2968 | Diligencia de ordenación que pide a la actora certificaciones antes de admitir la demanda | `diligencia-ordenacion-pide-actora-certificaciones-civ-2968` |
| CIV-2970 | Diligencia de ordenación que da audiencia al actor y al Fiscal sobre la competencia territorial | `diligencia-ordenacion-da-audiencia-actor-fiscal-sobre-civ-2970` |
| CIV-2972 | Diligencia de ordenación que cita a las partes a la vista con los apercibimientos legales | `diligencia-ordenacion-cita-partes-vista-civ-2972` |
| CIV-2974 | Diligencia de ordenación que cita a la vista con apercibimientos tras contestarse la reconvención | `diligencia-ordenacion-cita-vista-apercibimientos-tras-civ-2974` |
| CIV-2975 | Diligencia de ordenación que anula la vista señalada y fija otra por incomparecencia de un testigo | `diligencia-ordenacion-anula-vista-senalada-fija-otra-civ-2975` |
| CIV-2976 | Diligencia de ordenación que rechaza la excusa del testigo para no comparecer a la vista | `diligencia-ordenacion-rechaza-excusa-testigo-no-civ-2976` |
| CIV-2977 | Diligencia de ordenación que oye a las partes sobre un nuevo señalamiento por ausencia de un testigo | `diligencia-ordenacion-oye-partes-sobre-nuevo-civ-2977` |
| CIV-2978 | Diligencia de ordenación que tiene por interpuesta la apelación contra la sentencia matrimonial | `diligencia-ordenacion-tiene-interpuesta-apelacion-civ-2978` |
| CIV-2982 | Diligencia de inventario de los bienes matrimoniales sin acuerdo entre los cónyuges | `diligencia-inventario-bienes-matrimoniales-sin-acuerdo-civ-2982` |
| CIV-2984 | Diligencia de ordenación que oficia al Registro Civil para anotar la nulidad canónica convalidada | `diligencia-ordenacion-oficia-registro-civil-anotar-civ-2984` |
| CIV-2985 | Diligencia de ordenación que une informe fiscal y postura del cónyuge sobre la nulidad canónica | `diligencia-ordenacion-une-informe-fiscal-postura-civ-2985` |
| CIV-3005 | Diligencia de ordenación que manda librar mandamiento al Registro de la Propiedad o Mercantil | `diligencia-ordenacion-manda-librar-mandamiento-civ-3005` |
