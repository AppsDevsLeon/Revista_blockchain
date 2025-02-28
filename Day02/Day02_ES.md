## **Una Transacción en Vivo de Ethereum**

Lo primero que necesitaremos es una *billetera de Ethereum*. Así que ve a `Metamask`, ya que es una de las billeteras más populares y fáciles de usar. Descarga la billetera; se instalará como una pequeña extensión en la esquina superior derecha de tu navegador. De esta manera, podrás ver fácilmente en cualquier momento lo que tienes en tu billetera. Adelante, instala Metamask.

**Creación de la Billetera**

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a1.png)

Vamos a crear una billetera completamente nueva, así que haz clic en "create a wallet". Si ya tienes una billetera, puedes importarla mediante una frase semilla.

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a2.png)

Ahora vamos a crear nuestra contraseña y asegurarnos de que sea segura. Si deseas utilizar una cuenta y poner Ethereum real y dinero real en ella, necesitas hacer una copia de seguridad.

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a3.png)

Esto es solo una demostración, pero si le muestras esta frase secreta a otra persona, tendrá acceso a todos tus fondos. Así que, para todo lo que vamos a hacer, utilizaremos dinero ficticio.

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a4.png)

Presiona confirmar y verás un par de consejos. Recuerda tomarlos en serio, especialmente si vas a usar la cuenta con dinero real.

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a5.png)

Podemos ver la interfaz de usuario de esta billetera y, si miras en tus extensiones, puedes anclarla en tu navegador; incluso basta con hacer clic para obtener la misma interfaz.

Nuestra frase mnemotécnica, obtenida a partir de esa frase secreta, nos ha dado acceso a una nueva cuenta.

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a6.png)

**Etherscan**

Para la dirección de nuestra cuenta, podemos usar una herramienta como `Etherscan`.

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a7.png)

Si observamos esta dirección que acabamos de crear, podemos ver que no se han realizado transacciones. Está vacía. Tiene cero ether y, por lo tanto, ningún valor en dólares. La dirección anterior es única y representa exclusivamente la cuenta que acabamos de crear.

**Cuentas Múltiples**

Incluso podemos hacer clic en el círculo para crear más cuentas y asignarles un nombre diferente.

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a8.png)

La cuenta 2 tendrá una dirección diferente.

**Claves Públicas y Privadas, así como Mnemónicos**

El mnemónico que se nos ha dado nos permite crear múltiples cuentas con el mismo mnemónico. Tener ese mnemónico nos dará acceso a cada cuenta que se haya creado con él. Por eso, asegurar tu mnemónico es tan crucial, especialmente si creas múltiples cuentas diferentes. Cada cuenta también tiene un identificador único asociado: la dirección de la cuenta es la dirección pública. Sin embargo, también existe una clave privada para trabajar con esa cuenta, una clave secreta. Podemos verla haciendo clic en los tres puntos, yendo a los detalles de la cuenta y exportando la clave privada.

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a9.png)

Esta es una contraseña única asociada a esta cuenta. Si le das acceso a alguien a esta clave privada, tendrá acceso a la cuenta 2. No tendrá acceso a mi cuenta 1, ya que la clave privada de la cuenta 2 está asociada únicamente a esa cuenta. Sin embargo, el mnemónico está asociado a todas las cuentas.

**Mnemónico vs Clave Privada vs Clave Pública**

Por eso, cuando la gente dice “guarda tus claves en un lugar seguro”, se refieren tanto a las claves privadas como a los mnemónicos. Si pierdes tu clave privada, perderás el acceso a esa cuenta. Si pierdes tu mnemónico, pierdes el acceso a todas tus cuentas.

**Mainnet y Testnets**

¿Qué más está pasando en Metamask? Podemos ver una sección que dice `Ethereum Mainnet`. Si haces clic, verás varias otras redes.

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a10.png)

