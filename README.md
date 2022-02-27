# JavaAppWithKafka



## Sample Java ( Spring) application with Apache Kafka workflow added.

## Steps to run the app :
1 . clone the repo  
2 . execute the following commands in order ( from inside the directory where kafka is located in your local)  :  
 &nbsp;&nbsp;1. Start the zookeeper -  .\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties  
 &nbsp;&nbsp;2. Start the server - .\bin\windows\kafka-server-start.bat .\config\server.properties  
 &nbsp;&nbsp;3. Create a topic, here  using "myTopic" as an example  - ./kafka-topics.sh --create --topic myTopic -zookeeper \  localhost:2181 --replication-factor 1 --partitions 1  
3. run the java app -  ./mvnw spring-boot:run    (from inside the root directory of this repo)  
4. go to  - http://localhost:8080/kafka/produce?message=EnterYourMessageHere ( this command essentially sends a message to the kafka server)  
5. go to  - http://localhost:8080/kafka/messages - if you have followe every step above correctly then you wil see your message disaplayed.    
