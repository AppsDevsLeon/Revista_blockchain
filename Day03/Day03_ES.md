## **Firmar y Verificar una Transacción**

Vamos a hablar sobre la firma de transacciones, las claves privadas y otros aspectos de la criptografía, porque en el blockchain que se muestra a continuación vemos transacciones fantásticas, pero ¿cómo sabemos que fue Darcy quien envió 25 dólares a Bingley? ¿Cómo sabemos que realmente sucedió? Aquí es donde todas esas piezas que acabamos de aprender en nuestra testnet y en nuestra cuenta de Metamask cobrarán vida.

![Transaction](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day03/Images/b1.png)

**Claves Públicas y Privadas**

Aquí tenemos un ejemplo de claves públicas y privadas.

![Public_Private_Key](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day03/Images/b2.png)

**Clave privada:** Solo es conocida por el titular de la clave y se utiliza para *firmar* transacciones.

Realmente debes mantenerla en secreto, ya que la usarás como una especie de contraseña secreta para todas las transacciones.

Puedo elegir cualquier clave privada que desee utilizando el `Algoritmo de Firma Digital de Curva Elíptica` para Ethereum y Bitcoin. Ambos utilizan este algoritmo de firma digital de curva elíptica. Es una variante del algoritmo de firma digital y generará su propia clave pública.

Con esa clave pública, queremos que todos tengan acceso a ella; el mundo entero puede verla.

Utilizaremos la clave privada como una contraseña para, entre comillas, firmar digitalmente las transacciones, y luego las personas podrán verificarlas usando esta clave pública.

Veamos cómo se ve esto.

**Firmas**

Si vamos a la pestaña de firmas y, por ejemplo, tenemos el mensaje "hola mundo", lo que sucederá es que la clave privada que creamos se usará para firmar estos datos ("hola mundo") mediante un algoritmo de firma digital, generando así la firma del mensaje.

![Message_Signature](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day03/Images/b3.png)

Lo poderoso de cómo funciona este algoritmo es que puedes crear la firma del mensaje con tu clave privada, pero nadie más puede derivar tu clave privada a partir de la firma. Esto es lo que lo hace realmente, realmente poderoso.

Sin embargo, si verificamos usando nuestra clave pública, cualquiera puede comprobar que la firma es tuya.

![Message_Verification](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day03/Images/b4.png)

**Transacciones**

Si alguien intenta falsificar una transacción, tendrá que verificar su firma contra mi clave pública, y muy fácilmente se pondrá en rojo porque no se verifica.

Podemos aplicar lo mismo a las transacciones de forma idéntica.

![Transaction_verification](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day03/Images/b5.png)

Si quisiera enviar 20 dólares de mi cuenta a otra utilizando mi clave privada, podría firmar esa transacción y cualquiera en el mundo podría verificarla. Por eso se dice que debes proteger tus claves.

Tu dirección de Ethereum es una parte de tu clave pública. Para obtener nuestra dirección en Ethereum, simplemente tomamos la clave pública que hemos generado con nuestra clave privada, la hasheamos usando el mismo algoritmo de hash de Ethereum y tomamos los últimos 20 bytes. Así se deriva nuestra dirección.

Conocer la metodología exacta para obtener la dirección no es tan relevante, ya que puede variar de un blockchain a otro; solo ten en cuenta que, esencialmente, así se derivan la mayoría de estas direcciones.

*Nota: Esto no es la forma en que se envía la transacción. Esto solo la firma y crea una transacción lista para enviar. Más adelante aprenderemos cómo enviar estas transacciones.*

---

## **Los conceptos son los mismos**

Ahora que conocemos todas las piezas de criptografía, los detalles de cómo funciona el blockchain, cómo operan nuestras firmas y cómo todo se integra, hablemos un poco sobre cómo funciona esto en la práctica y qué está sucediendo.

Para muchos de estos aspectos, cada blockchain tiene algoritmos, métricas y criterios ligeramente diferentes para realizar estas operaciones. Por lo tanto, cuando hablamos de implementaciones específicas, ten en cuenta que el algoritmo exacto puede variar un poco, pero los conceptos siguen siendo los mismos. El hashing y las funciones hash son iguales sin importar dónde mires. Un blockchain descentralizado es similar en esencia sin importar la implementación, aunque la forma de implementarlo pueda variar.

