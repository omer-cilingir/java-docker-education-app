FROM openjdk:8-jdk-alpine
VOLUME /tmp
COPY files/education.jar /var/lib/education/
COPY files/application.properties /var/lib/education
ENTRYPOINT ["java","-jar","/var/lib/education/education.jar","--spring.config.location=/var/lib/education/application.properties"]
