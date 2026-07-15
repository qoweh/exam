# C 문제-정답-해설

- 대상: 요청한 두 디렉터리의 C 문제 86개
- 정답 검산: 입력 없는 코드는 임시 디렉터리에서 실제 컴파일/실행 결과로 재확인
- 입력값이 코드에 없는 문제는 특정 수치 대신 입력값 기준 일반식으로 정리
- `set`처럼 출력 순서가 보장되지 않는 경우는 원소 구성을 기준으로 정리

## 1. 02 C巩力 - 抗力1.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 118/02 C巩力 - 抗力1.c`

### 문제

```c
#include <stdio.h>
main()
{
	int i, j, k;
	scanf("%d %d", &i, &j);
	k = i + j;
	printf("%d\n", k);
}
```

### 정답

두 정수 `i`, `j`를 입력하면 `i + j`가 출력됩니다.

### 해설

핵심 개념: 입력 처리, 출력 형식, 연산자, 포인터. `scanf`가 정수 두 개를 읽고, 합을 `k`에 저장한 뒤 출력합니다.

## 2. 기출 따라잡기_문제10.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 118/기출 따라잡기_문제10.c`

### 문제

```c
#include <stdio.h>
main()
{
	int a = 5, b = 10, c = 15, d = 30, result;
	result = a * 3 + b > d || c - b / a <= d && 1;
	printf("%d\n", result);
}
```

### 정답

```text
1
```

### 해설

핵심 개념: 출력 형식, 연산자. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 3. 기출 따라잡기_문제2.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 118/기출 따라잡기_문제2.c`

### 문제

```c
#include <stdio.h>
main()
{
	int i = 10, j = 10, k = 30;
	i /= j;
	j -= i;
	k %= j;
	printf("%d, %d, %d\n", i, j, k);
}
```

### 정답

```text
1, 9, 3
```

### 해설

핵심 개념: 출력 형식, 연산자. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 4. 기출 따라잡기_문제4.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 118/기출 따라잡기_문제4.c`

### 문제

```c
#include <stdio.h>
main( )
{
	int result, a = 100, b = 200, c = 300;
	result = a < b ? b++ : --c;
	printf("%d, %d, %d\n", result, b, c);
}
```

### 정답

```text
200, 201, 300
```

### 해설

핵심 개념: 출력 형식, 연산자. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 5. 기출 따라잡기_문제5.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 118/기출 따라잡기_문제5.c`

### 문제

```c
#include <stdio.h>
main() {
	int i, j;
	scanf("%o#%x", &i, &j);
	printf("%d %d", i, j);
}
```

### 정답

`<8진수>#<16진수>` 형식으로 입력하면 두 값을 10진수로 출력합니다. 예를 들어 `10#10`을 입력하면 `8 16`이 출력됩니다.

### 해설

핵심 개념: 입력 처리, 출력 형식, 연산자, 포인터. `%o`는 8진수, `%x`는 16진수 입력이고, 출력은 `%d`라서 10진수로 보입니다.

## 6. 기출 따라잡기_문제6.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 118/기출 따라잡기_문제6.c`

### 문제

```c
#include <stdio.h>
main()
{
	int j = 024, k = 24, L = 0x24, hap;
	hap = j + k + L;
	printf("%d, %d, %d, %d\n", j, k, L, hap);
}
```

### 정답

```text
20, 24, 36, 80
```

### 해설

핵심 개념: 출력 형식, 연산자. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 7. 기출 따라잡기_문제7.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 118/기출 따라잡기_문제7.c`

### 문제

```c
#include <stdio.h>
int main( ) {
	int x = 7, y = 4, z;
	z = y % 3 < 3 ? 2 : 1;
	z = z & z >> 1;
	z = x > 5 && z <= 3 ? z * x : z / x;
	printf("%d", z);
	return 0;
}
```

### 정답

```text
0
```

### 해설

핵심 개념: 출력 형식, 연산자, 포인터. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 8. 기출 따라잡기_문제9.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 118/기출 따라잡기_문제9.c`

### 문제

```c
#include <stdio.h>
main() {
	int m = 4620;
	int a = m / 1000;
	int b = m % 1000 / 500;
	int c = m % 500 / 100;
	int d = m % 100 / 10;
	printf("1000원의 개수 : %d\n", a);
	printf("500원의 개수 : %d\n", b);
	printf("100원의 개수 : %d\n", c);
	printf("10원의 개수 : %d\n", d);
}
```

### 정답

```text
1000원의 개수 : 4
500원의 개수 : 1
100원의 개수 : 1
10원의 개수 : 2
```

### 해설

핵심 개념: 출력 형식, 연산자. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 9. 02 C 巩力 - 抗力1.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 119/02 C 巩力 - 抗力1.c`

### 문제

```c
#include <stdio.h>
main() {
	int score[] = { 86, 53, 95, 76, 61 };
	char grade;
	char str[] = "Rank";
	for (int i = 0; i < 5; i++) {
		switch (score[i] / 10) {
		case 10:
		case 9:
			grade = 'A';
			break;
		case 8:
			grade = 'B';
			break;
		case 7:
			grade = 'C';
			break;
		default: grade = 'F';
		}
		if (grade != 'F')
			printf( "%d is %c %s\n", i + 1, grade, str);
	}
}
```

### 정답

```text
1 is B Rank
3 is A Rank
4 is C Rank
```

### 해설

핵심 개념: 출력 형식, 연산자, switch, break, 반복문, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 10. 기출 따라잡기_문제11.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 119/기출 따라잡기_문제11.c`

### 문제

```c
#include <stdio.h>
main() {
	int n[] = { 5, 4, 3, 2, 1 };
	for (int i = 0; i < 5; i++)
		printf("%d", n[(i + 1) % 5]);
}
```

### 정답

```text
43215
```

### 해설

핵심 개념: 출력 형식, 연산자, 반복문, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 11. 기출 따라잡기_문제13.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 119/기출 따라잡기_문제13.c`

### 문제

```c
#include <stdio.h>
int main() {
	int number = 1234;
	int div = 10, result = 0;
	while (number != 0) {
		result = result * div;
		result = result + number % div;
		number = number / div;
	}
	printf("%d", result);
}
```

### 정답

```text
4321
```

### 해설

핵심 개념: 출력 형식, 연산자, 포인터, 반복문. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 12. 기출 따라잡기_문제14.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 119/기출 따라잡기_문제14.c`

### 문제

```c
#include <stdio.h>
int main(void) {
	char str[ ] = "REPUBLICOFKOREA";
	int a = 0;
	while (str[a] != '\0')
		++a;
	putchar(str[a-2]);
	return 0;
}
```

### 정답

```text
E
```

### 해설

핵심 개념: 연산자, 반복문, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 13. 기출 따라잡기_문제3.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 119/기출 따라잡기_문제3.c`

### 문제

```c
#include <stdio.h>
#include <stdlib.h>
main(int argc, char *argv[]) {
	int v1 = 0;
	int v2 = 35;
	int v3 = 29;
	if (v1 > v2 ? v2 : v1)
		v2 = v2 << 2;
	else
		v3 = v3 << 2;
	printf("%d", v2 + v3);
	return 0;
}
```

### 정답

```text
151
```

### 해설

핵심 개념: 출력 형식, 연산자, 포인터, 배열/문자열, 명령행 인자. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 14. 기출 따라잡기_문제5.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 119/기출 따라잡기_문제5.c`

