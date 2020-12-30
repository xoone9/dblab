# Lightsail

* **연구주제** : lightsail<br>
* **연구목적** : 아마존 aws이용<br>
* **연구일시** : 2020년 01월 02일 09:00~17:00<br>
* **연구자** : 김소원 <br>
* **연구장비** : Window 10, lightsail<br>
* **관련연구** : putty<br><br>

## 서론
아마존에서 지원하는 lightsail로 가상 서버를 사용해본다.
## 본론
### **Lightsail**
![사진1](https://t1.daumcdn.net/cfile/tistory/997FCA345C5F377012)<br>
Lightsail은 Amazon에서 지원하는 간편한 가상 사설 호스팅 서비스이다.<br>
몇번의 클릭 만으로도 SSD기반의 스토리지, DNS 관리, 정적 IP주소를 포함한 가상 서버를 바로 만들 수 있다.<br><br>

**Lightsail 인스턴스 만들기**
1. 아마존 aws에 로그인후 아래의 화면에서 lightsail에 접속한다.<br>
![사진2](https://user-images.githubusercontent.com/59681873/72315367-df450d80-36d5-11ea-8e39-8d86f29ecd1c.png)<br>

2. 인스턴스 생성에서 인스턴스 이미지를 선택해 준다.<br>
![사진3](https://user-images.githubusercontent.com/59681873/72315495-4e226680-36d6-11ea-8527-a2e64ebc0f42.png)<br>

3. 새로운 ssh키를 생성 해주고 인스턴스 플랜을 가장 기본으로 선택한다.<br>
내가 선택한 플랜은 한달 무료, 최대 750시간이다.<br>
![사진4](https://user-images.githubusercontent.com/59681873/72315547-7f029b80-36d6-11ea-854a-b0e7d9ac7669.png)<br>

4. 인스턴스 생성 완료<br><br>


**Lightsail에 Docker 설치**
```html
sudo su
sudo apt update
apt install docker
apt install docker.io
docker -v
docker run -i -t ubuntu:14.04

```
![사진5](https://user-images.githubusercontent.com/59681873/72315936-d7866880-36d7-11ea-9df6-5e8784d36464.png)
<br>
<br>


**도커 컨테이너 설치, 컨테이너 정보 확인, 컨테이너 삭제**
```html
docker create -i -t --name mycentos centos:7
docker inspect mycentos | grep Id
```
![사진6](https://user-images.githubusercontent.com/59681873/72316120-64c9bd00-36d8-11ea-8808-e5265ecc3056.png)

```html
docker ps(실행중인 컨테이너 목록)
docker start mycentos(mycentos컨테이너 실행)
docker ps
docker ps -a(전체 컨테이너 목록)
docker rm test2(test2 컨테이너 삭제)
docker ps -a
```

![사진7](https://user-images.githubusercontent.com/59681873/72316536-d3f3e100-36d9-11ea-96bb-5501484a723d.png)
<br>
<br>


**node.js 설치**
```html
docker pull node
docker run -i -t node
console.log("hello")
console.log("this is test")
```
![사진8](https://user-images.githubusercontent.com/59681873/72316250-e4f02280-36d8-11ea-8f12-51521b3ad24e.png)
<br>
<br>


**apache2 -y버전 설치**
```html
apt-get install apache2 -y
```


## 결론
Lightsail 프로그램사용이 window에 docker을 설치하고 환경을 설정하는거보다 쉽다는것을 알게 되었다.
Lightsiil 가상 환경에서는 명령어로 docker, apache를 바로 다운 받을 수 있어서 편리했다.

## 향후과제
아마존 aws서비스 이용해보기

## 참고자료
* https://git.dbcore.net/tutorials/web-development/tree/master/chapter01/docker