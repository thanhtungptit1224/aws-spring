# Quartz com Spring Boot Clustered


```shell script
mvn clean install
```

```shell script
docker-compose up --build
```

job qtest2_1:

```shell script
qtest2_1  | 2021-06-21 23:59:55.021  INFO 8 --- [eduler_Worker-3] com.example.quartz.service.TestService   : Running job on supervisor, job id ATestJob
qtest2_1  | 2021-06-21 23:59:55.021  INFO 8 --- [eduler_Worker-3] com.example.quartz.service.TestService   : Completed job on supervisor, job id ATestJob
qtest2_1  | 2021-06-21 23:59:55.026  INFO 8 --- [eduler_Worker-4] com.example.quartz.job.ATestJob          : ATestJob Running
qtest2_1  | 2021-06-21 23:59:55.026  INFO 8 --- [eduler_Worker-4] com.example.quartz.service.TestService   : Running job on supervisor, job id ATestJob
qtest2_1  | 2021-06-21 23:59:55.026  INFO 8 --- [eduler_Worker-4] com.example.quartz.service.TestService   : Completed job on supervisor, job id ATestJob
qtest2_1  | 2021-06-21 23:59:55.044  INFO 8 --- [eduler_Worker-5] com.example.quartz.job.ATestJob          : ATestJob Running
```

```shell script
docker rm -f quartz_qtest2_1
```

**qtest1_1**:
```shell script
qtest1_1  | 2021-06-21 23:59:56.013  INFO 8 --- [eduler_Worker-9] com.example.quartz.service.TestService   : Running job on supervisor, job id ATestJob
qtest1_1  | 2021-06-21 23:59:56.013  INFO 8 --- [eduler_Worker-9] com.example.quartz.service.TestService   : Completed job on supervisor, job id ATestJob
qtest1_1  | 2021-06-21 23:59:58.025  INFO 8 --- [duler_Worker-10] com.example.quartz.job.ATestJob          : ATestJob Running
qtest1_1  | 2021-06-21 23:59:58.025  INFO 8 --- [duler_Worker-10] com.example.quartz.service.TestService   : Running job on supervisor, job id ATestJob
qtest1_1  | 2021-06-21 23:59:58.025  INFO 8 --- [duler_Worker-10] com.example.quartz.service.TestService   : Completed job on supervisor, job id ATestJob

```
