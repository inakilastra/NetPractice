# NetPractice

## <h2>Teoria</h2>

<h3>TCP</h3>

TCP (del inglés Transmission Control Protocol), es uno de los protocolos fundamentales de Internet. 

El protocolo TCP es, al igual que los protocolos UDP y SCTP, un protocolo de Internet que está ubicado en la capa de transporte del modelo OSI. 
El objetivo de TCP es crear conexiones dentro de una red de datos compuesta por redes de computadoras para intercambiar datos. Además, en cuanto a su funcionamiento, garantiza que los datos llegarán a destino sin errores y en el mismo orden en el que fueron transmitidos.

También proporciona un mecanismo para distinguir distintas aplicaciones dentro de una misma máquina, a través del concepto de puerto.

TCP da soporte a muchas de las aplicaciones más populares de Internet (navegadores, intercambio de ficheros, clientes FTP, etc.) y protocolos de aplicación (HTTP, SMTP, SSH y FTP).

<h3>IP</h3>

Una dirección IP (del inglés, Internet Protocol) es una etiqueta numérica que identifica de manera lógica y jerárquica a una interfaz —habitualmente un dispositivo (computadora, laptop, teléfono inteligente)— conectada a la red, que utilice el protocolo de internet o que corresponda al nivel de red del modelo TCP/IP.1​ En principio se usa en la red global, aunque también para aplicaciones locales (como la identificación de un router en una red cerrada).

Una dirección IP tiene dos funciones principales: identificación de la interfaz de red y direccionamiento para su ubicación.

Una dirección IP es un número de 32 bits que a su vez esta divido en 4 bloque de 8 bits 	 	 


<h4>CLASES DE DIRECCIONES  IPV4</h4>

> Existen cinco clases de direcciones IP y el primer octeto determina la clase:
>
> - CLASE A - Soporta redes en Internet grandes.
>             Red . Host . Host . Host
>             Primer octeto 0 - 127 /8
>             Mascara 255.0.0.0
> - CLASE B - Soporta redes en Internet moderadas
>             Red . Red . Host . Host
>             Primer octeto 128 - 191  /16
>             Mascara 255.255.0.0
> - CLASE C - Soporta redes en internet pequeñas.
>             Red . Red . Red . Host
>             Primer octeto 192 - 223 /24
>             Mascara 255.255.255.0
> - CLASE D - Soporta Redes Multicast
>             Primer octeto 224 - 239
> - CLASE E - Sin uso. Redes experimentales.
>             Primer octeto 240 - 255

<table>
    <thead>
        <tr>
            <th>Clase</th>
            <th>Bits iniciales</th>
            <th>Intervalo (*)</th>
            <th>N.º de redes</th>
            <th>N.º de direcciones por red</th>
            <th>N.º de hosts por red(****)</th>
            <th>Máscara de red</th>
            <th>Dirección de broadcast</th>            
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>A</td>
            <td>0</td>
            <td>0.0.0.0 (**) - 127.255.255.255 (***)</td>
            <td>128</td>
            <td>16 777 216</td>
            <td>16 777 214</td>
            <td>255.0.0.0</td>
            <td>x.255.255.255</td>
        </tr>
        <tr>
            <td>B</td>
            <td>10</td>
            <td>128.0.0.0 - 191.255.255.255</td>
            <td>16 382</td>
            <td>65 536</td>
            <td>65 534</td>
            <td>255.255.0.0</td>
            <td>x.x.255.255</td>
        </tr>
        <tr>
            <td>C</td>
            <td>110</td>
            <td>192.0.0.0 - 223.255.255.255</td>
            <td>2 097 150</td>
            <td>256</td>
            <td>254</td>
            <td>255.255.255.0</td>
            <td>x.x.x.255</td>
        </tr>
        <tr>
            <td>D (Multicast)</td>
            <td>1110</td>
            <td>224.0.0.0 - 239.255.255.255</td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td>E (experimental)</td>
            <td>1111</td>
            <td>240.0.0.0 - 255.255.255.254</td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
        </tr>                                
    </tbody>
