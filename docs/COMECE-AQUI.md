# Comece aqui — Detection Engineer

## Para quem

Pessoas que precisam projetar o ciclo de vida de detecções: requisito de telemetria, lógica analítica, testes positivos e negativos, tuning, revisão e retirada.

## Rota guiada

### 1. Especificar

**Atividade:** Definir comportamento e contrato de dados.

**Saída:** Especificação analítica.

### 2. Validar

**Atividade:** Comparar sinais e controles negativos.

**Saída:** Matriz de testes.

### 3. Operar

**Atividade:** Definir tuning, responsável e rollback.

**Saída:** Ficha de implantação.


## Sessão inicial

Abra [Uma regra correta no campo errado](../examples/caso-01.md), leia as evidências e faça uma primeira análise antes de abrir o comentário. Copie a [ficha de trabalho](../templates/ficha.md) para seu caderno e preencha os campos. Compare sua conclusão com o critério de aceite.

**Critério de conclusão:** A regra só seleciona o evento positivo; o campo ausente gera problema de qualidade de dados, e não acusação automática.

## Fronteira editorial

ThreatHunting descobre e investiga; este repositório transforma comportamentos observáveis em especificações de detecção reproduzíveis.

[Início](../README.md) · [Referências](REFERENCIAS.md)
