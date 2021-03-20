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

![](C:\Users\5102000294\Pictures\git init.PNG)

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

![](C:\Users\5102000294\Pictures\git new repository.PNG)



새 repository를 하기의 Repository name에 입력해서 생성한다.

![](C:\Users\5102000294\Pictures\Create New Repository.PNG)

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

CSS : 

JS(JAVASCRIPT):HTML Page를 역동적으로 구현하기 위한 기능을 만드는 언어