### 문제

```c
#include <stdio.h>
main() {
	int c = 1;
	switch (3) {
		case 1: c += 3;
		case 2: c++;
		case 3: c = 0;
		case 4: c += 3;
		case 5: c -= 10;
		default: c--;
	}
	printf("%d", c);
}
```

### 정답

```text
-8
```

### 해설

핵심 개념: 출력 형식, 연산자, switch. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 15. 기출 따라잡기_문제6.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 119/기출 따라잡기_문제6.c`

### 문제

```c
#include <stdio.h>
main() {
	int input = 101110;
	int di = 1;
	int sum = 0;
	while (1) {
		if (input == 0) break;
			sum = sum + (input % 10) * di;
		di = di * 2;
		input = input / 10;
	}
	printf("%d", sum);
}
```

### 정답

```text
46
```

### 해설

핵심 개념: 출력 형식, 연산자, 포인터, break, 반복문. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 16. 기출 따라잡기_문제7.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 119/기출 따라잡기_문제7.c`

### 문제

```c
#include <stdio.h>
main() {
	int s, el = 0;
	for (int i = 6; i <= 30; i++) {
		s = 0;
		for (int j = 1; j <= i / 2; j++)
			if (i % j == 0)
				s = s + j;
		if (s == i)
			el++;
	}
	printf("%d", el);
}
```

### 정답

```text
2
```

### 해설

핵심 개념: 출력 형식, 연산자, 반복문. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 17. 02 C巩力 - 抗力1.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 120/02 C巩力 - 抗力1.c`

### 문제

```c
#include <stdio.h>
main() {
	int a = 50;
	int *b = &a;
	*b = *b + 20;
	printf("%d, %d\n", a, *b);
	char *s;
	s = "gilbut";
	for (int i = 0; i < 6; i += 2) {
		printf("%c, ", s[i]);
		printf("%c, ", *(s + i));
		printf("%s\n", s + i);
	}
}
```

### 정답

```text
70, 70
g, g, gilbut
l, l, lbut
u, u, ut
```

### 해설

핵심 개념: 출력 형식, 연산자, 포인터, 반복문, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 18. 기출 따라잡기_문제1.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 120/기출 따라잡기_문제1.c`

### 문제

```c
#include <stdio.h>
main() {
	char *p = "KOREA";
	printf("%s\n", p);
	printf("%s\n", p + 3);
	printf("%c\n", *p);
	printf("%c\n", *(p + 3));
	printf("%c\n", *p + 2);
}
```

### 정답

```text
KOREA
EA
K
E
M
```

### 해설

핵심 개념: 출력 형식, 연산자, 포인터. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 19. 기출 따라잡기_문제2.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 120/기출 따라잡기_문제2.c`

### 문제

```c
#include <stdio.h>
int main() {
	int ary[3];
	int s = 0;
	*(ary + 0) = 1;
	ary[1] = *(ary + 0) + 2;
	ary[2] = *ary + 3;
	for (int i = 0; i < 3; i++)
		s = s + ary[i];
	printf("%d", s);
}
```

### 정답

```text
8
```

### 해설

핵심 개념: 출력 형식, 연산자, 반복문, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 20. 기출 따라잡기_문제3.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 120/기출 따라잡기_문제3.c`

### 문제

```c
#include <stdio.h>
int main() {
	int* array[3];
	int a = 12, b = 24, c = 36;
	array[0] = &a;
	array[1] = &b;
	array[2] = &c;
	printf("%d", *array[1] + **array + 1);
}
```

### 정답

```text
37
```

### 해설

핵심 개념: 출력 형식, 연산자, 포인터, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 21. 기출 따라잡기_문제4.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 120/기출 따라잡기_문제4.c`

### 문제

```c
#include <stdio.h>
int main( ) {
	int a[4] = { 0, 2, 4, 8 };
	int b[3];
	int* p;
	int sum = 0;
	for (int i = 1; i < 4; i++) {
		p = a + i;
		b[i - 1] = *p - a[i - 1];
		sum = sum + b[i - 1] + a[i];
	}
	printf("%d", sum);
}
```

### 정답

```text
22
```

### 해설

핵심 개념: 출력 형식, 연산자, 포인터, 반복문, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 22. 기출 따라잡기_문제5.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 120/기출 따라잡기_문제5.c`

### 문제

```c
#include <stdio.h>
main() {
	char* a = "qwer";
	char* b = "qwtety";
	for (int i = 0; a[i] != '\0'; i++)
		for (int j = 0; b[j] != '\0'; j++)
			if (a[i] == b[j])
				printf("%c", a[i]);
}
```

### 정답

```text
qwe
```

### 해설

핵심 개념: 출력 형식, 연산자, 포인터, 반복문, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 23. 02 C 巩力 - 抗力1.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 121/02 C 巩力 - 抗力1.c`

### 문제

```c
#include <stdio.h>
struct jsu {
	char nae[12];
	int os, db, hab, hhab;
};
int main() {
	struct jsu st[3] = { {"데이터1", 95, 88}, {"데이터2", 84, 91}, {"데이터3", 86, 75} };
	struct jsu* p;
	p = &st[0];
	(p + 1)->hab = (p + 1)->os + (p + 2)->db;
	(p + 1)->hhab = (p + 1)->hab + p->os + p->db;
	printf("%d", (p + 1)->hab + (p + 1)->hhab);
}
```

### 정답

```text
501
```

### 해설

핵심 개념: 출력 형식, 연산자, 구조체, 포인터, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 24. 기출 따라잡기_문제1.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 121/기출 따라잡기_문제1.c`

### 문제

```c
#include <stdio.h>
main() {
	struct insa {
		char name[10];
		int age;
	} a[] = { "Kim", 28, "Lee", 38, "Park", 42, "Choi", 31 };
	struct insa* p;
	p = a;
	p++;
	printf("%s\n", p->name);
	printf("%d\n", p->age);
}
```

### 정답

```text
Lee
38
```

### 해설

핵심 개념: 출력 형식, 연산자, 구조체, 포인터, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 25. 기출 따라잡기_문제2.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 121/기출 따라잡기_문제2.c`

### 문제

```c
#include <stdio.h>
struct A {
	int n;
	int g;
};
main( ) {
	struct A st[2];
	for (int i = 0; i < 2; i++) {
		st[i].n = i;
		st[i].g = i + 1;
	}
	printf("%d", st[0].n + st[1].g);
}
```

### 정답

```text
2
```

### 해설

핵심 개념: 출력 형식, 연산자, 구조체, 반복문, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 26. 기출 따라잡기_문제3.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 121/기출 따라잡기_문제3.c`

### 문제

```c
#include <stdio.h>

struct dat {
	int x;
	int y;
};

int main( ) {
	struct dat a[] = {{1, 2}, {3, 4}, {5, 6}};
	struct dat* ptr = a;
	struct dat** pptr = &ptr;
	(*pptr)[1] = (*pptr)[2];
	printf("%d 그리고 %d", a[1].x, a[1].y);
	return 0;
}
```

