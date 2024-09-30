# Usa una imagen base de Java
FROM openjdk:17-jdk-alpine

# Establece el directorio de trabajo
WORKDIR /app

# Copia el JAR del microservicio al contenedor
COPY target/microservice_users-1.0.0.jar /app/user-service.jar

# Establece las variables de entorno para la conexión a la base de datos
ENV SPRING_DATASOURCE_URL=jdbc:mysql://usersDB:3306/BaseUsers
ENV SPRING_DATASOURCE_USERNAME=user
ENV SPRING_DATASOURCE_PASSWORD=userpassword

# Expone el puerto 8080 en el contenedor
EXPOSE 8080

# Ejecuta el JAR cuando se levanta el contenedor
ENTRYPOINT ["java", "-jar", "/app/user-service.jar"]
