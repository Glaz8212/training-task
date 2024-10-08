## C# 제네릭과 C++ 템플릿

제네릭과 템플릿은 둘 다 각각의 언어에서 매개  변수가 있는 형식을 지원하는 과정이다.

하지만, 둘 사이에는 많은 차이가 존재한다. 

- C# 제네릭과 C++ 템플릿의 주요 차이점

C# 제네릭은 구문 수준에서 매개 변수가 있는 형식에 대해 더 간단하게 접근할 수 있다.

하지만, C++ 템플릿에 비해 기능 중 일부를 제공받지 못한다.

구현 수준에서는 런타임에 C# 제네릭 형식 대체가 수행되어 인스턴스화 된 개체에 대해 제네릭 형식 정보가 유지된다.

C++는 컴파일 시점에서 템플릿이 인스턴스화 되지만, C#에서는 실행 시점에 타입이 지정된다.

이 차이로 인해, C++는 컴파일 시점에 복잡한 논리나 계산을 지원해주지만 C#에서는 불가능한 등

아래 사진에 있는 구체적인 차이점이 발생한다.

![image](https://github.com/Glaz8212/training-task/blob/main/240724-Generic/%EC%A0%9C%EB%84%A4%EB%A6%AD%EA%B3%BC%20%ED%85%9C%ED%94%8C%EB%A6%BF%EC%9D%98%20%EC%B0%A8%EC%9D%B4%EC%A0%90.png)

[C++ 템플릿과 C# 제네릭의 차이점 - C#](https://learn.microsoft.com/ko-kr/dotnet/csharp/programming-guide/generics/differences-between-cpp-templates-and-csharp-generics)