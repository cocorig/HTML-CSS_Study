# ☠️  🅷 🆃 🅼 🅻

 # 🚩 종류와 중요도에 따른 태그

## -  강조하기 위한 태그들

`<b>` vs `<strong>`  

b 태그(의미 x)는 글자를 굵게만 만들지만, strong 태그는 그 내용이 중요하다는 의미 또한 담고 있다.
이들이 굵게 보이는 것 또한 브라우저의 기본 설정일 뿐,
이러한 디자인 요소는 CSS(font-weight:bold)로 지정해주어야 한다.

`<em>` vs `<strong>` 

`<em>` : 음성 강조 하는 것처럼 문장의 의미, 강조할 내용임을 명시
`<strong>` : 문장의 일부에 중요성을 더하는 데 사용, 중요한 내용임을 명시

 `<i>` : 요소가 글자를 기울이기는 하지만, 기울임 꼴을 적용하기 위한 용도로 사용 x. 
  CSS font-style 속성을 사용한다. 문맥 중 다른 폰트로 꾸밀 때

### - 첨자 태그 

  지수, 변수, 화학식으로만 사용해야 한다 -> 단순 꾸미기 용도로 사용하려면  vertical-align
`<sup>`: `<p>`x`<sup>`3`</sup>` => x3
`<sub>`:  x<`sub>`n`</sub>``</p>` => xn  

#### - (구) 밑줄 태그와 취소선 태그

`<u>`는 과거 밑줄을 긋는 용도로 사용되었으나
현재는 CSS 효과와 함께 철자 오류 등을 강조하는 용도로 사용
`<s>` 태그는 더 이상 유효하지 않은 정보를 취소선을 나타냄

-----

#  🚩 인용된 콘텐츠

속성, 특성(attribute) : 태그의 동작을 설정 및 제어
태그마다 설정 가능한 속성들이 있음.

### - 긴 인용문
` <blockquote>` : 긴 인용문 사용, cite 속성으로 출처 표시
`<cite>` : 저작물의 출처 표시, 제목을 반드시 포함하여야 한다.

```html

  <blockquote cite="https://developer.mozilla.org/ko/docs/Web/HTML/Element/blockquote">
    <p>
      HTML &lt;blockquote&gt; 요소는 안쪽의 텍스트가 긴 <mark> 인용문 </mark> 임을 나타냅니다. <br>
      주로 들여 쓰기를 한 것으로 그려집니다. (외형을 바꾸는 법은 사용 일람을 참고하세요) <br>
      인용문의 출처 URL은 cite 특성으로, 출처 텍스트는 &lt;cite&gt; 요소로 제공할 수 있습니다.
    </p>
  </blockquote>
  <!-- 인용문 사이트 이름 ,blockquote 구현하는 데 사용-->
  <cite>&lt;blockquote&gt;: 인용 블록 요소</cite> from MDN
```
### - 짧은 인용문

`<q>` : 비교적 짧은 인용문에 사용, cite 속성으로 출처 표시

```html
    본 페이지는 "<mark>인용문</mark>"이란 키워드로 검색한 결과입니다. 
   <q cite="https://developer.mozilla.org/ko/docs/Web/HTML/Element/q"
    >HTML &lt;q&gt;요소는 둘러싼 텍스트가 짧은 <br> 인라인 <mark>인용문</mark>이라는것을 나타냅니다.</q>
```
### - `<mark>` 
 인용문 중 하이라이트 또는 사용자 행동과 연관된 곳 표시 ,페이지에서 사용자의 행동에 관련된
 특정 단어가 사용자의 검색이라는 행위의 결과일 때 사용한다.


###  -`<abbr>` 
태그로 머리글자 표현하기
abbr 태그를 사용하여 HTML 을 표기한 문단

####-  html에서 태그를 표시하고 싶을 때 
  <	 :`&lt;`
    ``> :	`&gt;`

  ------


#  🚩 나열되는 요소들
웹사이트에 나열되는 부분은 다 ul,li태그 사용
주의!
 ul,ol의 자식요소는 li만 가능하다!! li의 자식요소로는 다른 태그 사용가능!
