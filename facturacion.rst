Facturación
===========

Se detalla a continuación la facturación para la Argentina y en particular la facturación electrónica contra la AFIP.

Configurar Punto de Venta:
--------------------------
Según las reglas de facturación de la Argentina existen distintos Puntos de Ventas, lo cuales pueden ser: Manuales, Electrónicos o Tickeadora Fiscal.
Es por eso que antes de facturar se deben configurar los puntos de venta. 
Esto supone marcar qué tipo de Punto de venta es y qué facturas emite el mismo (A, B, C, etc.). 

.. image:: img/detallepuntodeventa.png
   :width: 750 px

A cada una de las facturas que se configuren se les deberá crear una secuencia para señalar la numeración que llevará ese tipo de factura en ese punto de venta específico.

.. image:: img/secuenciafactura.png
   :width: 750 px

En el caso de querer realizar facturas manuales se podrá modificar el template .odt de factura para generar la factura según la factura pre impresa que tenga la empresa.
El template de facturas viene armado para tomar los datos que devuelve la AFIP en la generación de facturas electrónicas lo que permite imprimir facturas válidas.
 
Para poder realizar la facturación es importante tener bien configurada la Empresa: cargar certificados de AFIP para la facturación electrónica, la condición ante el IVA y el CUIT y el logo de la misma (usado en la factura).
También se deberá cargar de forma correcta el cliente (CUIT y tipo de IVA).

Confeccionar una factura:
--------------------------
Una vez configurado un Punto de Venta se puede proceder a facturar. Para el caso de facturar de forma electrónica será necesario contar con acceso Internet.
Para conformar una factura será necesario Contar con: una Entidad, un término de pago y comenzar a llenar las lineas de la factura. 
Si el usuario tiene permiso, al igual que en los otros módulos de Tryton, el usuario podrá crear todas estos datos en el momento mismo de crear una factura.
 
.. image:: img/factura.png
   :width: 750 px

Factura Electrónica:
--------------------
En el caso de tratarse de una factura electrónica será necesario completar los datos que la AFIP solicita, es decir, ver si se trata de un Producto o Servicio y en este caso especificar las fechas del mismo. 
 
.. image:: img/afipfactura.png
   :width: 750 px

En el sector de transacciones se podrán ver los mensajes de las comunicaciones realizadas con la AFIP. 
 
Una vez completados los datos necesario para la factura se podrán realizar las acciones de validar o  confirmar la factura (según los permisos del usuario). Es la acción de confirmar que realiza la comunicación con la AFIP (caso de factura electrónica) y que inmuta todos los campos dejando la factura lista para realizar el pago.
 
.. image:: img/afipfactura.png
   :width: 750 px

Tryton maneja otras formas para la generación de tickets rápido (ver tryton pos). 
   
Recuperar Factura:
------------------

El módulo "Recuperar Factura" es una funcionaldiad para factura electrónica de la AFIP. Se utiliza ante cortes de conectividad al realizar una (o varias) facturas. Permite consultar en la AFIP por un numero de factura para ver si la misma existe en la AFIP y en caso de ser necesario traer los datos de la AFIP y agregarlos a una factura que quedó mal confeccionada.

En este caso, la factura quedará en estado borrador en nuestro sistema.

.. image:: img/01-factura-borrador.png
   :width: 750 px

Para poder pasarla a estado confirmado y guardar los datos de AFIP (CAE y fecha vencimiento CAE), utilizaremos el asistente de Recuperar Factura. Este asistente se ejecuta desde el botón de lanzar acciones en la sección de Facturas.

Cuando se ejecuta el asistente, debemos primer consultar en AFIP el número de comprobante que estamos queriendo recuperar. Para ello, completamos los datos de punto de venta, tipo de comprobante, y número de comprobante.

.. image:: img/02-asistente-buscar-factura.png
   :width: 750 px

Al consultar, nos traerá una pantalla con los datos de la factura confirmada en AFIP. Debemos ir a la pestaña *factura a recuperar* y buscar la factura que queremos pasar a estado confirmada y guardar los datos de AFIP.

.. image:: img/03-asistente-comprobar-factura.png
   :width: 750 px
.. image:: img/04-asistente-seleccionar-factura.png
   :width: 750 px

Realizada la acción de guardar factura, podemos comprobar que se le ha asignado su número de comprobante correspondiente y la ha pasado a estado confirmada (y obviamente creado el asiento contable).

.. image:: img/05-factura-confirmada.png
   :width: 750 px

Facturas de Proveedor:
----------------------
En el apartado Facturas de Proveedor podrá cargar las facturas de sus proveedores ingresando cada una de las lineas que la misma contiene.
