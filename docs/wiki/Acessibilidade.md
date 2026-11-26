# Acessibilidade

Meta: **WCAG 2.1 AA** e **eMAG**.

## Já aplicado no protótipo

- Link "ir para o conteúdo".
- Anel de foco amarelo (#FFCD07).
- Carrossel com pausa e região `aria-live`.
- Chave PCD com `role="switch"`.
- Rótulos em todos os campos e bordas de campo com contraste de 4,5:1 ou mais.
- Botões A−/A/A+ e modo escuro.

## VLibras

Carregar o script oficial `vlibras-plugin.js` apenas no navegador (não no render do servidor) e iniciar `new window.VLibras.Widget('https://vlibras.gov.br/app')`. O botão fica na lateral direita, sem sobrepor o chat. O VLibras não substitui contraste, teclado e leitor de tela.

## Como verificar

1. axe e Lighthouse a cada entrega.
2. Teste manual com teclado.
3. Teste com leitor de tela (a definir quais).
4. Testes com pessoas com deficiência (ver [Roadmap](Roadmap)).
