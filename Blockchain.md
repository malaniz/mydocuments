Blockchain
----------
Cada vez que surge algun concepto nuevo, tenemos que preguntarnos, porque? que
es? y como trabaja?

Porque usar una blockchain?
---------------------------
Las blockchains (o cadenas de bloques) son usadas cuando multiples partes
necesitan compartir datos y trasferir valor sin confiar entre ellas.
En la blockchain estas partes pueden estar en cualquier parte del mundo.

El mundo financiero describe esta confianza como el riesgo de contraparte:
>
> El riesgo de que la otra parte no cumpla su parte del contrato.
>
La blockchain elimina por completo el *riesgo de contraparte* a travez de un
sistema matematico:
>
> Criptografia y conexion distribuida p2p o peer to peer.
>

Antes de seguir, analicemos algunos puntos importantes de tecnologia.

1. *Bases de datos*, en 1960 emergieron los sistemas de bases de datos. Y estos
   se pensaron de manera centralizada y con esto queremos decir la ubicacion y
   el acceso a los datos es controlado por una autoridad central.

2. *Necesidad de compartir datos*, compartir grandes cumulos de datos es caro y
   complicado.

Que es una blockchain?
----------------------
Fundamentalmente, es *una blockchain es una base de datos compartida* que tiene
un *libro mayor sobre las transacciones* que se hacen en ella.

Como en un banco, el *libro mayor (ledger)* sigue el rastro de quien es due~no
de que fondos. Pero a diferencia de un banco, todos tienen una copia de ese
*ledger* y pueden verificar las cuentas de otros (y la propia por supuesto).
Cada copia del *ledger* se le llama *nodo*.

Ademas la blockchain elimina el problema de la confianza que afecta a las bases
de datos con las siguientes caracteristicas

- *Desentralizacion total*, leer/escribir a la base de datos es completamente
  descentralizado y seguro. Ninguna persona o grupo puede controlar toda la
  blockchain.

- *Tolerancia de fallos extrema*: la tolerancia a fallos es la capacidad de un
  sistema de lidear con datos corruptos. Y en su version extrema se refiere a
  que todas las cuentas comparten datos y validan los cambios.

- *Verificacion independiente*, las transacciones puede verificarse sin
  necesidad de un tercero y cualquiera puede hacerlas. Esto suele referirse
  como "des-intermediacion"

Como trabaja una blockchain?
----------------------------
Hora que tenemos una idea de porque las blockchains son utiles, veamos como trabaja.

Las *interacciones* entre *cuentas/accounts* en la red blockchain son llamadas
*transacciones*.  Estas transacciones pueden ser transacciones monetarias,
tales como enviar *ether, la criptomoneda usada en Ethereum*.  Tambien estas
transacciones pueden ser transmision de datos, tales como un comentario en un
blog. Un *grupo de transacciones* se le llama *Bloque o block*.

Cada *cuenta* en la red blockchain tiene una *firma unica*, que le hace saber
todos que cuenta inicia la transaccion. En una blockchain publica, cualquiera
puede leer o escribir datos. Leer el datos es gratis, pero escribir no lo es.
Este costo, es conocido como *gas* y su precio es en la criptomoneda de la red,
en nuestro caso *ether*. Esto ayuda a evitar spam y se paga para tener una red
segura.

Minado
------
Cualquier *nodo* de la red puede ayudar a *asegurar la red* con un proceso que
se le denomina *minado*.  Estos nodos compiten entre ellos por resolver un
problema matematico, los cuales le dan la seguridad a la red.

Este proceso necesita gran poder de computo, es por ello que *el minero*
ganador de la competencia es recompensados por su servicio. Esta recompensa
incentiva a los nodos a trabajar para asegurar la red y tambien incentiva a que
la seguridad de la red no estee en manos de un unico minero.
La recomponsa es en *ether*.

Hashing
-------
Una vez que se mina un nuevo bloque, se notifica a los otros mineros, comienza
el proceso de verificacion, y finalmente se agrega este nuevo bloque a sus
copias de la *cadena/chain* . Esto se hace a travez de hashing criptografico (o
simplemente, *hashing*). *Hashing* es un proceso "one-way", que toma un dato, y
devuelve un *string de longitud fija* que representa al dato.

Es importante notar que, el dato original no se puede reproducir desde su
*hash*, pero el mismo dato simpre va a reprodudir el mismo *hash*. Basicamente
es una funcion que no tiene una funcion inversa.
De esta manera, datos no verificados pueden ser *hashed* (convertirse a un
*hash*), y se comparan con el hash original. Si los datos son identicos,
entonces el dato es valido.

Una vez que mas de la mitad de los mineros validaron el nuevo bloque, la red se
dice que a *alcanzado un concenso* y el bloque vuelve parte permanente de la
blockchain. Ahora todos los nodos pueden bajar estos datos con la garantia de
que esta verificado.