### 정답

```text
5 그리고 6
```

### 해설

핵심 개념: 출력 형식, 연산자, 구조체, 포인터, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 27. 02 C巩力 - 抗力1.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 122/02 C巩力 - 抗力1.c`

### 문제

```c
#include <stdio.h>
int factorial(int n);
main() {
	int (*pf)(int);
	pf = factorial;
	printf("%d", pf(3));
}
int factorial(int n) {
	if (n <= 1)
		return 1;
	else
		return n * factorial(n - 1);
}
```

### 정답

```text
6
```

### 해설

핵심 개념: 출력 형식, 연산자, 재귀, 포인터. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 28. 기출 따라잡기_문제1.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 122/기출 따라잡기_문제1.c`

### 문제

```c
#include <stdio.h>
void align(int a[]) {
	int temp;
	for (int i = 0; i < 4; i++)
		for (int j = 0; j < 4 - i; j++)
			if (a[j] > a[j+1]) {
				temp = a[j];
				a[j] = a[j+1];
				a[j+1] = temp;
			}
}
main() {
	int a[] = { 85, 75, 50, 100, 95 };
	align(a);
	for (int i = 0; i < 5; i++)
		printf("%d ", a[i]);
}
```

### 정답

```text
50 75 85 95 100 
```

### 해설

핵심 개념: 출력 형식, 연산자, 반복문, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다. 마지막 출력에는 공백이 하나 남습니다.

## 29. 기출 따라잡기_문제2.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 122/기출 따라잡기_문제2.c`

### 문제

```c
#include <stdio.h>
#include <string.h>
void inverse(char *str, int len) {
	for(int i = 0, j = len - 1; i < j; i++, j--) {
		char ch = str[i];
		str[i] = str[j];
		str[j] = ch;
	}
}
int main() {
	char str[100] = "ABCDEFGH";
	int len = strlen(str);
	inverse(str, len);
	for(int i = 1; i < len; i += 2) {
		printf("%c", str[i]);
	}
	return 0;
}
```

### 정답

```text
GECA
```

### 해설

핵심 개념: 출력 형식, 연산자, 포인터, 반복문, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 30. 기출 따라잡기_문제3.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 122/기출 따라잡기_문제3.c`

### 문제

```c
#include <stdio.h>
char n[30];
char* getname() {
	printf("이름 입력 : ");
	gets(n);
	return n;
}

main() {
	char* n1 = getname();
	char* n2 = getname();
	char* n3 = getname();
	printf("%s\n", n1);
	printf("%s\n", n2);
	printf("%s\n", n3);
}
```

### 정답

이름을 세 번 입력하면 마지막으로 입력한 이름이 세 줄 모두에 출력됩니다.

### 해설

핵심 개념: 입력 처리, 출력 형식, 연산자, 재귀, 포인터, 배열/문자열. `n1`, `n2`, `n3`가 모두 전역 배열 `n`의 같은 주소를 받으므로, 세 번째 입력이 앞 입력을 덮어씁니다.

## 31. 기출 따라잡기_문제4.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 122/기출 따라잡기_문제4.c`

### 문제

```c
#include <stdio.h>
int func(int a) {
	if (a <= 1) return 1;
	return a * func(a - 1);
}

int main() {
	int a;
	scanf("%d", &a);
	printf("%d", func(a));
}
```

### 정답

정수 `a`를 입력하면 `a <= 1`일 때는 `1`, 그 외에는 `a!` 값이 출력됩니다.

### 해설

핵심 개념: 입력 처리, 출력 형식, 연산자, 재귀, 포인터. `func(a)`가 `a * func(a - 1)`로 재귀 호출되다가 `a <= 1`에서 멈춥니다.

## 32. 기출 따라잡기_문제5.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 122/기출 따라잡기_문제5.c`

### 문제

```c
#include <stdio.h>
int func( ) {
	static int x = 0;
	x += 2;
	return x;
}
int main( ) {
	int x = 0;
	int sum= 0;
	for(int i = 0; i < 4; i++) {
		x++;
		sum += func( );
	}
	printf("%d", sum);
	return 0;
}
```

### 정답

```text
20
```

### 해설

핵심 개념: 출력 형식, 연산자, 재귀, 반복문. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 33. 기출 따라잡기_문제6.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 122/기출 따라잡기_문제6.c`

### 문제

```c
#include <stdio.h>
int isPrime(int number) {
	for (int i = 2; i < number; i++)
		if (number % i == 0) return 0;
	return 1;
}
int main() {
	int number = 13195;
	int max_div = 0;
	for (int i = 2; i < number; i++)
		if (isPrime(i) == 1 && number % i == 0) max_div = i;
	printf("%d", max_div);
}
```

### 정답

```text
29
```

### 해설

핵심 개념: 출력 형식, 연산자, 재귀, 반복문. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 34. 기출 따라잡기_문제7.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 122/기출 따라잡기_문제7.c`

### 문제

```c
#include <stdio.h>
main() {
	int res = mp(2, 10);
	printf("%d", res);
}
int mp(int base, int exp) {
	int res = 1;
	for (int i = 0; i < exp; i++)
		res *= base;
	return res;
}
```

### 정답

```text
1024
```

### 해설

핵심 개념: 출력 형식, 연산자, 반복문. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 35. 기출 따라잡기_문제8.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 122/기출 따라잡기_문제8.c`

### 문제

```c
#include <stdio.h>
void func(int** arr, int size) {
	for(int i = 0; i < size; i++) {
		*(*arr + i) = (*(*arr + i) + i) % size;
	}
}
int main( ){
	int arr[] = {3, 1, 4, 1, 5};
	int* p = arr;
	int** pp = &p;
	int num = 6;
	func(pp, 5);
	num = arr[2];
	printf("%d", num);
	return 0;
}
```

### 정답

```text
1
```

### 해설

핵심 개념: 출력 형식, 연산자, 포인터, 반복문, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 36. 문제18.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제18.c`

### 문제

```c
#include <stdio.h>
struct Node {
	int value;
	struct Node* next;
};
void func(struct Node* node){
	while(node != NULL && node -> next != NULL) {
		int t = node -> value;
		node -> value = node -> next -> value;
		node -> next -> value = t;
		node = node -> next -> next;
	}
}
int main( ) {
	struct Node n1 = {1, NULL};
	struct Node n2 = {2, NULL};
	struct Node n3 = {3, NULL};
	n1.next = &n3;
	n3.next = &n2;
	func(&n1);
	struct Node* current = &n1;
	while(current != NULL){
		printf("%d", current -> value);
		current = current -> next;
	}
	return 0;
}
```

### 정답

```text
312
```

### 해설

핵심 개념: 출력 형식, 연산자, 구조체, 포인터, 반복문. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 37. 문제19.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제19.c`

### 문제

```c
#include <stdio.h>
int r1() {
	return 4;
}
int r10() {
	return (30 + r1());
}
int r100() {
	return (200 + r10());
}
int main() {
	printf("%d\n", r100());
	return 0;
}
```

### 정답

```text
234
```

### 해설

핵심 개념: 출력 형식, 연산자, 재귀. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 38. 문제20.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제20.c`

