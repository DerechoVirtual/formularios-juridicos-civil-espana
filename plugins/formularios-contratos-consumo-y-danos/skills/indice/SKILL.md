---
name: indice
description: "Índice de los 220 formularios de Contratos civiles y consumo. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Contratos civiles y consumo: índice de formularios

> Plugin `formularios-contratos-consumo-y-danos` · 220 formularios · normativa revisada el 25-11-2026.

## Qué es

Para los contratos entre particulares y con consumidores: compraventa, préstamo, permuta, obra y servicios, renta vitalicia, arras y opción de compra, reclamaciones de consumo y cláusulas abusivas, y resolución e incumplimiento de contratos. Los accidentes, seguros y daños están en `formularios-accidentes-y-responsabilidad-civil`.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Demanda de reclamación de cantidad por incumplimiento de contrato»
- «Contrato de compraventa de vivienda con arras penitenciales»
- «Nulidad de una cláusula abusiva en un contrato con consumidor»

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

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-contratos-consumo-y-danos:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario que se rellena está en `../<skill>/assets/formulario.md` y la guía del tema es el `marco.md` de esta carpeta.

### Demandas, peticiones y solicitudes iniciales (52)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0688 | Demanda de juicio ordinario para resolver un contrato de franquicia | `demanda-juicio-ordinario-resolver-contrato-franquicia-civ-0688` |
| CIV-0689 | Demanda de juicio ordinario para anular un depósito estructurado por error | `demanda-juicio-ordinario-anular-deposito-estructurado-civ-0689` |
| CIV-0735 | Demanda de juicio ordinario para reclamar el precio impagado de una compraventa | `demanda-juicio-ordinario-reclamar-precio-impagado-civ-0735` |
| CIV-0738 | Demanda de juicio ordinario para resolver un suministro con exclusiva y reclamar cantidad | `demanda-juicio-ordinario-resolver-suministro-exclusiva-civ-0738` |
| CIV-0749 | Demanda para resolver la compra de vivienda en construcción y reclamar lo entregado al banco | `demanda-resolver-compra-vivienda-construccion-reclamar-civ-0749` |
| CIV-0750 | Demanda de juicio ordinario por incumplimiento de un contrato de obra a precio alzado | `demanda-juicio-ordinario-incumplimiento-contrato-obra-civ-0750` |
| CIV-0751 | Demanda de juicio ordinario para exigir el cumplimiento de un contrato de suministro mercantil | `demanda-juicio-ordinario-exigir-cumplimiento-contrato-civ-0751` |
| CIV-0752 | Demanda de juicio ordinario contra el banco por comisiones por descubiertos y efectos devueltos | `demanda-juicio-ordinario-contra-banco-comisiones-civ-0752` |
| CIV-0753 | Demanda del cooperativista para que la cooperativa de viviendas le devuelva lo aportado | `demanda-cooperativista-cooperativa-viviendas-le-civ-0753` |
| CIV-0756 | Demanda de juicio ordinario contra el banco por la ejecución de un aval a primer requerimiento | `demanda-juicio-ordinario-contra-banco-ejecucion-aval-civ-0756` |
| CIV-0757 | Demanda del subcontratista contra el dueño de la obra por la acción directa del artículo 1597 CC | `demanda-subcontratista-contra-dueno-obra-accion-civ-0757` |
| CIV-0764 | Demanda de juicio ordinario de repetición contra el obligado cuando pagó un tercero | `demanda-juicio-ordinario-repeticion-contra-obligado-civ-0764` |
| CIV-0765 | Demanda de juicio ordinario por cobro de lo indebido | `demanda-juicio-ordinario-cobro-lo-indebido-civ-0765` |
| CIV-0767 | Demanda para resolver una compraventa mercantil por incumplimiento del vendedor y reclamar cantidad | `demanda-resolver-compraventa-mercantil-incumplimiento-civ-0767` |
| CIV-0772 | Demanda de juicio ordinario para anular una compraventa por extralimitación del mandatario | `demanda-juicio-ordinario-anular-compraventa-civ-0772` |
| CIV-0773 | Demanda de juicio ordinario para exigir el cumplimiento de una compraventa de bien mueble | `demanda-juicio-ordinario-exigir-cumplimiento-civ-0773` |
| CIV-0774 | Demanda por incumplimiento de la entrega en una venta como cuerpo cierto con defecto de cabida | `demanda-incumplimiento-entrega-venta-como-cuerpo-civ-0774` |
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
| CIV-0805 | Demanda de juicio verbal de reclamación de cantidad por compraventa, obra, contrato mixto o atípico | `demanda-juicio-verbal-reclamacion-cantidad-compraventa-civ-0805` |
| CIV-0806 | Demanda breve de juicio verbal de reclamación de cantidad | `demanda-breve-juicio-verbal-reclamacion-cantidad-civ-0806` |
| CIV-0807 | Demanda sobre venta de bienes muebles a plazos con exhibición de los bienes y depositario | `demanda-sobre-venta-bienes-muebles-plazos-exhibicion-civ-0807` |
| CIV-0808 | Demanda de juicio ordinario de reclamación de cantidad contra una sociedad y su administrador | `demanda-juicio-ordinario-reclamacion-cantidad-contra-civ-0808` |
| CIV-0809 | Demanda de juicio ordinario por impago de géneros suministrados, con intereses desde la compraventa | `demanda-juicio-ordinario-impago-generos-suministrados-civ-0809` |
| CIV-0812 | Demanda de juicio ordinario de impugnación de condiciones generales de la contratación (Ley 7 1998) | `demanda-juicio-ordinario-impugnacion-condiciones-civ-0812` |
| CIV-0815 | Demanda de juicio ordinario por incumplimiento de contrato de compraventa | `demanda-juicio-ordinario-incumplimiento-contrato-civ-0815` |
| CIV-0816 | Demanda de juicio ordinario de reclamación de cantidad por ejecución de obra civil | `demanda-juicio-ordinario-reclamacion-cantidad-civ-0816` |
| CIV-0817 | Demanda de juicio ordinario de reclamación de cantidad y enriquecimiento injusto en contrato de obra | `demanda-juicio-ordinario-reclamacion-cantidad-civ-0817` |
| CIV-0818 | Demanda ordinaria de rescisión por lesión según el Código civil catalán, con dictamen pericial | `demanda-ordinaria-rescision-lesion-segun-codigo-civil-civ-0818` |
| CIV-0819 | Demanda de juicio verbal de reclamación de cantidad por contrato de obra entre 2.000 y 15.000 euros | `demanda-juicio-verbal-reclamacion-cantidad-contrato-civ-0819` |
| CIV-0821 | Demanda de juicio ordinario de nulidad de compraventa por simulación absoluta | `demanda-juicio-ordinario-nulidad-compraventa-civ-0821` |
| CIV-0824 | Demanda de juicio ordinario de resolución de compraventa de plaza de garaje por incumplimiento | `demanda-juicio-ordinario-resolucion-compraventa-plaza-civ-0824` |
| CIV-0846 | Demanda de juicio verbal por reclamación de cantidad por contrato de obra de hasta 2.000 euros | `demanda-juicio-verbal-reclamacion-cantidad-contrato-civ-0846` |
| CIV-0849 | Demanda de juicio ordinario por las arras dobladas ante el desistimiento en la venta de un inmueble | `demanda-juicio-ordinario-arras-dobladas-ante-civ-0849` |
| CIV-0852 | Demanda por deuda reconocida en documento privado con causa fiduciaria o simulación relativa | `demanda-deuda-reconocida-documento-privado-causa-civ-0852` |
| CIV-2546 | Demanda de juicio verbal para reclamar una cantidad inferior a 150 euros | `demanda-juicio-verbal-reclamar-cantidad-inferior-150-civ-2546` |
| CIV-2559 | Demanda de juicio ordinario para reclamar comisiones debidas por un contrato de agencia | `demanda-juicio-ordinario-reclamar-comisiones-debidas-civ-2559` |
| CIV-2560 | Demanda del contratista contra la comunidad de propietarios para cobrar el saldo de la obra | `demanda-contratista-contra-comunidad-propietarios-civ-2560` |
| CIV-2592 | Demanda de juicio verbal para reclamar los alimentos debidos por un contrato vitalicio | `demanda-juicio-verbal-reclamar-alimentos-debidos-civ-2592` |
| CIV-2623 | Demanda del lesionado en un medio de transporte que no es vehículo a motor contra el transportista | `demanda-lesionado-medio-transporte-no-es-vehiculo-civ-2623` |
| CIV-2658 | Demanda ordinaria del usuario contra la concesionaria de la autopista, supuesto general | `demanda-ordinaria-usuario-contra-concesionaria-civ-2658` |

