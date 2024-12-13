# Git Command Gides

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

