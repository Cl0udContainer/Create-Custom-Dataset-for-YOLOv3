Pycharm과 labelImg 툴을 이용하여 YOLOv3용 Custom Dataset을 만들어 보자.   
## Pycharm Project 생성   
<img src="https://user-images.githubusercontent.com/81284736/112413185-1d6ea000-8d63-11eb-8509-e4a9ad52242a.jpg" width="300" height="300">   
원하는 폴더에 '영어 이름으로 된'프로젝트를 생성해 준다.   

## labelImg 설치
<pre><code>pip install labelImg</pre></code>
<img src="https://user-images.githubusercontent.com/81284736/112414424-5d368700-8d65-11eb-897e-aad418e53135.jpg" width="300" height="300">   

## labelImg 실행
<pre><code>labelImg</pre></code>
<img src=https://user-images.githubusercontent.com/81284736/112414754-f6659d80-8d65-11eb-99d6-65705a3a3196.jpg width="300" height="300"><img src=https://user-images.githubusercontent.com/81284736/112414866-2876ff80-8d66-11eb-8a8b-9981a707a14c.jpg width="300" height="300">   
Terminal창에 labelImg라고 입력하면 labelImg가 실행된다.   

## Dataset 폴더 지정하기
<img src=https://user-images.githubusercontent.com/81284736/112415410-1d709f00-8d67-11eb-8d12-7662a3c97ef3.jpg width="300" height="300">   
save format을 'YOLO'로 변경한 후, Open Dir을 클릭해 Dataset을 만들 폴더를 지정한다.      


## 각 사진마다 Bounding Box를 지정하기
<img src=https://user-images.githubusercontent.com/81284736/112416012-3037a380-8d68-11eb-8abd-97c39724c2f7.jpg width="300" height="300">   
각 사진에서 YOLO가 탐지하길 원하는 객체에 Bounding Box를 지정한다.   
Create\nRectBox 버튼을 클릭하면 사진처럼 경계선을 표시할 수 있고, 인식하려는 객체에 최대한 가까이(위 경우는 내 얼굴) 경계선을 지정한다.