### Contestaciones, oposiciones y alegaciones (5)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0769 | Contestación a la demanda de rescisión por lesión (Derecho civil catalán) | `contestacion-demanda-rescision-lesion-derecho-civil-civ-0769` |
| CIV-0804 | Contestación del demandado a la demanda por incumplimiento de venta de bienes muebles a plazos | `contestacion-demandado-demanda-incumplimiento-venta-civ-0804` |
| CIV-0855 | Contestación a la demanda alegando nulidad de la compraventa de vivienda por dolo | `contestacion-demanda-alegando-nulidad-compraventa-civ-0855` |
| CIV-2555 | Contestación del administrador de la sociedad vendedora a la demanda de rebaja del precio | `contestacion-administrador-sociedad-vendedora-demanda-civ-2555` |
| CIV-2556 | Contestación a la demanda de rebaja de precio por falta de cabida, con reconvención sobre las arras | `contestacion-demanda-rebaja-precio-falta-cabida-civ-2556` |

### Contratos, pactos y cláusulas (104)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0685 | Contrato de ejecución de obra entre comitente y contratista | `contrato-ejecucion-obra-entre-comitente-contratista-civ-0685` |
| CIV-0686 | Contrato de compraventa de vivienda en construcción según el Derecho civil catalán | `contrato-compraventa-vivienda-construccion-segun-civ-0686` |
| CIV-0687 | Contrato de promesa bilateral de compraventa | `contrato-promesa-bilateral-compraventa-civ-0687` |
| CIV-0694 | Contrato de compraventa de vivienda, local o plaza de garaje | `contrato-compraventa-vivienda-local-plaza-garaje-civ-0694` |
| CIV-0696 | Contrato de alquiler de vehículo sin conductor | `contrato-alquiler-vehiculo-sin-conductor-civ-0696` |
| CIV-0704 | Contrato de cesión de bienes a los acreedores en pago de deudas | `contrato-cesion-bienes-acreedores-pago-deudas-civ-0704` |
| CIV-0705 | Contrato de opción de compra con o sin precio | `contrato-opcion-compra-sin-precio-civ-0705` |
| CIV-0706 | Contrato de ejecución de obra con anexos de planos y valoración | `contrato-ejecucion-obra-anexos-planos-valoracion-civ-0706` |
| CIV-0709 | Contrato de ejecución de obra con aportación de materiales por el contratista | `contrato-ejecucion-obra-aportacion-materiales-civ-0709` |
| CIV-0727 | Contrato de arrendamiento de bienes muebles según modelo aprobado por la DGRN el 13 de marzo de 2000 | `contrato-arrendamiento-bienes-muebles-segun-modelo-civ-0727` |
| CIV-0728 | Contrato de transacción para poner fin a un pleito ya iniciado | `contrato-transaccion-poner-fin-pleito-ya-iniciado-civ-0728` |
| CIV-0729 | Contrato de alquiler de equipos informáticos | `contrato-alquiler-equipos-informaticos-civ-0729` |
| CIV-0730 | Contrato de venta de un local comercial | `contrato-venta-local-comercial-civ-0730` |
| CIV-0731 | Contrato de obra para la demolición de una edificación | `contrato-obra-demolicion-edificacion-civ-0731` |
| CIV-0739 | Contrato de venta a plazos de bienes muebles conforme a la Ley de Venta a Plazos | `contrato-venta-plazos-bienes-muebles-conforme-ley-civ-0739` |
| CIV-0740 | Contrato de venta a plazos de bienes muebles conforme a la Ley de Consumidores y Usuarios de 2007 | `contrato-venta-plazos-bienes-muebles-conforme-ley-civ-0740` |
| CIV-0744 | Contrato de construcción de un edificio de viviendas con mano de obra y materiales del constructor | `contrato-construccion-edificio-viviendas-mano-obra-civ-0744` |
| CIV-0758 | Contrato de construcción de obra llave en mano | `contrato-construccion-obra-llave-mano-civ-0758` |
| CIV-0762 | Acuerdo de quita de una deuda entre acreedor y deudor | `acuerdo-quita-deuda-entre-acreedor-deudor-civ-0762` |
| CIV-0777 | Contrato de compraventa de vivienda destinada a domicilio familiar | `contrato-compraventa-vivienda-destinada-domicilio-civ-0777` |
| CIV-0791 | Contrato por el que se ceden créditos | `contrato-ceden-creditos-civ-0791` |
| CIV-0793 | Contrato de permuta de una vivienda por obra a edificar | `contrato-permuta-vivienda-obra-edificar-civ-0793` |
| CIV-0794 | Contrato de cesión de posición contractual | `contrato-cesion-posicion-contractual-civ-0794` |
| CIV-0795 | Contrato por el que se ceden derechos | `contrato-ceden-derechos-civ-0795` |
| CIV-0797 | Contrato de ejecución de obra | `contrato-ejecucion-obra-civ-0797` |
| CIV-0798 | Contrato de compraventa de un local en construcción | `contrato-compraventa-local-construccion-civ-0798` |
| CIV-0799 | Contrato de venta de una vivienda urbana | `contrato-venta-vivienda-urbana-civ-0799` |
| CIV-0800 | Contrato de arras penitenciales con facultad de desistir | `contrato-arras-penitenciales-facultad-desistir-civ-0800` |
| CIV-0801 | Contrato de arras confirmatorias sobre una finca | `contrato-arras-confirmatorias-sobre-finca-civ-0801` |
| CIV-0802 | Contrato de opción de compra | `contrato-opcion-compra-civ-0802` |
| CIV-0803 | Contrato de compraventa de un bien inmueble | `contrato-compraventa-bien-inmueble-civ-0803` |
| CIV-0813 | Compraventa de vehículo (contrato) | `compraventa-vehiculo-contrato-civ-0813` |
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
| CIV-2547 | Contrato para devolver un pago duplicado hecho por error a quien no era el acreedor | `contrato-devolver-pago-duplicado-hecho-error-quien-no-civ-2547` |
| CIV-2548 | Contrato en que se reconoce un cobro indebido sin obligación de restituir | `contrato-reconoce-cobro-indebido-sin-obligacion-civ-2548` |
| CIV-2550 | Contrato de mutuo o préstamo de cosas fungibles | `contrato-mutuo-prestamo-cosas-fungibles-civ-2550` |
| CIV-2551 | Contrato de préstamo de dinero sin intereses | `contrato-prestamo-dinero-sin-intereses-civ-2551` |
| CIV-2558 | Contrato de arras penitenciales para la compraventa de una finca | `contrato-arras-penitenciales-compraventa-finca-civ-2558` |
| CIV-2563 | Contrato de permuta de inmuebles con compensación en dinero de la diferencia de valor | `contrato-permuta-inmuebles-compensacion-dinero-civ-2563` |
| CIV-2564 | Contrato de obra para construir un edificio entre la propiedad y el adjudicatario | `contrato-obra-construir-edificio-entre-propiedad-civ-2564` |
| CIV-2565 | Contrato de depósito irregular de una cantidad de dinero | `contrato-deposito-irregular-cantidad-dinero-civ-2565` |
| CIV-2566 | Contrato de estacionamiento de vehículos en un aparcamiento | `contrato-estacionamiento-vehiculos-aparcamiento-civ-2566` |
| CIV-2567 | Contrato de secuestro convencional de bienes muebles en litigio | `contrato-secuestro-convencional-bienes-muebles-litigio-civ-2567` |
| CIV-2570 | Contrato de renta vitalicia a cambio de la cesión de una finca | `contrato-renta-vitalicia-cambio-cesion-finca-civ-2570` |
| CIV-2571 | Contrato de hospedaje entre el hostelero y el huésped | `contrato-hospedaje-entre-hostelero-huesped-civ-2571` |
| CIV-2572 | Contrato de depósito voluntario de cosas muebles | `contrato-deposito-voluntario-cosas-muebles-civ-2572` |
| CIV-2574 | Contrato de permuta de un solar a cambio de edificación futura | `contrato-permuta-solar-cambio-edificacion-futura-civ-2574` |
| CIV-2575 | Contrato simplificado de venta de un bien ganancial | `contrato-simplificado-venta-bien-ganancial-civ-2575` |
| CIV-2576 | Contrato de compraventa con pacto de retro | `contrato-compraventa-pacto-retro-civ-2576` |
| CIV-2577 | Contrato privado de permuta de bienes | `contrato-privado-permuta-bienes-civ-2577` |
| CIV-2579 | Contrato de promesa de compraventa con entrega de arras | `contrato-promesa-compraventa-entrega-arras-civ-2579` |
| CIV-2580 | Contrato de venta a plazos de un inmueble con condición resolutoria | `contrato-venta-plazos-inmueble-condicion-resolutoria-civ-2580` |
| CIV-2581 | Contrato de opción de compra con entrega de arras | `contrato-opcion-compra-entrega-arras-civ-2581` |
| CIV-2582 | Contrato de compraventa de un vehículo de segunda mano | `contrato-compraventa-vehiculo-segunda-mano-civ-2582` |
| CIV-2583 | Contrato de compraventa a prueba o en calidad de ensayo | `contrato-compraventa-prueba-calidad-ensayo-civ-2583` |
| CIV-2586 | Acuerdo de rescisión de la compraventa a instancia del vendedor, que pierde las arras penitenciales | `acuerdo-rescision-compraventa-instancia-vendedor-civ-2586` |
| CIV-2587 | Contrato de compraventa de un coche nuevo con precio aplazado | `contrato-compraventa-coche-nuevo-precio-aplazado-civ-2587` |
| CIV-2588 | Acuerdo de rescisión de la compraventa a instancia del comprador, que pierde las arras penitenciales | `acuerdo-rescision-compraventa-instancia-comprador-civ-2588` |
| CIV-2590 | Contrato de compraventa de una vivienda en construcción | `contrato-compraventa-vivienda-construccion-civ-2590` |
| CIV-2591 | Contrato de compraventa de una vivienda urbana | `contrato-compraventa-vivienda-urbana-civ-2591` |
| CIV-2595 | Contrato vitalicio de cesión de un negocio a cambio de una renta vitalicia | `contrato-vitalicio-cesion-negocio-cambio-renta-civ-2595` |
| CIV-2596 | Contrato privado por el que el deudor cede un crédito a su acreedor para saldar la deuda | `contrato-privado-deudor-cede-credito-acreedor-saldar-civ-2596` |
| CIV-2597 | Contrato de renta vitalicia a cambio de una finca con hipoteca que garantiza el pago | `contrato-renta-vitalicia-cambio-finca-hipoteca-civ-2597` |
| CIV-2598 | Contrato de renta vitalicia a cambio de una finca con cláusula resolutoria y cláusula penal | `contrato-renta-vitalicia-cambio-finca-clausula-civ-2598` |
| CIV-2599 | Compraventa de local comercial segregado en propiedad horizontal con pago aplazado y cláusula penal | `compraventa-local-comercial-segregado-propiedad-civ-2599` |
| CIV-2600 | Contrato de compraventa de vivienda protegida con calificación provisional | `contrato-compraventa-vivienda-protegida-calificacion-civ-2600` |
| CIV-2604 | Contrato privado de reconocimiento de deuda con compensación y plazos de pago | `contrato-privado-reconocimiento-deuda-compensacion-civ-2604` |
| CIV-2610 | Contrato para comprar una vivienda de protección oficial con financiación cualificada | `contrato-comprar-vivienda-proteccion-oficial-civ-2610` |
| CIV-2612 | Contrato privado de compraventa de vivienda con pago aplazado financiado mediante crédito al consumo | `contrato-privado-compraventa-vivienda-pago-aplazado-civ-2612` |
| CIV-2614 | Contrato de ejecución de obra con aportación de materiales, por ajuste o a precio alzado | `contrato-ejecucion-obra-aportacion-materiales-ajuste-civ-2614` |
| CIV-2644 | Contrato de compraventa con pacto de retroventa en el que vende un matrimonio | `contrato-compraventa-pacto-retroventa-vende-matrimonio-civ-2644` |
| CIV-2645 | Contrato de compraventa de un local comercial ya construido con pacto de retro | `contrato-compraventa-local-comercial-ya-construido-civ-2645` |
| CIV-2647 | Contrato de compraventa de una plaza de garaje que no es anejo de la vivienda | `contrato-compraventa-plaza-garaje-no-es-anejo-vivienda-civ-2647` |
| CIV-2648 | Contrato de compraventa con pacto de retroventa de un bien privativo del vendedor | `contrato-compraventa-pacto-retroventa-bien-privativo-civ-2648` |
| CIV-2650 | Contrato privado de opción de compra unilateral a favor de una de las partes | `contrato-privado-opcion-compra-unilateral-favor-partes-civ-2650` |
| CIV-2652 | Contrato privado por el que el dueño de una finca concede una opción de compra | `contrato-privado-dueno-finca-concede-opcion-compra-civ-2652` |
| CIV-2653 | Contrato de compraventa de una cuota indivisa de un solar edificable | `contrato-compraventa-cuota-indivisa-solar-edificable-civ-2653` |
| CIV-2654 | Contrato privado de compraventa de una finca rústica | `contrato-privado-compraventa-finca-rustica-civ-2654` |
| CIV-2655 | Contrato privado por el que el titular cede todos sus derechos sobre un bien | `contrato-privado-titular-cede-todos-derechos-sobre-bien-civ-2655` |
| CIV-2656 | Contrato privado por el que un tercero asume la deuda de otro | `contrato-privado-tercero-asume-deuda-otro-civ-2656` |
| CIV-2666 | Contrato privado de cesión de un contrato entre empresas | `contrato-privado-cesion-contrato-entre-empresas-civ-2666` |
| CIV-2667 | Contrato de compraventa de solar urbano entre sociedades con arras penitenciales y pagos diversos | `contrato-compraventa-solar-urbano-entre-sociedades-civ-2667` |
| CIV-2668 | Acuerdo que reconoce la deuda y liquida la relación comercial con devolución de mercancía | `acuerdo-reconoce-deuda-liquida-relacion-comercial-civ-2668` |
| CIV-2669 | Contrato de compraventa de un trastero que no es anejo de la vivienda | `contrato-compraventa-trastero-no-es-anejo-vivienda-civ-2669` |
| CIV-2670 | Contrato de renta vitalicia a título gratuito | `contrato-renta-vitalicia-titulo-gratuito-civ-2670` |
| CIV-2675 | Contrato de venta de vivienda heredada con nuda propiedad y usufructo en distintos titulares | `contrato-venta-vivienda-heredada-nuda-propiedad-civ-2675` |
| CIV-2677 | Contrato privado de compraventa de vivienda arrendada con pago aplazado y condición resolutoria | `contrato-privado-compraventa-vivienda-arrendada-pago-civ-2677` |

