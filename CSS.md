# CSS

* CSS 기본 문법
  1. 인라인 스타일 시트: 우선순위가 높다.
  2. 내부 스타일시트: HTML내부에서 간단하게 작성.
  3. 외부 스타일시트:CSS 파일을 만든다.

---

* __선택자__

  * __타입 선택자__ : 태그 이름을 지정하여 선언

  ```css
  /* 타입선택자(태그선택자) */
  pre{
      text-align: center;
  }
  
  h1{
      text-align: right;
      color: blue;
  }
  ```

  * __id 선택자 __: 요소에 id를 지정하고 style에서 지정된 id값을 사용 `#` 으로 구분

  ```css
  /* id 선택자 */
  #sid01{
      color: green;
  }
  
  #sid02{
      color: yellow;
  }
  
  #sid03{
      color: blue;
  }
  ```

  * __class 선택자__ : 요소에 class를지정하고 style에서 지정된 class 값을 사용 `.` 로 구분

  ```css
  /* class 선택자 */
  .scls{
      color: pink;
  }
  .cls{
      background-color: blue;
  } 
  ```

  * __전체 선택자__ : *을 사용함

  ```css
  /* 전체선택자 */
  *{
      text-align: right;
      margin: 0;
      padding: 0;
  }
  ```

  * __자식 선택자__

  ```css
  #did > div > p{
      color: silver;
  }
  
  #did> p{
      color: orange;
  }
  ```

  * __인접 선택자__ : 지정한 요소 다음에 나오는 요소 선택

  ```css
  /* 인접 선택자 */
  h3 + b{
      background-color: black;
      color: white;
  }
  span + b{
      background-color: yellow;
      color: brown;
  }
  ```

  * __속성 선택자__ : 속성이 정의된 태그만 선택하는 선택자

  ```css
  /* 속성 선택자 */
  p[title]{
      color: skyblue;
  }
  p[name]{
      color: red;
  }
  p[title="b"]{
      background-color: yellow;
  }
  ```

  * __가상 클래스 선택자__

  ```css
  a:link{
      color: pink;
      font-size: 20pt;
  }
  a:visited{
      color: red;
  }
  a:hover{
      background-color: purple;
  }
  input:checked{
      width: 200px;
      height: 200px;
  }
  ```

  * __종속 선택자__ : 타입 선택자와 id 선택자(#) class 선택자(.)가 혼합된 형태.

  ```css
  /* 종속 선택자 */
  li.acls01{
      background-color: green;
  }
  li.acls02#sidli{
      background-color: yellow;
  } 
  ```

  * __하위  선택자__ : 특정 요소 하위의 요소를 지정할때 사용

  ```css
  /* 하위 선택자 */
  div span{
      background-color: yellow;
  }
  ```

  * __그룹 선택자__

  ```css
  /* 그룹 선택자 */
  p,pre,strong{
      color: lime;
  }
  ```

---

* __CSS 활용__

  * background 이미지 삽입

  ```CSS
   h1{ /* 태그 선택*/
              background-size: 300px;
              background-image: url("../1_html/image/img02.png"); /* URL을 통해 이미지 삽입*/
              background-repeat: no-repeat;
              background-position: center;
      }
  ```

  * `float, clear` (태그들을 나열해주는 방법)

  ```css
   #w01{  /*float을 통해 나열이 가능하며 clear를 적용한 css는 위에 float을 적용한 태그들을 냅두고 밑으로 내려온다.*/
              float: right;
              width: 200px;
              padding: 15px;
              background-color: lightgray;
              
   }
   #w02{
              /* float: left; */
              clear: right; 
              width: 200px;
              padding: 15px;
              background-color: pink;
              
   }
   #w03{ 
              /* clear: both; */
              width: 200px;
              padding: 15px;
              background-color: aqua;
   }
  ```

  * `display: inline-block `(태그들을 나열해주는 방법)

  ```css
     div{ /*블록형태의 태그들을 inline블록 형태로 변환 */
              display: inline-block;  
          }  
  ```

  *  `display: flex` (태그들을 나열해주는 방법)

  ```css
  /*width 크기에 맞게 일렬로 나열해주는 속성이다.ex)*/
  .header{
      position: fixed;
      top: 0;
      left: 0;
      border-bottom: 2px solid black;
      width: 100%;
      z-index: 10;
      background-color: white;
  }
  ```

  