


<span style="color:orange;">Word up</span>
<div id="main">


[참고] : https://gist.github.com/ihoneymon/652be052a0727ad59601

전체적인 마크다운언어 알려주는것 현재페이지 보여지는 내용들 

[참고] : https://inasie.github.io/it%EC%9D%BC%EB%B0%98/%EB%A7%88%ED%81%AC%EB%8B%A4%EC%9A%B4-expander-control/

마크다운에서 접기 기능을 하는것 마크다운 자체에는 없기떄문에 html을 이용한다.

<details>
<summary>접기/펼치기 버튼</summary>
<div markdown="1">

|제목|내용|
|--|--|
|1|1|
|2|10|

</div>
</details>

[참고] : https://a1010100z.tistory.com/entry/Markdown-%EB%A7%88%ED%81%AC%EB%8B%A4%EC%9A%B4-%EB%AC%B8%EC%84%9C-%EB%82%B4%EB%B6%80-%EB%A7%81%ED%81%AC-%EC%9D%B4%EB%8F%99

내가 궁금하던것 내부링크를 걸어서 원하는 위치로 이동하는것 규칙은 다음과같다.

[보여지는 텍스트](#이동할위치의텍스트)
~생략~
#이동할위치의텍스트 라 가정할떄
  
  --> 해본결과 되지않는다. <span>이나 <div>로 해당 글들을 묶어준후 아래처럼 사용하면된다. 
 
  [여기를참조하자](#text)
  
  
  

[공통] 마크다운 markdown 작성법
1. 마크다운에 관하여
1.1. 마크다운이란?
Markdown은 텍스트 기반의 마크업언어로 2004년 존그루버에 의해 만들어졌으며 쉽게 쓰고 읽을 수 있으며 HTML로 변환이 가능하다. 특수기호와 문자를 이용한 매우 간단한 구조의 문법을 사용하여 웹에서도 보다 빠르게 컨텐츠를 작성하고 보다 직관적으로 인식할 수 있다. 마크다운이 최근 각광받기 시작한 이유는 깃헙(https://github.com) 덕분이다. 깃헙의 저장소Repository에 관한 정보를 기록하는 README.md는 깃헙을 사용하는 사람이라면 누구나 가장 먼저 접하게 되는 마크다운 문서였다. 마크다운을 통해서 설치방법, 소스코드 설명, 이슈 등을 간단하게 기록하고 가독성을 높일 수 있다는 강점이 부각되면서 점점 여러 곳으로 퍼져가게 된다.

1.2. 마크다운의 장-단점
1.2.1. 장점
1. 간결하다.
2. 별도의 도구없이 작성가능하다.
3. 다양한 형태로 변환이 가능하다.
3. 텍스트(Text)로 저장되기 때문에 용량이 적어 보관이 용이하다.
4. 텍스트파일이기 때문에 버전관리시스템을 이용하여 변경이력을 관리할 수 있다.
5. 지원하는 프로그램과 플랫폼이 다양하다.
1.2.2. 단점
1. 표준이 없다.
2. 표준이 없기 때문에 도구에 따라서 변환방식이나 생성물이 다르다.
3. 모든 HTML 마크업을 대신하지 못한다.
[test](#test)2. 마크다운 사용법(문법)
2.1. 헤더Headers
큰제목: 문서 제목

<div id="Text">This is an H1</div>
=============
This is an H1
작은제목: 문서 부제목

This is an H2
-------------
This is an H2
글머리: 1~6까지만 지원

# This is a H1
## This is a H2
### This is a H3
#### This is a H4
##### This is a H5
###### This is a H6
This is a H1
This is a H2
This is a H3
This is a H4
This is a H5
This is a H6
####### This is a 7.

2.2. BlockQuote
이메일에서 사용하는 > 블럭인용문자를 이용한다.

#Text Test


> This is a blockqute.
This is a first blockqute.

This is a second blockqute.

# test This is a third blockqute.

이 안에서는 다른 마크다운 요소를 포함할 수 있다.

This is a H3
List
code
2.3. 목록
● 순서있는 목록(번호)
순서있는 목록은 숫자와 점을 사용한다.

1. 첫번째
2. 두번째
3. 세번째
첫번째
두번째
세번째
현재까지는 어떤 번호를 입력해도 순서는 내림차순으로 정의된다.

1. 첫번째
3. 세번째
2. 두번째
첫번째
세번째
두번째
딱히 개선될 것 같지는 않다. 존 그루버가 신경안쓰고 있다고...

● 순서없는 목록(글머리 기호)
* 빨강
  * 녹색
    * 파랑

+ 빨강
  + 녹색
    + 파랑

- 빨강
  - 녹색
    - 파랑
빨강
녹색
파랑
빨강
녹색
파랑
빨강
녹색
파랑
혼합해서 사용하는 것도 가능하다(내가 선호하는 방식)

* 1단계
    - 2단계
    	+ 3단계
            = 4단계
1단계
2단계
3단계 = 4단계
2.4. 코드<pre><code></code></pre>
4개의 공백 또는 하나의 탭으로 들여쓰기를 만나면 변환되기 시작하여 들여쓰지 않은 행을 만날때까지 변환이 계속된다.

한줄 띄어쓰면 인식이 제대로 안되는 문제가 발생하곤 합니다.

This is a normal paragraph:

    This is a code block.
end code block.
``` This is a normal paragraph: This is a code block. end code block. ```
실제로 적용해보면, This is a normal paragraph:

This is a code block.
end code block.

2.5. 수평선<hr/>
아래 줄은 모두 수평선을 만든다. 마크다운 문서를 미리보기로 출력할 때 페이지 나누기 용도로 많이 사용한다.

* * *

***

*****

- - -

---------------------------------------
2.6. 링크
참조링크
[link keyword][id]
[id]: URL "Optional Title here"

Link: [Google][googlelink]
[googlelink]: https://google.com "Go google"
Link: [Google][googlelink] [googlelink]: https://google.com "Go google"

인라인 링크
syntax: [Title](link)
Link: Google

자동연결
<http://example.com/>
<address@example.com>
http://example.com/ address@example.com

2.7. 강조
*single asterisks*
_single underscores_
**double asterisks**
__double underscores__
++underline++
~~cancelline~~
single asterisks single underscores double asterisks double underscores ++underline++ cancelline

2.8. 이미지
![사진테스트](https://user-images.githubusercontent.com/45536211/52957679-94dbe380-33d5-11e9-922d-8e99431bc9ac.jpg)
![사진테스트2](https://user-images.githubusercontent.com/45536211/52957688-986f6a80-33d5-11e9-86c8-db0e9dae5081.jpg)
사진 테스트

사이즈 조절 기능은 없기 때문에 <img width="" height=""></img>를 이용한다.

3. 마크다운 사용기
3.1. 이지윅(WSYWIG) 에디터
우리가 흔하게 접하는 웹에서 사용되는 에디터(네이버, 다음, 구글 등)이 대부분 이지웍 에디터에 속하며 기본적으로 HTML을 이용하여 스타일을 적용하여 문장을 꾸미는 형태를 취하게 된다. 그래서 하루패드와 같은 마크다운 에디터의 View 영역의 내용을 복사하여 붙여넣기를 하면 대체적으로 View영역에서 보이는 그대로 복사되는 편이다. 다만, 붙여넣기 이후에 문장들을 수정하려고 할 떄 문제가 되는데, 이는 스타일이 포함된 태그가 수정과정에서 변형되면서 전체적인 영향을 끼치는 탓이다. 티스토리 블로그에서는 쉽지 않고... 워드프레스의 경우에는 마크다운으로 작성된 포스트를 HTML로 변환해주는 기능을 활용하는 것이 좋다. 결론은, 복사해서 붙여넣기하면 가급적이면 본문은 수정하지 않는 것이 좋다.

3.2. 깃헙Github, 비트버킷Bitbucket과 요비Yobi 등
최근 유행하는 협업개발플랫폼의 경우에는 마크다운을 변환하는 컨버터 기능을 기본탑재하고 있기 때문에 마크다운 문법으로 작성한 텍스트를 그대로 복사해서 붙여넣거나 업로드하는 것만으로 마크다운의 적용이 가능하다.

3.3. MS워드 적용
View 영역의 항목을 그대로 붙여넣거나 HTML 내보내기 등으로 생성한 파일을 불러오는 형태로 사용가능하다. 적용한 헤더를 워드가 읽어드리면서 목차에 적용하기 때문에 이를 활용하면 목차까지도 손쉽게 적용이 가능해진다.

4. 정리
마크다운은 기본문법만 알고 있다면 일반 텍스트편집기에서도 손쉽게 작성이 가능한 마크업언어다. 현재 다양한 도구와 플랫폼에서 지원하고 있기 때문에 더욱 손쉽게 스타일적용된 문서를 작성할 수 있기 때문에 점점 널리 사용되고 있다. 마크다운을 이해하고 사용하면서 쉽고 빠르게 스타일문서를 작성해보세요. 저는 Dropbox 프로를 구매해서 집-랩탑-스마트폰이 각각 연동을 시켜서 사용하고 있습니다. 드랍박스에 저장된 마크다운 문서는 Dropbox 웹서비스 상에서 제공하기 때문에 웹상에서 바로 열람할 수도 있어 링크를 걸어서 다른 사람과 공유하는 형식으로 사용하고 있다.

링크 예: Markdown 설명
○ 참고문서
78 Tools for writing and previewing Markdown
John gruber 마크다운 번역
깃허브 취향의 마크다운 번역
허니몬의 마크다운 작성법

</div>
