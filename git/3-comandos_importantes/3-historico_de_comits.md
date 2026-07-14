# Visualizando o Histórico de Commits

À medida que você avança no desenvolvimento do seu projeto, o Git vai guardando cada um dos seus salvamentos. Para consultar toda a linha do tempo do seu trabalho, ver quem fez as alterações e ler as mensagens dos commits antigos, nós utilizamos o comando `git log`.

### 1. O Histórico Completo

Para ver uma listagem detalhada de todos os commits realizados no seu projeto (do mais recente para o mais antigo), digite o seguinte comando:

```bash
# Mostra o histórico detalhado com ID do commit, autor, data e mensagem completa
git log
```

### 2. O Histórico Resumido (Visualização em uma linha)
Se o seu projeto já tiver muitos commits, o comando git log tradicional pode deixar a tela muito poluída. Para ver um resumo bem direto e limpo, utilize:
```bash
# Mostra cada commit resumido em apenas uma linha, ideal para visões gerais
git log --oneline
```
Esse comando exibe apenas os primeiros caracteres do ID do commit (a versão reduzida) e o título da mensagem que você escreveu.

### 3. Limitando a quantidade de Commits exibidos
Se você quiser dar apenas uma espiada rápida nas últimas modificações, sem precisar carregar todo o histórico do projeto, você pode dizer ao Git exatamente quantos commits deseja ver na tela.

Basta adicionar um sinal de menos - seguido do número desejado:
```bash
# Mostra apenas as últimas 3 alterações salvas no projeto
git log -3
```
Você pode substituir o número 3 por qualquer quantidade que preferir, como: *git log -5* ou *git log -10*.