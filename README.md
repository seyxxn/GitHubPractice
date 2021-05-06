GitHub repository URL : <https://github.com/seyxxn/GitHubPractice>  

# git & GitHub Tutorial  

> ## **git** 은 **형상관리도구** (버전관리시스템)  
> ## **GitHub** 는 **원격 저장소** (원격 전송된 내역들이 저장되는 공간을 제공)  
    
## **(1) GitHub 사용 전 알아야 할 사전 지식**
----
**로컬 저장소** : 내 PC에 파일이 저장되는 개인 전용 저장소  
**원격 저장소** : 파일이 원격 저장소 전용 서버에서 관리되며 여러 사람이 함께 공유하기 위한 저장소  
**커밋 (commit)** : 파일을 추가하거나 변경한 내용을 저장소에 저장하는 작업  
**푸시 (push)** : 파일을 추가하거나 변경한 내용을 원격 저장소에 업로드하는 작업 (즉, 로컬저장소에 커밋한 파일들을 원격저장소에 추가하는 작업)  
**브랜치(branch)** : 하나의 프로젝트를 여러 갈래로 나누어 관리 가능하게 하는 기능, 최초 Git 초기화 시에는 기본적으로 **master** 브랜치가 생성   

![gitstate](src/gitstate.png)  

<Git의 3가지 상태>  

Committed : 데이터가 로컬 저장소에 안전하게 저장  
Modified : 수정한 파일을 아직 로컬 저장소에 커밋하지 않음  
Staged : 현재 수정한 파일을 곧 커밋할 것임을 의미  


## **(2) Git 설치**
---
### 2.1 Git SCM 접속 후 운영체제에 맞는 설치 파일 다운로드  
Git SCM URL : <https://git-scm.com/>  

### 2.2 Git Bash에서 깃 버전 확인
> ### git --version  
![버전확인](src/versionCheck.png)  

### 2.3 Git 사용자 등록 및 확인  
- Git 설치 후에는 Git의 사용 환경을 적절하게 설정해 주어야 함 (사용자 설정)   
- **git config** 명령어로 설정 내용을 확인하고 변경할 수 있음   
> ### git config --global user.name "name"  
> ### git config --global user.email "emailAddress"  
![사용자등록](src/user.png) 
- 프로젝트 마다 다른 설정을 하고 싶다면 --global 옵션을 제거  
-  --global 옵션을 넣는다면 이 컴퓨터에서 작업하는 모든 프로젝트에 공통으로 적용 

> ### git config --list  

![확인](src/userCheck.png)  
- --list 옵션을 통해 사용자 확인 가능  

## **(3) Git 저장소 생성**
---
- Git 저장소를 사용하는 방법은 2가지 존재  
     ### **3.1** 아직 버전관리를 하지 않는 로컬 저장소를 Git 저장소로 사용  
     ### **3.2** 다른 어딘가에서 Git 저장소를 Clone하여 사용  

### 3.1.1 로컬저장소로 사용할 폴더 생성  

![local](src/local.png)  
- SE_gitHub 폴더 생성  

### 3.1.2 해당 저장소로 위치 이동  
- 방법 1 ) **cd** (change directory) 명령어 사용  
        현재 디렉토리의 위치를 변경하는 명령어  

> cd [로컬 저장소 경로]  

![cd](src/cd.png)  

- 방법 2 ) 해당 로컬 저장소 폴더에서 마우스 우 클릭 후 Git Bash Here 실행  


![gitbash](src/gitbash.png)  
![이동완료](src/gitbash2.png)  

### 3.1.3 Git 원격 저장소 생성  
- 버전 관리를 하지 않는 기존 프로젝트를 Git으로 관리하고 싶은 경우에서 위의 과정을 통해 프로젝트의 디렉토리로 이동한 상태  
- 이동한 후 **git init** 명령어 실행  
- **git init**은 버전 관리를 하고 싶은 폴더에서 초기화를 하는 준비  
현재 디렉토리를 기준으로 Git 저장소가 생성됨 (.git 이라는 하위 디렉토리 생성) 

> git init  

![init](src/init.png)   

![gitFolder](src/gitfolder.png)  

- .git 폴더 생성됨 (새로운 Git 저장소가 생성)  

----

### 3.2.1 복제할 원격 저장소 Clone 주소 복사  

### 3.2.2 git clone 명령어 사용  
- 3.1 번은 버전관리를 하지 않는 기존 프로젝트를 Git으로 관리하는 방법이고, 이 부분에서 설명할 방법은 **기존 저장소를 복사**하는 방법  
- **git clone**은 다른 프로젝트에 참여하거나 Git 저장소를 복사하고 싶을 때 사용함  
- **git clone** 명령을 통해 로컬 저장소에 GitHub에 있던 원격 저장소를 복사 할 수 있음  
> git clone [URL]  

