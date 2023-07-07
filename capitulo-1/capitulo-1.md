# Atividade Capítulo 1

Nome Completo: Michel Tavares de Oliveira

## 1. O que é a arquitetura de segurança OSI?

Trata-se de uma arquitetura que divide as redes de computadores em 7 camadas sendo elas:

- Física
- Enlace
- Rede
- Transporte
- Sessão
- Apresentação
- Aplicação

## 2. Qual é a diferença entre ameaças à segurança passivas e ativas?

**Ataque passivo:**
Tenta descobrir ou alterar dados do sistema sem alterar os recursos. Exemplos:
- Vazamentos de mensagens
- Análise de dados

**Ataque Ativo:**
Tenta descobrir ou alterar dados de um sistema e afetar a operação.

## 3. Liste e defina resumidamente as categorias de ataques passivos e ativos à segurança.

Existem 2 categorias de ataque passivo:

1. Vazamento de conteúdo de mensagem: Inclui conversas telefônicas, mensagens de e-mail e transferência de arquivos contendo informações sensíveis ou confidenciais que não podem ser identificadas por terceiros independentes.

2. Análise de tráfego: Envolve terceiros acessando mensagens ou conteúdos sensíveis, mesmo que sejam criptografados, para entender o que está sendo enviado.

O ataque ativo tem 4 categorias:

1. Ocultação: Quando uma entidade finge ser diferente.
2. Encaminhamento: Obtenção de dados, como um pacote de rede, sem alterar seu conteúdo ou impedir sua transmissão, com a intenção de causar efeito não autorizado ou indesejado.
3. Edição de mensagens: Alteração de qualquer parte de uma mensagem, atraso ou reorganização de mensagens para produzir um efeito não autorizado.
4. Bloqueio do Serviço: Impedimento de que usuários legítimos interajam, negando-lhes acesso ou uso normal. O objetivo é sobrecarregar os recursos do sistema de destino, impedindo que ele funcione corretamente ou se torne inutilizável.

## 4. Liste e defina resumidamente as categorias dos serviços de segurança

1. Autenticação: Certeza de que a entidade se comunicando é aquela que ela afirma ser.
2. Controle de acesso: Capacidade de limitar e prevenir o acesso não autorizado a um recurso, exigindo autenticação ou identificação antes de conceder acesso.
3. Confidencialidade dos Dados: Proteção dos dados transmitidos contra ataques passivos, evitando a divulgação não autorizada dos dados.
4. Integridade de Dados: Certeza de que os dados recebidos são exatamente os mesmos enviados por uma entidade autorizada, sem modificações, inserções ou exclusões.
5. Irretratabilidade: Proteção total do fluxo, impedindo que o emissor ou receptor neguem uma mensagem transmitida. Prova-se que o emissor alegado realmente a transmitiu.


## 5. Liste e defina resumidamente as categorias dos mecanismos de segurança.

Existem dois grupos de mecanismos de segurança: específicos e difusos.

**Mecanismos de Segurança Específicos:**

- Codificação: Aplicação de algoritmos matemáticos para transformar os dados em um formato que não seja facilmente compreensível. A recuperação dos dados transformados requer o uso de um algoritmo e possivelmente uma ou mais chaves de criptografia.
- Assinatura digital: Dados anexados a uma unidade de dados ou uma transformação criptográfica dessa unidade, que permitem ao destinatário comprovar a origem e a integridade dos dados, além de protegê-los contra falsificação pelo destinatário.
- Controle de acesso: Conjunto de mecanismos usados para impor direitos de acesso aos recursos. Esses mecanismos determinam quais usuários ou entidades têm permissão para acessar determinados recursos.
- Integridade dos dados: Conjunto de mecanismos utilizados para garantir a integridade de uma unidade de dados específica ou de um fluxo contínuo de unidades de dados.
- Troca de autenticação: Mecanismo projetado para garantir a identidade de uma entidade por meio da troca de informações. Esse mecanismo ajuda a verificar se uma entidade é realmente quem afirma ser.
- Preenchimento de tráfego: Inserção de bits em lacunas de um fluxo de dados, com o objetivo de dificultar a análise do tráfego por terceiros.
- Controle de roteamento: Permite a seleção de rotas específicas que sejam fisicamente seguras para determinados dados e alterações de roteamento, especialmente quando há suspeita de uma violação de segurança.
- Notarização: Uso de um terceiro confiável para garantir certas propriedades de uma troca de dados, como autenticidade ou integridade dos dados transmitidos.

