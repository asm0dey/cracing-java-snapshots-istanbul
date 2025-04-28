FROM bellsoft/alpaquita-linux-base

RUN wget https://download.bell-sw.com/java/21.0.7+11/bellsoft-jdk21.0.7+11-linux-x64-musl-crac.apk -O /jdk.apk && apk add --allow-untrusted /jdk.apk && rm -f /jdk.apk
ADD spring-petclinic-3.4.0.jar /app/app.jar
WORKDIR /app
ENTRYPOINT java -XX:CRaCCheckpointTo=/app/checkpoint -jar /app/app.jar