![clone](src/clone.png)  

## **(4) Git 명령어**
----
### 4.1 원격저장소 조작  
- 원격 저장소를 조작할 수 있는 명령어로 **git remote** 사용  
>  git remote add [remote repository의 이름] [원격 저장소 github URL]  

![remote](src/remote.png)  

- remote repository 는 origin을 주로 사용
- 원격 저장소와 해당 로컬 저장소를 연결할 수 있음  

> git remote 

![remoteCheck](src/remoteCheck.png)  
- 추가한 원격저장소의 이름 목록을 확인  

### 4.2  파일 추적하기  

![문서생성](src/filecreate.png)  
- 로컬저장소에 Markdown_tutorial.md 문서 생성 후  
 **git add** 를 사용하여 파일 추적 가능
> git add [파일이름]  

![add](src/add.png)  
- add는 파일을 **추적**함  
따라서 어떤 파일을 만들고 add를 하기 전에 git status를 실행하면 Untracked 상태를 나타냄 (잠시 후 다룰 예정)

> git add .
- . 을 넣으면 모든 파일을 한번에 추적 가능 

### 4.3 파일 상태 확인하기
- **git status** 는 현재 나의 로컬 폴더와 Git과의 상태를 싱크 상태를 체크
> git status  

![초기상태](src/status1.png)
- on branch master는 현재 작업중인 브랜치가 master 임을 의미  
(기본 branch : master)  

- 현재, 로컬 저장소에 파일을 추가하고 아직 커밋(뒤에서 다룰 예정)하지 않았기 때문에 No commits yet 상태  

- new file : Markdown_tutorial.md 추가 된 파일 나타냄  

< 파일 상태 >
>- 1. untracked 상태 : 추적되지 않고 있는 파일, 즉 파일을 생성한 후 한번도 add 하지 않은 상태  
>- 2. Tracked 상태 : 파일이 git에 의해 그 변동사항이 추적되는 상태  
>        - 2.1 Staged 상태 : 파일 수정 후에 Staging area에 올라가 있는 상태  
>        - 2.2 Unmodified 상태 : 현재 파일이 최신 커밋 파일과 비교하여 바뀐 것이 없는 상태  
>        - 2.3 Modified 상태 : 현재 파일이 커밋 파일과 비교하여 바뀐게 있는 상태  

### 4.4 변경사항 확정 하기
- **git commit** 은 추가 된 파일이나 폴더의 내용을 저장소에 보낼 때 사용 (변경사항을 확정함)

> git commit -m "커밋 메세지(변경된 메세지 내용 입력)"

![commit](src/commit1.png)

- -m은 커밋메세지 옵션

> git commit -a 
- 별도의 add 명령어를 사용하지 않고 수정된 파일에 대해 add와 commit을 한번에 수행

> git commit -am "커밋 메세지"
- a와 m의 옵션을 합침  

![aftercommit](src/aftercommit.png)
- 커밋 한 후에 status 명령을 통해 상태 확인
- 더 이상 커밋할 것이 없음을 의미

### 4.5 커밋 히스토리 조회하기
- **git log** 로 로컬저장소의 커밋 히스토리를 탐색  
> git log  

![log](src/log.png)  
- 커밋 내용을 출력  

### 4.6 내 로컬저장소에서 원격저장소로 보내기
- 내 로컬 저장소에서 커밋한 파일들은 아직 내 로컬 저장소에만 있기 때문에 원격 저장소에서 다룰 수 없음    
- **git push** 를 사용하여 로컬저장소에 커밋한 파일들을 원격저장소에 추가  
> git push [원격 저장소 이름] [브랜치명]  

![push](src/push.png)  

![pushgithub](src/pushgithub.png)

- push 하고 나면 github에서 커밋 내용을 볼 수 있음
- push 없이 커밋만 하면 현재의 변경 내용은 아직 로컬 저장소 안에 머물고 있음, 이 변경 내용을 원격 서버로 올리려면 **push**가 필요  

### 4.7 **브랜치(branch)** 사용

- 하나의 프로젝트를 여러 갈래로 나누어 관리하고 싶기 때문에 사용

- 각각의 독립된 브랜치에서 마음대로 소스코드를 변경하여 작업한 후 원래 버전과 비교하여 또 하나의 새로운 버전을 만들어 냄

### 4.7.1 branch 목록 보기
> git branch

![branch1](src/branch1.png)

- 현재 브랜치 목록을 살펴봄
- master 브랜치 (기본 브랜치) 가 존재하며, \* 는 현재 활성화 된 브랜치

### 4.7.2 branch 생성 하기  
> git branch [브랜치명]  

![branchFirst](src/firstBranch.png)  
- 브랜치 생성  

- 독립적인 공간을 생성함

- 새로 만든 firstBranch는 master와 완전히 동일한 상태를 가진 공간 ( master 브랜치에서 브랜치를 생성했기 때문 )  

