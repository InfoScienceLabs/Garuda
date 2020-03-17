# Garuda

Garuda is open-Source product,you can visit [garuda](http://165.22.54.104:4200/).
you can understand the garuda application architecture with help of below diagram:-
![](image/)

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

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

## Running the tests

Explain how to run the automated tests for this system

### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc
