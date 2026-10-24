# Testes de Integração com GenAI

Este repositório reúne os artefatos de uma atividade acadêmica sobre o uso de Inteligência Artificial Generativa no apoio à criação de testes de integração.

O cenário utilizado é uma aplicação de estimativas e orçamentos de projetos de software. O experimento considera a integração entre uma API REST, o serviço de cálculo do orçamento e a persistência dos dados. A regra simplificada utilizada é:

`orçamento = horas estimadas × valor por hora`

Foram elaborados dois tipos de prompt:

- **Contrato da API:** direcionado à geração de cenários de entrada, saída, valores-limite, campos obrigatórios e dados inválidos.
- **Fluxo e integridade dos dados:** direcionado à comunicação entre API, serviço de cálculo e persistência, incluindo consistência dos valores e falhas entre componentes.

A pasta `prompts` contém as instruções utilizadas com a GenAI, enquanto a pasta `tests` apresenta os casos de teste de integração gerados. Todos os dados utilizados são fictícios e os comportamentos não definidos no escopo foram mantidos como pendências, sem criação de regras de negócio pela IA.
