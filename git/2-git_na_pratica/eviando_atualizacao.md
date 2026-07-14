# Enviando Atualizações para o GitHub (O Fluxo Diário)

Depois de fazer a primeira conexão entre a sua máquina e o GitHub, o seu trabalho do dia a dia seguirá um ciclo muito simples e repetitivo. Toda vez que você terminar uma tarefa, corrigir um bug ou implementar uma nova função, você precisará "empurrar" essas novidades para a nuvem.

Este é o **fluxo diário oficial** de todo desenvolvedor:


## O Passo a Passo das Atualizações

Sempre que terminar uma alteração no seu código, abra o terminal na pasta do projeto e execute a sequência abaixo:

```bash
# 1. Verifique quais arquivos foram alterados e o estado do repositório
git status

# 2. Prepare todos os arquivos modificados para o salvamento
git add .

# 3. Grave as alterações localmente com uma mensagem clara sobre o que foi feito
git commit -m "Descreva a atualização realizada"

# 4. Envie as novidades da sua máquina para o repositório no GitHub
git push origin main
```

Mas se você quer entender melhor o que cada comando faz e a sua importância, vá para o seguinte arquivo do repositório: [Criando um repositório](../../git/2-git_na_pratica/criacao_repositorio.md).