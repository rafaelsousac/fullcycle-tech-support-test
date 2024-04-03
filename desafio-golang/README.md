### Desafio Golang

A ideia deste desafio é que ao executar os testes, todos devem passar com êxito.

A versão do `Golang` deve ser mantida a `1.16`.

Para isso você deve rodar o projeto com os seguintes passos:

Rodar o container do Golang:

```bash
docker compose up
```

Entrar no container:

```bash
docker compose exec app bash
```

Instalar as dependências:

```bash
go mod tidy
```

Rodar os testes:

```bash
go test ./....
```

Erros ocorrerão e o desafio é resolve-los.