</table>
(*) La dirección que tiene los bits de host iguales a 0 sirve para definir la red en la que se ubica. Se denomina dirección de red. La dirección que tiene los bits correspondientes a host iguales a 1,1​ sirve para enviar paquetes a todos los hosts de la red en la que se ubica. Se denomina dirección de broadcast.<br />
(**) La dirección 0.0.0.0 es reservada por la IANA para identificación local.<br />
(***) Las direcciones 127.x.x.x se reservan para designar la propia máquina. Se denomina dirección de bucle local o loopback.<br />
(****) La primera dirección se reserva para identificar la red (p.ej. 18.0.0.0), mientras que la última dirección se emplea como dirección de difusión o broadcast (p.ej. 18.255.255.255). Ese es el motivo por el que el número máximo de hosts en una red es siempre igual al número de direcciones disponibles en un rango específico menos dos.

<h3>Mascara subred</h3>

La Máscara determina el número de subredes.

Una clase A con Máscara 255.0.0.0 tiene una unica red con hasta 16.777.214 Host 2 ^24 - 2 (reservados 0 y 255)

Si queremos crear subredes, ejemplo:
Máscara 255.0.0.0  11111111.0000000.00000000.00000000

Si usamos 4 bits del segundo octeto
11111111.**1111**000.00000000.00000000

se crean 16 subredes
2 ^4 = 16 y la Máscara pasa a ser: 255.240.0.0<br />
Cada una de esas subredes tiene menos capacidad de Hosts

Ejemplo de clase C
IP       192.168.168.0<br />
BINARIO  11000000.10101000.10101000.00000000<br />
MASCARA  255.255.255.0<br />
BINARIO  11111111.11111111.11111111.00000000<br />
Bits de Host 2 ^8 = 256<br />

Creamos 8 subredes<br />
MASCARA  255.255.255.224<br />
BINARIO  11111111.11111111.11111111.11100000<br />
Bits de Host 2 ^3 = 8<br />
Subredes Creadas<br />
IP       192.168.168.0<br />	
BINARIO  11000000.10101000.10101000.00000000<br />
IP       192.168.168.32	<br />
BINARIO  11000000.10101000.10101000.00100000<br />
IP       192.168.168.64	<br />
BINARIO  11000000.10101000.10101000.01000000<br />
IP       192.168.168.96<br />
BINARIO  11000000.10101000.10101000.01100000<br />
IP       192.168.168.128<br />
BINARIO  11000000.10101000.10101000.10000000<br />
IP       192.168.168.160<br />
BINARIO  11000000.10101000.10101000.10100000<br />
IP       192.168.168.192<br />
BINARIO  11000000.10101000.10101000.11000000<br />
IP       192.168.168.224<br />
BINARIO  11000000.10101000.10101000.11100000<br />

En el caso de esta última subred<br />
HOST     192.168.168.225<br />
BINARIO  11000000.10101000.10101000.11100001<br />
...<br />
HOST     192.168.168.254<br />
BINARIO  11000000.10101000.10101000.11111110<br />



Conversión Binario, Decimal y Hexadecimal

Sistema Binario ( Base 2 )
{ 0, 1 }
Sistema Decimal ( Base 10 )
{ 0, 1, 2, 3, 4, 5, 6, 7, 8, 9  }
Sistema Hexadecimal ( Base 16 )
{ 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F  }

Binario a Decimal
( Base 2 ) 10101010
<table>
    <thead>
        <tr>
            <th align="center">128</th>            
            <th align="center">64</th>
            <th align="center">32</th>
            <th align="center">16</th>
            <th align="center">8</th>
            <th align="center">4</th>
            <th align="center">2</th>
            <th align="center">1</th>            
        </tr>
    </thead>
    <tbody>
        <tr>
            <td align="center">1</td>
            <td align="center">0</td>
            <td align="center">1</td>
            <td align="center">0</td>
            <td align="center">1</td>
            <td align="center">0</td>
            <td align="center">1</td>
            <td align="center">0</td>
        </tr>                                
    </tbody>
