# blazor-tip
## 업데이트 예정 목록
 * 수명주기
 * Entity Framework
 * Dependency Injecttion(종속성 주입)
 * Scaffolding
 * Cascading

## 수명주기
1. **SetParametersAsync**
1. **OnInitializedAsync**
1. **OnParametersSetAsync**
1. **OnAfterRenderAsync(bool firstRender)**

SetParametersAsync → OninitialzedAsync → OnParametersSetAsync 이 순서대로 구성요소를 호출 한뒤 Render 요소를 위한 OnAfterRenderAsync가 호출이 되는데
이 4가지 수명주기 메서드에 대해 알아봅시다.

#### SetParametersAsync
▪️ &nbsp; 렌더링 트리에서 구성 요소의 부모에 의해 제공 되는 매개 변수를 설정 합니다.    
▪️ &nbsp;     
▪️ &nbsp;     
▪️ &nbsp;     

## Entity Framework
#### _Entity Framework란?_
C#과 같은 객체 지향형 프로그래밍 언어에서 데이터베이스를 쉽게 사용하기 위한 도구로 객체와 관계형 DB의 테이블을 매핑하여 (ADO.NET에서처럼 별도의 SQL 쿼리를 작성하지 않고도) 쉽게 데이터를 액세스할 수 있게 합니다.
