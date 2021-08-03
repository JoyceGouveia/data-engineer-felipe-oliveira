# Case Cortex
Os exercícios são baseados em parametrizações que serão solicitadas na hora da apresentação.
Dica: Quanto menos hardcoded, melhor :)

## Observações:
* Você pode utilizar um banco de dados relacional ou não relacional como PostgreSQL, Oracle, MYSQL, H2, HSQLDB, MongoDB, dentro outros, arquivos em disco, estrutura em memória ou qualquer outro serviço relacionado desejado.
* Ao enviar o código final, deve estar claro como rodar os projetos feitos e quais serviços precisam ser configurados/acessados.
* Preferencialmente, recomendamos uso de NodeJS, Python ou Java mas você pode utilizar qualquer linguagem e/ou tecnologia que queira.
* Se você disponibilizar os serviços em algum lugar para rodarmos diretamente, como um Heroku, você ganha pontos extras.
* Caso não consiga terminar algum exercício, sinalize no readme a dificuldade encontrada e/ou o que você faria diferente se tivesse mais tempo.

## Exercícios

### Exercício 1:
Construa uma aplicação que irá consumir dados da API do IBGE. Deve ser possível realizar uma chamada através de API REST contendo os parâmetros necessários como exemplo abaixo:
```
Tabela: 5167
Período: 2015
Variável: 5511
Nível territorial: N1
```
O serviço também deverá ser capaz de utilizar JOBS para execução de consultas através de CRON cadastradas anteriormente em banco de dados, depositando os dados obtidos no em arquivos em formatos de sua preferência.

### Exercício 2:
Faça um esquema de uma arquitetura utilizando o serviço feito no Exercício 1. A arquitetura deve atender os requisitos abaixo:

* Deve existir um esquema de filas para orquestração das chamadas à API do IBGE. Exemplo: A aplicação irá receber um requisição REST ou ler na base as consultas que devem ser executadas de acordo com a CRON e disparar mensagens para um consumidor da API do IBGE.

O resultado desse exercício deve ser um diagrama, um esquema. Você pode complementar com um texto, explicando como os itens da arquitetura se comunicam e como pensou para fazer o desenho da mesma.

Você pode também utilizar várias filas em diferentes lugares. Outras coisas não descritas na arquitetura também podem ser incluídas, como banco de dados (diversos), sistemas de logs, métricas, etc. É obrigatório ter ao menos uma fila.

### Exercício 3:
Implemente a arquitetura desenhada no exercício 2. Considere, caso a arquitetura fique muito complexa, implementar apenas uma parte dela. Desejável ao menos a parte da fila.

## Requisitos
* Disponibilizar o projeto neste repositório do GIT
* Disponibilizar um README documentando os processos construídos e como executar os projetos (fique à vontade para remover o `README.md` atual)

## Critérios de avaliação
* **Organização do código**: Separação de módulos, view, model, back-end, etc.
* **Flexibilidade do código**: Quanto mais variáveis parametrizáveis, melhor será a avaliação.
* **Assertividade**: A aplicação está fazendo o que é esperado? Se tem algo faltando, o README explica o porquê?
* **Clareza**: O README explica de forma resumida qual é o problema e como pode rodar a aplicação?
* **Legibilidade do código** (incluindo comentários)
* **Segurança**: Existe alguma vulnerabilidade clara?
* **Cobertura de testes** (Não esperamos cobertura completa)
* **Histórico de commits** (estrutura e qualidade)
* **Escolhas técnicas**: A escolha das bibliotecas, banco de dados, arquitetura, etc. É a melhor escolha para a aplicação?

## Prazo e como entregar
Este case não deve tomar muito do seu tempo - a ideia é que ele seja prático. Inicialmente você terá o prazo de 7 dias a partir do momento que você o receber, caso precise de mais tempo, basta avisar a pessoa de recrutamento que está em contato com você 😉.

Quando terminar o desafio, avisa pra gente e crie uma tag chamada `final` no seu repositório, para criar a tag basta seguir o passo a passo:
1. `git tag -a 'final' -m 'finalizei :-)'`
2. `git push origin 'final'`

Boa Sorte! 😃 🚀
