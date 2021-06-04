# variacion_base_monetaria
(A precio constante)

En este proyecto utilizo conexión a las APIS de BCRA y DATOS.GOB.AR para obtener los siguientes datos:

1 - Base Monetaria: https://api.estadisticasbcra.com <br>
2 - Indice de Precios al Consumidor: https://datos.gob.ar/series/api/series/?ids=148.3_INIVELNAL_DICI_M_26

NOTA: En el caso del BCRA utilizo una token propio por lo que deberán cambiar este dato para poder replicar el código.

Los pasos seguidos para lograr el cálculo de la variación monetaria a precio constante son los siguientes:

Antes de empezar se observa en la documentacion del IPC que el mes base es Diciemnbre 2016 = 100. Entonces tomamos esta fecha como inicio.

1 - Bajar datos de la base monetaria del BCRA <br>
2 - Transformar esta información a valor mensual (tomando como referencia el valor promedio) <br>
3 - Bajar datos del IPC desde datos.gob.ar <br>
4 - Transformar datos de IPC para poder concatenar con la base monetaria <br>
5 - Join <br>
6 - Calcular la variación: (BM / IPC) * 100 <br>
7 - Graficar

Finalmente obtenemos el siguiente gráfico como resultado.

OBSERVACIÓN: En la serie de IPC hay 12 valores nulos

<img src="/grafico.png"/>