Tradicionalmente, cuando ejecutas una aplicación, ya sea un sitio web o algo que se conecta a un servidor, interactúas con una entidad centralizada, a diferencia de lo que sucede en un blockchain con múltiples peers. Es operado por un único grupo centralizado. Aunque se ejecute en varios servidores, todos están controlados por el mismo grupo central. Como vimos, el blockchain funciona en una red de nodos independientes. Cuando observamos el peer A, el peer B, el peer C, etc., esos son ejemplos de distintos usuarios independientes ejecutando la tecnología blockchain en su nodo.

### **Nodo**

“Nodo” aquí se refiere a una instancia única de un sistema descentralizado. Cuando hablo de un nodo individual en un blockchain, me refiero a uno de esos peers (A, B, C, etc.) que ejecutan el software del blockchain. Es decir, un servidor ejecutando esta tecnología. La red es la combinación de estos nodos interactuando entre sí lo que crea el blockchain completo.  
Lo que hace a estos nodos tan potentes es que cualquiera puede unirse a la red, razón por la cual son descentralizados. La barrera de entrada consiste en algunos requisitos de hardware. Cualquiera puede unirse y participar, lo que los hace verdaderamente descentralizados. De hecho, puedes ir a GitHub ahora mismo y ejecutar tu nodo de Ethereum en pocos segundos.

### **Entidad Centralizada vs. Blockchain Descentralizado**

En el mundo tradicional, las aplicaciones son operadas por entidades centralizadas, y si esa entidad falla, es sobornada maliciosamente o decide apagarse, pueden hacerlo porque controlan todo.  
La tecnología blockchain, en cambio, no tiene este problema. Si un nodo o una entidad que opera varios nodos falla, no importa, ya que hay muchos nodos independientes en funcionamiento. El blockchain y el sistema persistirán mientras haya al menos un nodo activo. Afortunadamente, la mayoría de las cadenas populares como Bitcoin y Ethereum cuentan con miles de nodos. Como vimos en nuestra demostración, si un nodo actúa de forma maliciosa, los demás lo ignorarán, lo expulsarán o incluso lo sancionarán en algunos sistemas, ya que pueden comparar fácilmente sus nodos y detectar cuál está fuera de sincronía con la mayoría; y sí, la mayoría manda en el blockchain.

### **Las transacciones están registradas**

Cada blockchain mantiene una lista completa de cada transacción e interacción que ha ocurrido en él, y vimos que si un nodo intenta actuar maliciosamente, sus hashes quedarán desincronizados y no coincidirán con los de los demás. Esto confiere al blockchain una propiedad inmutable increíblemente potente, en la que nada puede modificarse o corromperse.

En esencia, podemos pensar en un blockchain como una base de datos descentralizada. Y en el caso de Ethereum, además tiene la capacidad de realizar cálculos de manera descentralizada.

### **Consenso**

Cuando recorrimos el ejemplo del blockchain y utilizamos la función de minería, vimos lo que se conoce como `proof of work` (prueba de trabajo). La prueba de trabajo y la prueba de participación (proof of stake) entran dentro del paraguas del consenso, y el consenso es un tema realmente importante en el mundo blockchain.

El consenso se define como el mecanismo utilizado para alcanzar un acuerdo sobre el estado o un valor único en el blockchain, especialmente en un sistema descentralizado. Mencioné brevemente este mecanismo en nuestro ejemplo al decir que si uno cambia algo y los otros dos no, la mayoría prevalecerá y expulsará al que cambió; esto es parte del mecanismo de consenso.

De manera muy general, un protocolo de consenso en un blockchain se puede desglosar en dos partes:

- `Algoritmo de Selección de Cadena`
- `Mecanismo de Resistencia a Sybil`

#### **Prueba de Trabajo / Mecanismo de Resistencia a Sybil**

La parte de minería que realizamos, o el algoritmo de prueba de trabajo, es lo que se conoce como un mecanismo de resistencia a Sybil, y es lo que actualmente utilizan Ethereum y Bitcoin.  
La prueba de trabajo se conoce como mecanismo de resistencia a Sybil porque define una forma de determinar quién es el autor del bloque: qué nodo realizó el trabajo para encontrar la solución (minería) y, por lo tanto, es el autor del bloque, permitiendo que los demás nodos verifiquen su exactitud.

### **Resistencia a Sybil**

La Resistencia a Sybil es la capacidad de un blockchain para defenderse de usuarios que crean una gran cantidad de identidades seudónimas para obtener una influencia desproporcionadamente ventajosa en el sistema. En términos sencillos, es la forma en que el blockchain se protege contra la creación de nodos falsos que permitan acumular cada vez más recompensas.  
Existen dos tipos de resistencia a Sybil de los que hablaremos aquí: POW (Prueba de Trabajo) y POS (Prueba de Participación).

### **POW**

