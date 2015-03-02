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

En el caso de tratarse de una factura electrónica será necesario completar los datos que la AFIP solicita, es decir, ver si se trata de un Producto o Servicio y en este caso especificar las fechas del mismo. 
 
.. image:: img/afipfactura.png
   :width: 750 px

En el sector de transacciones se podrán ver los mensajes de las comunicaciones realizadas con la AFIP. 
 
Una vez completados los datos necesario para la factura se podrán realizar las acciones de validar o  confirmar la factura (según los permisos del usuario). Es la acción de confirmar que realiza la comunicación con la AFIP (caso de factura electrónica) y que inmuta todos los campos dejando la factura lista para realizar el pago.
 
.. image:: img/afipfactura.png
   :width: 750 px

Tryton maneja otras formas para la generación de tickets rápido (ver tryton pos). 
   
