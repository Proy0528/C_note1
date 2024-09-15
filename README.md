# C_practice1_1강 필기 복습
## 1강 : 입출력
------
### 프로그램이 무엇인가?

PROGRAM - 절차

COMPUTER PROGRAM - 컴퓨터의 명령 이행/수행

- ***컴퓨터가 사용할 수 있는 언어는 : (1)*** 가 유일
    
    ***1) 기계어***
    
- ***기계어는 : (2)*** 으로 나타낸다
    
    ***2) 이진법***
    
- ***Compile? : (3)***
    
    ***3) 스크립트/코드를 기계어로 바꿔주는 작업***
    
- ***C언어를 compile 해주는 프로그램 : (4)***
    
    ***4) compiler***
    

Programming Language의 종류 : C 언어, Java, 등등

---

### 이진법을 사용하는 이유?

반도체의 원리

전기를 흐르게 만들거나 : 1

흐르지 않게 만들거나 : 0

- ***반도체 소자 1칸 : (5)***
    
    ***5) bit***
    
- ***CPU : (6)***
    
    ***6) bit들 여러개를 처리시키는 장치***
    
- ***32bit 운영체제 vs 64bit 운영체제 중 뭐가 더 좋을까? : (7)***
    
    ***7) 64bit***
    

---

### 이진법을 계산하려면..

- ***10진법을 쓸때 사용하는 숫자의 개수와 그 숫자들 : (8)***
    
    ***8) 10개 / 0, 1, 2, 3, 4, 5, 6, 7, 8, 9***
    
- ***이진법을 쓸떄 사용하는 숫자의 개수와 그 숫자들 : (9)***
    
    ***9) 2개 / 0, 1***
    

**EX) - 1011 : 2³ x 1 + 2² x 0 + 2¹ x 1 + 2⁰ x 1 = 11**

- ***110 : 10)***
    
    ***10) 6***
    
- ***101 : 11)***
    
    ***11) 5***
    
- ***011 : 12)***
    
    ***12) 3***
    
- ***1010 : 13)***
    
    ***13) 10***
    
- ***1111 : 14)***
    
    ***14) 15***
    
- ***1100 : 15)***
    
    ***15) 12***
    
- ***101011 : 16)***
    
    ***16) 43***
    

***EX) - 99 : 64 x 1 + 32 x 1 + 2 x 1 + 1 x 1***

***= 1100011***

***99 - 64 = 35***

***35 - 32 = 3***

***3 - 2 = 1***

***1 - 1 = 0***

[1강 : 이진법 연산 연습](https://www.notion.so/1-664d3df5842349b099e37ea70929a821?pvs=21)

---

### 16진법의 원리가 사용된 빛의 색?

“**보편적**” 색의 삼원색 : 빨간색 파란색 노란색

- ***색의 삼원색 : (10)***
    - ***10) Cyan Magenta Yellow (11)***
        
        ***11) 청록색 다홍색 노란색***
        

**잉크 색 : C M Y K(Black/Key)**

- ***빛의 삼원색 : (12)***
    
    ***12) Red Green Blue | RGB***
    

컴퓨터 격자 1칸 : 픽셀

각 rgb밝기는 ***8bit***씩 할당이 되어있다.

***(R, G, B)***

- ***EX : ( 128, 128, 128 )***
    
    ***회색***
    
- ***EX : ( 255, 0 , 0 )***
    
    ***빨간색***
    

---

### 16진법 계산

- ***16진법을 쓸때 사용하는 숫자의 개수와 그 숫자들 : (13)***
    
    ***13) 16개 / 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F***
    

1A = 26

16¹ x 1 = 16

16⁰ x A = 10

16 + 10 = 26

- ***FF : (14)***
    
    ***14) 255***
    

---

### **이진법 —> 16진법 변환**

- ***Tip - (15) Bit씩 끊는다.***
    
    ***15) 4bit***
    

**오른쪽부터 채워넣어 모자른 부분은 0으로 채워넣는다.**

16진법을 사용하는 이유?

→ 복잡한 이진법을 간단하게 나타내어 가독성이 좋다!

- ***0001, 1110, 0110, 0111, 1101***
    - ***1, 14, 6, 7, 13***
        
        ***1E67D***
        

---

---

---

### 컴퓨터 단축키

- ***검색창 : (16)***
    
    ***16) Window + S***
    
- ***파일 열기 : (17)***
    
    ***17) Window + E***
    
- ***CMD : (18)***
    
    ***18) Window + R***
    

**CMD 란? : 명령 프롬트 창**

EX) `explorer .` : 파일 열기

---

### Hello World!

```cpp
#include <stdio.h>

int main() {
	printf("hello, world!\n");
}
```

