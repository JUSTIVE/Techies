# Google IO extended 18 Gwangmyeong
---
## Material Design Session

sbs 뉴스의 Material 디자인 경험
Typograhpy
헤더의 경우 종이접기에서 착안

Material Design 이란?
> 되게 도형적인 느낌

프린트 디자인의 개념으로 깊이가 있고 그림자가 있는 익숙한 디자인의 개념

> 자유도가 높다

### 왜 Material design을 써야하는가?  
디자이너 뿐만 아니라 개발자에게도 매우 유용한 도구  
개발자와 디자이너가 협업을 할 수 있고 다양한 플랫폼과 프레임워크에 지원이 됨  
위의 근거를 통해 시간을 매우 아낄 수 있다.

맨 처음 UX라는건 만들어 볼때 타이포나 색 등의 디지털 환경에서의 경험이 매우 낮설었음  

SMIRROR 개발의 경험  
개발자들과 일일이 소통하는 것이 힘들었음  

TRAVEL DIARY 개발 경험  
디자인을 모르는 친구들과의 개발:  
개발을 공부한 친구들이 만든 툴을 본 소감  

'오 생각보다 괜찮은데?'

<참고>
#### Material Studies

### 올해 Material Design에 추가된 내용
- System Icons
- Color Palette
- Material Components
  - 다양한 플랫폼에 사용할 수 있는 오픈소스 컴포넌트
- 안드로이드 iOS Web Flutter

*코드랩은 다음 기회에*

올해 Material 최대 핵심: *Material Theme Editor*

Material Gallery
- Sketch에서 작업한 내용에 대해 comment를 달 수 있음
- element의 위치를 inspect 할 수 있다.

---

### Google Assistant what's New & Examples  
이번 GIO에서 100개의 update중 16개가 Assistant이다  
>모든 기술들이 모일 수 있는 플랫폼

4 important things
- Assistant의 현재
- Distribution Channel
- 자연스러운 동작
- 연동방식& 동작

#### Assistant의 현재 : 급속도로 성장중
5억대의 Smart Devices(2018.05 기준)  
1Milion Actions  
30 Langs 80 Nations(goal of 2018)  
화면+ 음성 = 더 편리해진 어시스턴트 => 더욱 더 많이 쓰일 서비스  
Multimodal Conversation(Voice only ~ Visual only)  
새로 등장하는 폼팩터:: 스마트 디스플레이(디스플레이+음성스피커)  
|Google Now| Google Myday |
|--|--|
|스크롤하다보면 온갖 잡다한 정보 다 제공 |시간과 공간을 베이스로 필요한 정보만(개인화)|
Google Assistant in Google Maps(not available in Korea)  

#### 더 자연스러운 동작
John Legend 및 6명의 목소리 추가(WaveNet)  
- Continued Conversation = 대화의 흐름 이해
>>"did the Worriers win?"  
"When's their next game?"  

- Multiple Actions
>>"who was the governer of California when Kevin Durant was frafted and what team drafted him?"

잘될지는 모르지만 일단 구글은 된다고 함
- Pretty please  
예의 범절에 맞게 유도

- Google Duplex  
Between analaog and Digital

삼성 페이와 같이 기존의 인프라를 그대로 이용할 수 있기 때문에 범용성이 좋고 상용화에 부담이 없음

#### 3d party 연동을 위한 
Default Routines  
구글 어시스턴트가 필요한 순간은 우리가 자주 이용하는 일상 패턴을 보조
todoist  
Drive meaningful habits& interactions  
- 데일리 업데이트/ 푸쉬 노티 /오늘의 명언 등록 등  
- 액션 링크:SNS등의 URL 링크로 이동
Multi surface conversation
>>Google home : "would you like to see in your phone?"

재화/서비스 구매
- 메뉴/pickup 장소/ 시간 추천기능  

예약

---

### Android Auto의 출시에 따른 개발자의 기회  
7월 12일 android auto 국내 출시  
IO 내용은 좀 배제하고 개발자로서의 조언/주의사항  

Android Auto(2015 출시)  
- Android Auto란?(Mirrorlink/ Mirroring)
- 상세하게
- 활용방한
- NHTSA 주의사항(자동차 사고를 줄이기 위한 주의사항)

#### 미러링
내 디바이스의 화면이 다른 화면에 보여주는 것   

#### 미러링크의 미러링
미러링크를 이용해서 T맵을 네비게이션에 보여줌
두 디바이스에 화면이 보임

#### Android Auto의 미러링
미러링 디바이스에서만 화면이 보임  

>2015년도엔.. 차량 IT 다 중는다 => 이젠 그만큼 기회가 있다.

- 자동차의 높은 품질 수준을 맞출 수 있다.
- 다른 회사의 차로 같은 사용자경험을 옮기기 편함

Google Assistant 사용 가능
- Okay google 뿐만 아니라 핸들의 음성 버튼을 눌러서 사용 가능
  - 차와 android auto간의 커뮤니케이션

핸즈프리  
- 전화 수신 및 문자 전송가능  
- 노래 틀기

#### 좀 더 상세하게
조도 센서,속력, Heading(자동차 벡터) 값... 음성인식 버튼 정보를 가져올 수 있음  
터널 안 DR(Dead Reckoning, 추측항법)==속력/ Heading
- 기존의 터널 진입시의 속도를 이용한 계산 혹은 네트워크 수신률에 따른 추측 항법보다 훨씬 정확한 정보로 DR 가능

#### 활용 방안  
카카오 모빌리티 모두가 고객
- 네비게이션 화면 하나에 카카오 택시와 네비게이션 통합  

내 차 위치공유 기능 개발(기존의 경우 18개월의 개발, 앱 개발시 1시간 이내로 단축 가능)  
목적지 예측 시간 기반의 서비스
- 예약, 픽업, 결제, Smart Home 등

#### NHTSA(닛짜) 주의사항  
>30자 이상을 화면에 보이지 말것  


#### 업데이트 필요?  
이제 네비게이션 업데이트의 광고가 아티팩트가 될 수 있다.

---

Q. Google 어시스턴트 vs 챗봇?  
A. Google Assistant는 챗봇의 기능을 포함하고, OS에 포함되어있기 때문에 다른 프로그램에 접근도 용이하고, 기존의 챗봇이 하지 못하는 기능들을 할 수 있음







