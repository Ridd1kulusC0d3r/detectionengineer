# Contribuindo para Detection Engineer

Obrigado pelo seu interesse em contribuir! Este projeto transforma comportamentos observáveis em especificações de detecção reproduzíveis, atuando como uma base documental.

## Como contribuir

1. **Problemas e Casos:** Inclua o problema resolvido, fonte original, data, limitações e condições de reutilização.
2. **Rigor Analítico:** Diferencie sempre observação, interpretação e hipótese.
3. **Direitos Autorais:** Recursos externos permanecem sujeitos às licenças e condições dos respectivos autores.
4. **Foco:** O objetivo é projetar o ciclo de vida (telemetria, lógica, testes, tuning, rollback). Evite enviar códigos executáveis complexos que fujam da proposta de exercício documental.

## Adicionando Novos Casos

Se você for criar um novo caso em `examples/`:

- Utilize o template de Issue `Novo Caso de Uso` para discutir a ideia antes de implementá-la.
- Siga a estrutura dos casos existentes.
- Inclua o critério de aceite (a resposta esperada) envolto em uma tag `<details>` no final do documento para que o leitor possa tentar resolver antes de ler a solução.

## Adicionando Referências

Se você for adicionar uma nova referência em `docs/REFERENCIAS.md`:

- Escolha a referência pelo problema que ela resolve, e não pela popularidade.
- Adicione uma pequena justificativa na coluna "Por que consultar".

## Processo de Pull Request

- Abra seu PR referenciando a Issue relacionada (se houver).
- Preencha o Checklist de PR adequadamente.
- Assegure-se de que a formatação Markdown está correta (usamos linter no CI).
