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