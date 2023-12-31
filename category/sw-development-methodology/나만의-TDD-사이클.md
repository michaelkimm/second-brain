
## 나만의 TDD 사이클 단계

### 전체 사이클
인수 테스트 -> (선택)서비스 테스트 -> 도메인 테스트

### 개별 사이클

```
1. 문제 정의 후, 요구 사항 분석
    - 📋 문제 정의: 필요한 기능을 한 문장으로 요약하기
    - 📋 요구 사항 분석: given/when/then 프레임 사용
2. 테스트 조건(해피 케이스) 주석으로 정의
    - 예외 케이스 생각나면 그때 그때 정리
3. 테스트 작성
4. 테스트 통과하는 로직 작성
    - (유연) TDD 사이클 대로라면 1~3 반복 후 최소 단위 모듈에서 4번을 시작해야함.
    - ✅ 비즈니스적인 의미 & 테스트 유용성을 고려하여 특정 레이어의 모듈은 1~3 skip
    - '내가 아는 것' -> '모르는 것' 방향으로 진행.
      - ❗ 내가 아는 것: 객체의 책임과 역할 등
      - ❓ 내가 모르는 것: 구현 방식 등
5. 리팩토링 진행
    - 우선순위: (1)재사용성, (2)가독성
    - 가독성
      - 💥 기능을 '명세'하는 역할을 하는가
      - 💥 읽는 사람을 고려하여 작성했는가(ex. 기획자, 개발자 등)
6. 예외 케이스 고려
    - 1~5번 반복
    - 🌟 예외 상황
      - request 데이터 누락(인증 정보)
      - 논리적 오류 check(비즈니스 규칙에 근거)
      - 시스템 오류 check(서버 down, memory 이슈 등)
7. 성능 고려
    - 1~6번 반복
    - ⏰ 데이터를 효율적으로 읽는가
    - ⏰ 데이터를 효율적으로 쓰는가
```

_* '5. 시스템 오류 check'와 '7. 성능 고려'는 개발 경험이 쌓임에 따라 1번에서 진행되도 함._