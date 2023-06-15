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

## git pull
### 특정 branch 를 이용하고 있을 때, 해당 branch 의 파일 변경 사항들을 가져온다.
```
git pull origin <branch name>
```

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
