FROM openjdk:17

COPY target/sentinel-dashboard.jar /sentinel-dashboard.jar

ENV TZ=Asia/Shanghai

EXPOSE 8080

# Configure the JAVA_OPTIONS, you can add -XshowSettings:vm to also display the heap size.

ENV JAVA_TOOL_OPTIONS="-agentlib:jdwp=transport=dt_socket,address=*:35005,server=y,suspend=n"


CMD java -jar sentinel-dashboard.jar