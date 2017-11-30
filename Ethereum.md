Que es ethereum?
================
Ethereum es una *blockchain que permite ejecutar programas* en su ambiente seguro.

Al final, *Etherem* es una *maquina virtual*, llamada EVM. Esta EVM permite
verificar y ejecutar codigo en la blockchain con la garatia que se ejecutara en
cada nodo. Este codigo esta en *smart contracts (contratos inteligentes)*

Ademas de rastrear el balance de cuentas, *Ethereum* mantiene el estado de la
EVM en la blockchain. Todos los nodos procesan smart contracts para verificar
la integridad de los contratos y sus salidas.


Que es un Smart Contract?
=========================
*Un SC es codigo que se ejecuta en la EVM*.
Un SC puede aceptar y almacenar: ether, datos o una combinacion de ambos.
Entonces, usando logica programada en el contrato, este puede distribuir ether
a otras cuentas o incluso otros SC.

Ejemplo:

Bob y Alice.
Alice quiere contratar a Bob para construir su patio.
Y usan un contrato de fideicomiso: almacenan el dinero en un lugar hasta que
una condicion se cumple.
(Entre las clausulas del contrato podría incluirse código liberando la garantía
de Bob a Alice si Bob no construye el patio o si realizara un mal trabajo).

*SC se es escriben en un Lenguaje de programacion llamado Solidity*.

Redes Ethereum
==============
Hasta ahora hemos descripto la blockchain publica de Ethereum, la principal
llamada *MainNet* o *Red principal*.  En esta red, los datos de la cadena
(incluyendo, balance de cuentas y transacciones) son publicos y cualquiera
puede crear un node y verificar transacciones. En esta red el *Ether* tiene un
valor de mercado y hay una taza de cambio contra otras cryptomonedas o monedas
fiat como dolares estado unidenses.

Pero hay otras redes, de hecho cualquiera puede crear su propia red ethereum.

Red local de prueba
-------------------
Esta red es para simular una red ethereum y se usa principalmente para desarrollo.
La mas recomendada es ethereumJS testRPC.

Redes publicas de prueba
------------------------
Desarrolladores suelen usar redes publicas de prueba (o testnets) para probar
aplicaciones ethereum antes del final release a la MainNet. El *ether* en estas
redes es usado solo para propositos de prueba y no tienen valor.

Hay 3 que son ampliamente usadas:
- Ropsten: la red oficial de testing y es una replica de la MainNet.
- Kovan: Una red que usa una prueba de concenso llamada: *proof of authority* o
  *prueba de autoridad*. Y significa que las transacciones son validadas por un
  grupo selecto de miembros, lo que lleva a un tiempo de bloque de 4 segundos.
  El proveedor de *ether* en esta red de prueba, entrega ether de forma
  controlada para mitigar ataques de spam.
- Rinkeby: Una red creada por la ethereum foundation que usa *proof of authority*.

Redes Privadas/Empresariales
----------------------------
Estas redes permiten a las partes compartir datos sin dar acceso publico. Suelen ser una buena opcion para:
- Compartir datos sensitivos, ejemplo: historias clinicas
- Escalar para manejar un rendimiento mas alto en las operaciones de
  lectura/escritura, debido al tama~no mas chico de la red.

DAPPS o aplicaciones distribuidas
---------------------------------
Son aplicaciones que usan smart contracts para su procesamiento.
La interfaz se hace en HTML, CSS, y Javascript y la aplicacion misma puede
almacenarse en un servidor tradicional o en un sistema de archivos
desentralizado como swarm o ipfs.

