# Documento de Requisitos — NEURAL_DEV_v1.0

## 1. Objetivo

Este documento descreve os requisitos identificados a partir do arquivo `index.html`, considerando exclusivamente o comportamento, conteúdo, componentes e tecnologias explicitamente presentes no HTML/CSS.

O projeto corresponde a uma página web em português (pt-BR), intitulada **“IA Generativa Aplicada à Programação”**, apresentada como um portfólio/perfil profissional com temática cyberpunk/terminal.

> **Nota:** o HTML não contém JavaScript funcional, portanto não foram identificadas classes JavaScript, funções de aplicação, APIs executadas ou regras de negócio implementadas no cliente. As “funções” abaixo representam funcionalidades visuais/navegacionais observáveis no documento.

---

## 2. Identificação do Projeto

| Item | Valor |
|---|---|
| Título da página | IA Generativa Aplicada à Programação |
| Identificador visual | NEURAL_DEV_v1.0 |
| Idioma | pt-BR |
| Tipo | Página web/portfólio |
| Tema | Cyberpunk / terminal / CRT |
| Framework CSS | Tailwind CSS via CDN |
| Ícones | Material Symbols Outlined |
| Fontes | JetBrains Mono e Space Mono |
| Responsividade | Sim, baseada em breakpoints do Tailwind |
| JavaScript próprio | Não identificado |
| Backend | Não identificado |

---

## 3. Estrutura Funcional

A página é composta pelos seguintes módulos:

1. Navegação principal
2. Hero / perfil
3. Informações do curso
4. Base de conhecimento
5. Stack tecnológica
6. Banco de projetos
7. Jornada de aprendizado
8. Habilidades desbloqueadas
9. Terminal interativo visual
10. Repositórios GitHub
11. Área de contato
12. Rodapé

---

## 4. Principais Funções do Projeto

### FR-001 — Navegação entre seções

O sistema deve disponibilizar uma barra de navegação superior contendo links para:

- Início
- Sobre
- Curso
- Tecnologias
- Projetos
- Contato

Os links existentes utilizam âncoras HTML (`href="#..."`) para navegação dentro da página.

**Observação:** o menu referencia `#sobre`, porém não existe uma seção com `id="sobre"` no HTML fornecido.

### FR-002 — Apresentação do perfil

A página deve apresentar uma área inicial contendo:

- identificação do módulo `HERO_MODULE`;
- mensagens de inicialização;
- título principal;
- imagem de perfil;
- nome do usuário;
- função profissional;
- descrição profissional.

O conteúdo do nome e da foto possui placeholders, como `[SEU NOME]` e `[ SUA FOTO AQUI ]`.

### FR-003 — Exibição das informações do curso

O sistema deve apresentar:

- instituição: SENAI Ary Torres;
- duração: 48h;
- instrutor: Prof. Leandro Toniati.

### FR-004 — Exibição da base de conhecimento

A página deve apresentar cards para:

- Conceitos IA
- Machine Learning
- IA Generativa
- Python
- GitHub
- Java + IA
- APIs
- Chatbots

Os cards possuem efeitos visuais de hover.

### FR-005 — Exibição da stack tecnológica

A página deve listar:

- Python
- Java
- ChatGPT
- Node.js
- SQL
- AWS

Cada item possui ícone e efeito visual de interação ao passar o mouse.

### FR-006 — Apresentação de projetos

O sistema deve apresentar quatro projetos com:

- identificador;
- status;
- descrição;
- tecnologias utilizadas.

Projetos identificados:

| Projeto | Status | Tecnologias |
|---|---|---|
| PROJETO_01 | Ativo | Python, OpenAI API |
| PROJETO_02 | Implementado | Java, Hadoop |
| PROJETO_03 | Em desenvolvimento | Node.js, Dialogflow |
| PROJETO_04 | Arquivado | Python, TensorFlow |

### FR-007 — Exibição da jornada de aprendizado

A página deve apresentar uma linha do tempo contendo:

1. Introdução à Programação e Lógica Básica.
2. Programação Orientada a Objetos com Java/Python.
3. Conceitos básicos de Machine Learning e Redes Neurais.
4. Desenvolvimento de aplicação full-stack com integração de IA Generativa.