Cuando compras ETH y trabajas con él, estás operando en la red principal de Ethereum (Mainnet). Cuando interactúas con contratos inteligentes o DEFI, trabajarás en la Mainnet con valor real. Sin embargo, como somos ingenieros, muchas veces querrás probar tus aplicaciones, hacer pruebas de integración o simplemente asegurarte de que tu código funcione. Por ello, también existen las testnets. Estas redes se parecen a Ethereum y funcionan de la misma manera, pero no utilizan dinero real y son solo para probar aplicaciones. Incluso podemos ir a `Rinkeby Etherscan` y ver el `Rinkeby Testnet Explorer`. Buscamos nuestra dirección y obtenemos la misma información exacta.

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a11.png)

Más adelante te mostraremos cómo trabajar con otras cadenas compatibles con EVM. Por ahora, no te preocupes por el significado de “compatible con EVM”; podemos trabajar con Avalanche, Polygon y otras a través de interfaces de red.

**Iniciando Nuestra Primera Transacción**

Vamos a realizar nuestra primera transacción en la Testnet de Rinkeby, lo cual simulará exactamente cómo es hacer la transacción en la red principal de Ethereum.

Vamos a ir a una aplicación llamada `Rinkeby Faucet`. Aquí es donde haremos nuestra primera transacción. Rinkeby será una de las dos testnets con las que trabajaremos; la otra será `Kovan`. Es importante saber cómo cambiar entre testnets y cadenas compatibles con EVM, por lo que trabajaremos con ambas. Por ahora, nos enfocamos únicamente en Rinkeby.

`Faucet` es una aplicación de testnet que nos da Ethereum de prueba de forma gratuita. Por ello, no tiene valor, ya que cualquiera puede obtenerlo gratis a través de estos faucets. Para obtener Ethereum de testnet en faucet.rinkeby.io, debemos publicar un tweet o una entrada en Facebook con ese tweet.

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a12.png)

Después del tweet, copiaremos el enlace del tweet y lo pegaremos en Rinkeby Faucet, luego haremos clic en “Give me ether” (18.75 ether/3 días).

Si tomamos la dirección de la cuenta y vamos a Rinkeby Etherscan, veremos que el saldo es de 18.75.

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a13.png)

Pero si miramos en `Ethereum Mainnet` no tenemos nada allí. Acabamos de completar nuestra primera transacción. Y si actualizamos la página, también podemos ver que esta fue la primera transacción realizada. Algunas cuentas nos enviaron 18.75 ether. Incluso podemos ver los detalles de la transacción.

**Detalles de la Transacción**

Etherscan es lo que se conoce como un `Block Explorer`. Un Block Explorer es una aplicación que nos permite ver fácilmente los detalles de lo que sucede en un blockchain. Podemos ver los detalles de la transacción que realizamos, y cada vez que trabajemos con un `Smart Contract` también veremos detalles similares.

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a14.png)

Podemos ver la información de arriba. Observamos un `hash de transacción` único. Este hash o identificador único identifica de manera exclusiva esta transacción.

Podemos ver el número de bloque, el cual veremos en un momento.

También observamos esta cuenta única, que es la cuenta del faucet.

**Tarifas de Gas, Tarifas de Transacción, Límite de Gas, Precio del Gas**

“Gas” se refiere a la tarifa pagada a los operadores de nodos por incluir exitosamente una transacción en un blockchain. Ahora bien, la forma exacta en que funciona esto cambiará muy pronto, pero el concepto es que cada vez que deseas cambiar el estado del blockchain –ya sea enviando algo de Ethereum o realizando cualquier otro tipo de transacción– debes pagar un poco de Ethereum o un poco del token nativo del blockchain para ejecutar esa transacción. Cada acción en el blockchain cuesta gas, y si realizas una operación que requiera mucha energía para el blockchain, costará más gas. Por ejemplo, si envío una transacción única, costará 21,000 gas. Sin embargo, si envío una transacción que invoque la función de un contrato inteligente y realice muchas otras operaciones, costará más gas. Vemos aquí que quien nos envió ETH también pagó a los mineros o validadores del blockchain un poco de Ethereum para incluir nuestra transacción. Nosotros elegimos cuánto de tarifa queremos enviar con nuestras transacciones.

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a15.png)

