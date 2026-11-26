# Guia de desenvolvimento

## Requisitos

- Node.js 22 ou superior e npm 10 ou superior
- Docker (para a stack completa, quando configurada)

## Rodar o front-end

```bash
git clone https://github.com/Paul0Ant0ni0/cpat-digital.git
cd cpat-digital/frontend
npm install
npm start          # http://localhost:4200
```

## Scripts

| Comando | O que faz |
| --- | --- |
| `npm start` | Servidor de desenvolvimento |
| `npm run build` | Build de produção, com SSR e pré-renderização |
| `npm test` | Testes unitários (Vitest) |
| `npm run lint` | ESLint |

## Estrutura do repositório

```
cpat-digital/
├── docs/        # Documentação e imagens
├── design/      # Identidade visual (Brand Book)
├── assets/      # Logos, ícones e ilustrações
├── flyers/      # Flyers e materiais gráficos
├── banners/     # Banners institucionais
├── mockups/     # Protótipos
├── frontend/    # Interface do usuário
├── backend/     # API e regras de negócio
└── README.md
```

## Docker

Em configuração (ver as issues de DevOps e JSON Server).
