# act.05

## 01 상속의 정의

`상속`의 사전적 의미

1. 뒤를 잇다.

2. 죽은 사람의 권리와 의무를 이어 받는 일

일반적으로는 부모가 자식에게 재산, 권리, 의무 등을 물려주는 것을 상속이라고 한다.

프로그래밍에서의 상속 또한 비슷한 역할을 한다.

물론 일반적인 재산, 권리, 의무를 물려주는 것이 아니라 "`클래스의 멤버를 물려준다.`"는 차이점이 있다.

이 때 물려주는 클래스를 "부모 클래스", 물려받는 클래스를 "자식 클래스"라고 얘기한다.


```Javascript
public class Main {

	public static void main(String[] args) {
		Parent p = new Parent();
		Child c = new Child();
		
		p.print();
		c.print();
	}

}

// Parent 클래스 정의
class Parent {
		
	public int iInt;
	
	public void print() {
		System.out.println("Parent Class");
	}
}

// Child 클래스 정의
class Child extends Parent{

}
```

- 자식 클래스는 부모 클래스로부터 물려받은 멤버 외에 `다른 멤버를 추가로 가질 수 있습니다.`

- 자식 클래스에서 정의된 멤버는 부모클래스 객체에서는 사용할 수 없습니다.

- 자식 클래스는 객체가 생성될 때는 부모클래스의 생성자가 무조건 실행됩니다.

	실행 되는 순서는
	
	1) 부모클래스 생성자
	
	2) 자식클래스 생성자
	
	순입니다.
