# Java 문제-정답-해설

- 대상: 요청한 두 디렉터리의 Java 문제 69개
- 정답 검산: 입력 없는 코드는 임시 디렉터리에서 실제 컴파일/실행 결과로 재확인
- 입력값이 코드에 없는 문제는 특정 수치 대신 입력값 기준 일반식으로 정리
- `set`처럼 출력 순서가 보장되지 않는 경우는 원소 구성을 기준으로 정리

## 1. 03 Java 巩力 - 抗力1.c

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 118/03 Java 巩力 - 抗力1.c`

### 문제

```java
import java.util.Scanner;
public class Test
{
	public static void main(String[] args)
{
		Scanner scan = new Scanner(System.in);
		int a = scan.nextInt();
		System.out.printf("a * 3 = %d\n", a * 3);
		System.out.println("a / 2 = " + (a / 2));
		System.out.print("a - 1 = " + (a - 1));
		scan.close();
	}
}
```

### 정답

정수 `a`를 입력하면 `a * 3`, `a / 2`의 정수 나눗셈 결과, `a - 1`이 차례대로 출력됩니다.

### 해설

핵심 개념: 입력 처리, 출력 형식, 연산자, static. Java의 `int / int`는 소수부를 버리는 정수 나눗셈입니다.

## 2. 기출 따라잡기_문제3.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 118/기출 따라잡기_문제3.java`

### 문제

```java
import java.util.Scanner;
public class Test {
	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);
		int a = scan.nextInt();
		int b = scan.nextInt();
		System.out.printf("%d", a + b);
		scan.close( );
	}
}
```

### 정답

두 정수 `a`, `b`를 입력하면 `a + b`가 출력됩니다.

### 해설

핵심 개념: 입력 처리, 출력 형식, 연산자, static, 배열. `Scanner`로 읽은 두 값을 더해 `printf`로 출력합니다.

## 3. 기출 따라잡기_문제8.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 118/기출 따라잡기_문제8.java`

### 문제

```java
public class Test {
	public static void main(String[] args) {
		int w = 3, x = 4, y = 3, z = 5;
		if((w == 2 | w == y) & !(y > z) & (1 == x ^ y != z)) {
			w = x + y;
			if(7 == x ^ y != w)
				System.out.println(w);
			else
				System.out.println(x);
		}
		else {
			w = y + z;
			if(7 == y ^ z != w)
				System.out.println(w);
			else
				System.out.println(z);
		}
	}
}
```

### 정답

```text
7
```

### 해설

핵심 개념: 출력 형식, 연산자, static. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 4. 03 Java 巩力 - 抗力1.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 119/03 Java 巩力 - 抗力1.java`

### 문제

```java
public class Test {
	public static void main(String[] args) {
		String str = "agile";
		int x[] = { 1, 2, 3, 4, 5 };
		char y[] = new char[5];
		int i = 0;
		while (i < str.length()) {
			y[i] = str.charAt(i);
			i++;
		}
		for (int p : x) {
			i--;
			System.out.print(y[i]);
			System.out.print(p + " ");
		}
	}
}
```

### 정답

```text
e1 l2 i3 g4 a5 
```

### 해설

핵심 개념: 출력 형식, static, 반복문, 배열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다. 마지막 출력에는 공백이 하나 남습니다.

## 5. 기출 따라잡기_문제1.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 119/기출 따라잡기_문제1.java`
- 계산 참고: 실행 결과 계산 시 `i- -`를 의도상 `i--`로 해석함

### 문제

```java
public class Test {
	public static void main(String[] args) {
		int a[] = new int[8];
		int i = 0;
		int n = 10;
		while(n > 0) {
			a[i++] = n % 2;
			n /= 2;
		}
		for(i = 7; i >= 0; i- -)
			System.out.print(a[i]);
	}
}
```

### 정답

```text
00001010
```

### 해설

실행 결과 계산 시 `i- -`를 의도상 `i--`로 해석함 핵심 개념: 출력 형식, 연산자, static, 반복문, 배열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 6. 기출 따라잡기_문제10.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 119/기출 따라잡기_문제10.java`

### 문제

```java
public class Test {
	public static void main(String[] args) {
		int j, i;
		for (j = 0, i = 0; i <= 5; i++) {
			j += i;
			System.out.print(i);
			if (i == 5) {
				System.out.print("=");
				System.out.print(j);
			}
			else
				System.out.print("+");
		}
	}
}
```

### 정답

```text
0+1+2+3+4+5=15
```

### 해설

핵심 개념: 출력 형식, 연산자, static, 반복문. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 7. 기출 따라잡기_문제12.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 119/기출 따라잡기_문제12.java`

### 문제

```java
public class Test {
	public static void main(String[] args) {
		int aa[][] = { {45, 50, 75},{89} };
		System.out.println(aa[0].length);
		System.out.println(aa[1].length);
		System.out.println(aa[0][0]);
		System.out.println(aa[0][1]);
		System.out.println(aa[1][0]);
	}
}
```

### 정답

```text
3
1
45
50
89
```

### 해설

핵심 개념: 출력 형식, static, 배열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 8. 기출 따라잡기_문제2.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 119/기출 따라잡기_문제2.java`

### 문제

```java
public class Test {
	public static void main(String[] args) {
		int ary[][] = new int[3][5];
		int n = 1;
		for(int i = 0; i < 3; i++) {
			for(int j = 0; j < 5; j++) {
				ary[i][j] = j * 3 + i + 1;
				System.out.print(ary[i][j] + " ");
			}
			System.out.println( );
		}
	}
}
```

### 정답

```text
1 4 7 10 13 
2 5 8 11 14 
3 6 9 12 15 
```

### 해설

핵심 개념: 출력 형식, static, 반복문, 배열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 9. 기출 따라잡기_문제4.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 119/기출 따라잡기_문제4.java`

