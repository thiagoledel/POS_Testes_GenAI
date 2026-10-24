# Prompt 1 - Contrato da API

Atue como engenheiro de testes de software especializado em APIs REST.

Estou testando uma API Java/Spring Boot de uma aplicacao de estimativas e orcamentos de projetos de software.

Considere a operacao ficticia:

`POST /api/projects/{projectId}/budget`

Entrada:
- `estimatedHours`: numero decimal maior ou igual a zero;
- `hourlyRate`: valor monetario maior ou igual a zero.

Saida esperada:
- identificador do projeto;
- horas consideradas;
- valor/hora considerado;
- total calculado pelo servico.

Regra: `total = estimatedHours * hourlyRate`.

Gere casos de teste de integracao com foco exclusivo no contrato REST, incluindo:
- fluxo valido;
- valores iguais a zero;
- horas negativas;
- valor/hora negativo;
- campo obrigatorio ausente;
- tipo de dado invalido.

Para cada caso, informe entrada, resultado esperado e justificativa. Nao invente novas regras de negocio. Quando o comportamento HTTP nao estiver definido, marque-o como pendente em vez de assumir uma resposta.
