***Projeto Modelagem de Dados - Engenharia de Dados:***
---

Este repositório contém a modelagem de dados de uma loja fictícia de venda de bicicletas, que realiza tanto operações transacionais do dia a dia (como vendas, cadastros, estoque), quanto análises gerenciais (como total de vendas por mês, por estado, por gênero etc).

Foram criados dois modelos distintos:

🧩 Modelo Relacional (OLTP) – para registrar e processar as transações da operação.

📊 Modelo Dimensional (OLAP) – para análise de dados e apoio à tomada de decisão.

---
🔹 Banco de Dados Relacional (OLTP)

✅ O que é:

Um banco de dados relacional armazena informações em tabelas interligadas por relacionamentos (chaves primárias e estrangeiras). É usado principalmente para registrar transações de forma segura, rápida e confiável.

🕒 Quando usar:

Sistemas que fazem operações de leitura e escrita frequentes

Aplicações transacionais, como:

Sistemas de vendas

Cadastro de clientes e produtos

Estoque, pagamentos e entregas

🟢 Vantagens:

Consistência e integridade dos dados com regras de relacionamento.

Redução de redundância (com normalização).

Alta performance para operações rápidas (INSERT, UPDATE, DELETE).

Suporte a transações ACID (garantia de que todas as operações ocorrem corretamente).

📌 Exemplo neste projeto:

Cadastro de clientes, produtos e itens de pedidos.

Relacionamento entre essas tabelas com chaves estrangeiras.

<p align="center">
  <img src="https://github.com/user-attachments/assets/c212cea9-62df-4fbb-867a-ef42aeed7d97" width="800px" />
</p>

---
🔸 Banco de Dados Dimensional (OLAP)

✅ O que é:

Um banco de dados dimensional é estruturado para facilitar consultas analíticas, geralmente em modelos estrela ou floco de neve. Ele organiza os dados em uma tabela de fato (eventos medidos, como vendas) conectada a várias tabelas de dimensões (como tempo, cliente, produto).

🕒 Quando usar:

Para criar dashboards, relatórios e análises históricas

Em projetos de Business Intelligence (BI) ou Data Warehousing

Quando há necessidade de agregar dados em grandes volumes

🟢 Vantagens:

Desempenho otimizado para consultas complexas.

Facilidade de entendimento dos dados por analistas e áreas de negócio.

Permite realizar análises como:

Vendas por região, período, categoria de produto, etc.

Ideal para extração de insights.

📌 Exemplo neste projeto:

Fato de vendas conectada a dimensões como:

Produto (produto, preço)

Cliente (estado, sexo, status)

Tempo (ano, mês, dia)

<p align="center">
  <img src="https://github.com/user-attachments/assets/a7993a0f-75d9-45ad-b49b-a40fd421527d" width="800px" />
</p>

---
📁 Estrutura do Projeto
```
Modelagem_Dados_Engenharia_Dados/
├── modelo-relacional/
│   ├── 1.CreateTable.sql
│   ├── 2.InsertClientes.sql
│   ├── 3.InsertIntoProdutos.sql
│   ├── 4.InsertIntoVendedores.sql
│   ├── 5.InsertIntoVendas.sql
│   ├── 6.InsertItensVenda.sql
│   └── diagrama-relacional.png
│
├── modelo-dimensional/
│   ├── 1.CreateTable.sql
│   ├── 2.InsertDimensaoTempo.sql
│   ├── 3.Desnormalizacao.sql
│   ├── 4.KPI.sql
│   └── diagrama-dimensional.png
│
└── README.md
```
