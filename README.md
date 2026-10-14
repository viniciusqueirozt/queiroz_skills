# Queiroz Skills

Skills reutilizáveis para o Codex. Cada skill tem suas próprias instruções e referências, sem depender dos arquivos de outro projeto.

## Disponível

| Skill | Versão | Objetivo |
|---|---|---|
| [stitch-telas](skills/stitch-telas/SKILL.md) | 1.0.0 | Preparar prompts, criar, refinar e revisar telas no Google Stitch com a identidade e os requisitos do projeto atual. |

## Como a stitch-telas funciona

1. **Entende o contexto:** lê os requisitos, a identidade visual e as referências disponíveis no projeto. Você informa a tela desejada e, para edição, o projeto/frame do Stitch.
2. **Prepara ou executa:** organiza um prompt; quando há acesso autorizado ao Stitch, gera ou refina a tela preservando as partes já aceitas. Também pode revisar exports que você fornecer.
3. **Revisa e entrega:** compara a saída real com o objetivo e as referências, verifica legibilidade, ações e consistência, e apresenta a imagem ou link com as correções e limitações encontradas.

Você pode usar a mesma skill em projetos diferentes: marca, cores, requisitos e tecnologia vêm do projeto atual. Ela não define regras de negócio nem muda a tecnologia do aplicativo por conta própria. A instalação fornece instruções ao agente; não cria acesso automático à sua conta do Stitch. Leia as [instruções completas](skills/stitch-telas/SKILL.md) antes de instalar, se quiser conhecer os critérios de revisão.

## Instalar pelo Codex

Envie este comando no Codex:

```text
Use $skill-installer para instalar a skill stitch-telas do repositório
viniciusqueirozt/queiroz_skills, no caminho skills/stitch-telas.
```

O instalador copia a skill para o ambiente local. Ela fica disponível no próximo turno; se não aparecer, reinicie o Codex. Se já existir uma instalação com esse nome, confira qual versão deseja manter antes de substituí-la.

## Instalação manual

1. No GitHub, use **Code > Download ZIP** e extraia o arquivo.
2. Dentro de `skills/`, copie a pasta inteira `stitch-telas` para `.agents/skills/` no projeto em que deseja usá-la.
3. Confira que o caminho final é `.agents/skills/stitch-telas/SKILL.md`. Não copie apenas o arquivo principal: mantenha `agents/` e `references/` juntos.
4. Abra o projeto no Codex. Se a skill não aparecer, reinicie o Codex.

Para disponibilizar manualmente em vários projetos, use a pasta pessoal `~/.agents/skills/stitch-telas/`, em vez de copiar para cada projeto. Escolha uma instalação para evitar duplicidades.

## Usar

```text
Use $stitch-telas para preparar a tela de [objetivo] deste projeto.
A plataforma é [Web/Mobile]. Estas são as referências e requisitos:
[contexto ou links]. Preserve a identidade visual e indique como revisar.
```

Para refinar uma tela existente, forneça o projeto/frame e diga o que preservar e o que corrigir. A skill se adapta aos documentos disponíveis, ao idioma e à tecnologia do projeto atual.

## Acesso ao Stitch

A skill não instala um conector nem autentica serviços. Para gerar ou editar telas, o ambiente precisa ter acesso autorizado ao Stitch por MCP ou navegador. Sem esse acesso, é possível preparar prompts e revisar exports fornecidos.

Este repositório distribui pastas de skills para uso local no Codex; não é um plugin publicado no diretório do ChatGPT. Uma imagem de interface não comprova funcionamento do aplicativo ou integração com o backend.

## Estrutura

```text
skills/
  stitch-telas/
    SKILL.md
    agents/openai.yaml
    references/briefing.md
    references/revisao.md
```

Novas skills podem ocupar novas pastas em `skills/`, cada uma com seu próprio `SKILL.md`.

## Documentação oficial

- [OpenAI — criar, descobrir e instalar skills](https://learn.chatgpt.com/docs/build-skills)
- [OpenAI — instalador de skills](https://github.com/openai/skills/tree/main/skills/.system/skill-installer)
