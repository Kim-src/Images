# ✅ 나만의 깃허브 블로그 만드는 방법

<br>

### 🔔 1. Introduction
### 📌 깃허브 블로그를 선택한 이유
> - Markdown 언어로 프로젝트 개발 내용을 카테고리별로 정리하고 싶었습니다.
> - 웹/앱/어플리케이션/소프트웨어 등의 개발 과정을 실시간으로 기록하고 싶었습니다.
> - 에러를 해결한 경우 그 방법을 기록 및 공유하고 싶었습니다.
> - 구글 애드센스를 이용하여 소소한 광고 수익을 발생시키고 싶었습니다.

### 📌 대중적인 개발 블로그 장단점 비교
> - GitHub 블로그 :  
>   장점 1. Markdown 언어로 글을 작성할 수 있기에 글 구조가 일관되어 깔끔합니다.  
>   장점 2. 깃허브와 연동되어 있어서 개발하며 실시간으로 글 작성하기 좋습니다.  
>   장점 3. 구글 애드센스를 이용하여 소소한 광고 수익을 발생시킬 수 있습니다.  
> - Velog 블로그 :  
>   장점 1. Markdown 언어로 글을 작성할 수 있기에 글 구조가 일관되어 깔끔합니다.  
>   단점 1. 깃허브와 연동되어 있지 않아서 글 작성을 위한 별도의 관리가 필요합니다.  
>   단점 2. 구글 애드센스를 이용할 수 없습니다.  
> - Tistory 블로그 :  
>   단점 1. Markdown 언어로 글을 작성할 수 없기에 글 구조가 일관되지 않습니다.  
>   단점 2. 깃허브와 연동되어 있지 않아서 글 작성을 위한 별도의 관리가 필요합니다.  
>   장점 1. 구글 애드센스를 이용하여 소소한 광고 수익을 발생시킬 수 있습니다.  

<br>

### 🔔 2. Methodology (1/2) : Repository 연동
### 📌 블로그 전용 GitHub Repository 생성
> - GitHub.com에 접속한 뒤 레포지토리를 생성해야 됩니다.
> - 레포지토리 생성창은 중앙에 위치중입니다.
> - Repository name 입력란에 ```user-name.github.io``` 내용을 입력합니다.
> - 작성자의 Repository name 입력 내용은 아래와 같습니다.
>   ```
>   Kim-src.github.io
>   ```
> - 아래는 Repository 생성창 모습입니다.
<p align="center"><img src="https://github.com/Kim-src/Images/assets/150884526/26b0e2b4-22a9-4c59-9718-39333cf324de" width="500px"></p>

