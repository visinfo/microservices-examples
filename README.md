# Getting Started

### Reference Documentation
For further reference, please consider the following sections:

* [Official Apache Maven documentation](https://maven.apache.org/guides/index.html)

# Coding Exercise Demo For Element  #

## Task ##
Imagine a modular insurance product. People can choose from 4 modules. Each module has a different selectable coverage and a different mathematical risk.

These are the modules:

• Bike(Coverage0-3k,Risk30%)

• Jewelry(Coverage500-10k,Risk5%)

• Electronics(Coverage500-6k,Risk35%)

• SportsEquipment(Coverage0-20k,Risk30%)

The user should be able to select the coverage for each module and see the calculated price. The price of the tariff, which is the individual configuration for each customer, should be calculated based on the risk:
[price] = [coverage]*[risk]

The solution should store calculated prices and make them accessible via an endpoint.


## Description ##

I have used Hexagonal/ Port and Adapter Design Architecture for this Demo

## Resources on Hexagonal / Ports and Adapters ##
 - [Hexagonal Architecture](http://alistair.cockburn.us/Hexagonal+architecture)
 - [Ports-And-Adapters / Hexagonal Architecture](http://www.dossier-andreas.net/software_architecture/ports_and_adapters.html)

This Project has Four Main Modules

 • ## domain ## (All Domain Models and Services)
 
 this module contain all business logic and domain models . I have create Four Models Risk,Product,Coverage,Order. Just to simply I have not created User domain and services .
 
 • in-memory-db-adapter(Storing data in memory )
 
 This module  Storing Product Configurations and Orders for User .To store these entities I  have used HashMap (just to avoid DB  dependencies)
 
 • rest-api-adapter
 
 This Module Expose Rest Endpoints.
 
if you just start the application and navigate to `http://localhost:8091/swagger-ui.html`. There you'll find a nice API documentation thanks to Swagger.

  Order just open docs/swagger.json  in swagger editor .
 ![Swagger Documentation](docs/swagger.json)
 
 .application
 
 this module configure all beans and dependencies

## Getting Started ##

Steps

1. Extract ZIP

2. cd demo/

3. Build Application   mvn clean package

4. Start application with  below commnand(make sure you have 8091 port opened)

java -jar application/target/application-0.0.1-SNAPSHOT.jar


