# POM for REST Microservices


Parent POM for basing REST / SpringBoot microservices in a docker container.

This creates an infrastructure for semantic versioning of API Implementations, packaged and deployed
with `jib` plugin and with the travis-ci build framwork creates Docker hub images based on those
image baselines.

Libraries:

 * REST
 * WebServices 
 * Karate REST Test framework & Cucumber publishing
 * JPA Persistence 
 * HATEOAS


## Libraries

Visible on Package documentation on Github pages:

https://npiper.github.io/rest.microservice.base/dependencies.html

* spring-boot 2.3.9.RELEASE



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