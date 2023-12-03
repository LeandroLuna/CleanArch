# CleanArch

## Origem da Clean Architecture**

A Clean Architecture é uma abordagem significativa no design de software, introduzida por Robert C. Martin, conhecido como Uncle Bob, há mais de dez anos. Inicialmente apresentada em seu blog, a Clean Architecture evoluiu para um livro extenso, sendo uma obra importante que não apenas descreve uma estrutura, mas também destaca a necessidade de compreensão dos detalhes.

A Clean Architecture é uma variação de outras arquiteturas, como a Hexagonal e Onion Architecture, compartilhando a missão de proteger o núcleo da aplicação. Ao comparar Clean Architecture com a Arquitetura Hexagonal, percebe-se que ambas buscam o mesmo objetivo, mas a Clean Architecture é mais detalhada, deixando mais aberta a forma de implementação.

Essa abordagem exige trabalhar com diversas camadas para proteger o coração da aplicação. As camadas representam limites arquiteturais, e durante o desenvolvimento, é crucial entender em qual camada se está e os limites a serem respeitados. A comunicação entre esses limites ocorre através de contratos e interfaces, promovendo o baixo acoplamento.

Clean Architecture é orientada a casos de uso, onde casos de uso representam as intenções de realizar ações que causem transformações no código. Essa ênfase em casos de uso é o que cria a chamada "Screaming Architecture", onde a estrutura da aplicação grita suas intenções de forma clara.

Embora o livro sobre Clean Architecture seja extenso, o módulo tem como objetivo fornecer uma orientação prática para evitar que os desenvolvedores se tornem apenas organizadores de pastas. Recomenda-se a leitura do livro para um embasamento mais profundo, pois ele aborda componentes, arquitetura, limites arquiteturais e regras de negócio, fornecendo uma compreensão mais abrangente e removendo lacunas básicas no conhecimento. Compreender a origem e a evolução da Clean Architecture é crucial para aplicar efetivamente esses conceitos no desenvolvimento de software.

## Pontos importantes sobre a Clean Architecture

- **Formatar o Software:** A arquitetura é crucial para dar forma ao software, assim como um projeto arquitetônico molda um prédio. É necessário ter um entendimento claro do design geral do software.

- **Divisão de Componentes:** Assim como um prédio tem divisões internas claras, a arquitetura de software envolve a definição clara de componentes. Cada componente tem seu lugar definido, facilitando o desenvolvimento e a compreensão do sistema.

- **Comunicação entre Componentes:** Na arquitetura de software, os componentes precisam se comunicar entre si. É essencial entender as diferentes formas de comunicação, assim como em um prédio onde a comunicação entre andares pode ocorrer por escadas, elevadores, ou outras vias.

- **Facilitação do Desenvolvimento:** Uma arquitetura sólida facilita o desenvolvimento, proporcionando uma compreensão clara dos limites e das responsabilidades de cada componente. Isso permite que diferentes partes do software sejam desenvolvidas independentemente sem interferir umas nas outras.

- **Pensar em Operação e Manutenção:** Uma arquitetura bem pensada não apenas facilita o desenvolvimento, mas também a operação e manutenção do software. Considerações como deploy, variáveis de ambiente, observabilidade, e escolha de fornecedores de observabilidade são essenciais desde o início.

- **Observabilidade e Logs:** O software deve ser projetado considerando a observabilidade, incluindo a gestão de logs. Decisões sobre onde armazenar logs, como lidar com observabilidade, e a escolha de ferramentas de monitoramento devem ser incorporadas desde o início do processo.

- **Flexibilidade e Opções Abertas:** Uma arquitetura eficaz proporciona flexibilidade, mantendo portas abertas para futuras decisões. A capacidade de agregar funcionalidades sem decisões precipitadas é uma característica importante de uma boa arquitetura.

## Keep Options Open

A estratégia de "Keep options open" (manter opções abertas) é um princípio-chave da arquitetura limpa. Uncle Bob destaca que uma boa arquitetura visa facilitar o processo, permitindo a postergação de decisões. Isso cria limites arquiteturais claros, reduzindo a dependência direta entre partes do sistema e mantendo opções abertas para o futuro.

