# Bitcoin e Blockchain - Conceitos Fundamentais


## - Bitcoin -

O *Bitcoin* foi concebido no contexto das crises econômicas e insatisfações geradas pela Crise Financeira de 2008, quando governos de várias partes do mundo adotaram pacotes de resgate bilionários para salvar instituições bancárias, muitas vezes sem oferecer compensações adequadas para a população que sofreu os impactos negativos.

Em termos de suas principais funcionalidades, o *Bitcoin* pode ser utilizado como:

- Um meio de troca (facilitador de transações);
- Um ativo de reserva de valor;
- Um sistema de pagamentos alternativo.

O funcionamento do *Bitcoin* é viabilizado por uma combinação de tecnologias, incluindo criptografia avançada, o uso de blockchain, descentralização das redes e mecanismos de incentivo para os participantes. Entretanto, é importante ressaltar que o *Bitcoin* ainda não é capaz de substituir completamente o sistema financeiro tradicional, que oferece uma gama mais ampla de serviços e funcionalidades que o *Bitcoin*, até o momento, não consegue abranger.

## Principais diferenças entre bancos convencionais e o bitcoin:

| Característica| Bitcoin | Bancos|
|-|-|-|
| **Contabilidade**| Utiliza a tecnologia *blockchain*, com um livro-razão público e imutável.| Centralizada e controlada por uma única entidade, com registros privados e auditados internamente. |
| **Armazenamento**| O valor é armazenado integralmente na carteira do usuário.| Sistema de reservas fracionárias, com parte dos depósitos disponível para saque e outra parte emprestada. |
| **Segurança** | Baseada em criptografia avançada e descentralizada.| Provida por sistemas institucionais e normas de compliance, supervisionados por reguladores financeiros. |
| **Emissão de moeda** | Regida por um algoritmo com emissão limitada e progressiva.| Determinada por políticas econômicas, como decisões de bancos centrais.|
| **Transações**| Ocorrência distribuída, verificadas por uma rede de nós descentralizados. | Centralizadas e processadas por sistemas controlados pelo banco, com intermediários.|
| **Autenticação**| Feita por meio da *blockchain*, sem necessidade de identidades pessoais. | Baseada em sistemas de identificação, como documentos e verificações de crédito.|
| **Regulamentação**| Enfrenta incertezas regulatórias, com legislações ainda em desenvolvimento. | Fortemente regulado por bancos centrais e autoridades governamentais, com regras definidas. |
| **Processo de decisão** | Mudanças no protocolo dependem do consenso da comunidade.| Decisões arbitrárias tomadas por diretores, acionistas ou reguladores, sem consulta ao cliente. |
| **Controle do dinheiro**| O controle está nas mãos do usuário, responsável por suas chaves privadas. | O banco controla o dinheiro, com o usuário acessando o saldo conforme as regras da instituição. |


## - Blockchain -


## Conceitos Fundamentais

A *blockchain* é uma estrutura de armazenamento de dados formada por uma sequência de blocos interligados. Cada bloco contém informações que apontam para o bloco anterior, garantindo a integridade e continuidade da cadeia, o que impede a manipulação ou quebra de dados históricos. Uma peça central nesse mecanismo é a função *hash*, que converte entradas de qualquer tamanho em uma saída (digest) de tamanho fixo e aparentemente aleatória. Os *hashes* são essenciais para a segurança e são caracterizados por serem fáceis de calcular, unidirecionais (não é possível reconstruir a entrada a partir do *hash*), resistentes a colisões (difícil gerar dois *hashes* idênticos para entradas diferentes) e adequados para desafios computacionais (*puzzle-friendly*), o que significa que mesmo pequenas alterações nos dados resultam em *hashes* completamente diferentes.

### Assinaturas Digitais

