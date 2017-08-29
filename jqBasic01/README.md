
jQuery Study Step01
=====

## jQuery

* 자바스크립트 라이브러리
* 간결하지만 강력한 코드(write less, do more.)
* 크로스 브라우징
* 다양한 플러그인 제공

> **jQuery가 주요 기능**
> HTML문서 탐색 및 조작, 이벤트 처리, 애니메이션 및 Ajax 통신의 효율적이고 크로스브라우징이 지원되는 API 제공

[jQuery API Documentation](http://api.jquery.com/)

*****

## jQuery(), $() 함수

`jQuery()`를 줄여서 `$()`로 사용(alias)

```js
// 동일한 코드
jQuery('div');
$('div');

jQuery.trim(value);
$.trim(value);
```

## 셀렉터(Selector)

* [Selectors | jQuery API Documentation](http://api.jquery.com/category/selectors/)
* [jQuery Selectors](https://www.w3schools.com/jquery/jquery_ref_selectors.asp)
* [Try jQuery Selector](https://www.w3schools.com/jquery/trysel.asp)

**기본 셀렉터**

| 셀렉터 | 설명 |
| ----- | ----- |
| $(*) | 모든 요소 |
| $('tagName') | 태그명과 일치하는 요소 |
| $('#id') | 아이디와 일치하는 요소 |
| $('.className') | 클래스명과 일치하는 요소 |
| $('selector1, selector2, selector3') | 여러 요소를 동시에 찾을 때 ,(쉼표) 사용 |

```js
// div와 a요소, wrapper 아이디를 가진요소, on 클래스는 가진 요소 탐색
$('div, a, #wrapper, .on');
```

* [Basic Selector](http://api.jquery.com/category/selectors/basic-css-selectors/)
* [Hierarchy Selector](http://api.jquery.com/category/selectors/hierarchy-selectors/)
* [Attribute Selector](http://api.jquery.com/category/selectors/attribute-selectors/)
* [Basic Filter Selector](http://api.jquery.com/category/selectors/basic-filter-selectors/)
* [Child Filter Selector](http://api.jquery.com/category/selectors/child-filter-selectors/)
* [Content Filter Selector](http://api.jquery.com/category/selectors/content-filter-selector/)
* [Form Selector](http://api.jquery.com/category/selectors/form-selectors/)
* [Visibility Filter Selector](http://api.jquery.com/category/selectors/visibility-filter-selectors/)
* [jQuery Extensions Selector](http://api.jquery.com/category/selectors/jquery-selector-extensions/)

> **셀렉터의 선택**
> jQuery 셀렉터 선택은 페이지의 성능을 개선하는데 큰 역할을 할 수 있습니다. 일반적으로 다음을 고려해서 선택하는 것이 좋습니다.
> 1. #id(id값으로 검색), element(요소명으로 검색)
> 2. .class(class 속성으로 검색)
> 3. 1, 2, 4번 이외의 셀렉터
> 4. jQuery 확장 셀렉터(jQuery Extensions Selector)
>
> `1`은 내부적으로 브라우저 표준 `getElementById`, `getElementsByTagName` 메서드로 대체되므로 모든 환경에서 빠르게 동작합니다.
> `2`도 내부적으로 `getElementsByClassName`, `querySelectorAll` 메서드로 대체되어 빠르지만 IE 구버전에서는 성능이 떨어질 수 있습니다.
> `4`는 jQuery가 항상 자체 해석을 하기 때문에 늘 속도가 떨어집니다.