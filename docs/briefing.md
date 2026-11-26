# Briefing — Reestruturação do site CPAT Campinas

> Itens marcados como "a validar" dependem de confirmação com a SMTR/IMA.

## Contexto e problema

O site atual do CPAT Campinas (https://cpat.campinas.sp.gov.br/) é antigo, pouco funcional e não atende critérios de acessibilidade, o que dificulta o acesso do trabalhador aos serviços de emprego e renda da Prefeitura.

O CPAT (Centro Público de Apoio ao Trabalhador) integra a Secretaria Municipal de Trabalho e Renda (SMTR) e é a porta de entrada para vagas, encaminhamento e atendimento ao cidadão.

Problemas identificados:

- Interface desatualizada, sem padrão visual do governo e sem hierarquia clara de informação.
- Navegação e busca pouco funcionais; não há FAQ, SAC, Ouvidoria ou chat integrados.
- Acessibilidade insuficiente: sem ajuste de fonte, sem modo escuro, contraste e foco de teclado não tratados.
- Lista de vagas sem filtros úteis (ordenação, modelo de trabalho, tipo de vaga, vaga exclusiva para PCD).
- Experiência fraca em celular, onde está boa parte do público.
- Falta de prova social: não há depoimentos de candidatos atendidos.

## Objetivo e solução

Entregar um site do CPAT moderno, acessível e funcional, que ajude o cidadão a encontrar vagas, entender os serviços e falar com a Prefeitura sem sair da página.

Objetivos específicos:

- Seguir o Design System do Gov.br (GovDS) para dar identidade e confiança institucional.
- Cumprir boas práticas de acessibilidade (WCAG 2.1 AA e eMAG).
- Facilitar a busca de vagas com filtros combináveis.
- Abrir canais de atendimento: chat, FAQ, SAC e Ouvidoria.
- Funcionar bem em desktop e celular.

Solução proposta: cinco telas prototipadas em versões clara e escura, versão mobile e um Design System próprio.

- **Home:** barra de acessibilidade, carrossel dinâmico, cartões de serviços, vagas em destaque, notícias, depoimentos, FAQ e rodapé com unidades e redes sociais.
- **Vagas de emprego:** filtros de ordenação, modelo de trabalho, tipo de vaga, escolaridade, município e chave para vagas exclusivas para PCD.
- **Serviços, Institucional e Atendimento:** conteúdos reorganizados; SAC e Ouvidoria em formulário único.
- **Chatbot (JivoChat)**, botões A−/A+ e modo escuro em todas as páginas.
- **Design System:** guia de estilo e design atômico, com tokens claro/escuro.

## Público-alvo e personas

Público principal: trabalhadores de Campinas e região em busca de vaga, qualificação ou orientação. Público secundário: empresas que oferecem vagas e a equipe do CPAT. As personas abaixo são propostas para validação e ainda não vêm de pesquisa com usuários.

| Persona | Perfil | Necessidade principal | Cuidado de design |
| --- | --- | --- | --- |
| Candidato em primeiro emprego | Jovem, usa celular, pouca experiência | Achar vaga de aprendiz, estágio ou trainee | Filtros simples, linguagem clara |
| Trabalhador com baixa escolaridade digital | Adulto, uso básico da internet | Entender o que fazer e onde ir | Texto grande, poucos passos, ajuda por chat |
| Pessoa com deficiência (PCD) | Pode usar leitor de tela ou teclado | Ver vagas exclusivas para PCD | WCAG AA, foco visível, rótulos corretos |
| Pessoa 50+ | Menos familiaridade com tecnologia | Ler com conforto e achar atendimento | Botões A−/A+, contraste alto |
| Empresa que anuncia vagas | RH ou dono de negócio | Saber como cadastrar vagas e falar com o CPAT | Caminho direto para SAC e contato |

## Levantamento de requisitos

**Requisitos funcionais**

| Cód. | Requisito | Prioridade |
| --- | --- | --- |
| RF01 | Pesquisa global no site | Alta |
| RF02 | Lista de vagas com ordenação (mais/menos recentes) | Alta |
| RF03 | Filtro por modelo de trabalho (presencial, híbrido, remoto) | Alta |
| RF04 | Filtro por tipo de vaga (aprendiz, estágio, trainee, temporário, efetivo, pessoa jurídica, terceiro, intermitente, freelance) com seleção múltipla | Alta |
| RF05 | Alternador para vagas exclusivas para PCD | Alta |
| RF06 | Filtros por título, escolaridade e município, com opção de limpar | Média |
| RF07 | Chatbot JivoChat disponível em todas as páginas | Alta |
| RF08 | FAQ com perguntas frequentes | Alta |
| RF09 | SAC, Ouvidoria e Fale conosco em formulário com protocolo e opção anônima | Alta |
| RF10 | Depoimentos de candidatos (a validar autorização de uso) | Média |
| RF11 | Carrossel de destaques dinâmico, com pausa | Média |
| RF12 | Cartões de serviços e notícias com filtro por categoria | Média |
| RF13 | Botão de modo escuro | Alta |
| RF14 | Botões A− e A+ para tamanho da fonte | Alta |
| RF15 | Links para redes sociais | Baixa |
| RF16 | Páginas Institucional, Serviços e Unidades | Alta |
| RF17 | Inventário e verificação de links quebrados | Alta |
| RF18 | VLibras em todas as páginas | Alta |
| RF19 | Ficha de transparência em cada vaga | Alta |

**Requisitos não funcionais**

| Cód. | Requisito | Critério |
| --- | --- | --- |
| RNF01 | Acessibilidade | WCAG 2.1 AA e eMAG; navegação por teclado; foco visível; contraste mínimo de 4,5:1 no texto e 3:1 nos componentes |
| RNF02 | Alvos de toque | Mínimo de 44 px |
| RNF03 | Responsividade | Desktop e mobile; no mobile as vagas aparecem só em cards |
| RNF04 | Desempenho | Carregamento rápido em rede móvel (meta a definir) |
| RNF05 | Privacidade | Conformidade com a LGPD; consentimento nos formulários |
| RNF06 | Consistência visual | Componentes reutilizáveis do Design System |
| RNF07 | Compatibilidade | Navegadores atuais; leitores de tela (a validar quais) |
| RNF08 | Manutenibilidade | Código em componentes Angular; tokens de tema em variáveis CSS |
| RNF09 | SEO | SSR ou pré-renderização, meta tags por rota, sitemap e robots |

Acessibilidade já aplicada no protótipo: link "ir para o conteúdo", anel de foco amarelo, carrossel com pausa e região `aria-live`, chave PCD com `role="switch"`, rótulos em todos os campos e bordas de campo com contraste de 4,5:1 ou mais.

## Design

O design parte do Gov.br Design System e define um Design System próprio do CPAT por cima dele, com tokens para os temas claro e escuro.

**Identidade e tokens (protótipo do redesign)**

| Token | Claro | Escuro | Uso |
| --- | --- | --- | --- |
| Primária | #1351B4 | #2D6BD1 (botões), #9DBFF7 (texto) | Ações, títulos, links |
| Azul profundo | #071D41 | #060C18 | Rodapé e hero |
| Destaque | #FFCD07 | #FFCD07 | Foco, selo PCD, atenção |
| Fundo | #F8F8F8 | #0B1424 | Página |
| Superfície | #FFFFFF | #14223A | Cards e painéis |
| Borda de campo | #767676 | #8397B8 | Inputs e checkboxes |

A família tipográfica do Gov.br é a Rawline; o protótipo usa Raleway como substituta. A escala de texto aceita ajuste de −2 a +4 passos pelos botões A−/A+.

**Princípios aplicados**

- Hierarquia visual: título, dados e ação em níveis distintos.
- Alinhamento e grid: contêiner de 1120 px, margens de 32 px, colunas fluidas.
- Consistência: mesmos botões em pílula, mesmos raios, mesmas cores de estado.
- Espaço em branco: 28 px entre cards de vaga, 48 px entre filtros e resultados.
- Gestalt: proximidade, similaridade, região comum, figura e fundo, continuidade, fechamento e prägnanz nos cards de vagas e no menu.
- Design atômico: átomos (botão, campo, selo, ícone), moléculas (campo com rótulo, card de serviço), organismos (cabeçalho, filtros, lista de vagas, rodapé), templates e páginas.

Telas do protótipo: Home (clara e escura), Vagas de emprego, Atendimento (SAC e Ouvidoria), Institucional, Serviços, Design System e versão Mobile (clara e escura). Os arquivos ficam em `mockups/redesign-govbr/`.

## Stack técnica

A primeira versão (v1) é só front-end: Angular com Tailwind CSS, seguindo o GovDS e o Design System do CPAT. Back-end, banco e hospedagem ficam para a v2.

| Camada | Escolha | Observação |
| --- | --- | --- |
| Front-end | Angular (componentes standalone, rotas, formulários reativos) | Cada tela do protótipo vira uma rota |
| Design System base | Gov.br Design System (GovDS) | Tokens, componentes e padrões oficiais |
| Design System CPAT | Biblioteca interna de componentes Angular | Tokens claro/escuro em variáveis CSS ligadas ao tema do Tailwind; átomos, moléculas e organismos |
| Estilo | Tailwind CSS | Tema com tokens do GovDS e do CPAT; modo escuro por classe; A−/A+ altera a fonte raiz |
| Chat | JivoChat (script do widget) | Exige o ID da conta do CPAT |
| Dados de vagas | JSON de exemplo atrás de um serviço Angular | Troca por API na v2; fonte a validar (Emprega Brasil, base do CPAT ou outra) |
| Back-end e banco | Fora da v1 | Hipótese: Ruby on Rails e PostgreSQL |
| Acessibilidade | axe e Lighthouse, mais teste manual com teclado e leitor de tela | Rodar em cada entrega |
| Qualidade | Testes unitários e e2e; Storybook ou página de componentes | Mantidos junto do Design System |
| Hospedagem e CI/CD | Build do Angular (SSR ou pré-renderização); servidor a definir com o IMA | Ambiente de homologação antes da produção |

O protótipo atual é apenas visual: filtros, carrossel, chat e formulários são simulados, e os dados de vagas, depoimentos e FAQ são de exemplo.

## Escopo da primeira versão

**Dentro da v1**

- Telas Home, Vagas de emprego, Serviços, Institucional e Atendimento, em desktop e mobile.
- Modo escuro, botões A−/A+, busca, carrossel, FAQ, depoimentos e redes sociais.
- Filtros de vagas funcionando sobre dados de exemplo; no mobile, só cards.
- Chat JivoChat carregado por script.
- Formulários de SAC e Ouvidoria com validação, sem envio real; o protocolo é simulado.
- SEO por rota e tratamento de links quebrados.
- Página 404 personalizada.

**Fora da v1 (v2)**

- Back-end, banco de dados e API de vagas.
- Envio real de SAC e Ouvidoria e integração real com o Emprega Brasil.
- Painel administrativo ou CMS.

**Como o front fica pronto para a v2:** os dados passam por serviços Angular com interfaces definidas; trocar o JSON de exemplo por uma API não exige refazer as telas.

**Como o Tailwind segue o design system:** o `tailwind.config` recebe os tokens do GovDS e do CPAT (cores, tipografia, espaçamento, raios) ligados a variáveis CSS, com `darkMode` por classe. Os componentes do GovDS são recriados como componentes Angular com utilitários do Tailwind, em vez de misturar o CSS do GovDS com o do Tailwind; esta escolha está a confirmar.

## Transparência das vagas

Cada vaga terá uma ficha com campos obrigatórios e opcionais, para o candidato saber o que esperar antes de se candidatar (RF19). Campo opcional sem preenchimento aparece como "Não informado".

| Campo | Preenchimento | Observação |
| --- | --- | --- |
| Razão social e nome fantasia da empresa | Opcional | A empresa pode optar por não divulgar |
| CNPJ de quem fará a contratação | Opcional | Exibido com máscara 00.000.000/0000-00 |
| Descrição das atividades do cargo | Obrigatório | Texto livre, com lista de atividades |
| Escolaridade e experiência exigidas | Obrigatório | Escolaridade como lista fixa; experiência em meses ou anos |
| Horário de trabalho | Opcional | Dias e faixa de horário |
| Local de trabalho e endereço | Opcional | Município e bairro continuam visíveis na lista |
| Informações sobre a entrevista | Obrigatório | Como, onde e quando será feita (presencial, on-line ou encaminhamento pelo CPAT) |

No protótipo, os detalhes da vaga abrem em um modal com todas as informações do card, a transparência, benefícios (opcional) e etapas do processo seletivo (opcional, oculto quando a empresa não informa), além de favoritar, copiar link e período de inscrição (data final opcional). Na v2, os campos obrigatórios devem ser validados no cadastro da vaga, e a SEO usa os mesmos campos no `JobPosting`.

## VLibras

O site terá o VLibras, tradutor de português para Libras do governo federal, em todas as páginas, para incluir pessoas surdas (RF18).

- **Como integrar:** carregar o script oficial `vlibras-plugin.js` apenas no navegador (não no render do servidor) e iniciar `new window.VLibras.Widget('https://vlibras.gov.br/app')`, com o bloco de marcação padrão do widget no `app.component`.
- **Posição:** o botão fica na lateral direita; o chat JivoChat fica no canto inferior, sem sobrepor o botão. No mobile, o botão deve ficar acima da navegação inferior.
- **Limite:** o VLibras ajuda na leitura do texto, mas não substitui as demais regras de acessibilidade, como contraste, teclado e leitor de tela.
- **Protótipo:** o canvas mostra apenas um botão simulado; o widget real só carrega no projeto Angular.

## SEO e Google Search

Para a v1 ser encontrada no Google e gerar boas prévias ao ser compartilhada, cada rota terá meta tags próprias e as páginas públicas serão renderizadas no servidor ou pré-renderizadas, já que uma SPA pura dificulta a indexação (RNF09).

| Item | O que fazer |
| --- | --- |
| Título e descrição | `title` e `meta description` únicos por rota, definidos nos dados da rota e aplicados com os serviços Title e Meta do Angular |
| Básico do `<head>` | `lang="pt-BR"`, `viewport`, `canonical` por página e `robots` (indexar páginas públicas; bloquear homologação) |
| Compartilhamento | Open Graph e Twitter Card com imagem 1200 × 630 px, título e descrição por página |
| Dados estruturados (JSON-LD) | `GovernmentOrganization` para o CPAT e a SMTR, com endereço e telefone das unidades; `JobPosting` em cada vaga, para o Google Vagas; `BreadcrumbList` nas páginas internas; `FAQPage` no FAQ, a confirmar nas regras atuais do Google |
| Renderização | Angular SSR ou pré-renderização das rotas públicas (Home, Serviços, Institucional, Vagas, Atendimento) |
| Indexação | `sitemap.xml` e `robots.txt`; site cadastrado no Google Search Console |
| Estrutura da página | Um `h1` por página, títulos em ordem, URLs curtas (`/vagas`, `/servicos`), texto alternativo nas imagens e links com texto descritivo |
| Desempenho | Core Web Vitals: rotas com carregamento sob demanda, imagens otimizadas e `font-display: swap` |
| URLs antigas | Redirecionamentos 301 das páginas do site atual para as novas, para não perder posicionamento |

A v1 pode também propor à SMTR o cadastro das unidades no Perfil da Empresa no Google (a validar).

## Links quebrados

Links externos mortos, como https://empregabrasil.mte.gov.br/, levam o cidadão a um erro e prejudicam a confiança e o SEO; a v1 trata isso com inventário, centralização e verificação automática (RF17).

1. **Inventariar:** listar todos os links do site atual (menu, páginas, rodapé e textos) e testar o status de cada um.
2. **Centralizar:** manter um arquivo único de links externos (por exemplo `external-links.ts`) com URL, rótulo, data da última verificação e alternativa; nenhum link escrito direto no template.
3. **Corrigir o Emprega Brasil:** confirmar com a SMTR a URL oficial vigente antes de publicar. Enquanto não houver, o botão mostra o atendimento por chat ou a página de Atendimento, em vez de levar a um erro.
4. **Verificar sempre:** rodar um verificador de links (por exemplo lychee ou linkinator) a cada build e em agenda semanal, falhando o build quando um link interno quebrar e avisando quando um externo cair.
5. **Proteger o usuário:** links externos com `rel="noopener noreferrer"` e aviso de "abre em nova aba" para leitores de tela; página 404 personalizada com busca e atalhos.

## Riscos, pontos a validar e próximos passos

Três pontos podem mudar o escopo: a fonte dos dados de vagas, o uso real do JivoChat e a autorização para depoimentos.

**A validar**

- Origem e formato dos dados de vagas, incluindo modelo de trabalho, tipo, data e vaga exclusiva para PCD, que hoje são de exemplo.
- Textos de serviços, FAQ e depoimentos, que são rascunhos e precisam de revisão da SMTR.
- Conta e ID do JivoChat, e links reais das redes sociais.
- Datas do histórico institucional: a fonte original mostra datas fora de ordem.
- Cobertura da borda de campo acessível nas telas Serviços, Atendimento e Institucional.
- Back-end, hospedagem e prazos com o IMA.

**Próximos passos**

1. Validar o briefing e as personas com a equipe do CPAT.
2. Revisar conteúdos e dados de exemplo com a SMTR.
3. Testar o protótipo com usuários reais, incluindo pessoas com deficiência.
4. Criar o projeto Angular com Tailwind CSS e a biblioteca do Design System do CPAT.
5. Implementar tela por tela, começando por Home e Vagas, com auditoria de acessibilidade a cada entrega.
