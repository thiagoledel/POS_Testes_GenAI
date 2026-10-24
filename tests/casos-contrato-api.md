# Casos de teste - contrato REST

## CT-01 - Calculo valido
Entrada: `estimatedHours=100`, `hourlyRate=150.00`.
Esperado: operacao aceita e total retornado igual a `15000.00`.

## CT-02 - Limite com zero horas
Entrada: `estimatedHours=0`, `hourlyRate=150.00`.
Esperado: operacao aceita e total igual a `0.00`.

## CT-03 - Horas negativas
Entrada: `estimatedHours=-1`, `hourlyRate=150.00`.
Esperado: requisicao rejeitada e calculo nao executado. Codigo HTTP exato: pendente de definicao do contrato.

## CT-04 - Valor/hora negativo
Entrada: `estimatedHours=100`, `hourlyRate=-150.00`.
Esperado: requisicao rejeitada e calculo nao executado. Codigo HTTP exato: pendente de definicao do contrato.

## CT-05 - Campo obrigatorio ausente
Entrada: payload sem `hourlyRate`.
Esperado: requisicao rejeitada antes da execucao da regra de calculo.

## CT-06 - Tipo de dado invalido
Entrada: `estimatedHours="cem"`, `hourlyRate=150.00`.
Esperado: payload rejeitado pela API e nenhum orcamento gerado.