### 문제

```java
public class Test{
	public static void main(String[] args){
		int a = 0, sum = 0;
		while (a < 10) {
			a++;
			if (a % 2 == 1)
				continue;
			sum += a;
		}
		System.out.println(sum);
	}
}
```

### 정답

```text
30
```

### 해설

핵심 개념: 출력 형식, 연산자, static, 반복문, continue. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 10. 기출 따라잡기_문제8.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 119/기출 따라잡기_문제8.java`

### 문제

```java
public class Test {
	public static void main(String[] args) {
		int result[] = new int[5];
		int arr[] = { 77, 32, 10, 99, 50 };
		for(int i = 0; i < 5; i++) {
			result[i] = 1;
			for(int j = 0; j < 5; j++)
				if(arr[i] < arr[j])
					result[i]++;
		}
		for(int k = 0; k < 5; k++)
			System.out.print(result[k]);
	}
}
```

### 정답

```text
24513
```

### 해설

핵심 개념: 출력 형식, static, 반복문, 배열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 11. 기출 따라잡기_문제9.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 119/기출 따라잡기_문제9.java`

### 문제

```java
public class Test {
	public static void main(String[] args) {
		int r = 0;
		for (int i = 1; i < 999; i++) {
			if (i % 3 == 0 && i % 2 == 0)
				r = i;
		}
		System.out.print(r);
	}
}
```

### 정답

```text
996
```

### 해설

핵심 개념: 출력 형식, 연산자, static, 반복문. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 12. 02 Java 巩力1 - 抗力1.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 123/02 Java 巩力1 - 抗力1.java`

### 문제

```java
class ClassA {
	int a = 10;
	int funcAdd(int x, int y) {
		return x + y + a;
	}
}
public class Test {
	public static void main(String[] args) {
		int x = 3, y = 6, r;
		ClassA cal = new ClassA();
		r = cal.funcAdd(x, y);
		System.out.print(r);
	}
}
```

### 정답

```text
19
```

### 해설

핵심 개념: 출력 형식, static. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 13. 03 Java 巩力2 - 抗力1.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 123/03 Java 巩力2 - 抗力1.java`

### 문제

```java
class ClassA {
	ClassA() {
		System.out.print('A');
		this.prn();
	}
	void prn() {
		System.out.print('B');
	}
}
class ClassB extends ClassA {
	ClassB() {
		super();
		System.out.print('D');
	}
	void prn() {
		System.out.print('E');
	}
	void prn(int x) {
		System.out.print(x);
	}
}
public class Test {
	public static void main(String[] args) {
		int x = 7;
		ClassB cal = new ClassB();
		cal.prn(x);
	}
}
```

### 정답

```text
AED7
```

### 해설

핵심 개념: 출력 형식, 상속/오버라이딩, static, super. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 14. 기출 따라잡기_문제2.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 123/기출 따라잡기_문제2.java`

### 문제

```java
public class Test {
	static int[] arr() {
		int a[] = new int[4];
		int b = a.length;
		for(int i = 0; i < b; i++)
			a[i] = i;
		return a;
	}
	public static void main(String[] args) {
		int a[] = arr();
		for(int i = 0; i < a.length; i++)
			System.out.print(a[i] + " ");
	}
}
```

### 정답

```text
0 1 2 3 
```

### 해설

핵심 개념: 출력 형식, static, 반복문, 배열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다. 마지막 출력에는 공백이 하나 남습니다.

## 15. 기출 따라잡기_문제3.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 123/기출 따라잡기_문제3.java`

### 문제

```java
class A {
	int a;
	public A(int a) { this.a = a; }
	void display() { System.out.println("a=" + a); }
}
class B extends A {
	public B(int a) {
		super(a);
		super.display();
	}
}
public class Test {
	public static void main(String[] args) {
		B obj = new B(10);
	}
}
```

### 정답

```text
a=10
```

### 해설

핵심 개념: 출력 형식, 상속/오버라이딩, static, super. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 16. 기출 따라잡기_문제4.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 123/기출 따라잡기_문제4.java`

### 문제

```java
class Test {
	public static void main(String args[]) {
		cond obj = new cond(3);
		obj.a = 5;
		int b = obj.func( );
		System.out.print(obj.a + b);
	}
}

class cond {
	int a;
	public cond(int a) {
		this.a = a;
	}
	public int func( ) {
		int b = 1;
		for (int i = 1; i < a; i++)
			b += a * i;
		return a + b;
	}
}
```

### 정답

```text
61
```

### 해설

핵심 개념: 출력 형식, static, 반복문, 배열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 17. 기출 따라잡기_문제5.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 123/기출 따라잡기_문제5.java`

### 문제

```java
class A {
	int a;
	int b;
}

public class Test {
	static void func1(A m) {
		m.a *= 10;
	}
	static void func2(A m) {
		m.a += m.b;
	}
	public static void main(String args[]) {
		A m = new A();
		m.a = 100;
		func1(m);
		m.b = m.a;
		func2(m);
		System.out.printf("%d", m.a);
	}
}
```

### 정답

```text
2000
```

### 해설

