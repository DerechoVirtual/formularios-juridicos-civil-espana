---
name: indice
description: "Índice de los 101 formularios de Mediación, MASC, arbitraje y jurisdicción voluntaria. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Mediación, MASC, arbitraje y jurisdicción voluntaria: índice de formularios

> Plugin `formularios-mediacion-arbitraje-y-voluntaria` · 101 formularios · normativa revisada el 25-11-2026.

## Qué es

Para resolver sin pleito o por cauces especiales: medios adecuados de solución de controversias (LO 1/2025), mediación civil y familiar, conciliación, arbitraje (convenio, solicitud, recusación, anulación de laudo), expedientes de jurisdicción voluntaria, justicia gratuita y reconocimiento de resoluciones extranjeras.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Solicitud de mediación previa a la demanda (MASC)»
- «Convenio arbitral para un contrato»
- «Demanda de reconocimiento de una sentencia extranjera (exequátur)»

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

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-mediacion-arbitraje-y-voluntaria:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario que se rellena está en `../<skill>/assets/formulario.md` y la guía del tema es el `marco.md` de esta carpeta.

### Demandas, peticiones y solicitudes iniciales (11)

| Código | Formulario | Skill |
|---|---|---|
| CIV-1718 | Solicitud de arbitraje de consumo del consumidor ante la Junta Arbitral | `solicitud-arbitraje-consumo-consumidor-ante-junta-civ-1718` |
| CIV-1732 | Demanda de nulidad de un acuerdo de mediación | `demanda-nulidad-acuerdo-mediacion-civ-1732` |
| CIV-1763 | Demanda de anulación de laudo arbitral por motivos formales | `demanda-anulacion-laudo-arbitral-motivos-formales-civ-1763` |
| CIV-1765 | Demanda de anulación de laudo arbitral por nulidad del convenio arbitral | `demanda-anulacion-laudo-arbitral-nulidad-convenio-civ-1765` |
| CIV-1770 | Demanda arbitral en materia de transporte | `demanda-arbitral-materia-transporte-civ-1770` |
| CIV-1773 | Demanda arbitral de desahucio de un arrendamiento de industria | `demanda-arbitral-desahucio-arrendamiento-industria-civ-1773` |
| CIV-1776 | Solicitud de arbitraje de consumo por un viaje combinado | `solicitud-arbitraje-consumo-viaje-combinado-civ-1776` |
| CIV-1784 | Solicitud de arbitraje de consumo por cláusula abusiva en la compraventa de vivienda | `solicitud-arbitraje-consumo-clausula-abusiva-civ-1784` |
| CIV-1786 | Solicitud de arbitraje de consumo por la facturación de telefonía | `solicitud-arbitraje-consumo-facturacion-telefonia-civ-1786` |
| CIV-1789 | Solicitud de arbitraje ante el Tribunal Arbitral del Colegio de Abogados | `solicitud-arbitraje-ante-tribunal-arbitral-colegio-civ-1789` |
| CIV-1791 | Demanda de anulación de laudo arbitral ante el Tribunal Superior de Justicia | `demanda-anulacion-laudo-arbitral-ante-tribunal-civ-1791` |

### Contestaciones, oposiciones y alegaciones (9)

