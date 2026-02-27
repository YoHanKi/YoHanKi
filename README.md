# 🛠 Contributed

### Redis Jedis [v6.1.0](https://github.com/redis/jedis/releases/tag/v6.1.0)
* **Issue [#3566](https://github.com/redis/jedis/issues/3566)**: `StreamEntry`(XREAD)가 `Map<String, String>` 기반이라 **illegal UTF-8을 포함한 바이너리 field/value가 손상(mangled)** 되는 문제를 제보하고, 손실 없는 `byte[]` 기반 API 필요성을 정리. 
* **Pull Request [#4152](https://github.com/redis/jedis/pull/4152)**: **XREAD/XREADGROUP 바이너리 스트림 지원 추가**. `StreamEntryBinary (Map<byte[], byte[]>)` 도입, `xreadBinary*` / `xreadGroupBinary*` API 추가, BuilderFactory 및 Jedis/UnifiedJedis 구현 반영, RESP2/RESP3 + (Jedis/Cluster/Pooled) 커버하는 테스트 구조로 확장.

### Redis Lettuce (lettuce-core)
* **Issue [#3526](https://github.com/redis/lettuce/issues/3526)**: `ft.search`에서 큰 응답(~200KB) 처리 시 Netty pooled buffer 재사용 때문에 결과가 깨지거나(JVM 결과 garbage) 환경에 따라 SIGSEGV로 크래시가 날 수 있는 메모리 corruption 이슈.
* **Pull Request [#3664](https://github.com/redis/lettuce/pull/3664)**: RediSearch 응답 파싱에서 `EncodedComplexOutput`이 pooled `ByteBuffer`의 read-only view를 저장하던 구조를 **heap으로 copy**하도록 변경해 buffer lifecycle에 의한 corruption/crash를 방지. 재현/회귀 방지용으로 `RediSearchIntegrationTests`에 large JSON payload stress test(`testSearchWithLargeJsonPayloads`) 추가.


# ✍ Stack
**Languages**

<img src="https://img.shields.io/badge/Java-007396?style=flat-square&logo=Java&logoColor=white"/> <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=JavaScript&logoColor=white"/> <img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=HTML5&logoColor=white"/> <img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=CSS3&logoColor=white"/>

**Frameworks & Libraries**

<img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=SpringBoot&logoColor=white"/> <img src="https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square&logo=SpringSecurity&logoColor=white"/> <img src="https://img.shields.io/badge/Spring_Cloud-6DB33F?style=flat-square&logo=SpringCloud&logoColor=white"/> <img src="https://img.shields.io/badge/Spring_Batch-6DB33F?style=flat-square&logo=SpringBatch&logoColor=white"/> <img src="https://img.shields.io/badge/Spring_WebFlux-6DB33F?style=flat-square&logo=Spring&logoColor=white"/> <img src="https://img.shields.io/badge/Vue.js-4FC08D?style=flat-square&logo=Vue.js&logoColor=white"/> <img src="https://img.shields.io/badge/Thymeleaf-005F0F?style=flat-square&logo=Thymeleaf&logoColor=white"/>

**Data Access & ORM**

<img src="https://img.shields.io/badge/JPA-007396?style=flat-square&logo=Java&logoColor=white"/> <img src="https://img.shields.io/badge/Hibernate-59666C?style=flat-square&logo=Hibernate&logoColor=white"/> <img src="https://img.shields.io/badge/MyBatis-339933?style=flat-square&logo=MyBatis&logoColor=white"/> <img src="https://img.shields.io/badge/QueryDSL-000000?style=flat-square&logo=QueryDSL&logoColor=white"/>

**Databases & Caching**

<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=PostgreSQL&logoColor=white"/> <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=MySQL&logoColor=white"/> <img src="https://img.shields.io/badge/MariaDB-003545?style=flat-square&logo=MariaDB&logoColor=white"/> <img src="https://img.shields.io/badge/Oracle-F80000?style=flat-square&logo=Oracle&logoColor=white"/> <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=Redis&logoColor=white"/>

**Testing & Performance**

<img src="https://img.shields.io/badge/JUnit_5-25A162?style=flat-square&logo=JUnit5&logoColor=white"/> <img src="https://img.shields.io/badge/JMeter-6EBAA7?style=flat-square&logo=ApacheJMeter&logoColor=white"/> <img src="https://img.shields.io/badge/Scouter-222222?style=flat-square&logo=&logoColor=white"/>

<a href="s">

[![Solved.ac Profile](http://mazassumnida.wtf/api/v2/generate_badge?boj=alcuz)](https://solved.ac/alcuz/)
</a>

[![Ashutosh's github activity graph](https://github-readme-activity-graph.vercel.app/graph?username=YoHanKi\&theme=vue\&radius=30)](https://github.com/ashutosh00710/github-readme-activity-graph)