As assinaturas digitais desempenham um papel crucial na autenticação de transações e documentos no ambiente digital. Elas garantem que somente o proprietário da assinatura possa usá-la para validar uma transação. Cada assinatura é exclusiva para o documento ou transação a que se refere, o que permite que qualquer pessoa verifique sua autenticidade de forma confiável. Isso é possível graças à combinação de uma chave pública e uma chave privada: a chave privada é utilizada para gerar a assinatura digital e deve ser mantida em sigilo absoluto, enquanto a chave pública é compartilhada para que terceiros possam verificar a validade da assinatura. É recomendável que os usuários mantenham mais de um par de chaves (pública/privada) para proteger seus ativos em caso de roubo ou comprometimento de uma das chaves.

### Funcionamento de uma Moeda Virtual

O exemplo da moeda virtual CentralCoin é útil para entender a lógica por trás das criptomoedas, como o Bitcoin. A principal diferença entre a CentralCoin e o Bitcoin reside na forma de validação das transações. Na CentralCoin, uma autoridade central é responsável por verificar e manter a blockchain, enquanto no Bitcoin, esse processo é descentralizado, sendo executado por uma rede distribuída de participantes (nós).

A *blockchain* da CentralCoin registra tanto a criação quanto a transferência de moedas. Para realizar uma transação, o usuário deve indicar quais moedas deseja usar (destruir) e quem serão os destinatários das novas moedas que serão geradas. O processo é finalizado com a assinatura digital do usuário, que autentica a transação. Um detalhe importante é que a soma das moedas destruídas deve ser maior que a das moedas criadas, pois a diferença representa uma taxa de transação que geralmente é destinada aos validadores da rede.

Esses conceitos são fundamentais para o funcionamento não apenas de criptomoedas, mas também de diversas aplicações descentralizadas que utilizam blockchain para segurança e verificação de dados.

### Rede Bitcoin

A rede Bitcoin é projetada para ser totalmente descentralizada, sem um controle central ou hierárquico, funcionando de acordo com um protocolo de consenso compartilhado por todos os participantes. Nessa rede, os computadores conectados são chamados de nós (*nodes*), e existem dois tipos principais: os *full nodes* e os *lite nodes*. 

- **Full nodes**: São nós que armazenam uma cópia completa da blockchain, contendo todo o histórico de transações. Eles podem operar de forma independente, validando transações e blocos sem depender de terceiros, e são essenciais para garantir a integridade e segurança da rede.
- **Lite nodes**: São versões mais leves dos nós, projetados para dispositivos com menos capacidade de armazenamento ou poder computacional, como smartphones. Eles não armazenam toda a blockchain, mas se conectam a *full nodes* para realizar operações, tornando-se uma opção mais acessível para usuários com recursos limitados.

A comunicação entre os nós da rede é feita por meio de um protocolo conhecido como "protocolo de fofoca" (*gossip protocol*), onde cada nó repassa as transações que recebeu para outros nós. Essa abordagem distribui rapidamente as informações pela rede, assegurando que todos os nós estejam atualizados sobre as transações mais recentes.

### Prova de Trabalho (*Proof of Work*)

A *Proof of Work* (PoW) é o mecanismo de consenso utilizado pela rede Bitcoin para validar transações e manter a segurança da blockchain. O processo envolve um cálculo complexo no qual os mineradores competem para encontrar um valor chamado *nonce* (um número arbitrário sem significado específico) que, ao ser combinado com os dados do bloco, produz um *hash* que cumpre o critério de dificuldade da rede — normalmente exigindo que o *hash* comece com um número específico de zeros.

Esse nível de dificuldade é ajustado dinamicamente para que novos blocos sejam criados aproximadamente a cada 10 minutos. Quando um minerador encontra o *nonce* correto, o bloco é transmitido para a rede, onde outros nós verificam sua validade. Se aprovado, o bloco é adicionado à blockchain. Se dois mineradores resolverem o problema simultaneamente, a rede escolherá o bloco que pertence à cadeia mais longa (com mais blocos subsequentes), descartando o outro.

