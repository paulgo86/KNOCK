# KNOCK for JEJU
>  **Knock API SERVER** for **Jeju** shop information.

# Requirements

> ## Register Shop
> 제주도의 업체 정보를 입력. <br>
> 업체 정보에는 업체명, 업체전화, 주소, 업체사진, 영업일, 개점, 폐점 시간, 쉬는날, 메뉴정보, 특이사항 과 같은 **업체정보**, <br>
> 노크설치여부, OS버전/비트, 기존포스프로그램명, 경로와 같은 **포스정보**, <br>
> 사업주명, 연락처, 서류사진, 사업자번호와 같은 **사업주 정보** 로 분류된다.<br>
> 위 정보들을 하나의 데이터베이스에 적재하고 현재 구동중인 소켓통신 서버가 <br>
> 사업자 번호를 통해 해당 업체의 정보를 최신화 해줄 수 있도록 구현한다. <br>

> ## View Shop Info
> 등록된 업체들의 정보를 출력한다. <br>
> 전체 업체의 정보를 간략히 출력하는 API 와 한 업체를 상세히 출력하는 API를 구현한다.<br>
> 전체 업체정보 출력에는 업체명, 노크설치여부, 사업주명 과 같은 대략적인 정보 출력한다. <br>
> 상세 업체정보 출력은 해당 업체의 모든 정보를 출력한다. <br>

# API DESC
## Knock 업체 입력 API

> ## 업체 정보
>|Path<br>(Method)	|Param	|Param Type	|Param Desc	|
>|:-:|:-:|:-:|:-:|
>|'/register'<br>(POST-multi)|shopName|string|업체명|
>|-|fullAddr|string|주소|
>|-|tel|string|전화번호|
>|-|parking|string|주차여부|
>|-|open|string|개점시간|
>|-|close|string|폐점시간|
>|-| break| string | 영업일|
>|-|special| string | 특이사항|
>|-| shopImages| file[] | 업체사진 |
>|-| posChk | string | 노크설치여부 |
>|-| posVersion | string |  OS 버전 |
>|-| posBit | string | OS bit |
>|-| prgName | string | 프로그램 명 |
>|-| prgPath | string | 프로그램 경로 |
>|-| masterName | string | 사업주이름 |
>|-| phone | string | 사업주 연락처 |
>|-| bsNum | string | 사업자 번호 |
>|-| docImages | file[] |  서류사진|
>|-| shopMenu | string | 메뉴정보|
