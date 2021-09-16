# JAVA 설치 및 환경설정

> AWS 활용



### 자바 설치하기

##### openjdk 설치

```shell
$ sudo apt-get install openjdk-8-jdk
```

![image-20210916224658536](java.assets/image-20210916224658536.png)

##### 자바 설치 확인

```shell
$ java -version
```

![image-20210916224804501](java.assets/image-20210916224804501.png)

- java를 찾을 수 없다고 나타남

1. 설치할 수 있는 openjdk 목록 확인

```shell
$ apt search openjdk
```

![image-20210916225055654](java.assets/image-20210916225055654.png)

2. 목록에 없다면 여러 버전 추가

```shell
$ sudo add-apt-repository ppa:openjdk-r/ppa
```

3. 패키지 업데이트

```shell
$ sudo apt-get update
```

![image-20210916225201837](java.assets/image-20210916225201837.png)

3. 설치 재 실행

```shell
$ sudo apt install openjdk-8-jdk
```

![image-20210916225441860](java.assets/image-20210916225441860.png)

4. 자바 버전 확인

```shell
$ java -version
```

![image-20210916225512962](java.assets/image-20210916225512962.png)



### 자바 환경설정 하기

1. 자바 위치 확인

```shell
$ which java
```

![image-20210916225612919](java.assets/image-20210916225612919.png)

```shell
$ readlink -f /usr/bin/java
```

![image-20210916225709271](java.assets/image-20210916225709271.png)

- /bin/java를 제외한 경로 복사
  - /usr/lib/jvm/java-8-openjdk-amd64/jre

2. 환경설정 파일 열기

- export JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64/jre
  export PATH=$JAVA_HOME/bin:$PATH
  export CLASS_PATH=$JAVA_HOME/lib:$CLASS_PATH

```shell
$ sudo nano /etc/profile
```

![image-20210916230106643](java.assets/image-20210916230106643.png)

3. 파일 업데이트

```shell
$ source /etc/profile
```

![image-20210916230303375](java.assets/image-20210916230303375.png)

4. 환경변수 셋팅 확인

```shell
$ echo $JAVA_HOME
```

![image-20210916230652216](java.assets/image-20210916230652216.png)