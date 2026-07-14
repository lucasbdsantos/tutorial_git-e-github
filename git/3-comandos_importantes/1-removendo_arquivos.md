# Removendo Arquivos da Área de Preparação

Às vezes, nós adicionamos arquivos para serem salvos pelo Git usando o comando `git add`, mas mudamos de ideia ou percebemos que incluímos um arquivo por engano. 

Quando isso acontece, precisamos remover esses arquivos da **área de preparação** (também conhecida como *Staging Area* ou arquivos preparados) antes de fazer o salvamento definitivo (*commit*).


## Como remover um arquivo específico

Se você quer tirar apenas **um arquivo** específico da área de preparação, utilize o seguinte comando substituindo pelo nome correto do seu arquivo:

```bash
# Remove um arquivo específico da área de preparação, mantendo o arquivo intacto no seu computador
git rm --cached nome-do-arquivo.txt
```

## Como remover todos os arquivos de uma vez

Se você adicionou muitos arquivos por engano e quer limpar toda a área de preparação de uma só vez, utilize o comando abaixo:

```bash
# Remove todos os arquivos e pastas da área de preparação de forma recursiva
git rm --cached -r .
```

## Uma alternativa mais moderna (Opcional)

Nas versões mais recentes do Git, existe um comando mais intuitivo criado especificamente para essa tarefa de "desfazer o git add":

```bash
# Desfaz o 'git add' de um arquivo específico
git restore --staged nome-do-arquivo.txt

# Desfaz o 'git add' de todos os arquivos da pasta atual
git restore --staged .
```