# 자바 정리

- [직렬화란?](#직렬화)
- [serialVersionUID란?](#serialVersionUID)


## 직렬화

- **직렬화(Serialization)**

직렬화란 객체를 데이터 스트림으로 만드는 것으로 객체에 저장된 데이터를 스트림에 쓰기(write)위해 연속적인(serial) 데이터로 변환하는 것
반대로 스트림으로부터 데이터를 읽어서 객체를 만드는 것을 역직렬화(deserialization)라고 한다.

```
직렬화 : 객체 -> 바이트 스트림 데이터
역직렬화 : 바이트 스트림 데이터 -> 객체
```

>객체는 클래스에 정의된 인스턴스 변수의 집합으로 메서드가 포함되지 않는다.

## serialVersionUID

serialVersionUID는 클래스를 직렬화한 클래스 버전의 고유 값으로 직렬화 또는 역직렬화를 할 때 serialVersionUID로 해당 클래스의 특정 버전이 맞는지 아닌지를 판단할 때 사용한다.
같은 클래스여도 클래스 내부 값이 변경되면 클래스 버전을 나타내는 serialVersionUID 값도 변경된다.

>serialVersionUID를 선언하지 않으면 JVM에서 default로 값을 자동 생성한다.
>따라서 선언하지 않아도 문제 없지만 컴파일러에 의해 예상치 못한 값이 발생할 수 있어 명시적으로 serialVersionUID 값을 선언하는 것을 권장한다.



참고 : 
- 자바의 정석 3rd Edition Chapter 15. 입출력 I/O
- [자바 직렬화(serialize)란? serialVersionUID 란?](https://velog.io/@hellonewtry/%EC%9E%90%EB%B0%94-%EC%A7%81%EB%A0%AC%ED%99%94%EB%9E%80-serialVersionUID-%EB%9E%80)
