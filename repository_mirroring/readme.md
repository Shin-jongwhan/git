### 250611
# repository 간 업데이트 시 연동(synchronization) 방법
### 나는 회사 gitlab에 있는 repository를 github에 공개할 목적으로 mirroring을 하였다.
### 1. 아래와 같이 branch를 하나 만들고 protected로 만든다.
#### ![image](https://github.com/user-attachments/assets/c0b89057-07b7-40bd-a7d5-3ce006d654bf)
### <br/>

### 2. github에서 token을 발급한다. 그리고 적절한 권한을 설정한다. 이하 내용을 생략
#### ![image](https://github.com/user-attachments/assets/a5f86974-2c6b-435c-8ee8-235e74d89558)
### <br/>

### 3. mirroring 할 repository branch의 setting으로 다시 가서 mirroring을 등록한다.
### URL은 아래와 같이 한다.
```
https://Theragen-Bio@github.com/Theragen-Bio/DeepOmicsFFPE-PLUS.git
```
### 그리고 password를 선택하고, 여기에 발급한 토큰을 넣는다.
### 그리고 아래 mirror repository를 누르면 끝난다 ! 매우 쉽다.
#### ![image](https://github.com/user-attachments/assets/e83babff-4932-4672-96ec-347f95a94a69)
