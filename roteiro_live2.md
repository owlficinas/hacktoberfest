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

![Ciclo de vida dos arquivos gerenciados pelo git](img/git1.png)

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

### Modifiquei os arquivos, como eu adiciono eles pra essa staging area?

O primeiro passo para indicar que queremos criar alterações no histórico é
adicionar os arquivos na **staging area**. Essa área é como se fosse uma mesa de
preparação, onde reunimos todas as modificações que queremos fazer, para então
adicioná-las

> O `git add` é o comando utilizado para adicionar arquivos à staging area

### Ok, mas já está no histórico?

Não! Para adicionarmos um conjunto de mudanças ao histórico, precisamos fazer um
**commit** após adicionar os arquivos à *staging area*. Um commit contém, além
dos arquivos modificados, uma mensagem e uma autoria.

>**Somente após um commit, nossas mudanças são registradas no histórico**. O
>comando para isso é o `git commit`

### Show! Fiz meu commit, todo mundo consegue ver o que eu fiz já?

Ainda não! Como foi dito no começo, a maior parte do trabalho no git é feita
offline. Para enviar para o repositório **remoto**, precisamos fazer um
**push**.

>**Somente após o push, os commits que adicionamos ao histórico são enviados ao
>servidor**. Para isso, utilizamos o `git push`

### Alguém fez um push na minha frente e meu código ficou desatualizado. E agora?

Sim! Mas não tem problema, o Git te impede de fazer um push caso isso aconteça,
porque você ainda não está com a versão atualizada do código. Para fazer essa
atualização, você precisa fazer um **git pull**, que é o comando para
atualizarmos nosso repositório local com as mudanças no repositório remoto

>**O `git pull` "atualiza" o repositório com as mudanças que foram feitas
>enquanto estávamos trabalhando offline**

### Bacana, mas como eu "baixo" um repositório?

O comando de **clone** baixa todo o histórico de commits e os arquivos de um
repositório:

> `git clone <url-do-repositório>`

### E eu posso sair mexendo no código dos outros assim?

Claro que não! Mesmo que o código seja aberto, não significa que qualquer pessoa
possa modificá-lo sem qualquer tipo de verificação. Somente as pessoas
mantenedoras de um repositório podem modificar seu conteúdo

Por isso, o primeiro passo após escolhermos em qual repositório queremos
contribuir é criar uma bifurcação, ou **fork**. Assim, temos uma cópia do
repositório que podemos modificar livremente, sem afetar o repositório original

> Para solicitarmos mudanças em projetos nos quais não somos pessoas mantenedoras,
> primeiro temos que criar um **fork** do repositório. Um fork compartilha as
> configurações de código e visibilidade do repositório original, normalmente
> chamado de **upstream**

:warning: Uma vez que um fork é feito, apesar de termos **visibilidade** das
mudanças que foram feitas no original, os arquivos em si não são modificados.
Somente quando fazemos um **sync**, efetivamente recebemos essas modificações.

### E se eu já for uma pessoa mantenedora?

Aí você não precisa de um fork! No entanto, como muitas vezes não queremos
alterar imediatamente o código principal, podemos fazer uma **ramificação (ou
*branch*)** do nosso código.

Uma *branch* é essencialmente um ponto onde é criada uma "linha do tempo
alternativa" para modificarmos o conteúdo do repositório sem modificar
diretamente o histórico principal

> Branches são ramificações no histórico do nosso repositório para podermos
> modificar o código sem alterar o código da branch principal

### Terminei minhas mudanças! E agora?

Após fazer as modificações no seu fork ou na sua branch, podemos solicitar que
elas sejam adicionadas ao repositório principal com um **pull request (ou PR)**.
Após abrir o PR, outras pessoas podem comentar, solicitar mais mudanças e/ou
correções, e eventualmente aprovar ou rejeitar as mudanças.

> Um PR é uma solicitação de mudança para adicionar alterações de uma branch ou
> um fork para outra branch (normalmente, mas não necessariamente, do
> repositório original)

## Resumo
![Resumo dos comandos do Git](img/git2.png)

 - No GitHub, crie um fork do repositório que você deseja contribuir
 - `git clone` pra baixar o repositório "forkado"
 - `git add` para adicionar os arquivos modificados ou que ainda
   não estão no repositório para a **staging area**
 - `git commit` para adicionar uma nova entrada no histórico
 - `git push` para enviar esses commits para o repositório remoto
 - Abra um PR para solicitar que suas mudanças sejam adicionadas ao repositório
   original

## Materiais úteis

- Nunca usou Git? [Dá pra aprender a se virar em 10 minutos!](https://www.freecodecamp.org/portuguese/news/aprenda-o-basico-de-git-em-menos-de-10-minutos/)
- Ainda não entendeu direito esse negócio de branches e forks? Tem esse tutorial
  interativo [aqui](https://learngitbranching.js.org/?locale=pt_BR)
- A [documentação do GitHub](https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/getting-started/about-collaborative-development-models#fork-and-pull-model) é muito boa para aprender como funcionam os forks e pull requests
