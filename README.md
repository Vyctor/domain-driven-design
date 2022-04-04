- [Domain Driver Design](#domain-driver-design)
  - [O que é?](#o-que-é)
  - [De onde vem?](#de-onde-vem)
  - [Complexidade de Software](#complexidade-de-software)
  - [Como o DDD pode me ajudar?](#como-o-ddd-pode-me-ajudar)
  - [Resumindo](#resumindo)
- [Domínios, subdomínios e contextos](#domínios-subdomínios-e-contextos)
  - [Domínio vs subdomínio](#domínio-vs-subdomínio)
  - [Escopo do problema vs espaço da solução](#escopo-do-problema-vs-espaço-da-solução)
  - [O que é um contexto delimitado (Bounded Context)?](#o-que-é-um-contexto-delimitado-bounded-context)
  - [Contexto é rei](#contexto-é-rei)
  - [Elementos transversais](#elementos-transversais)
- [Visão estratégica](#visão-estratégica)
  - [Modelagem estratégica / Context Mapping](#modelagem-estratégica--context-mapping)
  - [Padrões e starter kit](#padrões-e-starter-kit)

## Domain Driver Design

### O que é?

É uma forma de desenvolver software com o foco no coração da aplicação - o que chamamos de domínio - tendo o objetivo de entender suas regras, processos e complexidades, separando-as assim de outros pontos complexos que normalmente são adicionados durante o processo de desenvolvimento.

### De onde vem?

- Eric Evans foi o criador, lançando um livro em 2003 com Filosofia, Exemplos Gerais e Patterns.
- Vaughn Vernon, escreveu implementando domain driven design e domain driven design destilado.

### Complexidade de Software

- DDD é/deve ser aplicado para casos de projetos de software complexos
- Grandes projetos possuem muitas áreas, muitas regras de negócio, muitas pessoas com diferentes visões em diferentes contextos
- Não há como não utilizar técnicas avançadas em projetos de alta complexidade
- Grande parte da complexidade desse tipo de software não vem da tecnologia, mas sim da comunicação, separação de contextos, entendimentos do negócio por diversos ângulos
- Pessoas

### Como o DDD pode me ajudar?

- Entender com profundidade o domínio e subdomínios da aplicação
- Ter uma linguagem universal (ubíqua) entre todos os envolvidos
- Criar o design estratégico utilizando Bounded Contexts
- Criar o design tático para conseguir mapear e agregar as entidades e objetos de valor da aplicação, bem como os eventos do domínio
- Clareza do que é complexidade de negócio e complexidade técnica

### Resumindo

- DDD é primariamente sobre modelar uma linguagem universal em um contexto delimitado explicito.

## Domínios, subdomínios e contextos

### Domínio vs subdomínio

- Divisão dos domínios em subdomínios
  - Quando começo a olhar o domínio percebo que há várias coisas inerentes ao sistema
  - Percebo que existem graus de importância desse subdomínio para o negócio
- Core Domain
  - Domínio Principal
  - Razão de tudo existir
  - Coração do negócio
  - Diferencial competitivo da empresa
- Support Subdomain
  - Apoia o domínio
  - Faz a operação do domínio possível
- Generic Subdomain
  - Apoia o sistema mas não possui diferencial competitivo para a empresa
  - Softwares auxiliares

### Escopo do problema vs espaço da solução

Como partimos do entendimento do domínio até a modelagem, da separação do domínio em subdomínio e a separação dos subdomínios em contextos delimitados.

- Problema
  - Visão geral do domínio e suas complexidades
  - Subdomínios
- Solução
  - Análise e modelagem do domínio
  - Contextos delimitados

### O que é um contexto delimitado (Bounded Context)?

É uma divisão explícita dentro de um modelo de domínio. Dentro do limite todos termos e frases da linguagem ubíqua tem um significado específico, e o modelo reflete a linguagem com exatidão.

### Contexto é rei

- O contexto sempre vai determinar a área que estamos trabalhando e o problema que iremos resolver.
- Exemplo:
  - ticket (venda de ingressos)
  - ticket (suporte ao cliente)
- Quando eu tenho duas palavras diferentes que significam a mesma coisa, provavelmente estou em um contexto diferente

### Elementos transversais

- Muitas vezes apesar de estarmos em contextos diferentes, estes contextos se conversam.
  - Exemplo
    - Cliente (vendas de ingressos)
    - Cliente (suporte ao cliente)
- Quando uma entidade tem mais de um contexto devo criá-la nos diferentes contextos, evitando que uma entidade tente abarcar todas as possíveis implementações de contextos diferentes

## Visão estratégica

### Modelagem estratégica / Context Mapping

- Vendas de ingressos online
- Vendas de ingressos parceiros
- Suporte ao cliente
- Pagamento

### Padrões e starter kit

- Padrões
  - Partnership
  - Shared Kernel
  - Customer-Supplier Development
  - Conformist
  - Anticorruption-layer
  - Open host service
  - Published language
  - Separated ways
  - Big Ball of Mud

[Starter Kit - Context Mapping](https://github.com/ddd-crew/context-mapping)
