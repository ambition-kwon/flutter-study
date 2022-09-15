# ✍️Flutter Grammer

- type inference(추론)(최근에 나온 언어들) : var타입

```dart
void main(List<String> args) {
  var value1 = 18;
  var name1 = "khw";

  int value2 = 18;
  String name2 = "khw";

  dynamic value3 = 18; //evaluated at runtime(진짜 필요할 때만 써야함)
  dynamic name3 = "khw"; //실행을 하고 나서야 알 수 있다.
//dynamic은 엄밀하게 말해 type이 아니다.
  print(name1 + name2 + name3);
  print(value1);
  print(value2);
  print(value3);
}
```

- late : 나중에 결정 하겠다.
- final : 값을 한번 정하면 다시는 바꾸지 않겠다는 뜻(값 바꾸려고 하면 error)

```dart
final name = "khw";
final String name = "khw"; //이럴 필요는 없다.
//왜냐면 초기화 동시에 무조건 컴파일러가 checking하기 때문이다. 즉 final도 var처럼 취급한다.
```

- int(64bit), double(64bit) ← number관련 타입은 이거 두 개 밖에 없다.

> C언어 int는 32bit이다.
> 

```dart
var a = 1; //int
var a = 1.0; //double
const value = 7; //컴파일 할때 값을 정해서 고정
final value = 7; //실행할 때 값을 정해서 고정(web에서 뭐 불러올 때)
var a = 1.35e2; //10의 2승
var a = 0xF1A; //16진수
```

```dart
var s = "khw";
var a = 'khw'; //둘다 상관 없다.
var age = 25;
var myAge = "I am **$age** years old"; //$의 사용법

// 표현식은 필요하다(단순 변수 아니고 processing 할때) '{' and '}' proceeded by $
var test =
"${25.abs()}“
// This is 중복된다, don't do it because ${} already calls toString()
// toString()자체가 String으로 변환하는 것이기 때문에 ${}은 필요치 않다.

var redundant ="${25.toString()}";

var test = """
안녕하세요!
"""; //multiline String

var test = "khw";
print(test[0]); //slicing

var name = "khw";
var s = 'I am ' + name + ' and I am ' + (23).toString() + ' years old';

var value = "dddd" "qqqq" "ffff";
var value = "dddd" + "qqqq" + "ffff"; //두개는 같은 것. 굳이 밑에처럼 안해도 된다.

var buffer = StringBuffer();
for(var i = 0; i < 900000; ++i) buffer.write("$i ");
// StringBuffer doesn’t internally create a new string
var value = buffer.toString();

```

```dart
void main(List<String> args) {
  var value = "";
  for (var i = 0; i < 10; i++) {
    value += i.toString();
  }
  print(value);

  value = "";
  for (var i = 0; i < 10; i++) {
    value += "$i";
  }
  print(value);
	//아래 방법이 제일 빠르다.
	var buffer = StringBuffer();
	for(var i = 0; i < 900000; ++i) buffer.write("$i ");
	// StringBuffer doesn’t internally create a new string
	var value = buffer.toString();
}
```
