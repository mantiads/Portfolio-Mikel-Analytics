# <p align="center">Proyecto Data Analytics Fintech</p>

[Acceso a archivo Jupyter.](https://github.com/mantiads/Portfolio-Mikel-Analytics/blob/main/Codigo_analisis.ipynb)

## Análisis evolución productos comercializados.

Comenzamos analizando la evolución en la contratación de los productos comercializados a traves de las 17 distintas particiones (periodo mensual). 
- Hay productos a los cuales hay que dar una vuelta y ver porque no se están comercializando o son muy poco vendidos. Estamos hablando de loans, mortage, em_account_pp y em_account_p.
- Entre el segundo grupo de productos menos demandados nos encontramos con funds y securities.
    -  funds aumento contrataciones durante todo el 2018, aunque lleva los ultimos 6 meses atascado en las 1300 contrataciones.
    -  securities muestra un rápido crecimiento, aunque lleva los últimos 3 meses con signos de ralentecimiento.
- Al fijarnos en los depositos, vemos como se ha ido rebajando su contratación.
    - Los short_term_deposit comenzaron a perder contrataciones a finales del 2018, desapareciendo por completo a principios del 2019.
    - long_term_deposit sigue siendo un producto contratado aunque desde principios del 2019 muestra una tendencia negativa del 2% mensual aproximadamente. 
- Con respecto a las tarjetas, las dos muestras un buen crecimiento. Resaltal que contamos con 10 veces mas de contratación de tarjetas de debito frente a las de crédito.
- Los productos payroll y pension_plan muestras un comportamiento muy similar. Estos dos productos parece que se comercizan en conjunto. En Enero de 2019 ambas sufrieron una bajada repentina superior al 10%.
- payroll_account y emc_account llevan ambas un buen crecimiento, casi duplicando su contratacion la primera de ellas y aumentando un 50% la segunda.
- em_acount (La estrella del juego) disparó sus contrataciones desde el mes de Julio hasta Noviembre, donde parece que se está asentando. El 60% de los clientes en la última partición tiene este producto.

En un siguiente paso deberemos de analizar la evoluión de cada producto con respecto a los distintos patrones socio-demográficos de los que disponemos para identificar patrones y tendencias.
<p align="center">
<img src="/images/8_evolucion_contratos_particiones.png" alt="Analisis AVProductInstalled">
</p>

## Análisis socio-demográfico.
Pasamos a analizar ahora el perfil de los clientes en la última de las particiones (situación actual).

Comenzamos con el género. Vemos que está bastante igualada la distribución de los clientes. Con respecto a la edad la mayoría de clientes están entre 20 y 25 años.
<table>
  <tr>
    <td><img src="/images/12_genero.png" alt="Analisis AVProductInstalled" ></td>
    <td><img src="/images/13_edad.png" alt="Analisis AVProductInstalled" ></td>
  </tr>
</table>

Entrando en una mayor granularidad con respecto al análisis anterior, vemos como hay mayoría de mujeres en las franjas comprendidas entre los 20 y 30 años, mientras que ocurre lo contrario en la edades comprendidas entre 30 y 65 años.

<p align="center">
<img src="/images/14_piramide.png" alt="Analisis AVProductInstalled"  width="500">
</p>

A nivel de segmentos, la mayoría de clientes son Universitarios (lo que concuerda con el análisis de la distribución de edad), seguido de Particulares. Los clientes TOP representan menos del 2% de los clientes.
<p align="center">
<img src="/images/11_segment.png" alt="Analisis AVProductInstalled" width="500">
</p>

Con respecto al salario, siendo este el indicador de los ingresos de la unidad familiar, la mayoria se encuentran entre los 30K y 90K.

<p align="center">
<img src="/images/15_salario.png" alt="Analisis AVProductInstalled"  width="500">
</p>

Por Comunidad Autónoma, la mayoría de clientes son de Madrid, seguidos de Andalucia y Cataluña, mientras que las ciudades con mas clientes por orden son Madrid, Barcelona, Valencia y Murcia.

<p align="center">
<img src="/images/10_dist_geo_treemap.png" alt="Analisis AVProductInstalled">
</p>

Analizando el entry_chanel, disponiendo la empresa de 64 canales de entrada, el 44% de los clientes entran por un único canal y de manera acumulada el 95% del todas de clientes entran por 7 canales y el 99% por 11.
<p align="center">
<img src="/images/19_entry_channel_treemap.png" alt="Analisis AVProductInstalled">
</p>


## Análisis variación clientes.
Ponemos ahora el foco en el número de clientes que hay en cada una de las particiones para ver la evolución a lo largo de las 17 particiones. Lo primero que nos llama la antención es el incremento que hay el mes de Julio, seguido por los 4 siguientes meses, así como el número de bajas del mes de Enero 2019.

<table>
  <tr>
    <td><img src="/images/1_conteo_clientes_particion.png" alt="Analisis AVProductInstalled"></td>
    <td><img src="/images/3_ganados_vs_perdidos.png" alt="Analisis AVProductInstalled"></td>
    <td><img src="/images/9_perdidos.png" alt="Analisis AVProductInstalled"></td>
  </tr>
</table>
Si analizamos las nuevas altas con respecto al número de productos que contratan al alta, vemos que hay un incremento en el porcentaje de altas sin contratación de productos a lo largo de las 17 particiones que tenemos, partimos de un 5% llegando en la última partición al 60%.

El mes de Julio aparte de haber un incremento en las altas nuevas, casi el 80% de estas no estaban asociadas a la contratación de ningún producto.

Entendemos que se lanzó una campaña de captación de clientes potenciales para poder posteriormente venderles algún producto.

<p align="center">
  <img src="/images/4_altas_por_total_prod_contr.png" alt="Análisis AVProductInstalled" width="400">
</p>

Eliminado del analisis las altas que no contratan ninguno de los productos, podemos ver como desde los meses de Julio a Noviembre ha habido una mayor cantidad de contratación de productos al darse de alta. Entre el 90 y 95% de las nuevas incorporaciones con contratacion la hacen contratando únicamente un producto. El producto mayormente contratado al darse de alta es el em_acount (producto estrella).

<p align="center">
<img src="/images/5_analisis_prod_contratados_al_alta.png" alt="Analisis AVProductInstalled" width="800">
</p>
<p align="center">
<img src="/images/6_zoom_analisis_prod_contratados_al_alta.png" alt="Analisis AVProductInstalled" width="500">
</p>


Al pasar a ver la evolucion o popularidad de productos al alta podemos sacar las sigueintes conclusiones:
- Los depositos han perdido popularidad a la hora de darse de alta. Podemos ver como el short_term_deposit no se ha contratado en los últimos 6 meses al darse de alta y la bajada del long_term_deposit, donde en los tres ultimos meses a penas hay contrataciones.
- Hay productos que nunca se han contratado al darse de alta (em_account_pp, em_account_p, mortage y loans) y otros que a penas se han contratado (funds, securities y emc_account).
- Hay una tendencia a la baja de los productos payroll, pension_plan y payroll_account, mostrando un comportamiento identico el payroll y el pension_plan (deben de ser productos que se contratan a la par).
- Las contrataciones de la credit_card caen hasta ser algo insignificante.
- La debit_card tambien muestra una ligera tendencia descendente en las contrataciones al alta.
- em_account es la protagonista de este negocio, en los meses de Julio a Noviembre ha habido una explosión de contrataciones al darse de alta, manteniendo a lo largo del tiempo una tendencia estable.

<p align="center">
<img src="/images/7_tendencia_prod_al_alta.png" alt="Analisis AVProductInstalled">
</p>