Os objetivos fundamentais de uma boa arquitetura incluem dar suporte ao ciclo de vida completo do sistema. Isso abrange desde o desenvolvimento até o teste, deploy, observação, operação e manutenção. Uma arquitetura eficiente torna o sistema fácil de entender, desenvolver, manter e implantar, minimizando o custo ao longo do tempo e maximizando a produtividade do programador.

A importância de manter opções abertas é destacada como uma estratégia para evitar decisões precipitadas. Isso é particularmente crucial ao lidar com detalhes, pois o foco deve permanecer nas regras de negócio, que constituem o verdadeiro valor do software. Detalhes, como a escolha de tecnologias específicas, devem ser considerados como aspectos plugáveis e substituíveis, sem impactar as regras de negócio centrais.

Uma boa arquitetura contribui para a longevidade do software, facilitando a evolução tecnológica e prevenindo a acumulação de débitos técnicos. Ao manter opções abertas, os desenvolvedores podem se concentrar nas regras de negócio, atacando a complexidade no coração do software. Sendo assim, destaca-se a importância de não perder tempo com detalhes prematuros, e enfatiza-se que o valor real do software reside em suas regras de negócio.

## Use Cases

- **Definir Casos de Uso:**
   - Compreender que casos de uso representam intenções no desenvolvimento de software.
   - Reconhecer que, muitas vezes, as intenções não são claras ao olhar para o código de um software.

- **Clareza na Arquitetura:**
   - Entender que a arquitetura, ao trabalhar com casos de uso, oferece clareza sobre cada comportamento do software.

- **Postergar Decisões:**
   - Adotar a prática de "Keep options open" na Clean Architecture, postergando decisões sobre detalhes como banco de dados, sistema de fila, REST ou gRPC.

- **Independência dos Casos de Uso:**
   - Compreender que os detalhes não devem impactar as regras de negócio nos casos de uso, mantendo as opções abertas.

- **Use Cases versus SRP:**
   - Entender o Single Responsibility Principle (SRP) e resistir à tentação de reaproveitar código entre casos de uso semelhantes.
   - Reconhecer que casos de uso semelhantes podem evoluir de maneiras diferentes, violando a responsabilidade única se não forem independentes.

- **Duplicação Real versus Acidental:**
   - Avaliar a duplicação de código considerando se é uma duplicação real, que deve ser evitada, ou uma duplicação acidental que pode ser aceitável para evitar refatorações prematuras.

A ênfase está na independência e clareza dos casos de uso, permitindo que evoluam de acordo com suas intenções específicas, sem violar princípios como SRP e DRY. O foco é manter a flexibilidade na arquitetura, facilitando futuras mudanças e evolução do software.

## O fluxo dos Use Cases

- **Natureza do Use Case:**
   - Entender que o Use Case representa uma intenção no desenvolvimento de software, automatizando operações para simplificar tarefas cotidianas.

- **Regras de Negócio e Automação:**
   - Reconhecer que, para a automação acontecer, é necessário estabelecer regras de negócio que serão utilizadas pelo Use Case.

- **Orquestração do Fluxo:**
   - Compreender que o fluxo, a ordem e a orquestração das operações são representados pelo Use Case, que coordena múltiplas chamadas e passos para realizar uma intenção específica.

- **Exemplo Prático:**
   - Observar o exemplo prático de um empréstimo, onde o fluxo do Use Case envolve validação de nome, endereço, consulta de credit score e ações correspondentes.

- **Função do Use Case na Automação:**
   - Perceber que o Use Case, na prática, é responsável por fazer o fluxo das operações acontecerem, representando a automação desejada.

- **Relação com Regras de Negócio:**
   - Entender que as regras de negócio validam e estabelecem as regras do jogo, enquanto o Use Case acessa essas regras para gerar um fluxo lógico de acordo com as necessidades da empresa.

