## 자바의 코드구조
```java
/* 클래스 블록 */
public class 클래스명 {

    /* 메서드 블록 */
    [public|private|protected] [static] (리턴자료형|void) 메서드명1(입력자료형 매개변수, ...) {
        명령문(statement);
        ...
    }

    /* 메서드 블록 */
    [public|private|protected] [static] (리턴자료형|void) 메서드명2(입력자료형 매개변수, ...) {
        명령문(statement);
        ...
    }

    ...
}
```
[public|private|protected]는 public, private, protected가 오거나 아무것도 오지 않을 수 있다는 의미이다. public, private, protected는 메서드의 접근 제어자이다.

[static]은 static 키워드가 올 수도 있고 오지 않을 수도 있다는 의미이다. static이라는 키워드가 붙으면 static 메서드가 된다.

(리턴 자료형|void)는 메서드가 실행된 후 리턴되는 값의 자료형을 의미한다. 리턴값이 있을 경우에는 반드시 리턴 자료형을 표기해야 하며, 만약 리턴값이 없는 경우라면 void로 표기해야 한다. 이 항목은 void 또는 리턴 자료형이 반드시 있어야만 한다(그래서 [] 대신 ()로 표시했다.).

## 변수
### 화면에 글자 출력
``` java 
System.out.print("hello, world") // 화면에 글자 출력
System.out.printIn() // 괄호 안의 내용을 출력하고 줄바꿈도 해줌
```

### 변수 할당
기본적으로 변수 선언은 아래와 같다  
변수타입 변수이름;
``` java
int x; // 정수(integer)를 저장하기 위한 변수 선언
```

### 변수의 자료형
- 숫자
    ``` java
    // 정수를 저장하기 위한 타입
    int 
    long // 20억이 넘는 정수일때 사용
    // 실수를 저장하기위한 타입
    float // 오차없이 7자리
    double // 15자리
    ```
- 문자
    ``` java
    char // 문자(character)를 저장하기 위한 타입
    String // 여러 문자를 저장하기 위한 타입
    ```
- 예시
    ``` java
    int x = 100; // 정수 저장
    double pi = 3.14; // 실수 저장
    char ch = 'a'; // 문자(1개)
    String str = "abc"; //여러 문자(0~n개)
    ```

### 상수
상수는 변수와 마찬가지로 '값을 저장할 수 있는 공간'이지만, 변수와 달리 값을 한번 값을 저장하면 **다른 값으로 변경할 수 없다**
``` java
final int MAX_VALUE;
MAX_VALUE = 100; // 상수에 초기 값 저장
MAX_VALUE = 200; // ERROR 저장된 값 변경 불가
```

## 접근제어자
### public
public 접근 제어자가 붙은 변수나 메서드는 어떤 클래스에서도 접근이 가능하다.
``` java
package house;

public class HousePark {
    protected String lastname = "park";
    public String info = "this is public message.";
}
```

``` java
import house.HousePark;

public class Sample {
    public static void main(String[] args) {
        HousePark housePark = new HousePark(); 
        System.out.println(housePark.info); // 위에서 public 접근제어자를 사용하였기에 다른 클래스에서도 접근이 가능함.
    }
}
```

### private
접근 제어자가 private으로 설정되었다면 private이 붙은 변수나 메서드는 해당 클래스 안에서만 접근이 가능하다.
``` java
public class Sample {
    private String secret; // private로 접근제어자를 사용하였기에 Sample 내에서만 사용가능
    private String getSecret() {
        return this.secret;
    }
}
```

### protected
접근 제어자가 protected로 설정되었다면 protected가 붙은 변수나 메서드는 동일 패키지의 클래스 또는 해당 클래스를 상속받은 클래스에서만 접근이 가능하다.
``` java
package house;  // 패키지가 서로 다르다.

public class HousePark {
    protected String lastname = "park";
}
```

``` java
package house.person;  // 패키지가 서로 다르다.

import house.HousePark;

public class EungYongPark extends HousePark {  // HousePark을 상속했다.
    public static void main(String[] args) {
        EungYongPark eyp = new EungYongPark();
        System.out.println(eyp.lastname);  // 상속한 클래스의 protected 변수는 접근이 가능하다.
    }
}
```

### default
접근 제어자를 별도로 설정하지 않는다면 변수나 메서드는 default 접근 제어자가 자동으로 설정되어 동일한 패키지 안에서만 접근이 가능하다.
``` java
package house;  // 패키지가 동일하다.

public class HouseKim {
    String lastname = "kim";  // lastname은 default 접근제어자로 설정된다.
}
```

``` java
package house;  // 패키지가 동일하다.

public class HousePark {
    String lastname = "park";

    public static void main(String[] args) {
        HouseKim kim = new HouseKim();
        System.out.println(kim.lastname);  // HouseKim 클래스의 lastname 변수를 사용할 수 있다.
    }
}
```

## import
``` java
// import 패키지명.클래스명;
import java.utils.Date; 
// static import 패키지명
import static java.lang.Math.random; // Math.random()만 해당.
// static 멤버를 사용할때 클래스명을 생략할 수 있음
```
