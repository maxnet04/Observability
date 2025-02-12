# Temperatura por CEP - Tracing entre microservices
Sistema retorna clima atual baseado em um CEP informado

Desafio Pós Go Expert - 2024 Labs -> Consulta Temperatura baseado em um CEP informado - FullCycle

### Como Utilizar localmente:
#### Requisitos:
    - Certifique-se de ter o Go instalado em sua máquina.
    - Certifique-se de ter o Docker instalado em sua máquina.
    - Foi atulizado a API viaCEP para encontrar a localização que deseja consultar a temperatura: https://viacep.com.br/
    - Foi utilizado a API WeatherAPI para consultar as temperaturas desejadas: https://www.weatherapi.com/

  1. Clonar o Repositório:~
  ```git clone https://github.com/maxnet04/observability.git```

  2. Acesse a pasta do app:
  ```cd observability```

  3. Para rodar :
  ```docker compose up -d ```


    Observação: Necessario informar a API KEY da plataforma de consulta de temperatura no arquivo config.env na raiz do projeto conforma abaixo:
    WEATHER_API_KEY=XXXXXXXXXXXXXXXXXXXXX

### Como testar localmente:
Porta: HTTP server on port :8080

#### Execute o curl abaixo ou use um aplicação client REST para realizar a requisição:

    curl --request POST \
    --url http://localhost:8080/ \
    --header 'Content-Type: application/json' \
    --header 'User-Agent: insomnia/10.0.0' \
    --data '{
      "cep": "36205060"
    }'


###### Observação: Informar o CEP numerico 8 caracteres como "body"