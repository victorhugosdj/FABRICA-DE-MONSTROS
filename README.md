Criar uma branch (ramo) é como criar uma linha do tempo alternativa para o seu projeto: você pode testar coisas novas sem estragar o que já está funcionando na linha principal.

Aqui estão os comandos principais:

### 1. Criar e já entrar na branch (O mais usado)

Este comando cria a branch e já muda o seu terminal para dentro dela.

```bash
git checkout -b nome-da-sua-branch

```

*Dica: Em versões mais recentes do Git, você também pode usar `git switch -c nome-da-branch`.*

---

### 2. O modo "passo a passo"

Se preferir fazer uma coisa de cada vez:

1. **Cria a branch:**
```bash
git branch nome-da-sua-branch

```


2. **Entra nela:**
```bash
git checkout nome-da-sua-branch

```



---

### 3. Enviando a nova branch para o GitHub

Depois de criar a branch e fazer seus `commits`, o GitHub ainda não saberá que ela existe. Para "empurrar" a branch nova pela primeira vez, use:

```bash
git push -u origin nome-da-sua-branch

```

O parâmetro `-u` serve para que o Git lembre que essa branch local está conectada àquela que você acabou de criar no servidor.

### Resumo de boas práticas

* **Nomes curtos e claros:** Use nomes como `feature-login`, `ajuste-layout` ou `fix-bug-calculo`.
* **Evite espaços:** Use hífens (`-`) ou underscores (`_`).
* **Verifique onde você está:** Digite `git branch` para ver a lista de ramos e identificar em qual você está (ele aparecerá com um asterisco `*`).

Quer que eu te ajude a pensar em um padrão de nomes para as branches do seu projeto "Fabrica de monstros"?