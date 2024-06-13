## Cadastro

Nome: MVP Analisador CDD Java
Comando: mvp-analisador-cdd-java
Descrição: Um comando que analisa a complexidade de código inspirado no CDD(Cognitive Driven Development)

## Step 1

Prompt name: tenta-achar-blocos-extras-codigo

### Prompt

```
    Identifique no código abaixo instruções de bloco explícitas no código: Try, Catch, Switch, Case, for imperativo, while imperativo, lambdas. 

    {{selected_code}} 

    ## Resposta

    A resposta final deve ser uma lista com os elementos encontrados, pontuação e uma breve explicação sobre a escolha. Faça a lista mais resumida possível. 
```

## Step 2

Prompt name: tenta-achar-expressoes-booleanas

### Prompt

```
Identifique no código abaixo instruções explícitas de expressão booleana. 

 {{selected_code}} 

## Resposta

A resposta final deve ser uma lista com os elementos encontrados, pontuação e uma breve explicação sobre a escolha. Faça a lista mais resumida possível. Se não encontrar nada, retorno ZERO.  
```

## Step 3

Prompt name: tenta-encontrar-contexutal-coupling

### Prompt

```
Identifique no código abaixo acoplamentos com classes especificamente do projeto. Para cada acoplamento, contabilize um ponto. Cada acoplamento só deve ser contabilizado uma vez. 

* Restrição: Não contabilize acoplamento com classes de frameworks e libs como Hibernate, Spring etc. 

 {{selected_code}} 

 ## Resposta

A resposta final deve ser uma lista com os elementos encontrados, pontuação e uma breve explicação sobre a escolha. Faça a lista mais resumida possível. Se não encontrar nada, retorno ZERO. 
```

## Step 4

Prompt name: sumariza-resposta

### Prompt

```
Dado o seguinte contexto:

 {{tenta-achar-blocos-extras-codigo.answer}} 

  {{tenta-achar-expressoes-booleanas.answer}} 

   {{tenta-encontrar-contexutal-coupling.answer}} 

## Resposta

Cria uma lista com todos elementos do contexto e faça a somatória de pontos. 
```

## Step 5 (end)

Prompt name: sumariza-resposta

### Prompt

```
 {{sumariza-resposta.answer}} 
```