c언어 가이드책의 저자 : 데니스 리치 **<[Dennis Ritchie](https://www.google.com/search?sca_esv=7e63893fda4bafb0&sca_upv=1&cs=0&sxsrf=ACQVn08qJdLw9lSvGFDu5zo5o4FCrPwa8w:1712412758864&q=Dennis+Ritchie&stick=H4sIAAAAAAAAAONgVeLQz9U3MLI0NjYSSn4zbcebaVsU3mxsVXizoOHNvAmnGMHShpblKVAmSOUpRl79dH1Dw2LLlJJkg4oqGD8tx9w0Pr3M8hQjD4hvVGCZnmJqFH-KkQuk07i8xDC3Aqa2LKfKtMKyIuUR4wImboGXP-4JS01jmrTm5DXGfiYuAZ_8_OLUnMqg1JzEktSUkHwhMS4217ySzJJKIR4pLi6Io0rMkoQaGbm4g1NLQvJ981My0yqFioQKsOgWh-vmleLm4gTpTiqJTzYWckbVbSJkxMXpm5qblFpU7J8mpMrF5Zyfk5OaXJKZnyckLiXKJayfDBfQLy_KLAEqVIo1ctt1ado5NgdBBiBY4R7sIKWhJcjF5pKfm5iZJ6h-OIehPPeVvZYwF0dIYkV-Xn5upeBb7x_zl3x6b6_EyQnU43Am-o29FsMEJsamfSsOsfFwMAowGLFxMAgxMTFXMfAsYuVzSc3LyyxWCMosSc7ITJ3AxggA7b9XcboBAAA&sa=X&ved=2ahUKEwiWj83R4q2FAxVIc_UHHSQ-A6EQ7fAIegQIABAO)>**

왜 하필 hello world?

- ***왜 하필 hello world? : (19)***
    
    ***19) 데니스 리치의 가이드책에 있는 첫 예제가 hello world를 프린트하는 내용인데 그것이 전통 삼아 내려져오는게 유력하다.***
    

---

- ***#include <stdio.h>***
    
    ***외부 라이브러리 호출***
    

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/6787e3a8-98d5-4228-abd7-9eed7c52695c/398c8bd9-f1c8-4172-9737-076980096164/Untitled.png)

- ***—> (20)***
    
    ***20) 표준출력공간***
    
- ***반대로 값을 입력하는 (21)도 있다.***
    
    ***21) 표준입력공간***
    

**입력 : Input → I**

**출력 : Output → O**

**‘표준 : Standard → STD**

- ***<stdio.h> (22)***
    
    ***22) 표준 입출력과 관련된 모든 기능들을 가져오겠다.***
    
- ***.h (23)***
    
    ***23) 라이브러리 (header) 파일***
    

(야매로 배우자면 **함수**는 **소괄호가 열리고 닫히는 것**이다.

---

### 컴퓨터 3대 구성요소

- **1. (24)**
    
    ***24) CPU - 계산 담당***
    
- **2. (25)**
    
    ***25) MEMORY - 주기억 장치 : 변수 실행 공간***
    
- **3. (26)**
    
    ***26) (HARD)DISK - 보조기억 장치 : 저장***
    
- ***프로그래머가 되려면 가장 잘 다뤄야하는 것 : (27)***
    
    ***27) MEMORY***
    

**OS : Operating System / 영혼**

EX) Window, Max, Linux, Android, 등

ctrl + alt + delete → 작업관리자

---

성능탭 → 메모리 8GB (8짜리 땅)

**프로그램 실행 → 메모리 점유/차지**

***프로그램을 실행시키면 OS는 메모리 속 프로그램이 들어갈 공간을 만든다***

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/6787e3a8-98d5-4228-abd7-9eed7c52695c/b9134eac-d041-4940-9c2b-10dc67533a25/Untitled.png)

- ***—> 메모리 구조 : (28)***
    
    ***28)
    CODE***
    
    ***DATA***
    
    ***HEAP***
    
    ***STACK***
    

***OS***는 ***메인함수*** 를 **가장 먼저** ***스택*** 에 잡아서 보게 된다

***→ 메인함수를 실행시키면 메모리 어딘가에 메인함수가 잡힌 것***

- ***return 0; (29)***
    
    **29) os**한테 **"제대로 끝 마쳤다"** 를 **알림**
    

***F - function :* 함수/기능**

- ***int main() {
printf("hello, world!\n");
} (30)***
    
    ***hello world 라는 문자열을 표준 출력 공간에 보여주겠다.***
    

---

---

---

### Github, Notion, Velog

**Github : Version, Control, System (면접에 좋음!!)**

version을 제대로 다루는 서비스 였다.

공동작업 유용

**코드 저장 / 관리 : cloud 역할**

**포트폴리오 / 소스코드 올리는 사이트**

**Notion : 혼자 복습/내용 정리**

**Velog : 좋은 깃허브 프로젝트 게시 (면접에 좋음!!)**
