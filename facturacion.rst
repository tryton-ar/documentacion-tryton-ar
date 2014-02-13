Facturación
===========

Se detalla a continuación la facturación para la Argentina y en particular la facturación electrónica contra la AFIP.

Configurar Punto de Venta:
--------------------------
Según las reglas de facturación de la Argentina existen distintos Puntos de Ventas, lo cuales pueden ser: Manuales, Eletrónicos o Tickeadora Fiscal.
Es por eso que antes de facturar se deben configurar los puntos de venta. 
Esto supone marcar qué tipo de Punto de venta es y qué facturas emite el mismo (A, B, C, etc.). 

.. image:: img/detallepuntodeventa.png
   :width: 750 px

A cada una de las facturas que se configuren se les deberá crear una secuencia para señalar la numeración que llevará ese tipo de factura en ese punto de venta específico.

.. image:: img/secuenciafactura.png
   :width: 750 px

En el caso de querer realizar facturas manuales se podrá modificar el template .odt de fatcura para generar la factura según la factura pre imrpesa que tenga la empresa.
El template de facturas viene armado para tomar los datos que devuelve la AFIP en la generación de facturas electrónicas lo que permite imprimir facturas válidas.
 
Para poder realizar la facturación es importante tener bien configurada la Empresa: cargar certificados de AFIP para la facturación electrónica, la condición ante el IVA y el CUIT y el logo de la misma (usado en la factura).
También se deberá cargar de forma correcta el cliente (CUIT y tipo de IVA).
