# 데이터베이스 정리

- [트랜잭션이란?](#트랜잭션)
- [트랜잭션 ACID 특징](#트랜잭션_특징)
- [분산 데이터베이스란?](#분산_데이터베이스)
- [분산 데이터베이스 CAP 속성](#분산_데이터베이스_CAP_속성)


## 트랜잭션

- **트랜잭션(Transaction)** 이란?

트랜잭션은 한 단위를 이루는 일련의 연관된 데이터베이스 조작을 의미한다.
한 트랜잭션에 속하는 작업 중 하나라도 실패하면 트랜잭션 전체가 실패한 것으로 간주하여
그 트랜잭션에서 데이터베이스를 변경한 내용을 전부 원래대로 되돌려 놓는다(이를 롤백(=rollbcak)이라고 부른다). 
반대로 모든 작업이 성공적으로 처리되면 모든 변경 내용을 한꺼번에 반영시킨다(이를 커밋(=commit)이라고 부른다.).

## 트랜잭션_특징

- **원자성(Atomicity)** : 트랜잭션에 포함되는 모든 작업이 성공적으로 처리되지 않으면 트랜잭션에 있는 어떤 작업도 처리되지 않아야 한다.
- **일관성(Consistency)** : 트랜잭션은 트랜잭션이 시작되기 전과 트랜잭션이 종료된 후에 데이터베이스가 올바르고 일관된 상태가 되도록 처리되어야 한다. 
예를 들어, 참조 무결성이 깨지거나 하는 일이 일어나면 안 된다.
- **고립성(Isolation)** : 한 트랜잭션에서 데이터베이스를 변경한 내용은 트랜잭션이 커밋될 때까지 다른 어떤 질의나 트랜잭션과도 고립되어야만 한다.
- **영속성(Durability)** : 일단 커밋이 되고 나면 트랜잭션에 의해 변경된 내용은 영구적이어야 한다. 
데이터베이스 시스템은 데이터베이스의 현재 상태가 유실되지 않도록 시스템 충돌 등의 문제로부터 복구할 수 있는 방법을 갖추고 있어야 한다.

## 분산_데이터베이스

데이터베이스와 데이터 집합이 커질수록 대부분 분산형으로 가게 된다.
즉 데이터가 네트워크로 연결된 여러 위치에 저장된다. 분산 데이터베이스에는 중복성과 지연 시간(=latency) 감소 및 상황에 따른 비용 절감 같은 장점이 있다.
따라서 실무에 쓰이는 분산 데이터베이스는 여러 노드로 구성되며 서로 다른 데이터 센터에 나눠져 있는 경우도 많다.

## 분산_데이터베이스_CAP_속성

모든 분산 데이터베이스에는 시간 지연이 있으며 연결이 끊어지는 경우도 종종 있다. 따라서 완벽한 시스템은 동시에 모두 충복할 수는 없고 아래의 CAP 속성 중 두개의 속성만 만족할 수 있다.

- **일관성(Consistency)** : 모든 읽기 작업에서는 가장 최근에 쓰여진 것을 반환한다. 예를 들어 분산 은행 업무 애플리케이션이 있는데 최근에 어떤 노드에서 계좌에 입금을 했다면
다른 어떤 노드에서 읽기 작업을 하든 가장 최근의 계좌 잔고가 반영되어 있어야 한다.
- **접근성(Accessibility)** : 모든 요청에 대해 응답이 따른다. 하지만 반드시 가장 최근에 쓰인 내용이 반영되는 것은 아니다. 예를 들어, 어떤 분산 은행 업무 애플리케이션에서
언제 어느 노드에 대해 계좌 정보에 대한 질의를 하든 그 질의에 대한 응답을 받아볼 수 있다. 하지만 반드시 그 계좌의 최신 잔고 값을 받지는 못할 수도 있다.
- **구분성(Partitionability)** : 시스템을 노드로 구분할 수 있으며 네트워크 상의 노드 사이에서 데이터가 유실되더라도 시스템은 계속 제 기능을 한다.
예를 들어, 분산 은행 업무 애플리케이션에서 일부 노드가 다운되더라도 시스템 전체는 여전히 작동한다.

참고 : 프로그래밍 면접 이렇게 준비한다 4판