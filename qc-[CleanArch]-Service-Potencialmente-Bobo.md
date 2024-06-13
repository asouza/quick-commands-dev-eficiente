## Cadastro

Nome: [Clean Arch] Service Potencialmente Bobo
Comando: clean-arch-service--bobo
Descrição: Quick Command para avaliar se determinada camada de serviço simplesmente delega chamadas. 

## Step 1

Prompt name: avalia-codigo

### Prompt

```
## Contexto

A camada de service/use case de um software é a responsável por executar um fluxo de negócio. Só que muitas vezes a lógica que está lá dentro é muito simples, simplesmente delegando a chamada alguma classe da camada de dados. 

## Restrições

Uma classe estilo Service/Caso de Uso tem que merecer existir. Se a lógica é muito simples, algo como simplesmente uma delegação de chamada para outra camada, considere uma penalização forte. 

[exemplo]
  class ClientService {
    public void salva(ClientData clienteData) {
        clientDataRepository.save(clienteData);
    }
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