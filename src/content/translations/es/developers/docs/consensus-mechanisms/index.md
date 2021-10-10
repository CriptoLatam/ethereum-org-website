---
title: Mecanismos de consenso
description: Una explicación de los protocolos de consenso en los sistemas distribuidos y de su función en Etherum.
lang: es
sidebar: true
incomplete: true
---

Cuando se trata de blockchains como Ethereum (que, básicamente, son bases de datos distribuidas), los nodos de la red deben ser capaces de llegar a un acuerdo sobre el estado actual del sistema. Esto se consigue con ayuda de mecanismos de consenso.

A pesar de que no forma parte de la construcción de una dapp, entender los mecanismos de consenso te ayudará a explicar cuestiones que son importantes para ti y para la experiencia de tus usuarios, como los precios del gas y los tiempos de las transacciones.

## Requisitos previos {#prerequisites}

Para comprender mejor esta pagina, te recomendamos visitar nuestra [introducción a Ethereum](/developers/docs/intro-to-ethereum/).

## ¿Qué es un mecanismo de consenso? {#what-is-a-consensus-mechanism}

Los mecanismos de consenso (también conocidos como protocolos de consenso o algoritmos de consenso) permiten a los sistemas distribuidos colaborar y mantenerse seguros.

Durante décadas, estos mecanismos se han utilizado para establecer un consenso entre los nodos de la base de datos, los servidores de aplicaciones y otras infraestructuras empresariales. Durante los últimos años se han generado nuevos protocolos de consenso para permitir que sistemas criptoeconómicos, como Ethereum, realicen acuerdos sobre el estado de la red.

Un mecanismo de consenso en un sistema criptoeconómico también ayuda a prevenir ciertos tipos de ataques económicos. En teoría, un atacante puede comprometer el consenso mediante el control del 51% de la red. Los mecanismos de consenso están diseñados para hacer inviable este "ataque del 51%". Se han diseñado diferentes mecanismos para resolver este problema de seguridad de distintas formas.

<!-- ### Consensus -->

<!-- Formal requirements for a consensus protocol may include: -->

<!-- - Agreement: All correct processes must agree on the same value. -->
<!-- - Weak validity: For each correct process, its output must be the input of some correct process. -->
<!-- - Strong validity: If all correct processes receive the same input value, then they must all output that value. -->
<!-- - Termination: All processes must eventually decide on an output value -->

<!-- ### Fault tolerance -->
<!-- TODO explain how protocols must be fault tolerant -->

## Tipos de mecanismos de consenso {#types-of-consensus-mechanisms}

<!-- TODO -->
<!-- Why do different consensus protocols exist? -->
<!-- What are the tradeoffs of each? -->

### Prueba de trabajo {#proof-of-work}

Ethereum, al igual que Bitcoin, actualmente utiliza el protocolo de consenso de Prueba de trabajo (PoW, por sus siglas en inglés).

#### Creación del bloque {#pow-block-creation}

La Prueba de trabajo la realizan los [mineros](/developers/docs/consensus-mechanisms/pow/mining/), que compiten por crear nuevos bloques repletos de transacciones procesadas. El ganador comparte el nuevo bloque con el resto de la red y gana algunos ETH minados recientemente. El ganador de la carrera será el ordenador del minero que consiga resolver el rompecabezas con más rapidez; esto produce el enlace criptográfico entre el bloque actual y el anterior. La resolución de este rompecabezas es la tarea de la Prueba de trabajo.

#### Seguridad {#pow-security}

La red se mantiene segura por el hecho de que necesitarías el 51% de la potencia computacional de la red para defraudar a la cadena. Esto requeriría inversiones grandes en equipamiento y energía, que probablemente provocarían que gastaras más de lo que ganas.

Más información sobre la [Prueba de trabajo (PoW)](/developers/docs/consensus-mechanisms/pow/)

### Prueba de participación {#proof-of-stake}

Ethereum tiene planes de actualizarse para adoptar el protocolo de consenso de [Prueba de participación (PoS)](/developers/docs/consensus-mechanisms/pos/).

#### Creación de bloques {#pos-block-creation}

La Prueba de participación la realizan los validadores que hayan apostado ETH para participar en el sistema. Un validador se elige aleatoriamente para crear nuevos bloques, compartirlos con la red y obtener recompensas. En lugar de tener que realizar un trabajo informático intenso, bastará con que apuestes tus ETH en la red. Esto fomentará un comportamiento saludable de la red.

#### Seguridad {#pos-security}

