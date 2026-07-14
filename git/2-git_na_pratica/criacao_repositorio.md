# Criando e Inicializando um Repositório Git

Para que o Git comece a acompanhar as alterações do seu projeto, você precisa transformar uma pasta comum do seu computador em um **Repositório Git**. Veja o passo a passo abaixo de como fazer isso.

## Passo 1: Abrindo o terminal na pasta do seu projeto

1. Navegue até a pasta onde estão os arquivos do seu projeto (ou crie uma pasta nova vazia).
2. Clique com o **botão direito do mouse** em qualquer espaço em branco dentro dessa pasta.
3. No menu que aparecer, selecione a opção **"Git Bash Here"**.

Isso abrirá a tela preta do terminal do Git já apontando exatamente para a pasta do seu projeto.

</br>

## Comandos úteis de consulta (Navegação)

Antes de transformar a pasta em um repositório, é bom conhecer dois comandos básicos do terminal para listar e conferir seus arquivos:

```bash
# Lista todos os arquivos e pastas visíveis dentro da pasta atual
ls

# Lista TODOS os arquivos e pastas, incluindo os arquivos ocultos/escondidos
ls -a
```

</br>

## Passo 2: Inicializando o Repositório Git
Agora que você está na pasta correta, digite o comando abaixo para ativar o Git nela:

```bash
# Inicializa um novo repositório Git na pasta atual
git init
```
Ao executar este comando, o Git criará de forma invisível uma pasta chamada .git. É ela quem vai guardar todo o histórico de alterações do seu projeto daqui para frente!

**Observação**: Para iniciar um repositório Git, não é necessário que a pasta já tenha arquivos. Você pode inicializar o Git em uma pasta completamente vazia e começar seu projeto do zero!


## Passo 3: Preparando os Arquivos para o Salvamento 

Depois de inicializar o repositório e criar ou modificar seus arquivos, você precisa dizer ao Git quais dessas alterações devem ser salvas. Esse processo envia os arquivos para a **Área de Preparação** (conhecida em inglês como *Staging Area*). 

Pense no `git add` como o ato de colocar os produtos dentro do carrinho antes de passar no caixa (que será o commit).

### 1. Como adicionar um arquivo específico

Se você modificou vários arquivos, mas quer preparar e salvar apenas **um** deles, digite o comando informando o nome exato do arquivo:

```bash
# Adiciona apenas o arquivo mencionado à Área de Preparação
git add nome-do-arquivo
```

### 2. Como adicionar todos os arquivos de uma vez
Se você criou ou modificou muitos arquivos e não quer digitar o nome de cada um deles, o Git oferece caminhos mais rápidos. Existem 3 comandos para adicionar tudo de uma vez só:

#### Opção 1: Mais comum
```bash
# Adiciona todos os arquivos novos, modificados e deletados da pasta atual para a área de preparação
git add .
```

#### Opção 2
```bash
# Adiciona absolutamente todas as mudanças do projeto inteiro
git add -A
```

#### Opção 3
```bash
git add --all
```

</br>

## Como verificar a situação do seu repositório? (git status)

Assim que você transforma sua pasta em um repositório Git, você ganha acesso a um dos comandos mais importantes e utilizados no dia a dia:

```bash
# Mostra o estado atual do seu repositório (arquivos modificados, novos ou prontos para salvar)
git status
```

</br>

## Passo 4: Gravando as Mudanças no Histórico 

Depois de preparar os seus arquivos usando o comando `git add`, chega o momento de salvá-los definitivamente na linha do tempo do seu projeto. No Git, esse processo de salvar um "ponto de restauração" é chamado de **Commit**.

Para gravar suas alterações, utilize o comando abaixo:

```bash
# Salva as alterações que estavam preparadas, associando uma mensagem descritiva
git commit -m "Adiciona a estrutura inicial do projeto"
```

### Boas Práticas

O texto que você coloca entre aspas ("") logo após a opção -m (que vem de message) é a mensagem do seu commit.

Escrever mensagens claras e com uma lógica profissional é fundamental. Quando você ou sua equipe precisarem consultar o histórico de mudanças no futuro usando o git log, cada alteração será identificada por esse texto.

**Exemplos do que fazer e do que evitar:**
- git commit -m "ajustes" (Muito vago, ninguém sabe o que mudou)
- git commit -m "codigo funcionando" (Não explica o que o código faz)
- git commit -m "aaaaaaaaa" (Prejudica a organização do projeto)

**Mensagens boas (Recomendado):**
- git commit -m "Cria a página de login" (Direto e explicativo)
- git commit -m "Corrige o bug no cálculo do carrinho" (Mostra exatamente o problema resolvido)
- git commit -m "Atualiza o texto do arquivo de configurações" (Claro e objetivo)


## Passo 5: Enviando seu Projeto para o GitHub (Conexão Remota)
Agora que você já salvou suas alterações localmente no seu computador, é hora de enviar esses commits para a nuvem (o GitHub).

Para fazer isso pela primeira vez, execute esta sequência de 3 comandos no seu terminal:

```bash
# 1. Cria ou renomeia a ramificação principal para "main" (padrão recomendado de mercado)
git branch -M main
``` 
```bash
# 2. Conecta o seu repositório local ao link do repositório remoto que você criou no GitHub
git remote add origin URL_DO_SEU_REPOSITORIO_AQUI
```
```bash
# 3. Envia (empurra) o seu código local para a ramificação "main" do GitHub
git push -u origin main
```