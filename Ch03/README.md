# Reconnaissance & Information Gathering
## Active Information Gathering
공격자가 직접 대상 시스템이나 네트워크에 대한 정보를 수집하는 과정<br/>
## Passive Information Gathering
공격자가 직접 대상 시스템에 접근하지 않고도 정보를 수집하는 과정<br/>

## 리눅스 명령어 
| 명령어       | 설명                                                     |
| ------------ | -------------------------------------------------------- |
| ping         | 지정된 호스트에 ICMP 패킷을 보내 응답 시간을 측정        |
| nslookup     | 주어진 도메인 이름에 대한 DNS 레코드를 조회하고 해석     |
| whois        | 지정된 도메인에 대한 등록 정보와 관련된 기타 정보를 조회 |
| whatweb      | 웹 애플리케이션에 대한 기본적인 정보를 수집하고 분석     |
| theHarvester | 이메일, 하위 도메인 및 가상 호스트를 검색하는 도구       |

## 웹 주소 정보수집 사이트
```
https://ipinfo.info/html/ip_checker.php
```

## Whatweb을 통한 정보수집
```
whatweb xxx.xxx.xxx.1-xxx.xxx.xxx.xxx --aggression 3 -v --no-errors --log-verbose=results
```
- whatweb: WhatWeb 도구를 실행하는 명령어
- xxx.xxx.xxx.1-xxx.xxx.xxx.xxx: WhatWeb을 실행할 대상 IP 주소 범위
- --aggression 3: WhatWeb의 공격성 수준을 설정하는 옵션. 숫자가 클수록 더 많은 요청을 보내고 더 집중적으로 분석
- -v: WhatWeb의 실행 상세 정보를 표시하는 옵션 -v 옵션을 사용하면 실행 중에 WhatWeb이 수행하는 작업에 대한 자세한 정보가 터미널에 표시된다.
- --no-errors: WhatWeb 실행 중 발생하는 오류 메시지를 표시하지 않도록 하는 옵션
- --log-verbose=results: WhatWeb의 실행 결과를 자세한 로그로 기록하는 옵션. WhatWeb이 실행 결과를 "results"라는 파일에 자세히 기록

## 웹 주소를 통한 이메일 수집 사이트
```
https://hunter.io
```
## theHarvester를 통한 이메일 수집
```
theHarvester -d xxx.com -b all
```
- -d xxx.com: xxx.com 도메인을 대상으로 정보를 수집
- -b all: 지정된 도메인에 대해 수집할 정보의 유형을 지정. all 옵션은 모든 가능한 정보를 수집하도록 설정