핵심 개념: 출력 형식, 연산자, static, 배열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 18. 기출 따라잡기_문제6.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 123/기출 따라잡기_문제6.java`

### 문제

```java
class Parent {
	int x, y;
	Parent(int x, int y) {
		this.x = x;
		this.y = y;
	}
	int getX() {
		return x*y;
	}
}
class Child extends Parent {
	int x;
	Child(int x) {
		super(x+1, x);
		this.x = x;
	}
	int getX(int n) {
		return super.getX() + n;
	}
}
public class Main {
	public static void main(String[] args) {
		Parent parent = new Child(10);
		System.out.println(parent.getX());
	}
}
```

### 정답

```text
110
```

### 해설

핵심 개념: 출력 형식, 상속/오버라이딩, static, super. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 19. 기출 따라잡기_문제7.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 123/기출 따라잡기_문제7.java`

### 문제

```java
class Parent {
	int x, y;
	Parent(int x, int y) {
		this.x = x;
		this.y = y;
	}
	int getX() {
		return x*y;
	}
}
class Child extends Parent {
	int x;
	Child(int x) {
		super(x+1, x);
		this.x = x;
	}
	int getX(int n) {
		return super.getX() + n;
	}
}
public class Main {
	public static void main(String[] args) {
		Parent parent = new Child(10);
		System.out.println(parent.getX());
	}
}
```

### 정답

```text
110
```

### 해설

핵심 개념: 출력 형식, 상속/오버라이딩, static, super. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 20. 02 Java 巩力 - 抗力1.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 124/02 Java 巩力 - 抗力1.java`

### 문제

```java
abstract class Animal {
	String a = " is animal";
	abstract void look();
	void show() {
		System.out.println("Zoo");
	}
}
class Chicken extends Animal {
	Chicken() {
		look();
	}
	void look() {
		System.out.println("Chicken" + a);
	}
	void display() {
		System.out.println("two wings");
	}
}
public class Test {
	public static void main(String[] args) {
		Animal a = new Chicken();
		a.show();
	}
}
```

### 정답

```text
Chicken is animal
Zoo
```

### 해설

핵심 개념: 출력 형식, 상속/오버라이딩, 추상 클래스, static. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 21. 기출 따라잡기_문제1.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 124/기출 따라잡기_문제1.java`

### 문제

```java
class Parent {
	void show() { System.out.println("parent"); }
}
class Child extends Parent {
	void show() {System.out.println("child"); }
}
public class Test {
	public static void main(String[ ] args) {
		Parent pa = new Child();
		pa.show();
	}
}
```

### 정답

```text
child
```

### 해설

핵심 개념: 출력 형식, 상속/오버라이딩, static. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 22. 기출 따라잡기_문제2.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 124/기출 따라잡기_문제2.java`

### 문제

```java
abstract class Vehicle {
	String name;
	abstract public String getName(String val);
	public String getName() {
		return "Vehicle name : " + name;
	}
}
class Car extends Vehicle {
	private String name;
	public Car(String val) {
		name = super.name = val;
	}
	public String getName(String val) {
		return "Car name : " + val;
	}
	public String getName(byte[] val) {
		return "Car name : " + val;
	}
}
public class Test {
	public static void main(String[] args) {
		Vehicle obj = new Car("Spark");
		System.out.print(obj.getName());
	}
}
```

### 정답

```text
Vehicle name : Spark
```

### 해설

핵심 개념: 출력 형식, 상속/오버라이딩, 추상 클래스, static, super. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 23. 기출 따라잡기_문제3.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 124/기출 따라잡기_문제3.java`

### 문제

```java
class Parent {
	int compute(int num) {
		if(num <= 1) return num;
		return compute(num - 1) + compute(num - 2);
	}
}
class Child extends Parent {
	int compute(int num) {
		if(num <= 1) return num;
		return compute(num - 1) + compute(num - 3);
	}
}
public class Test {
	public static void main(String[] args) {
		Parent obj = new Child();
		System.out.print(obj.compute(4));
	}
}
```

### 정답

```text
1
```

### 해설

핵심 개념: 출력 형식, 연산자, 상속/오버라이딩, static. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 24. 기출 따라잡기_문제2.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 127/기출 따라잡기_문제2.java`

### 문제

```java
public class Main {
	public static void main(String[] args) {
		int sum = 0;
		try {
			func( );
		}
		catch (NullPointerException e) {
			sum = sum + 1;
		}
		catch (Exception e) {
			sum = sum + 10;
		}
		finally {
			sum = sum + 100;
		}
		System.out.print(sum);
	}
	static void func( ) throws Exception {
		throw new NullPointerException( );
	}
}
```

### 정답

```text
101
```

### 해설

핵심 개념: 출력 형식, static. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 25. 기출 따라잡기_문제3.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/Section 127/기출 따라잡기_문제3.java`

### 문제

```java
public class Main {
	static interface F {
		int apply(int x) throws Exception;
	}
	public static int run(F f) {
		try {
			return f.apply(3);
		} catch (Exception e) {
			return 7;
		}
	}
	public static void main(String[] args) {
		F f = (x) -> {
			if (x > 2) {
				throw new Exception( );
			}
			return x * 2;
		};
		System.out.print(run(f) + run((int n) -> n + 9));
	}
}
```

### 정답

```text
19
```

### 해설

핵심 개념: 출력 형식, 인터페이스, static. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 26. 문제10.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제10.java`

### 문제

```java
public class Problem {
	public static void main(String[] args) {
		int a = 035, b = 0x35, c = 35;
		System.out.printf("%d\n", a);
		System.out.printf("%d\n", b);
		System.out.printf("%d\n", c);
	}
}
```

### 정답

```text
29
53
35
```

### 해설

핵심 개념: 출력 형식, 연산자, static. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 27. 문제11.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제11.java`

### 문제

