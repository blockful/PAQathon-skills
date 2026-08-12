---
name: quebrar-tarefas
description: Quebra uma especificação em tarefas pequenas e ordenadas, cada uma cabendo num único pedido ao Lovable. Use quando o usuário disser "quebra em tarefas", "fatiar a spec", "por onde começo", ou já tiver a especificação fechada e quiser a lista de pedidos.
---

# 3 · Quebra em tarefas

O Lovable erra menos quando recebe um pedaço por vez.

## Entrada

```
ESPECIFICAÇÃO:
[COLE AQUI]
```

## Tarefa

Quebre a especificação em tarefas para o usuário pedir ao Lovable, uma por vez.

Cada tarefa precisa:
- entregar algo que já dá pra usar sozinho, mesmo que pequeno
- caber num pedido só
- vir com: título, o que entrega, como testar na tela se funcionou, e de qual tarefa anterior ela depende

Coloque na ordem em que devem ser pedidas. No final, diga quais tarefas não dependem de nada e poderiam ser feitas a qualquer momento.

## Saída

A lista ordenada de tarefas, cada uma pronta pra colar em `construir-tarefa`.
