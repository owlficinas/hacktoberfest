# Live 2 - Introdução a Git e GitHub

## O que é Git? E GitHub?

Ferramenta de controle de versão utilizada para acompanhar e gerenciar
alterações em arquivos textuais, geralmente código. Os conjunto dos arquivos que
são gerenciados pelo Git é chamado de **repositório**.

O que o diferencia de outras ferramentas de versionamento é que a maior parte do
seu funcionamento é **offline**: Podemos gerar novas versões do nosso código
localmente, e enviá-las a um servidor somente ao final.

O **GitHub** é um dos servidores que hospedam códigos versionados pelo Git, e hoje é
a maior plataforma de hospedagem de código do mundo.

## Legal! E como funciona esse tal de Git?

![Ciclo de vida dos arquivos gerenciados pelo git](https://git-scm.com/book/en/v2/images/lifecycle.png)

### Três estados

Quando estamos dentro de uma pasta gerenciada pelo git, temos três estados
possíveis para cada arquivo:

1. **Não modificado (ou *unmodified*)**: Os arquivos que estão sendo monitorados
   pelo git estão no estado **não modificado**, ou seja, não há mudanças em
   relação ao estado anterior.

2. **Modificado (ou *modified*)**: Uma vez que alteramos o arquivo, ele entra no estado de
   **modificado**. O Git detectou que houve mudança, mas como não indicamos a
   ele que queremos adicionar essa mudança ao histórico, nada é feito ainda.

3. **Preparado (ou *staged*)**: Uma vez que queremos adicionar as mudanças
   feitas nos arquivos ao histórico, devemos **adicionar** ela à área de
   preparação (ou *staging area*). Essa área indica que queremos que as
   modificações façam parte do histórico do nosso repositório.

Além disso, novos arquivos que ainda não foram adicionados ao histórico ficam
em outro estado: **não rastreados (ou *untracked*)** 

### Ok, mas já está no histórico?

Não! Para adicionarmos um conjunto de mudanças ao histórico, precisamos fazer um
**commit** após adicionar os arquivos à *staging area*. Um commit contém, além
dos arquivos modificados, uma mensagem e uma autoria.

>**Somente após um commit, nossas mudanças são registradas no histórico**

### Show! Fiz meu commit, todo mundo consegue ver o que eu fiz já?

Ainda não! Como foi dito no começo, a maior parte do trabalho no git é feita
offline. Para enviar para o repositório **remoto**, precisamos fazer um
**push**.

>**Somente após o push, os commits que adicionamos ao histórico são enviados ao
>servidor**

### E se alguém fez um push na minha frente? Meu código não vai estar desatualizado?

Sim! Mas não tem problema, o Git te impede de fazer um push caso isso aconteça,
porque você ainda não está com a versão atualizada do código. Para fazer essa
atualização, você precisa fazer um **git pull**, que é o comando para
atualizarmos nosso repositório local com as mudanças no repositório remoto

>**O git pull "atualiza" o repositório com as mudanças que foram feitas
>enquanto estávamos trabalhando offline**

### Bacana, mas como eu "baixo" um repositório?

O comando de **clone** baixa todo o histórico de commits e os arquivos de um
repositório:

> `git clone <url-do-repositório>`

## Resumo
 - `git clone` pra baixar o repositório
 - `git add` para adicionar os arquivos modificados ou que ainda
   não estão no repositório para a **staging area**
 - `git commit` para adicionar uma nova entrada no histórico
 - `git push` para enviar esses commits para o repositório remoto

## Materiais úteis

- Nunca usou Git? [Dá pra aprender a se virar em 10 minutos!](https://www.freecodecamp.org/portuguese/news/aprenda-o-basico-de-git-em-menos-de-10-minutos/)
- Já usou Git, mas ainda não entendeu esse negócio de branches? Tem esse tutorial
  interativo [aqui](https://learngitbranching.js.org/?locale=pt_BR)
- A [documentação do GitHub](https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/getting-started/about-collaborative-development-models#fork-and-pull-model) é muito boa para aprender como funcionam os forks e pull requests
