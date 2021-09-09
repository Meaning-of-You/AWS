# EC2 서버 접속하기

> PuTTY 활용



### PuTTY 설치

##### PuTTY

SSH 및 텔넷 클라이언트

##### PuTTY 설치하기

1. 사이트 접속

https://putty.org/

![image-20210909215225585](EC2_Putty.assets/image-20210909215225585.png)

2. 응용 프로그램 다운로드

![image-20210909215404346](EC2_Putty.assets/image-20210909215404346.png)

3. PuTTY 실행하기

![image-20210909215605070](EC2_Putty.assets/image-20210909215605070.png)



### Private Key 생성

1. PuTTYgen 설치

https://www.puttygen.com/download-putty

![image-20210909221339387](EC2_Putty.assets/image-20210909221339387.png)

2. 탄력적 IP 주소를 생성할 때 얻은 .pem 파일 확인

![image-20210909221004610](EC2_Putty.assets/image-20210909221004610.png)

3. PuTTYGen 실행 후 Conversions > Import key 선택

![image-20210909221522888](EC2_Putty.assets/image-20210909221522888.png)

4. .pem 파일을 추가하고 Save private key 클릭

![image-20210909221856921](EC2_Putty.assets/image-20210909221856921.png)

![image-20210909221922064](EC2_Putty.assets/image-20210909221922064.png)

4. 확장자를 .ppk로 지정 후 저장

![image-20210909222034439](EC2_Putty.assets/image-20210909222034439.png)



### PuTTY 설정하기

1. 탄력적 IP 주소 확인

- 앞서 할당 받은 IP 주소 복사

![image-20210909220109286](EC2_Putty.assets/image-20210909220109286.png)

2. PuTTY에 IP address 설정

![image-20210909220219264](EC2_Putty.assets/image-20210909220219264.png)

3. Connection > SSH > Auth 설정

- 앞서 생성한 .ppk 파일 업로드

![image-20210909222118745](EC2_Putty.assets/image-20210909222118745.png)

4. Session > Saved Sessions 이름 지정 후 저장

![image-20210909222311937](EC2_Putty.assets/image-20210909222311937.png)

5. 저장한 세션 선택 후 Open 클릭

![image-20210909222427768](EC2_Putty.assets/image-20210909222427768.png)

6. Accept 선택

![image-20210909222507701](EC2_Putty.assets/image-20210909222507701.png)

7. login 아이디 입력

- AMI에 따라 기본 계정이 다름

  https://docs.aws.amazon.com/ko_kr/AWSEC2/latest/UserGuide/managing-users.html

  - Amazon Linux 2 또는 Amazon Linux AMI의 경우:  `ec2-user`
  - CentOS AMI의 경우: `centos`
  - Debian AMI의 경우:`admin`
  - Fedora AMI의 경우: `ec2-user` 또는 `fedora`
  - RHEL AMI의 경우: `ec2-user` 또는 `root`
  - SUSE AMI의 경우: `ec2-user` 또는 `root`
  - Ubuntu AMI의 경우: `ubuntu`

![image-20210909222650017](EC2_Putty.assets/image-20210909222650017.png)