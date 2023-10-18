 
# 📃 Como colaborar em um projeto open source - Git, GitHub, PRs, boas práticas

## Workflow para suas contribuições

![](https://hackmd.io/_uploads/rkDlqnpWp.png)
  
## Boas práticas

### Em commits

Uma mensagem de commit é uma descrição das mudanças que você fez em um (ou mais) arquivos antes de commitá-los. 

Boas mensagens de commit são importantes em projetos colaborativos e open-source, pois facilitam a leitura, aprovação. Também são importantes nos projetos individuais, pois você pode acompanhar as mudanças de commits específicos. 

Muitos dos repositórios que você irá contribuir já tem um conjunto de regras em relação a suas mensagens de commits, dê uma lida antes de começar a trabalhar e mantenha o padrão do repositório ou leia o CONTRIBUTING.md

Um padrão de commit é

```
Tipo: objetivo

corpo (opcional)

```

Exemplo:

`Feat: Add login system` 

```
Feat: Adicionar sistema de login

O sistema de login foi adicionado utilizando X, Y, Z
```

#### Tipo

- **feat** - nova feature
- **fix** - resolução de bug
- **docs** - mudanças na documentação
- **style** - tudo relacionado com styling
- **refactor** - refatoração de código (mudanças que não resolvem bugs nem adiciona features)
- **test** - tudo relacionado com testagem
- **chore** - atualizando configurações de package manager, etc

#### Objetivo

- Contém uma pequena descrição das mudanças feitas. 
- Não deve ser maior que 50 caracteres. 
- Deve começar começar com letra maiúscula
- Ser no modo imperativo


#### Corpo

É usado para explicar quais são as mudanças e o porquê de fazê-las. Nem todos commits são complexos o suficiente para ter um body.

- Deve ter uma linha vazia entre o objetivo e o corpo
- Cada linha não pode ter mais que 72 caracteres



### Em Pull Request (PR)

No Git, um "pull request" é um pedido para puxar as suas alterações de uma branch para outro, normalmente de uma branch de desenvolvimento/funcionalidades que você trabalha para a branch principal do projeto.

Como parte disso, os proprietários do projeto vão querer revisar a mudança que você está propondo para a base de código deles. As sugestões aqui são para ajudar a fazer com que esse processo de revisão seja rápido e tranquilo. Por mais útil que a sua proposta de alteração possa ser, um pull request mal feito pode resultar na rejeição da sua alteração.

Exemplo de um bom pull request:

![](https://hackmd.io/_uploads/SyoCCjTbp.png)


Um bom pull request deve ter

- Detalhes sobre mudanças feitas
- Se há alguma mudança que pode parar o projeto
- Se mudar algo visual, é boa prática colocar prints de antes e depois 
- Link com uma issue

#### Linke com uma issue

Uma issue é um problema que o repositório tem. Você pode criar um PR com uma modificação que resolva essa issue. 

Quando você relaciona um PR com uma issue, assim que seu PR for aceito, a issue é resolvida. Para isso, existem algumas palavras chave que você deve usar com o ID da issue:

- close
- closes
- closed
- fix
- fixes
- fixed
- resolve
- resolves
- resolved

Exemplo:

```fixes #10```



#### Crie uma branch

Na maioria dos projetos, não é possível adicionar uma mudança direto na branch principal. Então, quando for fazer seu PR, crie uma branch específica para ele.

#### Seja conciso

Single Responsability Principle - Um módulo deve ser responsável por um, e apenas um, objetivo. Ou seja, é necessário que seu pull request tenha apenas uma finalidade, o ideal não é ter um pull request que faça/resolva mil coisas ao mesmo tempo

#### Siga os padrões do repositório

Fazer um código limpo e, **principalmente**, manter os padrões do repositório que você está contribuindo. Novamente, lembrem de ler o CONTRIBUTING.md

#### Teste suas alterações

Testar o código é um dos passos mais importantes pra qualquer ambiente de desenvolvimento, você pode utilizar maneiras de testes automáticos ou testes manuais mesmo, o ideal é que o código não tenha erros gritantes para o PR

### Criando uma PR

Dê uma olhada no repositório para ver se não há instruções para PRs. Também veja se não há PRs já criadas que resolvem o problema.

#### Comunicação

Atribua outros usuários para revisarem sua PR, comunique pelo canal de comunicação principal usado pelos devs do projeto (discord, slack, etc.)

  
## Ferramentas

Algumas outros projetos do GitHub, mesmo não sendo relacionados ao open source, são ferramentas como quaisquer outras. Como programador, fique ciente da existência desses projetos e use-os quando necessário, pode vir a calhar durante sua jornada na Hacktoberfest e sua caminhada como dev.  


### GitHub Issues

Issues são "problemas" do código a ser resolvido
Permitem com que você

- Acompanhe as mudanças do seu projeto
- Acompanhar trabalhos relacionados com a sua issue
- Facilita comunicação e discussão sobre a resolução
- Permite também com que outras pessoas encontrem pontos de melhora no seu projeto


### GitHub Projects

O Github projects permite com que você crie um board de tarefas (que são as issues) no formato de kanban. Permite com que você acompanhe as issues, pull requests e andamento do projeto.


### GitHub Codespaces

Crie um espaço de desenvolvimento dentro do seu navegador

### GitHub Pages

Permite que você crie sites a partir de repositórios do GitHub

### GitHub copilot

Ganhe um autocomplete no seu editor de preferência (se tiver disponível suporte).
Basta pegar seu benefícios do Student Developer Pack da Github e aprovar o uso do Copilot nas suas configurações do Github


### GitHub Actions

Com essa ferramenta podemos rodar scripts automaticamente quando um certo evento acontece.

Exemplos: https://docs.github.com/en/actions/examples/using-scripts-to-test-your-code-on-a-runner



## Repositórios com *good first issues*

- https://github.com/morgannadev/octocats_da_comunidade/
- https://github.com/ozdemirburak/full-name-generator
- https://github.com/levxyca/diciotech
- https://github.com/Codess-Cafe/Codess-Website/issues
- https://github.com/Google-DSC-DMCE  
- https://github.com/USKhokhar/fehrist

## Referências

Em geral muito [Google](https://www.google.com/search?client=firefox-b-d&q=how+to+write+a+pull+request#ip=1) (sério)

Mais especificamente:

- [5 Tips to creating a (good) pull request](https://www.danijelavrzan.com/posts/2023/02/create-pull-request/)

- [Writing A Great Pull Request Description](https://www.pullrequest.com/blog/writing-a-great-pull-request-description/)

- [Anatomy of a perfect pull request](https://opensource.com/article/18/6/anatomy-perfect-pull-request)

- [Writing a Good Pull Request](https://developers.google.com/blockly/guides/contribute/get-started/write_a_good_pr)