### Estatutos, actas, certificaciones y escrituras (23)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0796 | Escritura de poder para realizar actos de disposición | `escritura-poder-realizar-actos-disposicion-civ-0796` |
| CIV-2578 | Escritura de venta de un bien ganancial con autorización judicial | `escritura-venta-bien-ganancial-autorizacion-judicial-civ-2578` |
| CIV-2584 | Escritura pública de compraventa de bienes muebles | `escritura-publica-compraventa-bienes-muebles-civ-2584` |
| CIV-2589 | Escritura en que el vendedor ejercita el retracto convencional o derecho de retro | `escritura-vendedor-ejercita-retracto-convencional-civ-2589` |
| CIV-2602 | Escritura de dación en pago de un bien para extinguir una deuda | `escritura-dacion-pago-bien-extinguir-deuda-civ-2602` |
| CIV-2603 | Poder general sin límites para administrar, disponer y realizar actos de comercio | `poder-general-sin-limites-administrar-disponer-civ-2603` |
| CIV-2605 | Escritura de compraventa de VPO por un matrimonio en gananciales con subrogación en la hipoteca | `escritura-compraventa-vpo-matrimonio-gananciales-civ-2605` |
| CIV-2606 | Escritura de compraventa otorgada en cumplimiento de una sentencia | `escritura-compraventa-otorgada-cumplimiento-sentencia-civ-2606` |
| CIV-2611 | Escritura por la que el deudor cede a su acreedor un crédito que está reclamando judicialmente | `escritura-deudor-cede-acreedor-credito-esta-reclamando-civ-2611` |
| CIV-2646 | Escritura pública de compraventa de local comercial con pacto de retroventa | `escritura-publica-compraventa-local-comercial-pacto-civ-2646` |
| CIV-2649 | Escritura pública por la que se concede una opción de compra sobre una finca | `escritura-publica-concede-opcion-compra-sobre-finca-civ-2649` |
| CIV-2651 | Escritura de compraventa que ejecuta una opción de compra anterior | `escritura-compraventa-ejecuta-opcion-compra-anterior-civ-2651` |
| CIV-2657 | Escritura de carta de pago del precio aplazado y cancelación de la condición resolutoria | `escritura-carta-pago-precio-aplazado-cancelacion-civ-2657` |
| CIV-2662 | Acta notarial en la que el lesionado declara estar indemnizado y renuncia a las acciones | `acta-notarial-lesionado-declara-estar-indemnizado-civ-2662` |
| CIV-2664 | Escritura pública de opción de compra unilateral a favor de una de las partes | `escritura-publica-opcion-compra-unilateral-favor-partes-civ-2664` |
| CIV-2674 | Escritura de permuta de dos bienes de igual valor | `escritura-permuta-dos-bienes-igual-valor-civ-2674` |
| CIV-2676 | Poder de los padres de un novillero menor para su representación y dirección artística | `poder-padres-novillero-menor-representacion-direccion-civ-2676` |
| CIV-2678 | Escritura que revoca un poder otorgado anteriormente | `escritura-revoca-poder-otorgado-anteriormente-civ-2678` |
| CIV-2679 | Poder para administrar y disponer de una vivienda | `poder-administrar-disponer-vivienda-civ-2679` |
| CIV-2680 | Escritura de compraventa con pago del precio en el momento de firmar | `escritura-compraventa-pago-precio-momento-firmar-civ-2680` |
| CIV-2684 | Escritura de permuta de bienes de valor desigual | `escritura-permuta-bienes-valor-desigual-civ-2684` |
| CIV-2685 | Escritura de compraventa en la que el vendedor declara haber cobrado ya el precio | `escritura-compraventa-vendedor-declara-haber-cobrado-civ-2685` |
| CIV-2686 | Escritura de compraventa de vivienda arrendada con pago aplazado, intereses y condición resolutoria | `escritura-compraventa-vivienda-arrendada-pago-aplazado-civ-2686` |

