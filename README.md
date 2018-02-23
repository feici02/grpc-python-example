# gRPC example
Please follow step below.

## Install `grpc` and `grpc-tool` in a virtual environment
```
$ python -m venv venv
$ source venv/bin/activate
$ pip install grpcio grpcio-tools
# or just:
$ pip install -r requirements.txt
```
## Generate gRPC code
```
$ python -m grpc_tools.protoc -I. --python_out=. --grpc_python_out=. helloworld.proto
```

## Run the test
```
# start the server
$ python greeter_server.py

# run the client in another terminal
$ python greeter_client.py
Greeter client received: Hello, you!
Greeter client received: Hello again, you!
```
