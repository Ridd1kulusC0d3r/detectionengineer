# Resolução do Caso 01 — Uma regra correta no campo errado

> Este é um exemplo resolvido baseado no Caso 01.

## Nome / versão / responsável

- **Nome:** Detecção de atribuição de papel sem aprovação
- **Versão:** 1.0.0
- **Responsável:** Equipe de Engenharia de Detecção

## Comportamento e hipótese

- **Comportamento:** A regra busca identificar atribuições de funções (`role_assignment`) onde a aprovação está explicitamente registrada como ausente (`missing`).
- **Hipótese:** Contorno de políticas de acesso ao realizar atribuições de papéis sem aprovação explícita.

## Fonte e contrato de campos

- Campos obrigatórios:
  - `event_id`: Identificador único
  - `action`: Deve ser igual a `role_assignment`
  - `approval`: O status da aprovação, devendo conter um valor explícito (`approved` ou `missing`)
- A ausência do campo `approval` deve ser tratada como problema de qualidade de dados, não como ausência de aprovação (`missing`).

## Lógica e janela

- **Lógica:** `action == "role_assignment" AND approval == "missing"`
- **Janela:** Análise em fluxo contínuo ou lotes de curta duração.

## Casos positivos e negativos

- **Teste Positivo (E1):** `action=role_assignment` e `approval=missing`. (Gera sinal para triagem).
- **Teste Negativo (E2):** `action=role_assignment` e `approval=approved`. (Não seleciona).
- **Teste de Campo Ausente (E3):** `action=role_assignment` e campo `approval` inexistente. (Não seleciona; deve sinalizar problema no pipeline).

## Falsos positivos e exceções

- Interpretar ausência de campo como `missing` gera falso sinal de negócio.

## Validação por backend

- **Backend:** SIEM genérico.
- **Versão de conversor:** Não aplicável (exercício de mesa).
- **Status:** Validação pendente antes de produção.

## Rollback / revisão / retirada

- **Revisão:** Tratar erros de parsing caso o campo `approval` comece a ser omitido sistematicamente.
- **Rollback:** Desabilitar ou colocar a regra em modo de observação caso gere alertas em massa por problemas de qualidade de dados.

## Revisão

- [x] Cada conclusão aponta para uma evidência identificável.
- [x] Explicações alternativas e lacunas estão explícitas.
- [x] O critério de aceite foi revisado: A regra só seleciona o evento positivo; o campo ausente gera problema de qualidade de dados, e não acusação automática.
