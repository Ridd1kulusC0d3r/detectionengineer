# Validar antes de operar

## Contrato do exemplo

| Campo | Obrigatório | Valores do exercício |
|---|---|---|
| event_id | Sim | Identificador único |
| action | Sim | role_assignment |
| approval | Sim | approved ou missing |

`missing` é um valor de negócio explícito; campo ausente é erro de qualidade de dados. Em produção, sua origem e integridade precisam ser verificadas.

## Matriz de casos

| Caso | Entrada | Resultado esperado |
|---|---|---|
| Positivo | action=role_assignment, approval=missing | Candidato à triagem |
| Negativo | action=role_assignment, approval=approved | Não selecionar |
| Qualidade | action=role_assignment, approval ausente | Sinalizar qualidade dos dados |
| Fora de escopo | action=login, approval=missing | Não selecionar |

## Da especificação à operação

1. Identifique a fonte e o schema reais.
2. Escreva a consulta para o backend escolhido.
3. Reproduza os quatro casos e registre o resultado efetivo.
4. Avalie janela, duplicação, atraso, custo e falsos positivos.
5. Revise o procedimento de triagem com o SOC.
6. Defina versão, aprovador, rollback e próxima revisão.

Este documento é uma especificação de teste. Não declara uma regra Sigma ou consulta SIEM implantada ou validada.
