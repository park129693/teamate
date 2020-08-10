# teamate

# hyperledger fabric sample 

## pre-condition

* curl, docker, docker-compose, go, nodejs, python 
* hyperledger fabric-docker images are installed
* GOPATH are configured
* hyperledger bineries are installed (cryptogen, configtxgen ... etcs)

# -network

## 1. generating crypto-config directory, genesis.block, channel and anchor peer transactions

cd network

./generate.sh

## 2. starting the network, create channel and join 

./start.sh

# -chaincode

## 3. chaincode install, instsantiate and test(invoke, query, invoke)

./cc_tea.sh instantiate v1.0

# -prototype

cd ../prototype

## 4. nodejs module install

npm install

## 5. certification works

node enrollAdmin.js

node registerUser.js

## 6. server start

node server.js

## 7. open web browser and connect to localhost:8080

 

## 8. prototype  사이트맵구조

![sitemap](https://user-images.githubusercontent.com/65533250/89747476-e3b19780-daf9-11ea-93d5-513e465ce459.jpg)



### -web_template

##### 1.teamate/network 이동 

```shell
cd network
```



##### 2. ./teardown.sh 실행을 통해 container 제거

```shell
./teardown.sh
```



##### 3. ./start.sh 실행을 통한 network 실행

```shell
./start.sh
```



##### 4. ./cc_tea.sh 실행을 통한 chaincode install

```shell
./cc_tea.sh instantiate v1.0
```



##### 5. web_template로 이동 후 npm을 이용한 라이브러리 설치

```shell
cd ../web_template

npm install
```



##### 6. enrollAdmin.js 실행을 통한 adminID 등록

###### -web_template안에 wallet이 존재할 경우 rm -rf wallet을 통해 제거

```shell
node enrollAdmin.js
```



##### 7. registerUser.js 실행을 통한 user등록

```shell
node registerUser.js
```



##### 8. Server 실행

```shell
node server.js
```

