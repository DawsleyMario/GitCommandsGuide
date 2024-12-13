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