Para aumentar as chances de sucesso, muitos mineradores se unem em *mining pools*, onde trabalham juntos e dividem as recompensas de forma proporcional ao poder computacional que cada um contribuiu. Isso torna a mineração mais previsível e acessível, especialmente para aqueles com menos recursos computacionais.

### Saldo de Bitcoins

O saldo de bitcoins de um indivíduo é determinado pela soma de todas as moedas associadas às chaves públicas que ele controla e que ainda não foram "gastas" em transações (ou seja, ainda não foram destruídas). Cada transação no Bitcoin envolve a destruição de moedas antigas e a criação de novas moedas, que são então associadas a outras chaves públicas, o que forma a base do sistema de transferência de valor na rede. 

Essa abordagem elimina a necessidade de um intermediário central e oferece uma maneira transparente e verificável de realizar transações financeiras, com cada nova transação sendo registrada na blockchain e acessível a qualquer um que utilize um *full node*.

Aqui está o texto reorganizado e expandido, com a adição de uma tabela para comparar os tipos de carteiras:

## Carteiras de Criptomoedas

As carteiras de criptomoedas são essenciais para armazenar e gerenciar chaves privadas e públicas, que são utilizadas para realizar transações e manter o controle sobre os ativos digitais. As principais características que definem uma carteira são:

- **Conveniência**: A facilidade de uso e a praticidade de acesso.
- **Disponibilidade**: A capacidade de acessar e utilizar a carteira a qualquer momento.
- **Segurança**: O nível de proteção contra roubo, acesso não autorizado e ataques cibernéticos.

### Tipos de Carteiras

Existem diferentes tipos de carteiras, cada uma com seus prós e contras em termos de segurança, praticidade e custo. A seguir, as carteiras são classificadas em três categorias principais: carteiras de papel, de hardware e de software.

| Tipo de Carteira  | Características                                                                 | Segurança                                                                                   | Conveniência                                                                            |
|-------------------|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| **Papel**         | Contém uma chave pública e uma chave privada anotadas em papel.                   | Muito segura se armazenada corretamente, imune a hackers, pois não há conexão com a internet. | Baixa praticidade, já que deve ser protegida fisicamente e usada com cuidado em transações. |
| **Hardware**      | Armazena as chaves privadas em um dispositivo físico, que realiza transações de forma independente. | Extremamente segura, mesmo em computadores infectados por vírus. Dados podem ser recuperados. | Moderadamente prática, pois é necessário ter o dispositivo físico sempre à mão.         |
| **Software**      | Armazena as chaves no computador ou celular e pode gerar múltiplos pares de chaves. | Segurança depende da proteção do dispositivo (antivírus, senhas fortes). Possui backup de dados. | Muito prática, acessível em dispositivos móveis e desktops.                             |
| **Online**        | Carteira baseada em serviços na web, onde as chaves são gerenciadas por terceiros. | Arriscada, pois o usuário não controla as chaves privadas diretamente, aumentando o risco de ataques. | Altamente prática, acessível de qualquer lugar com conexão à internet.                  |

### Considerações de Segurança

- **Carteiras de papel**: São seguras se forem armazenadas corretamente em locais protegidos contra fogo, roubo ou danos físicos. No entanto, qualquer perda ou dano ao papel pode resultar na perda de acesso aos fundos.
  
- **Carteiras de hardware**: Consideradas uma das opções mais seguras, especialmente contra ataques digitais, pois mantêm as chaves privadas offline. Mesmo que o computador esteja infectado com malware, as transações permanecem seguras, já que as chaves privadas nunca entram em contato com o sistema.

- **Carteiras de software**: Embora convenientes, estão diretamente expostas a riscos se o dispositivo onde estão instaladas for comprometido. A segurança depende do uso de senhas fortes, softwares antivírus e backups regulares.

