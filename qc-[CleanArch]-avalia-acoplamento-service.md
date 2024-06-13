## Cadastro

Nome: [Clean Arch] avalia acoplamento service
Comando: clean-arch-avalia-acoplamento-camada
Descrição: Quick command para avaliar o nível de acoplamento da camada de serviço com camadas anteriores. 

## Step 1

Prompt name: avalia-codigo

### Prompt

```
## Contexto

A camada de service/use case de um software é a responsável por executar um fluxo de negócio. A ideia é que essa execução possa ser reaproveitada por diferentes formas de entradas de dados e também de protocolos. Por isso é muito importante que ela não tenha nenhuma influência de protocolos e seus respectivos formatos. 

## Restrições

Nessa camada não devemos encontrar chamadas diretas a métodos/funções conectados com determinado protocolo, uso de status de retorno linkados com protocolos etc. Ela também, idealmente, não deveria falar com outras camadas de serviço. Afinal de contas um caso de uso é específico. 


## Instrução

Analise o código considerando o contexto e restrições. 

[codigo]

 {{selected_code}} 

[/codigo]

## Resposta

A resposta deve ter uma nota entre e 0 e 10 avaliando a aderência do código ao padrão estabelecido e uma explicação sobre a nota. Foque a avaliação no contexto que foi passado.
```

## (end)

### Prompt

```
  {{avalia-codigo.answer}} 
```