createmigration:
	migrate create -ext=sql -dir=sql/migrations -seq init

# localhost:3306 ~> host.docker.internal:3306
migrate:
	migrate -path=sql/migrations -database "mysql://root:root@tcp(host.docker.internal:3306)/chat_test" -verbose up

# localhost:3306 ~> host.docker.internal:3306
migratedown:
	migrate -path=sql/migrations -database "mysql://root:root@tcp(host.docker.internal:3306)/chat_test" -verbose drop	

grpc:
	protoc --go_out=. --go-grpc_out=. proto/chat.proto --experimental_allow_proto3_optional

.PHONY: migrate createmigration migratedown grpc