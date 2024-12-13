# Git pull 


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

# Git fetch


> O comando git fetch é usado no Git para atualizar o repositório local com as alterações mais recentes do  > repositório remoto, sem mesclar automaticamente essas alterações no seu branch atual. É uma operação "segura" porque não modifica diretamente os arquivos no seu diretório de trabalho ou interfere com o histórico local.

**Exemplo Prático:**

O que acontece quando você usa git fetch?

1. O Git conecta-se ao repositório remoto configurado.

2. Recupera as referências e os objetos do repositório remoto (como commits, branches) que ainda não estão disponíveis localmente.

3. Atualiza os branches remotos (por exemplo, origin/main) para refletir o estado mais recente no remoto.

## Diferença entre git fetch e git pull

## git fetch: 

Atualiza apenas as informações sobre o estado do repositório remoto, sem alterar o branch local ou os arquivos de trabalho.

## git pull: 

Faz um git fetch seguido de um git merge no branch atual, ou seja, tenta integrar automaticamente as mudanças do remoto ao seu branch local.

## Quando usar git fetch?

Para verificar atualizações no repositório remoto sem impactar o que você está trabalhando localmente.

Antes de decidir mesclar (merge) ou rebasear seu branch com o remoto, para analisar o que mudou.

Para verificar se há novos branches ou tags no remoto.

## Exemplo

```sh
git fetch origin
```
Aqui, o Git irá buscar as alterações do repositório remoto chamado origin. Após isso, você pode verificar os novos commits ou branches usando:

```sh
git log origin/main
```
Depois de inspecionar as mudanças, você pode decidir o que fazer: mesclar as alterações, criar um rebase, ou simplesmente deixar como está.