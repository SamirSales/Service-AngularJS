# Service
"Em vez de preencher o controlador com código para buscar dados meteorológicos de um servidor, é melhor mover essa lógica independente para um serviço para que possa ser reutilizada por outras partes do aplicativo."

"Os serviços são uma maneira de fazer lógica de comunicação autônoma, como a previsão que busca dados meteorológicos de um servidor."

##  js/services/forecast.js

código      | funcionalidade
------------|---------
app.factory | cria um novo serviço chamado ***forecast***
$http       | para obter JSON do servidor
$http.get   | GET request

## MainController.js
Faz uso do ***forecast*** para obter dados do servidor. A requisição é assíncrona e os dados são guardados na variável ***$scope.fiveDay***.
