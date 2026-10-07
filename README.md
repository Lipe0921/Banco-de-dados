# Projeto Integrador — Sistema ERP para Funilaria

## Modelagem de Dados

Projeto desenvolvido para a modelagem de dados de uma empresa do segmento de funilaria automotiva.

---

# 1. Identificação da Equipe

**Curso:** Engenharia de Software  
**Disciplina:** Modelagem de Dados  
**Projeto:** Sistema ERP para Funilaria

| Integrante | RA |
|---|---|
| FELIPE DE SOUZA FERREIRA | RA |
| Nome do integrante 2 | RA |
| Nome do integrante 3 | RA |
| Nome do integrante 4 | RA |

---

# 2. Caracterização da Empresa

## 2.1 Segmento de atuação

A empresa analisada atua no segmento de **funilaria automotiva**, realizando serviços relacionados à reparação e manutenção de veículos.

O funcionamento da empresa envolve o atendimento de clientes, cadastro de veículos, abertura de ordens de serviço, elaboração de orçamentos, utilização de serviços e peças, relacionamento com fornecedores e registro de pagamentos.

## 2.2 Produtos e serviços

A empresa trabalha principalmente com serviços de reparação automotiva, utilizando serviços e peças na composição dos orçamentos.

## 2.3 Principais clientes

Os clientes são pessoas que possuem ou são responsáveis por veículos e procuram a empresa para realizar serviços de reparação automotiva.

## 2.4 Principais setores e envolvidos

- **Clientes:** solicitam serviços e possuem os veículos atendidos.
- **Funcionários:** realizam o atendimento das ordens de serviço.
- **Atendimento:** realiza cadastros e abertura de ordens.
- **Orçamentos:** registra serviços e peças necessários.
- **Estoque:** controla as peças disponíveis.
- **Fornecedores:** fornecem peças utilizadas pela empresa.
- **Financeiro:** registra os pagamentos.

## 2.5 Funcionamento do negócio

O processo começa com o cliente, que possui um ou mais veículos e solicita um atendimento.

A empresa registra uma ordem de serviço relacionada ao cliente e ao veículo. A ordem possui data de abertura, descrição do problema, previsão de entrega, status e funcionário responsável.

A partir da ordem de serviço é gerado um orçamento. O orçamento possui data, validade, valor total e status.

O orçamento é composto por itens. Cada item representa um serviço ou uma peça utilizada na composição do orçamento.

As peças possuem controle de estoque e podem ser fornecidas por diferentes fornecedores. A relação entre peça e fornecedor registra o preço de compra e a data de atualização.

Após o orçamento, é registrado o pagamento correspondente.

---

# 3. Justificativa da Escolha do Negócio

A escolha de uma empresa de funilaria foi realizada devido à variedade de processos envolvidos na prestação de serviços automotivos.

O negócio apresenta diferentes informações que precisam estar relacionadas, como clientes, veículos, ordens de serviço, funcionários, orçamentos, serviços, peças, fornecedores e pagamentos.

Essa característica permite aplicar conceitos de modelagem de dados, representando entidades, atributos, relacionamentos e cardinalidades.

---

# 4. Problemas e Necessidades Identificados

## 4.1 Problemas

| Problema | Impacto |
|---|---|
| Falta de centralização dos dados dos clientes | Dificuldade para consultar informações |
| Falta de organização dos dados dos veículos | Dificuldade para identificar os veículos |
| Controle das ordens de serviço | Dificuldade para acompanhar atendimentos |
| Controle dos orçamentos | Dificuldade para acompanhar valores e validade |
| Controle de peças | Dificuldade para acompanhar estoque |
| Controle de fornecedores | Dificuldade para identificar fornecedores |
| Controle de pagamentos | Dificuldade para acompanhar valores pagos |
| Controle dos funcionários | Dificuldade para identificar responsáveis |

## 4.2 Necessidades

O sistema deverá permitir:

- Cadastrar clientes;
- Cadastrar veículos;
- Relacionar veículos aos clientes;
- Registrar ordens de serviço;
- Relacionar ordens de serviço aos clientes e veículos;
- Identificar o funcionário responsável;
- Gerar orçamentos;
- Registrar itens dos orçamentos;
- Controlar serviços;
- Controlar peças;
- Controlar estoque;
- Cadastrar fornecedores;
- Relacionar fornecedores e peças;
- Registrar pagamentos;
- Consultar as informações cadastradas.

---

# 5. Principais Processos de Negócio

## 5.1 Cadastro de cliente

