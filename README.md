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
Create\nRectBox 버튼을 클릭하면 사진처럼 경계선을 표시할 수 있고, 인식하려는 객체(위 경우에는 내 얼굴)에 최대한 가까이 경계선을 지정한다.   

<img src=https://user-images.githubusercontent.com/81284736/112417179-5cecba80-8d6a-11eb-9f88-66b4cd8fdfff.jpg width="300" height="300">   

인식하려는 Class의 첫 번째 객체인 경우, Class이름을 정해 주어야 한다.   
위 경우는 '남자 얼굴'이므로,  'Man'이라 지정하였다.   
 Bounding Box를 저장하기 위해 Save버튼을 누른 후, Next Image버튼을 눌러 다음 사진으로 넘어간다.   
 
 <img src=https://user-images.githubusercontent.com/81284736/112418004-01bbc780-8d6c-11eb-9d28-077753da1e24.jpg width="300" height="300"><img src=https://user-images.githubusercontent.com/81284736/112418294-8e668580-8d6c-11eb-9260-ec81915a0d70.jpg width="300" height="300">   
 
 다음 사진에는 인식하고자 하는 두 개의 객체(남자 얼굴, 스마트폰)이 존재한다.   
 남자 얼굴에 Bounding Box를 설정하면, 이전 사진에서 생성한 Class인 Man을 클릭하여 지정할 수 있다.   
 스마트폰의 경우는, 새로운 Class인 'Smart Phone'을 생성해서 지정해주어야 한다.   
 이런식으로 새로운 Class는 해당 사진에서 직접 생성하여 지정할 수 있다.
 
 <img src=https://user-images.githubusercontent.com/81284736/112418709-5ad82b00-8d6d-11eb-8805-bd30fd22c908.jpg width="300" height="300">   
 
 데이터셋에 있는 모든 사진들에 대해 Bounding Box작업을 마치고 해당폴더에 가보면 이런 식으로 Classes파일과, 사진파일, 사진파일과 이름이 같은 txt파일이 존재하는 것을 확인할 수 있다.   
<img src=https://user-images.githubusercontent.com/81284736/112419813-69274680-8d6f-11eb-8ced-fd5694146497.jpg width="300" height="300"><img src=https://user-images.githubusercontent.com/81284736/112420117-fff40300-8d6f-11eb-89ec-f6ec7cc706d8.jpg width="300" height="300">   

### Classes파일
Classes파일에는 한 행에 'Class가 등록된 순서'대로 Classs이름이 지정되어 있다.   
### txt파일
한 줄에 각 객체마다 (txt파일과 이름이 같은 사진 지정한 객체의 Classes 파일안에서의 순서)&nbsp;&nbsp;&nbsp; (사진에서의 Bounding Box의 4꼭지점의 좌표)로 이루어진 정보가 기록된다.   

## 마치며
운이 좋으면 프로젝트에서 원하는 Data Set을 Google에서 제공하는 Open Image Dataset을 이용할 수도 있고, 혹은 구글링을 통해 얻을 수 있다.   
나 역시 프로젝트를 위해 필요한 이미지들 (남자, 여자얼굴 / 스마트폰) Open Image Dataset에서 구할 수 있었으나, 대부분의 사진이 백인으로 이루어져 있어, 학습시킨 YOLOv3가 동아시아 사람들을 인식할 때 정확도가 매우 낮았기 때문에, 약 20000장의 이미지를 Instagram과 Google에서 크롤링 하여 직접 Dataset을 만들 수 밖에 없었다.   
하루 날잡고 5~6시간?정도 걸린 것 같았다.   
건승을 빈다.
