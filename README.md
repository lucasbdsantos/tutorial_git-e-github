# Guia Prático de Git e GitHub

Este repositório foi criado exclusivamente para o aprendizado e a centralização de conhecimentos práticos e teóricos sobre Git e GitHub. Ele reúne conceitos fundamentais, comandos essenciais, guias passo a passo, boas práticas e ferramentas úteis para quem deseja dominar o controle de versão de código.  

## Estrutura do Repositório
```text
├── git/
│   ├── 1-configurando_git/     # Configuração inicial do usuário e segurança (SSH)
│   ├── 2-git_na_pratica/        # Criação, ciclo de vida e envio de repositórios locais
│   └── 3-comandos_importantes/  # Manipulação, histórico e gerenciamento avançado de arquivos
├── github/
│   ├── 1-criando_repositorio/   # Passos para criar repositórios remotos na plataforma web
│   ├── 2-clonado_repositorio/   # Procedimento para baixar projetos existentes para a máquina
│   ├── 3-repositorio_para_maquina/ # Instruções para sincronizar atualizações remotas na máquina
│   └── 4-funcoes_do_github/     # Ferramentas sociais, colaborativas e de acompanhamento
└── README.md
```

## Principais Conceitos Ensinados
- **Identidade e Rastreabilidade**: A necessidade intrínseca do Git de identificar o autor (nome e e-mail) de cada modificação para exibição correta no histórico.  
- **Autenticação via Assinatura Digital (SSH)**: O uso de um par de chaves criptográficas (pública e privada) usando o algoritmo moderno Ed25519 para realizar comunicações seguras e sem senhas com o servidor do GitHub.  
- **Área de Preparação (Staging Area)**: Um ambiente intermediário (funciona como um "carrinho antes do caixa") onde as alterações modificadas são temporariamente guardadas antes de serem salvas definitivamente.  
- **Ponto de Restauração (Commit)**: Gravação definitiva de alterações na linha do tempo do projeto, contendo uma mensagem descritiva.  
- **Ignorar Arquivos (.gitignore)**: Utilização de regras padronizadas e caracteres curinga (como o asterisco *) para evitar que arquivos confidenciais ou desnecessários sejam rastreados.  
- **Conexão Remota e Sincronização**: Vinculação de uma ramificação local do computador a uma ramificação hospedada em nuvem para empurrar (push) ou puxar (pull) alterações.  
- **Fluxo de Trabalho Colaborativo**: O ecossistema composto por clonar projetos existentes, fazer um Fork (cópia independente para o seu perfil) e submeter propostas de melhorias em projetos alheios via Pull Request.  