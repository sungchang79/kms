## Security > Secure Key Manager > 콘솔 사용 가이드

콘솔 사용 가이드에서는 Secure Key Manager를 사용하는 데 필요한 기본적인 내용을 설명합니다.
- **키 저장소 생성**
- **키 생성**
- **인증 정보 등록**
- **사용자 데이터 관리**

### 키 저장소 생성
Secure Key Manager는 키 저장소 단위로 인증 정보와 키를 관리합니다. 키 저장소가 없으면 다음과 같은 화면이 나타납니다.

![console-guide-01](http://static.toastoven.net/prod_kms/2020-03-24/console-guide-01.png)

**키 저장소 추가**를 클릭하면 키 저장소를 생성할 수 있는 창이 나타납니다.

![console-guide-02](http://static.toastoven.net/prod_kms/2020-03-24/console-guide-02.png)

이름과 설명을 입력하고 한 개 이상의 인증 방법을 선택한 후 **추가**를 클릭하면 키 저장소를 생성합니다. 생성한 키 저장소는 다음 그림과 같이 키 저장소 목록에 표시합니다.

![console-guide-03](http://static.toastoven.net/prod_kms/2020-03-24/console-guide-03.png)

키 저장소 목록에서 키 저장소를 클릭하면 다음 그림과 같이 키 저장소를 관리할 수 있는 메뉴가 나타납니다.

![console-guide-04](http://static.toastoven.net/prod_kms/2020-03-24/console-guide-04.png)

### 키 생성
Secure Key Manager는 키를 3가지 유형으로 구분합니다. 기밀 데이터는 문자열 데이터를 저장하고 API를 사용한 조회 기능을 제공합니다. 대칭키는 API를 사용한 데이터 암/복호화 기능을 제공합니다. 비대칭키는 API를 사용한 데이터 서명/검증 기능을 제공합니다. 사용자는 사용 목적에 맞는 키 유형을 선택한 후 키를 생성할 수 있습니다.

**키 관리** 메뉴를 클릭하면 다음 그림과 같이 키를 관리할 수 있는 화면을 표시합니다.

![console-guide-05](http://static.toastoven.net/prod_kms/2020-03-24/console-guide-05.png)

키 관리 화면에서 **키 추가**를 클릭하면 키를 생성할 수 있는 창이 나타납니다. 선택한 키 유형에 따라 원하는 데이터를 입력할 수 있습니다.

![console-guide-06](http://static.toastoven.net/prod_kms/2020-03-24/console-guide-06.png)


![console-guide-07](http://static.toastoven.net/prod_kms/2020-03-24/console-guide-07.png)


![console-guide-08](http://static.toastoven.net/prod_kms/2020-03-24/console-guide-08.png)


기밀 데이터를 선택하면 이름, 설명, 데이터를 입력할 수 있고 대칭키/비대칭키를 선택하면 이름, 설명, 회전 주기를 입력할 수 있습니다. 필수 데이터를 입력한 후 **추가**를 클릭하면 키를 생성합니다. 생성한 키는 다음 그림과 같이 키 관리 화면에 표시합니다.

![console-guide-09](http://static.toastoven.net/prod_kms/2020-03-24/console-guide-09.png)

### 키 가져오기
Secure Key Manager는 대칭키(AES-256)를 가져오는 기능을 지원합니다.

![console-guide-27](http://static.toastoven.net/prod_kms/2021-10-26/console-guide-01.png)

**키 데이터** 영역에 키값을 입력하여 업로드할 수 있으며, 업로드 가능한 키의 형태는 다음과 같습니다.

```
0xXX, 0xXX, ..., 0xXX
```

위와 같은 32개의 Hex String을 쉼표(`,`) 혹은 공백(` `)을 구분자로 구분하여 입력하여 키를 업로드합니다.

### 인증 정보 등록
Secure Key Manager에서 생성한 키는 인증에 성공한 클라이언트만 사용할 수 있습니다. 클라이언트 인증에 사용하는 인증 정보는 **IPv4 주소 관리**, **MAC 주소 관리**, **인증서 관리** 메뉴에서 등록합니다.

#### IPv4 주소 등록
**IPv4 주소 관리**를 클릭하면 다음 그림과 같이 클라이언트 인증에 사용하는 IPv4 주소 관리 화면이 나타납니다.

![console-guide-10](http://static.toastoven.net/prod_kms/2020-03-24/console-guide-10.png)

**IPv4 주소 추가**를 클릭하면 그림과 같이 IPv4 주소를 추가할 수 있는 창이 나타납니다.

![console-guide-11](http://static.toastoven.net/prod_kms/2020-03-24/console-guide-11.png)

클라이언트 IPv4 주소와 설명을 입력한 후 **추가**를 클릭하면 IPv4 주소를 추가합니다. 이때 IPv4 주소에는 클라이언트가 Secure Key Manager에 접속할 때 사용하는 IPv4 주소를 입력해야 합니다. 추가한 IPv4 주소는 다음 그림과 같이 IPv4 주소 관리 화면에 표시합니다.

![console-guide-12](http://static.toastoven.net/prod_kms/2020-03-24/console-guide-12.png)

#### MAC 주소 등록
**MAC 주소 관리**를 클릭하면 클라이언트 인증에 사용하는 MAC 주소 관리 화면이 나타납니다.
![console-guide-13](http://static.toastoven.net/prod_kms/2020-03-24/console-guide-13.png)

**MAC 주소 추가**를 클릭하면 MAC 주소를 추가할 수 있는 창이 나타납니다.

![console-guide-14](http://static.toastoven.net/prod_kms/2020-03-24/console-guide-14.png)

클라이언트 MAC 주소와 설명을 입력한 후 **추가**를 클릭하면 MAC 주소를 추가합니다. 추가한 MAC 주소는 MAC 주소 관리 화면에 나타납니다.

![console-guide-15](http://static.toastoven.net/prod_kms/2020-03-24/console-guide-15.png)

#### 클라이언트 인증서 등록
**인증서 관리**를 클릭하면 클라이언트 인증에 사용하는 인증서 관리 화면이 나타납니다..

![console-guide-16](http://static.toastoven.net/prod_kms/2020-03-24/console-guide-16.png)

**인증서 추가**를 클릭하면 인증서를 생성할 수 있는 창이 나타납니다.

![console-guide-17](http://static.toastoven.net/prod_kms/2020-03-24/console-guide-17.png)

인증서 이름, 비밀번호, 설명을 입력하고 사용 기간을 선택한 후 **추가**를 클릭하면 인증서를 생성합니다. 생성한 인증서는 다음과 같이 인증서 관리 화면에 나타납니다. 인증서 관리 화면에서 **다운로드** 아이콘을 클릭하면 인증서 파일을 다운로드합니다.

![console-guide-18](http://static.toastoven.net/prod_kms/2020-03-24/console-guide-18.png)

### 사용자 데이터 관리
Secure Key Manager는 사용자가 생성한 데이터(키, 인증 정보)의 상세 정보를 제공합니다. 사용자 데이터 목록에서 **상세 정보 아이콘**을 클릭하면 다음 그림과 같이 상세 정보를 표시합니다.

![console-guide-19](http://static.toastoven.net/prod_kms/2020-03-24/console-guide-19.png)

#### 사용자 데이터 삭제

사용자가 생성한 데이터의 초기 상태는 **사용 중**입니다. 불필요한 데이터를 삭제하려면 다음 그림과 같이 **상세 정보** 창에서 **삭제 요청**을 클릭합니다.

![console-guide-20](http://static.toastoven.net/prod_kms/2020-03-24/console-guide-20.png)

삭제를 요청하면 다음 그림과 같이 데이터 상태를 **삭제 예정**으로 변경합니다. **삭제 예정**으로 변경한 데이터는 사용할 수 없으며 7일 후 완전히 삭제합니다.

![console-guide-21](http://static.toastoven.net/prod_kms/2020-03-24/console-guide-21.png)

**삭제 예정** 상태의 데이터는 **즉시 삭제**를 클릭해서 삭제 예정 시간까지 기다리지 않고 바로 삭제하거나 **삭제 취소**를 클릭해서 **사용 중** 상태로 되돌릴 수 있습니다.

![console-guide-22](http://static.toastoven.net/prod_kms/2020-03-24/console-guide-22.png)

#### 대칭키/비대칭키 회전

Secure Key Manager에서는 대칭키/비대칭키를 회전할 수 있습니다. 다음 그림과 같이 대칭키/비대칭키 상세 정보 창에서 자동 회전 주기를 설정할 수 있습니다. 회전 주기를 '0'으로 설정하면 자동 회전을 사용하지 않습니다.

![console-guide-23](http://static.toastoven.net/prod_kms/2020-03-24/console-guide-23.png)

회전 주기에 30 이상의 값을 설정하면 다음 회전일을 표시하며 회전 주기마다 키를 자동으로 회전합니다.

![console-guide-24](http://static.toastoven.net/prod_kms/2020-03-24/console-guide-24.png)

대칭키/비대칭키 상세 정보 창에서 **즉시 회전**을 클릭하면 키를 바로 회전할 수 있습니다.

![console-guide-25](http://static.toastoven.net/prod_kms/2020-03-24/console-guide-25.png)

키를 회전하면 다음 그림과 같이 키 버전 목록에 새로운 버전이 추가됩니다.

![console-guide-26](http://static.toastoven.net/prod_kms/2020-03-24/console-guide-26.png)

예외로 키 가져오기를 통해 생성한 키는 Secure Key Manager를 통해 생성한 대칭키와는 다르게 회전 기능을 제공하지 않습니다. 조회 시 다음과 같이 키 회전 영역이 존재하지 않습니다.

![console-guide-28](http://static.toastoven.net/prod_kms/2021-10-26/console-guide-02.png)
