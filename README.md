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

### [ spring boot 토이프로젝트 ]
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

### [ spring boot 토이프로젝트 ]

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

<br>

## 06/08
### [ SQL 문제풀기 - HackerRank ]
- Employee 테이블에서 salary가 2000보다 많고, months가 10보다 작은 지원의 이름을 출력해라. 정렬은 employee_id 오름차순으로 하라.

<br>

## 06/09
### [ SQL 문제풀기 - HackerRank ]
- 다음과 같이 결과가 나오도록 출력하시오. 괄호안에는 직업명의 앞 1글자, 이는 이름으로 정렬. There are...이후는 총 직업수 별로 정렬하라.
```
Ashely(P)
Christeen(P)
Jane(A)
Jenny(D)
Julia(A)
Ketty(P)
Maria(A)
Meera(S)
Priya(S)
Samantha(D)
There are a total of 2 doctors.
There are a total of 2 singers.
There are a total of 3 actors.
There are a total of 3 professors.
```

<br>

> 결과

```sql
select name || '('  ||
                            case when occupation = 'Doctor' then 'D' 
                                    when occupation = 'Actor' then 'A' 
                                    when occupation = 'Singer' then 'S' 
                            else  'P' end || ')'
from OCCUPATIONS
order by name;

select concat('There are a total of',concat(' ',concat(count(occupation),concat(' ',concat(lower(occupation),'s.'))))) as total from occupations
group by occupation order by total;
```

- concat을 잘 쓰는 것이 관건이다.

<br>

## 06/10
### [ SQL 문제풀기 - HackerRank ]
- A,B,C 컬럼에 변의 길이가 써있다.
```
세 변의 길이가 같다면 Equilateral
두 변의 길이가 같다면 Isosceles
세 변의 길이가 다르다 Scalene
삼각형이 만들어지지 않는다 Not A Triangle 을 출력하라.
```
```SQL
select case when A+C <= B OR B+C <= A OR B+A <= C then 'Not A Triangle' 
                   when A = C AND B= C AND B = A then 'Equilateral'
                   when A = B OR B = C OR C = A then 'Isosceles'
                   ELSE 'Scalene' END
from TRIANGLES;
```
이런식으로 작성했는데, 처음에는 제대로 작성한것 같은데 틀렸다.
이유를 보아하니 먼저 삼각형이 만들어지고, 그 다음이 정삼각형, 이등변삼각형 순서로 가야 정확한 결과가 나온다는 것을 늦게 깨달았다.


<br>

## 06/11
### [ spring boot 토이프로젝트 ]
- 회원전체 조회 시, 순환참조 문제 발생
- 회원 생성, 삭제구현


### [ SQL 문제풀기 - HackerRank ]
- occupation의 열을 회전시켜서 출력해라. 컬럼은 첫번째부터 Doctor,Professor,Singer,Actor 순이다.

```SQL
WITH numbered_data AS (
    SELECT Name, Occupation,
           ROW_NUMBER() OVER (PARTITION BY Occupation ORDER BY Name) AS rn
    FROM OCCUPATIONS
)
SELECT
    MAX(CASE WHEN Occupation = 'Doctor' THEN Name END) AS Doctor,
    MAX(CASE WHEN Occupation = 'Professor' THEN Name END) AS Professor,
    MAX(CASE WHEN Occupation = 'Singer' THEN Name END) AS Singer,
    MAX(CASE WHEN Occupation = 'Actor' THEN Name END) AS Actor
FROM numbered_data
GROUP BY rn
ORDER BY rn;
```
열과 행을 PIVOT으로 했던 경험이 있는데, 집계함수를 쓰기 애매해서 구글링을 통해 위와 같은 SQL을 짰다.
1. WITH구문으로 임시테이블을 만들었다. 직업별 이름에 대해 ROW_NUMBER을 사용해서 직업별로 번호를 부여했다.
2. SELECT CASE문을 사용해서 각 직업별로 행 번호에 따라 데이터를 회전
3. GROUP BY를 이용해 행 번호별로 그룹화, MAX 함수를 사용하여 각 직업별 이름을 선택

<br>
실행결과

```
Aamina Ashley Christeen Eve
Julia Belvet Jane Jennifer
Priya Britney Jenny Ketty
NULL Maria Kristeen Samantha
NULL Meera NULL NULL
NULL Naomi NULL NULL
NULL Priyanka NULL NULL
```

<br>

## 06/12
### [ spring boot 토이프로젝트 ]
- 순환참조 문제 해결 (fetchType.LAZY를 넣으니 문제가 해결됨.)
- 회원(개별) 조회와 게시판 조회를 구현

### [ SQL 문제풀기 - HackerRank ]
- leaf 가 없으면 inner, 자식이 없으면 leaf, 부모가 없으면 root

```
1 2
3 2
5 6
7 6
2 4
6 4
4 15
8 9
10 9
12 13
14 13
9 11
13 11
11 15
15 NULL
```

```sql
select n,
case when N in(SELECT distinct b1.n FROM BST b1 join BST b2 on b1.n = b2.p where b1.p is not null) then 'Inner'
        when N in(SELECT distinct b1.n FROM BST b1 join BST b2 on b1.n = b2.p where b1.p is null) then 'Root' 
        else 'Leaf' end
from BST
order by n;
```
- case when 구문을 사용했다. 셀프조인을 통해 부모를 가진 노드와 부모가 없는 노드를 구분했고 나머지 경우를 leaf라고 정의했다.