```java
public class Problem {
	public static void main(String[] args) {
		int j, k, L, result;
		j = 10;
		k = 20;
		L = 30;
		result = j < k ? k++ : --L;
		System.out.printf("%d %d %d\n", result, k, L);
	}
}
```

### 정답

```text
20 21 30
```

### 해설

핵심 개념: 출력 형식, 연산자, static. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 28. 문제14.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제14.java`

### 문제

```java
public class Problem {
	public static void main(String[] args) {
		int a, b = 10;
		a = 20 % 11 / 3 * 5 - b;
		System.out.printf("%d\n", a);
	}
}
```

### 정답

```text
5
```

### 해설

핵심 개념: 출력 형식, 연산자, static. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 29. 문제16.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제16.java`

### 문제

```java
public class Problem {
	public static void main(String[] args){
		int a, b, c, hap;
		a = b = c = 2;
		hap = ++a | b-- & c--;
		System.out.printf("%d %d %d %d", hap, a, b, c);
	}
}
```

### 정답

```text
3 3 1 1
```

### 해설

핵심 개념: 출력 형식, 연산자, static. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 30. 문제17.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제17.java`

### 문제

```java
public class Test {
	public static void main(String[] args) {
		String str = "ITISTESTSTRING";
		String[] result = str.split("T");
		System.out.print(result[3]);
	}
}
```

### 정답

```text
S
```

### 해설

핵심 개념: 출력 형식, static, 배열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 31. 문제24.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제24.java`

### 문제

```java
class Static {
	public int a = 20;
	static int b = 0;
}

public class Test {
	public static void main(String[] args) {
		int a = 10;
		Static.b = a;
		Static st = new Static();
		System.out.println(Static.b++);
		System.out.println(st.b);
		System.out.println(a);
		System.out.print(st.a);
	}
}
```

### 정답

```text
10
11
10
20
```

### 해설

핵심 개념: 출력 형식, static. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 32. 문제30.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제30.java`

### 문제

```java
public class Main {
	public static class BO {
		public int v;
		public BO(int v) {
			this.v = v;
		}
	}
	public static void main(String[] args) {
		BO a = new BO(1);
		BO b = new BO(2);
		BO c = new BO(3);
		BO[] arr = {a, b, c};
		BO t = arr[0];
		arr[0] = arr[2];
		arr[2] = t;
		arr[1].v = arr[0].v;
		System.out.println(a.v + "a" + b.v + "b" + c.v);
	}
}
```

### 정답

```text
1a3b3
```

### 해설

핵심 개념: 출력 형식, static. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 33. 문제31.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제31.java`

### 문제

```java
public class Test {
	public static void main(String[] args) {
		String str1 = "Programming";
		String str2 = "Programming";
		String str3 = new String("Programming");
		System.out.println(str1==str2);
		System.out.println(str1==str3);
		System.out.println(str1.equals(str3));
		System.out.println(str2.equals(str3));
	}
}
```

### 정답

```text
true
false
true
true
```

### 해설

핵심 개념: 출력 형식, 연산자, static. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 34. 문제32.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제32.java`

### 문제

```java
public class Main {
	public static void main(String[ ] args) {
		new Child( );
		System.out.println(Parent.total);
	}
}
class Parent {
	static int total = 0;
	int v = 1;
	public Parent( ) {
		total += ++v;
		show( );
	}
	public void show( ) {
		total += total;
	}
}
class Child extends Parent {
	int v = 10;
	public Child( ) {
		v += 2;
		total += v++;
		show( );
		}
	@Override
	public void show( ) {
		total += total * 2;
	}
}
```

### 정답

```text
54
```

### 해설

핵심 개념: 출력 형식, 상속/오버라이딩, static. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 35. 문제33.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제33.java`

### 문제

```java
class Rectangle {
	int x, y;
	Rectangle(int x, int y) {
		this.x = x;
		this.y = y;
	}
	int getArea( ) {
		return x*y;
	}
}
class Square extends Rectangle {
	Square(int a) {
		super(a, a);
	}
	int getSquareArea( ) {
		return x*y;
	}
}
public class Main {
	public static void main(String[] args) {
		Square sq = new Square(10);
		System.out.println(sq.getSquareArea( ));
	}
}
```

### 정답

```text
100
```

### 해설

핵심 개념: 출력 형식, 상속/오버라이딩, static, super. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 36. 문제35.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제35.java`

### 문제

```java
public class Main {
	public static void main(String[ ] args) {
		int a = 5, b = 0;
		try {
			System.out.print(a/b);
		}
		catch(ArithmeticException e){
			System.out.print("출력1");
		}
		catch(ArrayIndexOutOfBoundsException e) {
			System.out.print("출력2");
		}
		catch(NumberFormatException e) {
			System.out.print("출력3");
		}
		catch(Exception e) {
			System.out.print("출력4");
		}
		finally {
			System.out.print("출력5");
		}
	}
}
```

### 정답

```text
출력1출력5
```

### 해설

핵심 개념: 출력 형식, 연산자, static. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 37. 문제37.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제37.java`

### 문제

```java
enum Tri {
	A("A"), B("AB"), C("ABC");
	private String code;
		Tri(String code) {
	this.code = code;
	}
	public String code( ) {
		return code;
	}
}
public class Main {
	public static void main(String[] args) {
		Tri t = Tri.values( )[Tri.A.name( ).length( )];
		System.out.print(t.code( ));
	}
}
```

### 정답

```text
AB
```

### 해설

