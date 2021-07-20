# blazor-tip
## 업데이트 예정 목록
 * 수명주기
 * Entity Framework
 * Dependency Injecttion(종속성 주입)
 * Scaffolding
 * Cascading

### 1. 수명주기
1. **SetParametersAsync**
1. **OnInitializedAsync**
1. **OnParametersSetAsync**
1. **OnAfterRenderAsync(bool firstRender)**

SetParametersAsync → OninitialzedAsync → OnParametersSetAsync 이 순서대로 구성요소를 호출 한뒤 Render 요소를 위한 OnAfterRenderAsync가 호출이 되는데
이 4가지 수명주기 메서드에 대해 알아봅시다.

#### SetParametersAsync
▪️ &nbsp; 렌더링 트리에서 구성 요소의 부모에 의해 제공 되는 매개 변수를 설정 합니다.
▪️ &nbsp;a
▪️ &nbsp;a
