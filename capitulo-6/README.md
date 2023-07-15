## SEGURANÇA DE REDES DE COMPUTADORES | 2022.2

Michel Tavares de Oliveira

1. O que é encriptação tripla?

A encriptação tripla, também conhecida como Triple DES (3DES), é um algoritmo de criptografia que é usado para proteger informações sensíveis. Ele utiliza três passos consecutivos do algoritmo DES para encriptar os dados. Basicamente, o algoritmo aplica o DES três vezes em sequência, usando duas ou três chaves diferentes. As chaves geralmente são de 56 bits cada, mas no total, a combinação de três chaves resulta em uma chave efetiva de 168 bits.

A aplicação do 3DES oferece uma camada extra de segurança em relação ao DES original, tornando-o mais resistente a ataques. No entanto, devido à sua complexidade e ao aumento do poder computacional atual, o 3DES tem sido gradualmente substituído por algoritmos mais avançados, como o AES (Advanced Encryption Standard). O AES é considerado mais seguro e eficiente em comparação ao 3DES.

2. O que é ataque meet-in-the-middle?

O ataque meet-in-the-middle (encontro no meio) é um tipo de ataque criptográfico que visa quebrar uma criptografia que utiliza duas etapas de encriptação diferentes. O princípio básico do ataque meet-in-the-middle é aproveitar a propriedade das funções de encriptação e desencriptação reversíveis. Ele explora a ideia de que a criptografia em duas etapas pode ser revertida para encontrar as chaves secretas envolvidas no processo.


3. Quantas chaves são usadas na encriptação tripla?

Tuchman propôs um método de encriptação triplo que utiliza apenas duas chaves. A função segue uma sequência encriptar-decriptar-encriptar. 3DES com duas chaves é uma alternativa relativamente popular ao DES, e tem sido adotada para uso nos
padrões de gerenciamento de chave ANSI X9.17 e ISO 8732.

Embora alguns ataques pareçam ser impraticáveis, qualquer um usando o 3DES com duas chaves
poderá sentir certa preocupação. Assim, muitos pesquisadores agora consideram o 3DES com três chaves a alternativa preferida. O 3DES com três chaves possui um tamanho de chave efetivo
de 168 bits.

4. Por que a parte do meio do 3DES é decriptação, em vez de encriptação?
Não existe significado criptográfico no uso da decriptação para o segundo estágio. Sua única vantagem é que permite que os usuários do 3DES decriptografem dados criptografados pelos usuários do DES único.

5. Por que alguns modos de operação de cifra de bloco só utilizam a encriptação, enquanto outros
empregam encriptação e decriptação?

Os modos de operação que envolvem apenas a etapa de encriptação a principal vantagem desses modos é a simplicidade e a eficiência do processo de encriptação, uma vez que cada bloco pode ser processado separadamente sem a necessidade de informações adicionais. No entanto, eles não fornecem autenticidade nem integridade dos dados. Portanto, esses modos são mais adequados para casos em que a confidencialidade é o único requisito necessário.

Por outro lado, os modos de operação que envolvem tanto a encriptação quanto a decriptação são confidencialidade, autenticidade e integridade dos dados. Eles usam uma combinação de etapas de encriptação e decriptação para alcançar esses objetivos. Geralmente, eles requerem algum processamento adicional para incluir informações extras, como vetores de inicialização (IVs) e autenticação de mensagem. Esses modos são mais adequados quando a confidencialidade e a integridade dos dados são requisitos essenciais, como em comunicações seguras ou armazenamento de dados sensíveis.

6. Você deseja construir um dispositivo de hardware para realizar encriptação de bloco no modo
cipher block chaining (CBC) usando um algoritmo mais forte do que DES. 3DES é um bom
candidato. A Figura 1 mostra duas possibilidades, ambas acompanhando a definição do CBC.
Qual das duas você escolheria:

(a) Por segurança?

Por segurança, seria adequado escolher a (b) CBC com três loops, visto que seriam mais passos a serem executados, e com isso, maior o caso de confidencialidade, autenticidade e integridade dos dados.

(b) Por desempenho?

Por desempenho, a (a) CBC com um loop seria o escolhido, visto que não demandaria tanto poder computacional na hora de gerar a criptografia. Portanto, um novo bloco de texto cifrado é produzido a cada loop, em oposição a cada 3 loops no caso de loop único. Isso dá à construção de três loops uma taxa de transferência três vezes maior do que a construção de um loop.
