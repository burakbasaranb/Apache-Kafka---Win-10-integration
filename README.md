
# Apache Kafka - Win10 Installation

#### STEP 1: Install JAVA JDK and JVM
Download Link: https://www.java.com/tr/download/

#### STEP 2: DOWNLOAD AND INSTALL KAFKA
Download Link: https://kafka.apache.org/downloads
- 2.1. Download last version as "kafka-3.4.0-src.tgz"
- 2.2. Use 7zip and unzip .tgz then .tar 

#### STEP 3: START THE KAFKA ENVIRONMENT
- 3.1. Open a terminal
- 3.2. Go to Kafka folder as "cd C:\Users\DESKTOP\Downloads\kafka"
```bash
	cd <kafka folder path>
```
- 3.3. Start the ZooKeeper service
```bash
	.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
```
- 3.4. Do not close terminal
	
#### STEP 4: START THE KAFKA BROKER SERVICE
- 4.1. Open secound terminal
- 4.2. Go to Kafka folder  as "cd C:\Users\DESKTOP\Downloads\kafka"
```bash
	cd <kafka folder path>
```
- 4.3. Start the Kafka broker service
```bash
	.\bin\windows\kafka-server-start.bat .\config\server.properties
```
- 4.4. Do not close terminal

#### STEP 5: CREATE A TOPIC TO STORE YOUR EVENTS
- 5.1. Open third terminal
- 5.2. Go to Kafka folder  as "cd C:\Users\DESKTOP\Downloads\kafka"
```bash
	cd <kafka folder path>
```
- 5.3. Create topic
```bash
	.\bin\windows\kafka-topics.bat --create --topic topic_demo --bootstrap-server localhost:9092
```

#### STEP 6: WRITE SOME EVENTS INTO THE TOPIC
- 6.1. Open producer to send (put) data to topic which is "topic_demo" 
```bash
	.\bin\windows\kafka-console-producer.bat --topic topic_demo --bootstrap-server localhost:9092
```
- 6.2. White line by line what you want
- 6.3. Exit press Ctrl + C

#### STEP 7:  READ THE EVENTS
- 7.1. Read from "topic_demo" topic
```bash
	.\bin\windows\kafka-console-consumer.bat --topic topic_demo --from-beginning --bootstrap-server localhost:9092
```