**Mecanismos de Segurança Difusos:**

- Funcionalidade confiada: Baseia-se no que é considerado correto com base em critérios estabelecidos, como uma política de segurança. É aquilo que se espera que atenda a determinadas condições de segurança.
- Rótulo de segurança: Marcação associada a um recurso, que pode ser uma unidade de dados, e identifica ou descreve os atributos de segurança desse recurso.
- Detecção de evento: Identificação de eventos relevantes para a segurança. É o processo de reconhecer e registrar eventos que possam ter impacto na segurança de um sistema ou ambiente.
- Trilha de auditoria de segurança: Dados coletados e potencialmente utilizados para auxiliar uma auditoria de segurança. Essa auditoria envolve uma revisão e análise independente dos registros e atividades do sistema, com o objetivo de avaliar a conformidade e a efetividade das medidas de segurança implementadas.
- Recuperação de segurança: Ações tomadas para lidar com solicitações de mecanismos, como funções de tratamento e gerenciamento de eventos, visando à recuperação de uma situação de segurança. É o processo de restauração da segurança após um incidente ou uma violação.

## 6. Considere um caixa eletrônico (ATM) no qual os usuários fornecem um cartão e um número de identificação pessoal (senha). Dê exemplos de requisitos de confidencialidade, integridade e disponibilidade associados com esse sistema e, em cada caso, indique o grau de importância desses requisitos.

- **Confidencialidade:** É importante que os dados do cartão e o número de identificação pessoal (senha) sejam mantidos em sigilo para evitar acessos não autorizados. O grau de importância é alto.
- **Integridade:** Os dados fornecidos pelo usuário, como o número de identificação pessoal (senha), devem ser transmitidos e armazenados de forma segura, garantindo que não sejam alterados ou corrompidos. O grau de importância é alto.
- **Disponibilidade:** O sistema de caixa eletrônico deve estar sempre disponível para os usuários realizarem suas transações. O grau de importância é alto, pois qualquer interrupção ou indisponibilidade pode causar inconveniência e frustração aos usuários.

7. Para responder as letras abaixo, por favor, consulte o livro-texto da disciplina:

(a) Desenhe uma matriz similar ao Quadro 1.4 que mostre o relacionamento entre serviços de segurança e ataques.

Para cada serviço da matriz, a relação se dá por meio do impacto do ataque no serviço de segurança.

|                        | Vazamento de conteúdo de mensagens | Análise de tráfego | Disfarce | Repasse | Modificação de mensagens | Negação do serviço |
|------------------------|-----------------------------------|--------------------|----------|---------|--------------------------|--------------------|
| Autenticação           | x                                 |                    |          |         |                          |                    |
| Controle de Acesso     |                                   | x                  | x        |         |                          |                    |
| Confidencialidade dos Dados | x                             | x                  |          |         |                          |                    |
| Integridade de Dados   |                                   |                    |          |         | x                        | x                  |
| Irretratabilidade      |                                   |                    |          |         |                          | x                  |

(b) Desenhe uma matriz similar ao Quadro 1.4 que mostre o relacionamento entre mecanismos de segurança e ataques.

|                        | Vazamento de conteúdo de mensagens | Análise de tráfego | Disfarce | Repasse | Modificação de mensagens | Negação do serviço |
|------------------------|-----------------------------------|--------------------|----------|---------|--------------------------|--------------------|
| Codificação            | x                                 | x                  |          |         |                          |                    |
| Assinatura digital     | x                                 |                    |          |         |                          |                    |
| Controle de acesso     | x                                 | x                  |          |         |                          | x                  |
| Integridade de dados   |                                   |                    | x        |         |                          | x                  |
| Troca de autenticação  | x                                 |                    |          |         |                          |                    |
| Preenchimento de tráfego | x                               |                    |          |         |                          |                    |
| Controle de roteamento | x                                 |                    |          |         |                          |                    |
| Notarização            |                                   |                    | x        | x
