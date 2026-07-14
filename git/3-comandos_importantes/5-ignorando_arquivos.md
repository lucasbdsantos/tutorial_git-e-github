# Ignorando Arquivos

Nem todos os arquivos do seu computador devem ser enviados para o GitHub. Arquivos de senhas, pastas de dependências (como a `node_modules`), arquivos gerados pelo sistema operacional (como `.DS_Store` ou `Thumbs.db`) ou relatórios temporários devem ficar apenas na sua máquina. 

Para dizer ao Git o que ele deve ignorar de forma automática, nós usamos um arquivo especial chamado `.gitignore`.


### Passo 1: Criando o arquivo .gitignore

Para começar, você deve criar esse arquivo na pasta raiz do seu projeto. Abra o terminal e digite o comando abaixo:

```bash
# Cria um arquivo invisível chamado .gitignore
touch .gitignore
```
Após rodar o comando, um arquivo chamado .gitignore (com um ponto no início do nome) será criado. Você pode abri-lo em qualquer editor de código (como o VS Code) ou até no Bloco de Notas para escrever as regras de ignorar.

### Passo 2: Escrevendo as regras de exclusão

Dentro do arquivo  `.gitignore `, você digita o nome dos arquivos ou os padrões que deseja que o Git ignore. Veja alguns exemplos práticos:

- Ignorar um arquivo específico: Escreva o nome exato dele.
```bash
senha.txt
index.html
teste.py
```

- Ignorar uma pasta inteira: Adicione uma barra / no final do nome da pasta.
```bash
minha-pasta-secreta/
```

- Ignorar por extensão (Uso de Astersco *): Se você quiser ignorar todos os arquivos de um formato específico (por exemplo, arquivos HTML), use o asterisco antes da extensão. O asterisco funciona como um caractere curinga que significa "qualquer nome".
```bash
*.html
```

**Observação**: Não precisa criar essas regras do zero! O próprio GitHub disponibiliza um repositório com modelos prontos de `.gitignore` para quase todas as linguagens de programação do mercado. Você pode consultar e copiar as regras diretamente aqui:

- [Modelos oficiais de .gitignore do GitHub](https://github.com/github/gitignore?tab=readme-ov-file)

</br>

## O que fazer se o Git continuar rastreando o arquivo?

Um erro muito comum acontece quando você cria um arquivo, salva ele no Git (faz um commit) e só depois disso decide colocá-lo no .gitignore.

O Git não vai ignorar esse arquivo automaticamente porque ele já começou a rastreá-lo antes da regra existir. O .gitignore só funciona de forma nativa para arquivos que nunca foram adicionados ao Git.

Para corrigir isso e fazer o Git passar a ignorar o arquivo de verdade, você precisa tirá-lo da memória do Git (sem apagá-lo do seu computador) usando o comando abaixo:
```bash
# Remove o arquivo do histórico de monitoramento do Git, deixando o arquivo salvo no seu computador
git rm --cached nome-do-arquivo.html
```
Depois de rodar esse comando, faça um novo commit. A partir daí, a regra do `.gitignore` começará a funcionar perfeitamente para ele!