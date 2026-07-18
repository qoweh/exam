# 정보처리기사 실기 Java — 선택 문제와 시험 문법 노트

선택한 원문 번호: 7, 13, 18, 23, 24, 28, 32, 36, 40, 44  
추가 외부문제: 배열 참조와 String 매개변수  
중복 코드: 선택한 Java 문제끼리는 중복 없음

---

## 외부문제 — 배열 참조와 String 매개변수

```java
public class Main {
    public static void change(String[] data, String s) {
        data[0] = s;
        s = "Z";
    }

    public static void main(String[] args) {
        String data[] = { "A" };
        String s = "B";

        change(data, s);
        System.out.println(data[0] + s);
    }
}
```

정답

```text
BB
```

풀이

Java는 메서드 호출 시 매개변수에 값을 복사해서 전달한다. 참조형도 예외가 아니며, 객체 자체가 넘어가는 것이 아니라 객체를 가리키는 참조값이 복사되어 넘어간다.

|단계|`data[0]`|`main`의 `s`|`change`의 `s`|설명|
|---|---:|---:|---:|---|
|초기값|`"A"`|`"B"`|-|`data` 배열의 첫 칸은 `"A"`, 변수 `s`는 `"B"`를 가리킨다.|
|`change(data, s)` 호출|`"A"`|`"B"`|`"B"`|배열 참조값과 문자열 참조값이 매개변수로 복사된다.|
|`data[0] = s;`|`"B"`|`"B"`|`"B"`|배열 객체의 0번 칸을 바꾸므로 `main`의 `data[0]`도 바뀐다.|
|`s = "Z";`|`"B"`|`"B"`|`"Z"`|매개변수 `s`만 새 문자열을 가리키게 된다. `main`의 `s`는 바뀌지 않는다.|
|출력|`"B"`|`"B"`|-|`data[0] + s`는 `"B" + "B"`가 된다.|

핵심은 `data[0] = s`는 배열 객체 내부를 변경하지만, `s = "Z"`는 지역 변수인 매개변수 `s`가 가리키는 대상만 바꾼다는 점이다. 따라서 `change`가 끝난 뒤에도 `main`의 `s`는 `"B"` 그대로이고, 출력은 `BB`가 된다.

---

## 문제 44 — 인스턴스 메서드 오버라이딩과 static 메서드 숨김

```java
class Parent {
    int x(int i) {
        return i + 2;
    }

    static String id() {
        return "P";
    }
}

class Child extends Parent {
    int x(int i) {
        return i + 3;
    }

    int x(String s) {
        return s.length();
    }

    static String id() {
        return "C";
    }
}

public class Main {
    public static void main(String[] args) {
        Parent ref = new Child();
        System.out.println(ref.x(2) + ref.id());
    }
}
```

정답

```text
5P
```

풀이

`ref`의 선언 타입은 `Parent`, 실제 객체는 `Child`다.

|식|결과|이유|
|---|---|---|
|`ref.x(2)`|5|인스턴스 메서드는 오버라이딩되어 실제 객체 `Child`의 `x(int)`가 실행된다.|
|`ref.id()`|`"P"`|`static` 메서드는 오버라이딩이 아니라 숨김이며, 선언 타입 `Parent` 기준으로 선택된다.|
|`5 + "P"`|`"5P"`|문자열과 더하면 문자열 연결이 된다.|

`Child`의 `x(String)`은 인수 타입이 다르므로 오버로딩일 뿐이고, `ref.x(2)`에는 관여하지 않는다.

---

## 문제 7 — 가변 길이 2차원 배열

```java
public class Main {
    public static void main(String[] args) {
        int aa[][] = {{45, 50, 75}, {89}};

        System.out.println(aa[0].length);
        System.out.println(aa[1].length);
        System.out.println(aa[0][0]);
        System.out.println(aa[0][1]);
        System.out.println(aa[1][0]);
    }
}
```

정답

```text
3
1
45
50
89
```

풀이

Java의 2차원 배열은 “배열의 배열”이다. 따라서 각 행의 길이가 서로 달라도 된다.

|식|뜻|값|
|---|---|---:|
|`aa[0]`|첫 번째 행 `{45, 50, 75}`|길이 3|
|`aa[1]`|두 번째 행 `{89}`|길이 1|
|`aa[0][0]`|첫 번째 행의 첫 원소|45|
|`aa[0][1]`|첫 번째 행의 둘째 원소|50|
|`aa[1][0]`|두 번째 행의 첫 원소|89|

