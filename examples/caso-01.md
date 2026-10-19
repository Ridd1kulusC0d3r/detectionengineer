# Caso 01 — Uma regra correta no campo errado

**Tipo:** exercício de mesa, dados e cenário sintéticos. Não exige instalação nem contato com serviços reais.

## Situação

A lógica seleciona action=role_assignment e approval=missing. E1 corresponde ao sinal; E2 tem approval=approved e é controle negativo; E3 não contém approval. Interpretar campo ausente como missing cria um falso sinal de negócio.

## Sua missão

1. Especifique quais campos são obrigatórios e quais valores são válidos.
2. Separe violação de política de falha no pipeline de dados.
3. Descreva testes positivo, negativo e de campo ausente.
4. Registre backend, versão de conversor e validação ainda pendente antes de produção.

## Entrega

Preencha a [ficha](../templates/ficha.md), citando o trecho ou identificador que sustenta cada conclusão. Se faltar uma informação, registre a lacuna em vez de inventar um resultado.

<details>
<summary>Comentário e critério de aceite</summary>

A regra só seleciona o evento positivo; o campo ausente gera problema de qualidade de dados, e não acusação automática.

A avaliação é qualitativa e exige revisão humana. Este exercício não mede eficácia em um ambiente real.

</details>

[Guia](../docs/COMECE-AQUI.md) · [Início](../README.md)
