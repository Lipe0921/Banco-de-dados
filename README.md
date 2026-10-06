# 🚗 ERP Prime Funilaria — Modelagem Lógica de Banco de Dados

Projeto acadêmico focado na transição do Modelo Conceitual (DER) para o Modelo Lógico (Relacional), aplicando regras de integridade referencial, cardinalidades e auditoria de entidades.

---

## 👥 Participantes

| Nome | Função |
| :--- | :--- |
| **Felipe de Souza Ferreira** | Modelagem Lógica & Documentação |
| **[Nome do Integrante 2]** | Diagramação DER & Mapeamento |
| **[Nome do Integrante 3]** | Regras de Negócio & Auditoria |
| **[Nome do Integrante 4]** | Código DBML & Dicionário de Dados |

---

## 📐 Diagrama Entidade-Relacionamento (DER Lógico)

```mermaid
erDiagram
    CLIENTE ||--o{ VEICULO : "possuim (1:N)"
    CLIENTE ||--o{ ORDEM_SERVICO : "solicita (1:N)"
    VEICULO ||--o{ ORDEM_SERVICO : "associado_a (1:N)"
    FUNCIONARIO ||--o{ ORDEM_SERVICO : "atende (1:N)"
    ORDEM_SERVICO ||--o{ ORCAMENTO : "gera (1:N)"
    ORCAMENTO ||--o{ PAGAMENTO : "gera_pagamento (1:N)"
    ORCAMENTO ||--|{ ITEM_ORCAMENTO : "contem (1:N - Fraca)"
    SERVICO ||--o{ ITEM_ORCAMENTO : "utilizado_em (1:N)"
    PECA ||--o{ ITEM_ORCAMENTO : "utilizado_em (1:N)"
    FORNECEDOR ||--o{ FORNECEDOR_PECA : "fornece (1:N)"
    PECA ||--o{ FORNECEDOR_PECA : "composta_por (1:N)"

    CLIENTE {
        int id_cliente PK
        string nome
        string cpf_cnpj
        string telefone
    }

    VEICULO {
        int id_veiculo PK
        string placa
        string chassi
        string cor
        int ano
        string marca
        string modelo
        int id_cliente FK
    }

    ORDEM_SERVICO {
        int id_os PK
        datetime data_abertura
        int id_veiculo FK
        string descricao_problema
        datetime previsao_entrega
        string status
        int id_cliente FK
        int id_funcionario FK
    }

    ORCAMENTO {
        int id_orcamento PK
        int id_os FK
        datetime data_orcamento
        date validade
        decimal valor_total
        string status
    }

    ITEM_ORCAMENTO {
        int id_orcamento PK_FK
        int nr_item PK
        int id_servico FK
        int id_peca FK
        int quantidade
        decimal valor_unitario
        decimal valor_total
    }

    FORNECEDOR_PECA {
        int id_fornecedor PK_FK
        int id_peca PK_FK
        decimal preco_compra
        date data_atualizacao
    }
