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

## Git merge

**Descrição:**  
No Git, o comando `git merge` é utilizado para combinar as alterações de um ramo (branch) em outro. Esse comando integra o histórico de ambos os ramos e tenta unir seus conteúdos. O Git tenta mesclar as alterações automaticamente, mas, se houver conflitos, você precisará resolvê-los manualmente.

### Exemplo Prático:

#### 1. **Mesclar um ramo de funcionalidade na branch principal:**

Suponha que você esteja trabalhando em um ramo de funcionalidade chamado `feature-branch` e deseja mesclá-lo na sua branch principal `main`. O procedimento seria:

1. **Primeiro**, verifique se você está na branch `main`(ou na branch que deseja mesclar):

    ```bash
    git checkout main
    ```

2. **Em seguida**, mescle o ramo `feature-branch` na `main`:

    ```bash
    git merge feature-branch
    ```

3. O Git tentará mesclar as alterações automaticamente. Se não houver conflitos, a mesclagem será concluída com sucesso e o Git criará um novo commit, combinando as alterações dos dois ramos.

#### 2. **Lidando com Conflitos:**
Se houver alterações conflitantes entre os dois ramos, o Git não conseguirá mesclar automaticamente e marcará o arquivo como conflituoso. Você verá as marcações de conflito no arquivo, como:

    
    <<<<<<< HEAD
    # Suas alterações no ramo atual
    =======
    # Alterações do ramo que está sendo mesclado
    >>>>>>> feature-branch
    

Você precisará editar manualmente o arquivo para resolver o conflito. Após resolver os conflitos:

1. **Marque o arquivo como resolvido:**

    ```bash
    git add <arquivo-conflitante>
    ```

2. **Finalize a mesclagem:**

    ```bash
    git merge --continue
    ```

#### 3. **Mesclagens Fast-Forward:**
Se o ramo que está sendo mesclado não tiver alterações divergentes, o Git fará uma mesclagem "fast-forward", movendo o ponteiro da branch `main` diretamente para o topo da `feature-branch`. Nesse caso, o Git não cria um commit de mesclagem, pois não há necessidade.

#### 4. **Abortar a Mesclagem:**
Se você quiser cancelar a mesclagem (por exemplo, se estiver confuso ou se houver muitos conflitos difíceis de resolver), pode abortá-la com:

    ```bash
    git merge --abort
    ```

Esse comando reverterá o repositório ao estado anterior à tentativa de mesclagem.

### Resumo:

- **`git merge <branch>`**: Mescla o ramo especificado na branch atual.
- **`--no-ff`**: Cria um commit de merge mesmo que a mesclagem possa ser feita como fast-forward.
- **`--continue`**: Continua a mesclagem após resolver os conflitos.
- **`--abort`**: Aborta a mesclagem atual.

O comando `git merge` é essencial para integrar as alterações feitas em diferentes ramos, permitindo que diferentes desenvolvedores trabalhem de forma colaborativa sem sobrescrever o trabalho dos outros.

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
Depois de inspecionar as mudanças, você pode decidir o que fazer: mesclar as alterações, criar um rebase, ou simplesmente deixar como está