El sistema de Prueba de participación se mantiene seguro, ya que sería necesario disponer del 51 % de los ETH apostados para defraudar al sistema. Y, además, la apuesta podría interrumpirse por comportamiento malicioso.

Más información sobre la [Prueba de participación (PoS)](/developers/docs/consensus-mechanisms/pos/)


#### Proof-of-Stake (PoS) {#proof-of-stake}

Este algoritmo de consenso nace como una alternativa al PoW y tiene como objetivo lograr un consenso distribuido. Fue usado por primera vez por Peercoin y fue creado en el 2011 luego de discutirse en un foro en Bitcointalk en ese mismo año.

Su funcionamiento difiere mucho del algoritmo anterior. En lugar de hacer que los mineros prueben que todas y cada una de las transacciones son legítimas, el Proof of Stake o Prueba de Participación o Estaca, requiere que una persona apueste, mantenga o bloquee monedas y valide la propiedad de las mismas. En pocas palabras, este algoritmo reemplaza la minería intensiva del PoW con un mecanismo donde los bloques se validan de acuerdo a la 'participación' de los involucrados.

Si bien hay diferentes formas en que se selecciona el nuevo creador de bloques para evitar la centralización por la cantidad de monedas que se pueden tener bloqueadas o en 'apuesta', en general, la cadena de bloques está asegurada por un proceso de selección pseudoaleatorio que considera la riqueza del nodo y la antigüedad de las monedas junto con un factor de aleatorización.

Existen muchas derivaciones de este algoritmo, entre las más resultantes tenemos: 

Prueba de Participación Anónima (PoSA): Cloakcoin, Spectrocoin

Prueba de Importancia (PoI): NEM

Prueba de Almacenamiento: Storj 

Prueba de Tiempo de Juego (PoST): Vericoin

Prueba de Velocidad de Estaca (PoSV): Reddcoin

Existen unas 415 monedas que usan este algoritmo en todas sus derivaciones, entre las más resultantes tenemos Binance Coin, Stellar, Dash, Neo, Cosmos, Ontology,  entre otras. En conjunto, este sector representa unos 9.27 Billones de dólares, un 3,52% del mercado en general.


#### Prueba de participación delegada (DPOS) {#dpos}

La Prueba de participación delegada (DPOS) es un mecanismo de consenso muy rápido y más conocido por su implementación en EOS y a menudo se lo conoce como democracia digital, gracias a su sistema de votación ponderado por estaca.

La forma en que funciona es que los usuarios votan por "delegados" a quienes se les da el poder de obtener ganancias al ejecutar un nodo completo. El peso de su voto depende de su participación o bloqueo de monedas. Dado que los delegados desean recibir la mayor cantidad de votos posible, se les incentiva constantemente a crear cosas valiosas para la comunidad, ya que es probable que reciban votos adicionales por hacerlo.

Se supone que este método es más eficiente y protege a los usuarios de interferencias regulatorias no deseadas. Sin embargo, su máximo exponente, EOS, ha sido objeto en las últimas semanas de una gran fuga de desarrolladores iniciales acusando al sistema de centralizado e inseguro.

Entre las más resultantes por supuesto tenemos a EOS, Tron, Cardano, Tezos, Lisk, Bitshares, Steem, entre otros, los cuales en conjunto suman un total de 24 blockchains que usan este algoritmo. El dominio del sector es bastante alto considerando la poca cantidad de proyectos involucrados, representando en término de capitalización bursátil,  el 2,64% del total del mercado. Esto es, unos $6.97B.

Este algoritmo se ha hecho popular entre los desarrolladores de aplicaciones descentralizadas (dApps), los cuales entre EOS y Tron dominan el subsector en términos de millones de dólares, según el sitio Dappreview.


#### PPrueba de actividad (PoA) {#poa}


El concepto fue introducido por primera vez en el año 2012 como una alternativa a la Prueba de Participación, PoS. La Prueba de actividad es esencialmente una estructura alternativa para Bitcoin y es una mezcla de dos de los mecanismos de consenso más populares: Prueba de Trabajo y Prueba de Estaca. Se introdujo la Prueba de actividad para frenar los temores sobre el fin de la minería en Bitcoin al agotarse los 21 millones de monedas disponibles y que complementa la Prueba de Trabajo para ayudar a prevenir un ataque del 51%.

Este mecanismo funciona comenzando de una manera de Prueba de Trabajo donde los mineros esencialmente resuelven un rompecabezas criptográfico y reclaman su recompensa si tienen éxito. La diferencia radica en el hecho de que los bloques minados son solo encabezados y direcciones de recompensa de minería en lugar de contener transacciones.

