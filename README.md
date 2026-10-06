# 🚗 Sistema de Gestão para Funilaria

Projeto acadêmico de Engenharia de Software desenvolvido para modelar um sistema de gerenciamento de uma funilaria.

O sistema tem como objetivo organizar as principais informações e processos da empresa, permitindo o gerenciamento de clientes, veículos, ordens de serviço, funcionários, orçamentos, serviços, peças, fornecedores e pagamentos.

---

## 📌 Sobre o Projeto

O projeto consiste na modelagem de um banco de dados para uma funilaria.

A proposta é representar, de forma estruturada, o fluxo de atendimento de um cliente e de seu veículo, desde o cadastro até a abertura de uma ordem de serviço, elaboração de orçamento, utilização de serviços e peças e realização dos pagamentos.

A modelagem foi desenvolvida utilizando conceitos de **Modelo Entidade-Relacionamento (MER)** e **modelo relacional**, utilizando chaves primárias, chaves estrangeiras e relacionamentos com diferentes cardinalidades.

---

## 🎯 Objetivos

### Objetivo Geral

Desenvolver uma estrutura de banco de dados capaz de armazenar e organizar as principais informações de uma funilaria, permitindo o controle dos processos relacionados aos seus clientes, veículos, serviços, peças, funcionários, fornecedores, orçamentos e pagamentos.

### Objetivos Específicos

- Cadastrar clientes;
- Cadastrar veículos;
- Associar veículos aos seus respectivos clientes;
- Registrar ordens de serviço;
- Registrar problemas apresentados pelos veículos;
- Controlar o status das ordens de serviço;
- Definir previsão de entrega;
- Associar funcionários às ordens de serviço;
- Criar e controlar orçamentos;
- Registrar serviços realizados;
- Registrar peças utilizadas;
- Controlar quantidade de peças em estoque;
- Cadastrar fornecedores;
- Relacionar fornecedores às peças fornecidas;
- Registrar valores de compra das peças;
- Registrar pagamentos;
- Manter a integridade e organização dos dados.

---

# 🗃️ Modelo do Banco de Dados

O banco de dados é composto pelas seguintes entidades:

- **CLIENTE**
- **VEICULO**
- **ORDEM_SERVICO**
- **FUNCIONARIO**
- **ORCAMENTO**
- **PAGAMENTO**
- **SERVICO**
- **PECA**
- **ITEM_ORCAMENTO**
- **FORNECEDOR**
- **FORNECEDOR_PECA**

---

# 📊 Diagrama Entidade-Relacionamento

O diagrama representa as entidades, seus atributos, chaves primárias (PK), chaves estrangeiras (FK) e os relacionamentos entre as entidades.

![Diagrama Entidade-Relacionamento](docs/diagrama-er.png)

---

# 🧩 Entidades

## 👤 CLIENTE

Representa os clientes da funilaria.

| Campo | Tipo | Chave |
|---|---|---|
| id_cliente | int | PK |
| nome | string | — |
| cpf_cnpj | string | — |
| telefone | string | — |

O cliente pode possuir um ou mais veículos e pode solicitar ordens de serviço.

---

## 🚘 VEICULO

Representa os veículos cadastrados no sistema.

| Campo | Tipo | Chave |
|---|---|---|
| id_veiculo | int | PK |
| placa | string | — |
| chassi | string | — |
| cor | string | — |
| ano | int | — |
| marca | string | — |
| modelo | string | — |
| id_cliente | int | FK |

Cada veículo está associado a um cliente.

### Relacionamento

**CLIENTE 1:N VEICULO**

Um cliente pode possuir vários veículos, enquanto cada veículo pertence a um cliente.

---

## 🔧 ORDEM_SERVICO

Representa o atendimento realizado pela funilaria.

| Campo | Tipo | Chave |
|---|---|---|
| id_os | int | PK |
| data_abertura | datetime | — |
| id_veiculo | int | FK |
| descricao_problema | string | — |
| previsao_entrega | datetime | — |
| status | string | — |
| id_cliente | int | FK |
| id_funcionario | int | FK |

A ordem de serviço registra o problema apresentado, a previsão de entrega e o status do atendimento.

Também identifica o cliente, o veículo e o funcionário relacionados ao atendimento.

---

## 👨‍🔧 FUNCIONARIO

Representa os funcionários da funilaria.

| Campo | Tipo | Chave |
|---|---|---|
| id_funcionario | int | PK |
| nome | string | — |
| cpf | string | — |
| cargo | string | — |
| telefone | string | — |
| data_contratacao | date | — |

Os funcionários são responsáveis pelo atendimento das ordens de serviço.

### Relacionamento

**FUNCIONARIO 1:N ORDEM_SERVICO**

Um funcionário pode atender várias ordens de serviço.

---

## 💰 ORCAMENTO

Representa o orçamento relacionado a uma ordem de serviço.

| Campo | Tipo | Chave |
|---|---|---|
| id_orcamento | int | PK |
| id_os | int | FK |
| data_orcamento | datetime | — |
| validade | date | — |
| valor_total | decimal | — |
| status | string | — |

O orçamento registra o valor total estimado, a data de elaboração, sua validade e seu status.

---

## 💳 PAGAMENTO

Representa os pagamentos realizados para os orçamentos.

| Campo | Tipo | Chave |
|---|---|---|
| id_pagamento | int | PK |
| id_orcamento | int | FK |
| data_pagamento | datetime | — |
| valor | decimal | — |
| forma_pagamento | string | — |
| status | string | — |

Permite registrar informações como:

- Data do pagamento;
- Valor pago;
- Forma de pagamento;
- Status do pagamento.

Um orçamento pode possuir registros de pagamento.

---

## 🔨 SERVICO

Representa os serviços oferecidos pela funilaria.

| Campo | Tipo | Chave |
|---|---|---|
| id_servico | int | PK |
| descricao | string | — |
| valor_padrao | decimal | — |
| tempo_padrao_horas | decimal | — |
| ativo | boolean | — |

O cadastro permite manter os serviços disponíveis e seus valores e tempos padrão.

---

## 🔩 PECA

Representa as peças utilizadas pela funilaria.

| Campo | Tipo | Chave |
|---|---|---|
| id_peca | int | PK |
| descricao | string | — |
| preco_unitario | decimal | — |
| estoque | int | — |
| ativo | boolean | — |

A entidade permite controlar o estoque e os valores das peças.

---

## 📋 ITEM_ORCAMENTO

Representa os itens que compõem um orçamento.

| Campo | Tipo | Chave |
|---|---|---|
| id_item | int | PK |
| id_orcamento | int | FK |
| id_servico | int | FK |
| id_peca | int | FK |
| quantidade | int | — |
| valor_unitario | decimal | — |
| valor_total | decimal | — |

Essa entidade permite detalhar os serviços e peças relacionados a cada orçamento.

O valor total de um item pode ser calculado através de:

```text
valor_total = quantidade × valor_unitario