`aa[1][1]`처럼 없는 칸을 접근하면 `ArrayIndexOutOfBoundsException`이 난다.

---

## 문제 13 — 생성자, 상속, 오버라이딩

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

public class Main {
    public static void main(String[] args) {
        int x = 7;
        ClassB cal = new ClassB();
        cal.prn(x);
    }
}
```

정답

```text
AED7
```

풀이

`new ClassB()`가 실행되면 자식 생성자 본문보다 부모 생성자가 먼저 실행된다.

|순서|실행 내용|출력|
|---|---|---|
|1|`ClassB()` 생성 시작, `super()`로 부모 생성자 호출| |
|2|`ClassA()`에서 `System.out.print('A')`|`A`|
|3|`this.prn()` 호출|실제 객체는 `ClassB`이므로 오버라이딩된 `ClassB.prn()` 실행|
|4|`ClassB.prn()`|`E`|
|5|부모 생성자 종료 후 자식 생성자 본문 실행|`D`|
|6|`cal.prn(x)`는 인수 1개이므로 `prn(int x)` 호출|`7`|

그래서 출력은 `A` → `E` → `D` → `7` 순서다. 부모 생성자 안의 `this`도 실제 객체를 가리키므로 오버라이딩 메서드가 호출된다는 점이 시험 포인트다.

---

## 문제 18 — 오버로딩과 오버라이딩 구분

```java
class Parent {
    int x, y;

    Parent(int x, int y) {
        this.x = x;
        this.y = y;
    }

    int getX() {
        return x * y;
    }
}

class Child extends Parent {
    int x;