**Gas vs Precio del Gas vs Límite de Gas vs Tarifa de Transacción**

¿Por qué querríamos pagar más por gas? ¿Por qué siquiera tengo la opción de pagar más?

Un blockchain solo puede procesar cierta cantidad de transacciones a la vez, y los nodos del blockchain tienen una capacidad limitada. Así que, cuando realizas una transacción, un nodo debe decidir por qué incluirla en el bloque. Si hay muchas personas intentando realizar transacciones, los nodos estarán altamente incentivados a elegir aquellas transacciones que les ofrezcan una tarifa más alta.

**Estimador de Gas**

Pudimos obtener el estimador de gas del blockchain en ethgasstation.info.

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a16.png)

Actualmente, indica que si deseas que tu transacción se procese de inmediato, te costará 81 wei; si quieres que se procese en menos de 5 minutos, te costará alrededor de 62 wei.

Así, el precio del gas en Ethereum fluctúa según cuántas personas lo utilicen, y lo mismo ocurre con las demás cadenas.

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a17.png)

Por lo general, cuando configuras el precio del gas en una transacción, puedes revisar tu "gas station" para ver el precio según tus necesidades, aunque todo depende de cuántas personas estén utilizando el blockchain al mismo tiempo.

La razón de estos precios es que los nodos solo pueden incluir una cantidad limitada de transacciones en un bloque, por lo que están incentivados a elegir aquellas transacciones que les ofrezcan tarifas más altas. Así, cuando muchas personas usan un blockchain, los precios serán muy altos; cuando pocas lo hagan, los precios serán muy bajos.

Con esta información, ya sabes cómo interactuar con blockchains y con el protocolo de Ethereum. Así, si no deseas aprender a programar, puedes comenzar a interactuar con Ethereum y sus protocolos utilizando solo esta información.

Echemos un vistazo bajo el capó de Ethereum para ver qué sucede con estas transacciones, con el gas y con los blockchains. Aprendamos todos los fundamentos de la tecnología blockchain.

## **Cómo Funciona el Blockchain / Qué Sucede Dentro del Blockchain**

**Hash o Hashing o SHA256**

Antes de comenzar, necesitamos observar esto que llamamos hash SHA256. Un hash parece un montón de números aleatorios y es la huella digital de algún dato.

El hash de abajo comienza con `e3b0`, que es el hash de la nada.

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a18.png)

Resulta que es la huella digital de lo que sea que escriba en esta caja. Si escribo el texto “blockchain” en esta caja, puedes ver que el hash cambia.

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a19.png)

Este es el hash del texto “blockchain” en minúsculas, que comienza con 5318. Si borro el texto y lo escribo nuevamente, obtendré el mismo hash. Es la `huella digital` del texto “blockchain”.

Podrías escribir toneladas de texto y siempre obtendrías un hash. Lo interesante es que, ya sea que haya muy poca información, ninguna o incluso toda la Biblioteca del Congreso, siempre obtendrás un hash tan largo como el mostrado arriba. No podrás adivinar cuál es; siempre obtendrás el mismo hash sin importar cuántas veces ingreses la misma información.

**Bloque**

Extendamos la idea de un hash a algo que llamaremos un bloque.

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a20.png)

Este es un bloque, y es muy similar al hash. Solo que la sección de datos se ha dividido en tres partes: una llamada “block” (bloque), que es simplemente un número o el número del bloque; un “nonce”, que es otro número; y más datos, muy similar a lo que teníamos antes. Sin embargo, el hash de este bloque incluye toda la información mostrada en la figura anterior, la cual comienza con cuatro ceros. Es un hash relativamente inusual, ya que la mayoría no comienza con cuatro ceros como el de arriba. Este caso sí lo hace y, dado que es arbitrario, podemos decir que el bloque está firmado.

Entonces, ¿qué pasaría si cambiara cualquier información en el bloque de arriba?

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a21.png)