### 문제

```c
#include <stdio.h>
struct Test {
	int i;
	const char *g;
};
int main( ) {
	struct Test test[ ] = {{1, "AB"}, {2, "DC"}, {3, "EB"}};
	struct Test *p = &test[1];
	printf("%s", p->g + (p->i - 1));
	return 0;
}
```

### 정답

```text
C
```

### 해설

핵심 개념: 출력 형식, 연산자, 구조체, 포인터, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 39. 문제21.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제21.c`

### 문제

```c
#include <stdio.h>
#include <stdlib.h>
void set(int** arr, int* data, int rows, int cols) {
	for (int i = 0; i < rows * cols; ++i) {
		arr[((i + 1) / rows) % rows][(i + 1) % cols] = data[i];
	}
}
int main( ) {
	int rows = 3, cols = 3, sum = 0;
	int data[] = {5, 2, 7, 4, 1, 8, 3, 6, 9};
	int** arr;
	arr = (int**) malloc(sizeof(int*) * rows);
	for (int i = 0; i < cols; i++) {
		arr[i] = (int*) malloc(sizeof(int) * cols);
	}
	set(arr, data, rows, cols);
	for (int i = 0; i < rows * cols; i++) {
		sum += arr[i / rows][i % cols] * (i % 2 == 0 ? 1 : -1);
	}
	for(int i = 0; i < rows; i++) {
		free(arr[i]);
	}
	free(arr);
	printf("%d", sum);
}
```

### 정답

```text
13
```

### 해설

핵심 개념: 출력 형식, 연산자, 포인터, 반복문, 배열/문자열, 연결 리스트. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 40. 문제22.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제22.c`

### 문제

```c
#include <stdio.h>

typedef struct student {
	char* name;
	int score[3];
} Student;

int dec(int enc) {
	return enc & 0xA5;
}

int sum(Student* p) {
	return dec(p->score[0]) + dec(p->score[1]) + dec(p->score[2]);
}

int main( ) {
	Student s[2] = { "Kim", {0xA0, 0xA5, 0xDB}, "Lee", {0xA0, 0xED, 0x81} };
	Student* p = s;
	int result = 0;
	for (int i = 0; i < 2; i++) {
		result += sum(&s[i]);
	}
	printf("%d", result);
	return 0;
}
```

### 정답

```text
908
```

### 해설

핵심 개념: 출력 형식, 연산자, 구조체, 재귀, 포인터, 반복문, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 41. 문제23.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제23.c`

### 문제

```c
#include <stdio.h>
#include <stdlib.h>
typedef struct Data {
	int value;
	struct Data *next;
} Data;

Data* insert(Data* head, int value) {
	Data* new_node = (Data*)malloc(sizeof(Data));
	new_node -> value = value;
	new_node -> next = head;
	return new_node;
}
Data* reconnect(Data* head, int value) {
	if (head == NULL || head -> value == value) return head;
	Data *prev = NULL, *curr = head;
	while (curr != NULL && curr -> value != value) {
		prev = curr;
		curr = curr -> next;
	}
	if (curr != NULL && prev != NULL) {
		prev -> next = curr -> next;
		curr -> next = head;
		head = curr;
	}
	return head;
}
int main( ) {
	Data *head = NULL, *curr;
	for (int i = 1; i <= 5; i++)
		head = insert(head, i);
	head = reconnect(head, 3);
	for (curr = head; curr != NULL; curr = curr -> next)
		printf("%d", curr->value);
	return 0;
}
```

### 정답

```text
35421
```

### 해설

핵심 개념: 출력 형식, 연산자, 구조체, 재귀, 포인터, 반복문, 연결 리스트. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 42. 문제25.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제25.c`

### 문제

```c
#include <stdio.h>
#include <stdlib.h>
struct node {
	int p;
	struct node* n;
};
int main( ) {
	struct node a = {1, NULL};
	struct node b = {2, NULL};
	struct node c = {3, NULL};
	a.n = &b; b.n = &c; c.n = NULL;
	c.n = &a; a.n = &b; b.n = NULL;
	struct node* head = &c;
	printf("%d %d %d", head -> p, head -> n -> p, head -> n -> n -> p);
	return 0;
}
```

### 정답

```text
3 1 2
```

### 해설

핵심 개념: 출력 형식, 연산자, 구조체, 포인터. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 43. 문제26.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제26.c`

### 문제

```c
#include <stdio.h>
#define SIZE 3

typedef struct {
	int a[SIZE];
	int front;
	int rear;
} Queue;

void enq(Queue* q, int val) {
	q -> a[q -> rear] = val;
	q -> rear = (q -> rear + 1) % SIZE;
}

int deq(Queue* q) {
	int val = q -> a[q -> front];
	q -> front = (q -> front + 1) % SIZE;
	return val;
}

int main( ) {
	Queue q = {{0}, 0, 0};
	enq(&q, 1);
	enq(&q, 2);
	deq(&q);
	enq(&q, 3);
	printf("%d 그리고 %d", deq(&q), deq(&q));
	return 0;
}
```

### 정답

```text
2 그리고 3
```

### 해설

핵심 개념: 출력 형식, 연산자, 구조체, 재귀, 포인터, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 44. 문제28.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제28.c`

### 문제

```c
#include <stdio.h>
int isPerfectNum(int num) {
	int sum = 0;
	for (int i = 1; i < num; i++) {
		if (num % i == 0)
			sum += i;
	}
	if (num == sum) return 1;
	else return 0;
}

main() {
	int r = 0;
	for (int i = 1; i <= 100; i++)
		if (isPerfectNum(i))
			r += i;
	printf("%d", r);
}
```

### 정답

```text
34
```

### 해설

핵심 개념: 출력 형식, 연산자, 재귀, 반복문. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 45. 문제29.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제29.c`

### 문제

```c
#include <stdio.h>
#include <stdlib.h>

struct node {
	char c;
	struct node* p;
};

struct node* func(char* s) {
	struct node* h = NULL, *n;
	while(*s) {
		n = malloc(sizeof(struct node));
		n -> c = *s++;
		n -> p = h;
		h = n;
	}
	return h;
}

int main( ) {
	struct node* n = func("BEST");
	while(n) {
		putchar(n -> c);
		struct node* t = n;
		n = n -> p;
		free(t);
	}
		return 0;
}
```

### 정답

```text
TSEB
```

### 해설

핵심 개념: 구조체, 재귀, 포인터, 반복문, 연결 리스트. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 46. 문제39.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제39.c`

### 문제

```c
#include <stdio.h>
#define MAX_SIZE 10

int isWhat[MAX_SIZE];
int point = -1;

int isEmpty() {
	if (point == -1) return 1;
	return 0;
}

int isFull() {
	if (point == 10) return 1;
	return 0;
}

void into(int num) {
	if (isFull() == 1) printf("Full");
	else isWhat[++point] = num;
}

int take() {
	if (isEmpty() == 1) printf("Empty");
	else return isWhat[point--];
	return 0;
}

main() {
	into(5); into(2);
	while (!isEmpty()) {
		printf("%d", take());
		into(4); into(1); printf("%d", take());
		into(3); printf("%d", take()); printf("%d", take());
		into(6); printf("%d", take()); printf("%d", take());
	}
}
```

