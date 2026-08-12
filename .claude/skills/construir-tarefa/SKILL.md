---
name: construir-tarefa
description: Monta o texto para colar no Lovable — a primeira mensagem com especificação + identidade visual + tarefa 1, e as seguintes com uma tarefa por vez. Use quando o usuário disser "prompt pro Lovable", "vou construir a tarefa X", "primeira mensagem no Lovable".
---

# 4 · Uma tarefa por prompt

A primeira mensagem carrega o contexto inteiro. As seguintes são curtas — uma tarefa cada.

## Entrada

```
ESPECIFICAÇÃO:
[COLE AQUI]

IDENTIDADE VISUAL / DESIGN.md:
[COLE AQUI]

TAREFA A CONSTRUIR AGORA:
[COLE AQUI]

É a primeira mensagem no Lovable? [sim/não]
```

Peça o que faltar antes de montar. Use só o que estiver colado aqui.

## Tarefa

**Se é a primeira mensagem**, monte assim:

```
Vou te passar a especificação completa do projeto e a identidade
visual. Leia tudo antes de construir.

[ESPECIFICAÇÃO]
[IDENTIDADE VISUAL]

Nesta primeira etapa, construa APENAS isto:

[TAREFA]

Não implemente as outras partes ainda. Se algo estiver ambíguo para
esta tarefa, me pergunte antes de decidir sozinho.
```

**Se não é a primeira**, a mensagem é só: `Agora a tarefa N: [TAREFA]`.

## Regras
- Antes de passar pra próxima, abra a tela e confira o item "como testo" da tarefa atual.
- Não acumule — duas tarefas quebradas ao mesmo tempo custam o triplo pra achar.
- Pedido pequeno vence pedido grande. Nunca "refaz tudo": aponte tela + elemento + comportamento.
- Travou duas vezes no mesmo erro? Volte um passo e melhore a especificação (`quando-quebra`).
