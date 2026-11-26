# SEO e Google Search

| Item | O que fazer |
| --- | --- |
| Título e descrição | `title` e `meta description` únicos por rota |
| `<head>` | `lang="pt-BR"`, `viewport`, `canonical` por página e `robots` (bloquear homologação) |
| Compartilhamento | Open Graph e Twitter Card com imagem 1200 × 630 px |
| JSON-LD | `GovernmentOrganization`, `JobPosting` por vaga, `BreadcrumbList`, `FAQPage` (a confirmar) |
| Renderização | Angular SSR ou pré-renderização das rotas públicas |
| Indexação | `sitemap.xml`, `robots.txt` e Google Search Console |
| Estrutura | Um `h1` por página, URLs curtas (`/vagas`, `/servicos`), texto alternativo e links descritivos |
| Desempenho | Core Web Vitals: rotas sob demanda, imagens otimizadas, `font-display: swap` |
| URLs antigas | Redirecionamentos 301 do site atual para o novo |

## Links quebrados

Links externos mortos, como https://empregabrasil.mte.gov.br/, são tratados com inventário, centralização em `external-links.ts`, confirmação da URL oficial com a SMTR e verificador de links no build.