### 정답

```text
213465
```

### 해설

핵심 개념: 출력 형식, 연산자, 재귀, 반복문, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 47. 문제40.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제40.c`

### 문제

```c
#include <stdio.h>
#include <ctype.h>
int main( ) {
	char *p = "It is 8";
	char result[100];
	int i;
	for(i = 0; p[i] != '\0'; i++) {
		if(isupper(p[i]))
			result[i] = (p[i] - 'A'+ 5) % 25 + 'A';
		else if(islower(p[i]))
			result[i] = (p[i] - 'a'+ 10) % 26 + 'a';
		else if(isdigit(p[i]))
			result[i] = (p[i] - '0'+ 3) % 10 + '0';
		else if(!(isupper(p[i]) || islower(p[i]) || isdigit(p[i])))
			result[i] = p[i];
	}
	result[i] = '\0';
	printf("변환된 문자열 : %s\n", result);
	return 0;
}
```

### 정답

```text
변환된 문자열 : Nd sc 1
```

### 해설

핵심 개념: 출력 형식, 연산자, 포인터, 반복문, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 48. 문제41.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제41.c`

### 문제

```c
#include <stdio.h>
void swap(int a, int b) {
	int t = a;
	a = b;
	b = t;
}
int main( ) {
	int a = 11;
	int b = 19;
	swap(a, b);
	switch(a) {
		case 1:
			b += 1;
		case 11:
			b += 2;
		deafult:
			b += 3;
			break;
	}
	printf("%d", a-b);
}
```

### 정답

```text
-13
```

### 해설

핵심 개념: 출력 형식, 연산자, switch, break. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 49. 문제42.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제42.c`

### 문제

```c
#include <stdio.h>
void func(char *d, char *s) {
	while (*s) {
		*d = *s;
		d++;
		s++;
	}
	*d = '\0';
}
int main( ) {
	char* str1 = "first";
	char str2[50] = "teststring";
	int result = 0;
	func(str2, str1);
	for (int i = 0; str2[i] != '\0'; i++) {
		result += i;
	}
	printf("%d\n", result);
	return 0;
}
```

### 정답

```text
10
```

### 해설

핵심 개념: 출력 형식, 연산자, 포인터, 반복문, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 50. 문제50.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제50.c`

### 문제

```c
#include <stdio.h>
main( ) {
	int field[4][4] = { {0,1,0,1}, {0,0,0,1}, {1,1,1,0}, {0,1,1,1} };
	int mines[4][4] = { {0,0,0,0}, {0,0,0,0}, {0,0,0,0}, {0,0,0,0} };
	int w = 4, h = 4;
	for (int y = 0; y < h; y++) {
		for (int x = 0; x < w; x++) {
			if (field[y][x] == 0) continue;
			for (int j = y - 1; j <= y + 1; j++) {
				for (int i = x - 1; i <= x + 1; i++) {
					if (chkover(w, h, j, i) == 1)
						mines[j][i] += 1;
				}
			}
		}
	}
}
int chkover(int w, int h, int j, int i) {
	if (i >= 0 && i < w && j >= 0 && j < h) return 1;
	return 0;
}
```

### 정답

출력 없음

### 해설

핵심 개념: 연산자, continue, 반복문, 배열/문자열. 값 계산이나 배열 갱신은 수행되지만 화면에 값을 내보내는 출력문이 없어 출력 결과가 없습니다.

## 51. 문제8.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제8.c`

### 문제

```c
#include <stdio.h>
int main( ) {
	int arr[3][3] = {1, 2, 3, 4, 5, 6, 7, 8, 9};
	int* parr[2] = {arr[1], arr[2]};
	printf("%d", parr[1][1] + *(parr[1]+2) + **parr);
}
```

### 정답

```text
21
```

### 해설

핵심 개념: 출력 형식, 연산자, 포인터, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 52. 310 데이터 입출력 - C언어 예상체크1.c

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/310 데이터 입출력 - C언어 예상체크1.c`

### 문제

```c
#include <stdio.h>
main() {
	int i, j;
	scanf("%o#%x", &i, &j);
	printf("%d %d", i, j);
}
```

### 정답

`<8진수>#<16진수>` 형식으로 입력하면 두 값을 10진수로 출력합니다. 예를 들어 `10#10`을 입력하면 `8 16`이 출력됩니다.

### 해설

핵심 개념: 입력 처리, 출력 형식, 연산자, 포인터. `%o`는 8진수, `%x`는 16진수 입력이고, 출력은 `%d`라서 10진수로 보입니다.

## 53. 310 데이터 입출력 - C언어.c

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/310 데이터 입출력 - C언어.c`

### 문제

```c
#include <stdio.h>
main( )
{
	int i, j, k;
	scanf("%d %d", &i, &j);
	k = i + j;
	printf("%d\n", k);
}
```

### 정답

두 정수 `i`, `j`를 입력하면 `i + j`가 출력됩니다.

### 해설

핵심 개념: 입력 처리, 출력 형식, 연산자, 포인터. `scanf`가 정수 두 개를 읽고, 합을 `k`에 저장한 뒤 출력합니다.

## 54. 316 연산자 우선순위 기출체크1.c

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/316 연산자 우선순위 기출체크1.c`

### 문제

```c
#include <stdio.h>
int main( ) {
	int x = 7, y = 4, z;
	z = y % 3 < 3 ? 2 : 1;
	z = z & z >> 1;
	z = x > 5 && z <= 3 ? z * x : z / x;
	printf("%d", z);
	return 0;
}
```

### 정답

```text
0
```

### 해설

핵심 개념: 출력 형식, 연산자, 포인터. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 55. 317 제어문 - C언어 기출체크1.c

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/317 제어문 - C언어 기출체크1.c`

### 문제

```c
#include <stdio.h>
main( ) {
	int c = 1;
	switch (3) {
	case 1: c += 3;
	case 2: c++;
	case 3: c = 0;
	case 4: c += 3;
	case 5: c -= 10;
	default: c--;
	}
	printf("%d", c);
}
```

### 정답

```text
-8
```

### 해설

핵심 개념: 출력 형식, 연산자, switch. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 56. 317 제어문 - C언어 기출체크2.c

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/317 제어문 - C언어 기출체크2.c`

### 문제

```c
#include <stdio.h>
int main(void) {
	char str[ ] = "REPUBLICOFKOREA";
	int a = 0;
	while (str[a] != '\0')
		++a;
	putchar(str[a-2]);
	return 0;
}
```

### 정답

```text
E
```

### 해설

핵심 개념: 연산자, 반복문, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 57. 317 제어문 - C언어.c

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/317 제어문 - C언어.c`

### 문제

```c
#include <stdio.h>
main() {
	int score[] = { 86, 53, 95, 76, 61 };
	char grade;
	char str[] = "Rank";
	for (int i = 0; i < 5; i++) {
		switch (score[i] / 10) {
		case 10:
		case 9:
			grade = 'A';
			break;
		case 8:
			grade = 'B';
			break;
		case 7:
			grade = 'C';
			break;
		default: grade = 'F';
		}
		if (grade != 'F')
			printf( "%d is %c %s\n", i + 1, grade, str);
	}
}
```

### 정답

```text
1 is B Rank
3 is A Rank
4 is C Rank
```

### 해설

핵심 개념: 출력 형식, 연산자, switch, break, 반복문, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 58. 319 break와 continue 기출체크2.java

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/319 break와 continue 기출체크2.java`

