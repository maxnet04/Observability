# Temperatura por CEP - Observabilidade e Monitoramento
Sistema  identifica a cidade e retorna o clima atual (temperatura em graus celsius, fahrenheit e kelvin) juntamente com a cidade. Esse sistema  implementa  OTEL(Open Telemetry) e Zipkin.

### Como Utilizar localmente:
#### Requisitos:
    - Certifique-se de ter o Go instalado em sua máquina.
    - Certifique-se de ter o Docker instalado em sua máquina.
    
- [GO](https://golang.org/doc/insttall) 1.17 ou superior
- [Docker](https://docs.docker.com/get-docker/)


### Variaáveis dde Ambiente

Certifiquese de informar a API KEY da plataforma de consulta de temperatura no arquivo config.env na raiz do projeto

 WEATHER_API_KEY=ZZZZZZZZZZZZZZ

Como Rodar localmente

  1. Clonar o Repositório:~
  ```git clone https://github.com/maxnet04/observability.git```


  2. Acesse a pasta do app:
  ```cd observability```

  3. Para rodar :
  ```docker compose up -d ```

  4. o serviço estará disponivel em http://localhost:8080.


### Como testar localmente:
Porta: HTTP server on port :8080

#### Execute o curl abaixo:

    curl --request POST \
    --url http://localhost:8080/ \
    --header 'Content-Type: application/json' \
    --header 'User-Agent: insomnia/10.0.0' \
    --data '{
      "cep": {cep}
    }'


###### Substitua pelo cep que deseja testar