Prueba de actividad, en resumen, selecciona un par aleatorio de la red para firmar un nuevo bloque. Este método requiere un intercambio continuo de datos. Para reducir el tráfico, la "plantilla" de bloque no incluye la lista de transacciones y, en su lugar, la agrega el último firmante.

Como punto en contra, hereda la desventaja tanto de la Prueba de Trabajo como de la Prueba de Participación en términos de altos recursos utilizados y validadores maliciosos.

Entre las monedas más populares que lo usan encontramos a Decred (DCR), Espers (ESP).


#### Prueba de quemadura (PoB) {#pob}

Proof of Burn es paralelo al concepto de que es imposible que alguien elimine datos de una cadena de bloques. Entonces, el concepto a inventar era 'quemar' monedas. Consiste proporcionar pruebas de que se han quemado algunas  monedas en el proceso de enviar una transacción a una dirección que no se puede utilizar. Este método solo funciona con monedas extraídas de monedas criptográficas de Prueba de Trabajo. Los usuarios intentarán quemar la mayor cantidad de monedas para poder "ganar" la recompensa de bloque. La mayoría de las veces se ha introducido la Prueba de quemadura para sembrar otras monedas destruyendo el valor de una.

Se dice que el proceso de selección es aleatorio, pero al mismo tiempo, también se dice que cuantas más monedas queme el usuario, mayores serán sus posibilidades de ser seleccionado para extraer el siguiente bloque. Esto es algo similar al proceso de Bitcoin donde la inversión radica en la potencia informática que necesita mejorar para obtener mejores hashrates.

Slimcoin (SLM) es la gran exponente de este algoritmo. También TGCoin o Third Generation Coin, utiliza el algoritmo. Sin embargo, La moneda auxiliar para Counterparty, una extensión de software de Bitcoin con funcionalidad de monedas de colores, se distribuyó a través de un proceso de prueba de quemado. Los participantes tuvieron que enviar Bitcoins a una dirección no confiable y recibieron tokens de Counterparty a cambio.



#### Prueba de capacidad (POC) {#poc}

La Prueba de capacidad es un mecanismo de consenso que utiliza un proceso llamado trazado. Con Prueba de Trabajo, los mineros usan la computación para adivinar la solución correcta; sin embargo, con Proof Of Capacity, las soluciones se almacenan previamente en almacenes digitales (como discos duros). Este proceso se llama trazado. Después de que se ha trazado un almacenamiento (lo que significa que se ha llenado de soluciones), puede participar en el proceso de creación de bloques.

Quien tenga la solución más rápida para el rompecabezas de un (nuevo) bloque, puede crear el nuevo bloque. Cuanta más capacidad de almacenamiento tenga, más soluciones podrá almacenar, mayores serán sus probabilidades de crear un bloque.

La prueba de capacidad contiene dos partes distintas en el trazado o la creación del archivo de parcelas y la extracción real de los bloques. El tamaño de su disco duro es el factor que define el tiempo que le llevará desarrollar los archivos de trazado. Esto varía de días a semanas pares.

Burstcoin fue el primero en introducir este concepto. Otros ejemplos son Chia, SpaceMint.



####  Prueba de tiempo transcurrido (POET) {#poet}

POET es un algoritmo de mecanismo de consenso que a menudo se usa en las redes de blockchain autorizadas para decidir los derechos de minería o los ganadores de bloque en la red. Las redes de blockchain autorizadas son aquellas que requieren que cualquier posible participante se identifique antes de poder unirse. Basado en el principio de un sistema de lotería justo donde cada nodo es igualmente probable que sea un ganador, el mecanismo POET se basa en distribuir las posibilidades de ganar de manera justa entre el mayor número posible de participantes de la red.

Este mecanismo de consenso sólo puede funcionar si existe un sistema para verificar que nadie pueda ejecutar múltiples nodos y que el tiempo de espera asignado sea realmente aleatorio. Sin un sistema como este, el mecanismo de consenso tiene defectos importantes.

Esencialmente, el flujo de trabajo es similar al mecanismo de consenso seguido por el algoritmo de Prueba de Trabajo (PoW) de Bitcoin, pero sin su alto consumo de energía. El caso más ejemplar de es Hyperledger Sawtooh, una plataforma blockchain modular, autorizada y de nivel empresarial.



####  Algoritmo de consenso del obelisco {#obelisco}

