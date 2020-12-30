# Javascript

* **연구주제** : Javascript<br>
* **연구목적** : 웹 프로그래밍을 위한 자바스크립트 공부<br>
* **연구일시** : 2020년 01월 08일 09:00~17:00<br>
* **연구자** : 김소원 <br>
* **연구장비** : window 10, vscode, javascript<br>
* **관련연구** : javascript<br><br>


## 서론
2월부터 시작될 졸업작품을 위해 자바스크립트 공부를 시작한다.<br>

## 본론
자바 스트립트 10일 끝내기로 목표를 잡고 하루에 두단원 진도를 나간다.<br>
책은 웹 프로그래밍을 위한 자바스크립트 기본편을 이용한다.<br>
실습은 이지스퍼블리싱 홈페이지에서 실습파일을 다운로드받아 사용한다.<br>


1. 글자색 바꾸기
```javascript
<!DOCTYPE html>
<html lang="ko">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<meta http-equiv="X-UA-Compatible" content="ie=edge">
	<title>글자색 바꾸기</title>
	<link rel="stylesheet" href="css/change-color.css">	
</head>
<body>
	<h1 id="heading">자바스크립트</h1>
	<p id="text">위 텍스트를 클릭해 보세요</p>

	<script src="js/change-result.js"></script>
</body>
</html>
```
<br>저장 후 Open with the Live Server하면 크롬에서 확인 가능하다.<br>

![사진1](https://user-images.githubusercontent.com/59681873/72406281-0b789100-379f-11ea-8b6f-e86bf7fc7199.JPG)<br>
![사진2](https://user-images.githubusercontent.com/59681873/72406285-0ca9be00-379f-11ea-8210-87868795e574.JPG)<br><br>


2. 현재 시간
```javascript
<!DOCTYPE html>
<html lang="ko">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<meta http-equiv="X-UA-Compatible" content="ie=edge">
	<title>What time is it?</title>
	<style>
		body {
			font-size:2em;
			text-align: center;
		}
	</style>
</head>
<body>
	<script>
		var now = new Date();
		var display = now.toLocaleTimeString();
		document.write("현재 시각은 " + display);	
	</script>
</body>
</html>
```
![사진3](https://user-images.githubusercontent.com/59681873/72406375-57c3d100-379f-11ea-984d-0761f0effa18.JPG)
<br><br>


3. 사용자 입력, 환영합니다.
```javascript
<!DOCTYPE html>
<html lang="ko">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<meta http-equiv="X-UA-Compatible" content="ie=edge">
	<title>Welcome</title>
	<style>
		body {
			font-size:1.3em;
			text-align: center;
		}
	</style>
</head>
<body>
	<h1>어서오세요</h1>
	<script>
		var name = prompt("이름을 입력하세요.");
		document.write("<b><big>" + name + "</big></b>님, 환영합니다.");
	</script>
</body>
</html>
```
<br>

![사진4](https://user-images.githubusercontent.com/59681873/72406428-8a6dc980-379f-11ea-89d4-5a0538e66eac.JPG)
![사진5](https://user-images.githubusercontent.com/59681873/72406430-8b066000-379f-11ea-985d-1f5d1f17f39a.JPG)
<br><br>


## 결론
* 태그는 HTML문서 어디에 있어도 상관없다.<br>하지만 편의를 위해 script 태그를 작성할때는 body사이에 작성한다.,<br>

* src는 외부 자바스크립트 파일 연결한다.
```javascript
<script src ="js/change.js"></script>
```
<br>

* prompt()는 사용자에게 어떤 값을 입력받을 때 사용하는 함수이다.<br> 사용자가 값을 입력할수 있도록 작은 창을 만들어 준다.<br>


* alert()는 웹 브라우저 화면에서 간단한 알림 내용을 표시하려고 할 때 사용한다.
```javascript
alert("환영합니다.");
```
<br>

* write 앞에 document.이 붙는이유 : write()함수는 document객체에 포함되어 있기 때문이다.
```javascript
var name = prompt("이름: ");
document.write(name + "님, 어서오세요!");
```
->홍길동님, 어서오세요!<br>


* console.log()함수는 괄호 안의 내용을 콘솔 창에 출력한다.<br>


* 자바 스크립트는 대소문자 구별한다.<br>

* 세미콜론으로 문장 구분한다. <br>하지만 세미콜론 안붙여도 실행 가능하다.

## 향후과제
매일 2단원 공부
## 참고자료
* 웹 프로그래밍을 위한 자바스크립트-기본편