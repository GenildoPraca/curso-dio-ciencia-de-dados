# Sistema de controle e gerenciamento de execução de ordens de serviço em uma oficina mecânica
## Narrativa e descrição da decisão adotada no modelo
* Clientes levam veículos à oficina mecânica para conserto ou revisões periódicas
    > Foi criado um relacionamento muitos para muitos porque um mesmo veículo pode trocar de proprietário. Desse modo será possível identificar com precisão qual cliente realizou o serviço no veículo e em qual data. O proprietário atual é identificado pelo registro ativo no momento (data_fim vazia)
* Cada veículo é designado a uma equipe responsável pelo orçamento e execução
    > Como a mesma equipe é responsável pelo orçamento e execução foi criado um relacionamento entre as entidades O.S. e equipe
    > O atributo **Tipo_OS** determina se é um conserto ou uma revisão periódica
    > Apesar do valor total ser possível obter pela soma dos valores das peças e serviços que compõem a O.S. foi incluído o campo na entidade para dispensar cálculos adicionais na exibição.
* Especialidade
    > Para especialidade foi criada uma entidade a fim de evitar redundância no cadastro dos mecânicos. Essa entidade também é utilizada na tabela de valores dos serviços com intuito de detalhar qual serviço pertence a cada especialidade
* Itens da O.S.
    > As entidades **Peça_Ordem_serviço** e **Serviço_Ordem_Serviço** armazenam as peças e serviços realizados, ambas possuem um valor unitário no momento da venda para permitir identificar o valor praticado no orçamento e execução independente de atualizações nas entidades básicas (Peças e Serviços) 