| Código | Formulario | Skill |
|---|---|---|
| CIV-1707 | Escrito de oposición a la prohibición de transmitir letras de cambio solicitada por el tenedor | `escrito-oposicion-prohibicion-transmitir-letras-cambio-civ-1707` |
| CIV-1738 | Oposición del demandante a la declinatoria por sumisión a mediación en un contrato de consumo | `oposicion-demandante-declinatoria-sumision-mediacion-civ-1738` |
| CIV-1772 | Oposición del demandante a la declinatoria por arbitraje alegando nulidad del convenio arbitral | `oposicion-demandante-declinatoria-arbitraje-alegando-civ-1772` |
| CIV-1778 | Contestación de la empresa a la solicitud de arbitraje con reconvención contra el reclamante | `contestacion-empresa-solicitud-arbitraje-reconvencion-civ-1778` |
| CIV-1779 | Contestación de la empresa al arbitraje alegando que el reclamante no es consumidor | `contestacion-empresa-arbitraje-alegando-reclamante-no-civ-1779` |
| CIV-1782 | Contestación de la empresa que rechaza el arbitraje de consumo | `contestacion-empresa-rechaza-arbitraje-consumo-civ-1782` |
| CIV-1785 | Contestación que rechaza el arbitraje de consumo por estar la empresa reclamada en concurso | `contestacion-rechaza-arbitraje-consumo-estar-empresa-civ-1785` |
| CIV-1787 | Contestación a la reconvención formulada en un arbitraje de consumo | `contestacion-reconvencion-formulada-arbitraje-consumo-civ-1787` |
| CIV-1793 | Alegaciones del reclamante en el trámite de audiencia ante el Colegio Arbitral de Consumo | `alegaciones-reclamante-tramite-audiencia-ante-colegio-civ-1793` |

### Recursos (2)

| Código | Formulario | Skill |
|---|---|---|
| CIV-1780 | Recurso ante la Comisión de Juntas Arbitrales contra la inadmisión de arbitraje de consumo | `recurso-ante-comision-juntas-arbitrales-contra-civ-1780` |
| CIV-1783 | Recurso contra la inadmisión de una solicitud de arbitraje ante la Comisión de Juntas | `recurso-contra-inadmision-solicitud-arbitraje-ante-civ-1783` |

### Contratos, pactos y cláusulas (11)

| Código | Formulario | Skill |
|---|---|---|
| CIV-1720 | Contrato de servicios de mediación | `contrato-servicios-mediacion-civ-1720` |
| CIV-1721 | Cláusula de sometimiento a arbitraje ante una cámara de comercio | `clausula-sometimiento-arbitraje-ante-camara-comercio-civ-1721` |
| CIV-1725 | Pacto de confidencialidad entre las partes de una mediación | `pacto-confidencialidad-entre-partes-mediacion-civ-1725` |
| CIV-1728 | Cláusula contractual de sometimiento previo a mediación | `clausula-contractual-sometimiento-previo-mediacion-civ-1728` |
| CIV-1741 | Acuerdo de mediación sobre un contrato de compraventa | `acuerdo-mediacion-sobre-contrato-compraventa-civ-1741` |
| CIV-1747 | Cláusula contractual de sometimiento a mediación y, en su caso, a arbitraje | `clausula-contractual-sometimiento-mediacion-caso-civ-1747` |
| CIV-1762 | Pacto de confidencialidad de las partes que inician una mediación mercantil | `pacto-confidencialidad-partes-inician-mediacion-civ-1762` |
| CIV-1794 | Cláusula de sumisión a arbitraje en los contratos entre las partes | `clausula-sumision-arbitraje-contratos-entre-partes-civ-1794` |
| CIV-1795 | Contrato de arbitraje entre sociedades mercantiles | `contrato-arbitraje-entre-sociedades-mercantiles-civ-1795` |
| CIV-2887 | Cláusula de sumisión a arbitraje para incluir en un contrato | `clausula-sumision-arbitraje-incluir-contrato-civ-2887` |
| CIV-2890 | Convenio arbitral para someter a arbitraje las controversias de un contrato ya celebrado | `convenio-arbitral-someter-arbitraje-controversias-civ-2890` |

### Estatutos, actas, certificaciones y escrituras (14)

