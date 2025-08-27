### 250827
# 리눅스 서버에 HTTPS 인증서 설정 방법
### full chain 말고 중간 발급자(CA) 인증서만 등록해주면 된다.
```
# 인증서 복사
cp [CA_cert] /usr/local/share/ca-certificates/

# update ca cert
update-ca-certificates
```
### <br/>

### 그 다음 다시 https로 git clone을 시도해본다.
### token 사용시 다음과 같이 사용한다.
```
git clone https://oauth2:[token]@[git_url]/[user_or_group]/[repository_name].git
```
#### <img width="697" height="149" alt="image" src="https://github.com/user-attachments/assets/b3517999-fb4d-420f-9b90-4601db7d62f2" />