- **Camadas e Papel do Use Case:**
   - Relacionar o Use Case com uma camada de aplicação, que orienta como a aplicação deve funcionar, diferenciando-a das regras estabelecidas nas entidades do domínio.

O Use Case, portanto, desempenha um papel fundamental na automação e orquestração das operações, proporcionando clareza e eficiência no desenvolvimento de software.

## Limites arquiteturais

Existem alguns limites arquiteturais na Clean Architecture, destacando-se a importância de separar componentes e estabelecer contratos para garantir a eficiência do software em diferentes momentos e fluxos. Reforça-se, assim, o princípio de que tudo que não impacta diretamente nas regras de negócio deve pertencer a um limite arquitetural distinto.

Um exemplo prático ilustra essa ideia, mostrando que elementos como o frontend ou o banco de dados não devem influenciar diretamente as regras da aplicação. Componentes que não impactam nas regras de negócio devem ser colocados em limites arquiteturais separados. Pode-se utilizar de abstrações para definir esses limites, exemplificando como as regras de negócio podem chamar uma interface que representa o acesso ao banco de dados.

A inversão de controle é uma prática para evitar dependências diretas, destacando que as regras de negócio dependem de interfaces, tornando-as agnósticas ao banco de dados. Um exemplo são os banco de dados que, de certa forma, deve chamar a camada de negócios por meio dessa interface.

A imagem clássica da Clean Architecture é como uma representação visual dos limites arquiteturais, onde cada círculo representa um limite arquitetural distinto. O objetivo é evitar vazamentos e rupturas desses limites, garantindo uma clara separação entre os componentes do sistema.

## Input vs Output

Tudo no desenvolvimento de software se resume a um ciclo de input e output. Ao criar um pedido, por exemplo, os dados de entrada (input) resultam em dados de saída (output) quando o pedido é criado.

- **Fluxo na Clean Architecture:**

Ao aplicar Clean Architecture, o fluxo de dados é crucial. O input, que pode vir de várias fontes como APIs, GraphQL ou GRPC, trafega pelas camadas da aplicação. Esse dado é processado pelos Use Cases, que determinam a intenção do software. Os dados então fluem pelas regras de negócio e são retornados como output, sendo formatados adequadamente para o solicitante pelo Presenter.

- **Ciclo de Entrada e Saída:**

O ciclo segue uma lógica de entrada e saída, onde o dado é recebido, processado conforme a intenção do Use Case, e o resultado é retornado como output. A transformação do output para o formato desejado é realizada pelo Presenter, garantindo uma resposta adequada para diferentes tipos de solicitantes, como web, GRPC ou GraphQL.

- **Limites Arquiteturais:**

Ao analisar o fluxo, é evidente que os limites arquiteturais são respeitados. Por exemplo, o Controller não chama diretamente a entidade, mas sim o Use Case, que coordena as operações e mantém a clareza nas responsabilidades.

- **Conclusão:**

A compreensão do ciclo de input versus output é essencial para a aplicação eficaz dos princípios da Clean Architecture. Ao seguir essa abordagem, o desenvolvedor consegue manter a clareza nas responsabilidades de cada camada e garantir a consistência do fluxo de dados na aplicação.

## Entendendo DTOs

O Data Transfer Object (DTO) é uma peça chave para compreender o fluxo de dados na arquitetura limpa. Ele desempenha um papel vital no transporte eficiente de dados entre os limites arquiteturais da aplicação.

**Propósito:**
O DTO é projetado para facilitar a transferência de dados, especialmente quando recebidos de sistemas externos, como APIs web. Funciona como um "envelope" que encapsula os dados necessários para serem processados pelo Use Case.

**Características:**
- O DTO é anêmico, carece de comportamento e regras de negócio. É estritamente uma estrutura de dados.
- Pode ser qualquer tipo de dado acessível, não necessariamente uma classe ou struct.
- Utilizado tanto para dados de entrada (input) quanto para dados de saída (output).
  
