<h2 style="background-color: #266DFC; color: #ffffff; padding: 0.5em;"> MVVM ➰</h2>


### MVVM의 특징
---

**Model-View-ViewModel**, 세 구성 요소로 구분할 수 있는 소프트웨어 아키텍쳐 패턴 
-  `Model`은 애플리케이션과 비즈니스 로직을 담당 
-  `View`는 사용자 인터페이스, 즉 UI를 담당 
-  `ViewModel`은 View ~ Model 사이의 연결고리로 View에 표시될 데이터와 명령을 준비하며 Model로부터 데이터를 받아 View가 표시할 수 있게한다.


### MVVM의 장점
---
1. **데이터 바인딩**을 통해 View와 ViewModel 간의 동기화를 처리함으로써 UI와 비즈니스 로직을 분리하여 앱의 **유지보수성과 테스트 용이성**을 높인다.
2. 명령 패턴(요청을 객체 형태로 캡슐화) 통해 사용자 인터랙션을 로직으로부터 분리하고, 유연하게 동작하게 할 수 있다.


### MVVM의 단점
---
1. MVC, MVP와 같은 간단한 패턴에 비해 학습하기 어려울 수 있다.
2. 대규모 데이터 세트를 다루는 애플리케이션과 같은 경우, 최적화를 고려하지 않으면 성능 저하가 발생할 수 있다.
3. 애플리케이션의 규모가 작을 경우, 맞지 않은 과도한 추상화일 수 있다.


### MVC와 MVVM의 차이 (+MVP)
---
컴포넌트 간의 상호작용 방식에서 차이가 존재한다.
<br>

<h5 style="background-color: #266DFC; color: #ffffff; padding: 0.5em;"> MVC</h5>
- Model : 애플리케이션의 데이터를 관리 
- View : 사용자 인터페이스 담당 
- Controller : Model과 View 사이를 연결하는 역할. 사용자의 이벤트에 반응하며 Model을 업데이트 및 View 재랜더링 

<h5 style="background-color: #266DFC; color: #ffffff; padding: 0.5em;"> MVVM</h5>
-  Model: 애플리케이션과 비즈니스 로직을 담당 
-  View: 사용자 인터페이스, 즉 UI를 담당 
-  ViewModel: View ~ Model 사이의 연결고리로 View에 표시될 데이터와 명령을 준비하며 Model로부터 데이터를 받아 View가 표시할 수 있게한다.

<h5 style="background-color: #266DFC; color: #ffffff; padding: 0.5em;"> MVC</h5>
- Model: 데이터와 비즈니스 로직 처리 
- View : 사용자 인터페이스 표시 
- Presenter : 뷰와 모델 사이의 중간 역할
- Interface : View ~ Presenter 사이의 결합을 유지 

MVVM은 **Controller 대신 ViewModel**이 Model과 View를 연결하는 역할을 하며, **데이터 바인딩을 통한 동기화를 자동화**함으로써 Controller의 작업량보다 더 효율적이라 할 수 있다.

### MVVM 패턴의 ViewModel과 AAC에서의 ViewModel의 차이점 
---

<h5 style="background-color: #266DFC; color: #ffffff; padding: 0.5em;"> MVVM의 ViewModel</h5>
1. View - Model 사이의 매개체 역할
2. View에 보여지는 데이터를 가공 <br>
<h5 style="background-color: #266DFC; color: #ffffff; padding: 0.5em;"> AAC의 ViewModel</h5>
1. 앱의 LifeCycle을 고려하여 UI 관련 데이터를 저장하고 관리
2. 화면 회전 시에도 데이터 보존 가능
