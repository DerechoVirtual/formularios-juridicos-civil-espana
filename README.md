# Formularios jurídicos de España para Claude · Civil

23 plugins de formularios de Civil, uno por materia. Cada formulario es una skill que Claude rellena paso a paso con los datos del caso y entrega en Word tal cual es el formulario (Times New Roman 11, interlineado 1,15 y texto justificado): 3021 skills en total, contando la skill `indice` de cada plugin, que sirve para encontrar el formulario adecuado.

Todas las skills trabajan con **Jurisprudenciator** (https://jurisprudenciator.lexiaipro.org): antes de redactar comprueban que el conector responde y verifican en fuentes oficiales las normas que cita el formulario. Sin Jurisprudenciator conectado, las skills no redactan. Normativa revisada el 25-11-2026.

Las demás jurisdicciones están en repositorios propios: [Mercantil](https://github.com/DerechoVirtual/formularios-juridicos-mercantil-espana), [Seguridad Social](https://github.com/DerechoVirtual/formularios-juridicos-seguridad-social-espana), [Administrativo y Tributario](https://github.com/DerechoVirtual/formularios-juridicos-administrativo-tributario-espana), [Laboral](https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana), [Penal](https://github.com/DerechoVirtual/formularios-juridicos-penal-espana).

## Instalación

En Claude Code:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-civil-espana
/plugin install formularios-gananciales-y-parejas-de-hecho@formularios-juridicos-civil-espana
```

Cada plugin ocupa contexto en la conversación, así que conviene instalar solo los de las materias con las que se trabaja.

En Claude (web, escritorio y Cowork) se puede añadir este repositorio desde **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-civil-espana`, o subir cada plugin como ZIP. Los ZIP están en la página de [versiones](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest).

## Plugins

| Plugin | Contenido | Skills | ZIP |
|---|---|---:|---|
| `formularios-gananciales-y-parejas-de-hecho` | Gananciales, regímenes económicos y parejas de hecho | 89 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-gananciales-y-parejas-de-hecho.zip) |
| `formularios-hijos-custodia-y-alimentos` | Hijos: custodia, visitas, alimentos, filiación y adopción | 160 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-hijos-custodia-y-alimentos.zip) |
| `formularios-familia-y-divorcio` | Familia: separación, divorcio y medidas | 237 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-familia-y-divorcio.zip) |
| `formularios-discapacidad-y-medidas-de-apoyo` | Discapacidad y medidas de apoyo (Ley 8/2021) | 47 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-discapacidad-y-medidas-de-apoyo.zip) |
| `formularios-herencias-y-donaciones` | Herencias, testamentos y donaciones | 164 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-herencias-y-donaciones.zip) |
| `formularios-alquileres-y-desahucios` | Alquileres y desahucios | 220 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-alquileres-y-desahucios.zip) |
| `formularios-comunidades-de-propietarios` | Comunidades de propietarios | 60 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-comunidades-de-propietarios.zip) |
| `formularios-propiedad-y-derechos-reales` | Propiedad, posesión, servidumbres e hipotecas | 44 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-propiedad-y-derechos-reales.zip) |
| `formularios-accidentes-y-responsabilidad-civil` | Accidentes, seguros y responsabilidad civil | 95 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-accidentes-y-responsabilidad-civil.zip) |
| `formularios-contratos-consumo-y-danos` | Contratos civiles y consumo | 221 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-contratos-consumo-y-danos.zip) |
| `formularios-prueba-civil` | Prueba en el proceso civil | 73 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-prueba-civil.zip) |
| `formularios-escritos-de-tramite-civiles` | Escritos de trámite en el proceso civil | 111 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-escritos-de-tramite-civiles.zip) |
| `formularios-proceso-civil` | Proceso civil: demandas, contestaciones, audiencia previa y vista | 187 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-proceso-civil.zip) |
| `formularios-reclamar-deudas-monitorio` | Cobrar deudas: monitorio y cambiario | 65 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-reclamar-deudas-monitorio.zip) |
| `formularios-medidas-cautelares-civiles` | Medidas cautelares y diligencias preliminares | 85 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-medidas-cautelares-civiles.zip) |
| `formularios-recursos-civiles` | Recursos civiles: reposición, apelación, casación y queja | 146 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-recursos-civiles.zip) |
| `formularios-subastas-y-ejecucion-hipotecaria` | Subastas, ejecución hipotecaria y lanzamientos | 74 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-subastas-y-ejecucion-hipotecaria.zip) |
| `formularios-oposicion-a-la-ejecucion` | Oposición a la ejecución, tercerías y recursos en la ejecución | 109 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-oposicion-a-la-ejecucion.zip) |
| `formularios-ejecucion-y-embargos` | Ejecución de sentencias y embargos | 194 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-ejecucion-y-embargos.zip) |
| `formularios-mediacion-arbitraje-y-voluntaria` | Mediación, MASC, arbitraje y jurisdicción voluntaria | 102 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-mediacion-arbitraje-y-voluntaria.zip) |
| `formularios-diligencias-de-ordenacion-civiles` | Diligencias de ordenación y de constancia del proceso civil | 147 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-diligencias-de-ordenacion-civiles.zip) |
| `formularios-decretos-y-providencias-civiles` | Decretos y providencias del proceso civil | 154 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-decretos-y-providencias-civiles.zip) |
| `formularios-resoluciones-judiciales-civiles` | Resoluciones judiciales civiles: autos, sentencias y actas | 237 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana/releases/latest/download/formularios-resoluciones-judiciales-civiles.zip) |

## Estructura

```
.claude-plugin/marketplace.json  catálogo del marketplace
plugins/<plugin>/                .claude-plugin/plugin.json, .mcp.json, skills/<skill>/SKILL.md y assets/formulario.md, README.md, PRIVACY.md, LICENSE
```

## Aviso

Los documentos que se generan son borradores que debe revisar un abogado; no constituyen asesoramiento jurídico. Las skills no guardan datos del cliente y las consultas a Jurisprudenciator describen el problema jurídico, no los datos personales.

Soporte: https://jurisprudenciator.lexiaipro.org/incidencias · Licencia: ver [LICENSE](LICENSE).