</table> 

Sumamos los que son 1:
128 + 32 + 8 + 2 = 170

Min 0 Max 128 + 64 + 32 + 16 + 8 + 4 + 2 + 1 =  255

Decimal a Binario
( Base 10 ) 132
132 = 128 + 4
128  64  32  16   8   4   2   1
   1     0    0     0   0   1   0   0
<table>
    <thead>
        <tr>
            <th align="center">128</th>            
            <th align="center">64</th>
            <th align="center">32</th>
            <th align="center">16</th>
            <th align="center">8</th>
            <th align="center">4</th>
            <th align="center">2</th>
            <th align="center">1</th>            
        </tr>
    </thead>
    <tbody>
        <tr>
            <td align="center">1</td>
            <td align="center">0</td>
            <td align="center">0</td>
            <td align="center">0</td>
            <td align="center">0</td>
            <td align="center">1</td>
            <td align="center">0</td>
            <td align="center">0</td>
        </tr>                                
    </tbody>
</table>    
( Base 10 ) 236
236 = 128 + 64 + 32 + 8 + 4
<table>
    <thead>
        <tr>
            <th align="center">128</th>            
            <th align="center">64</th>
            <th align="center">32</th>
            <th align="center">16</th>
            <th align="center">8</th>
            <th align="center">4</th>
            <th align="center">2</th>
            <th align="center">1</th>            
        </tr>
    </thead>
    <tbody>
        <tr>
            <td align="center">1</td>
            <td align="center">1</td>
            <td align="center">1</td>
            <td align="center">0</td>
            <td align="center">1</td>
            <td align="center">1</td>
            <td align="center">0</td>
            <td align="center">0</td>
        </tr>                                
    </tbody>
</table>  

Conversion Hexadecimal
Paso 1 Convertir un caracter cada vez
Paso 2 Convertir a Decimal
Paso 3 Convertir a Binario

<table>
    <thead>
        <tr>
            <th align="center">Decimal</th>
            <th align="center">0</th>
            <th align="center">1</th>
            <th align="center">2</th>
            <th align="center">3</th>
            <th align="center">4</th>
            <th align="center">5</th>
            <th align="center">6</th>
            <th align="center">7</th>                         
            <th align="center">8</th>
            <th align="center">9</th>
            <th align="center">10</th>
            <th align="center">11</th>
            <th align="center">12</th>
            <th align="center">13</th>
            <th align="center">14</th>
            <th align="center">15</th>           
        </tr>
    </thead>
    <tbody>
        <tr>
            <th align="center">Hexadecimal</th>
            <th align="center">0</th>
            <th align="center">1</th>
            <th align="center">2</th>
            <th align="center">3</th>
            <th align="center">4</th>
            <th align="center">5</th>
            <th align="center">6</th>
            <th align="center">7</th>                         
            <th align="center">8</th>
            <th align="center">9</th>
            <th align="center">A</th>
            <th align="center">B</th>
            <th align="center">C</th>
            <th align="center">D</th>
            <th align="center">E</th>
            <th align="center">F</th>  
        </tr>                                
    </tbody>
</table>  
Hexadecimal
Ejemplo 
Hexadecimal F en Decimal es 15 en Binario 1111
<table>
    <thead>
        <tr>
            <th align="center">8</th>
            <th align="center">4</th>
            <th align="center">2</th>
            <th align="center">1</th>            
        </tr>
    </thead>
    <tbody>
        <tr>
            <td align="center">1</td>
            <td align="center">1</td>
            <td align="center">1</td>
            <td align="center">1</td>
        </tr>                                
    </tbody>
</table>  