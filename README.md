# SISTEMAS OPERACIONAIS

## Índice
- [🌟 O que é um Sistema Operacional?](#o-que-é-um-sistema-operacional)
- [História dos Sistemas Operacionais](#história-dos-sistemas-operacionais)
  - [Gerações](#gera%C3%A7%C3%B5es)
- [Revisão sobre hardware de computadores](#revisão-sobre-hardware-de-computadores)
  - [CPU](#cpu)
  - [Memória](#memória)

## 🌟 O que é um Sistema Operacional?
Um sistema operacional é o software que controla e facilita o uso do computador. Ele organiza como os programadores interagem com o hardware e gerencia recursos como memória e processamento. Além disso, ele:
- 🚀 Isola processos para garantir que um programa não interfira em outro, aumentando a segurança e a estabilidade.
- 💬 Gerencia a comunicação entre o software e dispositivos como teclados e impressoras.
- 🎨 Oferece uma interface de usuário, que pode ser gráfica ou de linha de comando, para uma interação mais intuitiva.
- 🗂️ Cria abstrações para simplificar tarefas complexas, como trabalhar com arquivos, em vez de lidar diretamente com o hardware.

O objetivo principal é entender como essas abstrações facilitam o uso do computador e dos aplicativos.

## História dos Sistemas Operacionais

### Gerações
- **(1945–55) Válvulas 🔲**  
Os computadores usavam válvulas eletrônicas para processar dados. Essas máquinas eram enormes, consumiam muita energia e frequentemente falhavam, mas marcaram o início da era dos computadores eletrônicos, com exemplos como o ENIAC.

- **(1955–65) Transistores e Sistemas em Lotes (Batch) 💾**  
A tecnologia evoluiu com a introdução dos transistores, que substituíram as válvulas. Os computadores se tornaram menores, mais eficientes e confiáveis. Nesse período, surgiram os sistemas em lotes (batch), onde várias tarefas eram processadas em sequência sem intervenção humana.

  **Processo de Lote:**
  - 🗃️ Programadores levavam cartões para o 1401.
  - 📜 O 1401 lia o lote de tarefas em uma fita.
  - 🚚 O operador levava a fita de entrada para o 7094.
  - ⚙️ O 7094 executava o processamento.
  - 🚚 O operador levava a fita de saída para o 1401.
  - 🖨️ O 1401 imprimia as saídas.

- **(1965–1980) Circuitos Integrados (CIs) e Multiprogramação 💻**  
Os circuitos integrados (CIs) permitiram a construção de computadores ainda menores e mais poderosos. A multiprogramação também foi introduzida, permitindo que vários programas fossem executados simultaneamente, aumentando a eficiência dos sistemas.

- **(1980–Presente) Computadores pessoais 🖥️**  
Os computadores pessoais (PCs) se tornaram comuns, trazendo a computação para o uso doméstico e empresarial. Essa era é marcada por avanços contínuos em velocidade, capacidade e acessibilidade, com computadores cada vez mais poderosos e compactos.

## Revisão sobre hardware de computadores

Um sistema operacional está intimamente ligado ao hardware do computador no qual ele é executado. Ele estende o conjunto de instruções do computador e gerência seus recursos. Para funcionar, ele deve conhecer profundamente o hardware, pelo menos como aparece para o programador. Conceitualmente, um computador pessoal simples pode ser abstraído em um modelo que lembra A CPU, memória e dispositivos de E/S(entrada/saída) estão todos conectados por um sistema de barramento e comunicam-se uns com os outros sobre ele.


### CPU
A CPU, o "cérebro" do computador, executa programas ao buscar, decodificar e executar as instruções armazenadas na memória, repetindo esse processo até o programa terminar. Cada CPU tem um conjunto específico de instruções que pode executar, e diferentes tipos de CPUs, como x86 e ARM, não podem entender as instruções umas das outras. Como acessar a memória é mais lento do que executar instruções, a CPU usa registradores internos para armazenar temporariamente dados e resultados. Além desses registradores gerais, que ajudam a guardar variáveis e resultados temporários, há também registradores especiais. O contador de programa indica a próxima instrução a ser executada, o ponteiro de pilha gerencia a pilha de chamadas de funções e armazena informações temporárias e variáveis locais, e o PSW (Palavra de Status do Programa) contém informações sobre o estado do programa e as condições de execução. O sistema operacional precisa gerenciar esses registradores, especialmente quando troca entre diferentes programas. Ele deve salvar o estado dos registradores para poder retomar o programa exatamente de onde parou quando voltar a executá-lo.

### Memória
O segundo principal componente em qualquer computador é a memória. Idealmente, uma memória deve ser rápida ao extremo (mais rápida do que executar uma instrução, de maneira que a CPU não seja atrasada pela memória), abundantemente grande e muito barata. Nenhuma tecnologia atual satisfaz todas essas metas, assim uma abordagem diferente é tomada. O sistema de memória é construído como uma hierarquia de camadas. A camada superior consiste em registradores internos à CPU. Eles são feitos do mesmo material que a CPU e são, desse modo, tão rápidos quanto ela. Em consequência, não há um atraso ao acessá-los. Em seguida, vem a memória cache, que é controlada principalmente pelo hardware. A memória principal é dividida em linhas de cache, tipicamente 64 bytes, com endereços 0 a 63 na linha de cache 0, 64 a 127 na linha de cache 1 e assim por diante. As linhas de cache mais utilizadas são mantidas em uma cache de alta velocidade localizada dentro ou muito próximo da CPU. Quando o programa precisa ler uma palavra de memória, o hardware de cache confere se a linha requisitada está na cache.
