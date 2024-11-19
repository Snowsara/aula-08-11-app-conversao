# Aula 08-11 - App Conversão de moeda

## Avaliação

* Implemente para que o usuário possa fazer conversão de outras moedas (mínimo + 3 moedas);
* Descreva abaixo o seu entendimento acerca desta atividade, explorando as funcionalidades das classes que contruímos e os principais pontos da aplicação;

## Entrega

* Clone este repositório e faça o que se pede;
* Realize um commit das suas alterações no seu repositório;
* Envie o link do repositório na avaliação gerada no classroom;

## Descritivo do Aluno:
Um aplicativo de conversão de moedas, as moedas convertidas foram de real para dolar, real para iene(moeda Japonesa) e real para peso (moeda Agentina).
 Começando o código na linha 42 com " RadioGroup rg = findViewById(R.id.opcoes);", que está lidando com a interação de um RadioGroup e os RadioButtons dentro dele, 
permitindo que o usuário escolha uma opção, com base na escolha, definindo uma variável "opcaoSelecionada" com o valor correspondente à seleção e de um evento de
clique no "Button bt" para realizar a conversão.    
Em seguida nós temos na linha 65 um "private void coverter()", que é a parte da conversão da moeda. Nesse trecho, tendo duas verificações iniciais: se o usuário 
selecionou uma opção de conversão e se o usuário inseriu um valor a ser convertido. 
Depois, dentro ainda do "private void coverter()", temos o "try" que esta na linha 78 que é a parte importante do método "converter()" que realiza a conversão
de moeda, após o usuário ter selecionado a moeda e inserido o valor. O código faz uma requisição a uma API para obter a taxa de câmbio atual (o "currencyRate") 
entre as moedas e, em seguida, calcula o valor convertido com base na entrada do usuário.
Para o aplicativo rodar ele tem as principais funções: faz uma requisição à API de câmbio usando "AwesomeClient" e passa a opcaoSelecionada.
Se a requisição for bem-sucedida, ele analisa a resposta "jsonObject" API para obter a conversão da moeda. Se a conversão da moeda relevante for encontrada 
é convertida para um objeto "CurrencyRate".
Se a conversão for encontrada, o valor inserido pelo usuário é multiplicado pela taxa de câmbio (CurrencyRate) e o resultado é exibido em uma "TextView".
Se ocorrer um erro (seja na requisição ou em algum outro ponto), o erro é capturado e uma mensagem é exibida ao usuário via "Toast". 


 
