# branch command

- 브랜치 생성

```bash
$ git branch 브랜치명
```

- 브랜치 목록

```bash
$ git branch
```

- 브랜치 이동

```bash
# git checkout 까지만 입력한 상태에서 tab*2 -> checkout 가능한 브랜치명 확인 가능
$ git checkout 브랜치명
(브랜치명) $
```

```bash
$ git log --oneline
197992b (HEAD -> master, origin/master, origin/HEAD) 20210625 | modified 01_git_repository # HEAD: 현재 우리가 속한 위치
```



```bash
$ git log --all --graph --oneline # --all: 모든 브랜치의 로그 확인
# --graph: 그래프로 브랜치가 어떤 정보를 갖고 생성됐는지와 각 브랜치의 활동범위 구별
```



- 브랜치 생성+이동

```bash
$ git checkout -b 브랜치명
```



- 브랜치 병합

```bash
(master) $ git merge 브랜치명 # 반드시 master 브랜치에 다른 브랜치를 병합, 커밋과정 	자동으로 진행됨
# 커밋메세지를 변경하고 싶으면 1. i 2. 수정 3. esc 4. :wq(변경 저장), 					:q(기본값으로 저장)
```



- 브랜치 삭제

```bash
$ git branch -d 브랜치명
```



- 브랜치 강제 삭제

```bash
$ git branch -D 브랜치명 # merge가 되지 않은 브랜치는 강제로 삭제해야 함
```



## 3가지 병합 상황

### 1. fast-forward

"다른 브랜치를 생성한 후, master 브랜치에 변경 사항이 없을 때"

​	병합 명령어 입력 시, 별도의 과정없이 병합됨



### 2. 3-way Merge

"현재 브랜치(master)가 가리키는 커밋이 merge할 브랜치의 조상이 아니라면 깃은 현재 브랜치와 병합할 브랜치의 커밋 2개와 두 브랜치의 공통조상 하나를 사용한다"

#### 1. 새로운 브랜치 signup 생성

#### 2. signup 브랜치에서 signup.py 생성

- git add, commit 잊지 말기

#### 3. master 브랜치에서 new folder 생성

- git add, commit 잊지 말기

#### 4. master 브랜치와 signup 브랜치 병합

#### 5. signup 브랜치 삭제



### Merge Conflict

"두 개의 브랜치가 동일한 파일의 동일한 위치를 수정하고 merge 하려고 할 때 발생하는 현상

단, 동일 파일을 수정했다고 하더라도 서로 다른 영역을 수정한다면 merge conflict는 발생하지 

않는다"

- git이 자동으로 병합하지 못하는 상황
- 충돌이 난 부분을 수정하고 merge(add, commit)

#### 1. 새로운 브랜치 hotfix 생성

#### 2. hotfix 브랜치에서 b.txt에 새로운 내용 입력

- git add, commit

#### 3. master 브랜치에서 b.txt에 새로운 내용 입력

- git add, commit

#### 4. master 브랜치와 hotfix 병합

