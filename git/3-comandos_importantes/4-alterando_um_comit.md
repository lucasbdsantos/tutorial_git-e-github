# Alterando os comits

alterando um comit 
```bash
git log --amend -m "NOVO-COMIT"
```


```bash
git log --amend --no-edit
```

# Alterando o Último Commit (git commit --amend)

É muito comum fazermos um commit e, logo em seguida, perceber que esquecemos de adicionar um arquivo ou que digitamos a mensagem com algum erro de português. Para corrigir o **último commit feito**, o Git nos oferece a opção `--amend` (que significa "emendar").

---

## Cenário 1: Alterando apenas a mensagem do último commit

Se você salvou o commit, mas percebeu que escreveu a mensagem errada e quer apenas mudar o texto, utilize o comando abaixo:

```bash
# Altera a mensagem do último commit realizado para uma nova mensagem
git commit --amend -m "Sua nova mensagem corrigida aqui"