Obelisk es un algoritmo de consenso prometedor que tiene como objetivo eliminar las deficiencias de los algoritmos de Prueba de Trabajo (PoW) y Prueba de Participación (PoS) y hace posible mantener el estado de blockchain en la red distribuida con un mínimo poder de cómputo y sin necesidad de participación. Reduce la necesidad de minería, mejora significativamente la velocidad de las transacciones y ofrece una seguridad mejorada.

Obelisk intenta sortear los problemas de PoW y PoS distribuyendo la influencia en la red de acuerdo con un concepto llamado "red de confianza", donde la densidad de la red de suscriptores de un nodo determina su influencia en la cadena.

El caso más ejemplar de este algoritmo de consenso lo encontramos en el proyecto llamado SkyCoin.


####  Prueba de Asignación (PoA) {#poa}

Es un mecanismo de consenso de la nueva era que requiere menos potencia y puede ejecutarse en hardware de gama relativamente baja. El mecanismo de trabajo de PoA permite que las aplicaciones diarias de Internet de las cosas (IoT) se utilicen para funciones básicas de minería de capacidad limitada. Con su potencia de procesamiento a bordo, los dispositivos compatibles con IoT se pueden utilizar para la minería de criptomonedas.

Sin embargo, dado que la memoria disponible y la potencia de procesamiento en estos dispositivos es limitada, su contribución a la minería sigue siendo pequeña. El mecanismo de trabajo del algoritmo PoA facilita este tipo de minería "ligera".

El ejemplo más destacable está en la  cadena de bloques IOTW.




####  Prueba de punto de control (PoC) {#poc}

Proof of Checkpoint es un sistema híbrido que utiliza cualquier sistema Proof of Stake con un sistema Proof of Work. La idea de este concepto es mitigar los ataques al sistema de Prueba de Participación. Sin embargo, todavía está sujeto a un ataque a un nodo que ha estado desconectado durante un período prolongado de tiempo y, a su vez, puede usarse para proporcionar información falsa sobre la cadena de bloques.

Cada x cantidad de bloques en el sistema de Prueba de Participación requiere que se extraiga un bloque de Prueba de Trabajo. Cada bloque de Prueba de trabajo no contiene transacciones y están directamente vinculados tanto a la red de Prueba de trabajo como a la red de Prueba de participación.




####  Proof of Formulation (PoF) {#pof}

El novedoso algoritmo de consenso propuesto por la plataforma surcoreana FLETA  llamada Prueba de Formulación (PoF), trata de resolver las deficiencias de PoW (gasto de energía), PoS (falla de seguridad) y dPoS (centralización) combinando lo mejor de cada uno en un solo mecanismo de consenso.

En la Prueba de Formulación (PoF), la minería y la generación de bloques se realizan de manera diferente en comparación con las plataformas de blockchain existentes. Los formuladores actúan como generadores de bloques en la plataforma FLETA. Los observadores permiten la confirmación en tiempo real de los bloques que se generan y evitan el doble gasto.

Los formuladores sirven como la columna vertebral del algoritmo PoF. El algoritmo PoF, difiere del PoW en que no requiere una potencia informática enorme y también difiere del DpoS, donde solo los delegados elegidos pueden participar en la minería.

Debido al corto tiempo del bloque de solo 0.5 segundos, la minería es de alta velocidad, con solo cuatro segundos por bloque. Además, en el ecosistema minero de FLETA, los bloques se confirman instantáneamente a través de los Nodos de Observador. Entre los cinco nodos de observación, tres de ellos deberían validar los bloques inmediatamente después de generarlos, lo que permite que los bloques se difundan rápidamente.

FLETA actualmente tiene un mes de estar con su red principal en el aire, y gracias a su alta escalabilidad mediante el uso de tecnología paralela de fragmentación y una estructura independiente de múltiples cadenas, la plataforma promete ser un excelente entorno para el desarrollo ilimitado de Dapps al separar el rendimiento de la cadena principal y el dominio de datos, lo que permite que cada Dapp se opere de forma independiente, lo que reduce los costos excesivos de desarrollar y ejecutar aplicaciones descentralizadas.


## Más información {#further-reading}

<!-- TODO -->

## Temas relacionados {#related-topics}

- [Prueba de trabajo](/developers/docs/consensus-mechanisms/pow/)
- [Minería](/developers/docs/consensus-mechanisms/pow/mining/)
- [Prueba de participación](/developers/docs/consensus-mechanisms/pos/)
