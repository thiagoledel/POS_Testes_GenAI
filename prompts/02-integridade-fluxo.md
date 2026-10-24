# Prompt 2 - Fluxo de integracao e integridade dos dados

Atue como engenheiro de testes de integracao em uma aplicacao Java/Spring Boot.

O fluxo testado e:

API REST -> servico de calculo -> repositorio de orcamentos -> PostgreSQL.

A aplicacao recebe `estimatedHours` e `hourlyRate`, calcula `total = estimatedHours * hourlyRate` e persiste o resultado vinculado ao projeto.

Gere casos de teste que validem a integracao entre os componentes e a integridade dos dados. Considere:
- preservacao das entradas entre API e servico;
- precisao do calculo monetario;
- persistencia do total correto;
- rejeicao de valores negativos antes da persistencia;
- comportamento quando ocorrer falha de persistencia;
- garantia de que um erro nao grave um orcamento parcial ou inconsistente.

Utilize apenas dados ficticios. Para cada caso, informe pre-condicao, entrada, validacoes em cada componente e resultado esperado. Nao defina automaticamente politica de retry ou codigo HTTP quando isso nao tiver sido especificado: registre como ponto pendente.