| Código | Formulario | Skill |
|---|---|---|
| CIV-1717 | Acta final del procedimiento de mediación | `acta-final-procedimiento-mediacion-civ-1717` |
| CIV-1722 | Acta de inicio de una mediación intraprocesal derivada de un proceso judicial | `acta-inicio-mediacion-intraprocesal-derivada-proceso-civ-1722` |
| CIV-1723 | Acta final de mediación que termina sin acuerdo | `acta-final-mediacion-termina-sin-acuerdo-civ-1723` |
| CIV-1724 | Acta de constitución de un procedimiento de mediación | `acta-constitucion-procedimiento-mediacion-civ-1724` |
| CIV-1726 | Acta de sesión informativa sin efecto por incomparecencia de una de las partes | `acta-sesion-informativa-sin-efecto-incomparecencia-civ-1726` |
| CIV-1731 | Acta final de mediación que termina con acuerdo entre las partes | `acta-final-mediacion-termina-acuerdo-entre-partes-civ-1731` |
| CIV-1733 | Acta de renuncia del mediador a continuar la mediación | `acta-renuncia-mediador-continuar-mediacion-civ-1733` |
| CIV-1748 | Escritura notarial que eleva a público un acuerdo de mediación | `escritura-notarial-eleva-publico-acuerdo-mediacion-civ-1748` |
| CIV-1749 | Acta de la sesión constitutiva de mediación con pacto de confidencialidad | `acta-sesion-constitutiva-mediacion-pacto-civ-1749` |
| CIV-1752 | Acta inicial de mediación familiar y contrato de mediación | `acta-inicial-mediacion-familiar-contrato-mediacion-civ-1752` |
| CIV-1753 | Acta de cierre de la mediación familiar con los acuerdos alcanzados | `acta-cierre-mediacion-familiar-acuerdos-alcanzados-civ-1753` |
| CIV-1754 | Acta inicial o contrato de mediación familiar sometido al Derecho valenciano | `acta-inicial-contrato-mediacion-familiar-sometido-civ-1754` |
| CIV-1755 | Escritura pública que eleva a público los acuerdos de una mediación familiar | `escritura-publica-eleva-publico-acuerdos-mediacion-civ-1755` |
| CIV-2889 | Acta de audiencia y laudo en el procedimiento especial de arbitraje de consumo | `acta-audiencia-laudo-procedimiento-especial-arbitraje-civ-2889` |

### Comunicaciones, requerimientos y cartas (16)

| Código | Formulario | Skill |
|---|---|---|
| CIV-1709 | Denuncia a la sociedad rectora por robo, destrucción o extravío de valores de mercados oficiales | `denuncia-sociedad-rectora-robo-destruccion-extravio-civ-1709` |
| CIV-1716 | Solicitud conjunta de las partes para someter el conflicto a mediación | `solicitud-conjunta-partes-someter-conflicto-mediacion-civ-1716` |
| CIV-1729 | Solicitud de inicio de mediación por una parte en cumplimiento de un pacto de mediación | `solicitud-inicio-mediacion-parte-cumplimiento-pacto-civ-1729` |
| CIV-1730 | Comunicación al mediador de la decisión de una parte de dar por terminada la mediación | `comunicacion-mediador-decision-parte-dar-terminada-civ-1730` |
| CIV-1735 | Solicitud conjunta de suspender el proceso para intentar una mediación | `solicitud-conjunta-suspender-proceso-intentar-mediacion-civ-1735` |
| CIV-1740 | Solicitud conjunta de mediación por las partes de un contrato de suministro | `solicitud-conjunta-mediacion-partes-contrato-suministro-civ-1740` |
| CIV-1745 | Comunicación de causa que afecta a la imparcialidad del mediador, con conformidad para que siga | `comunicacion-causa-afecta-imparcialidad-mediador-civ-1745` |
| CIV-1746 | Solicitud de autorización judicial para que el progenitor custodio cambie de domicilio | `solicitud-autorizacion-judicial-progenitor-custodio-civ-1746` |
| CIV-1756 | Solicitud de homologación judicial del acuerdo alcanzado en mediación con proceso suspendido | `solicitud-homologacion-judicial-acuerdo-alcanzado-civ-1756` |
| CIV-1757 | Solicitud para dejar sin efecto la declaración de fallecimiento | `solicitud-dejar-sin-efecto-declaracion-fallecimiento-civ-1757` |
| CIV-1764 | Solicitud al tribunal de auxilio judicial para practicar prueba en un arbitraje | `solicitud-tribunal-auxilio-judicial-practicar-prueba-civ-1764` |
| CIV-1766 | Solicitud de inicio de un procedimiento arbitral ante una corte de arbitraje | `solicitud-inicio-procedimiento-arbitral-ante-corte-civ-1766` |
| CIV-1777 | Solicitud genérica de arbitraje de consumo | `solicitud-generica-arbitraje-consumo-civ-1777` |
| CIV-1788 | Solicitud de formalizar el convenio arbitral en el sistema arbitral de consumo | `solicitud-formalizar-convenio-arbitral-sistema-civ-1788` |
| CIV-1790 | Solicitud de designación judicial de árbitro único | `solicitud-designacion-judicial-arbitro-unico-civ-1790` |
| CIV-2886 | Solicitud de acto de conciliación previo a la demanda de desahucio por precario | `solicitud-acto-conciliacion-previo-demanda-desahucio-civ-2886` |

