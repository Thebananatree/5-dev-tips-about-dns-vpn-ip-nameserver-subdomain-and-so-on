## 가비아의 DNS레코드와 DNS호스트 차이

가비아의 DNS호스트 : 내 도메인으로 자체 네임서버를 구축한 경우, DNS 호스트메뉴란에서 네임서버 호스트를 관리할 수 있는 기능이다.

가비아의 DNS레코드 : 서브도메인, MX레코드 등 DNS레코드를 설정하는 곳이다.

참고링크 : https://customer.gabia.com/manual#/domain/286/1021 , https://customer.gabia.com/faq/detail#/2929/2948



#### [자체 네임서버 구축하고 사용시 과정과 이해]
1. 자체 네임서버 구축시에, 서버ip주소와 서버만 있다.
2. 그 다음 도메인을 하나 구매해서, 호스트명 ns, ns1와 같은거로 연결시켜줘야 한다.
(근데, 이게 서브도메인처럼 연결하는게 아니라, 가비아의 DNS호스트 같은 기능을갖은것으로 연결하는듯)

BUT, 가비아에 보면 <u>**내 도메인으로 자체 네임서버를 구축할 때, 해당 네임서버를 정상적으로 이용하려면 시행사에 호스트를 먼저 등록해야 합니다.**</u>  라고 나와있다.
[이때, 두가지 의미로 해석할 수 있는데 이 중에 맞는것은 나중에 자체 네임서버 구축시에 더 공부하기로 하자.]

호스트명이 ns,ns1등인 도메인을 네임서버에 연결해야 하는데, 위의 "시행사에 호스트를 먼저 등록"이라는 말을 어떻게 해석하냐로 나눠진다.
(1)경우. - 시행사란, 해당 네임서버를 사용하려는 도메인의 업체에 해당하여, 자체 구축한 네임서버를 사용하려는 도메인의 등록된 업체에 DNS호스트(네임서버 호스트 연결)를 등록해야한다는거다.
(2)경우. - 여기서에 시행사는, DNS호스트(가비아처럼 자체구축 네임서버에 호스트명이 ns,ns1과 같은 도메인을 연결해주는) 기능을 설정할 수 있는 업체에 등록하라는거다.(도메인업체 여부상관x)
    [즉, 2번의 경우에는, 자체구축한 네임서버를 사용하려는 도메인의 등록된 업체와 관련없이, 자체 네임서버를 ns1,ns와 같은 호스트의 도메인과 연결만 하면 된다는것]

3. 그러면, 이제 네임서버를 사용하려는 도메인에서 해당 호스트명(네임서버)의 도메인을 입력해준다.

* ns1,ns, whois, ftp와 같은 호스트명은 서브도메인(m. , blog. ,등등) 과 같은 개념이 아니라, 다르게 설정을 해줘야 하나보다.

참고링크 : https://customer.gabia.com/faq/detail#/2929/2948