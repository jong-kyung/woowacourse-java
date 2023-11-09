# 우아한테크코스 주차별 공통 피드백
## 1주차 피드백
1. 요구사항을 정확히 준수한다  
	> 과제 제출 전에 기능 요구 사항, 프로그래밍 요구 사항, 과제 진행 요구 사항의 항목을 모두 잘 지켰는지 다시 한 번 점검한다. 

2. 커밋 메시지를 의미 있게 작성한다
	> 커밋 메시지에 해당 커밋에서 작업한 내용에 대한 이해가 가능하도록 작성한다.

3. git을 통해 관리할 자원에 대해서도 고려한다
	> .class 파일은 java 코드가 있으면 생성할 수 있다. 따라서 .class 파일은 굳이 git을 통해 관리하지 않아도 된다.
	IntelliJ IDEA의 .idea  폴더, Eclipse의 .metadata 폴더 또한 개발 도구가 자동으로 생성하는 폴더이기 때문에 굳이 git으로 관리하지 않아도 된다.
	앞으로 git에 코드를 추가할 때는 git을 통해 관리할 필요가 있는지를 고려해볼 것을 추천한다.

4. Pull Request를 보내기 전 브랜치를 확인한다
	> 기능 구현 작업을 fork된 Repository의 main branch가 아닌, 기능 구현을 위해 새로 만든 브랜치에서 작업한 후 PR을 보낸다. 

5. PR을 한 번 작성했다면 닫지 말고 추가 커밋을 한다
	> PR을 이미 한 번 보냈다면, 새로운 PR을 생성할 필요가 없다. 수정이 필요하다면 추가 커밋을 하면 자동으로 반영된다. 단, 미션 제출 기간 이후에는 추가 커밋을 하지 않는다.
	이름을 통해 의도를 드러낸다
	나 자신, 다른 개발자와의 소통을 위해 가장 중요한 활동 중의 하나가 좋은 이름 짓기이다. 변수 이름, 함수(메서드) 이름, 클래스 이름을 짓는데 시간을 투자하라. 이름을 통해 변수의 역할, 함수의 역할, 클래스의 역할에 대한 의도를 드러내기 위해 노력하라. 연속된 숫자를 덧붙이거나(a1, a2, ..., aN), 불용어(Info, Data, a, an, the)를 추가하는 방식은 적절하지 못하다.

6. 축약하지 않는다
	> 의도를 드러낼 수 있다면 이름이 길어져도 괜찮다.
		>> 누구나 실은 클래스, 메서드, 또는 변수의 이름을 줄이려는 유혹에 곧잘 빠지곤 한다. 그런 유혹을 뿌리쳐라. 축약은 혼란을 야기하며, 더 큰 문제를 숨기는 경향이 있다. 클래스와 메서드 이름을 한 두 단어로 유지하려고 노력하고 문맥을 중복하는 이름을 자제하자. 클래스 이름이 Order라면 shipOrder라고 메서드 이름을 지을 필요가 없다. 짧게 ship()이라고 하면 클라이언트에서는 order.ship()라고 호출하며, 간결한 호출의 표현이 된다.  
		객체 지향 생활 체조 원칙 5: 줄여쓰지 않는다 (축약 금지)

7. 공백도 코딩 컨벤션이다
	> if, for, while문 사이의 공백도 코딩 컨벤션이다.

8. 공백 라인을 의미 있게 사용한다
	> 공백 라인을 의미 있게 사용하는 것이 좋아 보이며, 문맥을 분리하는 부분에 사용하는 것이 좋다. 과도한 공백은 다른 개발자에게 의문을 줄 수 있다.

9. space와 tab을 혼용하지 않는다
	> 들여쓰기에 space와 tab을 혼용하지 않는다. 둘 중에 하나만 사용한다. 확신이 서지 않으면 pull request를 보낸 후 들여쓰기가 잘 되어 있는지 확인하는 습관을 들인다.

10. 의미 없는 주석을 달지 않는다
	> 변수 이름, 함수(메서드) 이름을 통해 어떤 의도인지가 드러난다면 굳이 주석을 달지 않는다. 모든 변수와 함수에 주석을 달기보다 가능하면 이름을 통해 의도를 드러내고, 의도를 드러내기 힘든 경우 주석을 다는 연습을 한다.

