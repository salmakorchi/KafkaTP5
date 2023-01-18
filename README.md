# Démarrage Zookeeper 
Start zookeeper-server-start.bat ../../config/zookeeper.properties
![image](https://user-images.githubusercontent.com/57690392/213173692-12fa0b19-5052-4132-9d23-e19a3cc8c82a.png)

 
# Démarrage KAFKA
start kafka-server-start.bat ../../config/server.properties
![image](https://user-images.githubusercontent.com/57690392/213173795-6c988b4f-a6e8-433f-9edb-997096192867.png)

# lancement du kafka consumer 
start kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic R1
 ![image](https://user-images.githubusercontent.com/57690392/213173840-f6a33db4-81dd-4d37-b6aa-c741ca95d86e.png)

Il va attendre que des messages arrive a ce topic 

# Lancement du kafka Producer 
start kafka-console-producer.bat --broker-list localhost:9092 --topic R1

![image](https://user-images.githubusercontent.com/57690392/213173865-a3147477-19db-45d9-9551-eea684577a91.png)

#consumer a reçue les messages

 ![image](https://user-images.githubusercontent.com/57690392/213173914-e95f00fa-8fc7-4221-b6ef-acf412441237.png)



# Les dependances utilisé 
 
![image](https://user-images.githubusercontent.com/57690392/213173945-033b95f2-9d96-43aa-a1bf-1a8058d3acb7.png)



# On lance un nouveau consumer et on lance l’application
 ![image](https://user-images.githubusercontent.com/57690392/213173989-5bf3698c-af81-42d0-981f-0f3ded2c83ac.png)

# Supplier sur R3
 
 ![image](https://user-images.githubusercontent.com/57690392/213174036-149f181e-9d3a-4f41-823e-794ca581b330.png)

# Analytics 
![image](https://user-images.githubusercontent.com/57690392/213174081-5ab5f73a-257e-42c1-b227-d824a5964b83.png)

bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic R4 --property print.key=true --property print.value=true --property key.deserializer=org.apache.kafka.common.serialization.StringDeserializer --property value.deserializer=org.apache.kafka.common.serialization.LongDeserializer
 
 ![image](https://user-images.githubusercontent.com/57690392/213174183-bb13ac63-a91d-4a9a-9df7-cdf55fdac66b.png)

# Results
![image](https://user-images.githubusercontent.com/57690392/213178110-a997bd6b-84ec-4468-abfe-29b77a493aa2.png)


