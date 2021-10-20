# 디자인 패턴 정리

- [SOLID 설계 원칙](#SOLID)
  - [SRP](#SRP)
  - [OCP](#OCP)
  - [LSP](#LSP)
  - [ISP](#ISP)
  - [DIP](#DIP)

- [행동 패턴](#행동_패턴_Behavioral_Patterns)
  - [전략 패턴](#전략_패턴)

## SOLID

### SRP

- **단일 책임 원칙** (Single Responsibility Principle, **SRP**) 이란? 

**클래스는 단 한 개의 책임을 가져야 한다.**<br>

클래스가 여러 책임을 갖게 되면 그 클래스는 각 책임마다 변경되는 이유가 발생하기 때문에 한 개의 책임만 가져야 한다.
다른 말로 *"클래스를 변경하는 이유는 단 한 개여야 한다."*

> 단일 책임 원칙을 어긴다면..
> 1. 코드 변경 사항이 발생할 시에 갖고 있는 책임의 수만큼 변경사항이 비례하여 증가한다.
> 2. 클래스의 재사용이 어렵다.

### OCP

- **개방-폐쇄 원칙** (Open-Closed Principle, **OCP**)

**확장에는 열려 있어야 하고, 변경에는 닫혀 있어야 한다.**

즉

- 기능을 변경하거나 확장할 수 있으면서
- 그 기능을 사용하는 코드는 수정하지 않는다.


### LSP

- **리스코프 치환 원칙** (Liskov Substitution Principle, **LSP**)

### ISP

- **인터페이스 분리 원칙** (Interface Segregation Principle, **ISP**)

### DIP

- **의존 역전 원칙** (Dependency Inversion Principle, **DIP**)

## 행동_패턴_Behavioral_Patterns

### 전략_패턴

- 전략(Strategy) 패턴이란?

실행 중에 알고리즘을 선택할 수 있게 하는 행위로 전략 패턴은 알고리즘을 사용하는 클라이언트와는 독립적으로 다양하게 만들고
유연하고 재사용 가능한 객체를 설계하기 위해 만들어진 소프트웨어 디자인 패턴 개념이다.

전략 패턴은 다음의 특징이 있다.

- 특정한 계열의 알고리즘들을 정의하고
- 각 알고리즘을 캡슐화하며
- 이 알고리즘들을 해당 계열 안에서 상호 교체가 가능하게 만든다.


참고 : 

- 개발자가 반드시 정복해야 할 객체 지향과 디자인 패턴
- [위키백과-전략패턴](https://ko.wikipedia.org/wiki/%EC%A0%84%EB%9E%B5_%ED%8C%A8%ED%84%B4)
- [위키백과-디자인패턴(책)](https://ko.wikipedia.org/wiki/%EB%94%94%EC%9E%90%EC%9D%B8_%ED%8C%A8%ED%84%B4_(%EC%B1%85))