핵심 개념: 출력 형식, enum, static. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 38. 문제43.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제43.java`

### 문제

```java
public class Test {
	public static void check(int[] x, int[] y)
	{
		if(x == y) System.out.print("O");
		else System.out.print("N");
	}
	public static void main(String[] args) {
		int a[] = new int[] {1, 2, 3, 4};
		int b[] = new int[] {1, 2, 3, 4};
		int c[] = new int[] {1, 2, 3};
		check(a, b);
		check(b, c);
		check(a, c);
	}
}
```

### 정답

```text
NNN
```

### 해설

핵심 개념: 출력 형식, 연산자, static, 배열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 39. 문제44.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제44.java`

### 문제

```java
interface Number {
	int sum(int[] a, boolean odd);
}
public class Test {
	public static void main(String[] args) {
		int a[] = {1, 2, 3, 4, 5, 6, 7, 8, 9};
		OENumber OE = new OENumber( );
		System.out.print(OE.sum(a, true) + ", " + OE.sum(a, false));
	}
}
class OENumber implements Number {
	public int sum(int[] a, boolean odd) {
		int result = 0;
		for (int i = 0; i < a.length; i++) {
			if ((odd && a[i] % 2 != 0) || (!odd && a[i] % 2 == 0)) {
				result += a[i];
			}
		}
		return result;
	}
}
```

### 정답

```text
25, 20
```

### 해설

핵심 개념: 출력 형식, 연산자, 인터페이스, static, 반복문, 배열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 40. 문제45.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제45.java`

### 문제

```java
public class Test {
	public static String rf(String str, int index, boolean[] seen) {
		if(index < 0) return "";
		char c = str.charAt(index);
		String result = rf(str, index-1, seen);
		if(!seen[c]) {
			seen[c] = true;
			return c + result;
		}
		return result;
	}
	public static void main(String[] args) {
		String str = "abacabcd";
		int len = str.length( );
		boolean[] seen = new boolean[256];
		System.out.print(rf(str, len-1, seen));
	}
}
```

### 정답

```text
dcba
```

### 해설

핵심 개념: 출력 형식, static, 배열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 41. 문제47.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제47.java`

### 문제

```java
class Printer {
	void print(Integer a) {
		System.out.print("A" + a);
	}
	void print(Object a) {
		System.out.print("B" + a);
	}
	void print(Number a) {
		System.out.print("C" + a);
	}
}
public class Main {
	public static void main(String[] args) {
		new Collection<>(0).print( );
	}
	public static class Collection<T> {
		T value;
		public Collection(T t) {
			value = t;
		}
		public void print( ) {
			new Printer( ).print(value);
		}
	}
}
```

### 정답

```text
B0
```

### 해설

핵심 개념: 출력 형식, static, 제네릭. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 42. 문제48.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제48.java`

### 문제

```java
public class Main{
	static String[] x = new String[3];
	static void func(String[] x, int y) {
		for(int i = 1; i < y; i++) {
			if(x[i-1].equals(x[i])) {
				System.out.print("O");
			}
			else {
				System.out.print("N");
			}
		}
		for (String z : x) {
			System.out.print(z);
		}
	}
	public static void main(String[] args) {
		x[0] = "A";
		x[1] = "A";
		x[2] = new String("A");
		func(x, 3);
	}
}
```

### 정답

```text
OOAAA
```

### 해설

핵심 개념: 출력 형식, static, 반복문, 배열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 43. 문제49.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제49.java`

### 문제

```java
class Connection {
	private static Connection _inst = null;
	private int count = 0;
	public static Connection get() {
		if(_inst == null) {
			_inst = new Connection();
			return _inst;
		}
		return _inst;
	}
	public void count() { count++; }
	public int getCount() { return count; }
}
public class Test {
	public static void main(String[] args) {
		Connection conn1 = Connection.get();
		conn1.count();
		Connection conn2 = Connection.get();
		conn2.count();
		Connection conn3 = Connection.get();
		conn3.count();
		System.out.print(conn1.getCount());
	}
}
```

### 정답

```text
3
```

### 해설

핵심 개념: 출력 형식, 연산자, static. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 44. 문제7.java

- 원본 경로: `2026_정보처리기사_실기_10장코드모음/예상문제은행/문제7.java`

### 문제

```java
public class Test {
	public static void main(String[] args) {
		int i = 0, c = 0;
		while (i < 10) {
			i++;
			c *= i;
		}
		System.out.println(c);
	}
}
```

### 정답

```text
0
```

### 해설

핵심 개념: 출력 형식, static, 반복문. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 45. 311 데이터 입출력 - Java 예상체크1.java

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/311 데이터 입출력 - Java 예상체크1.java`

### 문제

```java
import java.util.Scanner;

public class Test {
	public static void main(String args[ ]) {
		Scanner scan = new Scanner(System.in); 
		int a = scan.nextInt( ); 
		int b = scan.nextInt( ); 
		System.out.printf("%d", a + b); 
		scan.close( );
	}
}
```

### 정답

두 정수 `a`, `b`를 입력하면 `a + b`가 출력됩니다.

### 해설

핵심 개념: 입력 처리, 출력 형식, 연산자, static. `Scanner`로 읽은 두 값을 더해 `printf`로 출력합니다.

## 46. 311 데이터 입출력 - Java.java

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/311 데이터 입출력 - Java.java`

### 문제

```java
import java.util.Scanner;
public class Test
{
	public static void main(String[] args)
	{
		Scanner scan = new Scanner(System.in);
		int a = scan.nextInt();
		System.out.printf("a * 3 = %d\n", a * 3);
		System.out.println("a / 2 = " + (a / 2));
		System.out.print("a - 1 = " + (a - 1));
		scan.close();
	}
}
```

### 정답

