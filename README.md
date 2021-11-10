# Segmentaci-n_de_clientes
Segmentacion_de_clientes_con_kmean_RFM


Las empresas emplean todos sus esfuerzos en establecer relaciones con sus clientes  y  disminuir la tasa  de abandono.Por lo que es necesario, segmentar para conocer a fondo a los clientes y así atender sus necesidades y resolver sus problemas. Así mismo, las empresas lanzan al mercado nuevos productos y servicios, por lo que desean saber qué segmentos se beneficiarían del lanzamiento de este nuevo producto?, para qué tipo de clientes se está diseñando el producto?, además de cuál será el retorno monetario de cada segmento si se lanza este nuevo producto/servicio?.
No definir segmentos, no sólo hará gastar más dinero en estrategias de marketing, sino que no se podrá satisfacer ni fidelizar bien a los clientes. Mediante la segmentación se puede identificar a los clientes más rentables, una vez que se sepa cómo son y qué quieren, buscar la mejor manera de fidelizarlos, en términos de canal de distribución, precio, calidad, etc. Al segmentar a los clientes ya no se corre el riesgo de hacer inversiones incoherentes, en recursos, agregados de valor y elementos que no generen ningún efecto positivo en el usuario. En cambio, destinarás recursos a estrategias alineadas a las características de cada segmento, que realmente promuevan satisfacción a estos, brindando un mayor potencial de retención y fidelización.



En general la segmentación de clientes permite:

Descubrir segmentos de clientes que representen buenas oportunidades de negocio.
Conocer a fondo a los clientes para atender sus necesidades y resolver sus problemas.
Enfocar acciones y campañas hacia un segmento  específico, acorde a sus necesidades.
Realizar estrategias de marketing y comunicación con mensajes personalizados.
Mejorar los resultados de la empresa gracias a la optimización de resultados.



Por otro lado, cada eCommerce puede realizar la segmentación en función de sus propias necesidades.Los factores que pueden ser más importantes son los siguientes:

1. Valor del carrito.

No todos los clientes son igual de valiosos para un eCommerce, una vez se ha realizado una transacción, los clientes que superen un importe previamente fijado pueden pasar a formar parte del segmento de los “clientes VIP”, asegurando así que recibirán una especial atención y seguimiento.

2.  Clientes recurrentes.

Los clientes recurrentes ya realizan compras de forma más o menos asidua, de forma que su seguimiento será especialmente importante para alargar en lo posible su vida útil y obtener el mayor número de pedidos posibles, ofreciendo puntualmente los productos que adquieren en el caso que se detecte algún tipo de fuga o pérdida de asiduidad.


3. Clientes que no han comprado en los últimos "x" días.


Evaluar el tiempo transcurrido desde la última compra para poder ofrecer productos alternativos o algún tipo de ventaja que llame la atención del usuario, para que vuelva a entrar en el eCommerce.


**Datos:**


Los datos utilizados son un conjunto de datos de comercio electrónico (Retail en linea) disponible en Kaggle a través de este enlace  https://www.kaggle.com/carrie1/ecommerce-data  http://archive.ics.uci.edu/ml/datasets.php


El conjunto de datos son datos transaccionales que contienen las transacciones durante 2011 para un minorista con sede en el Reino Unido. La empresa vende principalmente regalos únicos para todas las ocasiones. Muchos clientes de la empresa son mayoristas ".


**Variables del análisis**


InvoiceNo (invoice_num): Un número asignado a cada transacción (número de factura)

StockCode (stock_code): Código de producto

Description (description): Nombre del producto

Quantity (quantity): Número de productos comprados para cada transacción

InvoiceDate (invoice_date): Marca de tiempo para cada transacción ( fecha de la factura)

UnitPrice (unit_price): Precio del producto por unidad

CustomerID (cust_id): Identificador único de cada cliente

Country (country): Nombre del país

**Objetivo:**

Segmentar a los usuarios del eCommerce con el fin de enfocar acciones y campañas de marketing personalizadas a los usuarios pertenecientes a dichos grupos.

 **¿Qué se aplicará para lograr el objetivo?**

**Pre-procesamiento de datos**

-  Identificación de variables categóricas y numéricas
-  dentificación de variables con valores missing
- 	Eliminación de valores missing
- 	Identificación de registros duplicados
- 	Eliminación de registros duplicados

**Análisis Exploratorio de Datos:**

- 	Gráficos de Box Plot para identificación de outliers, mediana, media, y asimetría de las variables.
- 	Identificación de outliers mediante el método analítico: método hard edge
- 	Renombramiento de variables
- 	Creación de nuevas variables ( formato de año, mes y día )
- 	Gráficos de barras para transacciones por: mes, hora, día.

**Segmentación de clientes mediante el método RFM.**

- Segmentación de RFM mediante agrupación en clústeres de K-means.
- 
- Estandarización de las características de RFM
- 
- Elección del hiperparámetro k (número de grupos) mediante el método Elbow 

**Hallazgos:**


Mediante este análisis se encontró 3 segmentos o grupos de usuarios:
Clúster 0: Segmento de Usuarios Top .
Los clientes de esta categoría son compradores habituales recientes/ actuales (poca antigüedad , frecuencia alta). Su transacción más reciente fue hace solo unos días, con una frecuencia de 26 transacciones en los últimos seis meses . (son 66 usuarios, equivalente al 1.5 % de toda la base de usuarios).

**Clúster 1: Segmento de Usuarios Abandonados.**


Los usuarios de esta categoría son los clientes que optan por no participar ( frecuencia alta , frecuencia baja). Su última transacción fue hace más de 5 meses, con solo 0 o 1 transacción en los últimos seis meses. (son 1364 usuarios, equivalente al 31.5 % de toda la base de usuarios).


**Clúster 2: Segmento de Usuarios Casuales.**

Los usuarios de esta categoría son los clientes habituales (modestos tanto en recency como en frequency)). Su transacción más reciente se realizó en los últimos dos meses, con una frecuencia de hasta tres transacciones en los últimos seis meses. Son, como se ha observado ampliamente, la mayor parte de nuestra base de usuarios (son 2908 usuarios, equivalente al 67 % de toda la base de usuarios).











