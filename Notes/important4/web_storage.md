# 브라우저 저장소와 차이점

## web storage
* 키/값 쌍으로 데이터를 저장하고 키를 기반으로 데이터를 조회하는 패턴
* 영구저장소(LocalStorage)와 임시저장소(SessionStorage)를 따로 두어 데이터의 지속성을 구분할 수 있어 응용 환경에 맞는 선택이 가능하다.
* 쿠키의 단점을 극복하는 개선점이 도입되었다.
  
[쿠키와 차이점]
* 쿠키는 매번 서버로 전송된다. (storage는 저장된 데이터가 클라이언트에 존재할 뿐 서버에 전송하지 않는다.)
* 단순 문자열을 넘어 객체정보를 저장할 수 있다. (쿠키: 문자열만 가능)
* 용량의 제한이 없다. (쿠키는 용량에 있어 제한이 있다. 최대 쿠키수 20개/ 크기 4KB)
* 영구 데이터 저장이 가능하다.(만료기간 설정이 없다. 쿠키는 만료일자를 지정하게 되어있어 만료일자 도래 시 제거된다.)

### LocalStorage(로컬 스토리지)
* 저장한 데이터를 영구적으로 보관할 수 있다.
* 최대 크기: 5MB
* 사용 예시: 자동 로그인

### SessionStorage(세션 스토리지) 
* 현재 떠있는 탭 내에서만 데이터 유지 가능
* 새로고침 시 저장된 데이터는 사라지지 않지만, 탭을 닫고 브라우저를 새로 열었을 때는 사라짐
* 최대 크기: 5MB
* 사용 예시: 입력 폼 정보, 비로그인 장바구니

### Cookie(쿠키) 
* 모든 웹 요청에는 쿠키 정보가 포함된다 => 서버 부담 증가
* 최대 크기: 4KB
* 사용 예시: 팝업 창

## 서버 인증과 브라우저 저장소
* 서버 부하와 해킹 위험 때문에 Session, Cookie 방식으로 하지 않고 JWT 방식으로 진행한다.
