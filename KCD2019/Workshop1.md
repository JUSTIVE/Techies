# Workshop 1

발표자

- 최용호
- 넥슨 코리아 판교
- 자동화 솔루션

주의사항: 앞서나가지 말아주세요

## 도커가 좋은 이유

1. 재현성

어플리케이션 서비스 환경 구축
서버+데이터베이스(사내 위키)
매번 해야 하기 때문에 비효율적

이미지(노턴, 도커, AWS AMI 등)
여러 사람들이 이미지를 수정하고 쓰다 보니 트래킹이 안되고
버전 관리가 개판이 됨

그래서 요즘은 이미지의 코드화가 유행

도커는 Dockerfile을 이용하여 코드화
도커의 사용 과정

- Docerfile 작성
- 이미지 만들기
- 완성된 이미지를 이미지 저장소에 저장
- 컨테이너 형태로 구동

> `컨테이너` 란? 컨테이너 안의 짐들을 서로 격리하여 side effect를 없앰 이때 리눅스 커널의 network, storage 기술을 이용하여 격리, 가상화함

2. 가볍다

일반적인 Virtual OS의 경우에는 Hypervisor가 들어가고 그 위에 GuestOS가 구동되므로 무겁다. 그 위에 애플리케이션이 구동됨

도커의 경우에는 내 OS위에 Docket 위에 애플리케이션을 올림
그러나 내 Docker Kernel을 수정하면 앱들에 영향을 미친다

도커와 호스트의 성능 차이가 별로 없다

3. 이식성

도커는 리눅스 배포판이 아닌 리눅스 커널의 기능들을 이용하기 때문에 어느 배포판에서든 쓸 수 있다.

파일시스템은 좀 주의해야한다.
AUFS: 파일시스템, 18.06 버전 이후부터는 overlay2 스토리지 드라이버를 이용하여 모든 리눅스 배포판에서 동일한 성능 보장
그러나 overlay2를 지원하는 도커버전이 아닌 경우 우분투가 성능이 가장 좋다

비용을 아낄 수 있다.

- 물리 서버 이용하는 경우
동일한 구성의 서버를 작업해야 한다.

- 도커를 사용하는 경우 컨테이너 단위의 배포만 하면 된다.
컨테이너를 사용하는 경우 서버당 남는 자원이 발생하지 않으므로 효율적인 자원 관리를 할 수 있다.

생산성
- 협업이 쉽다.
-CaaS(Container as a Service)

>실습

[실-습 링크](https://www.notion.so/justblur/Docker-2-nignx-8158eb6b1f384c688fa6ac874de0f577)

도커 파일들이 너무 많아질 때 관리하고 네트워크를 관리하는 개념이 Docker Compose다
그리고 서비스 간에 통신을 할 수 있게 dns를 지원한다.
이는 docker inspect의 기능을 통해 네트워크 섹션의 이름을 이용하여 명시적인 이름을 이용한 통신(컨테이너의 ip, dns 등)
우분투는 ubuntu_default를 이용, 격리된 네트워크로 작동

- 볼륨은 어떻게 될까?

마찬가지로 inspect를 통해 볼 수 있다.

## 쿠버네티스

도커 오케스트레이션 도구

쿠버네티스/ 도커 스웜/

근데 왜 쿠버네티스?

- 메이져 회사들이 쿠버네티스를 이용 중

쿠버네티스의 기능

- 인텔리젼트 스케줄링
 - 노드의 리소스 상태에 따라 컨테이너 배치
- 장애가 발생한 노드 복구
- 컨테이너 확장
- 로컬 또는 외부 스토리지와의 연결
- 흩어져있는 컨테이너중 요청한 서비스에 해당하는 컨테이너를 찾아 전달
- 정책에 따라 이미지를 배포하거나 롤백
- 보안이 필요힌 데이터와 설정 파일을 안전하게 저장
- 흩어져있는 컨테이너들에 명령 전달(batch)

명령/ 서비스가 들어온 경우 master node가 받고 master 는 worker node들에 명령과 트래픽 분배를 수행함