En POW, el sistema es resistente a ataques Sybil porque un único nodo debe pasar por un proceso computacionalmente costoso llamado minería, que demostramos anteriormente para encontrar un nonce que haga que el hash comience con cuatro ceros (aunque cada blockchain puede variar el enigma o el problema).  
Esto funciona porque, sin importar cuántas cuentas seudónimas crees, cada una debe realizar esta costosa operación de encontrar la respuesta al problema de prueba de trabajo.

**Tiempo de Bloque**

Algunos blockchains hacen que este enigma sea intencionalmente difícil o fácil de resolver, lo que se conoce como tiempo de bloque. El tiempo de bloque es el intervalo entre la publicación de bloques y es proporcional a la dificultad de los algoritmos. Estos problemas pueden variar según lo largo que se desee que sea el tiempo entre bloques.  
Si el sistema quiere que el tiempo de bloque sea muy largo, hará el problema muy difícil, y viceversa. Más adelante hablaremos de ataques civiles y cómo pueden afectar el sistema, pero con POW es verificable quién es el autor del bloque, proporcionando resistencia ante comportamientos maliciosos.

### **Regla de Selección de Cadena**

Ahora es necesario combinar esto con la regla de selección de cadena para crear el consenso. Algunos protocolos de consenso tienen más características, pero de manera muy general hay dos elementos a considerar. El segundo es la regla de selección de cadena: ¿cómo determinamos cuál es el blockchain real y auténtico?

#### **Consenso Nakamoto**

Bitcoin y Ethereum utilizan una forma de consenso llamada `Consenso Nakamoto`, que es una combinación de POW y la regla de la cadena más larga. La red descentralizada decide que el blockchain que tenga la cadena más larga o el mayor número de bloques será el que se utilice. Esto tiene sentido, ya que cada bloque adicional que falte requiere cada vez más capacidad computacional para ponerse al día, de ahí las confirmaciones en las transacciones.

#### **Confirmaciones de Bloque**

El número de confirmaciones corresponde a la cantidad de bloques adicionales que se añaden después de que nuestra transacción se incluyó en un bloque. Por ejemplo, si vemos dos confirmaciones, significa que el bloque donde se realizó la transacción tiene dos bloques posteriores en la cadena más larga.  
Cabe señalar que, aunque muchas personas usan POW como sinónimo de protocolo de consenso, en realidad POW es solo una parte del protocolo de consenso general, que en el caso actual de Bitcoin y Ethereum es el Consenso Nakamoto.

### **Recompensas de Bloque y Tarifas de Transacción**

`Esto ha cambiado recientemente con la EIP 1559.`

POW también determina a dónde van las tarifas de transacción y las recompensas de bloque. ¿Recuerdas cómo realizamos la transacción? Hablamos del gas y de la tarifa de transacción. Entonces, ¿quién recibe el pago? ¿Quién obtiene la transacción y cuánto de la tarifa va a los mineros o validadores?  
En una red POW, se les llama mineros; en POS, se les llama validadores. Son un poco diferentes, y profundizaremos en eso cuando hablemos de POS.

En este sistema POW, todos los nodos compiten por ser los primeros en encontrar la solución al enigma del blockchain (en nuestro ejemplo, encontrar un hash que comience con cuatro ceros).  
Todos los nodos se esfuerzan por ser el primero, porque el primer nodo en resolver el problema recibirá la tarifa de transacción, es decir, se le pagará por ello.

Cuando un nodo recibe el pago, lo hace de dos maneras:  
- **Tarifas de transacción**  
  (Recuerda cómo hablamos de cambiar el precio del gas; esa es la tarifa que se paga a los nodos del blockchain por incluir la transacción).  
- **Recompensa de Bloque**  
  Probablemente hayas oído hablar de la reducción a la mitad de Bitcoin, en la que la recompensa de bloque se reduce a la mitad aproximadamente cada cuatro años. Esta recompensa incrementa la cantidad en circulación de la criptomoneda que se otorga (por ejemplo, en Ethereum se otorga en Ethereum y en Bitcoin en Bitcoin).

Así, estos nodos compiten para ser los primeros en resolver el problema y, de ese modo, ganar tanto la recompensa de bloque como la tarifa de transacción. En algunos blockchains, como Bitcoin, en cierto momento dejarán de otorgar recompensas de bloque y los nodos solo recibirán tarifas de transacción.

Las tarifas de gas son pagadas por quien inicia la transacción. Cuando obtuvimos fondos del faucet, algunos servidores pagaron la tarifa por nosotros. Sin embargo, cuando enviamos ether de una cuenta a otra, la cuenta remitente pagó la tarifa.

En POS también existe una tarifa de gas, pero se paga a los validadores en lugar de a los mineros, y hablaremos de eso en breve.

Ahora hablemos de dos tipos de ataques que pueden ocurrir en el mundo blockchain.

**Ataque Sybil**

El Ataque Sybil ocurre cuando un usuario crea muchas cuentas seudónimas para intentar influir en una red. Obviamente, en Bitcoin y Ethereum esto es muy difícil, ya que el usuario debe realizar todo ese trabajo en POW o aportar una gran cantidad de colateral en POS, de lo cual hablaremos más adelante.

**Ataque del 51%**

Como vimos en el protocolo de consenso, los blockchains acuerdan que la cadena más larga es la que se utiliza, siempre que represente al menos el 51% del resto de la red. Esto significa que, si tienes la cadena más larga y controlas más del 51% de la red, puedes realizar una bifurcación (fork) y forzar a la red a seguir tu cadena.  
Como mencioné, los ataques Sybil ocurren cuando una entidad intenta hacerse pasar por múltiples nodos, y es muy difícil lograrlo en POW y POS.

### **Regla de la Cadena Más Larga**

Ahora se puede ver que los blockchains son muy democráticos: el que tenga mayor respaldo y sea el más largo es el que el sistema utilizará. Cuando los nodos producen un nuevo bloque y lo añaden a la cadena más larga, los demás nodos seguirán esa cadena y agregarán esos bloques a su propia cadena. Cuando se selecciona un bloque de una cadena diferente y se reemplaza por otro bloque para continuar, es común que se produzcan reorganizaciones muy pequeñas.

Sin embargo, si un grupo de nodos alcanza el 51% del poder de la red, podría influir en la dirección que tome el sistema, lo que se conoce como un ataque del 51%. Esto ha ocurrido, por ejemplo, en blockchains como Ethereum Classic (que no es Ethereum). Por eso, cuanto más grande es un blockchain, más descentralizado y seguro se vuelve.

### **Desventajas del POW**

POW es fantástico porque nos permite proteger fácilmente contra ataques Sybil y mantener nuestros blockchains descentralizados y seguros. Sin embargo, tiene algunas desventajas. POW consume mucha electricidad porque cada nodo trabaja a máxima velocidad para ganar la carrera por las recompensas, lo que genera un impacto ambiental considerable.  
Desde la implementación de POW y el Consenso Nakamoto, muchos otros protocolos han tomado esta idea y han optado por mecanismos de resistencia a Sybil más ecológicos, siendo el más popular el POS.

#### **Prueba de Participación / Mecanismo de Resistencia a Sybil**

Algunas cadenas ya están utilizando el protocolo de Prueba de Participación (POS) y se encuentran activas y en crecimiento. Ejemplos de estas son `Avalanche`, `Solana`, `Polygon`, `Polkadot`, `Terra` y, además, Ethereum ha decidido actualizarse a ETH2, que también utilizará este algoritmo de POS.  
Es un mecanismo de resistencia a Sybil diferente. En lugar de resolver un problema computacionalmente difícil, los nodos en POS aportan un colateral (realizan staking) que garantiza que se comportarán de forma honesta. En el caso de Ethereum2, los nodos aportan Ethereum como garantía. Si se portan mal, serán penalizados (slash) o perderán parte del colateral. Esto hace que sea muy difícil crear muchas cuentas anónimas, ya que para cada una se debe aportar un stake, y si se actúa de manera incorrecta, se corre el riesgo de perder todo el dinero aportado.

**Validadores**

En POS, los mineros se llaman `validadores` porque ya no se dedica a la minería, sino que validan las transacciones de otros nodos. A diferencia de POW, donde cada nodo compite por ser el primero en encontrar un bloque, en POS se elige aleatoriamente a un nodo para proponer el nuevo bloque, y el resto de los validadores comprueba si la propuesta es honesta.  
Como vimos en la lección de criptografía, generalmente es muy sencillo para otros nodos verificar si una propuesta o transacción es legítima.

### **Aleatoriedad**

Este es un tema muy importante cuando hablamos de blockchains, ya que estos sistemas son deterministas y están aislados del mundo exterior. Por definición, un sistema determinista no puede tener números aleatorios. Entonces, ¿cómo elegimos los validadores de forma aleatoria?  
La respuesta varía de un blockchain a otro. En ETH2, por ejemplo, se utiliza un método denominado "aleatorio" (al menos en la implementación original). Se trata de una organización autónoma descentralizada que elige colectivamente el número aleatorio y decide, en conjunto, qué nodo será el siguiente en operar.