**Uso na Clean Architecture:**
- Normalmente, os dados de input são enviados para os Use Cases por meio de DTOs.
- Cada intenção do sistema pode exigir DTOs diferentes, adaptados às necessidades específicas de cada caso de uso.
- DTOs de input e output podem variar, pois a estrutura dos dados pode diferir nas operações de criação, alteração, etc.

**Fluxo de Uso:**
- Os dados são recebidos pela API e passam pelo Controller, que extrai os dados significativos da requisição.
- Esses dados são encapsulados em um DTO e enviados para o Use Case, que os processa conforme as regras de negócio.
- O resultado do Use Case é então enviado de volta ao Controller em um DTO de output.
- O Controller utiliza esse DTO para criar um objeto de resposta e retorna os dados processados à API.

## Presenters

Presenters são objetos de transformação essenciais na arquitetura limpa. Seu papel fundamental é receber dados, geralmente em forma de DTO de output, e adequá-los ao formato correto para entrega, como JSON, XML, ou outros, permitindo uma resposta consistente e personalizada.

**Função:**
- Presenters atuam como intermediários após o processamento pelo Use Case, focando na apresentação e formatação dos dados.
- Responsáveis por adaptar o DTO de output para diferentes formatos exigidos pela aplicação ou sistemas externos.
- Não se concentram na lógica de negócios, mas sim na apresentação dos resultados de forma adequada.

**Uso na Clean Architecture:**
- Após a execução do Use Case, o resultado, um DTO de output, é passado para o Presenter.
- O Presenter, então, realiza a transformação dos dados, proporcionando formatos específicos, como JSON ou XML, conforme necessário.
- Permite a flexibilidade na apresentação dos resultados, atendendo aos requisitos de diferentes partes da aplicação ou sistemas externos.

**Exemplo Prático:**
- Suponha um DTO de output contendo informações sobre uma nova categoria criada.
- Após a execução do Use Case, o Presenter entra em cena para personalizar o formato da resposta.
- Utilizando métodos específicos, como `toJson()` ou `toXML()`, o Presenter adapta o DTO para o formato desejado (JSON ou XML).
- O resultado formatado é então enviado para o Controller, pronto para ser retornado à API, Command Line Interface, ou outro destino.

## Entities: Clean Arch vs DDD

Entities, na Clean Architecture, diferem das entities no Domain Driven Design (DDD). Na Clean Architecture, entities representam uma camada que encapsula as regras de negócio invariáveis e críticas da aplicação. Por outro lado, no DDD, entities são representações de objetos únicos na aplicação, muitas vezes parte de agregados.

**Entities na Clean Architecture:**
- Em Clean Architecture, entities são conceituadas como "Enterprise Business Rules", definindo uma camada invariável e sólida.
- A camada de entities mantém regras globais, permanecendo constante independentemente das mudanças na aplicação.
- A definição de entities na Clean Architecture é menos explícita em termos de como criar essas entidades, mas enfatiza a importância das regras de negócio invariáveis.

**Relação com DDD:**
- A abordagem para criar a camada de entities na Clean Architecture pode se beneficiar dos padrões e táticas definidos pelo Domain Driven Design (DDD).
- Entities na Clean Architecture podem ser correlacionadas com a resultante dos agregados e domain services do DDD.
- O DDD cria camadas fortes, como agregados, domain services, eventos, que podem compor as entities na Clean Architecture.

**Separação de Conceitos:**
- O conjunto de camadas de domínio no DDD, como agregados, domain services, contratos, e eventos, pode contribuir para a definição das entities na Clean Architecture.
- A separação clara entre as entities e os Use Cases é destacada, sendo que as entities contêm regras críticas e invariáveis, enquanto os Use Cases podem variar com base no fluxo da aplicação.

**Clean Architecture em Prática:**
- Clean Architecture destaca a importância da camada de entities para encapsular as regras de negócio e fornece uma estrutura flexível e clara para o desenvolvimento de sistemas robustos.
- Os dados de várias fontes, como Web, Devices, DB, External Interfaces e UI, podem interagir com as entities, que geram valor para o negócio e retornam dados processados.