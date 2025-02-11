# ChatProject
  album of chartoom projects. \n
## GateServer:
  The GateServer serves as a gateway service, primarily handling connection and registration requests from clients. Since the servers are distributed, after receiving a user's connection request, the GateServer will query the status service to select the address of a ChatServer with a relatively light load and provide it to the client.\n
## ChatServer:
  ChatServer is a chat server that establishes TCP connections and supports distributed services. Multiple servers can be deployed.\n
## VerifyServer:
  When a user registers, the registration information is sent to the GateServer. The GateServer then invokes the VerifyServer to verify the rationality of the registration and sends a verification code to the client. The client can then use this verification code to register with the GateServer. \n
  Both the StatusServer, ServerA, and ServerB can directly access the Redis and Mysql services.