### 문제

```c
#include <stdio.h>
main() {
	int input = 101110;
	int di = 1;
	int sum = 0;
	while (1) {
		if (input == 0) break;
		sum = sum + (input % 10) * di;
		di = di * 2;
		input = input / 10;
	}
	printf("%d", sum);
}
```

### 정답

```text
46
```

### 해설

핵심 개념: 출력 형식, 연산자, 포인터, break, 반복문. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 59. 320 포인터 - C언어 기출체크1.c

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/320 포인터 - C언어 기출체크1.c`

### 문제

```c
#include <stdio.h>
int main() {
	int ary[3];
	int s = 0;
	*(ary + 0) = 1;
	ary[1] = *(ary + 0) + 2;
	ary[2] = *ary + 3;
	for (int i = 0; i < 3; i++)
		s = s + ary[i];
	printf("%d", s);
}
```

### 정답

```text
8
```

### 해설

핵심 개념: 출력 형식, 연산자, 반복문, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 60. 320 포인터 - C언어 기출체크2.c

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/320 포인터 - C언어 기출체크2.c`

### 문제

```c
#include <stdio.h>
main() {
	char* a = "qwer";
	char* b = "qwtety";
	for (int i = 0; a[i] != '\0'; i++)
		for (int j = 0; b[j] != '\0'; j++)
			if (a[i] == b[j])
				printf("%c", a[i]);
}
```

### 정답

```text
qwe
```

### 해설

핵심 개념: 출력 형식, 연산자, 포인터, 반복문, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 61. 320 포인터 - C언어.c

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/320 포인터 - C언어.c`

### 문제

```c
#include <stdio.h>
main() {
	int a = 50;
	int *b = &a;
	*b = *b + 20;
	printf("%d, %d\n", a, *b);
	char *s;
	s = "gilbut";
	for (int i = 0; i < 6; i += 2) {
		printf("%c, ", s[i]);
		printf("%c, ", *(s + i));
		printf("%s\n", s + i);
	}
}
```

### 정답

```text
70, 70
g, g, gilbut
l, l, lbut
u, u, ut
```

### 해설

핵심 개념: 출력 형식, 연산자, 포인터, 반복문, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 62. 321 구조체 - C언어 기출체크1.c

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/321 구조체 - C언어 기출체크1.c`

### 문제

```c
#include <stdio.h>
main( ) {
	struct insa {
		char name[10];
		int age;
	} a[ ] = { "Kim", 28, "Lee", 38, "Park", 42, "Choi", 31 };
	struct insa* p;
	p = a;
	p++;
	printf("%s\n", p->name);
	printf("%d\n", p->age);
}
```

### 정답

```text
Lee
38
```

### 해설

핵심 개념: 출력 형식, 연산자, 구조체, 포인터, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 63. 321 구조체 - C언어 기출체크2.c

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/321 구조체 - C언어 기출체크2.c`

### 문제

```c
#include <stdio.h>
struct A {
	int n;
	int g;
};
main( ) {
	struct A st[2];
	for (int i = 0; i < 2; i++) {
		st[i].n = i;
		st[i].g = i + 1;
	}
	printf("%d", st[0].n + st[1].g);
}
```

### 정답

```text
2
```

### 해설

핵심 개념: 출력 형식, 연산자, 구조체, 반복문, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 64. 321 구조체 - C언어.c

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/321 구조체 - C언어.c`

### 문제

```c
#include <stdio.h>
struct jsu {
	char nae[12];
	int os, db, hab, hhab;
};
int main() {
	struct jsu st[3] = { {"데이터1", 95, 88}, {"데이터2", 84, 91},
						{"데이터3", 86, 75} };
	struct jsu* p;
	p = &st[0];
	(p + 1)->hab = (p + 1)->os + (p + 2)->db;
	(p + 1)->hhab = (p + 1)->hab + p->os + p->db;
	printf("%d", (p + 1)->hab + (p + 1)->hhab);
}
```

### 정답

```text
501
```

### 해설

핵심 개념: 출력 형식, 연산자, 구조체, 포인터, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 65. 322 사용자 정의 함수 - C언어 기출체크1.c

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/322 사용자 정의 함수 - C언어 기출체크1.c`

### 문제

```c
#include <stdio.h>
void swap(int* a, int idx1, int idx2) {
	int t = a[idx1];
	a[idx1] = a[idx2];
	a[idx2] = t;
}

void Usort(int* a, int len) {
	for (int i = 0; i < len - 1; i++)
		for (int j = 0; j < len - 1 - i; j++)
			if (a[j] > a[j + 1])
				swap(a, j, j + 1);
}

main() {
	int a[] = { 85, 75, 50, 100, 95 };
	int nx = 5;
	Usort(a, nx);
}
```

### 정답

출력 없음

### 해설

핵심 개념: 포인터, 반복문, 배열/문자열. 값 계산이나 배열 갱신은 수행되지만 화면에 값을 내보내는 출력문이 없어 출력 결과가 없습니다.

## 66. 322 사용자 정의 함수 - C언어 기출체크2.c

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/322 사용자 정의 함수 - C언어 기출체크2.c`

### 문제

```c
#include <stdio.h>
int func(int a) {
	if (a <= 1) return 1;
	return a * func(a - 1);
}

int main() {
	int a;
	scanf("%d", &a);
	printf("%d", func(a));
}
```

### 정답

정수 `a`를 입력하면 `a <= 1`일 때는 `1`, 그 외에는 `a!` 값이 출력됩니다.

### 해설

핵심 개념: 입력 처리, 출력 형식, 연산자, 재귀, 포인터. `func(a)`가 `a * func(a - 1)`로 재귀 호출되다가 `a <= 1`에서 멈춥니다.

## 67. 322 사용자 정의 함수 - C언어.c

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/322 사용자 정의 함수 - C언어.c`

### 문제

```c
#include <stdio.h>
int factorial(int n);
main() {
	int (*pf)(int);
	pf = factorial;
	printf("%d", pf(3));
}
int factorial(int n) {
	if (n <= 1)
		return 1;
	else
		return n * factorial(n - 1);
}
```

### 정답

```text
6
```

### 해설

핵심 개념: 출력 형식, 연산자, 재귀, 포인터. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 68. 문제 05.c

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/예상문제은행/문제 05.c`

### 문제

