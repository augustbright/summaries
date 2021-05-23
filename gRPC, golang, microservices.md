# install protoc-gen-go
go get github.com/golang/protobuf/protoc-gen-go
go install github.com/golang/protobuf/protoc-gen-go

# write greet.proto
syntax = "proto3";

package greet;
option go_package = "/greetpb";

service GreetService{};

# generate code
protoc greet.proto --go_out=plugins=grpc:.