정수 `a`를 입력하면 `a * 3`, `a / 2`의 정수 나눗셈 결과, `a - 1`이 차례대로 출력됩니다.

### 해설

핵심 개념: 입력 처리, 출력 형식, 연산자, static. Java의 `int / int`는 소수부를 버리는 정수 나눗셈입니다.

## 47. 318 제어문 - Java 기출체크1.java

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/318 제어문 - Java 기출체크1.java`

### 문제

```java
public class Test {
	public static void main(String[] args) {
		int j, i;
		for (j = 0, i = 0; i <= 5; i++) {
			j += i;
			System.out.print(i);
			if (i == 5) {
				System.out.print("=");
				System.out.print(j);
			}
			else
				System.out.print("+");
		}
	}
}
```

### 정답

```text
0+1+2+3+4+5=15
```

### 해설

핵심 개념: 출력 형식, 연산자, static, 반복문. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 48. 318 제어문 - Java 기출체크2.java

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/318 제어문 - Java 기출체크2.java`

### 문제

```java
public class Test {
	public static void main(String[] args) {
		int r = 0;
		for (int i = 1; i < 999; i++) {
			if (i % 3 == 0 && i % 2 == 0)
				r = i;
		}
		System.out.print(r);
	}
}
```

### 정답

```text
996
```

### 해설

핵심 개념: 출력 형식, 연산자, static, 반복문. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 49. 318 제어문 - Java.java

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/318 제어문 - Java.java`

### 문제

```java
public class Test {
	public static void main(String[] args) {
		String str = "agile";
		int x[] = { 1, 2, 3, 4, 5 };
		char y[] = new char[5];
		int i = 0;
		while (i < str.length()) {
			y[i] = str.charAt(i);
			i++;
		}
		for (int p : x) {
			i--;
			System.out.print(y[i]);
			System.out.print(p + " ");
		}
	}
}
```

### 정답

```text
e1 l2 i3 g4 a5 
```

### 해설

핵심 개념: 출력 형식, static, 반복문, 배열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다. 마지막 출력에는 공백이 하나 남습니다.

## 50. 319 break와 continue 기출체크1.java

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/319 break와 continue 기출체크1.java`

### 문제

```java
public class Test{
	public static void main(String[] args){
		int a = 0, sum = 0;
		while (a < 10) {
			a++;
			if (a % 2 == 1)
				continue;
			sum += a;
		}
		System.out.println(sum);
	}
}
```

### 정답

```text
30
```

### 해설

핵심 개념: 출력 형식, 연산자, static, 반복문, continue. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 51. 323 Java의 클래스1 기출체크1.java

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/323 Java의 클래스1 기출체크1.java`

### 문제

```java
class A {
	int a;
	int b;
}
public class Test {
	static void func1(A m) {
		m.a *= 10;
	}
	static void func2(A m) {
		m.a += m.b;
	}
	public static void main(String args[]) {
		A m = new A();
		m.a = 100;
		func1(m);
		m.b = m.a;
		func2(m);
		System.out.printf("%d", m.a);
	}
}
```

### 정답

```text
2000
```

### 해설

핵심 개념: 출력 형식, 연산자, static, 배열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 52. 323 Java의 클래스1 기출체크2.java

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/323 Java의 클래스1 기출체크2.java`

### 문제

```java
class Static {
	public int a = 20;
	static int b = 0;
}

public class Test {
	public static void main(String[] args) {
		int a = 10;
		Static.b = a;
		Static st = new Static();
		System.out.println(Static.b++);
		System.out.println(st.b);
		System.out.println(a);
		System.out.print(st.a);
	}
}
```

### 정답

```text
10
11
10
20
```

### 해설

핵심 개념: 출력 형식, static. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 53. 323 Java의 클래스1.java

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/323 Java의 클래스1.java`

### 문제

```java
class ClassA {
	int a = 10;
	int funcAdd(int x, int y) {
		return x + y + a;
	}
}
public class Test {
	public static void main(String[] args) {
		int x = 3, y = 6, r;
		ClassA cal = new ClassA();
			r = cal.funcAdd(x, y);
		System.out.print(r);
	}
}
```

### 정답

```text
19
```

### 해설

핵심 개념: 출력 형식, static. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 54. 324 Java의 클래스2 기출체크1.java

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/324 Java의 클래스2 기출체크1.java`

### 문제

```java
class A {
	int a;
	public A(int a) { this.a = a; }
	void display() { System.out.println("a=" + a); }
}
class B extends A {
	public B(int a) {
		super(a);
		super.display();
	}
}
public class Test {
	public static void main(String[] args) {
		B obj = new B(10);
	}
}
```

### 정답

```text
a=10
```

### 해설

핵심 개념: 출력 형식, 상속/오버라이딩, static, super. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 55. 324 Java의 클래스2.java

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/324 Java의 클래스2.java`

### 문제

```java
public class Main {
	public static class Parent {
		public int x(int i) { return i + 2; }
		public static String id( ) { return "P"; }
	}
	public static class Child extends Parent {
		public int x(int i) { return i + 3; }
		public String x(String s) { return s + "R"; }
		public static String id( ) { return "C"; }
	}
	public static void main(String[] args) {
		Parent ref = new Child( );
		System.out.println(ref.x(2) + ref.id( ));
	}
}
```

### 정답

```text
5P
```

### 해설

핵심 개념: 출력 형식, 상속/오버라이딩, static. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 56. 326 Java의 활용 기출체크1.java

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/326 Java의 활용 기출체크1.java`

### 문제