```html
<ul>
    <!-- ul,ol의 자식요소로는 li만 가능하다-->
    <li>이틀치 옷
      <!-- <div></div>  li의 자식요소로는 사용가능하다-->
    </li>
    <li>세면도구</li>
    <li>수건</li>
    <li>학습도구</li>
    <ul>
      <li>노트북</li>
      <li>필기구</li>
      <li>교재</li>
    </ul>
  </ul>
  ```

  ## -  사전처럼 용어를 사용

  용어 사전  1:1 또는 n:n 가능,
  `dd(정의)`의 값이 변화할 수 있는 정보라면 dl을 사용하면 안 된다.
  이미 정의되어 있거나 설명이 정해져 있는 경우에만 사용할 수 있다.

  ```html
  <dl>
    <dt>용어</dt>
    <dd>정의</dd>
  </dl>
  
  ```

  #  🚩 이미지 넣기

 ` <img src="(이미지 파일 경로)" alt="(대체 텍스트)" title="(툴팁 텍스트)">`


##  이미지 태그의 속성

|속성 |	설명	| 비고|
|------|---|---|
|src	| 원본파일 경로	| 절대경로 또는 상대경로 (필수)|
|alt |	대체 텍스트 |	스크린 리더, 원본파일 무효 시 나타난다.(필수, 자세하게)|
|title|	툴팁| 	alt의 대체제나 반복이 되어서는 안 됨 (alt와 똑같지 않아야 함, 추가적인 설정알뿐 그림 설명을 툴팁에 사용해선 안된다 ),이미지에 마우스 올릴 때 생김|
|width	| 너비 |	픽셀 단위의 정수|
|height |높이 |	픽셀 단위의 정수|

> 절대경로 또는 상대경로
절대경로 : https://---(도로명, 지번주소) , 전체주소
상대경로 : 
 현재파일의 같은 방(폴더)이면  ./ 
 같은 폴더 안에 이미지폴더 안에  img.jpeg
 ./images/img.jpeg

../HTML/images/img.jpeg
상대경로에서 밖으로 나갈 떼 (내 방에서 나갈 때)../
내 방에서 나가서 HTML -> images 방에 들어가서 img.jpeg 가져와라


# 🚩 다른 곳으로의 링크

## - a 태그
> <a href="(연결할 주소)" target="(링크를 열 곳 옵션)">

|target| 속성값|	설명|	
|----|---|---|
|_self|	현재 |창	|기본|
|_`blank	`|새 창|	`텍스트나 내부 이미지의 alt 등으로 명시 필요`, 접근성을 위한 속성 , 패이지를 눈으로 보지 않는 사람들을 위해서 완전히 tab이 바뀌는 것에 대해 명시를 해줘야 한다 |
|_parent|	부모 프레임	|`<iframe>` 사용 시|
|_top	|최상위 프레임	|`<iframe>` 사용 시|


```html

 <a href="https://www.yalco.kr" target="_blank">
    <img 
    src="https://showcases.yalco.kr/html-css/01-07/yalco-logo.png" alt=" 얄코 사이트로(새 탬에서)"
    >
  </a>
<!-- 주소에 해당 id값을 넣어줘서 건너뛰기 링크로 바꿀 수 있다 -->
<a href="#target_99">타깃으로 이동</a>
```

## - address 태그
주소 및 연락처 정보를 포함
특별한 기능은 없고, 여기가 연락처라는 걸 명시한다.

```html

<address>
  웹사이트 주소: <a href="https://www.yalco.kr">yalco.kr</a> <br>
  오피스: 전산시 개발구 코딩동 123번길 45 <br>
  <!-- tel : 전화번호 연결 -->
  전화 <a href="tel:010-1234-5678">010-1234-5678</a> <br>
  <!-- mailto: - 이메일 -->
  이메일: <a href="mailto:yalco@kakao.com">yalco@kakao.com</a>
</address>

```


# 🚩 사용자로부터 입력받기 

