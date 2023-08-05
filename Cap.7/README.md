## SEGURANÇA DE REDES DE COMPUTADORES | 2022.2

1. Qual é a diferença entre aleatoriedades estatísticas e imprevisibilidade?

A preocupação na geração de uma sequência de números supostamente aleatórios tem sido de que a sequência de números seja aleatória em algum sentido estatístico bem definido. Existem dois critérios para isso, sendo a distribuição uniforme: a distribuição dos bits na sequência deve ser uniforme; ou seja, a frequência de ocorrência de cada um dos uns e zeros deve ser aproximadamente a mesma. E a independência: nenhum valor na sequência pode ser deduzido a partir dos outros.

Já a imprevisibilidade, requisito não é tanto que a sequência de números seja estatisticamente aleatória, mas que os membros sucessivos dela sejam imprevisíveis. Com “verdadeiras” sequências aleatórias, cada número é estatisticamente independente dos outros na sequência e, portanto, imprevisíveis.

Portanto, a aleatoriedade estatística pode ser compreendida e descrita por meio de técnicas estatísticas, enquanto a imprevisibilidade está relacionada a eventos ou resultados que não podem ser previstos, mesmo que sejam determinados por processos aleatórios.

2. Liste considerações de projeto importantes para uma cifra de fluxo.

Segurança Criptográfica, Tamanho da Chave e Geração de Números Pseudorrandômicos

3. Por que não é desejável reutilizar uma chave de cifra de fluxo?

Se dois textos claros forem encriptados com a mesma chave usando uma cifra de fluxo, então a criptoanálise normalmente é muito simples. Se os dois fluxos de texto cifrado passaram por uma operação XOR, o resultado é o XOR dos textos claros originais. Se os textos claros forem strings de texto, números de cartão de crédito ou outros fluxos de bytes com propriedades conhecidas, então a criptoanálise poderá ter sucesso.

4. Que operações primitivas são usadas no RC4?

O algoritmo é baseado no uso de uma permutação aleatória. Uma chave de tamanho variável de 1 a 256 bytes é usada para inicializar um vetor de estado S de 256 bytes, com elementos S[0], S[1], ..., S[255]. Em todos os momentos, S contém uma permutação de todos os números de 8 bits de 0 a 255. Para a encriptação e a decriptação, um byte k é gerado a partir de S selecionando uma das 255 entradas de uma forma sistemática. À medida que cada valor de k é gerado, as entradas em S são mais uma vez permutadas.

Para encriptar, faça o XOR do valor k com o próximo byte do texto claro. Para decriptar, faça o XOR do valor k com o próximo byte do texto cifrado.

5. Se apanharmos um algoritmo de congruência linear com um componente aditivo de 0:

Xn+1 = (aXn) mod m

então, podemos mostrar que, se m é primo, e se determinado valor de a produz o período máximo de m − 1, então a^k também produzirá o período máximo, desde que k seja menor que m e que m − 1 não seja divisível por k. Demonstre isso usando X0 = 1 e m = 31, e produzindo as sequências para ak = 3, 3², 3³ e 3⁴.

k = 1 (a^1 = 3):

X0 = 1

X1 = (3 * 1) mod 31 = 3

X2 = (3 * 3) mod 31 = 9

X3 = (3 * 9) mod 31 = 27

X4 = (3 * 27) mod 31 = 19

X5 = (3 * 19) mod 31 = 26

X6 = (3 * 26) mod 31 = 17

X7 = (3 * 17) mod 31 = 20

X8 = (3 * 20) mod 31 = 25

X9 = (3 * 25) mod 31 = 11

X10 = (3 * 11) mod 31 = 4

X11 = (3 * 4) mod 31 = 12

X12 = (3 * 12) mod 31 = 1

O período dessa sequência é 12.

k = 2 (a^2 = 9):

X0 = 1

X1 = (9 * 1) mod 31 = 9

X2 = (9 * 9) mod 31 = 19

X3 = (9 * 19) mod 31 = 25