    Child(int x) {
        super(x + 1, x);
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

정답

```text
110
```

풀이

`new Child(10)`에서 자식 생성자의 매개변수 `x`는 10이다.

|단계|계산|
|---|---|
|`super(x + 1, x)`|부모 필드 `Parent.x = 11`, `Parent.y = 10`|
|`this.x = x`|자식 필드 `Child.x = 10`|
|`parent.getX()`|매개변수 없는 `getX()` 호출|

`Child`에는 `getX(int n)`만 있고, `getX()`는 없다. 즉 `getX(int)`는 오버라이딩이 아니라 오버로딩이다. 따라서 `parent.getX()`는 부모의 `getX()`를 실행하고, `11 * 10 = 110`이 출력된다.

---

## 문제 23 — 예외 처리 순서와 finally

```java
public class Main {
    public static void main(String[] args) {
        int sum = 0;

        try {
            func();
        } catch (NullPointerException e) {
            sum += 1;
        } catch (Exception e) {
            sum += 10;
        } finally {
            sum += 100;
        }

        System.out.print(sum);
    }

    static void func() throws Exception {
        throw new NullPointerException();
    }
}
```

정답

```text
101
```

풀이

`func()`는 `NullPointerException`을 던진다. `NullPointerException`은 `Exception`의 하위 클래스이지만, 더 구체적인 `catch (NullPointerException e)`가 먼저 있으므로 이 블록이 실행된다.

|구간|실행 여부|`sum`|
|---|---|---:|
|초기값|실행|0|
|`try`의 `func()`|예외 발생|0|
|`catch (NullPointerException e)`|실행, `sum += 1`|1|
|`catch (Exception e)`|앞에서 처리되어 미실행|1|
|`finally`|항상 실행, `sum += 100`|101|

따라서 출력은 `101`이다. 예외 문제에서는 `catch` 순서가 중요하다. 넓은 타입인 `Exception`을 먼저 쓰면 뒤의 구체적인 예외는 도달할 수 없어 컴파일 오류가 난다.

---

## 문제 24 — 함수형 인터페이스와 람다 예외

```java
public class Main {
    static interface F {
        int apply(int x) throws Exception;
    }

    static int run(F f) {
        try {
            return f.apply(3);
        } catch (Exception e) {
            return 7;
        }
    }

    public static void main(String[] args) {
        F f = (x) -> {
            if (x > 2) throw new Exception();
            return x * 2;
        };

        System.out.print(run(f) + run((int n) -> n + 9));
    }
}
```

정답

```text
19
```

풀이

`run`은 항상 `f.apply(3)`을 호출한다.

|호출|람다식|`apply(3)` 결과|`run` 반환|
|---|---|---|---:|
|`run(f)`|`x > 2`이면 예외|`3 > 2`라서 예외 발생|7|
|`run((int n) -> n + 9)`|`n + 9`|`3 + 9 = 12`|12|

최종 출력은 `7 + 12 = 19`다. `F.apply`에 `throws Exception`이 선언되어 있으므로 첫 번째 람다 안에서 `throw new Exception()`을 쓸 수 있다.

---

## 문제 28 — 전위·후위 증감과 비트 연산자 우선순위

```java
public class Main {
    public static void main(String[] args) {
        int a, b, c, hap;
        a = b = c = 2;

        hap = ++a | b-- & c--;

        System.out.printf("%d %d %d %d", hap, a, b, c);
    }
}
```

정답

```text
3 3 1 1
```

풀이

Java에서 이 식은 `++a | (b-- & c--)`처럼 계산한다. `&`가 `|`보다 우선순위가 높다.

|부분|계산|결과|
|---|---|---:|
|초기값|`a = 2`, `b = 2`, `c = 2`| |
|`++a`|먼저 증가 후 사용|3|
|`b--`|값 2를 사용한 뒤 `b`는 1|2|
|`c--`|값 2를 사용한 뒤 `c`는 1|2|
|`b-- & c--`|`2 & 2 = 2`|2|
|`++a | ...`|`3 | 2 = 3`|3|

비트로 보면 `3`은 `011`, `2`는 `010`이므로 `011 | 010 = 011`, 즉 3이다. 최종적으로 `hap = 3`, `a = 3`, `b = 1`, `c = 1`이다.

---

## 문제 32 — 문자열의 `==`와 `equals()`

```java
public class Main {
    public static void main(String[] args) {
        String str1 = "Programming";
        String str2 = "Programming";
        String str3 = new String("Programming");

        System.out.println(str1 == str2);
        System.out.println(str1 == str3);
        System.out.println(str1.equals(str3));
        System.out.println(str2.equals(str3));
    }
}
```

정답

```text
true
false
true
true
```

풀이

`==`는 두 참조가 같은 객체를 가리키는지 비교한다. `equals()`는 문자열 내용을 비교한다.

|식|결과|이유|
|---|---|---|
|`str1 == str2`|`true`|문자열 리터럴은 문자열 풀에 저장되어 같은 객체를 공유한다.|
|`str1 == str3`|`false`|`new String(...)`은 새 객체를 만든다.|
|`str1.equals(str3)`|`true`|내용 `"Programming"`이 같다.|
|`str2.equals(str3)`|`true`|내용 `"Programming"`이 같다.|

시험에서는 `String` 비교가 나오면 거의 항상 `==`는 주소, `equals()`는 내용이라고 먼저 분리해서 보면 된다.

---

## 문제 36 — enum의 `values()`, `name()`, 배열 인덱스

```java
enum Tri {
    A("A"), B("AB"), C("ABC");

    private String code;

    Tri(String code) {
        this.code = code;
    }

    String code() {
        return code;
    }
}

public class Main {
    public static void main(String[] args) {
        Tri t = Tri.values()[Tri.A.name().length()];
        System.out.print(t.code());
    }
}
```

정답

```text
AB
```

풀이

`Tri.values()`는 enum 상수를 선언 순서대로 담은 배열을 반환한다.

|식|값|
|---|---|
|`Tri.values()`|`[Tri.A, Tri.B, Tri.C]`|
|`Tri.A.name()`|`"A"`|
|`Tri.A.name().length()`|1|
|`Tri.values()[1]`|`Tri.B`|
|`Tri.B.code()`|`"AB"`|

배열 인덱스는 0부터 시작하므로 `[1]`은 두 번째 상수 `B`다. 그래서 출력은 `AB`다.

---

## 문제 40 — 제네릭과 오버로딩 선택 시점

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
        new Collection<>(0).print();
    }

    static class Collection<T> {
        T value;

        Collection(T t) {
            value = t;
        }

