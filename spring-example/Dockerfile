FROM bellsoft/alpaquita-linux-base AS runner

RUN wget https://download.bell-sw.com/java/21.0.7+11/bellsoft-jdk21.0.7+11-linux-x64-musl-crac.apk -O /jdk.apk && apk add --allow-untrusted /jdk.apk && rm -f /jdk.apk
ADD ./build/libs/demo-0.0.1-SNAPSHOT.jar /app/app.jar
ENTRYPOINT java -XX:CRaCCheckpointTo=/app/checkpoint -jar /app/app.jar
