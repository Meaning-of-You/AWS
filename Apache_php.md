# Apache와 PHP 연동

> AWS 활용



### PHP 웹 서버 설치

1. php 설치

```shell
sudo add-apt-repository ppa:ondrej/php 
sudo apt-get update 
sudo apt-get install -y php5.6
```

![image-20210913224144660](Apache_php.assets/image-20210913224144660.png)

2. PHP 버전 확인

```shell
php -version
```

![image-20210913224218919](Apache_php.assets/image-20210913224218919.png)

3. index.php 파일 작성

```shell
sudo nano /home/project/index.php
```

![image-20210913224319768](Apache_php.assets/image-20210913224319768.png)

4. index.html 파일 삭제

```shell
cd /home/project
```

![image-20210913224618435](Apache_php.assets/image-20210913224618435.png)

- 파일 삭제
  - index.html 파일이 보호되어 있다고 나타남

```shell
rm index.html
```

![image-20210913224846633](Apache_php.assets/image-20210913224846633.png)

```shell
sudo rm index.html
```

![image-20210913224953541](Apache_php.assets/image-20210913224953541.png)

5. 브라우저 실행

![image-20210913225033951](Apache_php.assets/image-20210913225033951.png)

