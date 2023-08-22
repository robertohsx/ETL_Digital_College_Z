
# Projeto: Criando um Banco de dados e tabelas dimensões com PostgreSQL - Usando o PENTAHO

O projeto tem como desafio criar um Banco de Dados Dimensional, usando a transformação ETL de um arquivo CSV no Pentaho, criando tabelas dimensões e fato, realizando um output para o banco de dados Postgres, com o objetivo de ter eficiência e a rapidez nas consultas. 💼🔗


## 🚀 Começando

Neste projeto, realizamos a criação de um banco de dados roberto_DA_06 e o schema estoque sendo essa a base de todo o projeto.

> **O projeto foi realizado em 3 etapas:**

1. **Análise do Arquivo CSV**: Nesta etapa, analisamos o arquivo tbestoque.csv recebido, para entender os dados a serem análisados e fazer a separação das dimensões e fato.

2. **Modelagem, Tratamento e Criação das Tabelas no Pentaho**: Nesta etapa, criamos 4 modelagens para tratamento e criação das tabelas no Postgres:
dim_produto, dim_fornecedor, dim_loja e tabela_fato.

Na modelagem utilizamos:

-**Select Values:** A etapa "Select Values" é usada para selecionar colunas específicas de um conjunto de dados. Ela permite que você escolha quais colunas deseja manter no fluxo de trabalho, descartando as que não são necessárias para a análise ou transformação. 

-**Sort Rows:** A etapa "Sort Rows" é usada para ordenar os registros de um conjunto de dados com base nos valores de uma ou mais colunas. Isso é útil quando você deseja ter os dados organizados em uma ordem específica antes de realizar outras operações ou análises.

-**Unique Rows:** A etapa "Unique Rows" é usada para eliminar registros duplicados de um conjunto de dados. Ela garante que apenas uma instância de cada combinação única de valores nas colunas selecionadas seja mantida, reduzindo redundâncias nos dados.

-**Table Output:** A etapa "Table Output" é usada para enviar os resultados do fluxo de trabalho do Pentaho para uma tabela de banco de dados. Isso permite que os dados transformados ou processados sejam inseridos, atualizados ou substituídos em uma tabela específica do banco de dados. Nesse projeto inserimos as tabelas em um banco de dados dimensional no Postgres.

3. **Checagem das tabelas nos postgres**: Nesta etapa, realizamos selects para validar as inserções das tabelas transformadas no pentaho para o postgres.

- Select da Dimensão Fornecedor
```sql
SELECT * FROM estoque.dim_fornecedor;
```
- Select da Dimensão loja
```sql
SELECT * FROM estoque.dim_loja;
```
- Select da Dimensão produto
```sql
SELECT * FROM estoque.dim_produto;
```
 - Select da Tabela Fato
```sql
SELECT * FROM estoque.tabela_fato;
``` 

## ⚙️ Arquivos no Repositório:

-**Arquivo .ktr do Pentaho**.

-**Arquivo CSV da base de Dados**.


🚀Obrigado!
* Compartilhe com outras pessoas esse projeto 📢;


---

💻 [Roberto Hellery](https://github.com/robertohsx)
