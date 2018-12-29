# 파이썬 웹 배포 삽질!! 이제 그만

- 이새로찬(rochan87@gmail.com)(마이뮤직테이스트, 코인원)

## `두 도시의 거리를 계산하는 웹서비스`

요청->API/DB->계산->리스폰스

요청(Multi request)->API/DB(IO Bound)->계산(CPU Bound)->리스폰스

>플라스크와 장고를 개발할때 이걸 신경써야할까?
플라스크와 장고는 웹앱 프레임워크다

- 인증
- ORM
- 템플릿엔진
- 기타

일반적인 서비스
웹서버-> 애플리케이션 서버(Flask/Django)

-그러나 파이썬에는 해당이 없음
솔루션: WSGI:Web server Gateway interface(PEP 333)

파이썬 서비스
웹서버->WSGI 서버->애플리케이션서버

WSGI

- C로 작성
- Nginx에서 지원
- 낮은 메모리 사용량

- 디버깅이 어려움
- config가 어려움

gunicorn

- 파이썬으로 작성
- 다양한 작업 타입/쉬움
- 문서화가 좋음

- 디버깅이 편함

## Gunicorn

- Dynamic Configuration
- various worker(recommend:(2*num_core)+1)
  -CPU Bound가 많이 걸리면 워커를 더 늘려도 되고
  -IO Bound가 많이 걸리면 Thread를 더 늘려도 되고
- 기본 Worker 설정은 sync

request|Sync | ASync
---|---|---
IO|2.67|10.95
compute|4.15|3.75

웹앱->WSGI Server(Gunicorn)->Application Server(Flask)

Gunicorn은 Nginx를 강력하게 추천한다.

## Nginx

- web server
  - proxy server
    - managing connection  
  -reverse proxy

### 삽질기

Slow Client의 경우 Nginx의 버퍼 기능을 이용해서 실제 애플리케이션이 블락되는것을 방지 가능
