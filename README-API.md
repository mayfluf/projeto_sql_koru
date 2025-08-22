# projeto_sql_koru

# Projeto de Integração com Google Books API - Livraria DevSaber

## Objetivo do Projeto

Este projeto tem como objetivo realizar a coleta de dados sobre livros relacionados à programação em Python, utilizando a **Google Books API**. Os dados extraídos foram organizados em uma planilha **CSV**, armazenados na nuvem via **Google Cloud Storage** e posteriormente analisados no **BigQuery** com **SQL**. A API foi criada apenas para fins de conhecimento, seus dados nao foram integrados ao sql 

---

## Tecnologias Utilizadas

- **Google Colab**: Ambiente de desenvolvimento utilizado para execução de código Python e integração com a API.
- **Google Books API**: API pública utilizada para coletar informações sobre livros.
- **Pandas**: Biblioteca Python para manipulação e tratamento de dados.
- **Google Cloud Storage**: Armazenamento na nuvem para os arquivos CSV gerados.
- **BigQuery**: Plataforma de análise de dados em nuvem para integração e análise dos dados.
- **SQL**: Linguagem utilizada para consulta e análise de dados no BigQuery.

---

## Etapas do Projeto

### 1. Coleta de Dados via API

Foi realizada uma requisição à **Google Books API** para buscar livros relacionados ao tema **"Python Programming"**. A requisição foi feita diretamente no **Google Colab**, utilizando os seguintes parâmetros:

```python
url = "https://www.googleapis.com/books/v1/volumes"
params = {
    "q": "python programming",
    "maxResults": 40  # Selecionamos 40 resultados
}
response = requests.get(url, params=params)
response.raise_for_status()
data = response.json()
