# Sobre o projeto
Esse é um projeto de um dos módulos do treinamento fullcycle, onde o objetivo é apresentar a forma de comunicação RPC utilizando gRPC.

## Como rodar o projeto?

- Inicie o servidor:

```bash
  go run cmd/server/server.go
```

- Inicie o client:

```bash
  go run cmd/client/client.go
```

## Como compilar novos protos no projeto?
Você precisa ter o [protoc](https://grpc.io/docs/protoc-installation/) instalado e configurado em sua máquina.

- Depois de configurado rode o comando:
```bash
  protoc --proto_path=proto/ proto/*.proto --plugin=$(go env GOPATH)/bin/protoc-gen-go-grpc --go-grpc_out=. --go_out=.
```

- Não se esqueça de exportar o path:
```bash
  export PATH="$PATH:$(go env GOPATH)/bin" 
```

