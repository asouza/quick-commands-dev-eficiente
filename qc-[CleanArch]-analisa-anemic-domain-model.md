## Cadastro

Nome: [Clean Arch] Analisa Anemic Domain Model
Comando: clean-arch-anemic-domain-model
Descrição: Quick command que avalia se as lógicas sobre os estados de entidade estão realmente dentro das entidades. 

## Step 1

Prompt name: avalia-codigo

### Prompt

```
## Contexto

A camada de service/use case de um software é a responsável por executar um fluxo de negócio. Dentro deste fluxo, muitas classes consideradas entidades são utilizadas. Essas são classes que geralmente tem o estado do sistema. Idealmente toda lógica sobre estes estados deveriam viver em métodos das próprias entidades. 

## Restrições

Penalize sempre que tiver uma lógica sobre estado de uma entidade sendo executada direto na camada de serviço. Segue um exemplo:

[exemplo]
         //este é um exemplo onde a lógica poderia morar no na classe da variável **person**. 
		if ( person.getSchoolId() == null || person.getFirstName() == null || person.getLastName() == null
                || person.getPrimaryEmailAddress() == null ) {
               
         }
[/exemplo]

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