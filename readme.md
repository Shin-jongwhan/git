#### 230615
# git 사용법 정리
### <br/><br/><br/>

## git status
### 현재 branch 가 어디인지, 어떤 branch 가 있는지 알려준다.
```
git branch
```
#### ![image](https://github.com/Shin-jongwhan/git/assets/62974484/6cf2b64d-da4d-4a4c-baed-1df912ce0aae)
### <br/><br/><br/>

## git branch
### branch 생성 방법
```
# 기본으로 생성하는 방법
git branch [branch 이름] 

# 특정 branch 에서부터 생성하 방법
git branch [branch 이름] [가져올 branch]
```
### <br/>

### branch 이동 방법
```
git checkout [branch 이름]
```
### <br/><br/><br/>

## 원격 branch 이동 방법
### 원격 branch 를 검색하려면 -a 옵션을 쓴다.
```
git branch -a
```
#### ![image](https://github.com/Shin-jongwhan/git/assets/62974484/8082d35d-614e-45bd-92fe-17a3801b8b5d)
### git checkout 으로 원격 저장소에 있는 branch 를 가져온다.
```
git checkout -b 1.0.0 remotes/origin/1.0.0
```
### 저장소가 잘 바뀌었는지 git status 로 확인해보고, test 를 진행해본다.
```
touch test
git add .
git commit -m "remote branch jhshin_test_230623"
git push origin 1.0.0
```
### 업데이트가 1.0.0 branch 로 잘 된다.
#### ![image](https://github.com/Shin-jongwhan/git/assets/62974484/f187fe41-efea-471a-86bf-2c875c62c9e8)

## git pull
### 특정 branch 를 이용하고 있을 때, 해당 branch 의 파일 변경 사항들을 가져온다.
```
git pull origin <branch name>
```
### <br/><br/><br/>

## 파일 추가, 수정 등 업데이트 하는 방법
### 먼저 파일 변경 사항을 git 에 업데이트한다.
```
# add . 로 전체 변경 사항을 적용한다.
git add .
git commit -m 'update message'
git push

# origin 원격 저장소에 업로드하고 싶다면
git push origin [branch 이름]
```
### <br/><br/><br/>

## git tag
### 아래 사이트를 참고하였음
#### https://dev-coco.tistory.com/51
### tag 는 읽기 전용으로 git commit id 에 대한 태깅을 한다.
### 태그는 특정 commit 에 대한 내용을 수정할 수는 있으나, 태그는 수정이 불가능하다.
### 사용 목적은 정해져 있지 않지만 보통 소프트웨어의 버전을 release 할 때 사용한다.
#### ex) v1.0.1 ...
### <br/>

### git tag 조회
```
git tag

# 원하는 태그명만 보고자 할 경우
git tag -l v1.0*
```
#### ![image](https://github.com/Shin-jongwhan/git/assets/62974484/df7b5805-f6a3-42f1-8b16-630a0825a343)
### <br/>

### tag 는 Lightweight와 Annotated 두 가지 종류가 있다.
- Lightweight Tag : 단순히 버전같은 태그이름만 남기는 태그
- Annotated Tag : 태그를 만든 사람의 이름, 이메일, 태깅 날짜, 태그 메시지까지 저장한다. GPG(GNU Privacy Guard)로 서명도 할 수 있다.
### <br/>

### `Lightweight Tag` 방법
```
git tag v1.0.1

# git tag 정보 조회
git tag
```
### <br/>

### `Annotated Tag` 방법
### git tag -a 옵션을 쓰면 되고, -m 으로 해당 태그에 대한 정보와 작성자에 대한 정보를 쓴다.
```
git tag -a v1.0.2 -m "jhshin test"

git show v1.0.2
```
### 메세지 몇 줄 아래 보면 jhshin test 라고 적혀 있다.
#### ![image](https://github.com/Shin-jongwhan/git/assets/62974484/afa5dd96-f093-46a8-b771-86fe610452de)
### <br/>

## git tag 원격 저장소에 push
```
git push origin [tag name]
```
### gitlab 에서는 다음과 같이 tag 리스트들이 보인다.
#### ![image](https://github.com/Shin-jongwhan/git/assets/62974484/fc1d22f6-265b-4b10-a6eb-c861d2432c98)
### <br/>

## git tag 삭제
- 로컬 : git tag -d \[tag 명\] 으로 삭제한다.
- 원격 저장소 : git push origin :\[tag 명\] 으로 삭제한다.
```
git tag -d v1.0.1

git push origin :v1.0.1
```
### 삭제 확인
#### ![image](https://github.com/Shin-jongwhan/git/assets/62974484/bd6ecf57-e4b3-4ab9-a44e-24d6d361a7f8)
### <br/><br/><br/>
