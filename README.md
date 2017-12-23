http://www.baeldung.com/spring-cloud-bootstrapping

1. start config server <code>mvn spring-boot:run</code>
2. refresh config-client <code>curl -X POST http://localhost:8081/monitor -d path={app-config-client-1}</code>
- where <code>app-config-client-1</code> is the spring.application.name of client
- which basically calls <code>curl -X POST http://localhost:8090/bus/refresh</code> on the <code>app-config-client-1</code>
- that <code>/bus/refresh</code> does the same thing as <code>/refresh</code>