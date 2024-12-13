# Git Command Gides

## _Introdução ao Git e ao GitHub_

## O que é o Git?

O Git é um sistema de controle de versão distribuído amplamente utilizado por desenvolvedores para gerenciar projetos de software. Ele permite rastrear mudanças no código-fonte, colaborar com outras pessoas e reverter para versões anteriores quando necessário.

### Principais características do Git

- **Distribuído:** Cada usuário possui uma cópia completa do repositório.
- **Desempenho rápido:** Operações locais são extremamente rápidas.
- **Integridade dos dados:** Todas as mudanças são registradas de forma segura.
- **Branching poderoso:** Permite criar e mesclar branches facilmente.

## O que é o GitHub?

O GitHub é uma plataforma baseada na nuvem para hospedagem de repositórios Git. Ele facilita a colaboração entre desenvolvedores, permitindo compartilhamento de código, revisão de pull requests e gerência de projetos. Além disso, o GitHub oferece diversas funcionalidades como integração com CI/CD, Wikis e Issues para rastreamento de tarefas.

### Diferença entre Git e GitHub

- **Git:** É uma ferramenta de controle de versão que funciona localmente.
- **GitHub:** É uma plataforma online que utiliza Git para hospedar repositórios.

## Instalação do Git

### Windows

1. Acesse o site oficial do Git: https://git-scm.com/.
2. Baixe o instalador para Windows.
3. Execute o instalador e siga as instruções, configurando opções como editor padrão e comportamento do terminal.

### MacOS

1. Instale o Git via [Homebrew](https://brew.sh/):

   ```
   brew install git
   ```

2. Verifique a instalação:

   ```
   git --version
   ```

### Linux

1. Use o gerenciador de pacotes da sua distribuição:

   - **Ubuntu/Debian:**

     ```
     sudo apt update
     sudo apt install git
     ```

   - **Fedora:**

     ```
     sudo dnf install git
     ```

2. Confirme a instalação:

   ```
   git --version
   ```

## Configuração inicial do Git

Após instalar o Git, configure seu nome de usuário e e-mail para que suas contribuições sejam corretamente atribuídas:

```
git config --global user.name "Seu Nome"
git config --global user.email "seu.email@exemplo.com"
```

Verifique as configurações:

```
git config --list
```

## Criando uma conta no GitHub

1. Acesse https://github.com/.
2. Clique em **Sign up**.
3. Preencha os dados solicitados, como e-mail, nome de usuário e senha.
4. Complete o cadastro e confirme o e-mail.

Agora você está pronto para explorar o Git e o GitHub!

## Git pull 


> Descrição: O comando git pull é usado para atualizar o repositório local
> com as alterações do repositório remoto. A tradução básica para o conceito 
> seria algo como "puxar as alterações". 

**Exemplo Prático:** 

Como funciona o git pull?
1. O git pull combina dois comandos: git fetch (que busca as atualizações do repositório remoto) e git merge (que integra essas atualizações ao ramo local).


2. Sintaxe:
```sh
git pull [repositório] [branch]
```
repositório: O nome do repositório remoto (geralmente origin).
branch: O branch que você deseja atualizar (se não especificado, será o branch atual).


3. Exemplo de uso:
```sh
git pull origin main
```

## Git fetch


> O comando git fetch é usado no Git para atualizar o repositório local com as alterações mais recentes do  > repositório remoto, sem mesclar automaticamente essas alterações no seu branch atual. É uma operação "segura" porque não modifica diretamente os arquivos no seu diretório de trabalho ou interfere com o histórico local.

**Exemplo Prático:**

O que acontece quando você usa git fetch?

1. O Git conecta-se ao repositório remoto configurado.

2. Recupera as referências e os objetos do repositório remoto (como commits, branches) que ainda não estão disponíveis localmente.

3. Atualiza os branches remotos (por exemplo, origin/main) para refletir o estado mais recente no remoto.

# Diferença entre git fetch e git pull

# git fetch: 

Atualiza apenas as informações sobre o estado do repositório remoto, sem alterar o branch local ou os arquivos de trabalho.

# git pull: 

Faz um git fetch seguido de um git merge no branch atual, ou seja, tenta integrar automaticamente as mudanças do remoto ao seu branch local.

# Quando usar git fetch?

Para verificar atualizações no repositório remoto sem impactar o que você está trabalhando localmente.

Antes de decidir mesclar (merge) ou rebasear seu branch com o remoto, para analisar o que mudou.

Para verificar se há novos branches ou tags no remoto.

# Exemplo

```sh
git fetch origin
```
Aqui, o Git irá buscar as alterações do repositório remoto chamado origin. Após isso, você pode verificar os novos commits ou branches usando:

```sh
git log origin/main
```
Depois de inspecionar as mudanças, você pode decidir o que fazer: mesclar as alterações, criar um rebase, ou simplesmente deixar como está.