![수정](src/vi.png)  
- 생성한 firstBranch 에서 문서를 편집하기 위한 명령  

![수정](src/modi.png) 

- 문서를 편집함  

![과정](src/addstatus.png) 

- add를 통해 변경된 파일을 추적하게 함  
- status 를 통해 상태 확인  

![브랜치커밋](src/branch.png)

- firstBranch에 추가 한 내용을 커밋함 

- 브랜치에서 수정을 한 후에 커밋하면 firstBranch 에만 기록되며 master 브랜치에는 어떤 영향도 주지 않음  


        * 주의 ) 새로 만든 브런치를 원격 저장소로 전송하기 전  까지는 다른 사람들이 접근할 수 없음. 따라서, git push origin [브랜치명] 을 통해 push 해야함  
            
![사진](src/push1.png)

- push 명령을 통해 원격 저장소로 전송  

![브랜치깃허브](src/branchgit.png)  
- 원격 저장소에 생성된 firstBranch 확인 가능   

![수정된firstBranch](src/addbranch.png)  
- firstBranch 수정 된 내용 확인 가능   

### 4.7.3 브랜치 이동 하기
> git checkout [브랜치명]  

![checkout](src/checkout.png)  

- 독립된 작업 공간인 브랜치를 자유롭게 이동하기 위해 사용   
- **git checkout** firstBranch 를 통해 master 에서 firstBranch로 브랜지를 이동함

> git checkout -b [브랜치명]  
- 브랜치 생성 후 바로 이동 (생성과 이동을 동시에 가능) 

### 4.7.4 브랜치 병합하기  
- 한 프로젝트를 여러 명이서 협업을 할 때면 각자의 브랜치에서 작업을 한 것을 합쳐야 할 때가 있음
- 이때, 브랜치를 병합하는 명령어를 사용  
- 브랜치 병합 방법에는 2 가지가 존재

### 1) **merge** 이용
> git merge [브랜치명]  
- **merge**는 하나의 브랜치와 다른 브랜치의 변경 이력 전체를 합치는 방법

![merge](src/merge.png)
- secondBranch에 작성한 파일을 master 브랜치에 병합한 것  

- master 브랜치로 이동 후에 **merge** 사용

### 2) **rebase** 이용
> git rebase [브랜치명]  
- rebase는 말 그대로 re-base로 브랜치의 base를 다시 설정한다는 의미  
- 모든 커밋들이 합쳐지지 않고 각각 master 브랜치에 추가됨
- rebase는 커밋을 하나로 정리하여 푸시하기 때문에 깔끔함  

> Merge는 Merge 커밋 기록이 추가로 남게 되지만, Rebase는 브랜치 결합 시 Merge 커밋 기록이 남지 않음.  
따라서 마치 하나의 브랜치에서 작업한 것 처럼 보임

### 4.8 원격저장소에서 내 로컬저장소로 보내기
- 다른 사람이 원격저장소에 업데이트 한 파일이 있다면, 가장 최신의 상태로 작업하기 위해서 pull을 반드시 사용  
- **git pull** 을 사용하여 원격저장소와 내 로컬저장소의 상태를 동일하게 만듦

> git pull [원격 저장소이름] [브랜치명]
- 원격저장소의 변경사항을 가져와서 로컬저장소의 브랜치에 합치는 작업
- 변경 내용이 로컬 작업 디렉토리에 받아지고, 병합됨 

![commitpush](src/commitpush.png)
- 원격 저장소에서 commit 후 push 함

![pull](src/pull.png)  
- 로컬 저장소로 최신 변경 내용을 가져오기 위해 pull 사용

### 4.9 과거의 커밋으로 돌아가기 

- 커밋 했던 내용이 잘못되어서 이전의 상태로 되돌려야 하는 경우 발생 가능  
- **git reset** 명령을 통해 과거의 커밋으로 돌아감   
> git reset [옵션] [커밋ID] 

| 옵션 | staging area | working directory  |
|:-------|:---------:|---------:|  
| --mixed (default) | 초기화 | 변경 X |
| --hard | 초기화 | 초기화 | 
| --soft | 변경 X | 변경 X| 

- --mixed : 옵션을 적지 않으면 mixed로 동작, 돌아가려는 이력 이후에 변경된 내용에 대해서는 남아있지만 인덱스는 초기화  
- --hard : 돌아가려는 이력 이후의 모든 내용을 초기화  
- --soft : 돌아가려 했던 이력으로 되돌아 갔지만, 이후의 내용과 해당 내용의 인덱스도 그대로 있음

![commit](src/modicommit.png)  

- 수정 후 커밋함  

![mistakelog](src/mistakelog.png)  

- log 살펴보면 이 전에 커밋한 내용이 출력 됨

![reset](src/resethard.png)  

