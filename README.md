# CPAT Campinas — Digital

Projeto de modernização digital do CPAT Campinas (Centro Público de Apoio ao Trabalhador, Secretaria Municipal de Trabalho e Renda), reunindo identidade visual, design UI/UX, protótipos, ilustrações, materiais gráficos e o desenvolvimento de uma plataforma digital para aproximar trabalhadores das oportunidades de emprego, com uma experiência mais acessível, intuitiva e eficiente.

> **Status:** fase de design e documentação. O front-end (v1) ainda não foi iniciado.

## Problema e objetivo

O site atual é antigo, pouco funcional e não atende critérios de acessibilidade. O objetivo é entregar um site moderno que ajude o cidadão a encontrar vagas, entender os serviços e falar com a Prefeitura, seguindo o Gov.br Design System, WCAG 2.1 AA e eMAG.

## Antes e depois

Na coluna "antes", os prints do site atual trazem anotações de problemas de interface (UI Annotation). Cada número aponta para um problema listado ao lado.

### Home

![Home: antes e depois](docs/img/comparativo/home.png)

Anotações completas do site atual: [`antes-home.png`](docs/img/antes/antes-home.png)

### Vagas de emprego

![Vagas: antes e depois](docs/img/comparativo/vagas.png)

Anotações completas do site atual: [`antes-vagas.png`](docs/img/antes/antes-vagas.png)

### Serviços

![Serviços: antes e depois](docs/img/comparativo/servicos.png)

Anotações completas do site atual: [`antes-servicos.png`](docs/img/antes/antes-servicos.png)

## Telas do redesign

Protótipo seguindo o Gov.br Design System, com modo claro e escuro, ajuste de fonte (A−/A+) e VLibras. Os arquivos editáveis estão em [`mockups/redesign-govbr/`](mockups/redesign-govbr/).

| Home (claro) | Home (escuro) |
| --- | --- |
| ![Home](docs/img/depois/home.png) | ![Home escuro](docs/img/depois/home-escuro.png) |

| Vagas de emprego | Serviços |
| --- | --- |
| ![Vagas](docs/img/depois/vagas.png) | ![Serviços](docs/img/depois/servicos.png) |

| Atendimento (SAC e Ouvidoria) | Institucional |
| --- | --- |
| ![Atendimento](docs/img/depois/atendimento.png) | ![Institucional](docs/img/depois/institucional.png) |

| Mobile (claro) | Mobile (escuro) |
| --- | --- |
| <img src="docs/img/depois/mobile.png" width="320" alt="Mobile claro"> | <img src="docs/img/depois/mobile-escuro.png" width="320" alt="Mobile escuro"> |

Design System: [ver página completa](docs/img/depois/design-system.png)

## Nova identidade visual

Brand Book proposto, com o conceito "Oportunidades que conectam pessoas". Texto de apoio em [docs/identidade-visual.md](docs/identidade-visual.md).

![Capa do Brand Book](docs/img/identidade/capa.png)

| | |
| --- | --- |
| ![Conceito](docs/img/identidade/conceito.png) | ![Logotipo](docs/img/identidade/logotipo.png) |
| ![Cores](docs/img/identidade/cores.png) | ![Tipografia](docs/img/identidade/tipografia.png) |
| ![Elementos gráficos](docs/img/identidade/elementos.png) | ![Ilustrações](docs/img/identidade/ilustracoes.png) |
| ![Ícones](docs/img/identidade/icones.png) | ![Aplicações 1](docs/img/identidade/aplicacoes-1.png) |

![Aplicações 2](docs/img/identidade/aplicacoes-2.png)

## Estrutura do repositório

```
cpat-digital/
├── docs/        # Documentação (briefing, requisitos, identidade visual) e imagens (docs/img)
├── design/      # Identidade visual (Brand Book) e referências
├── assets/      # Logos, ícones e ilustrações
├── flyers/      # Flyers e materiais gráficos
├── banners/     # Banners institucionais
├── mockups/     # Protótipos e apresentações
├── frontend/    # Interface do usuário
├── backend/     # API e regras de negócio
└── README.md    # Apresentação do projeto
```

## Conteúdo atual

| Pasta | O que há |
| --- | --- |
| [`docs/`](docs/) | [Briefing](docs/briefing.md) (problema, solução, personas, requisitos, stack, SEO, escopo da v1) e [guia da identidade visual](docs/identidade-visual.md) |
| [`design/`](design/) | Brand Book em canvas do Claude Design: conceito, logotipo, cores, tipografia, elementos, ilustrações, ícones e aplicações |
| [`assets/logo/`](assets/logo/) | Símbolo do CPAT em SVG (cor, monocromático e negativo) |
| [`mockups/redesign-govbr/`](mockups/redesign-govbr/) | Protótipo do redesign (Home clara e escura, Vagas, Atendimento, Institucional, Serviços, Design System e Mobile) |
| `flyers/`, `banners/`, `frontend/`, `backend/` | Reservadas; cada uma tem um README com o plano |

Os arquivos `.dc.html` são exportações de canvas do Claude Design e abrem nele, não direto no navegador.

## Stack prevista

- **v1 (só front-end):** Angular + Tailwind CSS, seguindo o Gov.br Design System (GovDS) e o Design System do CPAT; dados de vagas em JSON de exemplo atrás de um serviço.
- **v2:** back-end e API de vagas (hipótese: Ruby on Rails e PostgreSQL), envio real de SAC e Ouvidoria e integração com o Emprega Brasil.

## Identidade visual

Conceito **"Oportunidades que conectam pessoas"**. Paleta: Azul Campinas `#0B2F7A`, Azul Conexão `#1F5BFF`, Grafite `#161C2A` e Âmbar `#FFB81C`. Tipografia: Sora e Inter. Detalhes em [docs/identidade-visual.md](docs/identidade-visual.md).

## Pendências

- Validar briefing e personas com a equipe do CPAT e revisar textos e dados com a SMTR.
- Definir a fonte dos dados de vagas e confirmar o link oficial do Emprega Brasil.
- Testar o protótipo com usuários reais, incluindo pessoas com deficiência.
- Criar o projeto Angular com Tailwind CSS.

## Autor

Paulo Antonio — [GitHub](https://github.com/Paul0Ant0ni0)
