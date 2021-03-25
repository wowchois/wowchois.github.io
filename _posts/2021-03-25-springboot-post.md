---
title: "Spring Boot Annotation 정리"
categories : SpringBoot
date: 2021-03-25 
---

1. @SpringBootApplication
: @EnableAutoConfiguration + @ComponentScan + @Configuation,
스프링부트를 기동하는 main 메소드 역할을 함 (.run() 이 포함됨)
해당 어노테이션이 선언된 클래스의 패키지를 최상위 패키지로 인식하고 ComponentScan을 수행

2. @ComponentScan
: @Controller, @Service, @Repository, @Configuration 이 붙은 클래스 Bean을 찾아 Context 등록

3. @EnableAutoConfiguration
: 스프링 context 만들 때 자동으로 기능 설정

4. @Configuration
: 클래스에 적용 후 @Bean을 해당 클래스에 적용하면 @Autowired로 호출 가능

5. @Required
: setter 메소드에 적용 시, 필수 프로퍼티

6. @RequestMapping ( = @GetMapping)
:  요청 URL을 어떤 메소드가 처리할 지 매핑

7. @SessionAttributes
: 세션 데이터 관리 (괄호 안에 key값으로 지정된 데이터는 세션으로 지정)

8. @RequestAttribute
: request 에 설정 된 속성값 호출

9. @RequestHeader
: request 의 header값 호출

10. @RequestBody
: request 의 body값 호출

11. @RequestPart
: request로 온 Multipart 값 호출

12. @EnableEurekaServer
: Eureka 서버로 만들어준다

13. @Transactional
: DB 트랜잭션 처리

14. @Cacheable
: 해당 메서드에 지정하면 메서드를 캐시에 적재 후 이후에 호출은 캐시에서 이뤄지며 호출 횟수를 줄여준다.
자원이 많고 자주 변경되지않는 메서드일때 사용.

15. @CachePut
: 캐시 업데이트를 위한 메서드 실행 강제 어노테이션.
지정된 메서드를 항상 호출하며, @Cacheable 과 같이사용하면 안됨.

16. @CacheEvict
: 캐시 데이터를 제거하는 트리거 어노테이션.