- reset --hard 를 통해 과거의 커밋으로 돌아감

- hard는 이 전 커밋을 삭제하기 때문에 더 이상 my mistake 커밋이 뜨지 않음  


### 4.10 태그(tag) 남기기  
- 태그는 커밋을 참조하기 쉽도록 알기 쉬운 이름을 붙이는 것  
- 한 번 붙인 태그는 브랜치처럼 위치가 이동하지 않고 고정됨  
> git tag [태그이름] [커밋아이디]  

> git tag 

![tag](src/tag.png)
- 식별자는 git log 하면 알 수 있음  
- firstTag 이라는 이름의 태그를 생성
- **git tag** 를 통해 tag 확인 


## **(5) 명령어 목록**  
---
| 명령어 | 사용 여부 | 설명 부분 링크 |  
|:-------|:---------:|--------------:|
| add | O |https://github.com/seyxxn/GitHubPractice#42--%ED%8C%8C%EC%9D%BC-%EC%B6%94%EC%A0%81%ED%95%98%EA%B8%B0|
| branch | O | https://github.com/seyxxn/GitHubPractice#47-%EB%B8%8C%EB%9E%9C%EC%B9%98branch-%EC%82%AC%EC%9A%A9|
| checkout | O |https://github.com/seyxxn/GitHubPractice#473-%EB%B8%8C%EB%9E%9C%EC%B9%98-%EC%9D%B4%EB%8F%99-%ED%95%98%EA%B8%B0|
| clone | O |https://github.com/seyxxn/GitHubPractice#322-git-clone-%EB%AA%85%EB%A0%B9%EC%96%B4-%EC%82%AC%EC%9A%A9|
| commit | O | https://github.com/seyxxn/GitHubPractice#44-%EB%B3%80%EA%B2%BD%EC%82%AC%ED%95%AD-%ED%99%95%EC%A0%95-%ED%95%98%EA%B8%B0|
| config | O |https://github.com/seyxxn/GitHubPractice#23-git-%EC%82%AC%EC%9A%A9%EC%9E%90-%EB%93%B1%EB%A1%9D-%EB%B0%8F-%ED%99%95%EC%9D%B8|
| init | O |https://github.com/seyxxn/GitHubPractice#313-git-%EC%9B%90%EA%B2%A9-%EC%A0%80%EC%9E%A5%EC%86%8C-%EC%83%9D%EC%84%B1|
| log | O | https://github.com/seyxxn/GitHubPractice#45-%EC%BB%A4%EB%B0%8B-%ED%9E%88%EC%8A%A4%ED%86%A0%EB%A6%AC-%EC%A1%B0%ED%9A%8C%ED%95%98%EA%B8%B0|
| merge | O |https://github.com/seyxxn/GitHubPractice#1-merge-%EC%9D%B4%EC%9A%A9|
| pull | O | https://github.com/seyxxn/GitHubPractice#48-%EC%9B%90%EA%B2%A9%EC%A0%80%EC%9E%A5%EC%86%8C%EC%97%90%EC%84%9C-%EB%82%B4-%EB%A1%9C%EC%BB%AC%EC%A0%80%EC%9E%A5%EC%86%8C%EB%A1%9C-%EB%B3%B4%EB%82%B4%EA%B8%B0|
| push | O | https://github.com/seyxxn/GitHubPractice#46-%EB%82%B4-%EB%A1%9C%EC%BB%AC%EC%A0%80%EC%9E%A5%EC%86%8C%EC%97%90%EC%84%9C-%EC%9B%90%EA%B2%A9%EC%A0%80%EC%9E%A5%EC%86%8C%EB%A1%9C-%EB%B3%B4%EB%82%B4%EA%B8%B0|
| rebase | X |https://github.com/seyxxn/GitHubPractice#2-rebase-%EC%9D%B4%EC%9A%A9|
| remote | O | https://github.com/seyxxn/GitHubPractice#41-%EC%9B%90%EA%B2%A9%EC%A0%80%EC%9E%A5%EC%86%8C-%EC%A1%B0%EC%9E%91|
| reset --hard | O | https://github.com/seyxxn/GitHubPractice#49-%EA%B3%BC%EA%B1%B0%EC%9D%98-%EC%BB%A4%EB%B0%8B%EC%9C%BC%EB%A1%9C-%EB%8F%8C%EC%95%84%EA%B0%80%EA%B8%B0|
| status | O|https://github.com/seyxxn/GitHubPractice#43-%ED%8C%8C%EC%9D%BC-%EC%83%81%ED%83%9C-%ED%99%95%EC%9D%B8%ED%95%98%EA%B8%B0|
| tag | O | https://github.com/seyxxn/GitHubPractice#410-%ED%83%9C%EA%B7%B8tag-%EB%82%A8%EA%B8%B0%EA%B8%B0|
