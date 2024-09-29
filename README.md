# MUD-BEN10

<div align="center">
    <img src="assets\ben-10.jpg" style="width:35vw"/>
    <p> Figura 1: Logo do Ben 10</p> 
</div>

##  Sobre o Projeto 

Projeto criado para a disciplina de Sistemas de Banco de Dados 1 do curso de Engenharia de Software da Universidade de Brasília (UnB). Neste projeto, foi desenvolvido um MUD (Multi-User Dungeon), no qual foram aplicados diversos conceitos de bancos de dados, resultando na entrega de um jogo funcional inspirado no famoso desenho Ben 10, criado pelo grupo [Man of Action](https://manofaction.tv/).

##  Como jogar 

###  Ferramentas Necessárias 

Antes de começar, você precisará das seguintes ferramentas instaladas no seu sistema:

- **Git**: Para clonar o repositório.
- **Docker**: Para criar e executar contêineres.
- **Docker Compose**: Para orquestrar múltiplos contêineres e simplificar a execução do projeto.

###  Configuração e Execução 

Siga os passos abaixo para configurar e executar o projeto:

####  1. Clone o Repositório 

Clone o repositório usando o comando abaixo:

```bash
git clone https://github.com/joao-artl/MUD-BEN10.git
```

####  2. Navegue para o Diretório Docker 

Entre no diretório onde o Docker Compose está configurado:

```bash
cd ./MUD-BEN10/docker
```

####  3. Derrube Contêineres Existentes 

Se você já tem contêineres rodando de uma sessão anterior, derrube-os e remova seus volumes com o comando:

```bash
docker compose down -v
```

####  4. Construa e Inicie os Contêineres 

Construa as imagens Docker e inicie os contêineres em segundo plano com:

```bash
docker compose up --build -d
```

####  5. Acesse o Contêiner e Execute o Jogo 

Depois que os contêineres estiverem em execução, você pode acessar o contêiner principal e iniciar o jogo com o seguinte comando:

```bash
clear
docker exec -it game /bin/bash -c "python3 -u app.py"
```