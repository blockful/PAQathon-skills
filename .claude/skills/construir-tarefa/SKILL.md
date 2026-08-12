---
name: construir-tarefa
description: Monta o texto para colar no Lovable — a primeira mensagem com especificação + identidade visual + tarefa 1, e as seguintes com uma tarefa por vez. Use quando o usuário disser "prompt pro Lovable", "vou construir a tarefa X", "primeira mensagem no Lovable".
---

# 4 · Uma tarefa por prompt

A primeira mensagem carrega o contexto inteiro. As seguintes são curtas — uma tarefa cada.

Monte o texto para o usuário colar no Lovable:

```
Vou te passar a especificação completa do projeto e a identidade
visual. Leia tudo antes de construir.

[ESPECIFICAÇÃO]
[DESIGN.md OU IDENTIDADE VISUAL]

Nesta primeira etapa, construa APENAS isto:

[TAREFA 1]

Não implemente as outras partes ainda. Se algo estiver ambíguo para
esta tarefa, me pergunte antes de decidir sozinho.
```

Se faltar a especificação, a identidade visual ou a tarefa, peça antes de montar.

Da tarefa 2 em diante a mensagem é só: `Agora a tarefa 2: [tarefa]`.

Regras:
- Antes de passar pra próxima, abra a tela e confira o item "como testo" da tarefa atual.
- Não acumule — duas tarefas quebradas ao mesmo tempo custam o triplo pra achar.
- Pedido pequeno vence pedido grande. Nunca "refaz tudo": aponte tela + elemento + comportamento.
- Travou duas vezes no mesmo erro? Volte um passo e melhore a especificação (`quando-quebra`).

Antes: `quebrar-tarefas`.
