# SKT FLY AI 4기
## 4주차: Git 다루기 기초 복습
### 1. 초기 설정
- ```git --version```: git version 확인
- ```git config --global core.autocrlf true``` : window의 경우 엔터 방식 차이로 인한 오류 방지, linux의 경우 true를 input으로 변경하면 된다.
  
- 사용자 구분을 위한 설정
    - ```git config --global user.name "본인 이름"```
    - ```git config --global user.email "본인 이메일"```
    - ```git config --global init.defaultBranch main``` : 초기 브랜치명 변경
    - ```git config --global --list``` : 초기 설정 확인

#### 2. 프로젝트 생성 및 연결
- 로컬에서 원격 연결 (로컬에 생성한 파일이 있는 경우)
  - cmd or prompt 창에서 cd 명령어로 원격에 저장하고 싶은 폴더 위치로 이동<br>
    - ```cd "절대경로 or 상대경로"```
  - 원격과 연동되는 git 저장소 생성
    -```git init```
  - git hub에 새로운 repository를 생성한다.
    - README.md 파일을 생성하지 않는다.
  - 생성된 원격 저장소와 로컬 저장소를 연결한다.
    - ```git remote add origin "repository 주소"```
  - 특정 파일 및 폴더 배제
    - 일부 파일의 경우 공유되면 않되거나 민감한 정보들이 있을 수 있다.
    - .gitignore 파일을 생성하고 저장하면 해당 파일은 업로드 되지 않는다.
  - 원격 저장소에 저장
    - 저장 전 현재 상황 확인
        - ```git status```
        - 해당 폴더에서 생성 및 수정, 삭제 등의 상태가 나타납니다.
        - 아직 로컬에서만 발생한 상황들 입니다.
    - 파일 stage 영역에 업로드
      - ```git add .``` : 해당 폴더의 모든 파일 변경사항 업로드
      - ```git add "특정파일"``` : 특정 파일의 변경사항 업로드
    - 파일 commit 하기
      - ```git commit -m "커밋 명"```
    - 로컬 저장소 업로드
      - ```git push -u origin main``` : -u: 초반에 한 번만 해당 명령어로 push하고 이후부터는 ```git push```로 업로드 가능하다.

- 원격에서 로컬연결 (원격 저장소 파일 내려받기)
  - cmd or prompt 창에서 cd 명령어로 원격에 저장하고 싶은 폴더 위치로 이동<br>
    - ```cd "절대경로 or 상대경로"```
  - 원격과 연동되는 git 저장소 생성
    -```git init```
  - 생성된 원격 저장소와 로컬 저장소를 연결한다.
    - ```git remote add origin "repository 주소"```
  - 내려받기
    - ```git pull origin main```
