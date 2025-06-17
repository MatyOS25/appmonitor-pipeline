# AppMonitor Pipeline

[![CI Status](https://img.shields.io/github/actions/workflow/status/MatyOS25/appmonitor-pipeline/ci.yml?branch=ci%2Fsetup)](https://github.com/MatyOS25/appmonitor-pipeline/actions/workflows/ci.yml)

## O Papel do Git na Entrega Contínua e a importância das branches e tags


O Git oferece recursos essenciais que tornam a Entrega Contínua possível e eficiente:

controle de versão distribuído que permite um trabalho cooperativo e eficiente. Mantem um histórico completo de alterações, facilita a identificação e resolução de conflitos.

Git tambem permite integração com pipelines de CI/CD, automatização de builds e testes, deploy automatizado para diferentes ambientes, rastreabilidade de mudanças em produção(graças ao histórico de commits).

Permite recuperar/voltar a estados anteriores a um commit caso tenha feito errado,


### A Importância de Branches e Tags


As branches são a base do git e do desenvolvimento de software, com elas podemos isolar o desenvolvimento de novas features, correções de bugs, experimentação de novas funcionalidades sem impactar o código em produção, já que estamos trabalhando em uma cópia do código em produção ou em uma versão anterior.

E essas branches são classificadas pelos usuarios a fim de facilitar a identificação e o uso das branches e depois de feitas as alterações, elas são mescladas com a branch principal, ou seja, a branch principal é atualizada com as alterações das branches, usando um sistema de merge genial.

E as tags são usadas para marcar pontos específicos no histórico do projeto, como versões estáveis, releases, etc. É uma forma clara de marcar um ponto de mudança chave no projeto.





### Tipos de Variáveis

Vars: armazenam dados não sensíveis, visíveis nos logs do workflow, declarar `APP_ENV=dev` e uso: `${{ vars.NOME_DA_VARIAVEL }}`

Env: definidas no escopo do workflow ou job, disponíveis durante a execução, visíveis nos logs, declarar `SUPPORT_EMAIL=suporte@appmonitor.io` e uso: `${{ env.NOME_DA_VARIAVEL }}`

Secret: armazenam dados sensíveis (tokens, senhas), nunca visíveis nos logs, criptografados(em repouso), declarar: `API_KEY` e uso: `${{ secrets.NOME_DO_SEGREDO }}`


Existem contextos que são: repository, environment, organization.

Repository: variáveis disponíveis para todos os workflows

Environment: variáveis específicas para ambientes (staging, production)

Organization: variáveis compartilhadas entre repositórios da organização









## Logs e Summaries no GitHub Actions

O GitHub Actions oferece ferramentas poderosas para depuração e monitoramento de pipelines:

Logs de Debug são ativados com `ACTIONS_STEP_DEBUG=true` mostrando informações detalhadas de cada step e exibem tempo de execução e recursos utilizados

Job Summaries: resumos personalizados de cada job que suportam markdown para melhor formatação e podem incluir:
  - Status do ambiente (OS, branch)
  - Resultados de testes
  - Links para artefatos
  - Métricas importantes

Mensagens de Workflow
- `::warning::` para avisos importantes
- `::error::` para erros críticos
Isto aparece destacado na interface do GitHub