### 📌 블로그 전용 로컬 저장소 설정
> - 블로그 생성을 희망하는 로컬 저장소를 선택해야 됩니다.
> - (쉬운 표현) 블로그 전용 파일들을 보관할 컴퓨터의 폴더를 선택해야 됩니다.
> - 그리고 Git Bash에 해당 폴더를 접근하기 위한 내용을 입력해야 됩니다.
> - 참고로 C드라이브와 가까울수록 로컬 저장소(= 폴더)에 접근이 용이합니다.
> - 왜냐하면 Git Bash 등에는 Ctrl + C/V로 내용을 입력할 수 없기 때문입니다.
> - 아래는 Git Bash를 다운로드 할 수 있는 Git 사이트 링크입니다.
> - [Git Bash 다운로드 링크(보통 최신 버전 설치)](https://git-scm.com/downloads)

### 📌 Git Bash 실행 및 로컬 저장소 접근
> - Git bash의 경우 폴더 접근(= 더블클릭)을 "/"로 표시합니다.
> - 예를들어 사용자 폴더로 접근을 원하면 ```$ cd /c/Users``` 내용을 입력해야 됩니다.
> - 폴더에 공백이 있는 경우에는 작은 따옴표 등으로 구분해야 됩니다.
> - 참고로 cd는 change directory의 축약어입니다.
> - 작성자의 Git Bash 입력 내용은 아래와 같습니다.
>   ```bash
>   $ cd /c/Users/ceoba/Dropbox/'2. PJT'
>   ```
> - 아래는 Git Bash로 작성자의 블로그 전용 로컬 저장소에 접근한 모습입니다.
<p align="center"><img src="https://github.com/Kim-src/Images/assets/150884526/c53815f4-ef24-484f-88bc-340d1ba0ee3e" width="500px"></p>

### 📌 로컬 저장소에 GitHub Repository 연동
> - 현재 온라인 저장소인 GitHub Repository가 준비되었을 것입니다.
> - 그리고 Git Bash로 로컬 저장소인 블로그 전용 폴더에 접근한 상태일 것입니다.
> - 이제 두 저장소끼리의 연동이 필요합니다.
> - 그러므로 ```$ git clone 레포지토리 주소``` 입력 후 엔터키를 누르면 됩니다.
> - 작성자의 Git Bash 입력 내용은 아래와 같습니다.
>   ```bash
>   $ git clone https://github.com/Kim-src/Kim-src.github.io
>   ```

<br>

### 🔔 2. Methodology (2/2) : Ruby, Jekyll, Bundler 설치
### 📌 Ruby Development Kit 설치
> - 웹 페이지 제작을 위해서 Ruby, Jekyll, Bundler가 필요합니다.
> - Ruby는 개발 언어, Jekyll은 웹 제작 tool, Bundler는 의존성 관리 tool입니다.
> - (상세하게) Ruby는 개발 언어이며 별도의 형태가 존재하지 않습니다.
> - 그래서 Git bash라는 입력창을 이용해 Ruby를 활용할 수 있습니다.
> - Jekyll은 framework 느낌인 Ruby 기반의 웹 제작용 도구입니다.
> - 그리고 Bundler는 Ruby 개발에 필요한 각종 라이브러리의 버전 관리 도구입니다.
> - 이들을 Spring으로 비유하면 Bundler는 pom.xml이고 Jekyll은 project 자체입니다.
> - 아래는 Ruby Development Kit를 다운로드 할 수 있는 사이트 링크입니다.
> - 참고로 버전 호환성을 위해 Ruby Devkit의 3.1.3-1 (x86) 버전을 추천합니다.
> - [Ruby Development Kit 다운로드 링크 (3.1.3-1 (x86) 설치)](https://rubyinstaller.org/downloads/archives/)
<p align="center"><img src="https://github.com/Kim-src/Images/assets/150884526/c1ecf348-5d93-4780-bdec-bff734aabb88" width="500px"></p>

### 📌 Git Bash로 Jekyll 설치
> - Jekyll은 Git Bash에서 설치 가능합니다.
> - GIt Bash 실행 후 로컬 저장소로 이동한 뒤 Jekyll을 설치하면 됩니다.
> - 작성자의 Git Bash 입력 내용은 아래와 같습니다.
>   ```bash
>   $ cd /c/Users/ceoba/Dropbox/'2. PJT'/Kim-src.github.io
>   $ gem install jekyll
>   $ jekyll -v
>   ```
> - 입력 결과 작성자의 Git Bash 출력 내용은 아래와 같습니다.
>   ```bash
>   jekyll 4.3.3
>   ```
> - 그리고 Jekyll 설치가 완료된 로컬 저장소는 아래와 같은 상태로 변경됩니다.
<p align="center"><img src="https://github.com/Kim-src/Images/assets/150884526/e733d653-1afe-4345-80e4-13511d8d6b2d" width="500px"></p>

### 📌 Git Bash로 Bundler 설치
> - Bundler 역시 Git Bash에서 설치 가능합니다.
> - Git Bash가 실행된 상태에서 아래 내용을 입력하면 됩니다.
> - 작성자의 Git Bash 입력 내용은 아래와 같습니다.
>   ```bash
>   $ gem install bundler
>   $ bundler -v
>   ```
> - 입력 결과 작성자의 Git Bash 출력 내용은 아래와 같습니다.
>   ```bash
>   Bundler version 2.5.6
>   ```
> - 그리고 Bundler 설치가 완료된 로컬 저장소는 다시 다음 상태로 변경됩니다.
<p align="center"><img src="https://github.com/Kim-src/Images/assets/150884526/670d434d-ee37-473b-9978-df490b2784dd" width="500px"></p>

<br>

### 🔔 3. Results : 브라우저에 웹 페이지 호출
### 📌 새로운 Jekyll Project 생성
> - 이제 첫 깃허브 블로그 웹 페이지를 생성할 모든 준비를 마쳤습니다.

> - 작성자 Git Bash 입력 내용 :
>   ```bash
>   $ cd /c/Users/ceoba/Dropbox/'2. PJT'/Kim-src.github.io
>   $ jekyll new ./
>   ```
> - 작성자 Git Bash 출력 내용 :
>   ```bash
>   - Jekyll 설치 관련 사항
>   ```
> - 아래 이미지는 Jekyll이 설치된 직후의 로컬 저장소 main 폴더 상태
<p align="center"><img src="https://github.com/Kim-src/Images/assets/150884526/af3faae6-5a78-4ae7-94b3-3bafc35a1fed" width="500px"></p>

### 📌 새로운 Bundle Tool 생성
> - 작성자 Git Bash 입력 내용 :
>   ```bash
>   $ bundle install
>   $ bundle update
>   $ bundle install
>   ```
> - 작성자 Git Bash 출력 내용 :
>   ```bash
>   - bundle 설치 및 업데이트 관련 사항
>   ```
> - 아래 이미지는 Bundle이 설치된 직후의 로컬 저장소 main 폴더 상태
<p align="center"><img src="https://github.com/Kim-src/Images/assets/150884526/9e32a194-ab2b-4a6e-ab5f-7949dcb8f18c" width="500px"></p>

### 📌 Jekyll 기본 웹 페이지 생성
> - Local Server Address (URL) 생성
> - 작성자 Git Bash 입력 내용 :
>   ```bash
>   $ bundle exec jekyll serve
>   ```
> - 작성자 Git Bash 출력 내용 :
>   ```bash
>   - Jekyll의 로컬 웹 서버 실행 사항
>   - 개발중인 웹 관련 서버(URL) 주소 출력
>   ```
> - 웹 페이지 호출 방법
>   ```bash
>   - 브라우저(Chrome 등) 주소창에 아래 주소 입력
>   - 아래 주소는 Git Bash에 일반적으로 출력되는 내용
>   - http://127.0.0.1:4000/
>   ```
### 📌 성공적으로 호출된 웹 페이지
> - 아래 이미지와 같은 Jekyll 기본 페이지가 호출되면 성공
<p align="center"><img src="https://github.com/Kim-src/Images/assets/150884526/33d309a9-8c3c-4b76-9728-a33b6b939968" width="500px"></p>

<br>

### 🔔 4. Conclusions : ~
### 📌 ~

<br>

### 🎁 5. References
> - [프로의 개발일지 블로그 1](https://devpro.kr/posts/Github-%EB%B8%94%EB%A1%9C%EA%B7%B8-%EB%A7%8C%EB%93%A4%EA%B8%B0-(1)/)
> - [프로의 개발일지 블로그 2](https://devpro.kr/posts/Github-%EB%B8%94%EB%A1%9C%EA%B7%B8-%EB%A7%8C%EB%93%A4%EA%B8%B0-(2)/)

<br>

***

<br>
<br>
<br>





