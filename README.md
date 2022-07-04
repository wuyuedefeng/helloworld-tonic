
```bash
# start server
$ cargo run --bin helloworld-server

# start client request
$ cargo run --bin helloworld-client
# or use grpcurl
# $ brew install grpcurl
$ grpcurl -plaintext -import-path ./proto -proto helloworld.proto -d '{"name": "Tonic"}' [::]:50051 helloworld.Greeter/SayHello

```