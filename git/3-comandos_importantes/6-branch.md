# Branches no Git

No Git, uma branch (ramificação) é uma referência que aponta para uma sequência de commits. Ela permite criar uma linha independente de desenvolvimento dentro de um projeto, sem interferir diretamente em outras branches.

As branches são utilizadas para desenvolver novas funcionalidades, corrigir bugs, testar ideias e realizar melhorias de forma isolada, mantendo a organização do projeto.

Essa organização permite que diferentes funcionalidades sejam desenvolvidas separadamente antes de serem integradas à branch principal, geralmente chamada `main`.

## Prática

Imagine que você encontrou um repositório público no GitHub que não administra e deseja contribuir com ele.

Você fez um `git clone` do projeto para sua máquina e pretende realizar algumas atualizações, corrigir problemas ou acrescentar novas funcionalidades.

Nesse cenário, o ideal é trabalhar em uma branch própria, mantendo suas alterações separadas da branch principal (main).

> **Importante**: Clonar um repositório público não significa que você tem permissão para enviar alterações diretamente para ele. Caso não tenha permissão de escrita, será necessário criar um `fork` do projeto e enviar suas alterações por meio de um `Pull Request`.

## Passo a passo na prática

Vou considerar que você já fez o git clone e abriu o projeto no VS Code.

Como você já pode ter realizado algumas alterações, primeiro precisamos verificar o estado atual do repositório antes de criar uma nova branch.

### Passo 1 — Verificar a branch atual

Abra o terminal do VS Code e execute:

```bash
git branch
```

Esse comando mostra as branches locais existentes.

Exemplo de resultado:

```bash
* main
```

O asterisco (*) indica a branch em que você está trabalhando atualmente.

Se aparecer main, significa que você está na branch principal local.

### Passo 2 — Criar sua branch

Se você estiver na main e tiver alterações ainda não commitadas, poderá criar uma nova branch diretamente:

```bash
git switch -c NOME_DA_BRANCH
```

Esse comando realiza duas operações:

- Cria uma branch chamada com o nome de sua escolha.
- Muda automaticamente para essa nova branch.

> **Observação: alterações que ainda não foram commitadas normalmente acompanham você durante a troca de branch, desde que não existam conflitos com o destino**.

Agora, confira as branches novamente:

```bash
git branch
```

Exemplo de resultado:

```bash
* NOME_DA_BRANCH
  main
```

*Pronto! Você está trabalhando em sua própria branch*.

### Passo 3 — Verificar suas alterações

Antes de preparar os arquivos para o commit, execute:

```bash
git status
```

Esse comando apresenta o estado atual do repositório, mostrando arquivos modificados, adicionados, removidos e aqueles que já estão preparados para o próximo commit.

É uma boa prática verificar essas informações antes de registrar suas alterações.

### Passo 4 — Adicionar os arquivos

Quando estiver tudo pronto, execute:

```bash
git add .
```

Esse comando adiciona as alterações dos arquivos ao Staging Area, também conhecida como área de preparação.

Essa área permite selecionar quais alterações farão parte do próximo commit.

### Passo 5 — Criar um commit

Agora, registre suas alterações:

```bash
git commit -m "feat: adiciona nova funcionalidade"
```

O commit funciona como um registro das alterações que você preparou no Staging Area.

O parâmetro -m permite adicionar uma mensagem para descrever o que foi realizado.


### Passo 6 — Enviar sua branch para o GitHub

Se você tiver permissão de escrita no repositório remoto, poderá enviar sua branch utilizando:

```bash
git push -u origin NOME_DA_BRANCH
```

Depois desse comando, sua branch estará disponível no GitHub.

> **Importante**: Se você clonou um repositório de outra pessoa e não tem permissão de escrita, o envio diretamente para o origin poderá ser recusado.

Nesse caso, o fluxo mais comum é utilizar um `Fork`.

E se eu não tiver permissão para enviar alterações ao repositório original?

Quando você não administra o repositório e não possui permissão de escrita, normalmente deverá seguir este fluxo:

- Acesse o repositório original no GitHub.
- Clique em Fork para criar uma cópia do projeto na sua própria conta.
- Configure seu repositório local para enviar alterações ao seu fork.
- Crie uma branch para desenvolver sua implementação.
- Faça os commits normalmente.
- Envie sua branch para o seu fork.
- Abra um Pull Request para propor a integração das suas alterações ao repositório original.

Dessa forma, o responsável pelo projeto poderá analisar suas alterações e decidir se deseja incorporá-las.

### E depois que o responsável aprovar o Pull Request?

Depois que seu Pull Request for aprovado e realizado o merge, suas alterações estarão integradas à branch de destino do repositório original, geralmente a main.

Quando for começar uma nova tarefa, o ideal é atualizar sua branch local para trabalhar com a versão mais recente do projeto.

### Dicas

Existe uma convenção de nomenclatura utilizada para organizar branches em projetos de desenvolvimento.

Ela ajuda a identificar rapidamente a finalidade de cada branch.

Alguns prefixos comuns são:

| Prefixo     | Finalidade                                  | Exemplo                      |
|-------------|---------------------------------------------|------------------------------|
| `feature/`  | Desenvolvimento de novas funcionalidades    | `feature/login`              |
| `bugfix/`   | Correção de bugs                            | `bugfix/correcao-login`       |
| `hotfix/`   | Correção urgente de problemas               | `hotfix/erro-producao`        |
| `docs/`     | Atualização da documentação                 | `docs/atualizar-readme`       |
| `refactor/` | Refatoração e organização do código         | `refactor/organizar-codigo`  |

> **Importante**: Esses prefixos são convenções adotadas por equipes e projetos. O Git não exige que você utilize esses nomes. Você pode escolher a nomenclatura que fizer mais sentido para a organização do seu projeto.