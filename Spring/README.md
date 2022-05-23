# Spring

+ [Spring Framework](#spring-framework)
  + [IoC (Inversion of Contol)]
  + [DI (Dependency Injection)]
  + [AOP (Aspect-Oriented Programming)]
+ [Spring Boot](#spring-boot)

***

## Spring Framework

### IoC (Inversion of Contol)

기존 프로그램은 구현 객체가 스스로 필요한 서버 구현 객첼르 생성하고, 연결하고 실행했다. 구현 객체가 프로그램의 제어 흐름을 스스로 조종했다.

Application Context 등장 이후, 구현 객체는 자신의 로직을 실행하는 역할만 담당한다. 프로그램의 제어 흐름은 **Application Context**가 담당한다.

프로그램의 제어 흐름을 직접 제어하는 것이 아니라, 외부에서 관리하는 것을 **제어의 역전**이라 한다.

#### Framework vs Library

### DI (Dependency Injection)

#### Runtime Dependency vs Compiletime Dependency

의존관계는 실행 시점에 결정되는 동적인 인스턴스 의존관계와 정적인 클래스 의존관계로 분리된다.

정적인 클래스 의존관계(컴파일타임 의존관계)는 애플리케이션을 실행하지 않고 import 코드만 보면 알 수 있다.

동적인 인스턴스 의존관계(런타임 의존관계)는 애플리케이션 실행 시점(런타임)에 실제 생성된 인스턴스가 연결된 의존관계이다.

#### Dependency Injection

애플리케이션 실행 시점(런타임)에 외부에서 실제 구현 객체를 생성하고 클라이언트에 전달해서 클라이언트와 서버의 실제 의존관계가 연결되는 것을 **의존관계 주입**이라 한다.

의존관계 주입덕분에 클라이언트 코드를 변경하지 않고, 클라이언트가 호출하는 대상의 인스턴스를 변경할 수 있다.

정적인 클래스 의존관계를 변경하지 않고, 동적인 객체 인스턴스 의존관계를 변경할 수 있다.

### AOP (Aspect-Oriented Programming)

## Spring Boot

+ 의존성 관리

  'spring-boot-start'을 통해 라이브러리 의존성을 간단하게 관리할 수 있습니다.
  
  기존에는 라이브러리 버전을 각각 입력해야 했지만,
  
  spring-boot-start 라이브러리 덕분에 스프링 및 서드 파티 라이브러리들을 호환되는 버전으로 자동으로 다운로드합니다.
  
+ 자동 설정

  DB, Template 등을 사용하기 위해서 필요한 Datasource, View 등 관련된 설정들을 자동으로 등록해준다.
  
  @SpringBootApplication에 있는 @EnableAutoConfiguration이 그 역할을 한다.

+ 내장 WAS

+ 모니터링


: 스프링 프레임워크 기반 프로젝트를 어려운 설정이나, WAS에 대한 설정 없이 바로 개발에 들어갈 수 있도록 만든 프레임워크이다.

- 스프링 프레임워크를 사용하려면 많은 XML 설정 파일들을 장성해야하고, 기존에 사용했던 설정들을 copy and paste하거나 검색을 통해 일일이 설정을 해야하나 스프링 부트를 사용하면 복잡한 설정 없이 쉽고 빠르게 프레임워크를 사용할 수 있다.