```java
abstract class Vehicle {
	String name;
	abstract public String getName(String val);
	public String getName() {
		return "Vehicle name : " + name;
	}
}
class Car extends Vehicle {
	private String name;
	public Car(String val) {
		name = super.name = val;
	}
	public String getName(String val) {
		return "Car name : " + val;
	}
	public String getName(byte[] val) {
		return "Car name : " + val;
	}
}
public class Test {
	public static void main(String[] args) {
		Vehicle obj = new Car("Spark");
		System.out.print(obj.getName());
	}
}
```

### 정답

```text
Vehicle name : Spark
```

### 해설

핵심 개념: 출력 형식, 상속/오버라이딩, 추상 클래스, static, super. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 57. 326 Java의 활용.java

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/326 Java의 활용.java`

### 문제

```java
abstract class Animal {
	String a = " is animal";
	abstract void look();
	void show() {
		System.out.println("Zoo");
	}
}
class Chicken extends Animal {
	Chicken() {
		look();
	}
	void look() {
		System.out.println("Chicken" + a);
	}
	void display() {
		System.out.println("two wings");
	}
}
public class Test {
	public static void main(String[] args) {
		Animal a = new Chicken();
		a.show();
	}
}
```

### 정답

```text
Chicken is animal
Zoo
```

### 해설

핵심 개념: 출력 형식, 상속/오버라이딩, 추상 클래스, static. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 58. 문제 04.java

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/예상문제은행/문제 04.java`

### 문제

```java
class Parent {
	int compute(int num) {
		if(num <= 1) return num;
		return compute(num - 1) + compute(num - 2);
	}
}
class Child extends Parent {
	int compute(int num) {
		if(num <= 1) return num;
		return compute(num - 1) + compute(num - 3);
	}
}
public class Test {
	public static void main(String[] args) {
		Parent obj = new Child();
		System.out.print(obj.compute(4));
	}
}
```

### 정답

```text
1
```

### 해설

핵심 개념: 출력 형식, 연산자, 상속/오버라이딩, static. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 59. 문제 07.java

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/예상문제은행/문제 07.java`

### 문제

```java
public class Test {
	public static void main(String[] args) {
		System.out.print(Test.check(1));
	}
	static String check(int num){
		return (num >= 0) ? "positive" : "negative";
	}
}
```

### 정답

```text
positive
```

### 해설

핵심 개념: 출력 형식, 연산자, static. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 60. 문제 20.java

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/예상문제은행/문제 20.java`

### 문제

```java
public class Test {
	public static void main(String[] args) {
		String str1 = "Programming";
		String str2 = "Programming";
		String str3 = new String("Programming");
		System.out.println(str1==str2);
		System.out.println(str1==str3);
		System.out.println(str1.equals(str3));
		System.out.println(str2.equals(str3));
	}
}
```

### 정답

```text
true
false
true
true
```

### 해설

핵심 개념: 출력 형식, 연산자, static. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 61. 문제 21.java

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/예상문제은행/문제 21.java`

### 문제

```java
class SuperObject {
	public void draw() {
		System.out.println("A");
		draw();
	}
	public void paint() {
		System.out.print('B');
		draw();
	}
}
class SubObject extends SuperObject {
	public void paint() {
		super.paint();
		System.out.print('C');
		draw();
	}
	public void draw() {
		System.out.print('D');
	}
}
public class Test {
	public static void main(String[] args) {
		SuperObject a = new SubObject();
		a.paint();
		a.draw();
	}
}
```

### 정답

```text
BDCDD
```

### 해설

핵심 개념: 출력 형식, 상속/오버라이딩, static, super. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 62. 문제 22.java

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/예상문제은행/문제 22.java`

### 문제

```java
class Connection {
	private static Connection _inst = null;
	private int count = 0;
	public static Connection get() {
		if(_inst == null) {
			_inst = new Connection();
			return _inst;
		}
		return _inst;
	}
	public void count() { count++; }
	public int getCount() { return count; }
}
public class Test {
	public static void main(String[] args) {
		Connection conn1 = Connection.get();
		conn1.count();
		Connection conn2 = Connection.get();
		conn2.count();
		Connection conn3 = Connection.get();
		conn3.count();
		conn1.count();
		System.out.print(conn1.getCount());
	}
}
```

### 정답

```text
4
```

### 해설

핵심 개념: 출력 형식, 연산자, static. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 63. 문제 23.java

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/예상문제은행/문제 23.java`

### 문제

```java
class P {
	public int calc(int n) {
		if (n <= 1) return n;
		return calc(n - 1) + calc(n - 2);
	}
}
class C extends P {
	public int calc(int n) {
		if (n <= 1) return n;
		return calc(n - 1) + calc(n - 3);
	}
}
public class Test {
	public static void main(String[] args) {
		P obj = new C();
		System.out.print(obj.calc(7));
	}
}
```

### 정답

```text
2
```

### 해설

핵심 개념: 출력 형식, 연산자, 상속/오버라이딩, static. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 64. 문제 27.java

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/예상문제은행/문제 27.java`

### 문제

```java
public class Test {
	public static void main(String[] args) {
		int ary[][] = new int[3][5];
		int n = 1;
		for(int i = 0; i < 3; i++) {
			for(int j = 0; j < 5; j++) {
			ary[i][j] = j * 3 + i + 1;
			System.out.print(ary[i][j] + " ");
			}
			System.out.println();
		}
	}
}
```

### 정답

```text
1 4 7 10 13 
2 5 8 11 14 
3 6 9 12 15 
```

### 해설

