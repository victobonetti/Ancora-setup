# Cria Pessoa Juridica

``` curl
curl --location 'http://localhost:9091/api/new-pj' \
--header 'Content-Type: application/json' \
--data '{
    "nrCnpj": "12321412412",
    "nmPessoa": "empresa1"
}'
```

# Cria usuario

``` curl
curl --location 'http://localhost:9091/api/new-user' \
--header 'Content-Type: application/json' \
--data-raw '{
    "nrCpf": "12321412412",
    "nrCnpj": "1",
    "nmPessoa": "teste",
    "dsEmail": "teste@email.com",
    "cdSenha": "123",
    "dsIsAdmin": "F"
}'
```

# Ler usuarios

``` curl
curl --location 'http://localhost:9091/api/users'
```

# Ler pfs

``` curl
curl --location --request GET 'http://localhost:9091/api/pfs'
```

# Ler pjs

``` curl
curl --location --request GET 'http://localhost:9091/api/pjs'
```

# Criar Reunião

``` curl
curl --location 'http://localhost:9091/api/meets/createMeeting' \
--header 'Content-Type: application/json' \
--data '{
    "titulo": "titulo teste reuniao",
    "userId": "1"
}'
```

# Obter Records de Reunião 
(A ROTA É http://localhost:9091/api/meets/getRecords/{SPACE_ID});
Ou seja, para acessar a rota precisamos do código SPACE_ID retornado pela rota http://localhost:9091/api/meets/createMeeting

``` curl
curl --location --request GET 'http://localhost:9091/api/meets/getRecords/spaces/ViL1_kUKfCAB' \
--header 'Content-Type: application/json'
```