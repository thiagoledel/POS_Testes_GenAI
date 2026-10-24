# Casos de teste - fluxo e integridade

## TI-01 - Integridade ponta a ponta
Pre-condicao: projeto ficticio existente.
Entrada: 80 horas e valor/hora de 200.00.
Validacoes: API recebe os valores; servico calcula 16000.00; repositorio persiste o mesmo total e o vincula ao projeto correto.
Esperado: dados retornados e persistidos permanecem consistentes.

## TI-02 - Precisao monetaria
Entrada: 10.5 horas e valor/hora de 123.45.
Validacoes: o valor deve percorrer API, servico e persistencia sem perda indevida de precisao.
Esperado: total de 1296.225 antes da aplicacao de qualquer regra de arredondamento. Regra de arredondamento: pendente de negocio.

## TI-03 - Valor negativo nao deve chegar ao banco
Entrada: -5 horas e valor/hora de 100.00.
Validacoes: rejeicao ocorre antes da persistencia; consultar repositorio para confirmar ausencia de novo orcamento.
Esperado: nenhum registro criado.

## TI-04 - Falha ao persistir
Entrada: 100 horas e valor/hora de 150.00, simulando indisponibilidade do repositorio.
Validacoes: calculo pode ocorrer em memoria, mas nenhuma confirmacao de orcamento persistido deve ser retornada.
Esperado: nenhum registro parcial. Codigo HTTP e estrategia de retry: pendentes de definicao.

## TI-05 - Consistencia entre resposta e persistencia
Entrada: 40 horas e valor/hora de 175.50.
Validacoes: comparar o total presente na resposta da API com o valor salvo no banco.
Esperado: ambos representam 7020.00 e mantem o mesmo identificador de projeto.
