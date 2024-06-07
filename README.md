# Today I Learned(TIL) - Jun

## 06/01

### 면접준비



### [ SQL 문제풀기 - HackerRank ]

- STATION 테이블에서 a,e,i,o,u 로 시작하고 끝나는 CITY를 중복없이 출력해라.

<br>

## 06/02

### 면접준비


### [ SQL 문제풀기 - HackerRank ]

- STATION 테이블에서 a,e,i,o,u 로 시작하지 않는 CITY를 중복없이 출력해라.


### [ java 문제풀기 - HackerRank ]

- scanner를 통해 숫자 3개를 받아와라

<br>

## 06/03

### 면접복기


### [ SQL 문제풀기 - HackerRank ]

- STATION 테이블에서 a,e,i,o,u 로 끝나지 않는 CITY를 중복없이 출력해라.

- STATION 테이블에서 a,e,i,o,u 로 시작하거나 끝나지 않는 CITY를 중복없이 출력해라.

- STATION 테이블에서 a,e,i,o,u 로 시작하지 않고 끝나지 않는 CITY를 중복없이 출력해라.

### [ java 문제풀기 - HackerRank ]

- if else 문제
    - scanner로 숫자 n을 받아라
    ```
    n이 홀수일 때,
        Weird 출력
    n이 짝수일 때,
        2<=n<=5 이면 Not Weird
        6<=n<=20 이면 Weird
        20<=n 이면 Not Weird
    ```
<br>

## 06/04

### [ SQL 문제풀기 - HackerRank ]

- Students 테이블에서 marks가 75 이상 받은 학생을 출력해라. 단, 이름의 끝 3글자를 기준으로 오름차순 정렬을 해라. 그 후, id 번호를 기준으로 오름차순 정렬을 해라.

### [ java 문제풀기 - HackerRank ]

- scanner에서 string, double, int를 각각 받아서 출력해라
    - nextInt() 다음에 nextLine() 이 올 경우 개행문자가 버퍼에서 사용되기 때문에 scan.skip("(\r\n|[\n\r\u2028\u2029\u0085])?"); 을 써서 해결하는 것을 기억 해 둬야 한다.


<br>


## 06/05

### [ spring boot 토이프로젝트]
- 목표
- 구현할 내용
- 기술
- 아키텍처
- erd
- 설정 : 지금 intellij에서 jsp를 못잡아서 진행을 못하는중..

### [ SQL 문제풀기 - HackerRank ]

- station 테이블에서 LAT_N 의 중앙값을 구하고 소수점 4자리로 반올림해라
    - round()와 median()를 사용
- Employee 테이블에서 직원 이름을 알파벳 순서로 출력하라

<br>

## 06/06

### [ spring boot 토이프로젝트]

드디어 Intellij가 jsp를 못잡던 문제를 해결했다.
이제 erd를 생성하면 될것같다.

<br>

## 06/07

### [ 정처기 대비 ]

---

### C 언어
```c
int a = 0;
int *p;         // *p 는 포인터변수라고 선언한 것이다.
p=&a;           // 여기 p도 *p이다.
```
*p의 *은 변수선언에서만 쓰인다 그 이후에 p도 *p라고 보면된다.
이제 p와 *p는 다르다고 보면 된다.

---
<br>

```c
int A = 10,B;       // A=10, B 선언
int *C = &B;        // *C에 B 주소 대입


B=A--;              // B에 10을 대입후 A=9가됨
B+=20;              // B=30

printf("%d",*C)     // C는 B의 주소. *C = *(B의주소)
                    // 즉, B의 주소가 가리키는 값 = B의 값 ->30
```

---
<br>

```c
char C[2][20]
```

이렇게 가정할 때,
```
c(주소 100) ->  c[0](주소 100) -> 첫번째자리(주소 100)

                c[1](주소 200) -> 첫번째자리(주소 200)
```
이런식이 된다.
즉, 배열 c는 c[0]의 주소값을 가지고 있고 이를 100이라고 가정했다. c[0]은 첫번째자리의 주소를 가리키고 있다.
하지만, 배열 c의 100주소와 c[0]이 가리키는 주소 100은 다른 것이다.
c[0]이 ABC를 가리키고 있다면 A는 주소 100, B는 주소 101, C는 주소102와 같다.

---

<br>

```c
char a[3][5] = {"ABC","DEF","GHI"};
char *p[] = {a[0], a[1], a[2]};     // p[]면 a[]의 값을 뜻하고
                                    // *p[]면 a[]의 주소값을 뜻한다.
int n = sizeof(p)/sizeof(p[0]);
for(int i=0;i<n;i++>)
    printf("%c",p[i][i]);
```

```
a(주소 100) ->  a[0](주소 100) -> A  B  C
                                (주소100)
                a[1](주소 105) -> D  E  F
                                (주소105)
                a[2](주소 110) -> G  H  I)
                                (주소110)

P -> {100, 105, 110}                               
```          
> **sizeof의 값은 무조건 바이트이다.**

p는 주소값이고, **주소값은 무조건 8byte**
따라서 sizeof(p) = 8*3 = 24, sizeof(p[0]) = 8

<br>

> %s 와 %c 차이

%s는 주소값을 받는다. 그 주소부터 끝에 있는 주소까지 모두 받는다.
예를 들어 printf("%s", p[1]) 이면, p[1]의 주소값이 105이므로, 105인 D부터 107인 F까지 출력해서 DEF가 출력된다.

%c는 문자하나를 받는다.




---

<br>

### 자료구조(스택구조)
```java
class StackInt{
    int size,top;
    int buf[];
    public void push(int x){
        ㄱ;                 // buf[++top]=x
    }
    public int pop(){
        ㄴ;                 // return buf[top--]
    }
}
```

스택구조는 값을 넣을 자리나 옮길자리를 가리키는 것이 중요하다!

A값을 넣을때 먼저 그 자리로 이동시켜야한다. (buf[++top]=A)

뺄때는 출력 후 자리를 이동해야한다.(return buf[top--])