



<img src="https://ciudadesabiertas.es/assets/img/cabiertas/logo.svg" alt="LogoCiudadesAbiertas" width="200"/> 

# DESARROLLO API REST DE DATOS REUTILIZABLE. MODELO DE TABLAS: EMPLEO

&nbsp;

## **ÍNDICE**   
1. [AUTORES](#id1)
2. [LINKS](#id2)
3. [TABLAS](#id4)  
    - [EMPLEO_OFERTA_PUBLICA](#id5)  
    - [EMPLEO_CONVOCATORIA_PUBLICA](#id6)  
    - [EMPLEO_BOLETIN_OFICIAL](#id7)  
    - [EMPLEO_PLAZA_TURNO](#id8) 
    - [TABLAS DE RELACIÓN NECESARIAS PARA MANTENER LA ESTRUCTURA DEL VOCABULARIO](#id9)  
       - [EMPLEO_REL_BOLETIN_CONVOCA](#id10) 
       - [EMPLEO_REL_OFERTA_CONVOCA](#id11) 
4. [TAXONOMÍAS SKOS](#id12)
      - [GRUPO-PROFESIONAL](#id13)
      - [EMPLEADO-PUBLICO](#id14)
      - [CUERPO](#id15)
      - [MODALIDAD](#id16)
      - [TURNO](#id17)

 



&nbsp;

## AUTORES <a name="id1"></a>
- Adolfo Antón Bravo
- Carlos Martínez de la Casa García
- Edna Ruckhaus
- Leticia Rubalcaba
- Oscar Corcho

&nbsp;

## LINKS <a name="id2"></a>


Este documento contiene la información detallada del modelo de datos asociado al vocabulario de los convenios. A continuación, se detallan los enlaces de interés asociados a este vocabulario:

- *[Documentación](http://vocab.ciudadesabiertas.es/def/sector-publico/empleo)*
- *[Repositorio](https://github.com/CiudadesAbiertas/vocab-sector-publico-empleo)*
- *[Issues](https://github.com/CiudadesAbiertas/vocab-sector-publico-empleo/issues)*

&nbsp;

## TABLAS <a name="id4"></a>  


[comment]: <!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!> 
&nbsp;
### EMPLEO_OFERTA_PUBLICA <a name="id5"></a>
&nbsp;

|     Campo                 |     Tipo               |     Ejemplo                                                                 |     Descripción                                                                                                                                                                                                                                                                                                                                           |     URL                                                                                 |
|---------------------------|------------------------|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
|     ikey                  |     VARCHAR(50)        |     1                                                                       |     Identificador de la   Tabla (PK).                                                                                                                                                                                                                                                                                                                     |                                                                                         |
|     id                    |     VARCHAR(50)        |     OFEM0001                                                                |     Identificación   de la oferta pública del empleo.                                                                                                                                                                                                                                                                                                     |     http://purl.org/dc/terms/identifier                                                 |
|     title                 |     VARCHAR(400)       |     Oferta de   Empleo Público del Ayuntamiento de Majadahonda para 2020    |     Un título de   la oferta de empleo público.                                                                                                                                                                                                                                                                                                           |     http://purl.org/dc/terms/title                                                      |
|     description           |     VARCHAR(2000)      |     Oferta de   Empleo Público del Ayuntamiento de Majadahonda para 2020    |     Una   descripción de la oferta del empleo público.                                                                                                                                                                                                                                                                                                    |     http://purl.org/description                                                         |
|     date_modified         |     DATETIME           |     2019-11-18T11:00:00.0                                                   |     La última   fecha en la que la oferta de empleo público se ha modificado o cuando la   fecha del archivo se ha actualizado por un alimentador de datos.                                                                                                                                                                                               |     http://schema.org/dateModified                                                      |
|     date_published        |     DATETIME           |     2019-11-18T11:00:00.0                                                   |     La fecha y   hora de publicación de la oferta de empleo público en formato ISO 8601.                                                                                                                                                                                                                                                                  |     http://schema.org/datePublished                                                     |
|     fecha_aprobacion      |     DATETIME           |     2019-11-18T11:00:00.0                                                   |     Fecha de   aprobación de la convocatoria o de la oferta de empleo público.                                                                                                                                                                                                                                                                            |     http://vocab.ciudadesabiertas.es/def/sector-publico/empleo#fechaAprobacion          |
|     municipio_id          |     VARCHAR (50)       |     28006                                                                   |     Un Municipio   es el ente local definido en el artículo 140 de la Constitución española y la   entidad básica de la organización territorial del Estado según el artículo 1   de la Ley 7/1985, de 2 de abril, Reguladora de las Bases del Régimen Local.   En esta ocasión es el municipio que realiza la oferta de empleo público.                  |     http://vocab.linkeddata.es/datosabiertos/def/sector-publico/territorio#Municipio    |
|     municipio_title       |     VARCHAR   (200)    |     Alcobendas                                                              |     Su nombre,   que se especifica con la propiedad dct:title, es el proporcionado por el   Registro de Entidades Locales del Ministerio de Política Territorial, en   http://www.ine.es/nomen2/index.do                                                                                                                                                  |     http://vocab.linkeddata.es/datosabiertos/def/sector-publico/territorio#Municipio    |
|     provincia_id          |     VARCHAR (50)       |     28                                                                      |     Entidad   local con personalidad jurídica propia, determinada por la agrupación de   Municipios y división territorial para el cumplimiento de las actividades del   Estado. Su identificador, que se   especifica con la propiedad dct:identifier, es el proporcionado por el INE en   http://www.ine.es/daco/daco42/codmun/codmun09/09codmun.xls    |     http://vocab.linkeddata.es/datosabiertos/def/sector-publico/territorio#Provincia    |
|     provincia_title       |     VARCHAR   (200)    |     Madrid                                                                  |     Su nombre,   que se especifica con la propiedad dct:title, es el proporcionado por el Registro   de Entidades Locales del Ministerio de Política Territorial, en   http://www.ine.es/nomen2/index.do                                                                                                                                                  |     http://vocab.linkeddata.es/datosabiertos/def/sector-publico/territorio#Provincia    |
|     autonomia_id          |     VARCHAR (50)       |     Comunidad-Madrid                                                        |     Comunidad   Autónoma o Ciudad Autónoma                                                                                                                                                                                                                                                                                                                |     http://vocab.linkeddata.es/datosabiertos/def/sector-publico/territorio#Autonomia    |
|     autonomia_title       |     VARCHAR   (200)    |     Comunidad de   Madrid                                                   |     Su nombre,   que se especifica con la propiedad dct:title                                                                                                                                                                                                                                                                                             |     http://vocab.linkeddata.es/datosabiertos/def/sector-publico/territorio#Autonomia    |
|     boletin_oficial_id    |     VARCHAR (50)       |     BOL00001                                                                |     Boletín   oficial de la autoridad administrativa donde se pública la oferta de empleo   público.                                                                                                                                                                                                                                                      |     http://vocab.ciudadesabiertas.es/def/sector-publico/empleo#BoletinOficial           |





[comment]: <!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!> 
&nbsp;
### EMPLEO_CONVOCATORIA_PUBLICA <a name="id6"></a>
&nbsp;


|     Campo                     |     Tipo                |     Ejemplo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |     Descripción                                                                                                                                                             |     URL                                                                                     |
|-------------------------------|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
|     ikey                      |     VARCHAR (50)        |     1                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |     Identificador de la   Tabla (PK).                                                                                                                                       |                                                                                             |
|     id                        |     VARCHAR (50)        |     CONEM0001                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |     Identificación   de la convocatoria pública de empleo.                                                                                                                  |     http://purl.org/dc/terms/identifier                                                     |
|     title                     |     VARCHAR   (400)     |     Convocatoria   titulo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |     Una   denominación dada al recurso.                                                                                                                                     |     http://purl.org/dc/terms/title                                                          |
|     description               |     VARCHAR   (2000)    |     Bases específicas del proceso   selectivo para el acceso por turno libre a     plazas de "Técnico de Administración General", funcionario   de carrera, en el Ayuntamiento de Majadahonda (Madrid), por el sistema de   oposición                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |     Una   descripción del recurso dentro de un contexto dado.                                                                                                               |     http://purl.org/description                                                             |
|     date_published            |     DATETIME            |     2019-11-18T11:00:00.0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |     La fecha y   hora de publicación en formato ISO 8601.                                                                                                                   |     http://schema.org/datePublished                                                         |
|     fecha_aprobacion          |     DATETIME            |     2019-11-18T11:00:00.0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |     Fecha de   aprobación de la convocatoria o de la oferta de empleo público.                                                                                              |     http://vocab.ciudadesabiertas.es/def/sector-publico/empleo#fechaAprobacion              |
|     fecha_resolucion          |     DATETIME            |     2019-11-18T11:00:00.0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |     Fecha de   resolución de la convocatoria.                                                                                                                               |     http://vocab.ciudadesabiertas.es/def/sector-publico/empleo#fechaResolucion              |
|     estado_plazo              |     BIT(1)              |     Default 0 (Valores True (1) / False   (0))                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |     Estado del Plazo de presentación de   solicitudes para la convocatoria de empleo público. En caso de que este en el   plazo, el resultado será True(1).                 |     http://vocab.ciudadesabiertas.es/def/sector-publico/empleo#estadoPlazo                  |
|     plazos                    |     VARCHAR(200)        |     Hasta el   03/11/2020                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |                                                                                                                                                                             |                                                                                             |
|     num_plazas_convo          |     INT(10)             |     3                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |     Número de   plazas convocadas.                                                                                                                                          |     http://vocab.ciudadesabiertas.es/def/sector-publico/empleo#numeroPlazasConvocadas       |
|     lista_espera_ex           |     BIT(1)              |     Default 0 (Valores True (1) / False   (0))                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |     Convocatoria para una lista de espera   extraordinaria.                                                                                                                 |     http://vocab.ciudadesabiertas.es/def/sector-publico/empleo#listaEsperaExtraordinaria    |
|     observaciones             |     VARCHAR   (2000)    |     El plazo de   presentación de solicitudes será de veinte días naturales a contar desde el   siguiente al de la publicación de esta resolución en el «Boletín Oficial del   Estado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |     Observaciones   a la convocatoria de empleo público.                                                                                                                    |     http://vocab.ciudadesabiertas.es/def/sector-publico/empleo#observaciones                |
|     disposiciones             |     VARCHAR   (2000)    |     BOLETÍN   OFICIAL DEL ESTADO, Dispuesto el 17/09/2020, Publicado el 12/10/2020.   Resolución de 17 de septiembre de 2020, del Ayuntamiento de Majadahonda   (Madrid), referente a la convocatoria para proveer varias plazas   (https://www.boe.es/diario_boe/txt.php?id=BOE-A-2020-12155). BOLETÍN OFICIAL   DE LA COMUNIDAD DE MADRID, Dispuesto el 24/07/2020 Publicado el 03/09/2020,   Majadahonda. Ofertas de empleo. Convocatoria proceso selectivo,   (http://www.bocm.es/bocm-20200903-43?ajax_popup=1)                                                                                                                                                                                                                                                                                                                                                                                                           |     Disposiciones   legales de una convocatoria de empleo público.                                                                                                          |     http://vocab.ciudadesabiertas.es/def/sector-publico/empleo#disposiciones                |
|     requisitos                |     VARCHAR   (2000)    |     Estar en   posesión o en condiciones de obtener el Título Universitario de Licenciado en   Derecho, en Ciencias Políticas y de la Administración, en Económicas, en   Administración y Dirección de Empresas, en Ciencias Actuariales y Financieras   o de los Títulos de Grado correspondientes o equivalentes                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |     Requisitos   de una convocatoria de empleo público.                                                                                                                     |     http://vocab.ciudadesabiertas.es/def/sector-publico/empleo#requisitos                   |
|     bases                     |     VARCHAR   (2000)    |     Cumplir  los    requisitos  generales  establecidos  en    el  artículo  56    del  texto  refundido    de  la  Ley    del Estatuto  Básico  del    Empleado  Público  aprobado por  Real    Decreto  Legislativo  5/2015,…                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |     Bases de la   convocatoria de empleo público.                                                                                                                           |     http://vocab.ciudadesabiertas.es/def/sector-publico/empleo#bases                        |
|     bases_url                 |     VARCHAR   (200)     |     https://www.majadahonda.org/documents/36614/743494/TAG+-+Bases.pdf/c134244d-d770-8eb8-ddef-1a6f11b3e04a                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |     URL de las   bases de la convocatoria de empleo público.                                                                                                                |     http://vocab.ciudadesabiertas.es/def/sector-publico/empleo#basesURL                     |
|     formulario_inscripcion    |     VARCHAR   (200)     |     https://www.majadahonda.org/como-solicitar-la-admision-a-un-proceso-selectivo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |     URL del   formulario de inscripción a la convocatoria de empleo público.                                                                                                |     http://vocab.ciudadesabiertas.es/def/sector-publico/empleo#formularioInscripcion        |
|     pruebas                   |     VARCHAR   (2000)    |     Quienes   deseen tomar parte en el   proceso   selectivo deberán hacerlo mediante solicitud normalizada que será facilitada   gratuitamente en el Ayuntamiento de   Majadahonda, o mediante su descarga en la   página web www.majadahonda.org.4.2. La  solicitud deberá ir acompañada,  necesariamente, de  justificante  que    acredite  el  pago    de  la tasa por derechos de   examen. En caso de tener derecho a bonificación en el pago de dicha tasa por   estar en alguno de los supuestos recogidos en la Ordenanza  Fiscal    nº15  del  Ayuntamiento  de    Majadahonda  (BOCM  nº    311,  de  31    de diciembre  de  2012)    se  presentará  carta    de  pago  bonificada    y  documentación  que    acredite  tal derecho.4.3 El   plazo de presentación de solicitudes será de 20 días naturales contados a   partir del siguiente al de la publicación del anuncio de convocatoria en el   BOE….    |     Pruebas   selectivas para la convocatoria de empleo público.                                                                                                            |     http://vocab.ciudadesabiertas.es/def/sector-publico/empleo#pruebas                      |
|     grupo_profesional         |     VARCHAR (200)       |     SKOS:  http://vocab.linkeddata.es/datosabiertos/kos/sector-publico/empleo/grupo-profesional/A1                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |     Grupo   profesional: A, B, C o E.     URL SKOS:     http://vocab.linkeddata.es/datosabiertos/kos/sector-publico/empleo/grupo-profesional                                |     http://vocab.ciudadesabiertas.es/def/sector-publico/empleo#grupoProfesional             |
|     empleado_publico          |     VARCHAR   (200)     |     SKOS:    http://vocab.linkeddata.es/datosabiertos/kos/sector-publico/empleo/empleado-publico/funcionario                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |     Tipo de   empleado público: tipo de funcionario y tipo de personal laboral.                                                                                             |     http://vocab.ciudadesabiertas.es/def/sector-publico/empleo#empleadoPublico              |
|     cuerpo                    |     VARCHAR   (200)     |     SKOS:  http://vocab.linkeddata.es/page/datosabiertos/kos/sector-publico/empleo/cuerpo/administracion-general                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |     Cuerpo o   escala de la administración pública: general, especial, general o especial,   habilitado de carácter nacional, general o habilitado de carácter nacional.    |     http://vocab.ciudadesabiertas.es/def/sector-publico/empleo#cuerpo                       |
|     modalidad                 |     VARCHAR   (200)     |     SKOS:  http://vocab.linkeddata.es/datosabiertos/kos/sector-publico/empleo/modalidad/oposicion                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |     Modalidad de   la convocatoria: Oposición, Concurso o Concurso-oposición.                                                                                               |     http://vocab.ciudadesabiertas.es/def/sector-publico/empleo#modalidad                    |





[comment]: <!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!> 
&nbsp;
### EMPLEO_BOLETIN_OFICIAL <a name="id7"></a>
&nbsp;

|     Campo             |     Tipo               |     Ejemplo                                                                  |     Descripción                                                                                                                                                                                |     URL                                                  |
|-----------------------|------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
|     ikey              |     VARCHAR (50)       |     1                                                                        |     Identificador de la   Tabla (PK).                                                                                                                                                          |                                                          |
|     id                |     VARCHAR (50)       |     BOE-A-2020-283                                                           |     Identificador del   boletín oficial de empleo.                                                                                                                                             |     http://purl.org/dc/terms/identifier                  |
|     title             |     VARCHAR   (200)    |     Boletín Oficial de la   Comunidad de Madrid: jueves 12 noviembre 2020    |     Una   denominación dada al recurso.                                                                                                                                                        |     http://purl.org/dc/terms/title                       |
|     description       |     VARCHAR (400)      |     Boletín Oficial del   Estado: lunes 2 de noviembre de 2020, Núm. 283     |     Una   descripción del recurso dentro de un contexto dado.                                                                                                                                  |     http://purl.org/description                          |
|     id_local          |     VARCHAR(200)       |     URI:      https://www.boe.es/eli/es-md/a/2020/11/02                      |     El identificador único   que se usa como una referencia en el sistema local para mantener la   compatibilidad hacia atrás. Por ejemplo el CELEX a nivel de la UE o el NOR en   Francia.    |     http://data.europa.eu/eli/ontology#id_local          |
|     date_published    |     DATETIME           |     2019-11-18T11:00:00.0                                                    |     La fecha y   hora de publicación en formato ISO 8601.                                                                                                                                      |     http://schema.org/datePublished                      |




[comment]: <!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!> 
&nbsp;
### EMPLEO_PLAZA_TURNO <a name="id8"></a>
&nbsp;

|     Campo              |     Tipo             |     Ejemplo                                                                                   |     Descripción                                                                                                                                                                                                   |     URL                                                                                     |
|------------------------|----------------------|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
|     ikey               |     VARCHAR (50)     |     1                                                                                         |     Identificador de la   Tabla (PK).                                                                                                                                                                             |                                                                                             |
|     id                 |     VARCHAR (50)     |     Ejemplo: 188647-libre                                                                     |     Referencia inequívoca   al recurso dentro de un contexto dado.                                                                                                                                                |     http://purl.org/dc/terms/identifier                                                     |
|     plazas_x_turno     |     INT(10)          |     3                                                                                         |     Plaza de trabajo por   turno o vía de ingreso a la convocatoria.                                                                                                                                              |     http://vocab.ciudadesabiertas.es/def/sector-publico/empleo#PlazaPorTurno                |
|     turno_plaza        |     VARCHAR (200)    |     SKOS:   http://vocab.linkeddata.es/datosabiertos/kos/sector-publico/empleo/turno/libre    |     Turno de presentación   para una plaza: libre, estabilización, promoción interna, reservado por algún   motivo.     URL SKOS:     http://vocab.linkeddata.es/datosabiertos/kos/sector-publico/empleo/turno    |     http://vocab.ciudadesabiertas.es/def/sector-publico/empleo#turnoPlaza                   |
|     convocatoria_id    |     VARCHAR (50)     |     CONEM0001                                                                                 |     Convocatoria   de Empleo Público para cubrir plazas que provienen de la Oferta de Empleo   Público.     FK de la   tabla EMPLEO_CONVOCATORIA_PUBLICA                                                          |     http://vocab.ciudadesabiertas.es/def/sector-publico/empleo#ConvocatoriaEmpleoPublico    |



[comment]: <!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!> 
&nbsp;
### TABLAS DE RELACIÓN NECESARIAS PARA MANTENER LA ESTRUCTURA DEL VOCABULARIO <a name="id9"></a>


&nbsp;
#### EMPLEO_REL_BOLETIN_CONVOCA <a name="id10"></a>
&nbsp;

|     Campo              |     Tipo            |     Ejemplo                                                                                 |     Descripción                                                                                                                                       |     URL                                                                                     |
|------------------------|---------------------|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
|     ikey               |     VARCHAR (50)    |     1                                                                                       |     Identificador de la   Tabla (PK).                                                                                                                 |                                                                                             |
|     id                 |     VARCHAR (50)    |     Interno Para mantener   coherencia con la estructura de la API. Ejemplo: EMRELCON001    |     Referencia inequívoca   al recurso dentro de un contexto dado.                                                                                    |     http://purl.org/dc/terms/identifier                                                     |
|     boletin_id         |     VARCHAR (50)    |     BOE-A-2020-283                                                                          |     Boletín oficial de la   autoridad administrativa.     FK de la tabla EMPLEO_BOLETIN_OFICIAL                                                       |     http://vocab.ciudadesabiertas.es/def/sector-publico/empleo#BoletinOficial               |
|     convocatoria_id    |     VARCHAR (50)    |     CONEM0001                                                                               |     Convocatoria   de Empleo Público para cubrir plazas que provienen de la Oferta de Empleo   Público.     FK de la   tabla EMPLEO_OFERTA_PUBLICA    |     http://vocab.ciudadesabiertas.es/def/sector-publico/empleo#ConvocatoriaEmpleoPublico    |




[comment]: <!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!> 
&nbsp;
#### EMPLEO_REL_OFERTA_CONVOCA <a name="id11"></a>
&nbsp;

|     Campo              |     Tipo            |     Ejemplo                                                                                 |     Descripción                                                                                                                                             |     URL                                                                                     |
|------------------------|---------------------|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
|     ikey               |     VARCHAR (50)    |     1                                                                                       |     Identificador de la   Tabla (PK).                                                                                                                       |                                                                                             |
|     id                 |     VARCHAR (50)    |     Interno Para mantener   coherencia con la estructura de la API. Ejemplo: EMRELCON001    |     Referencia inequívoca   al recurso dentro de un contexto dado.                                                                                          |     http://purl.org/dc/terms/identifier                                                     |
|     oferta_id          |     VARCHAR (50)    |     OFEM0001                                                                                |     Oferta de   Empleo Público que realiza la administración para cubrir plazas según las   necesidades.     FK de la   tabla EMPLEO_OFERTA_PUBLICA         |     http://vocab.ciudadesabiertas.es/def/sector-publico/empleo#OfertaEmpleoPublico          |
|     convocatoria_id    |     VARCHAR (50)    |     CONEM0001                                                                               |     Convocatoria   de Empleo Público para cubrir plazas que provienen de la Oferta de Empleo   Público.     FK de la   tabla EMPLEO_CONVOCATORIA_PUBLICA    |     http://vocab.ciudadesabiertas.es/def/sector-publico/empleo#ConvocatoriaEmpleoPublico    |



&nbsp;

## TAXONOMÍAS SKOS <a name="id12"></a>
&nbsp;

### GRUPO-PROFESIONAL <a name="id13"></a>
http://vocab.linkeddata.es/datosabiertos/kos/sector-publico/empleo/grupo-profesional
&nbsp;
Tesauro que recoge los grupos profesionales de la Administración General del Estado en España.
|     Término    |     Label    |
|----------------|--------------|
|     A1         |     A1       |
|     A2         |     A2       |
|     B          |     B        |
|     C1         |     C1       |
|     C2         |     C2       |



&nbsp;
### EMPLEADO-PUBLICO <a name="id14"></a>
http://vocab.linkeddata.es/datosabiertos/kos/sector-publico/empleo/empleado-publico
&nbsp;
Tesauro que recoge los tipos de empleados públicos en España.
|     Tipo                |     Subtipo 1                      |     Subtipo 2                                  |     Label                                                |
|-------------------------|------------------------------------|------------------------------------------------|----------------------------------------------------------|
|     funcionario         |                                    |                                                |     funcionario                                          |
|                         |     funcionario-carrera            |                                                |     Funcionario de carrera.                              |
|                         |     funcionario-interino           |                                                |     Funcionario   interino.                              |
|                         |                                    |     funcionario-interino-acumulacion-tareas    |     Funcionario interino   por acumulación de tareas.    |
|                         |                                    |     funcionario-interino-programa              |     Funcionario interino   por programa.                 |
|                         |                                    |     funcionario-interino-sustitucion           |     Funcionario interino   por sustitución.              |
|                         |                                    |     funcionario-interino-vacante               |     Funcionario interino   por plaza vacante.            |
|     Personal-laboral    |                                    |                                                |     Personal Laboral.                                    |
|                         |     personal-laboral-fijo          |                                                |     Personal Laboral Fijo.                               |
|                         |     personal-laboral-indefinido    |                                                |     Personal laboral Indefinido.                         |
|                         |     personal-laboral-temporal      |                                                |     Personal Laboral Temporal.                           |
|                         |                                    |     personal-laboral-temporal-en-convenio      |     Personal Laboral Temporal en Convenio.               |



&nbsp;
### CUERPO <a name="id15"></a>
http://vocab.linkeddata.es/datosabiertos/kos/sector-publico/empleo/cuerpo
&nbsp;
Tesauro que recoge los cuerpos de la Administración General del Estado de España.
|     Término                                              |     Label    |
|----------------------------------------------------------|--------------|
|     administración-especial                              |     AE       |
|     administracion-general                               |     AG       |
|     administracion-general-o-especial                    |     AGE      |
|     habilitado-caracter-nacional                         |     HCN      |
|     habilitado-general-o-habilitado-caracter-nacional    |     AGHCN    |




&nbsp;
### MODALIDAD <a name="id16"></a>
http://vocab.linkeddata.es/datosabiertos/kos/sector-publico/empleo/modalidad
&nbsp;
Tesauro que recoge las modalidades de las convocatorias de empleo público en España.
|     Término               |     Label                  |
|---------------------------|----------------------------|
|     concurso              |     Concurso.              |
|     concurso-oposicion    |     Concurso oposición.    |
|     oposicion             |     Oposición.             |



&nbsp;
### TURNO <a name="id17"></a>
http://vocab.linkeddata.es/datosabiertos/kos/sector-publico/empleo/turno	
&nbsp;
Tesauro que recoge los turnos de acceso de la Administración General del Estado de España.
|     Término      |     Label         |
|------------------|-------------------|
|     interno      |     Interno.      |
|     libre        |     Libre.        |
|     reservado    |     Reservado.    |

     


















&nbsp;


<p float="right" align="center">
<img src="https://ciudadesabiertas.es/assets/img/cabiertas/gobEspana-logo.svg" alt="Logo Gobierno España" width="200"/>
<img src="https://ciudadesabiertas.es/assets/img/cabiertas/red-logo.svg" alt="Logo red.es" width="150"/>
<img src="https://ciudadesabiertas.es/assets/img/cabiertas/ciudadesInteligentes-logo.svg" alt="Logo CiudadesInteligentes" width="150"/>
<img src="https://ciudadesabiertas.es/assets/img/cabiertas/unionEuropea-logo.svg" alt="Logo UnionEuropea" width="200"/>
</p>


<p float="right" align="center">
<img src="https://ciudadesabiertas.es/assets/img/cabiertas/ayuntAcoruna-logo.svg" alt="Logo AyuntACoruña" width="200"/>
<img src="https://ciudadesabiertas.es/assets/img/cabiertas/ayuntMadrid-logo.svg" alt="Logo Madrid" width="100"/>
<img src="https://ciudadesabiertas.es/assets/img/cabiertas/ayuntSantiagoCompostela-logo.svg" alt="Logo Concello Santiago" width="200"/>
<img src="https://ciudadesabiertas.es/assets/img/cabiertas/ayuntZaragoza-logo.svg" alt="Logo Ayun.Zaragoza" width="200"/>
</p>



