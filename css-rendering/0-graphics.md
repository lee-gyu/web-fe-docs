# Ch.0 Graphics

- Refs.
    - <https://www.youtube.com/watch?v=_o1zsrBkZyg&list=PLBNdLLaRx_rKXwi7MulM6v1UG9JLKWIYS>

그래픽스 시스템은 결국 화면 상의 픽셀을 어떻게 그리는가에 대한 문제이다.\
x, y, width, height, color이게 전부이다.

## Fixed Number

직접 어떤 위치에 무엇을 그릴지를 다 결정하면, 쉽게 그릴 수 있지만, 화면 크기가 달라지면 문제가 발생한다.\
고정된 상수 값은 디바이스나 환경에 적응적으로 변화할 수 없다.\
이를 해결하기 위해 상대적인 계산 식이 적용되는 스타일을 사용한다. (Abstract Calculator)

`%`, `LEFT`, `BLOCK`, `INLINE`, `FLOAT`

Abstract Calculator > Components > Framework

- Framework (html graphics 체계 전체)
- Components (img, input,,,)
- Abstract Calculator (실제 계산되는..)

상대적으로 용어를 생각해야한다. Framework라는 것은 맥락에 따라 다르게 의미를 생각하면 된다.\
외국 문화에서 만들어진 용어를 절대적인 의미를 지닌 것으로 생각하면 이해가 어렵다.

## Rendering System

어떠한 대상을 원하는 모습으로 출력하는 체계 (그래픽으로 보여줘, JSON 형태로 보여줘 등)

- Geometry Calculate (지역을 계산, x, y, width, height)
    - reflow
- Fragment Fill (색칠하기)
    - repaint
- 영역을 나눈 뒤, 채운다.

휴대폰 디스플레이 입장에서는 브라우저 창 안에서 스케일링이 되기 때문에 px ratio가 디바이스마다 다를 수 있다.

## CSS Specifications

right으로 배치하는 것은, 부모의 width에서 자식의 width를 뺀 값을 x로 쓰는 것이다.\
이런 것을 추상적으로 해주는 것이 CSS이다. (text-align: right)\
CSS는 굉장히 풍부한 계산 체계를 추상적으로 제공한다. (overflow, 100%, float, position...)

CSS의 추상적인 것이 구체적으로 어떻게 계산되는지를 안다면 더 많은 것을 이해하며 레이아웃을 설계할 수 있다.\
구체적으로 개발이 가능한 사람. 오랫동안 개발이 가능.\
대충 개발이 가능한 사람. 항상 새로운 신규 개발자로 대체될 수 있음.

현대의 CSS는 다른 그래픽스 시스템에서 효율적인 것들을 차용해서 현재는 굉장히 복잡한 시스템이 되었다.

CSS 표준 사양서를 보면, 어떤 것이 어떻게 계산되는지를 알 수 있다. (모든 브라우저는 이 사양서를 따라야 하므로.)

### CSS Level 1

- 고작 A4 한 장 분량

### CSS Level 2

다양한 벤더들이 각자의 방식으로 구현하다가, W3C에서 표준을 만들었다.\
MS가 IE로 세상을 지배할 때의 시기

### CSS Level 2 + Module (각 사양 내용을 모듈화)

### CSS Level 2.1

특정 팀에서 Level 3 Module 포함시켜버림... 그런데 Level 3로 넘어가기엔 힘든 부분이 많았다고 판단함 (color3, text3 등)

### Module Level

신규 사양을 만들고, level 1로 만듦.\
CSS는 너무 난잡하고, 브라우저마다 특이함.\
CSS의 모든 것을 다 아는 것은 불가능하다고도 볼 수 있음.

- transforms 1 (level1, 2 등을 지원하는지 봐야함)
- masking 1
- flex-box 1

## 다른 사양

- w3c (w3c Community And Business Groups) - <https://www.w3.org/community/>
- WICG (Web Platform Incubator Community Group) - Google 주 멤버 Chromium에 강력하게 영향을 미침
- RICG (Responsive Issues Community Group)
- 커뮤니티에서 만들어서 w3c에 draft로 제출. 브라우저사는 해당 스펙을 구현하기도 함 (구글, 애플, 모질라, MS 등)
