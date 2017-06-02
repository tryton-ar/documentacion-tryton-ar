Contratos
=========

El módulo "Contratos" es desarrollado por la empresa española NanTic. Copiamos la documentación completa del módulo. 

Si nuestra empresa tiene un contrato de servicios con un cliente, por el cual prestamos periódicamente algún tipo de servicio, esta funcionalidad nos permitirá hacer que el sistema genere las facturas de dichos servicios según la periodicidad pactada con nuestro cliente. En primer lugar veremos como configurar el sistema indicándole qué servicios serán elegibles en los contratos, posteriormente veremos como informar un nuevo contrato y por último, cómo generar los consumos y las facturas derivadas del contrato.
Configuración

Como ya hemos comentado, lo primero que deberemos hacer es indicarle al sistema qué servicios podrán ser facturados por medio de los contratos. Para ello accederemos a |menu_servicio_contrato| y se nos abrirá una pestaña con todos los productos que hayamos añadido previamente (si es la primera vez que accedemos, el listado nos aparecerá vacío). Si queremos añadir un nuevo producto deberemos clicar en Nuevo y en el formulario que se nos abrirá tendremos que seleccionar el |product| de tipo servicio que queramos añadir (solo nos dejará escoger entre esta tipología de productos).

Por último deberemos indicar en |menu_config_contratos| la secuencia que se utilizará cuando se generen los contratos. 
Introducir un nuevo contrato

Para introducir un nuevo contrato deberemos acceder a |menu_contratos| y clicar en Nuevo. En el formulario que se nos abrirá deberemos indicar un |party|, cuando empezará el periodo en |start_period_date|, la fecha de incio de factura en |first_date_inv| y la |freq| e |interval| con la que queremos que se generen las facturas. Estos dos últimos campos están relacionados entre sí: en |freq| indicaremos la periodicidad que queramos como base, y en |interval| cada cuanto del valor elegido en |freq| queremos que se genere la factura. Por ejemplo, si queremos que la factura se genere cada mes indicaremos:

    |freq|: Mensualmente.
    |interval|: 1.

Si queremos que la factura se genere cada dos semana lo podremos hacer de dos formas:

    |freq|: Semanalmente.
    |interval|: 2.

o también:

    |freq|: Diariamente.
    |interval|: 14.

.. note:: En el campo |interval| el sistema no distingue entre 1, 0 o dejarlo vacío. En los tres casos el sistema realizará las facturas como si le hubiéramos indicado 1.

Una vez rellenados los campos de la cabecera, tendremos que indicar las |lines| del contrato clicando en el icono Nuevo del propio campo. En la ventana que nos aparecerá deberemos indicar, al menos, |line_start_date|. Además si queremos, podremos definir |unit_price| y la |description| que aparecerá en la factura cuando se genere. Además, si lo deseamos, podremos seleccionar una |end_date_line| de la línea, un producto del tipo servicio en |service|.

Con la información introducida, podremos guardar el contrato en estado borrador (lo que no supondrá una activación del mismo) o clicar en Validar para activarlo.
Generar consumos y facturas de un contrato

Cuando hayamos validado el contrato con los parámetros acordados con nuestro cliente, podremos generar los consumos y facturas derivados del mismo. Un consumo representa la realización de un servicio, y se genera según la información introducida en el contrato, por cada línea de contrato se generará una línea de consumo para cada periodo. Posteriormente, sobre la información de los consumos se generarán la correspondiente factura del periodo con una línea para cada consumo.

Por medio de |menu_create_consupmitions| podremos generar los consumos pendientes de todos los contratos validados hasta la fecha indicada. Una vez los genere el asistente, se nos abrirá una pestaña con todas las líneas de consumo, tendiendo en la pestaña A facturar los consumos que todavía no se han facturado. También podremos acceder al listado de los consumos generados por medio de |menu_contract_consumption|.

Cuando queramos facturar la líneas de consumo generadas, lo haremos por medio del asistente |menu_create_invoices|. Con ello generaremos una factura en estado borrador con los consumos pendientes por cada contrato y periodo. Es decir, que de un contrato con dos líneas se generarán dos líneas de consumo por periodo pero solo una factura con dos líneas de factura.


Contratos se utiliza para facilitar la gestión en aquellas empresas u organziaciones que necesitan facturar o realizar débitos de forma recurrente (semanalk, quincenal, mensual, etc.). Es decir cobro de cuotas, suscripciones, etc.

El contrato permite distintas opciones de configuración que cumplen con los distintos csaos de uso (cobro por adelantado, vencido, cálculo parcial, etc.).

Contratos en Argentina: 
-----------------------

Se realizó el desarrollo que permite generar las facturas y postearlas en la AFIP (Facturación Electrónica). Es decir luego de generarse los consumos del mes se puede generar las facturas de forma automática con un asistente. 

Se desarrolló un Módulo Cobranzas (ver documentación Cobranzas) que permite seleccionar un medio de pago en la Entidad o en el contrato para poder realizar débitos automáticos con distintos medios de pago. 