|태그|설명|비고|
|------|---|---|
|`<form>`  |정보를 제출하기 위한 태그들을 포함|	autocomplete 속성: 자동완성 여부 (기본: on)|
|`<input>`|	입력을 받는 요소	|type 속성을 통해 다양화|
|`<label>`|	인풋 요소마다의 라벨|	for 속성값을 인풋 요소의 id와 연결. `인풋의 클릭 영역 확장 `|
|`<button>`|	버튼	| type 속성에 submit(제출), reset(초기화), button(기본 동작 없음)|

 > id와 for가 같아야 레이블을 클릭했을 때 해당 인풋 요소가 선택된다.
```html

  <form autocomplete="off">
    <label for="name">이름</label>
    <!-- name 속성은 html상으론 의미 x , 정보들을 서버로 보낼 떼 사용 -->
    <input id="name" type="text" name="my-name">
    <label  for="age">나이</label>
    <input id="age" type="number" name="my-age" >

    <button type="submit">제출</button>
    <button type="reset">초기화</button>
  
  </form>

```
 - input 의 name 속성은 ?
name 속성은 html상으론 의미 x , 정보들을 서버로 보낼 때 사용한다.
서버에서 각 항목을 받을 때 `무엇에 대한 값인지 구분`하는 이름으로 작용한다.
- value -> input이 갖는 초기값

## 텍스트 관련 인풋 속성들

|속성|설명|비고|
|------|---|---|
placeholder	|빈 칸에 보이는 안내문	|
maxlength	|최대 길이	|
minlength	|최소 길이	| 위반 시 submit이 거부됨

  maxlength="5" -> 5글자 넘기면 x , 5글자 이하
  minlength="4" -> 4글자 이상 써야 함 , 4글자 이상

[👉 MDN input 태그 속성들]('https://developer.mozilla.org/ko/docs/Web/HTML/Element/Input')



## 체크 관련 인풋 속성들

|속성|타입|설명|
|------|---|---|
checked	|체크박스 & 라디오|	체크됨 여부|
name|	라디오 (다른 타입들에서도 사용)|	옵션들의 그룹으로 사용됨| name을 똑같이 정해서 그룹을 만든다, 그룹 중 하나만 선택 가능|
value	|라디오 (다른 타입들에서도 사용)|	각 옵션마다 실제로 넘겨질 값|

## 기타 인풋 타입


|속성|설명|
|------|---|
accept	|받아들일 수 있는 파일 형식| accept="image/png, image/jpeg"
multiple	|	여러 파일 업로드 가능 여부, 파일 선택할 때 여러 개로 드래그 가능한지|	

```htm

 <h1>기타 인풋 타입</h1>

    <form action="#">
      
      <label for="fileIP">파일</label>
      <input
          type="file"
          id="fileIP"
          accept="image/png, image/jpeg"
          multiple
          >
      <!-- 굳이 사용자에 보이지 않아도 되는 정보를 안 보이게 처리 -->
      <label for="hdnIp">hidden</label> <br>
        <input
          id="hdnIp"
          type="hidden"
        >
    </form>
    <form action="#">
      <!-- xxx.@  이메일형식 -->
      <label for="emailIP">이메일</label>
      <input type="email" name="email" id="emailIP">
      <button type="submit">제출</button>
    </form>
```

## 인풋 요소 공통(대부분) 속성

`value` : defalut값 지정할 수 있다. 예를 들어 사용자의 계정설정에서 내 아이디 부분이 전에 입력한 대로 떠서 수정하곳 싶은 부분만 수정하도록 하고 싶을 때 사용할 수도 있다.

`autofocus `: 클릭하지 않아도 페이지 로드 시 자동으로 선택되도록 포커스
`readonly `: 수정할 수 없고, 읽기만 가능, 제출 시 값이 전송됨  -->
`required `: 필수 값, 입력하지 않고 제출할 수 없다.
`disabled `: 입력불가, 제출 시 전송하지 않는 값

## 옵션 관련 속성들

## - select 태그

<p align = "center" width="100%">
  <img  alt="img-1" src="https://github.com/cocorig/likelion-Frontend/assets/95855640/0d08b82c-c727-4e90-a921-bd10364d8ac4" width="30%">
  
  <img alt="img-0" src="https://github.com/cocorig/likelion-Frontend/assets/95855640/f0a8ade0-6704-4e93-9910-6f1e19e23db7" width="30%">
