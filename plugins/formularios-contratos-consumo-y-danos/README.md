# Contratos civiles, consumo y reclamación de daños

> Plugin de Claude Code `formularios-contratos-consumo-y-danos` · **173 formularios** · Civil · normativa revisada el 24-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Para los contratos y la responsabilidad civil: compraventa, préstamo, permuta, obra y servicios entre particulares, reclamaciones de consumo y cláusulas abusivas, seguros reclamados por particulares, resolución e incumplimiento de contratos y reclamación de daños y perjuicios.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 173 está al final):

- **Demandas, peticiones y solicitudes iniciales** (72). Por ejemplo: Demanda de juicio ordinario para resolver un contrato de franquicia; Demanda de juicio ordinario para anular un depósito estructurado por error; Demanda de una aseguradora contra otra en ejercicio de la acción de repetición.
- **Contestaciones, oposiciones y alegaciones** (6). Por ejemplo: Contestación a la demanda de rescisión por lesión (Derecho civil catalán); Contestación a la demanda de repetición de la aseguradora contra el asegurado; Contestación del demandado a la demanda por incumplimiento de venta de bienes muebles a plazos.
- **Contratos, pactos y cláusulas** (54). Por ejemplo: Contrato de ejecución de obra entre comitente y contratista; Contrato de compraventa de vivienda en construcción según el Derecho civil catalán; Contrato de promesa bilateral de compraventa.
- **Estatutos, actas, certificaciones y escrituras** (1). Por ejemplo: Escritura de poder para realizar actos de disposición.
- **Comunicaciones, requerimientos y cartas** (26). Por ejemplo: Reclamación extrajudicial previa de los gastos de formalización de una hipoteca; Requerimiento del comprador para resolver la compraventa de inmueble e indemnizar daños y perjuicios; Requerimiento al promotor para resolver la compraventa de vivienda sobre plano y devolver lo pagado.
- **Escritos de trámite y otros** (14). Por ejemplo: Escrito de desistimiento del tomador de un seguro de vida; Escrito del consumidor para desistir de servicios financieros contratados a distancia; Documento de desistimiento del comprador en un contrato de compraventa.

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Demanda de reclamación de cantidad por incumplimiento de contrato»
   - «Reclamación de daños por un accidente»
   - «Nulidad de una cláusula abusiva en un contrato con consumidor»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-contratos-consumo-y-danos:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-contratos-consumo-y-danos:escrito-desistimiento-tomador-seguro-vida-civ-0683`. Los nombres están en la lista de formularios de abajo.

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
- **Espacio que ocupa:** unos 10.418 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-contratos-consumo-y-danos@formularios-juridicos-civil-espana`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-civil-espana
/plugin install formularios-contratos-consumo-y-danos@formularios-juridicos-civil-espana
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-civil-espana`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-contratos-consumo-y-danos.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (173)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0683 | Escrito de desistimiento del tomador de un seguro de vida | `escrito-desistimiento-tomador-seguro-vida-civ-0683` |
| CIV-0684 | Escrito del consumidor para desistir de servicios financieros contratados a distancia | `escrito-consumidor-desistir-servicios-financieros-civ-0684` |
| CIV-0685 | Contrato de ejecución de obra entre comitente y contratista | `contrato-ejecucion-obra-entre-comitente-contratista-civ-0685` |
| CIV-0686 | Contrato de compraventa de vivienda en construcción según el Derecho civil catalán | `contrato-compraventa-vivienda-construccion-segun-civ-0686` |
| CIV-0687 | Contrato de promesa bilateral de compraventa | `contrato-promesa-bilateral-compraventa-civ-0687` |
| CIV-0688 | Demanda de juicio ordinario para resolver un contrato de franquicia | `demanda-juicio-ordinario-resolver-contrato-franquicia-civ-0688` |
| CIV-0689 | Demanda de juicio ordinario para anular un depósito estructurado por error | `demanda-juicio-ordinario-anular-deposito-estructurado-civ-0689` |
| CIV-0690 | Demanda de una aseguradora contra otra en ejercicio de la acción de repetición | `demanda-aseguradora-contra-otra-ejercicio-accion-civ-0690` |
| CIV-0691 | Reclamación extrajudicial previa de los gastos de formalización de una hipoteca | `reclamacion-extrajudicial-previa-gastos-formalizacion-civ-0691` |
| CIV-0692 | Demanda de juicio ordinario contra la aseguradora por impago de un seguro contra robo | `demanda-juicio-ordinario-contra-aseguradora-impago-civ-0692` |
| CIV-0693 | Demanda de daños y perjuicios del franquiciado tras la resolución del contrato de franquicia | `demanda-danos-perjuicios-franquiciado-tras-resolucion-civ-0693` |
| CIV-0694 | Contrato de compraventa de vivienda, local o plaza de garaje | `contrato-compraventa-vivienda-local-plaza-garaje-civ-0694` |
| CIV-0695 | Demanda de juicio ordinario para resolver un contrato de servicios con préstamo vinculado | `demanda-juicio-ordinario-resolver-contrato-servicios-civ-0695` |
| CIV-0696 | Contrato de alquiler de vehículo sin conductor | `contrato-alquiler-vehiculo-sin-conductor-civ-0696` |
| CIV-0697 | Demanda del beneficiario contra la aseguradora que deniega la indemnización de un seguro de vida | `demanda-beneficiario-contra-aseguradora-deniega-civ-0697` |
| CIV-0698 | Demanda de juicio ordinario del beneficiario por incumplimiento de un seguro de accidentes | `demanda-juicio-ordinario-beneficiario-incumplimiento-civ-0698` |
| CIV-0699 | Requerimiento del comprador para resolver la compraventa de inmueble e indemnizar daños y perjuicios | `requerimiento-comprador-resolver-compraventa-inmueble-civ-0699` |
| CIV-0700 | Requerimiento al promotor para resolver la compraventa de vivienda sobre plano y devolver lo pagado | `requerimiento-promotor-resolver-compraventa-vivienda-civ-0700` |
| CIV-0701 | Requerimiento al vendedor para resolver la compraventa de una plaza de garaje por incumplimiento | `requerimiento-vendedor-resolver-compraventa-plaza-civ-0701` |
| CIV-0702 | Requerimiento para resolver la compraventa de inmueble por retraso y devolver lo pagado | `requerimiento-resolver-compraventa-inmueble-retraso-civ-0702` |
| CIV-0703 | Requerimiento al avalista (banco o aseguradora) de devolver lo pagado tras resolver la compraventa | `requerimiento-avalista-banco-aseguradora-devolver-lo-civ-0703` |
| CIV-0704 | Contrato de cesión de bienes a los acreedores en pago de deudas | `contrato-cesion-bienes-acreedores-pago-deudas-civ-0704` |
| CIV-0705 | Contrato de opción de compra con o sin precio | `contrato-opcion-compra-sin-precio-civ-0705` |
| CIV-0706 | Contrato de ejecución de obra con anexos de planos y valoración | `contrato-ejecucion-obra-anexos-planos-valoracion-civ-0706` |
| CIV-0707 | Comunicación al vendedor de falta de conformidad del producto de uso especial y reparación | `comunicacion-vendedor-falta-conformidad-producto-uso-civ-0707` |
| CIV-0708 | Comunicación al vendedor de la resolución del contrato por reparación o sustitución insatisfactoria | `comunicacion-vendedor-resolucion-contrato-reparacion-civ-0708` |
| CIV-0709 | Contrato de ejecución de obra con aportación de materiales por el contratista | `contrato-ejecucion-obra-aportacion-materiales-civ-0709` |
| CIV-0710 | Reclamación de daños por defectos en la calidad del suministro eléctrico | `reclamacion-danos-defectos-calidad-suministro-electrico-civ-0710` |
| CIV-0711 | Comunicación al vendedor de falta de conformidad del producto y petición de reparación o cambio | `comunicacion-vendedor-falta-conformidad-producto-civ-0711` |
| CIV-0712 | Comunicación del consumidor que acepta la modificación del contrato de viaje combinado | `comunicacion-consumidor-acepta-modificacion-contrato-civ-0712` |
| CIV-0713 | Comunicación del consumidor que resuelve el contrato de viaje combinado | `comunicacion-consumidor-resuelve-contrato-viaje-civ-0713` |
| CIV-0714 | Reclamación a la aerolínea por denegación de embarque por overbooking | `reclamacion-aerolinea-denegacion-embarque-overbooking-civ-0714` |
| CIV-0715 | Reclamación a la aerolínea por daños o pérdida del equipaje facturado | `reclamacion-aerolinea-danos-perdida-equipaje-facturado-civ-0715` |
| CIV-0716 | Comunicación al organizador o minorista de incumplimientos en la ejecución del viaje combinado | `comunicacion-organizador-minorista-incumplimientos-civ-0716` |
| CIV-0717 | Reclamación a la aerolínea por cambio de clase del pasajero en el vuelo contratado | `reclamacion-aerolinea-cambio-clase-pasajero-vuelo-civ-0717` |
| CIV-0718 | Reclamación a la aerolínea por retraso del vuelo contratado | `reclamacion-aerolinea-retraso-vuelo-contratado-civ-0718` |
| CIV-0719 | Documento de desistimiento del comprador en un contrato de compraventa | `documento-desistimiento-comprador-contrato-compraventa-civ-0719` |
| CIV-0720 | Comunicación al minorista u organizador de la cesión de la reserva de un viaje combinado | `comunicacion-minorista-u-organizador-cesion-reserva-civ-0720` |
| CIV-0721 | Hoja de reclamación en servicios de asistencia técnica de aparatos de uso doméstico | `hoja-reclamacion-servicios-asistencia-tecnica-aparatos-civ-0721` |
| CIV-0722 | Hoja de reclamación en talleres de reparación de vehículos | `hoja-reclamacion-talleres-reparacion-vehiculos-civ-0722` |
| CIV-0723 | Reclamación extrajudicial a la operadora por defectos en el servicio de telefonía | `reclamacion-extrajudicial-operadora-defectos-servicio-civ-0723` |
| CIV-0724 | Desistimiento del consumidor en servicios financieros a distancia con datos del producto adquirido | `desistimiento-consumidor-servicios-financieros-civ-0724` |
| CIV-0725 | Ejecución de obra o instalación (contrato) | `ejecucion-obra-instalacion-contrato-civ-0725` |
| CIV-0726 | Reclamación a la aerolínea por cancelación del vuelo contratado | `reclamacion-aerolinea-cancelacion-vuelo-contratado-civ-0726` |
| CIV-0727 | Contrato de arrendamiento de bienes muebles según modelo aprobado por la DGRN el 13 de marzo de 2000 | `contrato-arrendamiento-bienes-muebles-segun-modelo-civ-0727` |
| CIV-0728 | Contrato de transacción para poner fin a un pleito ya iniciado | `contrato-transaccion-poner-fin-pleito-ya-iniciado-civ-0728` |
| CIV-0729 | Contrato de alquiler de equipos informáticos | `contrato-alquiler-equipos-informaticos-civ-0729` |
| CIV-0730 | Contrato de venta de un local comercial | `contrato-venta-local-comercial-civ-0730` |
| CIV-0731 | Contrato de obra para la demolición de una edificación | `contrato-obra-demolicion-edificacion-civ-0731` |
| CIV-0732 | Contrato de servicios profesionales de asesoría jurídica o de abogado | `contrato-servicios-profesionales-asesoria-juridica-civ-0732` |
| CIV-0733 | Carta a la aseguradora reclamando el pago de la cobertura de un seguro de defensa jurídica | `carta-aseguradora-reclamando-pago-cobertura-seguro-civ-0733` |
| CIV-0734 | Demanda de juicio verbal para que se haga una obra y se indemnice, contra fontanero y aseguradora | `demanda-juicio-verbal-haga-obra-indemnice-contra-civ-0734` |
| CIV-0735 | Demanda de juicio ordinario para reclamar el precio impagado de una compraventa | `demanda-juicio-ordinario-reclamar-precio-impagado-civ-0735` |
| CIV-0736 | Demanda de juicio verbal contra conductor y aseguradora por daños y lucro cesante en accidente | `demanda-juicio-verbal-contra-conductor-aseguradora-civ-0736` |
| CIV-0737 | Demanda de juicio verbal contra la aseguradora por incumplir el seguro de defensa jurídica | `demanda-juicio-verbal-contra-aseguradora-incumplir-civ-0737` |
| CIV-0738 | Demanda de juicio ordinario para resolver un suministro con exclusiva y reclamar cantidad | `demanda-juicio-ordinario-resolver-suministro-exclusiva-civ-0738` |
| CIV-0739 | Contrato de venta a plazos de bienes muebles conforme a la Ley de Venta a Plazos | `contrato-venta-plazos-bienes-muebles-conforme-ley-civ-0739` |
| CIV-0740 | Contrato de venta a plazos de bienes muebles conforme a la Ley de Consumidores y Usuarios de 2007 | `contrato-venta-plazos-bienes-muebles-conforme-ley-civ-0740` |
| CIV-0741 | Contrato de servicios de mantenimiento entre un cliente y una empresa | `contrato-servicios-mantenimiento-entre-cliente-empresa-civ-0741` |
| CIV-0742 | Contrato de servicios entre una aseguradora y un perito tasador | `contrato-servicios-entre-aseguradora-perito-tasador-civ-0742` |
| CIV-0743 | Contrato de servicios de limpieza entre una comunidad de propietarios y una empresa | `contrato-servicios-limpieza-entre-comunidad-civ-0743` |
| CIV-0744 | Contrato de construcción de un edificio de viviendas con mano de obra y materiales del constructor | `contrato-construccion-edificio-viviendas-mano-obra-civ-0744` |
| CIV-0745 | Oferta motivada de la aseguradora al perjudicado sin reclamación previa | `oferta-motivada-aseguradora-perjudicado-sin-civ-0745` |
| CIV-0746 | Reclamación del conductor perjudicado a la compañía aseguradora | `reclamacion-conductor-perjudicado-compania-aseguradora-civ-0746` |
| CIV-0747 | Demanda del asegurado contra su propia compañía aseguradora | `demanda-asegurado-contra-propia-compania-aseguradora-civ-0747` |
| CIV-0748 | Carta del comprador resolviendo la compraventa de un vehículo y reclamando cantidad | `carta-comprador-resolviendo-compraventa-vehiculo-civ-0748` |
| CIV-0749 | Demanda para resolver la compra de vivienda en construcción y reclamar lo entregado al banco | `demanda-resolver-compra-vivienda-construccion-reclamar-civ-0749` |
| CIV-0750 | Demanda de juicio ordinario por incumplimiento de un contrato de obra a precio alzado | `demanda-juicio-ordinario-incumplimiento-contrato-obra-civ-0750` |
| CIV-0751 | Demanda de juicio ordinario para exigir el cumplimiento de un contrato de suministro mercantil | `demanda-juicio-ordinario-exigir-cumplimiento-contrato-civ-0751` |
| CIV-0752 | Demanda de juicio ordinario contra el banco por comisiones por descubiertos y efectos devueltos | `demanda-juicio-ordinario-contra-banco-comisiones-civ-0752` |
| CIV-0753 | Demanda del cooperativista para que la cooperativa de viviendas le devuelva lo aportado | `demanda-cooperativista-cooperativa-viviendas-le-civ-0753` |
| CIV-0754 | Impugnación de la jura de cuentas del abogado por partidas indebidas | `impugnacion-jura-cuentas-abogado-partidas-indebidas-civ-0754` |
| CIV-0755 | Impugnación de la jura de cuentas del abogado por honorarios excesivos | `impugnacion-jura-cuentas-abogado-honorarios-excesivos-civ-0755` |
| CIV-0756 | Demanda de juicio ordinario contra el banco por la ejecución de un aval a primer requerimiento | `demanda-juicio-ordinario-contra-banco-ejecucion-aval-civ-0756` |
| CIV-0757 | Demanda del subcontratista contra el dueño de la obra por la acción directa del artículo 1597 CC | `demanda-subcontratista-contra-dueno-obra-accion-civ-0757` |
| CIV-0758 | Contrato de construcción de obra llave en mano | `contrato-construccion-obra-llave-mano-civ-0758` |
| CIV-0759 | Documento de resolución por mutuo acuerdo de una compraventa de inmueble | `documento-resolucion-mutuo-acuerdo-compraventa-inmueble-civ-0759` |
| CIV-0760 | Carta comunicando la resolución del contrato por retraso en la construcción de las viviendas | `carta-comunicando-resolucion-contrato-retraso-civ-0760` |
| CIV-0761 | Requerimiento al comprador para otorgar la escritura de la vivienda | `requerimiento-comprador-otorgar-escritura-vivienda-civ-0761` |
| CIV-0762 | Acuerdo de quita de una deuda entre acreedor y deudor | `acuerdo-quita-deuda-entre-acreedor-deudor-civ-0762` |
| CIV-0763 | Demanda de juicio ordinario por daños de tráfico tras juicio por delito leve y reserva de acciones | `demanda-juicio-ordinario-danos-trafico-tras-juicio-civ-0763` |
| CIV-0764 | Demanda de juicio ordinario de repetición contra el obligado cuando pagó un tercero | `demanda-juicio-ordinario-repeticion-contra-obligado-civ-0764` |
| CIV-0765 | Demanda de juicio ordinario por cobro de lo indebido | `demanda-juicio-ordinario-cobro-lo-indebido-civ-0765` |
| CIV-0766 | Demanda de responsabilidad civil por la infidelidad de un cónyuge | `demanda-responsabilidad-civil-infidelidad-conyuge-civ-0766` |
| CIV-0767 | Demanda para resolver una compraventa mercantil por incumplimiento del vendedor y reclamar cantidad | `demanda-resolver-compraventa-mercantil-incumplimiento-civ-0767` |
| CIV-0768 | Demanda de repetición de la aseguradora contra el conductor condenado por delito vial | `demanda-repeticion-aseguradora-contra-conductor-civ-0768` |
| CIV-0769 | Contestación a la demanda de rescisión por lesión (Derecho civil catalán) | `contestacion-demanda-rescision-lesion-derecho-civil-civ-0769` |
| CIV-0770 | Contestación a la demanda de repetición de la aseguradora contra el asegurado | `contestacion-demanda-repeticion-aseguradora-contra-civ-0770` |
| CIV-0771 | Demanda contra la aseguradora para cobrar la indemnización de un siniestro de responsabilidad civil | `demanda-contra-aseguradora-cobrar-indemnizacion-civ-0771` |
| CIV-0772 | Demanda de juicio ordinario para anular una compraventa por extralimitación del mandatario | `demanda-juicio-ordinario-anular-compraventa-civ-0772` |
| CIV-0773 | Demanda de juicio ordinario para exigir el cumplimiento de una compraventa de bien mueble | `demanda-juicio-ordinario-exigir-cumplimiento-civ-0773` |
| CIV-0774 | Demanda por incumplimiento de la entrega en una venta como cuerpo cierto con defecto de cabida | `demanda-incumplimiento-entrega-venta-como-cuerpo-civ-0774` |
| CIV-0775 | Demanda de juicio verbal contra la aseguradora por incumplimiento del seguro combinado del hogar | `demanda-juicio-verbal-contra-aseguradora-civ-0775` |
| CIV-0776 | Autorización notarial para el uso de un vehículo | `autorizacion-notarial-uso-vehiculo-civ-0776` |
| CIV-0777 | Contrato de compraventa de vivienda destinada a domicilio familiar | `contrato-compraventa-vivienda-destinada-domicilio-civ-0777` |
| CIV-0778 | Demanda por incumplimiento de compraventa de inmueble entregado con menor cabida de la pactada | `demanda-incumplimiento-compraventa-inmueble-entregado-civ-0778` |
| CIV-0779 | Demanda de juicio ordinario de repetición entre deudores solidarios condenados | `demanda-juicio-ordinario-repeticion-entre-deudores-civ-0779` |
| CIV-0780 | Demanda genérica de juicio ordinario de reclamación de cantidad por incumplimiento de contrato | `demanda-generica-juicio-ordinario-reclamacion-cantidad-civ-0780` |
| CIV-0781 | Demanda de juicio verbal para resolver un arrendamiento de bienes muebles | `demanda-juicio-verbal-resolver-arrendamiento-bienes-civ-0781` |
| CIV-0782 | Demanda de repetición de la promotora contra arquitecto, aparejador y constructora de la edificación | `demanda-repeticion-promotora-contra-arquitecto-civ-0782` |
| CIV-0783 | Demanda de nulidad de un contrato de permuta financiera (swap) contra el banco | `demanda-nulidad-contrato-permuta-financiera-swap-civ-0783` |
| CIV-0784 | Demanda de juicio ordinario para exigir escritura pública de una compraventa privada | `demanda-juicio-ordinario-exigir-escritura-publica-civ-0784` |
| CIV-0785 | Demanda de juicio ordinario para resolver el contrato por entrega de cosa distinta (aliud pro alio) | `demanda-juicio-ordinario-resolver-contrato-entrega-civ-0785` |
| CIV-0786 | Demanda de reclamación de cantidad por contrato de obra contra una sociedad civil irregular | `demanda-reclamacion-cantidad-contrato-obra-contra-civ-0786` |
| CIV-0787 | Demanda para resolver la compraventa de inmueble por retraso en la entrega y recuperar lo pagado | `demanda-resolver-compraventa-inmueble-retraso-entrega-civ-0787` |
| CIV-0788 | Demanda para resolver la compraventa de inmueble por falta de entrega del bien por la promotora | `demanda-resolver-compraventa-inmueble-falta-entrega-civ-0788` |
| CIV-0789 | Demanda de juicio ordinario para exigir el cumplimiento de una permuta inmobiliaria | `demanda-juicio-ordinario-exigir-cumplimiento-permuta-civ-0789` |
| CIV-0790 | Demanda de rescisión de un contrato garantizado con hipoteca | `demanda-rescision-contrato-garantizado-hipoteca-civ-0790` |
| CIV-0791 | Contrato por el que se ceden créditos | `contrato-ceden-creditos-civ-0791` |
| CIV-0792 | Carta de pago en que el acreedor confiesa haber cobrado la deuda | `carta-pago-acreedor-confiesa-haber-cobrado-deuda-civ-0792` |
| CIV-0793 | Contrato de permuta de una vivienda por obra a edificar | `contrato-permuta-vivienda-obra-edificar-civ-0793` |
| CIV-0794 | Contrato de cesión de posición contractual | `contrato-cesion-posicion-contractual-civ-0794` |
| CIV-0795 | Contrato por el que se ceden derechos | `contrato-ceden-derechos-civ-0795` |
| CIV-0796 | Escritura de poder para realizar actos de disposición | `escritura-poder-realizar-actos-disposicion-civ-0796` |
| CIV-0797 | Contrato de ejecución de obra | `contrato-ejecucion-obra-civ-0797` |
| CIV-0798 | Contrato de compraventa de un local en construcción | `contrato-compraventa-local-construccion-civ-0798` |
| CIV-0799 | Contrato de venta de una vivienda urbana | `contrato-venta-vivienda-urbana-civ-0799` |
| CIV-0800 | Contrato de arras penitenciales con facultad de desistir | `contrato-arras-penitenciales-facultad-desistir-civ-0800` |
| CIV-0801 | Contrato de arras confirmatorias sobre una finca | `contrato-arras-confirmatorias-sobre-finca-civ-0801` |
| CIV-0802 | Contrato de opción de compra | `contrato-opcion-compra-civ-0802` |
| CIV-0803 | Contrato de compraventa de un bien inmueble | `contrato-compraventa-bien-inmueble-civ-0803` |
| CIV-0804 | Contestación del demandado a la demanda por incumplimiento de venta de bienes muebles a plazos | `contestacion-demandado-demanda-incumplimiento-venta-civ-0804` |
| CIV-0805 | Demanda de juicio verbal de reclamación de cantidad por compraventa, obra, contrato mixto o atípico | `demanda-juicio-verbal-reclamacion-cantidad-compraventa-civ-0805` |
| CIV-0806 | Demanda breve de juicio verbal de reclamación de cantidad | `demanda-breve-juicio-verbal-reclamacion-cantidad-civ-0806` |
| CIV-0807 | Demanda sobre venta de bienes muebles a plazos con exhibición de los bienes y depositario | `demanda-sobre-venta-bienes-muebles-plazos-exhibicion-civ-0807` |
| CIV-0808 | Demanda de juicio ordinario de reclamación de cantidad contra una sociedad y su administrador | `demanda-juicio-ordinario-reclamacion-cantidad-contra-civ-0808` |
| CIV-0809 | Demanda de juicio ordinario por impago de géneros suministrados, con intereses desde la compraventa | `demanda-juicio-ordinario-impago-generos-suministrados-civ-0809` |
| CIV-0810 | Demanda ordinaria de nulidad del contrato y, subsidiariamente, incumplimiento e indemnización | `demanda-ordinaria-nulidad-contrato-subsidiariamente-civ-0810` |
| CIV-0811 | Contestación por incumplimiento contractual con reconvención de resolución e indemnización | `contestacion-incumplimiento-contractual-reconvencion-civ-0811` |
| CIV-0812 | Demanda de juicio ordinario de impugnación de condiciones generales de la contratación (Ley 7 1998) | `demanda-juicio-ordinario-impugnacion-condiciones-civ-0812` |
| CIV-0813 | Compraventa de vehículo (contrato) | `compraventa-vehiculo-contrato-civ-0813` |
| CIV-0814 | Documento de reconocimiento de deuda con aplazamiento de pago | `documento-reconocimiento-deuda-aplazamiento-pago-civ-0814` |
| CIV-0815 | Demanda de juicio ordinario por incumplimiento de contrato de compraventa | `demanda-juicio-ordinario-incumplimiento-contrato-civ-0815` |
| CIV-0816 | Demanda de juicio ordinario de reclamación de cantidad por ejecución de obra civil | `demanda-juicio-ordinario-reclamacion-cantidad-civ-0816` |
| CIV-0817 | Demanda de juicio ordinario de reclamación de cantidad y enriquecimiento injusto en contrato de obra | `demanda-juicio-ordinario-reclamacion-cantidad-civ-0817` |
| CIV-0818 | Demanda ordinaria de rescisión por lesión según el Código civil catalán, con dictamen pericial | `demanda-ordinaria-rescision-lesion-segun-codigo-civil-civ-0818` |
| CIV-0819 | Demanda de juicio verbal de reclamación de cantidad por contrato de obra entre 2.000 y 15.000 euros | `demanda-juicio-verbal-reclamacion-cantidad-contrato-civ-0819` |
| CIV-0820 | Demanda ordinaria por daños materiales en accidente de tráfico contra concesionaria y aseguradora | `demanda-ordinaria-danos-materiales-accidente-trafico-civ-0820` |
| CIV-0821 | Demanda de juicio ordinario de nulidad de compraventa por simulación absoluta | `demanda-juicio-ordinario-nulidad-compraventa-civ-0821` |
| CIV-0822 | Contestación a demanda ordinaria de conductor y aseguradora codemandados por daños de un accidente | `contestacion-demanda-ordinaria-conductor-aseguradora-civ-0822` |
| CIV-0823 | Demanda de juicio verbal por daños en cosas de tráfico contra el Consorcio de Seguros | `demanda-juicio-verbal-danos-cosas-trafico-contra-civ-0823` |
| CIV-0824 | Demanda de juicio ordinario de resolución de compraventa de plaza de garaje por incumplimiento | `demanda-juicio-ordinario-resolucion-compraventa-plaza-civ-0824` |
| CIV-0825 | Demanda de juicio ordinario por daños de tráfico contra conductor, propietario y aseguradora | `demanda-juicio-ordinario-danos-trafico-contra-civ-0825` |
| CIV-0826 | Demanda de juicio ordinario contra la aseguradora por lesiones derivadas de accidente de tráfico | `demanda-juicio-ordinario-contra-aseguradora-lesiones-civ-0826` |
| CIV-0827 | Contrato de obra de vivienda unifamiliar a precio alzado con pago aplazado | `contrato-obra-vivienda-unifamiliar-precio-alzado-pago-civ-0827` |
| CIV-0828 | Contrato de compraventa de bien mueble con exclusión de la responsabilidad por evicción | `contrato-compraventa-bien-mueble-exclusion-civ-0828` |
| CIV-0829 | Contrato de permuta de inmuebles futuros que se adquirirán por herencia | `contrato-permuta-inmuebles-futuros-adquiriran-herencia-civ-0829` |
| CIV-0830 | Contrato de compraventa de bien mueble con entrega simultánea al pago o diferida | `contrato-compraventa-bien-mueble-entrega-simultanea-civ-0830` |
| CIV-0831 | Contrato de compraventa de bien futuro pendiente de adjudicación de herencia, con pago aplazado | `contrato-compraventa-bien-futuro-pendiente-civ-0831` |
| CIV-0832 | Contrato de resolución de compraventa de vivienda adjudicada a otro, con restitución y mejora | `contrato-resolucion-compraventa-vivienda-adjudicada-civ-0832` |
| CIV-0833 | Contrato de comodato de una máquina a cambio de cancelar un préstamo personal | `contrato-comodato-maquina-cambio-cancelar-prestamo-civ-0833` |
| CIV-0834 | Contrato de restitución de un bien recibido de mala fe por error de entrega | `contrato-restitucion-bien-recibido-mala-fe-error-civ-0834` |
| CIV-0835 | Cláusula de garantía y retención de parte del precio en un contrato de obra de vivienda | `clausula-garantia-retencion-parte-precio-contrato-obra-civ-0835` |
| CIV-0836 | Contrato de compraventa de bien mueble embargado con descuento de la deuda del precio | `contrato-compraventa-bien-mueble-embargado-descuento-civ-0836` |
| CIV-0837 | Contrato de promesa de compraventa de inmueble con cláusula penal y pago aplazado | `contrato-promesa-compraventa-inmueble-clausula-penal-civ-0837` |
| CIV-0838 | Contrato de obra de vivienda unifamiliar entre propietario y constructor con pago aplazado | `contrato-obra-vivienda-unifamiliar-entre-propietario-civ-0838` |
| CIV-0839 | Contrato de restitución y mejora de un bien mueble transmitido sin consentimiento | `contrato-restitucion-mejora-bien-mueble-transmitido-civ-0839` |
| CIV-0840 | Contrato de compraventa de piso en construcción con pago aplazado y entrega diferida | `contrato-compraventa-piso-construccion-pago-aplazado-civ-0840` |
| CIV-0841 | Contrato de compraventa de inmueble urbano con compromiso de elevarlo a escritura pública | `contrato-compraventa-inmueble-urbano-compromiso-civ-0841` |
| CIV-0842 | Contrato de renta vitalicia con garantía y condición resolutoria | `contrato-renta-vitalicia-garantia-condicion-resolutoria-civ-0842` |
| CIV-0843 | Contrato de permuta de bienes inmuebles | `contrato-permuta-bienes-inmuebles-civ-0843` |
| CIV-0844 | Contrato de permuta de bienes muebles con cláusula condicional de prueba | `contrato-permuta-bienes-muebles-clausula-condicional-civ-0844` |
| CIV-0845 | Demanda de juicio ordinario por daños derivados de accidente de circulación de vehículos de motor | `demanda-juicio-ordinario-danos-derivados-accidente-civ-0845` |
| CIV-0846 | Demanda de juicio verbal por reclamación de cantidad por contrato de obra de hasta 2.000 euros | `demanda-juicio-verbal-reclamacion-cantidad-contrato-civ-0846` |
| CIV-0847 | Demanda sucinta de juicio verbal por daños derivados de la circulación de vehículos de motor | `demanda-sucinta-juicio-verbal-danos-derivados-civ-0847` |
| CIV-0848 | Demanda de juicio ordinario para resolver una compraventa de inmueble por impago e indemnizar daños | `demanda-juicio-ordinario-resolver-compraventa-inmueble-civ-0848` |
| CIV-0849 | Demanda de juicio ordinario por las arras dobladas ante el desistimiento en la venta de un inmueble | `demanda-juicio-ordinario-arras-dobladas-ante-civ-0849` |
| CIV-0850 | Demanda de juicio ordinario por accidente de tráfico contra el Consorcio de Compensación de Seguros | `demanda-juicio-ordinario-accidente-trafico-contra-civ-0850` |
| CIV-0851 | Demanda contra la agencia minorista por defectuosa prestación de servicios de un viaje combinado | `demanda-contra-agencia-minorista-defectuosa-prestacion-civ-0851` |
| CIV-0852 | Demanda por deuda reconocida en documento privado con causa fiduciaria o simulación relativa | `demanda-deuda-reconocida-documento-privado-causa-civ-0852` |
| CIV-0853 | Demanda de juicio ordinario para reclamar honorarios de asesoramiento jurídico por iguala | `demanda-juicio-ordinario-reclamar-honorarios-civ-0853` |
| CIV-0854 | Escrito del demandante frente a la alegación de un crédito compensable por el demandado | `escrito-demandante-frente-alegacion-credito-civ-0854` |
| CIV-0855 | Contestación a la demanda alegando nulidad de la compraventa de vivienda por dolo | `contestacion-demanda-alegando-nulidad-compraventa-civ-0855` |

## Privacidad

Ver `PRIVACY.md`.