```c
#include <stdio.h>
#include <stdlib.h>
void set(int** arr, int* data, int rows, int cols) { 
    for (int i = 0; i < rows * cols; ++i) { 
        arr[((i + 1) / rows) % rows][(i + 1) % cols] = data[i]; 
    }
    
}
int main( ) { 
    int rows = 3, cols = 3, sum = 0; 
    int data[] = {5, 2, 7, 4, 1, 8, 3, 6, 9}; 
    int** arr; arr = (int**) malloc(sizeof(int*) * rows); 
    for (int i = 0; i < cols; i++) { 
        arr[i] = (int*) malloc(sizeof(int) * cols); // {*, *, *}, {*, *, *}, {*, *, *} 
    } 
    set(arr, data, rows, cols); 
    for (int i = 0; i < rows * cols; i++) { 
        sum += arr[i / rows][i % cols] * (i % 2 == 0 ? 1 : -1); 
    } 
    for(int i = 0; i < rows; i++) { 
        free(arr[i]); 
    } 
    free(arr); 
    printf("%d", sum);
}
```

### 정답

```text
13
```

### 해설

핵심 개념: 출력 형식, 연산자, 포인터, 반복문, 배열/문자열, 연결 리스트. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 69. 문제 06.c

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/예상문제은행/문제 06.c`

### 문제

```c
#include <stdio.h> 
#include <stdlib.h> 
typedef struct Data { 
    int value; struct Data *next;
} Data;

Data* insert(Data* head, int value) { 
    Data* new_node = (Data*)malloc(sizeof(Data)); 
    new_node -> value = value; new_node -> next = head; return new_node;
}

Data* reconnect(Data* head, int value) { 
    if (head == NULL || head -> value == value) return head; 
    Data *prev = NULL, *curr = head; 
    while (curr != NULL && curr -> value != value) { 
        prev = curr; curr = curr -> next; 
    } 
    if (curr != NULL && prev != NULL) { 
        prev -> next = curr -> next; curr -> next = head; head = curr; 
    } 
    return head;
}

int main( ) { 
        Data *head = NULL, *curr; 
        for (int i = 1; i <= 5; i++) 
            head = insert(head, i); 
        head = reconnect(head, 3);
        for (curr = head; curr != NULL; curr = curr -> next) 
            printf("%d", curr->value); 
        return 0; 
}
```

### 정답

```text
35421
```

### 해설

핵심 개념: 출력 형식, 연산자, 구조체, 재귀, 포인터, 반복문, 연결 리스트. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 70. 문제 08.c

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/예상문제은행/문제 08.c`

### 문제

```c
#include <stdio.h>
#include <stdlib.h>

main(int argc, char *argv[]) {
	int v1 = 0;
	int v2 = 35;
	int v3 = 29;
	if (v1 > v2 ? v2 : v1)
		v2 = v2 << 2;
	else
		v3 = v3 << 2;
	printf("%d", v2 + v3);
	return 0;
}
```

### 정답

```text
151
```

### 해설

핵심 개념: 출력 형식, 연산자, 포인터, 배열/문자열, 명령행 인자. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 71. 문제 09.c

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/예상문제은행/문제 09.c`

### 문제

```c
#include <stdio.h>

main() {
	int m = 4620;
	int a = m / 1000;
	int b = m % 1000 / 500;
	int c = m % 500 / 100;
	int d = m % 100 / 10;
	printf("1000원의 개수 : %d\n", a);
	printf("500원의 개수 : %d\n", b);
	printf("100원의 개수 : %d\n", c);
	printf("10원의 개수 : %d\n", d);
}
```

### 정답

```text
1000원의 개수 : 4
500원의 개수 : 1
100원의 개수 : 1
10원의 개수 : 2
```

### 해설

핵심 개념: 출력 형식, 연산자. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 72. 문제 10.c

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/예상문제은행/문제 10.c`

### 문제

```c
#include <stdio.h>
#include <ctype.h>

int main( ) {
	char *p = "It is 8";
	char result[100];
	int i;
	for(i = 0; p[i] != '\0'; i++) {
		if(isupper(p[i]))
			result[i] = (p[i] - 'A'+ 5) % 25 + 'A';
		else if(islower(p[i]))
			result[i] = (p[i] - 'a'+ 10) % 26 + 'a';
		else if(isdigit(p[i]))
			result[i] = (p[i] - '0'+ 3) % 10 + '0';
		else if(!(isupper(p[i]) || islower(p[i]) || isdigit(p[i])))
			result[i] = p[i];
	}
	result[i] = '\0';
	printf("변환된 문자열 : %s\n", result);
	return 0;
}
```

### 정답

```text
변환된 문자열 : Nd sc 1
```

### 해설

핵심 개념: 출력 형식, 연산자, 포인터, 반복문, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 73. 문제 11.c

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/예상문제은행/문제 11.c`
- 계산 참고: 원본 첫 글자 `f#include`의 선행 `f`를 오타로 보고 제거해 계산함

### 문제

```c
f#include <stdio.h>
main() {
	int n[] = { 5, 4, 3, 2, 1 };
	for (int i = 0; i < 5; i++)
		printf("%d", n[(i+1)%5]);
}
```

### 정답

```text
43215
```

### 해설

원본 첫 글자 `f#include`의 선행 `f`를 오타로 보고 제거해 계산함 핵심 개념: 출력 형식, 연산자, 반복문, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 74. 문제 12.c

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/예상문제은행/문제 12.c`

### 문제

```c
#include <stdio.h>
main() {
	int n[] = { 73, 95, 82 };
	int sum = 0;
	for (int i = 0; i < 3; i++)
		sum += n[i]; // 73+95=168, 168+82=250
	switch (sum / 30) {
		case 10:
		case 9: printf("A");
		case 8: printf("B");
		case 7:
		case 6: printf("C");
		default: printf("D");
	}
}
```

### 정답

```text
BCD
```

### 해설

핵심 개념: 출력 형식, 연산자, switch, 반복문, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 75. 문제 13.c

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/예상문제은행/문제 13.c`

### 문제

```c
#include <stdio.h>
main() {
	int E[] = { 64, 25, 12, 22, 11 };
	int n = sizeof(E) / sizeof(E[0]); // 5
	int i = 0;
	do {
		int j = i + 1;
		do {
			if (E[i] > E[j]) {
			int tmp = E[i];
			E[i] = E[j];
			E[j] = tmp;
			}
			j++;
		} while (j < n);
		i++;
	} while (i < n - 1);
	for (int i = 0; i <= 4; i++)
		printf("%d ", E[i]);
}
```

### 정답

```text
11 12 22 25 64 
```

### 해설

핵심 개념: 출력 형식, 연산자, 반복문, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다. 마지막 출력에는 공백이 하나 남습니다.

## 76. 문제 14.c

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/예상문제은행/문제 14.c`

### 문제

```c
#include <stdio.h>
main() {
	int c = 0;
	for (int i = 1; i <= 2023; i++)
		if (i % 4 == 0)
			c++;
	printf("%d", c);
}
```

### 정답

```text
505
```

### 해설

핵심 개념: 출력 형식, 연산자, 반복문. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 77. 문제 15.c

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/예상문제은행/문제 15.c`

### 문제

```c
#include <stdio.h>
main() {
	char* p = "KOREA";
	printf("1. %s\n", p);
	printf("2. %s\n", p + 1);
	printf("3. %c\n", *p);
	printf("4. %c\n", *(p + 3));
	printf("5. %c\n", *p + 4);
}
```

### 정답

```text
1. KOREA
2. OREA
3. K
4. E
5. O
```

### 해설

