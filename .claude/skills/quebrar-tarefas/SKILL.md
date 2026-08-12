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
- sair como um prompt fechado: quem lê só ele já implementa, sem ter a spec em mãos

## Formato de cada tarefa

````
### Tarefa N — [título]

```
[PROMPT PRONTO PRA COLAR — escrito direto pra IA, contendo:]

Contexto: o que é o produto, quem usa, e o que já existe no app neste
ponto (resultado das tarefas anteriores).

Construa: o comportamento exato desta tarefa — telas, campos, estados
(vazio, carregando, erro), validações e regras de negócio que a spec
define pra esta parte.

Dados: de onde vem cada dado de verdade — tabela/coleção e campos, ou
a API/integração. Nada de mock, dado fixo no código, lista de exemplo
ou placeholder: se o dado ainda não existe, crie a estrutura real e
deixe a tela vazia.

Não faça: as partes da spec que ficam pras próximas tarefas.

Se algo estiver ambíguo, pergunte antes de decidir sozinho.
```

**Depende de:** tarefa X (ou nada)
**Como testo:** o que abrir na tela e o que tem que aparecer
````

Coloque na ordem em que devem ser pedidas. No final, diga quais tarefas não dependem de nada e poderiam ser feitas a qualquer momento.

Se a spec não disser de onde vem algum dado, não invente: liste no final as lacunas que o usuário precisa fechar antes de pedir aquela tarefa.

## Saída

A lista ordenada de tarefas, cada uma com seu prompt pronto pra colar.