### FR-008 — Exibição de habilidades

O sistema deve listar as seguintes habilidades:

- Algoritmos e Estruturas de Dados
- Programação Orientada a Objetos
- Integração de APIs RESTful
- Treinamento de Modelos de ML Básicos
- Prompt Engineering Avançado
- Versionamento de Código (Git/GitHub)
- Desenvolvimento de Chatbots (NLP)
- Arquitetura de Microsserviços Básica
- Deploy em Cloud (AWS/GCP basics)

### FR-009 — Exibição do terminal

A página deve apresentar um terminal visual contendo comandos e respostas simuladas, incluindo:

- execução de script de apresentação;
- carregamento do perfil;
- exibição da função profissional;
- consulta das informações do curso;
- comando de ping para `servidor_contato`.

O HTML não implementa execução real desses comandos.

### FR-010 — Exibição de repositórios GitHub

A página deve apresentar dois repositórios:

- `visualizador-rede-neural`
- `refatoracao-codigo-auto`

Cada item contém nome e descrição.

Os links estão configurados como `href="#"`, portanto não apontam para URLs reais no arquivo analisado.

### FR-011 — Disponibilização de canais de contato

A área de contato deve apresentar ações para:

- iniciar link do GitHub;
- iniciar link do LinkedIn;
- transmitir e-mail seguro.

No HTML analisado, os três links utilizam `href="#"` e não possuem integração funcional.

### FR-012 — Rodapé

O rodapé deve apresentar:

- copyright `© 2024 GEN_AI_LAB`;
- status do sistema `OPERACIONAL`;
- links visuais para GitHub, LinkedIn e terminal.

Os links do rodapé também utilizam `href="#"`.

---

## 5. Principais Classes e Componentes

Como o projeto fornecido é um único HTML sem classes de domínio em JavaScript, as principais “classes” identificáveis são classes CSS e agrupamentos estruturais.

### 5.1 Classes CSS customizadas

#### `.crt`

Aplica uma camada visual semelhante a monitor CRT utilizando pseudo-elemento `::before`.

Características:

- linhas horizontais;
- efeito de separação RGB;
- posição fixa;
- `z-index: 999`;
- não interfere com eventos (`pointer-events: none`).

#### `.glow`

Aplica brilho ao texto por meio de `text-shadow`.

#### `.border-glow`

Aplica brilho às bordas por meio de `box-shadow`.

#### `.typing-effect`

Implementa efeito visual de digitação utilizando:

- `overflow: hidden`;
- `border-right`;
- `white-space: nowrap`;
- animação `typing`;
- animação `blink-caret`.

#### `.glitch-hover`

Aplica efeito de glitch durante o hover.

#### `.bg-grid`

Cria uma grade de fundo usando dois gradientes lineares.

---

## 6. Animações CSS

### `typing`

Anima a largura de um elemento de zero até 100%.

### `blink-caret`

Alterna a cor da borda direita para simular cursor piscando.

### `glitch-skew`

Altera progressivamente o `skew` do elemento durante o efeito glitch.

---

## 7. Componentes Estruturais HTML

### `nav`

Responsável pela navegação superior.

Principais características:

- sticky;
- largura total;
- borda inferior;
- backdrop blur;
- menu responsivo.

### `main`

Contêiner principal da página.

Utiliza:

- largura máxima;
- espaçamento vertical entre seções;
- margens horizontais;
- comportamento responsivo.

### `section#inicio`

Módulo de apresentação/hero.

### `section#curso`

Módulo de informações do curso.

### `section#conhecimento`

Módulo da base de conhecimento.

### `section#tecnologias`

Módulo da stack tecnológica.

### `section#projetos`

Módulo de projetos.

### `section#jornada`

Módulo da jornada de aprendizado.

### `section#habilidades`

Módulo de habilidades.

### `section#terminal`

Módulo de terminal visual.

### `section#github`

Módulo de repositórios.

### `section#contato`

Módulo de comunicação.

### `footer`

Rodapé institucional.

