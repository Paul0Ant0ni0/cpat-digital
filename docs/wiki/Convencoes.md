# Convenções

## Issues

- Título com o tipo entre colchetes: `[Front-End]`, `[Back-End]`, `[DB]`, `[Design]`, `[DevOps]`, `[QA]`, `[Docs]`, `[Pesquisa]`.
- Primeira linha do corpo: `Prioridade: Alta | Média | Baixa · Estimativa: Xh`.
- Labels de prioridade (`prioridade: alta`, `média`, `baixa`), de versão (`v1`, `v2`) e de área.
- Critérios de aceite em lista de tarefas.

## Commits

Mensagens curtas, no imperativo, em português. Para fechar uma issue: `Closes #número`.

## Branches e pull requests

Branches a partir da `main`, uma por issue (por exemplo `feat/12-links-quebrados`). Pull request referenciando a issue e passando por lint, build e testes.

## Código

- Componentes Angular standalone.
- Estilos com Tailwind e tokens do tema; nada de cores escritas direto.
- Textos da interface em português do Brasil.
- Acessibilidade em todo componente: rótulos, foco visível e contraste.
