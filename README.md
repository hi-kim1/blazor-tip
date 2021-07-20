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

#### 모델
데이터 액세스가 모델을 통해 수행됩니다. 모델은 엔터티 클래스 및 데이터베이스와의 세션을 나타내는 컨텍스트 개체로 구성됩니다. 컨텍스트 개체를 사용하여 데이터를 쿼리하고 저장할 수 있습니다.
     
▪️ &nbsp; 기존 데이터베이스에서 모델을 생성합니다.    
▪️ &nbsp; 데이터베이스와 일치하는 모델을 직접 코딩합니다.    

```csharp
using System.Collections.Generic;
using Microsoft.EntityFrameworkCore;

namespace Intro
{
    public class BloggingContext : DbContext
    {
        public DbSet<Blog> Blogs { get; set; }
        public DbSet<Post> Posts { get; set; }

        protected override void OnConfiguring(DbContextOptionsBuilder optionsBuilder)
        {
            optionsBuilder.UseSqlServer(
                @"Server=(localdb)\mssqllocaldb;Database=Blogging;Integrated Security=True");
        }
    }

    public class Blog
    {
        public int BlogId { get; set; }
        public string Url { get; set; }
        public int Rating { get; set; }
        public List<Post> Posts { get; set; }
    }

    public class Post
    {
        public int PostId { get; set; }
        public string Title { get; set; }
        public string Content { get; set; }

        public int BlogId { get; set; }
        public Blog Blog { get; set; }
    }
}
```