El hash anterior ya no comenzará con cuatro ceros y el fondo se volverá rojo. Ahora sabemos que este bloque, con esa información, no es válido ni está firmado, y ahí es donde entra el `Nonce`. Este número es simplemente un valor que puedes modificar para intentar encontrar uno que haga que el hash vuelva a comenzar con cuatro ceros.

Arriba puedes ver el botón `mine` (minar). Cuando hago clic en él, el sistema recorre todos los números a partir del 1 para encontrar uno cuyo hash comience con cuatro ceros; a este proceso se le llama minería.

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a22.png)

Se detuvo en 64,658 y ese hash resulta comenzar con cuatro ceros, cumpliendo la definición de un `bloque firmado`.

**Blockchain**

Un blockchain es simplemente la cadena de estos bloques. ¿Cómo se unen? Hagámoslo.

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a23.png)

Al igual que antes, el bloque número 1 no tiene bloque previo. Aunque hay una sección de datos, tiene un campo `Prev` que en el primer bloque es simplemente un conjunto de ceros.

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a24.png)

El campo `prev` del bloque 2 muestra “0000ae”, que es el hash del bloque anterior (en este ejemplo, del bloque 4). Cada bloque apunta hacia el bloque que lo precede. Recuerda que en el primer bloque no hay bloque anterior, por lo que su campo prev es simplemente un conjunto de ceros; es un número ficticio.

Al igual que hicimos antes, ¿qué pasa si cambio alguna información en el bloque 5?

Cambiará el hash de ese bloque y lo invalidará.

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a25.png)

¿Qué pasaría si cambiara algo en el bloque 4?

Cambiará el hash, pero ese nuevo hash se copiará en la sección del hash previo del bloque 5, alterando también el bloque 5. Es decir, se romperán ambos bloques.

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a26.png)

Podemos retroceder hasta el punto que queramos en el pasado y romper ese bloque, y se romperán todos los bloques posteriores. Todo lo anterior estaba en verde.

Si quisiera cambiar algo en el blockchain, podría ir al bloque número 5 y modificarlo. Luego, podría re-minarlo y elegir un nonce diferente. Esencialmente, se puede alterar el cambio.

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a27.png)

¿Qué pasaría si retrocedo en el tiempo y rompo el bloque 3?

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a28.png)

Ahora necesito minar el bloque 3, eligiendo un nonce que haga que su hash comience con cuatro ceros, pero los bloques 4 y 5 seguirán rotos. Aunque el bloque 3 empiece con cuatro ceros, al combinar esos ceros con diferentes datos en el campo prev del bloque 4, el hash de este último seguirá siendo incorrecto. Por lo tanto, también debo minar los bloques 4 y 5, respectivamente.

Lo que quiero decir es que si cambio el último bloque, solo necesito re-minarlo. Pero si retrocedo y cambio un bloque anterior, debo minar todos los bloques posteriores. Cuantos más bloques retrocedas, más difícil será realizar un cambio. Así es como un blockchain resiste la mutación y el cambio.

`¿Cómo sé que mi blockchain ha sido re-minado?`

**Blockchain Descentralizado/Distribuido**

Echemos un vistazo al `Blockchain Distribuido`.

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a29.png)

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a30.png)

Se ve exactamente igual que el blockchain anterior, pero cada uno tiene un peer diferente. Puedes ver que el Peer B tiene la misma estructura que el Peer A. La lista podría continuar indefinidamente. Hay muchos peers en internet, y todos tienen una copia completa del blockchain.

Si miro el hash del bloque 5 del Peer A, comienza con "0000e4", y si miro el bloque 5 del Peer B, también comienza con "0000e4". Deben ser idénticos.

Si escribo algo en el bloque 4 del Peer B y vuelvo a minar los bloques 4 y 5...

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a31.png)

