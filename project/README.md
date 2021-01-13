# Ethereum Dapp for Tracking Items on a Supply Chain
The write-up part of this project consists of the following elements:
- UML diagrams
- Libraries
- IPFS

**Disclaimer:**
In order to focus on the asks, I will not include steps in the different implementations that are not explicity requested. For example, If a product could not be validated successfully, it would not progress further down the process chain. The basic assumption is that everything is _just fine_ and that every participant is somehow _pre validated_. Therefore the overall process would not be used in a real world scenario, the way it is implemented for this project.

## General information
- contract address in Rinkeby: ```0x0```
- Node version    : ```v14.15.1```
- Solidity version: ```^0.4.24 (solc-js)```
- Truffle version : ```v5.1.59 (core: 5.1.59)```
- Web3.js version : ```v1.2.9```

## How to use?
- Clone this repository
```git clone <URL>```

- Install the dependencies
```switch into the ./project directory```
```npm install```


## UML Diagrams
The following diagrams are required:
- Activity Diagram
- Sequence Diagram
- State Diagram
- Class Diagram (Data Model)

### Acticity Diagram
This diagram illustrates the basic activities and the related actors (swim-lanes).\
\
The _Farmer_ is responsible to grow the plants and the process starts once the coffee beans can be harvested. The first activity is to **harvest** the coffee. Next, several **process**ing steps are executed in order to create the final product. In this example we will abstract all of those steps away and assume that all required steps are encapsulated in a single activity. Now the coffee can be **pack**ed and can be sold (**sell**) to the next actor, who is the _Distributor_.\
\
The _Distributor_ **buy**s coffee from the _Farmer_ and then **ship**s the goods to the _Retailer_.\
\
The _Retailer_ **receive**s coffee from the _Distributor_ and puts the goods for sale, so that the _Customer_s can **purchase** the coffee.

![](./UML/activity-diagram.png)

### Sequence Diagram
This diagram illustrates the function call orders. The _blue_ parts are not implemented explicitly, but were mentioned in the project documentation.

![](./UML/sequence-diagram.png)

### State Diagram
This diagram modells the interactions between Actors, the involved methods and required pre-conditions, as well as the States.

![](./UML/state-diagram.png)

### Class Diagram
This diagram illustrates the contract structure and dependencies, as well as attributes and methods.
![](./UML/class-diagram.png)

## Libraries
The following libraries and versions are used in this project:

## IPFS
The InterPlanetary File-System provides the ability to host our web application in a fully decentralized way. 