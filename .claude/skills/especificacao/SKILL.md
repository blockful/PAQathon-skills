---
name: especificacao
description: Escreve a especificação de uma página em markdown a partir das decisões já fechadas, sem inventar nada. Use depois da entrevista, ou quando o usuário pedir "escreve a spec", "fecha a especificação", "consolida o que decidimos".
---

# 2 · Especificação fechada

## Entrada

```
DECISÕES JÁ FECHADAS (saída da entrevista, PRD, fluxo, features):
[COLE AQUI]
```

Se o bloco acima vier vazio, peça as decisões antes de escrever. Use só o que estiver colado aqui.

## Tarefa

Sem perguntas novas — é síntese. Escreva a especificação em markdown, no máximo uma página. Se não cabe em uma página, ainda tem decisão em aberto.

Seções, nesta ordem:
1. O que é, e para quem
2. O que vai existir — em linguagem de quem usa, não de quem constrói
3. O que é simulado e o que funciona de verdade — o corte esperto para esta versão
4. Como saberemos que ficou certo — uma lista de coisas que dá pra verificar olhando a tela pronta
5. O que está FORA do escopo
6. Decisões que já tomamos, e por quê

Não invente nada que não esteja na entrada. Se faltar alguma coisa, coloque numa seção final "ainda em aberto" em vez de chutar.

## Saída

A especificação em markdown, pronta pra colar em `quebrar-tarefas`.
