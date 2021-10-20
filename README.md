# Coding_Rule

GVCS, The AngularJS commit conventions

# Google Java Coding Style

## 1. 소스파일 기본

클래스 이름과 동일하게 대소문자 구별<br>스페이스키만 허용

## 2. 소스파일 구조

```
라이센스

package문

import문

class 선언
```

### 1. package문

- 한문장만 허용한다.

### 2. import문

- '\*'허용하지 않고 한문장만 허용한다.
- 그룹핑해서 순서에 맞춰서 작성한다.
- 다른 그룹간 공백라인을 한 줄 추가한다.

```
import android.app.ActionBar;
import android.app.ActionBar.LayoutParams;
import android.widget.SearchView.OnQueryTextListener;

import com.android.contacts.ContactsUtils;
import com.android.contacts.R;
import com.android.contacts.calllog.CallLogFragment;
```

### 3. class문

- 자바파일에는 하나의 class만 존재한다.
- Class member는 순서의 절대성은 없으니 논리성이 필요하다.
- 새로운 메소드가 추가되었다고 그 메소드가 마지막이면 안 된다.
- 동일한 메소드명(생성자, 오버라이딩 메소드)는 한 곳에 모아야 한다.

## 3. 포멧팅

### - A. 중괄호

    중괄호는 무조건 쓴다.
    또한 여는 중괄호, 닫는 중괄호는 그 줄에 혼자만 존재할 수 있다.

### - B. Line-wrapping

```
하나의 문장이 페이지를 넘어갈 경우
두 문장이상으로 나눠서 표현하는 행위
기본적으로 2번 이상의 들여쓰기를 해야한다. (4개의 스페이스 이상)

    대입연산자(=)이 아닌 곳에서 잘라야 할 경우
       심볼(‘.’, ‘+’, ‘-‘, ‘\*” …) 앞에서 내린다.

    대입연산자(=)의 경우
        대입 연산자 뒤에서 문장을 내린다.

    함수호출의 경우
       ‘(‘는 첫 문장에 두고 나머지를 다음 문장에 내린다.

    콤마(‘,’)의 경우
        앞의 식별자와 동일한 단어로 취급한다.
```

### - C. 공백처리

```
공백라인
    클래스 멤버들을 구별하는 데 사용
    메소드 내부에서 논리적으로 그룹핑 되는 부분
    공백문자
        ‘(‘사이에 공백 문자 else, catch와
        그 이전에 오는 ‘}’ 다음 공백문자 연산자 앞 뒤로는 공백문자 연산자와
        비슷한 심볼에서도 앞 뒤로 공백문자 삽입
```

### - D. 기타

```
switch문
    switch문 내에서 들여쓰기 적용
    아무 처리가 없더라도 default 무조건 존재

들여쓰기는 스페이스 2개
한 문장 = 하나의 statement
한 문장 = 하나의 변수만 선언

변수 선언 = 함수 처음에 하지 않고 최대한 변수가 사용되는 근처에서 선언
변수의 스코프를 최소화

한 라인 문자는 80~100 사용
```

## 4. 네이밍

모든 식별자들은 ASCII와 숫자 값만 사용해야 한다.<br>
식별자에 prefix나 suffixes는 사용하지 않는다.<br>
(ASCLL = 아세키코드, prefix = 접두사, suffixes = 접미사)<br>

### Type 명에 대한 규칙

```
A. package명
    모두 소문자로 기술

B. class명
    UpperCarmelCase 사용

C. Method명
    lowerCarmelCase 사용
    소문자로 시작

D. 상수명
    CONTANT_CASE 방식
    모두 대문자, 단어 사이 밑줄
```

## 5. 프로그래밍 관례

```
@Override는 필수

예외처리
    모든 예외는 무시하지 말고 처리

Static 멤버 접근
    반드시 클래스 명으로 접근
    생성한 객체 내 static 멤버로 접근하지 않음
```

# The AngularJS commit conventions

### 변경 내역을 표시하는데 3가지 내용이 포함한다.

1. 새로운 특징
2. 버그 수정
3. 주요 변경 내용

### 중요하지 않은 커밋

1. 포매팅 변화(공백, 빈줄 (추가, 제거), 들여쓰기
2. 세미콜론 누락
3. 주석

커밋 메세지의 형식

```
<type>(<scope>): <short summary>
<BLANK LINE>

<body>
<BLANK LINE>
<footer>

100자를 넘지 말아야 한다.
```

```
<type>(<scope>): <short summary>
커밋 메세지 헤더
```

Type

- feat : 새로운 기능 추가
- fix : 버그 수정
- docs : 문서 관련
- style : 스타일 변경 (포매팅 수정, 들여쓰기 추가, …)
- refactor : 코드 리팩토링
- test : 테스트 관련 코드
- build : 빌드 관련 파일 수정
- ci : CI 설정 파일 수정
- perf : 성능 개선
- chore : 그 외 자잘한 수정

Scope // 위치(함수이름, 메소드, 클래스이름)

- $location
- $browser
- $compile
- $rootScope \* ngHref

Short summary<br>
명령문, 현재 시제로

```
change(X : changed, changes)
```

첫글자 => 소문자, 마침표 사용하지 않는다.
