## Cadastro

Nome: [Clean Arch] Adapter externo aderente ao padrao
Comando: clean-arch-adapter-externo-padrao
Descrição: Analisa a qualidade do código de um adapter externo(por exemplo um controller) do ponto de vista da arquitetura limpa. 

## Step 1

Prompt name: avalia-codigo

### Prompt

```
## Contexto

A responsabilidade da camada mais externa é receber os dados de entrada, realizar qualquer validação que tenha relação específica com esses dados e, depois, simplesmente chamar a próxima camada para que ela possa executar o fluxo de negócio em si. 

## Pontos de atenção

Nessa camada mais externa não devemos ter acesso direto a banco de dados, serviços externas etc. Ela recebe dados, verifica a validade dos mesmos, eventualmente transforma para o formato esperado da próxima camada e aí faz a chamada. 

## Instrução

Analise o código considerando o contexto e a restrição. 

[codigo]
 {{selected_code}} 
[/codigo]

## Resposta

A resposta deve ter uma nota entre e 0 e 10 avaliando a aderência do código ao padrão estabelecido e uma explicação sobre a nota. 
```

## (end)

### Prompt

```
  {{avalia-codigo.answer}} 
```