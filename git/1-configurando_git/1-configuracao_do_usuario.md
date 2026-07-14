# Configuração do usúario

Antes de começar a criar seus projetos e salvar suas alterações, você precisa dizer ao Git quem é você. Isso é fundamental porque todo projeto no Git registra quem fez cada modificação. 

Esses dados vão aparecer no histórico do seu repositório, permitindo que outras pessoas saibam quem escreveu aquela linha de código.

## Comandos de Configuração

Abra o seu terminal (ou Git Bash) e digite os comandos abaixo, substituindo os textos entre aspas pelas suas informações:

```bash
# Define o nome que aparecerá no seu histórico de alterações
git config --global user.name "Seu Nome Completo"

# Define o e-mail associado à sua conta do GitHub
git config --global user.email "seu.email@exemplo.com"
```