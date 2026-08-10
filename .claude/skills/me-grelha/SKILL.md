---
name: me-grelha
description: Transforma uma ideia vaga em uma especificação clara por meio de rodadas de perguntas estruturadas, terminando em uma spec consolidada e autossuficiente. Use quando o usuário disser "me grelha", "grill me", pedir para ser entrevistado/questionado sobre um plano, quiser testar/estressar uma ideia, ou trouxer uma ideia mal definida que precisa virar spec antes de implementar.
---

# Grill Me

## O que faz

Transforma uma **ideia vaga em uma especificação clara** através de perguntas estruturadas.

O fluxo é simples:

**Ideia → Perguntas → Decisões → Spec**

Você não precisa começar com um plano. A skill explora o problema, elimina ambiguidades e, ao final, consolida tudo em uma única spec.

## Como funciona

As perguntas acontecem em **rodadas**.

Cada rodada aborda apenas questões que já podem ser respondidas com base no que foi definido anteriormente.

Explore, quando relevante:

* objetivo;
* contexto;
* usuários;
* comportamento esperado;
* requisitos;
* restrições;
* casos extremos;
* decisões técnicas;
* critérios de sucesso;
* fora de escopo.

Não pergunte algo que dependa de uma decisão ainda não tomada.

## Papel do usuário

O usuário controla as decisões.

Ele pode discordar, corrigir premissas, limitar o escopo, mudar decisões ou responder "não sei".

Não invente respostas para preencher lacunas.

Se algo importante estiver indefinido, pergunte.

Se algo só puder ser decidido experimentando ou testando, registre como questão aberta.

## Quando terminar

Encerre quando houver informação suficiente para alguém entender **o que precisa ser feito, como deve funcionar e quais limites devem ser respeitados**.

Evite perguntas que não alterariam materialmente a especificação.

Se o escopo estiver grande demais, ajude a reduzi-lo antes de continuar.

## Entregável

Ao terminar a entrevista, gere uma única **spec** consolidando as decisões da conversa.

A spec deve registrar apenas decisões realmente tomadas. Não introduza novos requisitos durante a síntese.

Use uma estrutura simples:

```md
# [Nome]

## Objetivo
O que será feito e por quê.

## Escopo
O que está incluído.

## Requisitos
Como deve funcionar.

## Decisões
Principais decisões tomadas durante a entrevista.

## Casos importantes
Comportamentos, exceções e casos extremos relevantes.

## Fora de escopo
O que explicitamente não será feito.

## Critérios de sucesso
Como saberemos que está funcionando corretamente.

## Questões abertas
O que ainda precisa ser decidido, se houver.
```

A spec deve ser **autossuficiente**: alguém que não participou da entrevista deve conseguir entendê-la sem precisar consultar a conversa.

O objetivo final não é fazer muitas perguntas. É transformar uma ideia pouco definida em **decisões conscientes e uma especificação pronta para execução**.

