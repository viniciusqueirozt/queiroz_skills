# Revisão visual e de comportamento

Verifique identidade contra a fonte do projeto e composição contra a referência escolhida. Uma referência agradável pode ter falhas de acessibilidade ou layout que não devem ser reproduzidas.

| Dimensão | O que verificar |
|---|---|
| Requisitos | Conteúdo, ações, estados e destinos correspondem ao pedido e às decisões |
| Identidade | Marca, tipografia, cores, ícones e componentes seguem o projeto |
| Hierarquia | Objetivo e ação principais claros; agrupamento e leitura coerentes |
| Layout | Conteúdo e ações alcançáveis; sem corte, sobreposição ou largura fixa indevida |
| Estados | Variante coerente com base; feedback e recuperação adequados ao contexto |
| Acessibilidade | Contraste, labels, nomes de ações, foco, teclado e toque quando aplicáveis |
| Plataforma | Densidade e navegação apropriadas; safe areas/teclado/rolagem para mobile |
| Rastreabilidade | Frame, versão, link e referência identificados para continuar trabalho |

Use “atende”, “falha”, “não se aplica” ou “não verificado”. Não esconda falha de requisito numa nota estética geral.

## Sinais de exportação que merecem inspeção

- Tokens do HTML/tema diferentes dos normativos.
- Ação visível no PNG, mas oculta, desabilitada ou coberta no preview.
- Fonte de ícones distinta da biblioteca escolhida.
- Rótulos acessíveis em outro idioma.
- Zoom bloqueado, foco removido ou alvos pequenos numa interface Web.
- Conteúdo longo, mensagem de erro ou teclado que tornam ação inacessível.
- Uma base refeita ao gerar seu estado, causando inconsistência entre variantes.

Esses sinais não são todos defeitos em qualquer contexto: um botão desabilitado pode ser correto em carregamento; uma dimensão PNG pode representar escala de exportação. Confirme o estado e a evidência antes de corrigir.

Priorize falhas de requisito e acesso à ação, depois legibilidade/layout, depois consistência e acabamento. Compare as partes relevantes à tarefa sem forçar um checklist desproporcional.

## Nota de revisão

```text
Tela/frame e versão:
Referência/sistema visual usados:
Resultado observável:
Checagens e viewports realmente executados:
Critérios atendidos e falhas:
Itens não verificados:
Próximo refinamento ou decisão necessária:
```

Inspeção estática não prova autenticação, autorização, pagamentos, offline, persistência ou sucesso de backend. Preserve essa distinção quando apresentar um protótipo com interações simuladas.
