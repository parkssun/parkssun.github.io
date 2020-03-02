---
title: "TDDStudy-Conference_RefactoringTraining"
date: 2019-04-26 20:20:00
categories: TDD
---
# presenter
- 박재성


 # Refactoring & TDDS
- TDD 내부에는 이미 많은 Refactoring이 존재 따라서, Refactoring과 TDD를 분리시켜서 이야기 하는 것은 옳지 않다.
- TDD와 Refactoring은 연습한다고 잘할수 있을까?!
    - 테스하기 쉬운 코드와 테스트하기 어려운 코드를 분리해서 볼 수 있는 눈
    - 테스트 하기 어려운 코드를 테스트 하기 쉬운 코드로 설계하는 감.
- ComfortZone?
    - 이를 깨는 연습을 해야한다.
    - 명확하고 구체적인 연습을 해야함.
    - 코드리뷰를 할 수 있는 환경, Feedback을 받을 수 있는 환경이 되어야함.
    - 한가지 특정 부분을 개선시키기 위해서 연습, 즉 한번에 너무 많을 것들을 연습하려고 하지 말라.
    - 즉 이런 연습 방법을 설계해야한다.

# 의식적인 연습으로 TDD, Refactoring연습하기.
- TDD와 단위테스트를 만드는 것은 다르다.

## 처음에는 단위 테스트를 만드는 것을 연습하라.
- 즉, 내가 사용하려는 함수에 Input을 만들어서 보내고, Act하게 만든 후, Result를 보고 Assert를 동작하게 하는 sequence를 연습하는게 중요하다.
- 내가 구현하는 메소드 중 Input/ Output이 명확한 클래스 메소드 들에 대한 단위테스트 연습을 해야한다.

## TDD연습
- TDD 책을 읽고 바로 프로젝트에 적용한다?! 거의 필패..
- TDD하고 싶으면 장난감 프로젝트로 시작한다.
- 예를 들어서, 문자열 덧셈 계산기 요구사항.

### 참고. TDD Cycle
- Test Fail : 이거 정확하게 뭔지 모르겠어!!
- Test Pass : Test를 Pass하는 code를 작성
- Refactoring
- Test를 먼저 만들고, 이를 기반으로 Production code를 만든다.
- TDD를 연습할 때는 작은 project로 시작하라.

## Refactoring 연습
- 테스트 코드는 변경하지 말고, 테스트 대상 코드를 개선하는 연습을 한다.

### 메소드 분리
- method가 한가지 일만 하도록 한다.
- 들어쓰기(indent)가 2인 곳은 method분리를 하자.
- else를 쓰지 않도록 노력
- 중간에 Return 할 수 있다면 Return하면 중간에 코드를 읽을 필요 없다.
- local 꼭 필요한지 보고 그렇지 않다면 method에 바로 넣도록 한다.
- 즉, code의 logic이 보이도록 만들고, 궁금하면 들어가서 보도록 만든다.
- 극단적인 연습을 해보자. test가 있기 때문에 Refactoring이 가능하다.
- method 코드라인 수를 줄여보자.

### 클래스 분리
- 모든 원시 값과 문자열을 포장한다.
- 분리 연습을 하기 위해서 활용가능한 원칙
    - 1. 일급 collection을 쓴다.
        - 원시 값들을 가지고 놀수 있도록 이를 클래스화한다.
    - 2. 3개 이상의 인스턴스 변수를 가지는 클래스를 쓰지 않는다.
        - 정량적인 연습을 해보자.

### 장난감 프로젝트 난이도 높이자.
- 게임과 같은 입력과 출력이 명확한 코드
- 의존관계가 없는 프로그램
- 약간의 로직이 있는 프로그램
- 예
    - 로또
    - 사다리 타기
    - 볼링게임점수
    - 체스게임
    - 지뢰찾기 게임
### 의존관계 추가를 통한 난이도 높이기.
- 이게 실질적인 우리 회사에서의 프로젝트

### 한 단계 더 나아가는 방법
- 컴파일 에러를 최소화 하면서 리팩토링하기
- ATDD 기반으로 응용 애플리케이션 개발하기
- legacy code에 testcode 적용하기.
- 유지보수 역량이 좋은 사람이 되어야 한다.
-