# MySQL과 PHP 연동

> AWS 활용



### MySQL 연동

1. MySQL 연동 라이브러리 설치

```shell
sudo apt install php5.6-mysql 
sudo service mysql restart 
sudo apachectl restart
```

![image-20210913231536584](MySQL_php.assets/image-20210913231536584.png)

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



### 오류 해결 1번 방법 (실패)

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

- 오류 해결 X

3. 인증 방식 재수정

```shell
alter user min@'%' identified with mysql_native_password by '비밀번호';
```

![image-20210913231840371](MySQL_php.assets/image-20210913231840371.png)

4. 인증방식 확인

```shell
SELECT user, host, plugin FROM mysql.user;
```

![image-20210913231911486](MySQL_php.assets/image-20210913231911486.png)

- 오류 해결 X



### 오류 해결 2번 방법 (성공)

1. min 유저로 접속

```shell
sudo mysql -u min -p
```

![image-20210913232835470](MySQL_php.assets/image-20210913232835470.png)

2. 생성되어 있는 데이터베이스 확인

```shell
show databases;
```

![image-20210913232814231](MySQL_php.assets/image-20210913232814231.png)

3. index.php 코드 수정

```shell
sudo nano index.php
```

![image-20210913233221503](MySQL_php.assets/image-20210913233221503.png)

4. 브라우저 확인

![image-20210913233155366](MySQL_php.assets/image-20210913233155366.png)