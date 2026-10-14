# Contexto mínimo para uma tela

Encontre as respostas nos arquivos ou no pedido antes de perguntar. Não transforme esta lista em formulário obrigatório.

| Informação | Uso |
|---|---|
| Projeto e tela/frame | Garantir que a alteração ocorre no destino escolhido |
| Objetivo e usuário | Escolher conteúdo, hierarquia e ação dominante |
| Plataforma/dispositivo | Definir navegação, densidade, layout e checagens |
| Conteúdo e ações | Diferenciar requisito, exemplo e pendência |
| Estado | Base, carregamento, erro, vazio, offline ou outro estado pertinente |
| Sistema visual | Reutilizar identidade, tokens, componentes e ativos existentes |
| Referência visual | Entender o que preservar e o que melhorar |
| Escopo autorizado | Prompt, geração, refinamento, revisão ou lote |

Se o usuário fornecer apenas uma ideia, prepare um conceito com hipóteses explicitadas. Se houver projeto existente, prefira seus padrões e confirme o frame quando ambíguo. Ausência de DESIGN.md não impede preparar um prompt ou propor identidade para uma exploração pedida.

## Prompt de geração

```text
Tela: [nome/código e estado].
Plataforma: [a plataforma deste projeto].
Objetivo: [resultado para o usuário].
Contexto de acesso: [papel/contexto, quando existir].
Sistema visual: [o sistema aprovado e aplicado, ou a proposta desta tarefa].
Estrutura: [grupos de conteúdo em ordem de leitura].
Conteúdo e ações: [requisitos verificáveis].
Referência: [composição/elementos que interessam ao pedido].
Limites: [lacunas de produto que não devem ser inventadas].
```

Preencha de forma concreta e enxuta, removendo itens não aplicáveis. Esses campos orientam o raciocínio, não um schema de API. Não enviar marcadores vazios como requisitos ao Stitch.

## Prompt de refinamento

```text
Refine somente [frame confirmado] — [nome e estado].
Preserve [partes aceitas: conteúdo, identidade, hierarquia ou componente].
Corrija [problema observado] para que [resultado verificável].
Use o sistema visual vigente deste projeto.
Mantenha o escopo de [tela/estado], sem adicionar funcionalidades.
```

Para um lote, liste telas e dependências reais e revise uma unidade antes de multiplicar o padrão. Quando faltar uma decisão que bloqueia parte do lote, trabalhe nas telas independentes dentro do pedido.