---

## 8. Requisitos Funcionais Detalhados

### RF-01 — Navegação interna

**Descrição:** permitir acesso às principais áreas da página através da navegação superior.

**Entrada:** clique em um item do menu.

**Saída esperada:** navegação para a seção correspondente.

**Dependência:** IDs HTML das seções.

**Problema identificado:** o link `SOBRE` aponta para `#sobre`, mas o documento não possui essa âncora.

### RF-02 — Responsividade

**Descrição:** adaptar a apresentação para diferentes larguras de tela.

**Evidência:** utilização de classes Tailwind como `md:`, `sm:` e `lg:`.

**Comportamento esperado:** reorganização das grades e disposição dos elementos conforme o tamanho da viewport.

### RF-03 — Apresentação visual cyberpunk

**Descrição:** utilizar estética visual baseada em terminal, neon verde, CRT e glitch.

**Recursos:** classes `.crt`, `.glow`, `.border-glow`, `.glitch-hover` e `.bg-grid`.

### RF-04 — Cards de conhecimento

**Descrição:** apresentar os tópicos da base de conhecimento em cards.

**Interação:** efeitos de hover.

**Limitação atual:** não existe ação funcional associada ao clique dos cards.

### RF-05 — Cards de projetos

**Descrição:** apresentar projetos e seus respectivos estados.

**Dados mínimos:**

- nome;
- status;
- descrição;
- tecnologias.

### RF-06 — Linha do tempo

**Descrição:** representar visualmente a evolução do aprendizado.

**Interação:** visual somente; não foram identificados controles ou navegação dinâmica.

### RF-07 — Terminal visual

**Descrição:** apresentar uma simulação de terminal.

**Limitação:** os comandos exibidos são conteúdo estático. Não há entrada de teclado ou processamento JavaScript.

### RF-08 — Links externos

**Descrição:** permitir acesso a GitHub, LinkedIn e e-mail.

**Estado atual:** links ainda não configurados, pois utilizam `href="#"`.

---

## 9. Requisitos Não Funcionais

### RNF-01 — Interface responsiva

A interface deve funcionar em diferentes tamanhos de tela utilizando os breakpoints disponíveis no Tailwind CSS.

### RNF-02 — Identidade visual consistente

A interface deve preservar a identidade visual baseada em:

- fundo escuro;
- verde neon;
- tipografia monoespaçada;
- bordas destacadas;
- estética terminal/CRT.

### RNF-03 — Tipografia

Devem ser utilizadas as fontes:

- JetBrains Mono;
- Space Mono.

### RNF-04 — Ícones

Os ícones devem utilizar Material Symbols Outlined conforme as referências existentes no HTML.

### RNF-05 — Acessibilidade estrutural

Os elementos devem permanecer semanticamente organizados em navegação, conteúdo principal, seções e rodapé.

**Observação:** o HTML não apresenta evidências suficientes para afirmar conformidade completa com WCAG.

### RNF-06 — Desempenho

O projeto utiliza recursos externos via CDN:

- Tailwind CSS;
- Google Fonts;
- Material Symbols.

A disponibilidade desses recursos depende de conectividade externa.

---

## 10. Tecnologias e Dependências

### Front-end

- HTML5
- Tailwind CSS
- CSS3

### Bibliotecas/recursos externos

- Tailwind CSS CDN
- Google Fonts
- Material Symbols Outlined

### Tecnologias mencionadas no conteúdo do portfólio

- Python
- Java
- Node.js
- SQL
- AWS
- ChatGPT
- GitHub
- OpenAI API
- Hadoop
- Dialogflow
- TensorFlow
- GCP

**Importante:** as tecnologias acima são mencionadas como stack, projetos ou habilidades. O HTML não comprova que todas estejam efetivamente implementadas na página.

---

## 11. Modelo de Dados Visual

O projeto utiliza informações estruturadas diretamente no HTML, sem banco de dados identificado.

### Curso

```text
Curso
├── Instituição
├── Duração
└── Instrutor
```

### Projeto

```text
Projeto
├── Identificador
├── Status
├── Descrição
└── Tecnologias
```

