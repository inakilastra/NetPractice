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

<table>
    <thead>
        <tr>
            <th>Clase</th>
            <th>Bits iniciales</th>
            <th>Intervalo (*)</th>
            <th>N.º de redes</th>
            <th>N.º de direcciones por red</th>
            <th>N.º de hosts por red(‡)</th>
            <th>Máscara de red</th>
            <th>Dirección de broadcast</th>            
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>A</td>
            <td>0</td>
            <td>0.0.0.0 (**) - 127.255.255.255 (†)</td>
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