<br>

## 06/13
### [ spring boot 토이프로젝트 ]
- 게시판 개별 조회
    - (회원id로 조회, 글번호로 조회)

### [ SQL 문제풀기 - HackerRank ]
- company_code, founder, total number of lead managers, total number of senior managers, total number of managers, and total number of employees를 출력하고 company_code 를 기준으로 오름차순으로 정렬하라

	![Alt text](<스크린샷 2024-06-14 122951.png>)

```sql
select C.company_code,
            C.founder,
            count(L.lead_manager_code) as "total lead managers",
            count(S.senior_manager_code) as "total senior managers",
            count(M.manager_code) as "total managers",
            count(E.employee_code) as "total employees"
from Company C join Lead_Manager L
on C.company_code = L.company_code
join Senior_Manager S
on L.lead_manager_code = S.lead_manager_code
join Manager M
on S.senior_manager_code= M.senior_manager_code
join Employee E
on M.manager_code = E.manager_code
GROUP BY C.company_code, C.founder
order by C.company_code;
```
결과
```
C1 Angela 836 836 836 836
C10 Earl 44 44 44 44
C100 Aaron 362 362 362 362
C11 Robert 3 3 3 3
C12 Amy 648 648 648 648
C13 Pamela 858 858 858 858
C14 Maria 105 105 105 105
C15 Joe 30 30 30 30
C16 Linda 72 72 72 72
C17 Melissa 288 288 288 288
```
자기전까지 해 봤는데, join이 잘못된건지 count가 같은 값이 나오는 문제가 생겼다. employee_code의 count가 전부 같게 들어간걸까..? 내일 다시 해 봐야겠다.

<br>

## 06/13
### [ SQL 문제풀기 - HackerRank ]

어제 풀어봤던 sql문을 보고 다시 풀어봤다.
join을 내가 잘 못쓰는건가 해서 with문을 오랜만에 써봤다.
```sql
with
A as
(
select C.company_code,
            C.founder,
            count(L.lead_manager_code) as "total lead managers"
from Company C join Lead_Manager L
on C.company_code = L.company_code
GROUP BY C.company_code, C.founder,L.lead_manager_code
),
B as
(
select L.company_code,
            count(S.senior_manager_code) as "total senior managers"
from Lead_Manager L join Senior_Manager S
on L.lead_manager_code = S.lead_manager_code
GROUP BY L.company_code
),
C as
(
    select M.company_code,
                count(M.manager_code) as "total managers"
    from Senior_Manager S join Manager M
    on S.senior_manager_code= M.senior_manager_code
    GROUP BY M.company_code
)
,
D as
(
    select E.company_code,
                count(E.employee_code) as "total employees"
    from Employee E join Manager M
    on E.manager_code= M.manager_code
    GROUP BY E.company_code
)
select A.company_code, A.founder, A."total lead managers", B."total senior managers", C."total managers", D."total employees"
from A join B
on A.company_code = B.company_code
join C on B.company_code = C.company_code
join D on C.company_code = D.company_code
order by company_code;
```
이런식으로 생각보다 길게 쿼리가 나왔다.
그런데 분명 구조는 맞게 들어가고 값도 맞는 값인것 같은데 틀리다고 해서 한참을 고민해 봤다. 그럼에도 찾지 못해서 토론에 들어가보니 count에 distinct를 써야하는것 같았다.

분명 문제에서 "테이블에는 중복된 값이 포함될 수 있습니다." 라고 했는데, 이 말이 "중복된 값이 들어가 있으니 중복을 제거해라" 인 것이라 깨달았다.

그래서 어제 한 쿼리문에 distinct만 추가해 봤는데, 맞는 값이 나왔다...
```sql
select C.company_code,
            C.founder,
            count(distinct L.lead_manager_code) as "total lead managers",
            count(distinct S.senior_manager_code) as "total senior managers",
            count(distinct M.manager_code) as "total managers",
            count(distinct E.employee_code) as "total employees"
from Company C join Lead_Manager L
on C.company_code = L.company_code
join Senior_Manager S
on L.lead_manager_code = S.lead_manager_code
join Manager M
on S.senior_manager_code= M.senior_manager_code
join Employee E
on M.manager_code = E.manager_code
GROUP BY C.company_code, C.founder
order by C.company_code;
```

<br>

>+++

애초에 employee 값에 모든 코드값이 들어가 있어서 이렇게 짧게 쓰는것도 가능한것 같다.
```sql
SELECT c.company_code, c.founder, 
            COUNT( DISTINCT e.lead_manager_code),
            COUNT( DISTINCT e.senior_manager_code),
            COUNT( DISTINCT e.manager_code),
            COUNT( DISTINCT e.employee_code)
FROM Company c
JOIN Employee e ON  c.company_code = e.company_code
GROUP BY c.company_code, c.founder
ORDER BY c.company_code
```

company_code도 문자열에 숫자가 혼합되어있어서 

ORDER BY LENGTH(company_code), company_code으로 하려고 했는데,
알고보니 그냥 정렬만 하면 되는 거였다.
점점 sql 난이도가 올라가면서 한문제 한문제 푸는데 굉장히 오래걸리는것 같다.

### [ spring boot 토이프로젝트 ]
- 유저 이름 업데이트 구현 
