### Escritos de trámite y otros (38)

| Código | Formulario | Skill |
|---|---|---|
| CIV-1705 | Escrito de jurisdicción voluntaria para revocar o cesar nombramientos de auditor | `escrito-jurisdiccion-voluntaria-revocar-cesar-civ-1705` |
| CIV-1706 | Escrito de jurisdicción voluntaria para exigir la exhibición de libros contables | `escrito-jurisdiccion-voluntaria-exigir-exhibicion-civ-1706` |
| CIV-1708 | Escrito de inicio del expediente de jurisdicción voluntaria sobre depósito de mercancías | `escrito-inicio-expediente-jurisdiccion-voluntaria-civ-1708` |
| CIV-1710 | Escrito del perceptor que presta fianza para garantizar la devolución de rendimientos de valores | `escrito-perceptor-presta-fianza-garantizar-devolucion-civ-1710` |
| CIV-1711 | Escrito de inicio del expediente de jurisdicción voluntaria sobre valores mobiliarios sustraídos | `escrito-inicio-expediente-jurisdiccion-voluntaria-civ-1711` |
| CIV-1712 | Escrito de jurisdicción voluntaria para convocar la asamblea general de obligacionistas | `escrito-jurisdiccion-voluntaria-convocar-asamblea-civ-1712` |
| CIV-1713 | Escrito de jurisdicción voluntaria para reducir capital o amortizar o enajenar participaciones | `escrito-jurisdiccion-voluntaria-reducir-capital-civ-1713` |
| CIV-1714 | Escrito para que el emisor pague los rendimientos del título tras seis meses sin oposición | `escrito-emisor-pague-rendimientos-titulo-tras-seis-civ-1714` |
| CIV-1715 | Escrito que comunica a la sociedad rectora la apertura del expediente de jurisdicción voluntaria | `escrito-comunica-sociedad-rectora-apertura-expediente-civ-1715` |
| CIV-1719 | Oferta pública de adhesión del empresario al sistema arbitral de consumo | `oferta-publica-adhesion-empresario-sistema-arbitral-civ-1719` |
| CIV-1727 | Citación de las partes a la sesión informativa de una mediación | `citacion-partes-sesion-informativa-mediacion-civ-1727` |
| CIV-1734 | Escrito conjunto pidiendo homologar un acuerdo parcial de mediación y continuar el proceso | `escrito-conjunto-pidiendo-homologar-acuerdo-parcial-civ-1734` |
| CIV-1736 | Escrito pidiendo levantar la suspensión del proceso porque la mediación terminó sin acuerdo | `escrito-pidiendo-levantar-suspension-proceso-porque-civ-1736` |
| CIV-1737 | Escrito pidiendo levantar la suspensión del proceso porque la mediación quedó sin efecto | `escrito-pidiendo-levantar-suspension-proceso-porque-civ-1737` |
| CIV-1739 | Diligencia de celebración de la sesión informativa de mediación | `diligencia-celebracion-sesion-informativa-mediacion-civ-1739` |
| CIV-1742 | Diligencia de celebración de las sesiones de mediación, conjuntas o individuales | `diligencia-celebracion-sesiones-mediacion-conjuntas-civ-1742` |
| CIV-1743 | Escrito de renuncia del mediador al expediente de mediación | `escrito-renuncia-mediador-expediente-mediacion-civ-1743` |
| CIV-1744 | Escrito de una parte mediada comunicando al mediador que abandona la mediación | `escrito-parte-mediada-comunicando-mediador-abandona-civ-1744` |
| CIV-1750 | Escrito pidiendo suspender el juicio ordinario para intentar la mediación | `escrito-pidiendo-suspender-juicio-ordinario-intentar-civ-1750` |
| CIV-1751 | Escrito pidiendo suspender el juicio verbal para intentar la mediación | `escrito-pidiendo-suspender-juicio-verbal-intentar-civ-1751` |
| CIV-1758 | Escrito de conformidad con la declinatoria por sometimiento a mediación (Ley 5 de 2012) | `escrito-conformidad-declinatoria-sometimiento-civ-1758` |
| CIV-1759 | Escrito pidiendo reanudar el juicio ordinario suspendido tras una mediación sin acuerdo | `escrito-pidiendo-reanudar-juicio-ordinario-suspendido-civ-1759` |
| CIV-1760 | Escrito pidiendo reanudar el juicio verbal suspendido tras una mediación sin acuerdo | `escrito-pidiendo-reanudar-juicio-verbal-suspendido-civ-1760` |
| CIV-1761 | Escrito de declinatoria por haberse sometido la cuestión a mediación | `escrito-declinatoria-haberse-sometido-cuestion-civ-1761` |
| CIV-1767 | Declinatoria de jurisdicción por sometimiento de la cuestión a arbitraje | `declinatoria-jurisdiccion-sometimiento-cuestion-civ-1767` |
| CIV-1768 | Escrito de recusación de un árbitro | `escrito-recusacion-arbitro-civ-1768` |
| CIV-1769 | Petición de complemento del laudo para subsanar una omisión | `peticion-complemento-laudo-subsanar-omision-civ-1769` |
| CIV-1771 | Petición de corrección del laudo por extralimitarse parcialmente el árbitro | `peticion-correccion-laudo-extralimitarse-parcialmente-civ-1771` |
| CIV-1774 | Escrito del reclamante que amplía la solicitud en un arbitraje de consumo | `escrito-reclamante-amplia-solicitud-arbitraje-consumo-civ-1774` |
| CIV-1775 | Aceptación del arbitraje de consumo y contestación a la solicitud (modelo genérico) | `aceptacion-arbitraje-consumo-contestacion-solicitud-civ-1775` |
| CIV-1781 | Recusación de un árbitro en un procedimiento arbitral de consumo | `recusacion-arbitro-procedimiento-arbitral-consumo-civ-1781` |
| CIV-1792 | Encargo de arbitraje a institución arbitral en virtud de convenio arbitral | `encargo-arbitraje-institucion-arbitral-virtud-convenio-civ-1792` |
| CIV-1796 | Escrito solicitando la celebración de acto de conciliación (general) | `escrito-solicitando-celebracion-acto-conciliacion-civ-1796` |
| CIV-2885 | Declinatoria en juicio verbal por haberse sometido la cuestión a arbitraje | `declinatoria-juicio-verbal-haberse-sometido-cuestion-civ-2885` |
| CIV-2888 | Escrito del abogado que acepta el cargo de árbitro | `escrito-abogado-acepta-cargo-arbitro-civ-2888` |
| CIV-2891 | Escrito que acepta la propuesta de la otra parte de someter la controversia a arbitraje | `escrito-acepta-propuesta-otra-parte-someter-civ-2891` |
| CIV-2892 | Escrito de la aseguradora que promueve un expediente de consignación de jurisdicción voluntaria | `escrito-aseguradora-promueve-expediente-consignacion-civ-2892` |
| CIV-2893 | Escrito que aporta el justificante de la consignación en el expediente de jurisdicción voluntaria | `escrito-aporta-justificante-consignacion-expediente-civ-2893` |
