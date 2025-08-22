# Projeto: Pipeline de Dados e Análise com SQL no BigQuery — Livraria DevSaber

---
- Este projeto tem como objetivo construir um data warehouse na plataforma Google BigQuery para a Livraria DevSaber, uma loja online especializada em livros. A proposta é estruturar, ingerir e analisar os dados de vendas da loja, utilizando consultas SQL para responder perguntas de negócio relacionadas a clientes, produtos e desempenho comercial.


## Visão Geral do Pipeline
O projeto foi dividido em etapas fundamentais para garantir uma estrutura de dados eficiente e escalável:

1. Criação de Tabelas
Utilização do comando CREATE OR REPLACE TABLE para recriar tabelas sem erros.

- Estrutura organizada no padrão projeto.dataset.tabela.

- Tipos de dados utilizados:

- STRING para textos

- INT64 para números inteiros

- NUMERIC para valores decimais

- DATE, DATETIME, TIMESTAMP para datas e horários

---
2. Paradigma Sem Chaves
-O BigQuery não impõe restrições de PRIMARY KEY ou FOREIGN KEY.

- Relacionamentos são mantidos por meio de JOIN nas consultas SQL.

- Essa abordagem melhora a performance em grandes volumes de dados.
---

3. Consultas SQL e  Views
   
---

# Mini Projeto: Livraria DevSaber
Cenário: A Livraria DevSaber possui dados de vendas registrados e precisa estruturá-los para análise.

Missão: Criar um data warehouse com tabelas de clientes, produtos e vendas.

---

Objetivo: Utilizar SQL para responder perguntas como:

Quais produtos têm maior volume de vendas?

Quais clientes compram com mais frequência?

Qual estado compra mais?

---
# Coleta de Dados via Google Books API

Neste projeto, utilizei a **Google Books API** para coletar dados sobre livros relacionados à programação em Python. A API foi utilizada para buscar informações e detalhes relevantes dos livros.

### **Importante:**
Embora os dados tenham sido coletados da API e processados no projeto, **não houve modificação nos dados originais**. A ideia foi simplesmente extrair e organizar as informações para análise, sem alterar qualquer dado presente no mini projeto ou nos dados previamente armazenados. A coleta foi feita apenas para fins de aprendizado e análise, sem impacto nos dados existentes.

Os dados extraídos foram convertidos em um **arquivo CSV** e carregados no **Google Cloud Storage**, para posterior análise no **BigQuery**.

Este processo permitiu a integração dos dados da API com o restante das informações da **Livraria DevSaber** para fins de análise, sem interferir nos dados originais do projeto.

---
# Como Executar
-Crie um projeto no Google Cloud

-Configure o BigQuery e o Cloud Storage

-Estruture os datasets e tabelas conforme o modelo

-Ingestione os dados via batch ou streaming

-Execute as consultas SQL no BigQuery

-Crie views para automatizar análises recorrentes
