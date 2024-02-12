FROM openjdk:21
EXPOSE 8080
ADD target/k8s-example.jar k8s-example.jar
ENTRYPOINT ["java", "-jar", "/k8s-example.jar"]