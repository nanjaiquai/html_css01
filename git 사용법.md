###### **형상관리프로그램을 설치한다.**

https://www.git-scm.com/download 사이트에 접속해서 GIT설치프로그램을 설치한다.

설치한후CMD창을 전부 껐다가 다시 실행한다.

버전 관리를 위해서는 버전 관리하고자 하는 폴더로 이동한 후, GIT명령어를 이용해 초기화 명령어를 이용해서 초기화시켜준다.

```powershell
git init
```

다음과 같은 결과가 나온다.

```powershell
>> Initialized empty Git repository in E:\99. My Documents\GitHub\html_css/.git/
```

![git 초기화 결과 화면](https://github.com/nanjaiquai/html_css01/blob/main/image/git%20init.PNG?raw=true)

버전을 관리할 파일을 STATE상에 올려놓는 과정과 COMMIT하는 과정을 거쳐야 만이 그 파일이 버전이 정해지면서 관리를 할 수 있다.

```powershell
git add .
git commit -m <원하는 메시지>
```

처음 git을 설치하고 실행을 하게되면 다음과 같은 결과가 나온다.

```powershell
Run

 git config --global user.email "you@example.com"
 git config --global user.name "your name"
```

등록을 한 후 다시한번 git commit명령어를 실행한다.

```powershell
git commit -m <원하는 메시지>
```



git을 원격에 등록시켜 놓고 관리한다.

github.com에 접속해서 회원 가입을 해서 본인의 계정을 생성하고, 로그인을 한다.

New 를 선택해서 새로운 원격지 repository를 생성한다.

![새 저장소 만들기 선택](https://github.com/nanjaiquai/html_css01/blob/main/image/git%20new%20repository.PNG?raw=true)



새 repository를 하기의 Repository name에 입력해서 생성한다.

![새 저장소 만들기](https://github.com/nanjaiquai/html_css01/blob/main/image/Create%20New%20Repository.PNG?raw=true)

다음과 같은 명령어를 이용해서 원격 github repository와 local git repository를 연결한다.

```powershell
git remote add origin https://github.com/nanjaiquai/html_css.git
```

branch 생성

```powershell
git branch -M main
```

push명령어를 이용해서 원격에 올린다.

```powershell
E:\99. My Documents\GitHub\html_css>git push -u origin main
info: please complete authentication in your browser...
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 389 bytes | 194.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/nanjaiquai/html_css01.git
 * [new branch]      main -> main
Branch 'main' set up to track remote branch 'main' from 'origin'.
```

push명령어는 업데이트마다 계속해서 사용되는 명령어이다.



# HTML

html의 기본구조(Interface)는

```html
<!DOCKTYPE html>
<html>
    <head>
        //문서의 속성들이나 meta속성들이나 title을 정의한다.
    </head>
    <body>
        //웹브라우저상에서 주소창 밑에 있는 부분을 body라고 이 바디에 표현되는 콘텐츠 또는 기능들을 정의한다.
    </body>
</html>
```



###### html 문서는 3가지의 종류로 문서를 작성한다.

HTML, CSS, JAVASCRIPT

CSS : **Cascading Style Sheets**(**CSS**)는 [HTML](https://developer.mozilla.org/ko/docs/Web/HTML)이나 [XML (en-US)](https://developer.mozilla.org/en-US/docs/Web/XML)([SVG](https://developer.mozilla.org/ko/docs/Web/SVG), [XHTML](https://developer.mozilla.org/ko/docs/Glossary/XHTML) 같은 XML 방언(dialect) 포함)로 작성된 문서의 표현을 기술하기 위해 쓰이는 [스타일시트](https://developer.mozilla.org/ko/docs/Web/API/StyleSheet) 언어입니다.

JS(JAVASCRIPT):HTML Page를 역동적으로 구현하기 위한 기능을 만드는 언어



html_css/test2.html문서를 보면

```html
<!DOCTYPE html>
<html>

<head>
    <title>웹 페이지의 구성 요소</title>
    <style>
        body {
            background -color: linen;
            color: green;
            margin-left: 40px;
            margin-right: 40px;
        }

        h3 {
            text-align: center;
            color: darkred;
        }

        hr {
            height: 5px;
            border: solid grey;
            background-color: grey
        }

        span {
            color: blue;
            font-size: 20px;
        }
    </style>
    <script>
        function show() { // <img>에 이미지 달기
            document.getElementById("fig").src = "ElvisPresley.png"
        }

        function hide() { // <img>에 이미지 제거
            document.getElementById("fig").src = "";
        }
    </script>
</head>

<body>
    <h3 onmouseover="show()" onmouseout="hide()">
        Elvis Presley</h3>
    <hr>
    <div>
        <img id="fig" src=""></div>
    He was an American singer and actor. In November
    1956, he made his film debut in <span>Love Me
        Tender</span>. He is often referred to as
    "<span>the King of Rock and Roll</span>".
</body>

</html>
```

CSS -> <style> 내용 </style>

javascript -> <style> 내용 </style>

태그를 선언하고 그 안에 적는 onmouseover, onmouseout 같은 것을 이벤트 리스너와 id, src와 같은 속성을 적어서 html기능을 추가한다.



###### 메타데이터

데이터의 성질 등을 나타내는 데이터

메터데이터를 정의 내리는 태그는 HTML 페이지에 대한 메타 데이터를 담기 위한 태그들

-<base>, <link>,<script>,<style>,<title>,<meta>

head 태그 안에 위의 태그를 사용한다.

단, script태그는 body태그 안에도 사용할 수 있다.

```
<meta> 태그는 다양한 메타 데이터 표현
– 웹 페이지의 저작자, 문자 인코딩 방식, 내용 등
➢ 웹 페이지의 저작자가 “황기태”임을 표기하는 사례
▪ <meta name="author" content="황기태">
➢ 웹 페이지의 내용 설명
▪ <meta name="description" content="입학 요령에 대한 자세한 사항">
➢ 웹 페이지의 키워드(검색 엔진에 의해 검색되게 하기 위함)
▪ <meta name="keywords" content="컴퓨터, 소프트웨어, 스마트폰">
➢ charset 속성으로 웹 페이지에 사용하는 문자 코드 지정
▪ <meta charset=“UTF-8”>

```

###### img태그

<img>태그의 src 속성에 이미지 파일의 주소 지정

- src에 지정할 수 있는 이미지 종류
  - BMP, GIF, PNG, JPG(JPEG), animated-GIF

![image-20210322210318879](https://user-images.githubusercontent.com/32979365/111987285-613e8b00-8b52-11eb-94c0-c4cd00064ac6.png)

