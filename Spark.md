# Spark 설치 및  환경설정

> AWS 활용



### Spark 설치하기

##### scala 다운로드

1. scala 설치

```shell
$ sudo apt-get install scala
```

![image-20210918222806411](Spark.assets/image-20210918222806411.png)

```shell
$ scala
```

![image-20210918222838462](Spark.assets/image-20210918222838462.png)

2. 환경변수 설정

```shell
$ sudo nano etc/profile
```

![image-20210918223132849](Spark.assets/image-20210918223132849.png)

##### spark 다운로드

1. 버전을 선택하고 spark-3.1.2-bin-hadoop3.2.tgz 클릭

https://spark.apache.org/downloads.html

![image-20210918223319286](Spark.assets/image-20210918223319286.png)

2. 주소를 복사해서 다운로드

![image-20210918223356038](Spark.assets/image-20210918223356038.png)

```shell
$ wget https://dlcdn.apache.org/spark/spark-3.1.2/spark-3.1.2-bin-hadoop3.2.tgz
```

![image-20210918223617786](Spark.assets/image-20210918223617786.png)

3. 다운받은 파일 압축 풀기

```shell
$ tar xvf spark-3.1.2-bin-hadoop3.2.tgz
```

![image-20210918223833476](Spark.assets/image-20210918223833476.png)

4. spark 위치 이동

```shell
$ sudo mv spark-3.1.2-bin-hadoop3.2/ /usr/spark
```

5. spark 환경변수 설정

```shell
$ sudo nano etc/profile
```

![image-20210918224127826](Spark.assets/image-20210918224127826.png)

6. spark 설치 확인

```shell
$ /usr/spark/bin/spark-shell
```

![image-20210918224244819](Spark.assets/image-20210918224244819.png)

```shell
println("spark is running")
```

![image-20210918224308657](Spark.assets/image-20210918224308657.png)