Todos los bloques en el Peer B aparecen en verde. Sin embargo, la cadena del Peer A muestra que el último hash comienza con "0000e4", el Peer C muestra "0000e4", pero el intermedio muestra "00004c". Así, con solo echar un vistazo al hash del Peer B, se nota que algo anda mal en él, a pesar de que todos sus hashes empiezan con cuatro ceros. Esencialmente, se trata de un voto de dos contra uno: el Peer A dice "0000e4", el Peer B "00004c" y el Peer C "0000e4". Por ello, "0000e4" prevalece. Así funciona una copia completamente distribuida: tener una copia en muchas computadoras permite ver rápidamente si todos los bloques son idénticos. Dado que los blockchains pueden tener entre 400,000 y 500,000 bloques, en lugar de revisarlos todos, basta con mirar el hash del bloque más reciente para saber si algo en el pasado ha sido alterado.

**Tokens / Historial de Transacciones**

Eso es todo. No hay nada más, pero resulta poco útil porque en esa sección de datos no hay nada que tenga significado real. Se sigue escribiendo texto irrelevante. Entonces, lo que queremos es un `token`. Hagamos un token en nuestro blockchain.

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a32.png)

Los tokens anteriores son arbitrarios, es decir: 25 dólares de "Darcy" a "Bingle", 4.27 de "Elizabeth" a "Jane". Básicamente, son todas las transacciones que se están realizando. Se reemplazaron los datos con estas transacciones y, como vimos antes, hay múltiples bloques. No importa cuántas transacciones existan. Si vamos a otros peers, notamos que tenemos copias idénticas de esos bloques. Ahora es cuando la inmutabilidad es importante. Si cambio algo en el bloque 4 del Peer A, el hash del último bloque será totalmente diferente del hash del último bloque de los otros peers. Si retrocedo en el tiempo y cambio algunos valores, se notará. Ese es el objetivo de usar el blockchain para resistir cualquier modificación en el pasado.

No estamos llevando un registro de que "Darcy" tenga 100 dólares y que le envíe 25 a "Bingle". Solo indicamos que "Darcy" transfiere 25 a "Bingle". No almacenamos el saldo de una cuenta bancaria, sino únicamente los movimientos de dinero. Esto plantea la pregunta: “¿Tiene Darcy 25 dólares?”

Tenemos un problema en esta versión del blockchain: no sabemos si Darcy realmente tiene 25 dólares. Así que observemos una transacción de `Coinbase`.

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a33.png)

Coinbase añadirá una transacción de coinbase a nuestros bloques. Esto significa que vamos a generar 100 dólares de la nada y asignárselos a "Anders", sin que exista una transacción previa en el bloque, ya que nadie tenía dinero antes.

En el siguiente bloque, otros 100 dólares salen de la nada y se asignan a "Anders". Ahora tenemos transacciones y todas provienen de "Anders", ya que es el único que tiene dinero en ese momento. "Anders" envía 10 de sus dólares a "Sophie". ¿`Tiene "Anders" 10 dólares? Sí, porque la transacción de coinbase le otorgó 100 dólares. Sumando todas las transacciones que "Anders" realiza, no se exceden de 100, cumpliendo con una regla básica de la moneda: no se puede crear dinero de la nada; su emisión está controlada.

![Metamask](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a34.png)

Si observamos el blockchain que hemos creado y avanzamos en el tiempo, notamos que "Jackson" envía 2 dólares a "Alexa". ¿Tiene Jackson 2 dólares? Retrocedemos un bloque y vemos que "Emily" recibió 10 dólares de "Anders" y se los transfirió a "Jackson". Así que Jackson sí tiene el dinero. Este es uno de los beneficios de tener un historial en el blockchain: es fácil retroceder.

**Resumen**

- Ethereum funciona con Keccak256.
- Un hash es una cadena única de longitud fija para identificar un dato.
- Un algoritmo hash es una función que convierte datos en un hash único.
- La minería es el proceso de encontrar una “solución” al “problema” del blockchain.
- Los nodos reciben pago por minar bloques.
- Un bloque es una lista de transacciones minadas juntas.
- Los blockchains son descentralizados y distribuidos porque muchos usuarios independientes ejecutan el software de blockchain y se verifican entre sí para detectar comportamientos honestos o maliciosos.
- El nonce es un “número utilizado una sola vez” para encontrar la solución al problema del blockchain.
- El nonce también se usa para definir el número de transacción de una cuenta o dirección.
