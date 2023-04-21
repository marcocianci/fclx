### 17 / 04 / 2023

https://github.com/devfullcycle/fclx

https://fcexperience.fullcycle.com.br/aulas/

# aula 01 :: Docker e Containers e Microsserviço do ChatGPT
https://youtu.be/UugkE-OeE4E

# fclx
FC LX - Docker e Containers e Microsserviço do ChatGPT | https://www.youtube.com/watch?v=UugkE-OeE4E&amp;ab_channel=FullCycle

```
go mod tidy
go run cmd/chatservice/main.go
# cria o banco de dados 
make migrate
# cmd pra entrar no docker
docker exec chatservice bash
```

### compilar libtiktoken
```
docker-compose up -d
❯ docker-compose up -d
[+] Running 3/3
 ✔ Network chatservice_default  Created                                                                            0.4s
 ✔ Container mysql              Started                                                                            1.3s
 ✔ Container chatservice_app    Started                                                                            1.4s
docker-compose exec chatservice bash 
apt update
apt install -y protobuf-compiler
# executar dentro da pasta tiktoken-cffi (/home/marco/.asdf/installs/golang/1.20.3/packages/pkg/mod/github.com/j178/tiktoken-go@v0.2.1/tiktoken-cffi)
# que esta dentro do docker /app/
❯ docker-compose exec chatservice bash
root@e83db4a39696:/go/src# cd tiktoken-cffi/
root@e83db4a39696:/go/src/tiktoken-cffi#
cargo build --release
```
depois de fazer o build, copiar a pasta **target** para a pasta q estava com erro, no meu caso eh:
**/installs/golang/1.20.3/packages/pkg/mod/github.com/j178/tiktoken-go@v0.2.1/tiktoken-cffi **

rodar dentro do docker do chatmessage
```
make grpc
```


cp -r /home/marco/.asdf/installs/golang/1.20.3/packages/pkg/mod/github.com/j178/tiktoken-go@v0.2.1/tiktoken-cffitarget tiktoken-cffi

ls -lash /home/malevisa/.asdf/installs/golang/1.20.3/packages/pkg/mod/github.com/j178/tiktoken-go@v0.2.1/tiktoken-cffi
cp -r target /home/malevisa/.asdf/installs/golang/1.20.3/packages/pkg/mod/github.com/j178/tiktoken-go@v0.2.1/tiktoken-cffi

