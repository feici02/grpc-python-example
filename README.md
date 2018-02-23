# gRPC example

## Install `grpc` and `grpc-tool` in a virtual environment
```
$ python -m venv venv
$ source venv/bin/activate
$ pip install grpcio grpcio-tools
# or just:
$ pip install -r requirements.txt
```

## Example helloworld
This example is from the [Quick Start](https://grpc.io/docs/quickstart/) part of the gRPC docs.
```
$ cd helloworld
```

### Generate gRPC code
```
$ python -m grpc_tools.protoc -I. --python_out=. --grpc_python_out=. helloworld.proto
```

### Run the test
```
# start the server
$ python greeter_server.py

# run the client in another terminal
$ python greeter_client.py
Greeter client received: Hello, you!
Greeter client received: Hello again, you!
```

## Example route_guide
This example is from the [Tutorials](https://grpc.io/docs/tutorials/) part of the gRPC docs.

### Generate gRPC code
```
$ python -m grpc_tools.protoc -I. --python_out=. --grpc_python_out=. route_guide.proto
# or
$ python run_codegen.py
```

### Run the test
```
# start the server
$ python route_guide_server.py

# run the client in another terminal
$ python route_guide_client.py
```