Cadastro de identificação, nome, CPF/CNPJ e telefone.

## 5.2 Cadastro de veículo

Cadastro de placa, chassi, cor, ano, marca e modelo, relacionado ao cliente.

## 5.3 Abertura de ordem de serviço

Registro da data de abertura, cliente, veículo, descrição do problema, previsão de entrega, status e funcionário responsável.

## 5.4 Geração do orçamento

Registro da data, validade, valor total e status.

## 5.5 Composição do orçamento

Registro dos itens, serviços ou peças, quantidade, valor unitário e valor total.

## 5.6 Controle de peças

Controle da descrição, preço unitário, estoque e situação ativa/inativa.

## 5.7 Relacionamento com fornecedores

Relacionamento entre peças e fornecedores, com preço de compra e data de atualização.

## 5.8 Registro do pagamento

Registro da data, valor, forma de pagamento e status.

---

# 6. Requisitos Funcionais

- **RF01:** Cadastrar clientes.
- **RF02:** Consultar clientes.
- **RF03:** Cadastrar veículos.
- **RF04:** Associar veículo a cliente.
- **RF05:** Cadastrar funcionários.
- **RF06:** Cadastrar serviços.
- **RF07:** Cadastrar peças.
- **RF08:** Cadastrar fornecedores.
- **RF09:** Abrir ordem de serviço.
- **RF10:** Associar ordem de serviço ao cliente.
- **RF11:** Associar ordem de serviço ao veículo.
- **RF12:** Associar funcionário à ordem de serviço.
- **RF13:** Gerar orçamento.
- **RF14:** Registrar itens do orçamento.
- **RF15:** Registrar serviços no orçamento.
- **RF16:** Registrar peças no orçamento.
- **RF17:** Controlar estoque.
- **RF18:** Relacionar fornecedores e peças.
- **RF19:** Registrar preço de compra.
- **RF20:** Registrar pagamento.
- **RF21:** Consultar ordens de serviço.
- **RF22:** Consultar orçamentos.

---

# 7. Requisitos Não Funcionais

- **RNF01 — Segurança:** proteger as informações armazenadas.
- **RNF02 — Controle de acesso:** permitir operações conforme permissões.
- **RNF03 — Integridade:** preservar a integridade dos relacionamentos.
- **RNF04 — Confiabilidade:** manter os dados consistentes.
- **RNF05 — Usabilidade:** apresentar informações de forma clara.
- **RNF06 — Desempenho:** apresentar informações em tempo adequado.
- **RNF07 — Disponibilidade:** manter o sistema disponível durante o funcionamento da empresa.

---

# 8. Regras de Negócio

- **RN01:** Um cliente pode possuir nenhum ou vários veículos.
- **RN02:** Cada veículo deve estar associado a exatamente um cliente.
- **RN03:** Um cliente pode solicitar nenhuma ou várias ordens de serviço.
- **RN04:** Cada ordem de serviço deve estar associada a exatamente um cliente.
- **RN05:** Um veículo pode estar relacionado a nenhuma ou várias ordens de serviço.
- **RN06:** Cada ordem de serviço deve estar associada a exatamente um veículo.
- **RN07:** Um funcionário pode atender nenhuma ou várias ordens de serviço.
- **RN08:** Cada ordem possui exatamente um funcionário responsável.
- **RN09:** Cada ordem de serviço gera exatamente um orçamento.
- **RN10:** Cada orçamento pertence a exatamente uma ordem de serviço.
- **RN11:** Um orçamento pode possuir nenhum ou vários itens.
- **RN12:** Cada item pertence a exatamente um orçamento.
- **RN13:** Um serviço pode estar relacionado a nenhum ou vários itens.
- **RN14:** Um item pode estar relacionado a no máximo um serviço.
- **RN15:** Uma peça pode estar relacionada a nenhum ou vários itens.
- **RN16:** Um item pode estar relacionado a no máximo uma peça.
- **RN17:** Cada item de orçamento deve estar associado a exatamente um serviço ou a uma peça. Um item não pode estar associado simultaneamente aos dois.
- **RN18:** Cada orçamento possui exatamente um pagamento.
- **RN19:** Cada pagamento está relacionado a exatamente um orçamento.
- **RN20:** Um fornecedor pode estar relacionado a nenhuma ou várias peças.
- **RN21:** Uma peça pode estar relacionada a nenhum ou vários fornecedores.
- **RN22:** A relação fornecedor/peça registra preço de compra e data de atualização.
- **RN23:** Cada peça possui uma quantidade de estoque registrada.
- **RN24:** Serviços podem ser ativos ou inativos.
- **RN25:** Peças podem ser ativas ou inativas.
- **RN26:** O cliente da ordem de serviço deve corresponder ao cliente proprietário do veículo.

