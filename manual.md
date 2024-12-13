# Git Command Gides

1. Git Init (Inicializando um repositório)
O comando git init é usado para criar um novo repositório Git em um diretório existente. Ele transforma uma pasta comum em um repositório Git, permitindo que você comece a rastrear mudanças nos arquivos dentro desse diretório.

Como funciona:
Ele cria uma subpasta oculta chamada .git, onde o Git armazenará todo o histórico do repositório, configurações e metadados necessários.
Após executar git init, você pode adicionar arquivos ao controle de versão com git add e salvar as alterações com git commit.
Quando usar:
Ao iniciar um projeto do zero.
Quando deseja versionar arquivos que já estão em uma pasta local no seu computador.
Exemplo prático:
bash
Copiar código
mkdir meu_projeto
cd meu_projeto
git init
Resultado: Agora, o diretório meu_projeto é um repositório Git vazio pronto para rastrear arquivos.

2. Git Clone (Clonando um repositório)
O comando git clone é usado para copiar um repositório Git existente (local ou remoto) para o seu computador. Ele cria uma cópia completa do repositório, incluindo todo o histórico de commits e arquivos.

Como funciona:
Você fornece a URL do repositório remoto (como no GitHub ou GitLab) ou o caminho de um repositório local.
O Git cria uma nova pasta no seu sistema, baixa todos os arquivos e configurações do repositório original e configura a conexão com o remoto, permitindo sincronizações futuras.
Quando usar:
Quando precisa trabalhar em um projeto já existente hospedado em um servidor remoto ou compartilhado por outro desenvolvedor.
Para obter o código-fonte de um repositório público ou privado.
Exemplo prático:
bash
Copiar código
git clone https://github.com/usuario/projeto.git
Resultado: Uma cópia do repositório projeto será criada no seu computador, em uma pasta chamada projeto.

Resumo das diferenças:
Comando	Finalidade	Contexto de uso
git init	Inicializa um novo repositório Git	Projetos iniciados do zero
git clone	Copia um repositório existente	Projetos já existentes hospedados remotamente
Com esses dois comandos, você pode tanto iniciar um projeto novo quanto participar de projetos já existentes, estabelecendo o controle de versão com o Git.