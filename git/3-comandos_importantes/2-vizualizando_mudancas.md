# Visualizando as Mudanças nos Arquivos

Depois de fazer alterações nos arquivos do seu projeto, é muito comum querer conferir exatamente o que foi modificado (o que foi adicionado, alterado ou deletado) antes de salvar essas alterações. É para isso que serve o comando `git diff`.

Por padrão, o `git diff` compara a versão do arquivo que já foi salva no seu último **commit** (o estado seguro do seu projeto) contra a versão do arquivo que você **modificou atualmente** no seu computador.


## Como visualizar as mudanças

Para ver todas as alterações feitas no seu projeto desde o último commit, digite o seguinte comando no seu terminal:

```bash
# Mostra as diferenças textuais entre os arquivos modificados e o último commit
git diff
```

Se você quiser verificar as mudanças de apenas um arquivo específico, basta passar o nome dele logo após o comando:
```bash
# Mostra as diferenças de um único arquivo
git diff nome-do-arquivo.txt
```

## Como ler o resultado do Git Diff?
Quando você executa o comando git diff, o terminal exibe o código com algumas marcações de cores e símbolos. Aprender a ler essa tela é muito simples:

- **Linhas em vermelho (precedidas por um sinal de menos -)**: Representam o código ou texto que foi removido ou alterado.

- **Linhas em verde (precedidas por um sinal de mais +)**: Representam o código ou texto que foi adicionado de novo no lugar.

## Outras formas úteis do comando
À medida que você avança no uso do Git, dois cenários muito comuns vão acontecer. Veja como o git diff te ajuda neles:

### 1. Comparar arquivos que já estão na Área de Preparação (Staging Area)

Se você já usou o comando git add em um arquivo, o comando git diff comum não vai mostrar nada. Para ver as alterações dos arquivos que já estão prontos para o commit, use:
```bash
# Compara os arquivos preparados (após o git add) com o último commit
git diff --staged
```

### 2. Comparar apenas os nomes dos arquivos alterados

Se você modificou muitos arquivos e o texto completo da tela ficar muito confuso, você pode pedir para o Git listar apenas os nomes dos arquivos que sofreram alterações:
```bash
# Lista apenas o nome dos arquivos modificados e o resumo das linhas alteradas
git diff --stat
```