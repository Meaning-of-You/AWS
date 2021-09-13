# MySQL과 PHP 연동

> AWS 활용



### MySQL 연동

1. MySQL 연동 라이브러리 설치

```shell
sudo apt install php5.6-mysql 
sudo service mysql restart 
sudo apachectl restart
```

![image-20210913225323295](MySQL_php.assets/image-20210913225323295.png)

2. 설치 패키지 확인

```shell
dpkg -l | grep php
```

![image-20210913231047004](MySQL_php.assets/image-20210913231047004.png)

3. index.php 코드 작성

```shell
sudo nano index.php
```

- '데이터베이스 IP (퍼블릭 IPv4 주소)', 
- '사용자 이름', 
- '비밀번호',
-  '데이터베이스 이름',
-  '3306');

![image-20210913230136720](MySQL_php.assets/image-20210913230136720.png)

4. 브라우저 실행

![image-20210913230246324](MySQL_php.assets/image-20210913230246324.png)



### 오류 해결

1. MySQL 접속

```shell
sudo mysql -u root -p
```

![image-20210913231016302](MySQL_php.assets/image-20210913231016302.png)

2. 인증 방식 수정

```shell
alter user root@localhost identified with mysql_native_password by '비밀번호';
```

![image-20210913230913704](MySQL_php.assets/image-20210913230913704.png)

