# Spring

+ [Spring Framework](#spring-framework)
  + [IoC (Inversion of Contol)]
  + [DI (Dependency Injection)]
  + [AOP (Aspect-Oriented Programming)]

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