11. IDE의 코드 자동 정렬 기능을 활용한다
    > IDE의 코드 자동 정렬 기능을 사용하면 더 깔끔한 코드를 볼 수 있다.
    - IntelliJ IDEA: ⌥⌘L, Ctrl+Alt+
    - Eclipse: ⇧⌘F, Ctrl+Shift+F

12. Java에서 제공하는 API를 적극 활용한다
	> 함수(메서드)를 직접 구현하기 전에 Java API에서 제공하는 기능인지 검색을 먼저 해본다.
	Java API에서 제공하지 않을 경우 직접 구현한다.
	예를 들어 사용자를 출력할 때 사용자가 2명 이상이면 쉼표(,) 기준으로 출력을 위한 문자열은 다음과 같이 구현 가능하다.

	``` java
	List<String> members = Arrays.asList("pobi", "jason");
	String result = String.join(",", members); // "pobi,jason"
	```

13. 배열 대신 Java Collection을 사용한다
	> Java Collection 자료구조(List, Set, Map 등)를 사용하면 데이터를 조작할 때 다양한 API를 사용할 수 있다.  
	예를 들어 List<String>에 "pobi"라는 값이 포함되어 있는지는 다음과 같이 확인할 수 있다.

	``` java
	List<String> members = Arrays.asList("pobi", "jason");
	boolean result = members.contains("pobi"); // true
	```

