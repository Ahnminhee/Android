## Context 정의
- Application 환경에 대한 전역 정보를 접근하기 위한 인터페이스
- Context를 통해 어플리케이션에 특화된 리소스나 클래스에 접근 가능
- Activity 실행, Intent 브로드캐스팅 그리고 Intent 수신 등과 같은 프로그램 수준의 작업을 수행하기 위한 API 호출 가능
    -> API: startActivity(), bindService()와 같은 메소드

## Context 역할
- 어플리케이션과 관련된 정보에 접근  -> 정보 관리: ActivityManagerService
- 어플리케이션과 관련된 시스템 레벨의 함수 호출

자신이 어떤 어플리케이션을 나타내고 있는지 알려주는 ID 역할
ACtivityManagerService에 접근할 수 있는 통로 역할

## Context 종류
1. Application Context
- Application 생명주기에 영향을 받음
2. Activity Context
- Activity 생명주기와 함께 동작해 onDestroy()와 함께 사라짐
- Activity 환경 정보를 담고 있고 Context에 Intent를 통해 다른 액티비티를 띄우면 스택이 쌓임
