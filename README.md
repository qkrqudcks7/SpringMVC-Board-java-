# :baby_chick: Spring Framework springMVC


## :question: Spring Framework란?

- 자바 플랫폼을 위한 오픈소스 애플리케이션 프레임워크로서 엔터프라이즈급 애플리케이션을 개발하기 위한 모든 기능을 종합적으로 제공하는 경량화된 솔루션.
- Spring Framework는 경량 컨테이너로 자바 객체를 담고 직접 관리한다. 객체의 생성 및 소멸 그리고 라이프 사이클을 관리하며 언제든지 Spring 컨테이너로 부터 필요한 객체를 가져와 사용할 수 있다.

### :question: IOC 기반(Inversion of Control, 제어의 역전)

- 자신의 모든 권한을 framework에 위임한다. 즉 제어의 흐름을 사용자가 갖는 것이 아니라 framework가 갖는 것.
- 객체의 생성부터 생명주기 등 모든 객체에 대한 제어권을 넘긴 것.

:grey_exclamation: IOC 구성요소

<br> 1. DI(Dependency Injection) 의존성 주입 </br>

- 객체가 서로 의존하는 관계가 되도록 의존성을 주입하는 것.
- 각 클래스 사이에 필요로 하는 의존관계를 빈 설정 정보를 바탕으로 컨테이너가 자동으로 연결해 주는 것.

<br> 2. DL(Dependency Lookup) 의존성 검색 </br>

- 컨테이너에서 제공하는 api를 이용하여 사용하고자 하는 빈을 검색하는 것


<hr>


## :fire: Spring Framework 특징

### :star: POJO (Plain Old Java Object)

- getter/setter를 가진 단순 자바 오브젝트
- 의존성이 없고 테스트 및 유지보수가 편리하다
- 다양한 설계과 구현이 가능하다.

### :star: AOP (Aspect Oriented Programming)

- 관점 지향 프로그래밍, 어떤 로직을 기준으로 핵심적인 관점, 부가적인 관점으로 나누어서 보고 그 관점을 기준으로 각각 모듈화 하는 것.
- 중복 되는 코드를 제거 할 수 있고, 공통 기능 하나의 수정으로 모든 핵심 기능들의 공통 기능을 수정 할 수 있어 효율적인 유지보수가 가능하며 재활용성이 극대화됨.
- 반복되는 코드를 Aspect로 모듈화하고 핵심적인 비즈니스 로직에서 분리하여 재사용하는 것.

 Aspect : 중복 된 코드들을 모듈화 한 것. ex) 트랜잭션 , 보안
 
 Target : Aspect를 적용하는 곳. ex) 클래스, 메소드
 
 Advice : 실질적으로 부가기능을 담은 구현체
 
 JointPoint : Advice가 적용될 위치. ex) 메소드 진입 지점, 생성자 호출 시점
 
 PointCut : JointPoint의 상세한 스펙을 정의한 것. 
 
 Weaving : PointCut에 의해 결정된 Target의 JoinPoint에 Advice를 삽입하는 과정
 
 ### :question: Spring AOP
 
 - 프록시 패턴 기반의 AOP구현체.
 - 스프링 Bean에만 AOP를 적용 가능.
 - 모든 AOP의 기능을 제공하지 않고, 스프링 IoC와 연동해 엔터프라이즈 애플리케이션의 각종 문제(중복 코드, 객체 관계간 복잡도)에 대한 해결책을 지원하는 것이 목적.
 
 :question: 프록시 객체란?
 
 - 핵심 기능의 실행은 다른 객체에 위임하고 부가적인 기능을 제공하는 객체이다.
 - 핵심 기능은 구현하지 않고, 여러 객체에 공통으로 적용할 수 있는 기능을 구현한다.
 
