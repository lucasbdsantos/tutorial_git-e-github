# Configurando a Autenticação via Chave SSH no GitHub

A autenticação via **SSH** (*Secure Shell*) é um método de comunicação muito mais seguro e prático do que o tradicional HTTPS. 

Em vez de digitar seu usuário e senha (ou token de acesso) toda vez que fizer um envio para o GitHub, o seu computador se valida usando uma "assinatura digital" gerada por um par de chaves de segurança: uma **Chave Privada** (que fica protegida na sua máquina) e uma **Chave Pública** (que você cadastra no site do GitHub).


**Observação: todos os comandos a seguir, são para criar uma chave SSH no Windows. Se quiser criar uma chave em outra máquina, vá para o último tópico do arquivo, *Dica***

## Passo 1: Gerando uma nova Chave SSH

Para criar a sua assinatura digital segura, você precisa gerar esse par de chaves. O algoritmo mais moderno, leve e seguro recomendado pelo próprio GitHub é o **Ed25519**.

1. Abra o seu **Git Bash**.
2. Cole o comando abaixo, substituindo pelo endereço de e-mail que você usa na sua conta do GitHub:

```bash
ssh-keygen -t ed25519 -C "seu_email@exemplo.com"
```

## Passo 2: Salvando a Chave e criando uma Frase Secreta
Durante a criação da chave no terminal, o Git fará algumas perguntas na tela. Veja como responder:

1. Local de salvamento: O terminal mostrará uma mensagem perguntando onde salvar a chave:

```bash
Enter a file in which to save the key (/c/Users/seu-usuario/.ssh/id_ed25519):
```
Apenas aperte ENTER para aceitar o local padrão recomendado.

2. Criando uma Frase Secreta (Passphrase): Em seguida, o terminal pedirá uma senha de segurança para proteger a sua chave no computador:

```bash
Enter passphrase (empty for no passphrase): [Digite uma senha segura]

Enter same passphrase again: [Digite a mesma senha novamente]
```

**Nota Visual**: Ao digitar a senha no terminal, nenhum caractere ou asterisco vai aparecer na tela. Isso é uma medida padrão de segurança do Git/Linux. Digite normalmente e aperte ENTER. Se preferir não usar senha, apenas aperte ENTER duas vezes para deixar em branco.

## Passo 3: Copiando a sua Chave Pública
Agora que as chaves foram criadas, você precisa copiar o conteúdo da sua Chave Pública (o arquivo com final .pub) para inseri-lo no site do GitHub.

Para mostrar o conteúdo da chave diretamente no terminal para você copiá-lo, digite:

```bash
# Exibe a sua chave pública na tela para que você possa selecioná-la e copiá-la
cat ~/.ssh/id_ed25519.pub
```
Selecione todo o texto gerado na tela (ele começará com algo parecido com ssh-ed25519 AAAA... e terminará com o seu e-mail) e copie-o.

## Passo 4: Adicionando a Chave no seu Perfil do GitHub
Agora você precisa dizer ao GitHub que esse computador está autorizado a mexer nos seus repositórios.

1. Acesse o site do GitHub e faça login na sua conta.
2. No canto superior direito, clique na sua foto de perfil e selecione Settings (Configurações). 
3. No menu lateral esquerdo, procure e clique na opção SSH and GPG keys. 
4. Clique no botão verde New SSH key (Nova chave SSH). 
5. Preencha os campos da seguinte forma:
   - Title (Título): Dê um nome que te ajude a lembrar de qual computador é essa chave (ex: Notebook Pessoal, Computador do Trabalho).
   -  Key type (Tipo de chave): Deixe selecionado como Authentication Key.
   - Key (Chave): Cole exatamente o texto que você copiou no Passo 3 dentro dessa caixa.
6. Clique no botão verde Add SSH key (Adicionar chave SSH).


## Passo 5: Testando a Conexão SSH com o GitHub
Para ter certeza absoluta de que o seu computador está conectado de forma segura com o seu GitHub, você pode realizar um teste rápido rodando o seguinte comando no seu Git Bash:

```bash
# Faz um teste de conexão criptografada direto com o servidor do GitHub
ssh -T git@github.com
```
O terminal exibirá uma mensagem de aviso de segurança perguntando se você confia na conexão:

```bash
Are you sure you want to continue connecting (yes/no/[fingerprint])?
```
Digite yes e aperte ENTER.

Se tudo estiver configurado corretamente, você receberá uma mensagem de boas-vindas parecida com esta:

*Hi NOME-DO-USUÁRIO! You've successfully authenticated, but GitHub does not provide shell access.*

Pronto! A conexão SSH está completa, segura e pronta para ser usada nos seus clones, pulls e pushes do dia a dia.

</br>

## Dica 

Se você quiser entender melhor o processo de criação de uma chave SSh e saber criar uma chave SSh em outra máquina, consulte o seguinte documento disponibilizado pelo github: [Gerando uma chave SSH](https://docs.github.com/pt/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)