# POM for REST Microservices

 * JPA Persistence
 * HATEOS


## Libraries

* spring-boot 1.5.2.RELEASE
* spring-boot-starter-actuator
* spring-boot-starter-web
* spring-boot-starter-web-services
* spring-boot-starter-data-jpa
* spring-boot-starter-hateoas
* io.prometheus 0.0.26
* com.jayway.jsonpath:jsonpath
* lombok 1.16.20
* commons-io 2.3


[Google - Schema.org parser](https://github.com/google/schemaorg-java)

# ProtoBuf

Should use Proto Buffers instead of JSON?

```
message Person {
  required string name = 1;
  required int32 id = 2;
  optional string email = 3;

  enum PhoneType {
    MOBILE = 0;
    HOME = 1;
    WORK = 2;
  }

  message PhoneNumber {
    required string number = 1;
    optional PhoneType type = 2 [default = HOME];
  }

  repeated PhoneNumber phone = 4;
}
```

https://developers.google.com/protocol-buffers/docs/overview#a-bit-of-history	

http://h22208.www2.hpe.com/eginfolib/networking/docs/sdn/sdnc2_7/5200-0910prog/content/s_sdnc-app-ha-versioning-GPB.html

https://tech.travelaudience.com/bigtable-storing-protobuf-bytes-in-one-column-vs-splitting-the-content-into-column-families-c231bdff8db7

https://www.baeldung.com/spring-rest-api-with-protocol-buffers


# Monitoring

Prometheus, Spring actuator dependencies

https://g00glen00b.be/monitoring-spring-prometheus-grafana/