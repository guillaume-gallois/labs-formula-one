# The FormulaOne project
## Goals
The FormulaOne app displays and process the data of the Formula One World Championship.

The ultimate goal is to use different tools and frameworks from the open-source Java ecosystem.

This software is shitty and doesn't come with warranty whatsoever.

## Useful commands
source /home/guillaume/tk/scripts/java8.sh
source /home/guillaume/tk/scripts/java12.sh

### build & run spring boot app
./gradlew build && java -jar build/libs/labs-formula-one-back-0.1.0.jar

### build & run docker app
./gradlew build docker --info && docker run -p 8080:8080 guillaume/labs-formula-one-back:latest

### run formula_one_database database
docker-compose rm -f -s -v && docker-compose up --build

docker exec -ti labsformulaone_db_1 bash
mysql -u userFormulaOne -p
    (passwordUserFormulaOne)
use formula_one_database;
show tables;

## Useful resources
- http://ergast.com/mrd/
- https://spring.io/guides/gs/spring-boot-docker/