---

# 9. Restrições e Políticas Organizacionais

1. Um veículo não pode ser cadastrado sem estar relacionado a um cliente.
2. Uma ordem de serviço não pode ser registrada sem cliente.
3. Uma ordem de serviço não pode ser registrada sem veículo.
4. Uma ordem de serviço deve possuir funcionário responsável.
5. Uma ordem de serviço gera exatamente um orçamento.
6. Um orçamento pertence a exatamente uma ordem de serviço.
7. Um orçamento pode possuir nenhum ou vários itens.
8. Cada item pertence a somente um orçamento.
9. Cada item deve representar uma peça ou um serviço.
10. Uma peça deve possuir controle de estoque.
11. Uma peça pode possuir diferentes fornecedores.
12. Um fornecedor pode fornecer diferentes peças.
13. O preço de compra é registrado na relação fornecedor/peça.
14. A data de atualização é registrada na relação fornecedor/peça.
15. Cada orçamento possui um pagamento.
16. Cada pagamento está relacionado a um único orçamento.
17. Serviços e peças podem ser classificados como ativos ou inativos.
18. O cliente relacionado à ordem deve ser compatível com o cliente proprietário do veículo.

---

# 10. Fluxogramas

## 10.1 Fluxograma — Cadastro e Ordem de Serviço

![Fluxograma da Ordem de Serviço](diagramas/fluxograma_ordem_servico.png)

```text
INÍCIO
  ↓
Cliente solicita atendimento
  ↓
Cliente cadastrado?
  ├─ NÃO → Cadastrar cliente
  └─ SIM
       ↓
Identificar veículo
       ↓
Veículo cadastrado?
  ├─ NÃO → Cadastrar veículo
  └─ SIM
       ↓
Registrar problema
       ↓
Registrar ordem de serviço
       ↓
Associar cliente, veículo e funcionário
       ↓
Definir previsão e status
       ↓
FIM
```

## 10.2 Fluxograma — Geração do Orçamento

![Fluxograma do Orçamento](diagramas/fluxograma_orcamento.png)

```text
INÍCIO
  ↓
Selecionar ordem de serviço
  ↓
Analisar problema
  ↓
Definir serviços e peças
  ↓
Criar orçamento
  ↓
Adicionar itens
  ↓
Definir quantidade e valores
  ↓
Calcular valor total
  ↓
Definir validade e status
  ↓
FIM
```

## 10.3 Fluxograma — Peças e Fornecedores

![Fluxograma de Peças e Fornecedores](diagramas/fluxograma_pecas_fornecedores.png)

```text
INÍCIO
  ↓
Identificar peça
  ↓
Peça cadastrada?
  ├─ NÃO → Cadastrar peça
  └─ SIM
       ↓
Verificar estoque
       ↓
Identificar fornecedor
       ↓
Fornecedor cadastrado?
  ├─ NÃO → Cadastrar fornecedor
  └─ SIM
       ↓
Relacionar fornecedor e peça
       ↓
Registrar preço de compra e atualização
       ↓
FIM
```

## 10.4 Fluxograma — Pagamento

![Fluxograma de Pagamento](diagramas/fluxograma_pagamento.png)

```text
INÍCIO
  ↓
Selecionar orçamento
  ↓
Verificar valor
  ↓
Registrar pagamento
  ↓
Informar data, valor, forma e status
  ↓
Associar pagamento ao orçamento
  ↓
FIM
```

---

# 11. Entidades

| Entidade | Descrição |
|---|---|
| CLIENTE | Dados dos clientes |
| VEICULO | Dados dos veículos |
| ORDEM_SERVICO | Ordens de serviço |
| FUNCIONARIO | Dados dos funcionários |
| ORCAMENTO | Orçamentos |
| PAGAMENTO | Pagamentos |
| SERVICO | Serviços disponíveis |
| PECA | Peças disponíveis |
| FORNECEDOR | Dados dos fornecedores |
| ITEM_ORCAMENTO | Itens que compõem o orçamento |
| FORNECEDOR_PECA | Relação entre fornecedores e peças |

---

# 12. Atributos

## 12.1 CLIENTE

