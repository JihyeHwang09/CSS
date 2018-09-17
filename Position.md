## `position`: `static` | `relative` | `absolute` | `sticky` | `fixed`;

## 기본값(default): static

###`static`
- 일반적인 흐름(normal flow)를 따라 배치된다.
- `top`, `right`, `bottom`, `left`, `z-index` 속성들이 효과를 주지 X.

###`relative`
- 일반적인 흐름(normal flow)를 따라 배치된다.
- 요소 자신에 대한 상대적인 `top`, `right`, `bottom`, `left`속성에 의한 좌표로 배치된다.
- ** relative에 별도의 거리 속성을 주지 X경우 -> static과 동일하게 동작한다. **
- 요소의 좌표는 다른 요소들의 위치에 영향을 주지 X.
- `z-index`의 값이 auto가 아닐 경우 -> 새로운 statcking context를 만든다. 


###`absolute`
- 일반적인 문서 흐름에서 제거된다.
- 페이지 레이아웃 요소에 대한 공간이 생성되지 X.
1. **가장 가까운 위치에 있는 조상에 대해 상대적 위치로 배치된다.**
2. 그렇지 않으면 -> 초기 컨테이닝 블록을 기준으로 배치된다.
- 최종 위치는 `top`, `right`, `bottom`, `left`값에 의해 결정된다.
- `z-index`의 값이 auto가 아닐 경우 -> 새로운 statcking context를 만든다. 
- 절대적으로 배치된(positioned) 박스들은 마진을 가질 수 있으며, 다른 마진에 의해 망가지지 X.

###`fixed`
- 요소가 일반적인 문서 흐름에서 제거된다.
- 페이지 레이아웃에서 요소에 대한 공간이 생성되지 X.
- 스크린의 '뷰포트(viewport)를 기준으로 한 위치'에 배치된다.<br>
  -> 스크롤되어도 움직이지 않는 고정된 자리를 갖게 된다.
- 최종 위치는 `top`, `right`, `bottom`, `left`값에 의해 결정된다.<br>
  -> 이 값은 항상 새로운 stacking context를 생성한다.
- 조상의 `transform` 속성이 **none이 아닌 다른 것으로 설정되면**, <br>
  그 조상은 뷰포트 대신, 컨테이너로 사용된다. 


###`sticky`
- 요소가 일반적인 문서 흐름에 따라 배치된다.
- 그런 다음 `top`, `right`, `bottom`, `left`값을 기준으로 <br>
  플로우 루트(flow root) 및 해당 요소를 포함하는 블록(containing block)에 대한 <br>
  상대적(relative) 위치에 자리하게 된다.
- 이 오프셋은 다른 요소들에 영향을 주지 X.
- 항상 새로운 stacking context를 생성한다.
- 테이블과 관련된 요소들에 미치는 `sticky`의 효과는 동일하다.
- 브라우저 사양에 따라 overflow: hidden 또는 auto 요소 내에서 작동하지 않을 수 있다.
