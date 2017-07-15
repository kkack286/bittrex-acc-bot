# bittrex-acc-bot
this application is 'Bittrex Accumulation Checking Bot'.

# 1. 이건 뭐하는 건가요?
이런 아이디어에서 시작했습니다.

> 누군가 코인의 가격을 올리려고 한다면 적은 거래량 와중에도 지속적으로 코인을 매집하려고 할 것이다. 이러한 움직임을 포착하려면 거래 기록을 살펴봐야겠다.

이러한 아이디어에서 착안해서 **거래량이 적은 코인들을** 모니터링 하는 프로그램을 만들어보자고 생각했고, 이 프로그램을 만들었습니다.

다만 여기서 저는 선택을 해야했습니다.

1. 거래소
2. 거래량의 기준

첫번째로 거래소 같은 경우 폴로닉스 말고 **비트렉스**를 타겟으로 했습니다. 그 이유는 폴로닉스보다는 비트렉스가 더 많은 코인을 취급하기도 하고 대체로 거래량이 적고 덜 알려진 신생 코인들을 취급하기 때문이었습니다.
두번째로 거래량이 얼마나 작은 것을 기준으로 할 것인가는 일단 24h 거래량 기준으로 **100BTC 미만**인 코인들을 모니터링 하는 것으로 했습니다. 이 기준이 적당한지는 조금 고민을 해보았지만 최적의 값이라고는 생각하지 않지만 일단 100BTC로 잡았습니다.

# 2. 어떻게 보는건가요?
접속하게되면 다음과 같은 웹 페이지를 확인할 수 있습니다.

![alt text](https://github.com/lleellee0/images/blob/master/screenshot_1.png)

표 형태로 데이터를 제공하고 있습니다. 먼저 다음을 보시면 되겠습니다.

![alt text](https://github.com/lleellee0/images/blob/master/screenshot_3.png)

BTC-2GIVE 의 경우 1.82% (0.01/0.46) 이라고 나와있습니다.
이 정보가 의미하는 것은 다음과 같습니다.

1. 현재로부터 1시간 이내의 거래량 중 1.82%가 Buy로 체결된 것이다. (100%라면 모든 주문이 Buy)
2. 현재로부터 1시간 이내의 거래량 중 Buy의 볼륨은 0.01BTC이다.
3. 현재로부터 1시간 이내의 총 거래량은 0.46BTC이다.

데이터가 무엇을 의미하는지 아시겠나요? 가장 위쪽에 있는 1h, 3h, 6h, 12h, 1d, 3d, 1w 등은 각각 1시간, 3시간, 6시간, 12시간, 1일, 3일, 1주일을 의미합니다.

![alt text](https://github.com/lleellee0/images/blob/master/screenshot_4.png)

위에 있는 시간을 클릭하면 해당 열을 기준으로 데이터가 정렬됩니다.

# 3. 내가 직접 설치하여 사용하기
안타깝게도 이 프로그램은 DB에 데이터를 쌓아서 정보를 만들어내기 때문에 서버역할을 해줄 컴퓨터가 하나 필요합니다. 거래 로그를 수집해야하기 때문에 항상 켜져있는 컴퓨터가 좋습니다. 채굴이나 트레이딩을 주로 하는 분들은 분명 이렇게 사용할만한 컴퓨터가 있을거라고 생각하지만 혹여나 없으신 분들은 호스팅을 사용해서 사는 것을 추천드립니다.(트래픽이 문제가 될 것 같긴 하지만 차차 줄여보겠습니다..)

윈도우에서 설치하는 방법과 우분투에서 설치하는 방법으로 나눠서 작성하겠습니다.

## 3.1 윈도우에서 설치하기
Node.js 설치
Mysql 설치
DB 관련 설정 변경

![alt text](https://github.com/lleellee0/images/blob/master/screenshot_2.png)

## 3.2 우분투에서 설치하기

# 4. 개발하면서 느낀점
