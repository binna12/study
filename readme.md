## 결제(부트페이)
* [부트페이](https://cli.vuejs.org/)를 통해 개발되었으니 부트페이 메뉴얼 참고
* [부트페이 메뉴얼](https://docs.bootpay.co.kr/)
* 계정 ID: minismart@cloud-stones.com
* 계정 PW: zmffkdnem1!
* payment.js, PaymentService.php
```php
/*
아마 문서에서 못찾을꺼 같아서 아래사항은 적어둠
아래 코드가 실제 결제를 수행하도록 만드는 코드임
부트페이 php API 가 일반적인 패턴은 status에서 200 으로 리턴하면 정상적으로 작동하는 케이스고 아닐 경우에는 잘못결제한것
*/
$bootpay->submit($receiptId);
```

## 결제(나이스페이)
* [나이스페이 관리자 바로가기](https://npg.nicepay.co.kr/logIn.do)
* 계정 ID: cloud0001
* 계정 PW: 클라우드3!
* && 참조문서 링크 추가
* API 문서 링크 추가

## 결제(이니시스)
* [이니시스 관리자 바로가기](https://iniweb.inicis.com/security/login.do)
* 계정 ID: baedalgeek
* 계정 PW: 클라우드1!
* && 참조문서 링크 추가

## 푸쉬
* [firebase cloud message 매뉴얼](https://firebase.google.com/docs/cloud-messaging/http-server-ref)
* DB table: push
* cron file: PushScheduler.php
* 설명: push table에 데이터를 PushScheduler.php 를 지정 시간(3초) 마다 수행하여 전송하도록 구현
PushScheduler.php

## 안드로이드앱
* key store file: C:\Users\CLOUDSTONE\AndroidStudioProjects\android_extract.jks
* key store password: zauphoezv1
* key alias: key0
* key password: zauphoezv1
* 참고) 키스토어 파일 날라갔을경우 공유문서함에 android_key_store.jks 파일 검색

## 정기휴무
* DB table: storeRegularHoliday
* cron file: RegularHoliday.php
* 상점추가로 인해서 storeRegularHoliday 테이블에 데이터를 추가한 이후에 RegularHoliday.php 를 직접한번 수행해줘야함
* 주행 주기는 매월 1일임

## 홈
* baedalgeek_web
- timelineComponent.js 타임벨트를 결정하는 스크립트
- cardComponent.js 하나의 카드 묶음
```html
<card-component :type="'normalStore'" :orientation="'horizontal'" :s-style="'small'"></card-component>
<card-component :type="'specialStore'" :orientation="'vertical'" :s-style="'big'"></card-component>
```
- type: 어떤 데이터를 가져올지 결정 ex)specialStore, normalStore, popularMenu, recommendMenu
- orientation: 가로로 화면 뚤고 나갈지 화면싸이즈에 맞춰서 세로로 출력할지 결정 ex) horizontal, vertical
- s-style: 카드 한장의 크기 ex) big, medium, small

* baedalgeek_admin
- UpdateRank.php 업데이트 주기는 매주 월요일이며 ProbabilityLibrary.php 에서 표준정규분포의 z-table 값으로 산출해서 상점 및 인기메뉴에 순서를 정한다

## TODO 프린터
- [JSPrintManager 다운로드](https://www.neodynamic.com/downloads/jspm/)
- [JSPrintManager Document](https://www.neodynamic.com/Products/Help/JSPrintManager3.0/articles/getting-started.html)
- 