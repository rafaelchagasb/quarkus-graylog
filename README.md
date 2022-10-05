# Integration with Infinispan

## How do I run?

1 Run docker
```shell
docker-compose up -d
```

2 Open your browser

http://localhost:9000/

User: admin

Password: admin

3 Create Input UDP GELF(PORT 12201)

Open http://localhost:9000/system/inputs and choose "GELF UDP" and click in "Launch new input". 

![graylog_inputs](https://user-images.githubusercontent.com/724699/194117501-6e019232-9057-4c97-97e9-d161966d57ec.jpg)

Mark check *Global* and put one title.

![graylog_inputs_2](https://user-images.githubusercontent.com/724699/194117762-b194d3f4-7353-47ba-b5e2-a78bf6123b37.jpg)


4 Run project

```shell
mvn compile quarkus:dev
```

## How do I test?

1 Send a request

curl --location --request GET 'http://localhost:8080/hello/Robert'

2 Open browser graylog(http://localhost:9000/) and click "All messages"

![graylog_inputs_3](https://user-images.githubusercontent.com/724699/194122179-faf1d372-1f17-4fa2-af11-8ad7fca1c717.jpg)