### Repositório

```text
Repositório
├── Nome
└── Descrição
```

### Habilidade

```text
Habilidade
└── Descrição
```

---

## 12. Regras e Estados Identificados

Os projetos utilizam estados textuais:

- `ATIVO`
- `IMPLEMENTADO`
- `EM DESENVOLVIMENTO`
- `ARQUIVADO`

A jornada utiliza estados de progresso:

- `SEQUENCIA_INICIAL`
- `MODULO_01_COMPLETO`
- `INTEGRACAO_IA_INICIALIZADA`
- `EXECUCAO_PROJETO_FINAL`

Esses estados são apresentados visualmente e não possuem lógica de alteração implementada.

---

## 13. Integrações Identificadas

### Tailwind CSS

Carregado externamente por CDN.

### Google Fonts

Utilizado para carregar:

- JetBrains Mono;
- Space Mono;
- Material Symbols Outlined.

### GitHub/OpenAI/etc.

São referências de conteúdo do portfólio. Não há chamadas de API, autenticação ou integração funcional implementada no HTML fornecido.

---

## 14. Pontos Pendentes para Implementação

Os seguintes elementos aparecem como intenção funcional, mas não estão implementados:

1. URL real do GitHub.
2. URL real do LinkedIn.
3. Link funcional de e-mail.
4. Links dos repositórios.
5. Conteúdo/âncora da seção `#sobre`.
6. Interatividade real dos cards da base de conhecimento.
7. Execução real do terminal.
8. Processamento de comandos no terminal.
9. Integrações com APIs.
10. Persistência de dados.
11. Backend.
12. Autenticação.
13. Banco de dados.
14. Formulário real de contato.

---

## 15. Critérios de Aceitação

### CA-01 — Navegação

- O menu deve apresentar as opções previstas.
- Cada opção deve direcionar à seção correspondente.
- A âncora `#sobre` deve ser criada ou o link deve ser removido/corrigido.

### CA-02 — Perfil

- A área inicial deve apresentar nome, função, descrição e imagem.
- Os placeholders devem ser substituídos pelos dados definitivos.

### CA-03 — Curso

- Instituição, duração e instrutor devem ser exibidos corretamente.

### CA-04 — Tecnologias

- Os seis itens da stack devem ser apresentados.
- A disposição deve permanecer adequada em desktop e mobile.

### CA-05 — Projetos

- Os quatro projetos devem apresentar identificador, status, descrição e tecnologias.

### CA-06 — Contato

- GitHub, LinkedIn e e-mail devem possuir destinos reais antes da publicação.

### CA-07 — Terminal

- Caso seja desejada interatividade real, comandos devem ser processados por JavaScript ou backend.
- Caso permaneça demonstrativo, deve ser tratado explicitamente como terminal visual estático.

---

## 16. Limitações da Análise

A análise foi baseada exclusivamente no `index.html` fornecido.

Não foram identificados no arquivo:

- arquivos JavaScript externos próprios;
- classes de programação em JavaScript;
- funções JavaScript;
- endpoints;
- banco de dados;
- arquivos de configuração de backend;
- componentes de framework;
- testes automatizados;
- regras de autenticação;
- lógica de negócio executável.

Portanto, não é possível afirmar a existência dessas funcionalidades apenas com base no arquivo analisado.

---

## 17. Resumo Executivo

O projeto é uma **landing page/portfólio pessoal voltada a IA generativa aplicada à programação**, construída em HTML com Tailwind CSS e CSS customizado.

Sua principal função é apresentar visualmente:

- perfil profissional;
- formação;
- conhecimentos;
- tecnologias;
- projetos;
- jornada de aprendizado;
- habilidades;
- repositórios;
- canais de contato.

A arquitetura atual é essencialmente **estática e client-side**, sem lógica JavaScript identificada. A maior parte das interações observadas são efeitos CSS e navegação por âncoras.

Para transformar o protótipo em uma aplicação funcional, os principais próximos passos seriam configurar os links reais, implementar as interações pretendidas e, caso necessário, adicionar JavaScript/backend para terminal, contatos, integrações e persistência.