X4 = (9 * 25) mod 31 = 12

X5 = (9 * 12) mod 31 = 4

X6 = (9 * 4) mod 31 = 5

X7 = (9 * 5) mod 31 = 8

X8 = (9 * 8) mod 31 = 7

X9 = (9 * 7) mod 31 = 28

X10 = (9 * 28) mod 31 = 22

X11 = (9 * 22) mod 31 = 20

X12 = (9 * 20) mod 31 = 26

X13 = (9 * 26) mod 31 = 17

X14 = (9 * 17) mod 31 = 10

X15 = (9 * 10) mod 31 = 30

X16 = (9 * 30) mod 31 = 16

X17 = (9 * 16) mod 31 = 23

X18 = (9 * 23) mod 31 = 14

X19 = (9 * 14) mod 31 = 3

X20 = (9 * 3) mod 31 = 27

X21 = (9 * 27) mod 31 = 1

O período dessa sequência é 21.

k = 3 (a^3 = 27):

X0 = 1

X1 = (27 * 1) mod 31 = 27

X2 = (27 * 27) mod 31 = 23

X3 = (27 * 23) mod 31 = 4

X4 = (27 * 4) mod 31 = 19

X5 = (27 * 19) mod 31 = 8

X6 = (27 * 8) mod 31 = 7

X7 = (27 * 7) mod 31 = 28

X8 = (27 * 28) mod 31 = 22

X9 = (27 * 22) mod 31 = 10

X10 = (27 * 10) mod 31 = 30

X11 = (27 * 30) mod 31 = 16

X12 = (27 * 16) mod 31 = 14

X13 = (27 * 14) mod 31 = 3

X14 = (27 * 3) mod 31 = 13

X15 = (27 * 13) mod 31 = 29

X16 = (27 * 29) mod 31 = 25

X17 = (27 * 25) mod 31 = 28

O período dessa sequência é 17.

k = 4 (a^4 = 81):

X0 = 1

X1 = (81 * 1) mod 31 = 19

X2 = (81 * 19) mod 31 = 12

X3 = (81 * 12) mod 31 = 5

X4 = (81 * 5) mod 31 = 8

X5 = (81 * 8) mod 31 = 25

X6 = (81 * 25) mod 31 = 11

X7 = (81 * 11) mod 31 = 22

X8 = (81 * 22) mod 31 = 10

X9 = (81 * 10) mod 31 = 30

X10 = (81 * 30) mod 31 = 26

X11 = (81 * 26) mod 31 = 17

X12 = (81 * 17) mod 31 = 20

X13 = (81 * 20) mod 31 = 1

O período dessa sequência é 13.

6. (a) Qual é o período máximo que pode ser obtido do seguinte gerador?

Xn+1 = (aXn) mod 2⁴

O valor de 2^4 é 16, então o período máximo será 15, porque o gerador produzirá 15 números distintos antes de começar a se repetir.

(b) Qual deverá ser o valor de a?

O valor de a deve ser um número primo relativamente pequeno.

#O valor de a deve ser um número primo relativo a 16 para que o período máximo de 16 seja alcançado. Isso significa que a e 16 não podem ter fatores primos em comum, exceto 1. Por exemplo, a = 3, 5, 7, 11, ou 13 seriam valores adequados para obter o período máximo.

(c) Que restrições são exigidas na semente?

A semente precisa estar entre 0 <= 0 X0 < m. Ou seja, A restrição para a semente é que ela deve ser um número inteiro entre 0 e 15 (inclusive) para garantir a geração de números aleatórios dentro do intervalo desejado

7. Que valor de chave RC4 deixará S inalterado durante a inicialização? Ou seja, após a permutação inicial de S, as entradas de S serão quais aos valores de 0 a 255 na ordem crescente.

Para que o vetor S permaneça inalterado após a inicialização da chave no algoritmo RC4, é necessário que a chave seja uma sequência de bytes que seja uma permutação dos valores de 0 a 255 em ordem crescente.