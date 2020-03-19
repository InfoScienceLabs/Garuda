# Garuda

[Garuda](http://165.22.54.104:4200/) is open-Source product.
you can understand the garuda application architecture with help of below diagram:-
![](image/applicationarchitecturediagram.png)

## Getting Started

There are following 4 parts of garuda:-
* Garuda-API [click to clone](https://github.com/Infosciencelabsdev/Garuda-API)
* Garuda-Processor [click to clone](https://github.com/Infosciencelabsdev/Garuda-Processor)
* Garuda-Angular [click to clone](https://github.com/Infosciencelabsdev/Garuda-Angular)
* Garuda-Explorer [click to clone](https://github.com/Infosciencelabsdev/Garuda-Explorer)
```
After cloning all above parts of Garuda, you have to Look on Prerequisites and Installing
```
### Prerequisites

This is the tech Stack we are using to develop Garuda. Make sure you are familiar with all of these:-
1. NodeJs - Server Side
2. Hapi Framework - Creating routes using Server
3. TypeScript - Language used for Node and Angular
4. MySql - Database
5. Sawtooth Javascript SDK - To store data over Blockchain
6. Docker - Making microservices using containers.
7. Angular 6/7/8 - Front End Portion



### Installing

To reproduce the Garuda Environment in your local system you can refer to this:

#### Setting up RethinkDB:
* Install RethinkDB. 
* Run RethinkDB as a service by running it at startup:[Start_RethinkDB](https://rethinkdb.com/docs/start-on-startup/)
 You can access RerthinkDB at localhost:8080.
* You can create databases and tables under 'TABLES' and access the data under "DATA EXPLORER",Create a database: "explorer" and create 2 tables under this: "PropData" [Primary Key: 'propId'] and 'PropDetails" [Primary Key: 'primId']

#### Setting up MongoDB:
* Install MongoDB
* Create users and give them authentication:[Create User in MongoDB](https://docs.mongodb.com/manual/reference/method/db.createUser/)
* For accessing glock (db of garuda) you need to give admin role for the credentials 
  ```username: OneUser and pwd:  onetrwpassword ```
#### Setting up garuda server:
* Clone the beta 2.0 branch of garuda_api.
* npm install
* In the terminal execute: npm run buildstart

```
Note : If you get any node module errors click on the error and at the point mentioned add "any" in front of [ ] at both the places. This is a typescript error with web3 which is an ethereum dependency.
```
#### Setting up the sawtooth network:
* In a terminal navigate to garuda_api directory and execute "docker-compose up" 
* Docker Compose file is already included with the necessary changes.
#### Setting up the garuda processor.
* Clone the garuda_processor repo
* ``` npm install ```
* To execute it: 
```
ts-node index.ts

```
#### Setting up the Angular repositories:
* For Garuda Application clone the garuda-angular beta 2.0 branch
* Install Angular and do ``` npm install ```
* Change the url for server in url.ts from xxx.xx.xx.xxx to localhost to give the api calls to your local server.
* To run the project execute:
    ``` 
    ng serve --port 4200
    
    ````
* For Garuda Explorer clone garuda-explorer and do ``` npm install ```
* Change the url in the config file for this also to localhost
* To run the project execute:
    ```
     ng serve --port 4100 
     
    ```


## Authors

* **INFO SCIENCE LABS** - *Initial work* - [Info Science Lab](https://github.com/Infosciencelabsdev)

See also the list of [contributors](https://github.com/Infosciencelabsdev/Garuda/graphs/contributors) who participated in this project.

## License
This project is licensed under the Apache License- see the [LICENSE](LICENSE) file for details