핵심 개념: 출력 형식, 연산자, 포인터. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 78. 문제 16.c

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/예상문제은행/문제 16.c`

### 문제

```c
#include <stdio.h>
struct Test { 
    int i;
    const char *g;
};

int main( ) { 
    struct Test test[ ] = {{1, "AB"}, {2, "DC"}, {3, "EB"}}; 
    struct Test *p = &test[1]; 
    printf("%s", p->g + (p->i - 1)); 
    return 0;
}
```

### 정답

```text
C
```

### 해설

핵심 개념: 출력 형식, 연산자, 구조체, 포인터, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 79. 문제 17.c

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/예상문제은행/문제 17.c`

### 문제

```c
#include <stdio.h>
#include <string.h>

void inverse(char *str, int len) {
	for(int i = 0, j = len - 1; i < j; i++, j--) {
		char ch = str[i];
		str[i] = str[j];
		str[j] = ch;
	}
}

int main() {
	char str[100] = "ABCDEFGH"; // HGFEDCBA
	int len = strlen(str);
	inverse(str, len);
	for(int i = 1; i < len; i += 2) {
		printf("%c", str[i]);
	}
	return 0;
}
```

### 정답

```text
GECA
```

### 해설

핵심 개념: 출력 형식, 연산자, 포인터, 반복문, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 80. 문제 18.c

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/예상문제은행/문제 18.c`

### 문제

```c
#include <stdio.h>
char n[30];
char* getname() {
	printf("이름 입력 : ");
	gets(n);
	return n;
}

int main() {
	char* n1 = getname();
	char* n2 = getname();
	char* n3 = getname();
	printf("%s\n", n1);
	printf("%s\n", n2);
	printf("%s\n", n3);
	return 0;
}
```

### 정답

이름을 세 번 입력하면 마지막으로 입력한 이름이 세 줄 모두에 출력됩니다.

### 해설

핵심 개념: 입력 처리, 출력 형식, 연산자, 재귀, 포인터, 배열/문자열. `n1`, `n2`, `n3`가 모두 전역 배열 `n`의 같은 주소를 받으므로, 세 번째 입력이 앞 입력을 덮어씁니다.

## 81. 문제 19.c

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/예상문제은행/문제 19.c`

### 문제

```c
#include <stdio.h>
int isPerfectNum(int num) {
	int sum = 0;
	for (int i = 1; i < num; i++) {
		if (num % i == 0)
			sum += i;
	}
	if (num == sum) return 1;
	else return 0;
}

main() {
	int r = 0;
	for (int i = 1; i <= 100; i++)
		if (isPerfectNum(i))
			r += i;
	printf("%d", r);
}
```

### 정답

```text
34
```

### 해설

핵심 개념: 출력 형식, 연산자, 재귀, 반복문. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 82. 문제 28.c

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/예상문제은행/문제 28.c`

### 문제

```c
#include <stdio.h>
int func(int a) {
	if (a <= 1) return 1;
	return a * func(a - 1);
}
int main() {
	int a;
	scanf("%d", &a);
	printf("%d", func(a));
}
```

### 정답

정수 `a`를 입력하면 `a <= 1`일 때는 `1`, 그 외에는 `a!` 값이 출력됩니다.

### 해설

핵심 개념: 입력 처리, 출력 형식, 연산자, 재귀, 포인터. `func(a)`가 `a * func(a - 1)`로 재귀 호출되다가 `a <= 1`에서 멈춥니다.

## 83. 문제 29.c

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/예상문제은행/문제 29.c`

### 문제

```c
#include <stdio.h>
#define MAX_SIZE 10

int isWhat[MAX_SIZE];
int point = -1;

int isEmpty() {
	if (point == -1) return 1;
	return 0;
}

int isFull() {
	if (point == 10) return 1;
	return 0;
}

void into(int num) {
	if (isFull() == 1) printf("Full");
	else isWhat[++point] = num;
}

int take() {
	if (isEmpty() == 1) printf("Empty");
	else return isWhat[point--];
	return 0;
}

main() {
	into(5); into(2);
	while (!isEmpty()) {
		printf("%d", take());
		into(4); into(1); printf("%d", take());
		into(3); printf("%d", take()); printf("%d", take());
		into(6); printf("%d", take()); printf("%d", take());
	}
}
```

### 정답

```text
213465
```

### 해설

핵심 개념: 출력 형식, 연산자, 재귀, 반복문, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 84. 문제 30.c

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/예상문제은행/문제 30.c`

### 문제

```c
#include <stdio.h>
int isPrime(int number) {
	for (int i = 2; i < number; i++)
		if (number % i == 0) return 0;
	return 1;
}

int main() {
	int number = 13195;
	int max_div = 0;
	for (int i = 2; i < number; i++)
		if (isPrime(i) == 1 && number % i == 0) max_div = i;
	printf("%d", max_div);
}
```

### 정답

```text
29
```

### 해설

핵심 개념: 출력 형식, 연산자, 재귀, 반복문. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 85. 문제 32.c

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/예상문제은행/문제 32.c`

### 문제

```c
#include <stdio.h>
main( ) {
	int field[4][4] = { {0,1,0,1}, {0,0,0,1}, {1,1,1,0}, {0,1,1,1} };
	int mines[4][4] = { {0,0,0,0}, {0,0,0,0}, {0,0,0,0}, {0,0,0,0} };
	int w = 4, h = 4;
	for (int y = 0; y < h; y++) {
		for (int x = 0; x < w; x++) {
			if (field[y][x] == 0) continue;
			for (int j = y - 1; j <= y + 1; j++) {
				for (int i = x - 1; i <= x + 1; i++) {
					if (chkover(w, h, j, i) == 1)
						mines[j][i] += 1;
				}
			}
		}
	}
}

int chkover(int w, int h, int j, int i) {
	if (i >= 0 && i < w && j >= 0 && j < h) return 1;
	return 0;
}
```

### 정답

출력 없음

### 해설

핵심 개념: 연산자, continue, 반복문, 배열/문자열. 값 계산이나 배열 갱신은 수행되지만 화면에 값을 내보내는 출력문이 없어 출력 결과가 없습니다.

## 86. 문제 37.c

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/예상문제은행/문제 37.c`

### 문제

```c
#include <stdio.h>
#include <ctype.h>
int main( ) { 
    char *p = "It is 8"; 
    char result[100]; 
    int i; 
    for(i = 0; p[i] != '\0'; i++) { 
        if(isupper(p[i])) 
            result[i] = (p[i] - 'A'+ 5) % 25 + 'A'; 
        else if(islower(p[i])) 
            result[i] = (p[i] - 'a'+ 10) % 26 + 'a'; 
        else if(isdigit(p[i])) 
            result[i] = (p[i] - '0'+ 3) % 10 + '0'; 
        else if(!(isupper(p[i]) || islower(p[i]) || isdigit(p[i]))) 
            result[i] = p[i]; 
    } 
    result[i] = '\0'; 
    printf("변환된 문자열 : %s\n", result);
    return 0;
}
```

### 정답

```text
변환된 문자열 : Nd sc 1
```

### 해설

핵심 개념: 출력 형식, 연산자, 포인터, 반복문, 배열/문자열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.
