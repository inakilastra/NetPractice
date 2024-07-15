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

Clase	Bits iniciales	Intervalo (*)	N.º de redes	N.º de direcciones por red	N.º de hosts por red(‡)	Máscara de red	Dirección de broadcast
A	0	0.0.0.0 (**) - 127.255.255.255 (†)	128	16 777 216	16 777 214	255.0.0.0	x.255.255.255
B	10	128.0.0.0 - 191.255.255.255	16 382	65 536	65 534	255.255.0.0	x.x.255.255
C	110	192.0.0.0 - 223.255.255.255	2 097 150	256	254	255.255.255.0	x.x.x.255
D (Multicast)	1110	224.0.0.0 - 239.255.255.255	 	 	 	 	 
E (experimental)	1111	240.0.0.0 - 255.255.255.254	 	 	 	 	 

<table>
    <thead>
        <tr>
            <th>Column 1</th>
            <th>Column 2</th>
            <th>Column 3</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td rowspan=4 align="center">R1 Text</td>
            <td rowspan=2 align="center">R2 Text A</td>
            <td align="center">R3 Text A</td>
        </tr>
        <tr>
            <td align="center">R3 Text B</td>
        </tr>
        <tr>
            <td rowspan=2 align="center">R2 Text B</td>
            <td align="center">R3 Text C</td>
        </tr>
        <tr>
            <td align="center">R3 Text D</td>
        </tr>
    </tbody>
</table>