| Atributo | Tipo | Descrição |
|---|---|---|
| id_cliente | int | Identificador único do cliente |
| nome | string | Nome do cliente |
| cpf_cnpj | string | CPF ou CNPJ |
| telefone | string | Telefone de contato |

## 12.2 VEICULO

| Atributo | Tipo | Descrição |
|---|---|---|
| id_veiculo | int | Identificador do veículo |
| placa | string | Placa |
| chassi | string | Número do chassi |
| cor | string | Cor |
| ano | int | Ano |
| marca | string | Marca |
| modelo | string | Modelo |
| id_cliente | int | Cliente proprietário |

## 12.3 ORDEM_SERVICO

| Atributo | Tipo | Descrição |
|---|---|---|
| id_os | int | Identificador da ordem |
| data_abertura | datetime | Data e hora de abertura |
| id_veiculo | int | Veículo relacionado |
| descricao_problema | string | Problema apresentado |
| previsao_entrega | datetime | Previsão de entrega |
| status | string | Situação da ordem |
| id_cliente | int | Cliente relacionado |
| id_funcionario | int | Funcionário responsável |

## 12.4 FUNCIONARIO

| Atributo | Tipo | Descrição |
|---|---|---|
| id_funcionario | int | Identificador do funcionário |
| nome | string | Nome |
| cpf | string | CPF |
| cargo | string | Cargo |
| telefone | string | Telefone |
| data_contratacao | date | Data de contratação |

## 12.5 ORCAMENTO

| Atributo | Tipo | Descrição |
|---|---|---|
| id_orcamento | int | Identificador do orçamento |
| id_os | int | Ordem relacionada |
| data_orcamento | datetime | Data de criação |
| validade | date | Validade |
| valor_total | decimal | Valor total |
| status | string | Situação |

## 12.6 PAGAMENTO

| Atributo | Tipo | Descrição |
|---|---|---|
| id_pagamento | int | Identificador |
| id_orcamento | int | Orçamento relacionado |
| data_pagamento | datetime | Data |
| valor | decimal | Valor pago |
| forma_pagamento | string | Forma de pagamento |
| status | string | Situação |

## 12.7 SERVICO

| Atributo | Tipo | Descrição |
|---|---|---|
| id_servico | int | Identificador |
| descricao | string | Descrição |
| valor_padrao | decimal | Valor padrão |
| tempo_padrao_horas | decimal | Tempo estimado |
| ativo | boolean | Situação do serviço |

## 12.8 PECA

| Atributo | Tipo | Descrição |
|---|---|---|
| id_peca | int | Identificador |
| descricao | string | Descrição |
| preco_unitario | decimal | Preço unitário |
| estoque | int | Quantidade em estoque |
| ativo | boolean | Situação da peça |

## 12.9 FORNECEDOR

| Atributo | Tipo | Descrição |
|---|---|---|
| id_fornecedor | int | Identificador |
| nome | string | Nome |
| cnpj | string | CNPJ |
| endereco | string | Endereço |
| telefone | string | Telefone |
| email | string | E-mail |

## 12.10 ITEM_ORCAMENTO

| Atributo | Tipo | Descrição |
|---|---|---|
| id_item | int | Identificador do item |
| id_orcamento | int | Orçamento relacionado |
| id_servico | int | Serviço, quando o item representar serviço |
| id_peca | int | Peça, quando o item representar peça |
| quantidade | int | Quantidade |
| valor_unitario | decimal | Valor unitário |
| valor_total | decimal | Valor total |

### Regra do item

Cada item de orçamento deve representar **exatamente um tipo de item: serviço ou peça**.

Portanto, `id_servico` ou `id_peca` deve ser informado, mas os dois não podem ser preenchidos simultaneamente.

## 12.11 FORNECEDOR_PECA

| Atributo | Tipo | Descrição |
|---|---|---|
| id_fornecedor | int | Fornecedor relacionado |
| id_peca | int | Peça relacionada |
| preco_compra | decimal | Preço de compra |
| data_atualizacao | date | Data de atualização |

`id_fornecedor` e `id_peca` identificam a associação entre fornecedor e peça.

---

# 13. Relacionamentos

| Relacionamento | Entidades |
|---|---|
| possui | CLIENTE — VEICULO |
| solicita | CLIENTE — ORDEM_SERVICO |
| associado_a | VEICULO — ORDEM_SERVICO |
| atende | FUNCIONARIO — ORDEM_SERVICO |
| gera | ORDEM_SERVICO — ORCAMENTO |
| gera_pagamento | ORCAMENTO — PAGAMENTO |
| contém | ORCAMENTO — ITEM_ORCAMENTO |
| utilizado_em | SERVICO — ITEM_ORCAMENTO |
| utilizado_em | PECA — ITEM_ORCAMENTO |
| fornece | FORNECEDOR — FORNECEDOR_PECA |
| participa | PECA — FORNECEDOR_PECA |

