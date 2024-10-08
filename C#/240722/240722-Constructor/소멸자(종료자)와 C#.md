## 소멸자(종료자)와 C#

- 소멸자란?

C#의 객체는 생성자와 소멸자를 가질 수 있다. 생성자는 객체가 생성되는 시점에, 소멸자는 소멸되는 시점에 호출된다. 이때 주의할 점은 생성자는 사용자가 원할 때 객체가 생성되기 때문에 시점을 예상 가능하지만, 소멸자는 그렇지 않다는 것이다.

- C++과 C# 소멸자의 비교

C++의 메모리는 프로그래머가 크게 관여하기 때문에 이를 위해 객체의 소멸 시점도 명확하다.

반면, C#은 메모리를 CLR의 가비지 컬렉터가 관리하기 때문에, 객체의 소멸 시점을 프로그래머가 정확하게 알 수 없다.

- C#에서 소멸자의 호출

즉, 소멸 타이밍을 프로그래머가 정확하게 알 수 없는 C#에서는 

```csharp
class Car
{
    ~Car()  // 종료자
    {
            // cleanup statements...
    }
}
```

처럼 Car 클래스를 종료자로 선언하면, Finalize를 암시적으로 호출한다.

Finalize는 기본 클래스의 Finalize를 호출하는 재귀 형태로 이루어져 있다. 이러한 작업을 위해 가비지 컬렉터는 해당 객체를 즉시 메모리에서 해제하지 않고 다른 작업 큐에 넣어 두었다가 처리가 모두 마무리 된 후 메모리에서 해제한다.

즉, 쓸데 없이 메모리에 자리를 차지하는 시간이 길어지므로 반드시 필요한 작업이 있는것이 아니라면 소멸자를 선언하지 않는 것이 성능적으로 유리해진다.