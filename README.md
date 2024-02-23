# Teste Seleção Desenvolvedor Web
## Abaixo segue os testes para a seleção de Desenvolvedores Web


### Nossa Stack:
Para os testes os requisitos abaixo não são obrigatórios, eles servem apenas como base para as tecnologias você terá contato durante o trabalho.
Requisistos de  Frontend
 - HTML
 - Framework React.js
 - Requisições HTTP com fetch ou axios

Requisistos de Backend
 - Python
 - Django
 - Django Rest Framework

Requisistos de SQL
 - Relatórios Básico com SQL

### Como aplicar os testes
Para aplicar basta criar um repositório público no github, codificar os teste e enviar o link para o email: dev@easygestor.com com o assunto **teste dev-web 2024**

Os testes estão dividos em três partes:
- Frontend
- Backend
- SQL

Cada uma das partes possui duas opções, você pode escolher uma das opções para codificar ou até mesmo escolher as duas! Só serão consideradas as opções que estiverem finalizadas.
Olha, também é importante que os passos para a execução do projeto estejam bem escritos.
### Ex: Projeto Cadastro de cliente
Clone o repositório
```bash
    git clone git@github.com:usuario/projeto-cadastro-cliente.git
```
Acesse a pasta do projeto
```bash
    cd projeto-cadastro-cliente
```
Baixe as dependências
```bash
    npm install
```
Starte o projeto
```bash
    npm start
```
No caso do SQL não precisa o passo a passo.

### Segue as opções de testes.


## Frontend
Utilize o Framework React.js para codificar pelo menos uma das opções abaixo.
- Documentação React.js https://react.dev/learn
### Opção 1: Formulário Cadasto de Cliente
**Objetivo**: Codificar um componente funcional React.js que renderize um formulário de cadastro de cliente com os campos: nome, cpf, email, telefone, sexo e nascimento. Utilize os hooks: **useState** para guardar os dados. Os dados devem ser exibidos em console.debug no formato do JSON.
```json
    {
        "nome": "Jhon Doe",
        "cpf": "99999999999",
        "email": "jhon.doe@email.com",
        "telefone": "99999999999",
        "sexo": "Masculino",
        "nascimento": "20/11/1996",
    }
```
**Critérios que serão avaliados**: codificação de um componente básico e o seu fluxo de dados.

### Opção 2: React Pokedex
**Objetivo**: Codificar um componente funcional simples que consuma a API Pokedex para buscar um Pokemon pelo nome e exibir quantas habilidades ele tem, no formato do JSON abaixo. As habilidades devem exibidas em uma lista.
```json
{
    "abilities": [
        {
            "name": "synchronize",
        },
        {
            "name": "inner-focus",
        }
    ]
}
```

**Critérios que serão avaliados**: Executar consumo de API, formatação e exibição dos dados.

API Pokedex: https://pokeapi.co/api/v2/pokemon/umbreon

## Backend
Codifique utilizando a linguagem Python, ou utilize framework Django ou Django Rest Framework para codificar uma das opções abaixo.
- Documentação Django https://docs.djangoproject.com/en/5.0/intro/tutorial01/
- Documentação Django REST framework https://www.django-rest-framework.org/tutorial/quickstart/

### Opção 1: Script Python Busca CNPJ
**Objetivo**: Codifique um script python que realize a consulta do CNPJ em uma empresa na API do receitaws. O script deve receber como entrada um cnpj e exibir na tela os dados no formtado do JSON abaixo:
Utilize a biblioteca requests para realizar a requisição para o endpoint: https://receitaws.com.br/v1/cnpj/49310078000100
```json
    {
        "razao_social": "UBER DO BRASIL TECNOLOGIA LTDA.",
        "codigo_atividade_principal": "74.90-1-04",
        "endereco": {
            "numero": "949",
            "cep": "05.426-200",
            "municipio": "SAO PAULO",
            "estado": "SP",
        }
    }
```
CNPJ Exemplo: 17.895.646/0001-87
**Critérios que serão avaliados**: Criar uma estrutura básica de um projeto Django e compreender a comunicação do projeto Djanco com apis de terceiros.


### Opção 2: API Crud de Produtos
**Objetivo**: Criar uma API para CRUD de produtos (nome, valor, cod_barras).
**Critérios que serão avaliados**: Criar uma estrutura básica de um projeto Django que faça a criação, edição, listagem e delete produtos.
## SQL

Analise a estrutura de base de dados gerada a partir da SQL abaixo e utilize a linguagem SQL para extrair um dos relatórios abaixo.

- SQL cheatsheet https://devhints.io/mysql

```sql
-- Tabela de Produtos
CREATE TABLE products (
    product_id SERIAL PRIMARY KEY,
    name VARCHAR(255) NOT NULL,
    description TEXT,
    price DECIMAL(10, 2) NOT NULL,
    created_at TIMESTAMP WITHOUT TIME ZONE DEFAULT CURRENT_TIMESTAMP
);

-- Tabela de Vendas
CREATE TABLE sales (
    sale_id SERIAL PRIMARY KEY,
    product_id INT NOT NULL,
    quantity INT NOT NULL,
    sale_price DECIMAL(10, 2) NOT NULL,
    sale_date DATE NOT NULL,
    created_at TIMESTAMP WITHOUT TIME ZONE DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (product_id) REFERENCES products (product_id)
);
```

### Opção 1: Vendas do mês
**Objetivo**: Desenvolva uma SQL que pegue todas as vendas de um produto dentro de um período, ex todas as vendas do produto XPTO feitas fevereiro de 2024.
**Critérios que serão avaliados**: Utilizar os comados **SELECT**, **FROM** e **WHERE** para extrair o relatório.

### Opção 2: Produtos mais vendidos
**Objetivo**: Desenvolva uma SQL para listar os produtos mais vendidos em um intervalo de tempo, exemplo: produtos mais vendido em fevereiro de 2024.
**Critérios que serão avaliados**: Utilizar os comados **SELECT**, **FROM**,**WHERE**, **GROUP BY** e **ORDER BY** para extrair o relatório.

# Let's Bora! Boa sorte!

![YOU DO IT!](http://www.quickmeme.com/img/33/3347e87ac569bd717b2ddb8e1c8d0ccb456772106696a51d5bea52fc1b6d45d9.jpg "Título opcional da imagem")
