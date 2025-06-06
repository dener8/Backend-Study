### 1부 소개

프로그램을 동작하게 만드는 일은 어린 고등학생도 할 수 있는 일이다. 하지만 동작하게 만드는건 누구나 할 수 있지만 제대로 만드는 일은 전혀 다르다.

### 1장 설계와 아키텍처란

설계, 아키텍처는 둘이 큰 구분이 없는데, 아래처럼 보통 사용함

- 아키텍처: 저수준의 세부사항과는 분리된 고수준의 무언가
- 설계: 저수준의 구조, 결정사항

저수준의 세부사항과 고수준의 구조는 모두 소프트웨어 전체 설계의 구성요소임

소프트웨어 아키텍처의 목표는 필요한 시스템을 만들고, 유지보수하는데 투입되는 인력을 최소화하는게 목적

보통 프로젝트를 진행하면 인력은 지수적으로 투입되지만, 생산성은 지수적으로 낮아지게 된다.

하지만 개발자는 이전 코드를 리팩토링을 하는 일은 잘 일어나지 않는데, 계속해서 다음에 만들어야할 기능이 생기기 때문이다.

제이슨 고먼이라는 사람이 6일동안 실험을 하나 했는데, 정수를 로마 숫자로 변환하는 프로그램을 만들었음. 이때 차이점은 하루마다 TDD 적용하고, 다음날은 TDD를 적용하지 않는 날의 차이였는데, TDD를 적용한 날이 TDD를 적용하지 않은 날보다 10% 더 빠르다는 것을 확인했음 (이건 TDD가 숙련된 사람의 기준으로 보임)

여기서 이야기하고 싶은 점은 ‘빨리 가는 유일한 방법은 제대로 가는 것이다’라는 점이니 ‘자신을 과신하지 말라는 점’

### 2장 두 가지 가치에 대한 이야기

소프트웨어 개발자는 행위, 구조에 대한 가치를 높게 유지해야하는 책임을 지님. 하지만 현실의 개발자는 하나의 가치에만 집중하는데, 하필 덜 중요한 가치에 집중하는 경향이 있음

- 행위: 프로그래머는 이해관계자가 기능명세서나 요구사항 문서를 구체화할 수 있도록 도움. 많은 프로그래머들이 기능명세서랑 문서 가지고 구현하고, 버그를 수정하는 일만이 자신의 작업이라고 믿는데 틀림
- 아키텍처(구조): 소프트웨어는 부드러움을 지니도록 만들어졌는데, 이 말은 변경하기 쉬워야 한다는 말임 (변경하기 쉽지 않다면 그게 하드웨어랑 무슨 차이가 있을까), 이해관계자는 범위가 비슷한 변경사항을 제시하지만, 개발자는 이해관계자가 퍼즐 조각을 맞추라는 지시로 느껴지는데, 이건 시스템의 형태와 요구사항의 형태가 서로 맞지 않기 때문임. 이때 문제는 당연히 아키텍처이고, 아키텍처는 ‘형태’라는 단어에 독립적이야함

소프트웨어의 가치

- 행위는 긴급하지만 매번 높은 중요도를 가지는 것은 아니다
- 아키텍처는 중요하지만 즉각적인 긴급성을 필요로 하는 경우는 절대 없다

→ 어떤 일은 긴급하면서 중요할 수도 있지만, 긴급하지 않고 중요하지도 않은 일이 있을 수도 있음

그래서 아래처럼 우선 순위를 매겨볼 수 있다.

1. 긴급하고 중요한
2. 긴급하지 않지만 중요한
3. 긴급하고 중요하지 않은
4. 긴급하지 않지만 중요하지 않은

여기서 1, 3은 행위일 것이고, 아키텍처는 2, 4일 것이다.

그래서 긴급성이 아닌 아키텍처의 중요성을 설득하는 일(2순위)도 개발팀이 마땅이 책임져야 한다.

아키텍처를 위해 투쟁하라. 개발자는 아키텍처를 안전하게 보호할 책임이 있다.

(나중가서 구조적으로 고치는데 오래 걸린다는 시간을 이야기하기보다, 미리미리 아키텍처 개선을 하겠다고 짧은 시간을 여러번 가져가는게 더 중요하다고 생각하는 것 같음)
