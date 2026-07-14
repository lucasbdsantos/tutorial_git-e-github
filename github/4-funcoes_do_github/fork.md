# Fazendo um Fork no GitHub

No GitHub, a palavra **Fork** representa o ato de tirar uma "cópia" de um repositório que pertence a outra pessoa e salvá-la diretamente dentro do seu próprio perfil. 

Pense nisso como tirar a fotocópia de um livro de receitas de um amigo: o livro original continua intacto com ele, mas agora você tem a sua própria cópia idêntica para rabiscar, testar novos ingredientes e fazer o que quiser, sem alterar o trabalho dele.


## Como fazer um Fork?

O processo de fazer um fork é feito de forma visual diretamente pelo site do GitHub:

1. Acesse o repositório da pessoa ou organização que você deseja copiar.
2. No canto superior direito da página, procure pelo botão escrito **"Fork"** (ele geralmente tem o ícone de um caminho se dividindo).
3. Clique nele, escolha o seu perfil como destino e confirme em **"Create fork"**.

Pronto! Em poucos segundos, uma cópia exata do projeto aparecerá sob o seu nome de usuário (ex: `seu-usuario/nome-do-projeto`).


## Como funciona a sincronização entre os projetos?

Uma dúvida muito comum de quem está começando é: *"Se o dono do projeto original fizer alterações, o meu projeto copiado muda sozinho?"*

A resposta é **não**. O seu repositório "forkado" é totalmente independente. Porém, o GitHub é inteligente e avisa você quando isso acontece:

* **Independência:** Tudo o que o criador original mudar lá, não afetará o seu código de forma automática.
* **Aviso de atualizações:** O GitHub exibirá uma mensagem na página do seu repositório dizendo se o seu projeto está atualizado ou "atrás" (*behind*) em relação ao original.
* **Como atualizar (Sincronizar):** Se você quiser trazer as novidades do criador original para a sua cópia, basta clicar no botão **"Sync fork"** (Sincronizar fork) que o GitHub mostra logo abaixo do nome do repositório.


## Para que serve o Fork no dia a dia?

Existem dois motivos principais para você fazer um fork de um projeto:

1. **Usar como ponto de partida:** Você gostou muito de um modelo de portfólio ou projeto de outra pessoa e quer usá-lo como base para criar o seu próprio.
2. **Contribuir com projetos de código aberto (Open Source):** Se você encontrar um erro no projeto de alguém e souber como consertar, você faz um *fork*, corrige o erro na sua cópia e depois envia uma proposta de melhoria para o criador original através de um **Pull Request**.