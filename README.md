# Teste Seleção Desenvolvedor Web


### Nossa Stack:
Para os testes os requisitos abaixo não são obrigatórios, eles servem apenas como base para as tecnologias você terá contato durante o trabalho.
##### Requisistos Frontend
 - HTML
 - Framework React.js
 - Requisições HTTP com fetch ou axios

##### Requisistos Backend
 - Python
 - Django
 - Django Rest Framework

##### Requisistos de SQL
 - Relatórios Básico com SQL

 ##### Requisistos Linux
 - Linha de comandos
 - Shell Scripting

### Como aplicar os testes
Para aplicar basta criar um repositório público no github, codificar os teste e enviar o link para o email: dev@easygestor.com com o assunto **teste dev-web 2024**

Os testes estão dividos em três partes:
- Frontend
- Backend
- SQL

Cada uma das partes possui duas opções, você pode escolher uma das opções para codificar ou até mesmo escolher as duas, sinta-se desafiada(o)! Só serão consideradas as opções que estiverem funcionais de acordo com os requisitos.

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
No caso do SQL não precisa o passo a passo, pode ser em um arquivo *.sql* de fácil acesso ao conteúdo.

### Segue as opções de testes.


## Frontend
Utilize o Framework React.js para codificar pelo menos uma das opções abaixo.
- Documentação React.js https://react.dev/learn
### Opção 1: Formulário Cadasto de Cliente
**Objetivo**: Codificar um componente funcional React.js que renderize um formulário de cadastro de cliente com os campos: nome, cpf, email, telefone, sexo e nascimento. Utilize os hooks: **useState** para guardar os dados. Os dados devem ser exibidos em console.debug no formato do JSON abaixo
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
##### Requisitos
 - Todos os dados do formulário são obrigatórios
 - O formulário deve exibir em console.debug caso algum dado esteja faltando
 - O console.debug final deve ser exibido somente se todos os dados estiverem preenchidos

**Critérios que serão avaliados**: Codificação de um componente funcional básico e o fluxo de dados através do hook **useState**.

### Opção 2: React Pokedéx
**Objetivo**: Codificar um componente funcional simples que consuma a API Pokedex para buscar um Pokemon pelo nome e exibir quantas habilidades ele tem, no formato do JSON abaixo
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
##### Requisitos
 - O componente precisa renderizar um input e um botão
 - O componente não deve realizar a requisição caso o valor do input seja vazio
 - O componente precisa exibir o nome do Pokemón e a quantidade de habilidades em um texto centralizado, ex: Pokemón: snorlax - Habilidades: 2
 - O componente deve exibir as habilidades em uma lista HTML
 - O componente deve tratar os **HTTP STATUS CODE**: **200** se o pokemón foi localizado e **404** se o pokemón não for localido na pokedéx.

**Critérios que serão avaliados**: Consumo de api através de um componente funcional, compreendendo os status de retorno da API e a formatação e exibição dos dados em lista.

##### Dica:
API Pokedex: https://pokeapi.co/api/v2/pokemon/umbreon

```json
    {
        "abilities" : [
            // as habilidades estão nessa chave
        ]
    }
```

## Backend
Utilize a linguagem Python, ou o framework Django ou Django Rest Framework para codificar uma das opções abaixo.
- Documentação Django https://docs.djangoproject.com/en/5.0/intro/tutorial01/
- Documentação Django REST framework https://www.django-rest-framework.org/tutorial/quickstart/

### Opção 1: Script Python Busca CNPJ
**Objetivo**: Codifique um script python que realize a consulta do CNPJ de uma empresa na API do receitaws. O script deve receber como entrada um cnpj e exibir na tela os dados no formtado do JSON abaixo:
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
##### Requisitos
 - O Script deve receber uma string via input
 - O Script deve tratar o input antes de fazer a requisição
 - O Script deve validar o input e somente realzar a requisição se o input estiver no formtado de CNPJ válido
 - O Script deve utilizar a biblioteca Python requests para realizar a requisição
 - O Script deve validar o status code da requisição
 - O Script deve validar a resposta da requisição e indicar se o CNPJ foi localizado na API ou não.
 - O Script deve exibir os dados no formato JSON acima



**Critérios que serão avaliados**: Codificação básica de um script na linguagem Python, compreensão do fluxo de input e output de dados e tratamentos de requisições HTTP com a linguagem Python.

endpoint: https://receitaws.com.br/v1/cnpj/49310078000100
##### Dica:

```python
import re
# Define o padrão de regex para CNPJs. Este padrão aceita CNPJs com ou sem separadores (., /, -).
padrao_cnpj_regex = r'\d{2}\.?\d{3}\.?\d{3}/?\d{4}-?\d{2}'
# Exemplo de CNPJ para teste
cnpj_para_testar = "12.345.678/9012-34"
# Verifica se o CNPJ testado corresponde ao padrão definido
if re.match(padrao_cnpj_regex, cnpj_para_testar):
    print("O CNPJ é válido.")
else:
    print("O CNPJ é inválido.")
```

### Opção 2: CRUD de Empresas
**Objetivo**: Criar um CRUD de empresas com os campos: razao_social, atividade_principal, numero_endereco, cep, municipio e estado. Utilize a linguagem de programação Python ou o frameword web Django.

##### Requisitos Script Python
 - O Script deve ter a navegação fácil para guiar o usuário até a ação desejada
 - O Script deve ter uma interface fácil para a o input de dados
 - O Script deve fornecer os feedbacks para cada ação: criação, edição, pesquisa e remoção de empresa.

##### Requisitos Projeto Django
 - O projeto Django deve ter a navegação fácil para guiar o usuário até a ação desejada
 - O projeto Django deve ter uma interface fácil para a o input de dados
 - O projeto Django deve fornecer os feedbacks para cada ação: criação, edição, pesquisa e remoção de empresa.

**Critérios gerais que serão avaliados**: Compreender o panorama geral do CRUD de dados em tabelas de banco de dados.

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
