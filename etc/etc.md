# 기타 CS 지식들 정리

- [TDD란?](#TDD)
- [BDD란?](#BDD)
- [TDD와 BDD 차이](#TDD와_BDD_차이)
- [DDD](#DDD) 


## TDD

- TDD(Test Driven Development, **테스트 주도 개발**)

반복 테스트를 이용한 소프트웨어 방법론으로, 작은 단위의 테스트 케이스를 작성하고 이를 통과하는 코드를 추가하는 단계(피드백)를 반복하여 구현한다.
짧은 개발 주기의 반복에 의존하는 개발 프로세스이며 애자일 방법론 중 하나인 eXtream Programming(XP)의 'Test-First' 개념에 
기반을 둔 단순한 설계를 중요시한다.

> - TDD 개발 방식의 장점
>   - 보다 튼튼한 객체 지향적인 코드 생산
>   - 재설계 시간의 단축
>   - 디버깅 시간의 단축
>   - 테스트 문서의 대체 가능
>   - 추가 구현의 용이함
> - TDD 개발 방식의 단점
>   - 생산성의 저하
>   - 기존의 개발 방식에서 벗어난 TDD 방법을 따로 학습 필요

참고 : [[기술면접] TDD(Test-Driven-Development) 방법론에 대해서](https://wooaoe.tistory.com/33)

### BDD 

- BDD(Behavior Driven Development, **행위 주도 개발**)

TDD를 근간으로 파생된 개발 방법으로 TDD에서 한 발 더 나아가 테스트 케이스 자체가 요구 사항이 되도록 하는 개발 방법이다.
BDD를 통해 개발을 하게 된다면 테스트 메소드의 이름을 "이 클래스가 어떤 행위를 해야 한다(should do something)" 와 같은 식으로 정의한다.

- BDD의 기본 개발 패턴

BDD는 시나리오를 기반으로 테스트 케이스를 작성하며 함수 단위 테스트를 권장하지 않는다. 이때 시나리오는 개발자가 아닌 사람이 봐도 이해할 수 있을 정도의 수준을 권장한다.

- **Feature** : 테스트에 **대상의 기능/책임을 명시**한다.
- **Scenario** : 테스트 **목적에 대한 상황을 설명**한다.
- **Given** : 시나리오 **진행**에 **필요한 값을 설정**한다.
- **When** : 시나리오를 **진행**하는데 **필요한 조건을 명시**한다.
- **Then** : 시나리오를 **완료**했을 때 **보장해야 하는 결과를 명시**한다.

따라서 _테스트 대상은 A 상태에서 출발하며(**Given**) 어떤 상태를 가했을 때(**When**) 기대하는 상태로 완료되어야 한다(**Then**)._

참고 : [BDD (Behaviour-Driven Development)에 대한 간략한 정리](https://www.popit.kr/bdd-behaviour-driven-development%EC%97%90-%EB%8C%80%ED%95%9C-%EA%B0%84%EB%9E%B5%ED%95%9C-%EC%A0%95%EB%A6%AC/)

### TDD와_BDD_차이

![image](https://user-images.githubusercontent.com/22315365/137946254-1eb7ae96-c06a-4771-aa57-58472e302bf1.png)

참고 : [kotest가 있다면 TDD 묻고 BDD로 가!](https://if.kakao.com/session/106)

### DDD

- DDD(Domain Driven Design, **도메인 주도 설계**)