핵심 개념: 출력 형식, static, 반복문, 배열. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 65. 문제 31.java

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/예상문제은행/문제 31.java`

### 문제

```java
class Car implements Runnable {
	int a;
	public void run() {
		try {
			while(++a < 100) {
				System.out.println("miles traveled : " + a);
				Thread.sleep(100);
			}
		} catch(Exception E) { }
	}
}

public class Test {
	public static void main(String args[]) {
		Thread t1 = new Thread(new Car());
		t1.start();
	}
}
```

### 정답

```text
miles traveled : 1
miles traveled : 2
miles traveled : 3
miles traveled : 4
miles traveled : 5
miles traveled : 6
miles traveled : 7
miles traveled : 8
miles traveled : 9
miles traveled : 10
miles traveled : 11
miles traveled : 12
miles traveled : 13
miles traveled : 14
miles traveled : 15
miles traveled : 16
miles traveled : 17
miles traveled : 18
miles traveled : 19
miles traveled : 20
miles traveled : 21
miles traveled : 22
miles traveled : 23
miles traveled : 24
miles traveled : 25
miles traveled : 26
miles traveled : 27
miles traveled : 28
miles traveled : 29
miles traveled : 30
miles traveled : 31
miles traveled : 32
miles traveled : 33
miles traveled : 34
miles traveled : 35
miles traveled : 36
miles traveled : 37
miles traveled : 38
miles traveled : 39
miles traveled : 40
miles traveled : 41
miles traveled : 42
miles traveled : 43
miles traveled : 44
miles traveled : 45
miles traveled : 46
miles traveled : 47
miles traveled : 48
miles traveled : 49
miles traveled : 50
miles traveled : 51
miles traveled : 52
miles traveled : 53
miles traveled : 54
miles traveled : 55
miles traveled : 56
miles traveled : 57
miles traveled : 58
miles traveled : 59
miles traveled : 60
miles traveled : 61
miles traveled : 62
miles traveled : 63
miles traveled : 64
miles traveled : 65
miles traveled : 66
miles traveled : 67
miles traveled : 68
miles traveled : 69
miles traveled : 70
miles traveled : 71
miles traveled : 72
miles traveled : 73
miles traveled : 74
miles traveled : 75
miles traveled : 76
miles traveled : 77
miles traveled : 78
miles traveled : 79
miles traveled : 80
miles traveled : 81
miles traveled : 82
miles traveled : 83
miles traveled : 84
miles traveled : 85
miles traveled : 86
miles traveled : 87
miles traveled : 88
miles traveled : 89
miles traveled : 90
miles traveled : 91
miles traveled : 92
miles traveled : 93
miles traveled : 94
miles traveled : 95
miles traveled : 96
miles traveled : 97
miles traveled : 98
miles traveled : 99
```

### 해설

핵심 개념: 출력 형식, static, 스레드, 반복문, 배열. 새 스레드에서 `++a < 100` 조건을 검사하므로 `a`가 1부터 99일 때만 각 줄이 출력됩니다.

## 66. 문제 33.java

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/예상문제은행/문제 33.java`

### 문제

```java
public class Main { 
    public static class BO { 
        public int v; public BO(int v) { 
            this.v = v; 
        } 
    } 
    public static void main(String[] args) { 
        BO a = new BO(1); 
        BO b = new BO(2); 
        BO c = new BO(3); 
        BO[] arr = {a, b, c}; 
        BO t = arr[0]; 
        arr[0] = arr[2]; 
        arr[2] = t; 
        arr[1].v = arr[0].v; 
        System.out.println(a.v + "a" + b.v + "b" + c.v); 
    }
}
```

### 정답

```text
1a3b3
```

### 해설

핵심 개념: 출력 형식, static. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 67. 문제 35.java

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/예상문제은행/문제 35.java`

### 문제

```java
enum Tri { 
    A("A"), B("AB"), C("ABC"); 
    private String code; 
    Tri(String code) { 
        this.code = code; 
        
    }
    public String code( ) { 
        return code;
        }
} 

public class Main { 
    public static void main(String[] args) { 
        Tri t = Tri.values( )[Tri.A.name( ).length( )]; 
        System.out.print(t.code( ));
        }

}
```

### 정답

```text
AB
```

### 해설

핵심 개념: 출력 형식, enum, static. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 68. 문제 39.java

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/예상문제은행/문제 39.java`

### 문제

```java
class Printer { 
    void print(Integer a) { 
        System.out.print("A" + a); 
    } 
    void print(Object a) {
        System.out.print("B" + a);
    }
    void print(Number a) { 
        System.out.print("C" + a);
    }
}

public class Main { 
    public static void main(String[] args) { 
        new Collection<>(0).print( );
    } 
    public static class Collection<T> { 
        T value; 
        public Collection(T t) { 
            value = t;
        } 
        public void print( ) { 
            new Printer( ).print(value);
        }
    }
}
```

### 정답

```text
B0
```

### 해설

핵심 개념: 출력 형식, static, 제네릭. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.

## 69. 문제 02.java

- 원본 경로: `2026_정보처리기사_실기_총정리_10장 코드모음/예상문제은행/문제 02.java`

### 문제

```java
class Parent { 
	void show( ) { System.out.println("parent"); }
}
class Child extends Parent { 
	void show( ) {  System.out.println("child"); }
}
public class Test {
	public static void main(String[ ] args) {
		Parent pa = new Child( );
		pa.show( );
	}
}
```

### 정답

```text
child
```

### 해설

핵심 개념: 출력 형식, 상속/오버라이딩, static. 입력 없는 원본 코드를 컴파일/실행해 출력값을 재검산했고, 출력문에 전달되는 값과 줄바꿈을 그대로 반영했습니다.