- **Carteiras online**: Essas carteiras são as mais convenientes, mas também as mais vulneráveis. Como o controle das chaves privadas está nas mãos de terceiros (geralmente uma plataforma online), há um risco maior de ataques cibernéticos ou falhas de segurança no provedor do serviço.

Aqui está o texto reorganizado, com informações adicionais e mudanças nas palavras para maior clareza:

## - Exchanges de Criptomoedas -

As *exchanges* são plataformas online que conectam compradores e vendedores de criptomoedas, como o Bitcoin. Elas funcionam de forma semelhante às bolsas de valores tradicionais, mas com foco em ativos digitais. As *exchanges* cobram uma pequena taxa por transação, servindo como intermediárias no mercado de criptomoedas. 

Uma diferença crucial em relação aos bancos e bolsas de valores tradicionais é que as *exchanges* de criptomoedas, em muitos países, ainda não estão plenamente regulamentadas. Essa falta de supervisão legal as torna mais vulneráveis a ataques cibernéticos e aumenta os riscos para os usuários, uma vez que muitos mecanismos de proteção financeira presentes no sistema bancário tradicional não se aplicam aqui.

### Fatores de Risco em Exchanges de Criptomoedas

Ao contrário de instituições financeiras tradicionais, as *exchanges* não possuem algumas salvaguardas que oferecem mais segurança aos clientes. Elas carecem de:

- **Requerimentos de reserva**: Diferente dos bancos, que são obrigados a manter uma porcentagem dos depósitos disponíveis em reservas, as *exchanges* não têm a mesma exigência.
- **Controle de investimentos**: Não há uma regulação rigorosa que supervisione como as *exchanges* gerenciam os fundos de seus clientes.
- **Fundo Garantidor de Créditos**: Enquanto bancos possuem garantias governamentais, como o Fundo Garantidor de Créditos (FGC) no Brasil, que protege os depositantes até certo valor em caso de falência, as *exchanges* não oferecem essa segurança.
- **Injeções de liquidez**: Bancos podem contar com injeções de liquidez por parte dos governos ou bancos centrais em momentos de crise. As *exchanges* não têm esse tipo de suporte financeiro, o que as torna mais vulneráveis a crises de liquidez.

Essa combinação de falta de regulação, proteção e suporte torna as *exchanges* um alvo frequente de hackers e ataques cibernéticos. Portanto, os usuários devem estar cientes dos riscos ao confiar grandes somas de dinheiro em plataformas de *exchange*.

## - Questão do Anonimato em Transações com Bitcoin -

O anonimato nas transações com Bitcoin é um ponto frequentemente debatido. Embora muitas pessoas pensem que o Bitcoin oferece anonimato total, na realidade, ele oferece **pseudonimato**, ou seja, as transações não estão diretamente ligadas à identidade real dos usuários, mas são rastreáveis através da blockchain. Cada transação realizada no Bitcoin é pública e registrada permanentemente na blockchain, permitindo que qualquer pessoa possa acompanhar o fluxo de bitcoins de uma chave pública para outra.

O problema surge quando uma chave pública pode ser associada à identidade de um usuário, seja através de práticas inadequadas de segurança ou de informações públicas. Isso pode comprometer a privacidade do indivíduo, já que, uma vez conhecida a chave pública de alguém, é possível rastrear todas as transações feitas por essa pessoa, revelando informações como hábitos de compra, frequência de transações e até com quem ela interage economicamente.

Portanto, embora o Bitcoin seja muitas vezes visto como uma moeda anônima, é importante lembrar que ele é **rastreável**, e há medidas que podem ser tomadas para melhorar a privacidade, como o uso de diferentes carteiras para diferentes transações e ferramentas de ofuscação de transações (como *coin mixers*). Contudo, o completo anonimato não é garantido, e é algo que deve ser considerado por qualquer pessoa que busca proteger sua privacidade ao usar criptomoedas.


