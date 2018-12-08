# SSHDemo
Demo : use SSH key


#### 빅데이터전공 20155342 지현규   
GIT with SSH  
=============================
Explanation of Git's SSH
------------------------
```Secure Shell을 이용하여 로그인 없이 원격저장소 사용하기 
> 기존 HTTPS로 사용했을 경우 복잡한 설정 없이도 원격저장소에 PUSH 가능!  
> 하지만 PUSH,원격저장소에 접속할마다 아이디와 PW를 입력해야하는 번거로움  
> SSH 통신방식을 이용하여 원격저장소를 접근하면 단점해결!  
```
## How to Use
![generatesshkey](https://user-images.githubusercontent.com/43162502/49690154-72c11c00-fb6f-11e8-97e9-2d372eaa2863.png)

### 1. SSH 공개키 만들기
* ssh-keygen이라는 프로그램으로 키를 생성
  > ssh-keygen프로그램은 리눅스나 Mac의 ssh패키지에 포함    
  > 윈도우는 MSysGit패키지에 포함 
* Git bash : ssh-keygen 입력
  1. 키를 저장할 경로입력(기본적으로 ~/.ssh 디렉토리에 저장)  
  2. 키의 암호 두 번 입력(암호를 비워두면 키를 사용할 때 암호를 묻지 않음) 
### 2.	~/.ssh 디렉토리에 SSH key생성확인
```id_rsa : 개인키 / id_rsa.pub : 공개키```
-	생성된 비밀번호 키는 SHA256알고리즘을 통해 RSA형식으로 생성
### 3.	private키는 개인의 컴퓨터 / public키는 서버컴퓨터에 복사하여 저장
----------------------------------------------------------------------
> <원리>  
> -	키를 생성하면 개인컴퓨터에 private / public key가 생성된다.  
> -	Public key를 접속하고 싶은 서버에 복사하여 등록한다 
> -	서버컴퓨터에 접속할경우 개인컴퓨터에 있는 private키와 서버에 있는 public키가 짝꿍을 이룬다면 비밀번호 입력절차 없이 안전하게 접속가능  
> - __공개키 유출조심__
----------------------------------------------------------------------
* 공개키 내용출력
  +	cat id_rsa.pub
* 내용을 복사
* Github.com의 settings 접속
   + SSH and GPG Keys 탭에 내용 붙여넣기(Title : 제목, Key : 내용) – add SSH key
   
   ![github1](https://user-images.githubusercontent.com/43162502/49690157-7bb1ed80-fb6f-11e8-8a5c-b1402aa79355.png)
![github2](https://user-images.githubusercontent.com/43162502/49690159-7e144780-fb6f-11e8-92f3-77265c4bff66.png)



----------------------------------------------------------------------
# SSH로 GitHub사용 : Clone과 Push 성공!

![success](https://user-images.githubusercontent.com/43162502/49690156-79e82a00-fb6f-11e8-90e0-42c7a3851dbb.png)

* 주의 Clone시 HTTPS가 아닌 SSH주소 복사

![github3](https://user-images.githubusercontent.com/43162502/49690160-7f457480-fb6f-11e8-8b14-feefa3b6fd09.png)
![github4](https://user-images.githubusercontent.com/43162502/49690162-8076a180-fb6f-11e8-9ae0-857e540890bf.png)

#### 빅데이터전공 20155342 지현규   