### Comunicaciones, requerimientos y cartas (23)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0691 | Reclamación extrajudicial previa de los gastos de formalización de una hipoteca | `reclamacion-extrajudicial-previa-gastos-formalizacion-civ-0691` |
| CIV-0700 | Requerimiento al promotor para resolver la compraventa de vivienda sobre plano y devolver lo pagado | `requerimiento-promotor-resolver-compraventa-vivienda-civ-0700` |
| CIV-0701 | Requerimiento al vendedor para resolver la compraventa de una plaza de garaje por incumplimiento | `requerimiento-vendedor-resolver-compraventa-plaza-civ-0701` |
| CIV-0702 | Requerimiento para resolver la compraventa de inmueble por retraso y devolver lo pagado | `requerimiento-resolver-compraventa-inmueble-retraso-civ-0702` |
| CIV-0707 | Comunicación al vendedor de falta de conformidad del producto de uso especial y reparación | `comunicacion-vendedor-falta-conformidad-producto-uso-civ-0707` |
| CIV-0708 | Comunicación al vendedor de la resolución del contrato por reparación o sustitución insatisfactoria | `comunicacion-vendedor-resolucion-contrato-reparacion-civ-0708` |
| CIV-0711 | Comunicación al vendedor de falta de conformidad del producto y petición de reparación o cambio | `comunicacion-vendedor-falta-conformidad-producto-civ-0711` |
| CIV-0712 | Comunicación del consumidor que acepta la modificación del contrato de viaje combinado | `comunicacion-consumidor-acepta-modificacion-contrato-civ-0712` |
| CIV-0713 | Comunicación del consumidor que resuelve el contrato de viaje combinado | `comunicacion-consumidor-resuelve-contrato-viaje-civ-0713` |
| CIV-0714 | Reclamación a la aerolínea por denegación de embarque por overbooking | `reclamacion-aerolinea-denegacion-embarque-overbooking-civ-0714` |
| CIV-0716 | Comunicación al organizador o minorista de incumplimientos en la ejecución del viaje combinado | `comunicacion-organizador-minorista-incumplimientos-civ-0716` |
| CIV-0717 | Reclamación a la aerolínea por cambio de clase del pasajero en el vuelo contratado | `reclamacion-aerolinea-cambio-clase-pasajero-vuelo-civ-0717` |
| CIV-0718 | Reclamación a la aerolínea por retraso del vuelo contratado | `reclamacion-aerolinea-retraso-vuelo-contratado-civ-0718` |
| CIV-0720 | Comunicación al minorista u organizador de la cesión de la reserva de un viaje combinado | `comunicacion-minorista-u-organizador-cesion-reserva-civ-0720` |
| CIV-0723 | Reclamación extrajudicial a la operadora por defectos en el servicio de telefonía | `reclamacion-extrajudicial-operadora-defectos-servicio-civ-0723` |
| CIV-0726 | Reclamación a la aerolínea por cancelación del vuelo contratado | `reclamacion-aerolinea-cancelacion-vuelo-contratado-civ-0726` |
| CIV-0748 | Carta del comprador resolviendo la compraventa de un vehículo y reclamando cantidad | `carta-comprador-resolviendo-compraventa-vehiculo-civ-0748` |
| CIV-0760 | Carta comunicando la resolución del contrato por retraso en la construcción de las viviendas | `carta-comunicando-resolucion-contrato-retraso-civ-0760` |
| CIV-0761 | Requerimiento al comprador para otorgar la escritura de la vivienda | `requerimiento-comprador-otorgar-escritura-vivienda-civ-0761` |
| CIV-0792 | Carta de pago en que el acreedor confiesa haber cobrado la deuda | `carta-pago-acreedor-confiesa-haber-cobrado-deuda-civ-0792` |
| CIV-2553 | Requerimiento al concedente para que cumpla la opción de compra de un inmueble | `requerimiento-concedente-cumpla-opcion-compra-inmueble-civ-2553` |
| CIV-2554 | Requerimiento al concedente por incumplir la opción de compra de un inmueble inscrito | `requerimiento-concedente-incumplir-opcion-compra-civ-2554` |
| CIV-2585 | Carta al comprador que declara resuelta la venta por impago de los plazos convenidos | `carta-comprador-declara-resuelta-venta-impago-plazos-civ-2585` |

