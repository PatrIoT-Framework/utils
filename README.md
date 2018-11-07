# Iproute2, iptables REST API

IPRoute rest api is used for remote
control of routing tables on virtual machine / container.
IPTable rest api is same as ip-route rest api used for remote
control of ip tables on virtual machine / container.

REST API for ip tables forked from:
 * [api-iptables](https://github.com/obabec/iptables-api/) - REST API for iptables

## Getting Started
These instructions will get you a copy of the project up and running on your 
local machine for development purposes.

### Prerequisites
#### Python

```
pip install pyroute2
pip install -U jsonpickle
pip install Flask

```
#### Go
```
go get -u github.com/gorilla/mux
go get -u github.com/oxalide/go-iptables
go get -u github.com/gorilla/handlers

```
## Compile
```
cd iptables
go build -o iptables-api
```
## Deployment
#### iproute2:
```
cd iproute
flask run --host=IP
```
#### iptables:
```
cd iptables
./iptables-api -ip IP
```
IP is IPv4 on which will be API listening