</p>

```html

 <label for="lang">언어</label> <br>

 <select id="lang">
   <option value="">-- 언어 선택 --</option>
   <option value="html">HTML</option>
   <option value="css">CSS</option>
   <option value="js">자바스크립트</option>
   <option value="ts">타입스크립트</option>
 </select>

```


## - optgroup 태그



<p align = "center" width="100%">
  <img width="40%"  height="400px"  alt="스크린샷 2023-07-16 오후 8 58 50" src="https://github.com/cocorig/likelion-Frontend/assets/95855640/9339e856-3d69-42b9-b81b-899e72f512ff">
  <img  width="40%" alt="스크린샷 2023-07-16 오후 8 58 43" src="https://github.com/cocorig/likelion-Frontend/assets/95855640/3f5cbb5f-9c58-4b8d-8e1f-3ae839a15996">
</p>

```html

 <h2>optgroup 태그</h2>

 <label for="shopping">쇼핑 목록</label> <br>
 <select id="shopping">
  <!-- optgroup으로 묶어줌 -->
   <optgroup label="과일">
     <option value="f_apl">사과</option>
     <option value="f_grp">포도</option>
     <option value="f_org">오렌지</option>
   </optgroup>
   <optgroup label="채소">
     <option value="v_crt">당근</option>
     <option value="v_tmt">토마토</option>
     <option value="v_ept">가지</option>
   </optgroup>
   <optgroup label="육류">
     <option value="m_bef">소고기</option>
     <option value="m_prk">돼지고기</option>
     <option value="m_ckn">닭고기</option>
   </optgroup>
 </select>

```



<img  width="212" alt="스크린샷 2023-07-16 오후 8 59 55" src="https://github.com/cocorig/likelion-Frontend/assets/95855640/595202bd-07b4-4c86-a65b-a6092f2f8ae8">

```html

 <h2>datalist 태그</h2>

 <label for="job">현재 직업</label> <br>
 <input id="job" list="jobs">
 <!-- list와 id를 연결, 권장하는 샘플 값들을 지정할 수 있다. -->
 <datalist id="jobs">
   <option value="학생">
   <option value="디자이너">
   <option value="퍼블리셔">
   <option value="개발자">
 </datalist>


```

|속성|태그|설명|
|------|---|---|
|multiple	|`<select>`|	다중 선택 가능. 잘 사용x , 대신 checkbox 사용|
|selected	|`<option>`	|기본값으로 선택됨 ( checkbox, radio의 checked처럼 )|
|value	|`<option>`	|실제로 서버로 전송될 값|
|list	|`<input>`|	연결할 `<datalist>`의 ID|

---
### pre태그 (x)
html에서 작성한 그대로 화면에 적용된다. 아스키 아트를 사용할 때 씀
하지만 스크린 리더는 pre태그의 내용을 건너뛰거나 내용을 읽지 않으므로 접근성을 위해 잘 쓰지 않는다.

### iframe (x)

웹사이트 안에 또 다른 사이트를 넣을 수 있다, 특별한 경우 아닌 이상 잘 쓰지 않는다.

⚠️ 권장되지 않는 요소
보안상 위험 ( clickjacking 등 )
사용성 저하 ( 뒤로 가기 문제 등 )
검색 최적화 제한
브라우저에 무리(한 화면에서 열기 때문)

### kdd
`<kdd>Ctrl</kdd> + <kdd>C</kdd>`
 -> <kdd>Ctrl</kdd> + <kdd>C</kdd> 와 같은 키보드 입력을 나타낼 때 사용

---


## `<span>과 <div>`는 특별한 기능이 없는 컨텐츠 주머니 

이 둘의 차이는 주머니의 모양과 차지하는 공간이다.

인라인: `<strong>, <em>, <a> 등의 태그에서 기능을 빼면 <span>,`  그 요소 크기만큼 차지해서 나란히 한 줄에 나열된다.
블록 : `<h1~6>, <p>, <ul> 등의 태그에서 기능을 빼면 <div>` 한 줄 다 차지, 마당을 갖는다