# CPAT Campinas — Digital

Projeto de modernização digital do CPAT Campinas (Centro Público de Apoio ao Trabalhador, Secretaria Municipal de Trabalho e Renda), reunindo identidade visual, design UI/UX, protótipos, ilustrações, materiais gráficos e o desenvolvimento de uma plataforma digital para aproximar trabalhadores das oportunidades de emprego, com uma experiência mais acessível, intuitiva e eficiente.

> **Status:** fase de design e documentação. O front-end (v1) ainda não foi iniciado.

## Problema e objetivo

O site atual é antigo, pouco funcional e não atende critérios de acessibilidade. O objetivo é entregar um site moderno que ajude o cidadão a encontrar vagas, entender os serviços e falar com a Prefeitura, seguindo o Gov.br Design System, WCAG 2.1 AA e eMAG.

## Estrutura do repositório

```
cpat-digital/
├── docs/        # Documentação (briefing, requisitos, identidade visual)
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