### Escritos de trámite y otros (13)

| Código | Formulario | Skill |
|---|---|---|
| CIV-0719 | Documento de desistimiento del comprador en un contrato de compraventa | `documento-desistimiento-comprador-contrato-compraventa-civ-0719` |
| CIV-0722 | Hoja de reclamación en talleres de reparación de vehículos | `hoja-reclamacion-talleres-reparacion-vehiculos-civ-0722` |
| CIV-0725 | Ejecución de obra o instalación (contrato) | `ejecucion-obra-instalacion-contrato-civ-0725` |
| CIV-0754 | Impugnación de la jura de cuentas del abogado por partidas indebidas | `impugnacion-jura-cuentas-abogado-partidas-indebidas-civ-0754` |
| CIV-0759 | Documento de resolución por mutuo acuerdo de una compraventa de inmueble | `documento-resolucion-mutuo-acuerdo-compraventa-inmueble-civ-0759` |
| CIV-0776 | Autorización notarial para el uso de un vehículo | `autorizacion-notarial-uso-vehiculo-civ-0776` |
| CIV-0814 | Documento de reconocimiento de deuda con aplazamiento de pago | `documento-reconocimiento-deuda-aplazamiento-pago-civ-0814` |
| CIV-0854 | Escrito del demandante frente a la alegación de un crédito compensable por el demandado | `escrito-demandante-frente-alegacion-credito-civ-0854` |
| CIV-2568 | Documento sencillo de dación en pago de una deuda | `documento-sencillo-dacion-pago-deuda-civ-2568` |
| CIV-2569 | Documento privado de reconocimiento de deuda | `documento-privado-reconocimiento-deuda-civ-2569` |
| CIV-2573 | Documento de participación en un número de lotería entre depositario y portador | `documento-participacion-numero-loteria-entre-civ-2573` |
| CIV-2608 | Dación en pago en documento privado sometida a una condición suspensiva | `dacion-pago-documento-privado-sometida-condicion-civ-2608` |
| CIV-2609 | Elevación a público de una compraventa privada con un otorgante fallecido, interviniendo su viuda | `elevacion-publico-compraventa-privada-otorgante-civ-2609` |
