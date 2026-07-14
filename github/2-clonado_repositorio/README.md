# Clonando um repositório

Muitas vezes, em vez de começar um projeto do zero no seu computador, você precisará baixar um projeto que já existe no GitHub. Esse processo de "baixar" uma cópia exata de um repositório remoto para a sua máquina é chamado de **Clonar**.


## Passo a Passo para Clonar um Repositório

### Passo 1: Copiar o endereço do repositório
No GitHub, acesse a página do projeto que você deseja baixar:
1. Clique no botão verde escrito **"Code"** (Código).
2. Escolha uma das opções e copie o endereço fornecido:
   * **HTTPS:** É o método mais comum e simples para iniciantes (ex: `https://github.com/usuario/nome-do-projeto.git`).
   * **SSH:** Usado quando você já tem chaves de segurança configuradas no seu computador.

### Passo 2: Preparar a pasta no seu computador
1. Abra o gerenciador de arquivos do seu computador e navegue até o local onde deseja guardar o projeto (por exemplo, dentro de uma pasta chamada `Projetos` ou `Documentos`).
2. Clique com o **botão direito do mouse** em um espaço vazio dessa pasta e selecione **"Git Bash Here"**.

### Passo 3: Executar o comando de clonagem
No terminal que se abriu, digite o seguinte comando, substituindo pelo endereço que você copiou no Passo 1:

```bash
# Cria uma pasta local com todos os arquivos e histórico do projeto do GitHub
git clone URL_DO_REPOSITORIO
``` 

## O que acontece depois que eu clono?

Ao pressionar Enter, o Git vai se conectar ao GitHub, baixar todos os arquivos, pastas e todo o histórico de commits do projeto.

Uma nova pasta com o nome do repositório será criada no seu computador.

**Observação**: Antes de começar a rodar outros comandos Git (como git status ou git add) após a clonagem, você precisa entrar na pasta do projeto que foi criada!

Para fazer isso pelo terminal, digite o comando cd (que significa change directory ou mudar de diretório) seguido do nome da pasta:

```bash
cd NOME-DA-PASTA-DO-PROJETO
```