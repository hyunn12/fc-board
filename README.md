# fc-board


## usecase 작성

- 액터와 유즈케이스 사이는 연관 관계(직선)으로 표기
- 유즈케이스와 유즈케이스 사이는 포함, 확장 관계(점선)으로 표기

### 관계 종류

#### include 포함관계
- 하위 기능이 상위 기능에 포함됨을 의미
- 점선으로 표기, 화살표는 상위 -> 하위

``` mermaid
flowchart LR
    Login -. <<`include>> .-> Auth
```

#### extend 확장관계
- 상위기능이 일어남으로서 일어날 수 있는 여러가지 분기 중 하나임을 의미
- 점선으로 표기, 화살표는 하위 -> 상위

``` mermaid
flowchart RL
    Login_Fail -. <<`extend>> .-> Login
```