        void print() {
            new Printer().print(value);
        }
    }
}
```

정답

```text
B0
```

풀이

겉으로는 `new Collection<>(0)`이므로 `T`가 `Integer`처럼 보인다. 하지만 `Collection<T>` 클래스 안의 `value`는 컴파일 시점에 타입 변수 `T`이고, `T`에는 별도 상한이 없으므로 기본 상한은 `Object`다.

오버로딩은 런타임 객체 타입이 아니라 컴파일 시점의 참조 타입으로 고른다.

|후보 메서드|`value`의 컴파일 시점 타입 `T`로 호출 가능 여부|
|---|---|
|`print(Integer a)`|항상 `Integer`라고 보장할 수 없어 선택 안 됨|
|`print(Number a)`|항상 `Number`라고 보장할 수 없어 선택 안 됨|
|`print(Object a)`|모든 `T`는 `Object`이므로 선택됨|

따라서 `print(Object a)`가 실행되어 `B0`이 출력된다.

---

## 시험 대비 Java 문법·주의사항

### 1. 연산자 우선순위: `&`, `^`, `|`, `&&`, `||`, `?:`

문제 풀이용으로는 다음 흐름을 먼저 외우면 충분하다.

```text
괄호
증감 ++ --
단항 ! ~ + -
산술 * / %  →  + -
시프트 << >> >>>
관계 < <= > >=  →  동등 == !=
비트 AND &
비트 XOR ^
비트 OR |
논리 AND &&
논리 OR ||
삼항 ?:
대입 = += -= ...
```

핵심 비교:

|연산자|특징|
|---|---|
|`&`|정수에서는 비트 AND, boolean에서는 논리 AND. 단락 평가 없음|
|`^`|정수에서는 비트 XOR, boolean에서는 둘이 다르면 `true`|
|`&#124;`|정수에서는 비트 OR, boolean에서는 논리 OR. 단락 평가 없음|
|`&&`|왼쪽이 `false`이면 오른쪽을 평가하지 않음|
|`&#124;&#124;`|왼쪽이 `true`이면 오른쪽을 평가하지 않음|
|`?:`|조건식 뒤 마지막 쪽에서 갈라지는 삼항 연산자|

표에서 `|`는 Markdown 표 기호와 겹치지만, 실제 Java 연산자는 세로 막대 하나다.

### 2. `==`와 `equals()`

|비교|의미|대표 예|
|---|---|---|
|`a == b`|기본형은 값 비교, 참조형은 같은 객체인지 비교|`str1 == str2`|
|`a.equals(b)`|객체가 정의한 내용 비교|`str1.equals(str3)`|

`String` 리터럴끼리는 문자열 풀 때문에 `==`가 `true`가 될 수 있다. 하지만 시험에서 문자열 내용 비교를 묻는다면 보통 `equals()`가 정답 포인트다.

### 3. enum 기본 메서드

|메서드|예시|결과|
|---|---|---|
|`values()`|`Tri.values()`|선언 순서대로 enum 배열 반환|
|`valueOf(String)`|`Tri.valueOf("A")`|이름이 `"A"`인 enum 상수 반환|
|`name()`|`Tri.A.name()`|선언된 이름 `"A"` 반환|
|`ordinal()`|`Tri.A.ordinal()`|선언 순서 인덱스. 첫 번째는 0|
|`compareTo()`|`Tri.A.compareTo(Tri.C)`|ordinal 차이를 기준으로 비교|
|`toString()`|`Tri.A.toString()`|기본은 `name()`과 같지만 오버라이딩 가능|

`values()`와 `valueOf(String)`은 컴파일러가 enum에 자동으로 만들어 주는 정적 메서드다. `name()`과 `ordinal()`은 `java.lang.Enum`의 메서드이며 오버라이딩할 수 없다.

### 4. 상속 문제에서 먼저 볼 것

- 생성자는 부모 → 자식 순서로 실행된다.
- 인스턴스 메서드는 실제 객체 기준으로 오버라이딩된다.
- `static` 메서드는 오버라이딩이 아니라 숨김이며, 참조 변수의 선언 타입 기준으로 선택된다.
- 메서드 이름이 같아도 매개변수가 다르면 오버로딩이다.
- 부모 타입 변수로 자식 객체를 가리키면, 호출 가능한 메서드 목록은 일단 부모 타입 기준으로 결정된다.

### 5. 제네릭과 오버로딩

제네릭 타입 변수 `T`는 상한이 없으면 컴파일 시점에 `Object`처럼 취급된다.

```java
class Box<T> {
    T value;
}
```

`T extends Number`처럼 상한을 주면 `T`는 최소한 `Number`로 볼 수 있다. 하지만 상한이 없는 `T`는 `Integer`, `Number` 전용 오버로드로 바로 들어가지 않고 `Object` 쪽이 선택될 수 있다.

### 6. 출력 문제 체크리스트

- `System.out.print`는 줄바꿈이 없고, `println`은 줄바꿈이 있다.
- `+`에서 한쪽이 문자열이면 이후는 문자열 연결이다.
- 배열 인덱스는 0부터 시작한다.
- 예외는 가장 구체적인 `catch`부터 검사한다.
- `finally`는 예외 처리 여부와 관계없이 실행된다.
- 람다식은 함수형 인터페이스, 즉 추상 메서드가 하나인 인터페이스에 대입된다.
