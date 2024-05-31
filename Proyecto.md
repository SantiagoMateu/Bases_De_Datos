Información: El gobierno ha implementado que cada familia debe tener los siguientes productos como mínimo e indispensable para tener una alimentación básica.

2 paquetes de arroz “Luccheti” de 500gr, el cual cuesta 2030 pesos por unidad.
3 aceites “Natura” de 1.5lt, con un valor de 3260 pesos por unidad.
1 paquete de azúcar “Ledesma” de 1kg, con un valor de 1349 pesos por unidad.
3 paquetes de polenta “Arcor” de 730gr, con un valor de 1868 pesos por unidad
4 latas de arvejas “Campagnola” de 300gr, con un valor de 1095 pesos por unidad


 PRODUCTOS                                                                        
|---------------------------------------------------------------------------------|
|PRO_ID|PRO_Nombres|PRO_Marcas_ID|PRO_Unidades de Medida_ID|PRO_Pesos_ID|PRO_Valor|
|------|-----------|-------------|-------------------------|------------|---------|
|  1   |Arroz	   |     1	     |            2            |	 1      |  2030   |
|  2   |Aceite	   |     2	     |            3	           |     2	    |  3260   |
|  3   |Azúcar	   |     3	     |            1	           |     3	    |  1349   |
|  4   |Polenta	   |     4	     |            2	           |     4	    |  1868   |
|  5   |Lata de A  |     5	     |            2            |	 5	    |  1095   |
-----------------------------------------------------------------------------------

 STOCKS                                           
|-------------------------------------------------|                                  
| STO_ID | STO_PRO_ID | STO_SDS_ID | STO_Cantidad |
|--------|------------|------------|--------------|
|  1     |     1      |     1      |     1000     |
|  2     |     2	  |     1	   |     400      |
|  3     |     3      |     2	   |     300      |
|  4	 |     4 	  |     3	   |     250      |
|  5	 |     5	  |     2	   |     300      |
|--------|------------|------------|--------------|

 MARCAS                
|----------------------|          
| MAR_ID | MAR_Nombres |
|--------|-------------|
|   1	 |  Lucchetti  |
|   2	 |  Natura     |
|   3	 |  Ledesma    |
|   4	 |  Arcor      |
|   5	 |  Campagnola |
|--------|-------------|

 PESOS    
|----------------------|             
| PES_ID | PES_Números |
|--------|-------------|
|   1	 |     500     |
|   2	 |     1.5     |
|   3	 |     1       |
|   4 	 |     730     |
|   5	 |     300     |
|--------|-------------|

 UNIDADES_DE_MEDIDA
|---------------------|
| UDM_ID | UDM_Nombres|
|--------|------------|
|   1	 | Kilogramos |
|   2	 | Gramos     |
|   3	 | Litros     |
|--------|------------|

 SUCURSALES_DE_SUPERMERCADO
|--------|.............|
| SDS_ID | SDS_Nombres |
|--------|-------------|
|   1	 |  Bolívar    |
|   2	 |  Olavarría  |
|   3	 |  Junín      |
|--------|-------------|

PRO_Nombres: Es un tipo de Dato “Varchar”
PRO_Marcas_ID: Es un tipo de Dato “Numérico”
PRO_Unidades_De_Medida_ID: Es un tipo de Dato “Numérico”
PRO_Pesos_ID: Es un tipo de Dato “Numérico”
PRO_Valor: Es un tipo de Dato “Numérico”

Mar_Nombres: Es un tipo de Dato “Varchar”
PES_Numeros: Es un tipo de Dato “Numérico”
UDM_Nombres: Es un tipo de Dato “Varchar”

SDS_Nombres: Es un tipo de Dato “Varchar”


CONSULTAS DE SQL

SELECT PRO_ID, PRO_Nombres 
FROM PRODUCTOS 
WHERE PRO_ID in 1

PRODUCTOS
| PRO_ID | PRO_Nombres |
| 1	     | Arroz       |

SELECT PRO_Nombres, MAR_Nombres
FROM PRODUCTOS PRO, MARCAS MAR
WHERE PRO.PRO_MAR_ID = MAR,MAR_ID

| PRO_Nombres |	MAR_Nombres |
| Arroz	      | Lucchetti   |

UPDATE SUCURSAL_DE_SUPERMERCADOS
SET SDS_Nombres = Tandil
WHERE SDS_ID = 3

| SDS_ID | SDS_Nombres |
| 3	     | Tandil      |

INSERT INTO STOCKS (STO_PRO_ID, STO_SDS_ID, STO_Cantidad) Values ( 6,6,3,500 )

| STO_ID | STO_PRO_ID | STO_SDS_ID | STO_Cantidad |
|   6	 |     6	  |      3	   |     500      |

DELET FROM SUCURSALES_DE_SUPERMERCADO 
WHERE SDS_ID = 1

SUCURSALES_DE_SUPERMERCADO
| SDS_ID | SDS_Nombres |
| 1	     | Bolívar     |