---

# 14. Cardinalidades

As cardinalidades devem corresponder às representadas no DER entregue pela equipe.

| Relacionamento | Cardinalidade |
|---|---|
| CLIENTE — VEICULO | 1:N |
| CLIENTE — ORDEM_SERVICO | 1:N |
| VEICULO — ORDEM_SERVICO | 1:N |
| FUNCIONARIO — ORDEM_SERVICO | 1:N |
| ORDEM_SERVICO — ORCAMENTO | 1:1 |
| ORCAMENTO — PAGAMENTO | 1:1 |
| ORCAMENTO — ITEM_ORCAMENTO | 1:N |
| SERVICO — ITEM_ORCAMENTO | 1:N |
| PECA — ITEM_ORCAMENTO | 1:N |
| FORNECEDOR — PECA | N:N, resolvido por FORNECEDOR_PECA |

---

# 15. Chaves Primárias e Estrangeiras

| Tabela | Chave primária | Chaves estrangeiras |
|---|---|---|
| CLIENTE | id_cliente | — |
| VEICULO | id_veiculo | id_cliente |
| FUNCIONARIO | id_funcionario | — |
| ORDEM_SERVICO | id_os | id_cliente, id_veiculo, id_funcionario |
| ORCAMENTO | id_orcamento | id_os |
| PAGAMENTO | id_pagamento | id_orcamento |
| SERVICO | id_servico | — |
| PECA | id_peca | — |
| FORNECEDOR | id_fornecedor | — |
| ITEM_ORCAMENTO | id_item | id_orcamento, id_servico, id_peca |
| FORNECEDOR_PECA | id_fornecedor + id_peca | id_fornecedor, id_peca |

---

# 16. Diagrama Entidade-Relacionamento

O DER deverá ser disponibilizado no repositório dentro da pasta `diagramas`.

![Diagrama Entidade-Relacionamento](diagramas/DER.png)

---

# 17. Justificativas Técnicas

## 17.1 Uso de chaves primárias

Cada entidade possui um identificador próprio para permitir sua identificação única e facilitar os relacionamentos entre as tabelas.

## 17.2 Uso de chaves estrangeiras

As chaves estrangeiras representam os relacionamentos entre as entidades e garantem a referência entre os registros.

## 17.3 ITEM_ORCAMENTO

A entidade `ITEM_ORCAMENTO` permite representar tanto serviços quanto peças dentro de um orçamento.

Para evitar ambiguidade, cada item deve representar **um único tipo**: serviço ou peça. Assim, `id_servico` e `id_peca` não devem ser preenchidos simultaneamente.

## 17.4 FORNECEDOR_PECA

A entidade associativa `FORNECEDOR_PECA` é utilizada para representar a relação muitos-para-muitos entre fornecedores e peças.

Ela também permite armazenar informações próprias dessa associação, como preço de compra e data de atualização.

---

# 18. Dicionário de Dados

O dicionário de dados apresenta as entidades, atributos, tipos e descrições utilizadas na modelagem.

O documento completo deverá ser disponibilizado no repositório em:

`documentos/dicionario_de_dados.pdf`

---

# 19. Estrutura do Repositório

```text
projeto-funilaria/
│
├── README.md
│
├── diagramas/
│   ├── DER.png
│   ├── fluxograma_ordem_servico.png
│   ├── fluxograma_orcamento.png
│   ├── fluxograma_pecas_fornecedores.png
│   └── fluxograma_pagamento.png
│
└── documentos/
    └── dicionario_de_dados.pdf
```

---

# 20. Considerações Finais

A modelagem apresentada organiza os principais dados e processos envolvidos no funcionamento de uma empresa de funilaria.

O modelo contempla clientes, veículos, funcionários, ordens de serviço, orçamentos, pagamentos, serviços, peças e fornecedores, permitindo representar os principais relacionamentos necessários para o funcionamento do negócio.

O DER e o dicionário de dados servem como base para as próximas etapas do desenvolvimento do sistema.

---

## Integrantes

- Nome do integrante 1 — RA
- Nome do integrante 2 — RA
- Nome do integrante 3 — RA
- Nome do integrante 4 — RA
