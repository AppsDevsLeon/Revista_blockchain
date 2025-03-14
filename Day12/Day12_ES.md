## **Hash, Hashing y SHA-256**

Antes de comenzar, debemos entender qué es exactamente un hash y, más específicamente, el hash SHA-256. Un hash se asemeja a una secuencia aparentemente aleatoria de números y letras, actuando como una huella digital única de datos digitales específicos.

## ¿Qué es SHA-256?

SHA-256 (Secure Hash Algorithm 256-bit) es una función criptográfica que genera una cadena única y fija de 256 bits (32 bytes), generalmente representada en hexadecimal con 64 caracteres. Este algoritmo genera valores exclusivamente dentro del rango hexadecimal, es decir, números del 0-9 y letras de la A hasta la F.

Antes de continuar, echemos un vistazo más profundo al hash SHA256. Un hash luce como un montón de números aleatorios y funciona como una huella digital de información digital específica.

Por ejemplo, el siguiente hash inicia con `e3b0`, y es la representación del hash SHA-256 cuando no hay ningún dato (un valor vacío):

![Metamask](Images/a18.png)

Si escribimos cualquier texto en una caja, como por ejemplo la palabra `blockchain`, el hash generado cambia completamente:

![Metamask](Images/a19.png)

Este hash específico para la palabra "blockchain" es:

```
ef7797e13d3a75526946a3bcf00daec9fc9c9c4d51ddc7cc5df888f74dd434d1
```

Si modificamos ligeramente el texto original, por ejemplo cambiando la última letra a mayúscula `blockchaiN`, el hash generado es totalmente diferente:

```
6cfa1dbb6eb068b5050efee9f90a954fb0896e5c97e84713bfe023b9408c2cef
```

Podrías escribir toneladas y toneladas de texto y siempre obtendrás un hash del mismo tamaño. Ya sea una pequeña cantidad de información, ninguna información o una biblioteca completa del Congreso, siempre obtendrás un hash con la longitud mostrada anteriormente. Nunca podrás adivinar cuál será el hash. Siempre tendrás el mismo hash sin importar cuántas veces ingreses la misma información.

## Propiedades Matemáticas del SHA-256

SHA-256 utiliza un procedimiento matemático riguroso que involucra operaciones lógicas y aritméticas como:

- **Operaciones de bits**: AND, OR, XOR, NOT
- **Desplazamientos de bits**: rotaciones y desplazamientos hacia la derecha
- **Adiciones módulo 2³²**: suma binaria con desbordamiento controlado (mod 2³²)

El algoritmo procesa los datos en bloques de 512 bits (64 bytes). Cada bloque se divide en 16 palabras de 32 bits, que se expanden a 64 palabras mediante un proceso de expansión y mezcla matemática que incrementa la seguridad y la aleatoriedad aparente del resultado final.

Estas operaciones aseguran la alta seguridad del algoritmo SHA-256, haciéndolo resistente a ataques criptográficos conocidos.

## Propiedades Importantes del SHA-256

- **Longitud fija:** Siempre 256 bits, representados como 64 caracteres hexadecimales (0-9 y A-F).

- **Determinista:** La misma entrada siempre producirá el mismo hash.

- **Unidireccional:** No es posible revertir un hash para recuperar los datos originales.

- **Resistente a colisiones:** Es prácticamente imposible encontrar dos entradas diferentes que generen el mismo hash.

## Efecto Avalancha

SHA-256 tiene una característica llamada **efecto avalancha**. Este efecto significa que un pequeño cambio en los datos originales generará un hash totalmente diferente e impredecible. Esto es crucial para garantizar la integridad y seguridad.

Por ejemplo:
- Texto original: `blockchain`
  - Hash: `ef7797e13d3a75526946a3bcf00daec9fc9c9c4d51ddc7cc5df888f74dd434d1`
- Texto modificado: `blockchaiN`
  - Hash: `6cfa1dbb6eb068b5050efee9f90a954fb0896e5c97e84713bfe023b9408c2cef`

Esta propiedad hace imposible alterar datos sin cambiar radicalmente el resultado del hash, garantizando integridad en múltiples aplicaciones tecnológicas actuales.

## Aplicaciones del SHA-256

SHA-256 es ampliamente usado en:

- Blockchain (Bitcoin, Ethereum, etc.)
- Verificación de integridad de archivos
- Almacenamiento seguro de contraseñas
- Firmas digitales

La importancia de SHA-256 radica en la combinación de rapidez y seguridad que ofrece en un sinfín de aplicaciones tecnológicas actuales.


