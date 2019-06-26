# The FormulaOne project  
## Goals  
The FormulaOne app displays and process the data of the Formula One World Championship.  
  
The ultimate goal is to use different tools and frameworks from the open-source Java ecosystem.  
  
This software is shitty and doesn't come with warranty whatsoever.  
  
## Useful commands  
    java8
    java12
  
### labs-formula-one
#### start back-end + database
    docker-compose rm -f -s -v && docker-compose up --build
#### see database
    docker exec -ti labsformulaone_db_1 bash
    mysql -u userFormulaOne -p
        (passwordUserFormulaOne)  
    use formula_one_database;
    show tables;

### labs-formula-one-back
#### spring boot app: build and run
    ./gradlew build
    java -jar build/libs/labs-formula-one-back-0.1.0.jar
  
#### docker app: build, run and push   
    ./gradlew build docker --info
    docker run -p 8080:8080 guillaume/labs-formula-one-back:latest
    docker push guillaumegalloissuperstar/labs-formula-one-back
 
## Useful resources  
- http://ergast.com/mrd/
- https://spring.io/guides/gs/spring-boot-docker