### **Pros y Contras de POS**

POS también tiene sus ventajas y desventajas.  
**Pros:**  
- Es un excelente mecanismo de resistencia a Sybil y permite determinar de forma efectiva quién debe ser el autor de un bloque.  
- Requiere mucho menos gasto computacional para generar un nuevo bloque, ya que, en lugar de que todos los nodos compitan, solo uno es responsable de proponerlo y el resto se limita a validarlo.

**Contras:**  
- Se considera que la red es algo menos descentralizada debido a los costos iniciales del staking, lo que implica un gasto para participar. Esto abre un debate filosófico sobre cuán descentralizado debe ser un sistema, algo que la comunidad deberá definir.  
- No obstante, el consenso entre los ingenieros blockchain es que POS es muy descentralizado y seguro. La mejora en el impacto ambiental, que puede reducirse hasta en un 99%, es una de las dos razones principales por las que Ethereum se está migrando a ETH2.

### **Problema de Escalabilidad y Solución de Sharding**

- **Escalabilidad**

Cuando hablamos de tarifas de gas, nos referimos a que estas pueden aumentar considerablemente si muchas personas desean enviar transacciones, ya que un bloque tiene un espacio limitado y los nodos solo pueden añadir cierta cantidad de transacciones. Por lo tanto, cuando muchas personas quieren usar el blockchain, el precio del gas se dispara. Esto no es muy escalable, ya que se vuelve cada vez más costoso utilizar el blockchain a medida que más usuarios intentan incluir sus transacciones en los bloques. Existe, en cierto modo, un límite en la cantidad de usuarios que pueden utilizar el sistema debido a las restricciones financieras impuestas por el aumento de las tarifas de gas. ETH2 no solo aborda el impacto ambiental de POW al migrar a POS, sino que también implementa una nueva metodología llamada `Sharding`.

- **Sharding**

El sharding es una solución a este problema de escalabilidad. Un blockchain con sharding significa que se trata de un blockchain de blockchains. Existe una cadena principal que coordina varias cadenas conectadas a ella. Esto implica que hay más cadenas disponibles para que las personas realicen transacciones, lo que aumenta efectivamente el espacio de bloque. El sharding puede incrementar enormemente la cantidad de transacciones en una capa 1 de blockchain.  
Además, existe el concepto de *Layer 1*, que se refiere a cualquier implementación base de blockchain, como Bitcoin o Ethereum.

### **Capa 1 y Capa 2**

- **Capa 1:** Se refiere a cualquier implementación base de blockchain, por ejemplo, Bitcoin o Ethereum.  
- **Capa 2:** Es cualquier aplicación que se añade sobre la Capa 1, construida encima del blockchain. Ejemplos de Capa 2 son Chainlink, Arbitrum u Optimism. Arbitrum y Optimism son especialmente interesantes, ya que son soluciones de Capa 2 que buscan resolver el problema de escalabilidad y se conocen como `Rollups`.

### **Rollups**

Arbitrum y Optimism agrupan sus transacciones en una Capa 1, como Ethereum. No entraremos en demasiados detalles sobre cómo funcionan los rollups, pero lo importante es saber que un rollup es similar a una `cadena shardizada`. Ellos derivan su seguridad de la capa base (Layer 1) como Ethereum y envían en bloque sus transacciones a dicha capa. Resuelven algunos de los problemas de escalabilidad al ofrecer otra cadena en la que se pueden realizar transacciones, manteniéndose siempre anclados a la seguridad de la capa base. A diferencia de las *side chains*, que derivan su seguridad de sus propios protocolos, los rollups obtienen su seguridad de la capa base. Por ello, por ejemplo, Arbitrum y Optimism son casi tan seguros como Ethereum.

---

### **Resumen**

- BTC y ETH son blockchains de Prueba de Trabajo que siguen el Consenso Nakamoto.
- ETH2 será un blockchain shardizado de Prueba de Participación.
- Los ataques Sybil se previenen gracias a protocolos como POW y POS.
- Un ataque del 51% se vuelve cada vez más difícil a medida que el blockchain crece.
- El consenso es la forma en que los blockchains deciden cuál es el estado de la cadena.
- El sharding y los rollups son soluciones a los problemas de escalabilidad en la Capa 1.
- Una Capa 1 es cualquier implementación base de blockchain, como Bitcoin o Ethereum.
- Un problema de escalabilidad en el blockchain es la falta de espacio en los bloques para el número de transacciones, lo que lleva a tarifas de gas muy elevadas.
- Las tarifas de gas indican cuánto cuesta interactuar con un blockchain.
