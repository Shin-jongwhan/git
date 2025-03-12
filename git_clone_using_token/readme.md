### 250312
## token을 사용하여 clone 하는 방법
### 먼저 token을 발급해야 하는데, project 별로 생성할 수도 있고, 계정 별로 생성할 수도 있다. 둘 줄 어느 걸로 이용해도 된다.
#### ![image](https://github.com/user-attachments/assets/f113f4e3-5a93-4a34-b1a2-42a190f9326f)
### <br/>

### git clone
#### ex)
#### repo_url : https://를 제외한 \[domain_name or IP\]/\[user_name\]/\[project\].git과 같은 형태의 url
```
git clone https://oauth2:[token]@[repo_url] -b master test
```
