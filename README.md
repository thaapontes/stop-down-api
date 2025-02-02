# Stop Down API

Repositório para o desenvolvimento da API do sistema de gerenciamento para escola de aviação. Projeto proposto pela disciplina PCS3216 - Laboratório de Engenharia de Software da Escola Politécnica da USP

# Setup

## Flask + PostgreSQL

Criar uma pasta chamada `stop-down`, caso ela ainda não exista, e entrar nela utilizando o comando `cd stop-down`, rodar `git clone https://github.com/matthews34/stop-down-api.git`, renomear a pasta `stop-down-api` para `api`, entrar nela e seguir os passos a seguir para fazer o setup do ambiente virtual e do PostgreSQL (requer *python 3.6* e *PostgreSQL 11* instalados).

### Venv

Para fazer o setup do virtualenv, instalar o módulo com `pip install virtualenv`, então criar um ambiente virtual com um dos comandos abaixo (usar o segundo caso o primeiro não funcione):

```{bash}
virtualenv venv
python -m venv venv
```

por fim, é necessário entrar no ambiente criado e instalar as dependências:

```{bash}
source venv/bin/activate (linux)
venv\Scripts\activate (windows)
pip install -r requirements.txt
```

**NOTAS** 

- Para sair do ambiente virtual, bastar rodar o comando `deactivate`.

- Quando for rodar a **API** é importante observar se está dentro do ambiente virtual ou não (se tem um venv entre parenteses)

### PostgreSQL

- Criar um usuário e um banco de dados ambos chamados *stopdown*

- Modificar a senha do usuário *stopdown* para *semtempoirmao*

**NOTA** Os passos acima são necessários para que as credenciais utilizadas para a conexão da API com o banco de dados funcionem

### Rodando a API

- Para rodar a API, basta entrar no ambiente virtual e executar o comando `python manage.py run`. Assim, a API estará rodando em seu localhost, na porta 5000 (localhost:5000)

### Observações

- Pode ser necessário atualizar as dependências da **API** (rodando `pip install -r requirements.txt`) caso novos módulos sejam adicionados ao projeto
