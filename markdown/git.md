# Git 깃

- 분산 <u>버전 관리</u> 시스템

버전 관리

- 코드의 히스토리(버전)을 관리하는 도구

- 개발되어온 과정 파악 가능

- 이전 버전과의 변경 사항 비교 및 분석

분산

- 중앙 집중 (은행)
- 분산형 (블록체인, 같은 정보를 여러 사람이 나눠 갖고 있음)

깃은 **변경사항**만을 저장

![캡처](git.assets/%EC%BA%A1%EC%B2%98.PNG)

**깃허브**: 깃 기반의 저장소 서비스

git bash here: 명령어 실행기. unix/linux 명령어 사용 가능

깃은 명령어를 통해서 사용

CLI(Command - Line Interface) <> GUI(Graphic user interface)

VSCODE-new terminal로 명령프롬포트 사용 가능

+옆의 드롭다운-> git bash-> unix, linux 명령어 사용 가능

문서 바탕화면에서 빈공간 우클릭-git bash here로 바탕화면에서 git bash 열 수 있다

##### 간단한 Unix/Linux 명령어

- 현재 위치의 폴더, 파일 목록 보기	ls
- 현재 위치 이동하기	cd <path> / cd .. <이전 위치로 돌아가기
- ~ <<home 디렉토리(로컬디스크c, 사용자, mulan)를 나타낸다
- 폴더 생성하기	mkdir cli_test
- 파일 생성하기	touch test.txt
- 파일 삭제	rm test.txt	// 폴더 삭제	rm -r cli_test

![캡처3](git.assets/%EC%BA%A1%EC%B2%983.PNG)

BasicCar.py 생성

README.md(): 프로젝트 설명 파일 꼭 형성해주기

-> 특정 버전으로 남긴다 = "**커밋(Commit)**한다"

**커밋**은 세가지 영역을 바탕으로 동작

- Working Directory	작업하고 있는 실제 디렉토리(.git이 있는 디렉토리)

  ​																						(RacingGround)

- Staging Area	커밋으로 남기고 싶은, 특정 버전으로 관리하고 싶은 파일이 있는 곳

- Repository	커밋이 저장되는 곳. 특정 디렉토리를 **버전 관리**하는 저장소

git init	**로컬 저장소를 생성**하는 명령어

git init Initialized empty Git repository in ~ //~에 빈 저장소를 생성하였다

![캡처2](git.assets/%EC%BA%A1%EC%B2%982.PNG)

![캡처5](git.assets/%EC%BA%A1%EC%B2%985.PNG)

![캡처6](git.assets/%EC%BA%A1%EC%B2%986.PNG)

- git status	git의 현재 상태	git add하기 전엔 untracked files 뜬다

- git add BasicCar.py README.md // git add . <<모든 파일을 staging area로 올림

git config --*global* user.email "akddnfsla@gmail.com"

git config --global user.name "wlgud2" //vscode 에서 쓰는 user name과 깃허브 아이디(wlgud2)가 같아야 함

​					**global**: 전 역에서 쓸 수 있다 // <>local

- git commit -m "커밋 이름"// m	커밋 메세지. 버전의 제목

- git add에서 basiccar와 readme 모두 staging area에 올렸다면, commit 파일에 두 파일의 수정 사항이 다 저장됨
  - basiccar만 staging area에 올렸다면, 커밋 시, 하나만 저장

working tree clean 		이전 커밋된 결과보다 변경된 사항 없음

- git log : git의 commit history 보기	//빠져나가기: q
- git diff : 두 commit 간 차이 보기



#### Remote Repository깃헙에서 제공. 인터넷과 연결해서 사용

Local Repository	내 피씨에서만 사용

깃허브에서 new repository-> public: 다른 사람도 내 repo를 볼 수 있다( push는 나만 할 수 있다 )

private: 나만 볼 수 있다

gitignore: 깃허브에서 관리하지 않을 파일

![dd](git.assets/dd.PNG)

https://~: 내 remote repo 주소

- git remote add origin https://github.com/wlgud2/remote_repo.git

  ​					origin: remoe repo의 자주 쓰는 별명

- git push -u origin master

  ​								*master: master branch ( 커밋을 쌓는 가지)*

  -> 깃한테 푸시 명령. origin으로. 내 로컬에 있는 master에 대한 변경사항(커밋)을.

  -> -u: origin(remote repo)의 master 와 local repo의 master 연결(최초 푸시때 한번만 하면 된다)

  -> 앞으로 수정, add, commit 후 **push**를 통해 origin에도 commit 보내야함