### 참고자료
[git- 간편안내서](https://rogerdudler.github.io/git-guide/index.ko.html)

## 2주차 피드백
1. README.md를 상세히 작성한다
	> 미션 저장소의 README.md는 소스코드에 앞서 해당 프로젝트가 어떠한 프로젝트인지 마크다운으로 작성하여 소개하는 문서이다. 해당 프로젝트가 어떠한 프로젝트이며, 어떤 기능을 담고 있는지 기술하기 위해서 마크다운 문법을 검색해서 학습해 보고 적용해 본다.

2. 기능 목록을 재검토한다
	> 기능 목록을 클래스 설계와 구현, 함수(메서드) 설계와 구현과 같이 너무 상세하게 작성하지 않는다. 클래스 이름, 함수(메서드) 시그니처와 반환값은 언제든지 변경될 수 있기 때문이다. 너무 세세한 부분까지 정리하기보다 구현해야 할 기능 목록을 정리하는 데 집중한다. 정상적인 경우도 중요하지만, 예외적인 상황도 기능 목록에 정리한다. 특히 예외 상황은 시작 단계에서 모두 찾기 힘들기 때문에 기능을 구현하면서 계속해서 추가해 나간다.

3. 기능 목록을 업데이트한다
	> README.md 파일에 작성하는 기능 목록은 기능 구현을 하면서 변경될 수 있다. 시작할 때 모든 기능 목록을 완벽하게 정리해야 한다는 부담을 가지기보다 기능을 구현하면서 문서를 계속 업데이트한다. 죽은 문서가 아니라 살아있는 문서를 만들기 위해 노력한다.

4. 값을 하드 코딩하지 않는다
	> 문자열, 숫자 등의 값을 하드 코딩하지 마라. 상수(static final)를 만들고 이름을 부여해 이 변수의 역할이 무엇인지 의도를 드러내라. 구글에서 "java 상수"와 같은 키워드로 검색해 상수 구현 방법을 학습하고 적용해 본다.

5. 구현 순서도 코딩 컨벤션이다
	> 클래스는 상수, 멤버 변수, 생성자, 메서드 순으로 작성한다.
	
	``` java
	class A {
		상수(static final) 또는 클래스 변수

		인스턴스 변수

		생성자

		메서드
	}
	```

6. 변수 이름에 자료형은 사용하지 않는다
	> 변수 이름에 자료형, 자료 구조 등을 사용하지 마라.
	
	``` java
	String carNameList = Console.readLine();
	String[] arrayString = carNameList.split(",");
	```

7. 한 함수가 한 가지 기능만 담당하게 한다
	> 함수 길이가 길어진다면 한 함수에서 여러 일을 하려고 하는 경우일 가능성이 높다. 아래와 같이 한 함수에서 안내 문구 출력, 사용자 입력, 유효값 검증 등 여러 일을 하고 있다면 이를 적절하게 분리한다.

	``` java
	public List<String> userInput() {
		System.out.println("경주할 자동차 이름을 입력하세요(이름은 쉼표(,)를 기준으로 구분).");
		String userInput = Console.readLine().trim();
		String[] splittedName = userInput.split(",");
		for (int index = 0; index < splittedName.length; index++) {
			if (splittedName.length < 1 || splittedName.length > 5) {
				throw new IllegalArgumentException("[ERROR] 자동차 이름은 1자 이상 5자 이하만 가능합니다.");
			}
		}
		return Arrays.asList(splittedName);
	}
	```

8. 함수가 한 가지 기능을 하는지 확인하는 기준을 세운다
	> 만약 여러 함수에서 중복되어 사용되는 코드가 있다면 함수 분리를 고민해 본다. 또한, 함수의 길이를 15라인을 넘어가지 않도록 구현하며 함수를 분리하는 의식적인 연습을 할 수 있다.

9. 테스트를 작성하는 이유에 대해 본인의 경험을 토대로 정리해본다
	> 단지 기능을 점검하기 위한 목적으로 테스트를 작성하는 것은 아니다. 테스트를 작성하는 과정을 통해서 나의 코드에 대해 빠르게 피드백을 받을 수 있을 뿐만 아니라 학습 도구(학습테스트를 통해 JUnit 학습하기.pdf)로도 활용할 수 있다. 이런 경험을 통해 테스트에 대해 어떤 유용함을 느꼈는지 알아본다.

10. 처음부터 큰 단위의 테스트를 만들지 않는다
	> 테스트의 중요한 목적 중 하나는 내가 작성하는 코드에 대해 빠르게 피드백을 받는 것이다. 시작부터 큰 단위의 테스트를 만들게 된다면 작성한 코드에 대한 피드백을 받기까지 많은 시간이 걸린다. 그래서 문제를 작게 나누고, 그 중 핵심 기능에 가까운 부분부터 작게 테스트를 만들어 나간다.
	- 큰 단위의 테스트
    	- 자동차경주를 시작해서 사용자가 이름, 진행 횟수를 입력하면, 게임을 진행한 후 그 결과를 알려준다.

	- 작은 단위의 테스트
    	- 무작위 값이 4 이상이면 자동차가 전진한다.
    	- 무작위 값이 3 이하이면 자동차가 전진하지 않는다.

## 3주차 피드백
1. 함수(메서드) 라인에 대한 기준
	> 프로그래밍 요구사항을 보면 함수 15라인으로 제한하는 요구사항이 있다. 이 기준은 main() 함수에도 해당된다. 공백 라인도 한 라인에 해당한다. 15라인이 넘어간다면 함수 분리를 위한 고민을 한다

2. 발생할 수 있는 예외 상황에 대해 고민한다
	> 정상적인 경우를 구현하는 것보다 예외 상황을 모두 고려해 프로그래밍하는 것이 더 어렵다. 예외 상황을 고려해 프로그래밍하는 습관을 들인다. 예를 들어 로또 미션의 경우 아래와 같은 예외 상황을 고민해 보고 해당 예외에 대해 처리를 할 수 있어야 한다.

	- 로또 구입 금액에 1000 이하의 숫자를 입력
	- 당첨 번호에 중복된 숫자를 입력
	- 당첨 번호에 1~45 범위를 벗어나는 숫자를 입력
	- 당첨 번호와 중복된 보너스 번호를 입력

3. 비즈니스 로직과 UI 로직을 분리한다
	> 비즈니스 로직과 UI 로직을 한 클래스가 담당하지 않도록 한다. 단일 책임의 원칙에도 위배된다.

	``` java
	public class Lotto {
		private List<Integer> numbers;

		// 로또 숫자가 포함되어 있는지 확인하는 비즈니스 로직
		public boolean contains(int number) {
			...
		}

		// UI 로직
		private void print() {
			...
		}
	}
	```
	> 현재 객체의 상태를 보기 위한 로그 메시지 성격이 강하다면 toString()을 통해 구현한다. View에서 사용할 데이터라면 getter 메서드를 통해 데이터를 전달한다.

4. 연관성이 있는 상수는 static final 대신 enum을 활용한다

	``` java
	public enum Rank {
		FIRST(6, 2_000_000_000),
		SECOND(5, 30_000_000),
		THIRD(5, 1_500_000),
		FOURTH(4, 50_000),
		FIFTH(3, 5_000),
		MISS(0, 0);

		private int countOfMatch;
		private int winningMoney;

		private Rank(int countOfMatch, int winningMoney) {
			this.countOfMatch = countOfMatch;
			this.winningMoney = winningMoney;
		}
	}
	```

5. final 키워드를 사용해 값의 변경을 막는다
	> 최근에 등장하는 프로그래밍 언어들은 기본이 불변 값이다. 자바는 final 키워드를 활용해 값의 변경을 막을 수 있다.	

	``` java
	class A {
		상수(static final) 또는 클래스 변수

		인스턴스 변수

		생성자

		메서드
	}
	```

6. 객체의 상태 접근을 제한한다
	> 인스턴스 변수의 접근 제어자는 private으로 구현한다.
	
	``` java
	public class WinningLotto {
		private Lotto lotto;
		private Integer bonusNumber;

		public WinningLotto(Lotto lotto, Integer bonusNumber) {
			this.lotto = lotto;
			this.bonusNumber = bonusNumber;
		}
	}
	```

7. 객체는 객체스럽게 사용한다
	> Lotto 클래스는 numbers를 상태 값으로 가지는 객체이다. 그런데 이 객체는 로직에 대한 구현은 하나도 없고, numbers에 대한 getter 메서드만을 가진다.

	``` java
	public class Lotto {
		private final List<Integer> numbers;
		
		public Lotto(List<Integer> numbers) {
			this.numbers = numbers;
		}

		public int getNumbers() {
			return numbers;
		}
	}

	public class LottoGame {
		public void play() {
			Lotto lotto = new Lotto(...);

			// 숫자가 포함되어 있는지 확인한다.
			lotto.getNumbers().contains(number);
			
			// 당첨 번호와 몇 개가 일치하는지 확인한다.
			lotto.getNumbers().stream()...
		}
	}
	```

	> Lotto에서 데이터를 꺼내지(get) 말고 메시지를 던지도록 구조를 바꿔 데이터를 가지는 객체가 일하도록 한다.

	``` java
	public class Lotto {
		private final List<Integer> numbers;

		public boolean contains(int number) {
			// 숫자가 포함되어 있는지 확인한다.
			...
		}
		
		public int matchCount(Lotto other) {
			// 당첨 번호와 몇 개가 일치하는지 확인한다.
			...
		}
	}

	public class LottoGame {
		public void play() {
			Lotto lotto = new Lotto(...);
			lotto.contains(number);
			lotto.matchCount(...); 
		}
	}
	```

	[참고](https://tecoble.techcourse.co.kr/post/2020-04-28-ask-instead-of-getter/)

8. 필드(인스턴스 변수)의 수를 줄이기 위해 노력한다
	> 필드(인스턴스 변수)의 수가 많은 것은 객체의 복잡도를 높이고, 버그 발생 가능성을 높일 수 있다. 필드에 중복이 있거나, 불필요한 필드가 없는지 확인해 필드의 수를 최소화한다.
	예를 들어 총상금 및 수익률을 구하는 다음 객체를 보자.

	``` java
	public class LottoResult {
		private Map<Rank, Integer> result = new HashMap<>();
		private double profitRate;
		private int totalPrize;
	}
	```
	> 위 객체의 profitRate와 totalPrize는 등수 별 당첨 내역(result)만 있어도 모두 구할 수 있는 값이다. 따라서 위 객체는 다음과 같이 하나의 필드만으로 구현할 수 있다

	``` java
	public class LottoResult {
		private Map<Rank, Integer> result = new HashMap<>();

		public double calculateProfitRate() { ... }
		
		public int calculateTotalPrize() { ... }
	}
	```


9.  성공하는 케이스 뿐만 아니라 예외에 대한 케이스도 테스트한다
	> 테스트를 작성하면 성공하는 케이스에 대해서만 고민하는 경우가 있다. 하지만 예외에 대한 부분 또한 처리해야 한다. 특히 프로그램에서 결함이 자주 발생하는 부분 중 하나는 경계값이므로 이 부분을 꼼꼼하게 확인해야 한다.

	``` java
	@DisplayName("보너스 번호가 당첨 번호와 중복되는 경우에 대한 예외 처리")
	@Test
	void duplicateBonus() {
		assertThatThrownBy(() ->
				new WinningLotto(new Lotto(List.of(1, 2, 3, 4, 5, 6), 6))
		).isInstanceOf(IllegalArgumentException.class);
	}
	```

10. 테스트 코드도 코드다
	> 테스트 코드도 코드이므로 리팩터링을 통해 개선해 나가야 한다. 특히 반복적으로 하는 부분을 중복되지 않게 만들어야 한다. 예를 들어 단순히 파라미터의 값만 바뀌는 경우라면 아래와 같이 테스트할 수 있다.

	``` java
	@DisplayName("천원 미만의 금액에 대한 예외 처리")
	@ValueSource(strings = {"999", "0", "-123"})
	@ParameterizedTest
	void underLottoPrice(Integer input) {
		assertThatThrownBy(() -> new Money(input))
				.isInstanceOf(IllegalArgumentException.class);
	}
	```

11. 테스트를 위한 코드는 구현 코드에서 분리되어야 한다
	> 테스트를 위한 편의 메서드를 구현 코드에 구현하지 마라. 아래의 예시처럼 테스트를 통과하기 위해 구현 코드를 변경하거나 테스트에서만 사용되는 로직을 만들지 않는다.
	
	- 테스트를 위해 접근 제어자를 바꾸는 경우
    - 테스트 코드에서만 사용되는 메서드

12. 단위 테스트하기 어려운 코드를 단위 테스트하기
	> 아래 코드는 Random 때문에 Lotto에 대한 단위 테스트를 하기 힘들다. 단위 테스트가 가능하도록 리팩터링한다면 어떻게 하는 것이 좋을까?

	``` java
	import camp.nextstep.edu.missionutils.Randoms;

	public class Lotto {
		private List<Integer> numbers;

		public Lotto() {
			this.numbers = Randoms.pickUniqueNumbersInRange(1, 45, 6);
		}
	}

	——————

	public class LottoMachine {
		public void execute() {
			Lotto lotto = new Lotto();
		}
	}
	```
	
	> 올바른 로또 번호가 생성되는 것을 테스트하기 어렵다. 테스트하기 어려운 것을 클래스 내부가 아닌 외부로 분리하는 시도를 해 본다.

	``` java
	public class Lotto {
		private List<Integer> numbers;

		public Lotto(List<Integer> numbers) {
			this.numbers = numbers;
		}
	}

	——————

	import camp.nextstep.edu.missionutils.Randoms;

	public class LottoMachine {
		public void execute() {
			List<Integer> numbers = Randoms
				.pickUniqueNumbersInRange(1, 45, 6);
			Lotto lotto = new Lotto(numbers);
		}
	}
	```
	> 위 코드는 A 상황을 B로 바꾼 것이다. 

	```
	A.

	Application(테스트하기 어려움)
		⬇️
	LottoMachine(테스트하기 어려움)
		⬇️
	Lotto(테스트하기 어려움) ➡️ Randoms(테스트하기 어려움)
	```

	``` java
	B.
 
	Application(테스트하기 어려움) 
		⬇️
	LottoMachine(테스트하기 어려움) ➡️ Randoms(테스트하기 어려움) 
		⬇️
	Lotto(테스트하기 쉬움)
	```
	[참고](https://tecoble.techcourse.co.kr/post/2020-05-07-appropriate_method_for_test_by_parameter/)

	> 이처럼 단위 테스트를 할 때 테스트하기 어려운 부분은 분리하고 테스트 가능한 부분을 단위 테스트한다. 테스트하기 어려운 부분은 단위 테스트하지 않아도 된다. 남은 LottoMachine은 어떻게 테스트하기 쉽게 바꿀 수 있을지 고민해 본다.

13. private 함수를 테스트 하고 싶다면 클래스(객체) 분리를 고려한다
	> 가독성의 이유만으로 분리한 private 함수의 경우 public으로도 검증 가능하다고 여겨질 수 있다. public 함수가 private 함수를 사용하고 있기 때문에 자연스럽게 테스트 범위에 포함된다. 하지만 가독성 이상의 역할을 하는 경우, 테스트하기 쉽게 구현하기 위해서는 해당 역할을 수행하는 다른 객체를 만들 타이밍이 아닐지 고민해 볼 수 있다. 다음 단계를 진행할 때에는 너무 많은 역할을 하고 있는 함수나 객체를 어떻게 의미 있는 단위로 분할할지에 초점을 맞춰 진행한다.