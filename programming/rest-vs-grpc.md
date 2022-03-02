# REST vs gRPC

Both REST and gRPC are protocols for communication.



REST is a way client-server communication based on HTTP/1 w/ GET, PUT, POST, DELETE, PATCH methods. Roy Fielding introduced with a set of concepts like cachability, stateless behavior etc.



References

{% embed url="https://en.wikipedia.org/wiki/Representational_state_transfer" %}

{% embed url="https://www.ics.uci.edu/~fielding/pubs/dissertation/rest_arch_style.htm" %}



gRPC



[gRPC (Remote Procedure Call) is an open-source data exchange technology](https://www.baeldung.com/grpc-introduction) developed by Google using the [HTTP/2 protocol](https://www.baeldung.com/netty-http2).

**It uses the** [**Protocol Buffers binary format (Protobuf) for data exchange**](https://www.baeldung.com/spring-rest-api-with-protocol-buffers#1-introduction-to-protocol-buffers). Also, this architectural style enforces rules that a developer must follow to develop or consume web APIs.

RPC follows a client-response model of communication for [designing web APIs that rely on HTTP/2](https://www.baeldung.com/java-9-http-client). Hence, **gRPC allows streaming communication and serves multiple requests simultaneously**. In addition to that, **gRPC also supports unary communication similar to REST**.



{% embed url="https://www.baeldung.com/rest-vs-grpc" %}

{% embed url="https://grpc.io" %}

[https://dudewho.codes/talks/building-better-python-microservices-with-grpc/](https://dudewho.codes/talks/building-better-python-microservices-with-grpc/)
