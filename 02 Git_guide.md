# Github를 위한 기초 Git 사용법

### 1. 시작 전 준비

#### (1) Git 설치

- Github 사용을 위해 [https://git-scm.com/](https://git-scm.com/) 에서 Git을 다운받아 설치해 주세요.

- Git은 Windows에서는 Git Bash를 통해, mac os에서는 터미널에서 실행하시면 됩니다.

  -  터미널에서 git --version을 입력하시면 설치가 완료되었는지 확인할 수 있습니다.

    ![](/Users/jeongsuhyeon/Git/git version.png)

#### (2) Github 가입

- 우선, 깃허브 [https://github.com/](https://github.com/)에 가입하셔서 새로운 repository를 설정해 줍니다.

<img src="/Users/jeongsuhyeon/Git/new repository.PNG" style="zoom:75%;" />



### 2.  Git 세팅

#### (1) 최초 사용자 설정

- `git` 설정 (user.name & user.email) : **최초 1회 설정**

- user.email은  **Github 아이디**로 작성하셔야 합니다.

  ```shell
  $ git config --global user.name "suhyeon4820"
  $ git config --global user.email "bananacco@naver.com"
  ```

  

#### (2) Git으로 프로젝트 관리 시작 : `git init`

- 폴더를 하나 생성하고, Github에 업로드 할 파일을 작성한다. 

- 터미널에서 생성한 폴더가 있는 위치로 이동한 이후 `git init` 명령어로 git 관리를 시작한다.

  ```shell
  $ git init
  ```

  

#### (3) Commit을 위한 Staging : `git add`

- 현재 코드 상태의 스냅샷을 찍기 위한 파일 선택 (== Staging Area에 파일 추가)

  ```shell
  $ git add [파일 이름] # .은 모든 변경 사항을 staging area로 올림
  ```



####  (4) 버전 관리를 위한 스냅샷 저장 : `git commit`

- 현재 상태에 대한 스냅샷을 commit 하여, 버전 관리를 진행한다.

  ```shell
  $ git commit -m "커밋 메시지"
  ```

  

#### (5)  원격 저장소 정보 추가 : `git remote`

- Github 원격(remote) 저장소(repository)를 생성하고 폴더와 연결한다.

- 새로운 원격 저장소가 추가될 때만 입력한다.

  ```shell
  $ git remote add origin [github 원격 저장소 주소]
  ```



#### (6) 원격 저장소로 코드 `git push`

- 최종적으로 Github 원격 저장소에 push한다.

  ```shell
  $ git push origin master
  ```

  

#### (7) 그 외 명령어

- 현재 `git` 의 상태를 조회 `git status`

   ```shell
  $ git status
  ```

- 버전 관리 이력을 조회

  ```shell
  $ git log
  ```


- 폴더명 변경

  ```shell
  $ git mv 바꿀파일명 바뀐파일명
  ```

- 파일, 폴더 삭제

  ```
  $ git rm -rf 파일명 = 원격, 로컬 저장소에서 삭제
  $ git rm -r --cached 파일명 = 원격 저장소에서 삭제
  ```

##  3. `READEME.md`

> 원격(remote) 저장소(repository)에 대한 정보를 기록하는 마크다운 문서. 일반적으로 해당 프로젝트를 사용하기 위한 방법 등을 기재한다.



#### (1) (자신만의) TIL 원칙에 대한 간단한 내용 추가

- 마크다운 작성법 pdf에서 배우고 실습한 내용을 토대로 `README.md` 파일을 작성한다.
- 형식은 자유롭게 작성하되 마크다운 문법(의미론적)을 지켜서 작성한다.



#### (2) 저장 후 버전관리 : `add` , `commit` , `push`

- 작성이 완료되면 아래의 명령어를 통해 commit 이력을 남기고 원격 저장소로 push한다.

  ```shell
  $ git add README.md
  $ git commit -m "add README.md"
  $ git push origin master
  ```

  

## 4. 추가 학습 내용 관리

#### (1) 추가 내용 관리

- 폴더 내에서 학습을 원하는 내용의 폴더를 생성하고 파일들을 생성한 후 작업을 진행한다.

  ```shell
  $ mkdir python
  ```

#### (2) 변경 사항을 저장하고, 원격저장소로 옮긴다.

- 업데이트가 완료되면 아래의 명령어를 통해 commit 이력을 남기고 원격 저장소로 push한다.

  ```shell
  $ git add .
  $ git commit -m "학습 내용 추가"
  $ git push origin master
  ```

  