# AppMonitor Pipeline

## O Papel do Git na Entrega Contínua e a importância das branches e tags


O Git oferece recursos essenciais que tornam a Entrega Contínua possível e eficiente:

controle de versão distribuído que permite um trabalho cooperativo e eficiente. Mantem um histórico completo de alterações, facilita a identificação e resolução de conflitos.

Git tambem permite integração com pipelines de CI/CD, automatização de builds e testes, deploy automatizado para diferentes ambientes, rastreabilidade de mudanças em produção(graças ao histórico de commits).

Permite recuperar/voltar a estados anteriores a um commit caso tenha feito errado,


### A Importância de Branches e Tags


As branches são a base do git e do desenvolvimento de software, com elas podemos isolar o desenvolvimento de novas features, correções de bugs, experimentação de novas funcionalidades sem impactar o código em produção, já que estamos trabalhando em uma cópia do código em produção ou em uma versão anterior.

E essas branches são classificadas pelos usuarios a fim de facilitar a identificação e o uso das branches e depois de feitas as alterações, elas são mescladas com a branch principal, ou seja, a branch principal é atualizada com as alterações das branches, usando um sistema de merge genial.

E as tags são usadas para marcar pontos específicos no histórico do projeto, como versões estáveis, releases, etc. É uma forma clara de marcar um ponto de mudança chave no projeto.

