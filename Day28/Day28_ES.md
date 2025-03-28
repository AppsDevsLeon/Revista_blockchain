
## **Algoritmos de consenso en blockchain: Proof of Work (PoW)**


Proof of Work o “Prueba de Trabajo” es el algoritmo de consenso más conocido en la actualidad y fue utilizado por primera vez en Bitcoin. PoW crea un mecanismo en el que los nodos mineros compiten para resolver complejos problemas matemáticos. 

El primer minero en resolver el problema tiene el derecho de proponer un nuevo bloque, que será añadido a la cadena de bloques una vez que haya sido validado por otros nodos. Este minero recibirá una recompensa en la criptomoneda nativa de la red por la creación o “minado” de este nuevo bloque. Además, también recibirá las tarifas de comisión de las transacciones que procesó en el bloque como parte de los incentivos por participar y asegurar la red. 

> “Un minero es un equipo hardware especializado que ejecuta un software de minería para procesar transacciones y validarlas para una red blockchain”

El algoritmo de consenso PoW asegura que solo las transacciones legítimas sean registradas en la cadena de bloques y, además, implementa la regla de la cadena más larga, que establece que la versión de la cadena de bloques con el mayor trabajo acumulado es la válida. 

A través de este mecanismo, la blockchain de Bitcoin logra la tolerancia a fallas bizantinas, proporcionando un sistema robusto que puede resistir ataques y mantener la integridad de las transacciones, previniendo el doble gasto y garantizando que todos los nodos converjan en una única versión de la red. 

**Las principales ventajas de PoW son:**

- Alto nivel de seguridad, debido a la gran cantidad de potencia computacional requerida para alterar la cadena o ejecutar ataques como el ataque de denegación de servicio distribuido (DDoS) o el ataque del 51%.
- Mantiene la descentralización, ya que fomenta la participación de múltiples mineros, ayudando a mantener la red descentralizada.
- Garantiza la inmutabilidad de las transacciones y previene el doble gasto.

No obstante, debido al tiempo y esfuerzo que se requiere para validar las transacciones, PoW puede enfrentar desafíos de escalabilidad y rendimiento.  

Además de Bitcoin, otras redes subsiguientes, como Litecoin y Monero, también utilizan el algoritmo de consenso Proof of Work para asegurar sus respectivos sistemas.  

---

## **El protocolo Proof of Work (PoW)**


El protocolo de Prueba de Trabajo, nos sirve para evitar ciertos comportamientos indeseados en una red. Su nombre proviene del inglés Proof of Work (PoW). Este protocolo funciona bajo el concepto de requerir un trabajo al cliente, que luego es verificado por la red. Normalmente el trabajo solicitado, consiste en realizar complejas operaciones de cómputo.

Estas operaciones que luego son verificadas por la red. Una vez que son aprobadas, se da acceso al cliente para que use los recursos de la misma. Con ello se busca impedir que clientes maliciosos puedan consumir todos los recursos de forma incontrolada. Una situación que puede acabar por denegar el servicio prestado al resto de clientes de la red.

Un ejemplo muy simple de entender es el famoso captcha que se pone cuando se quiere hacer un registro en una web. La web pone este reto que el visitante ha de resolver. Si lo resuelve tendrá acceso al servicio. Esto evita que un atacante pueda crear millones de registros y así colapsar la página web. No obstante, el reto en una comunicación entre ordenadores no puede ser tan complejo. Debe ser solventable, aunque con una complejidad relativa.

La principal característica de esta estrategia es su asimetría. El trabajo por parte del cliente es moderadamente difícil de realizar, pero la verificación por parte de la red es sencilla. Esto quiere decir, que la prueba de trabajo lleva mucho tiempo en producirse y es computacionalmente costosa. Pero verificarla es sencillo, pues la prueba diseña patrones que facilitan la verificación.

Fue precisamente esta característica, la que llamó la atención de Satoshi Nakamoto a la hora de diseñar el Bitcoin. Es por ello que implementó el sistema HashCash (un sistema PoW) en su reconocida criptomoneda.

---

## **¿Cómo funciona el protocolo PoW?**

El proceso que se lleva a cabo, se puede dividir en las siguientes grandes etapas:

**Etapa #1:** El cliente o nodo establece una conexión con la red. En este punto, la red le asigna una tarea computacionalmente costosa. Esta tarea debe ser resuelta a los fines de recibir un incentivo económico.

**Etapa #2:** Comienza la resolución del acertijo. Esto conlleva el uso de mucha potencia de computación hasta resolver el enigma entregado. Este proceso es el que recibe el nombre de minería.

**Etapa #3:** Una vez resuelta la tarea computacional, el cliente comparte esta con la red para su verificación. En este punto, se verifica rápidamente que la tarea cumpla con los requisitos exigidos. Si lo hace, se brinda acceso a los recursos de la red. En caso contrario, se rechaza el acceso y la solución presentada del problema. Es en este punto, donde se realizan las verificaciones de protección contra el doble gasto. Una protección que evita, que se presente más de una vez, una tarea ya asignada y verificada por la red.

**Etapa #4:** Con la confirmación que la tarea ha sido cumplida, el cliente accede a los recursos de la red. Gracias a esto, recibe una ganancia por el trabajo computacional realizado.

---

Son estas cuatro etapas, las que permiten y modelan el funcionamiento de la Prueba de Trabajo. La facilidad de este modelo permite trasladar el mismo a distinto software para aprovechar su potencial. Pero es en las blockchains donde observamos una mayor utilidad, brindando unos niveles de seguridad excepcionales a pesar de la baja complejidad del protocolo. Y al mismo tiempo, permite que millones de personas puedan participar de forma concurrente en la red.
