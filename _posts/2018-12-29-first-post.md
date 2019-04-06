---
title: "1일차"
date: 2018-12-29 13:00:00 -0400
---
목표 :  C++ 강의 1.5~1.14 듣기 

목표 설정 이유 : 알고리즘 문제 풀이를 위한 C++의 필요성 

과정 : 

수업을 들으면서 직접 코드를 따라 작성하면서 개념을 이해하였습니다.

특히 이번 수업 중 전처리기에 대한 설명이 가장 흥미로웠으며, STL에 대한 관심이 더욱 증가했습니다.

지금까지 Java로 알고리즘 문제를 풀어왔었는데, 제 실력이 부족하고 실행 속도와 간편한 library 부족이 C++을 배우게 되었습니다.

팀원들 간 같이 공부하는 부분이 아직은 없다 보니까, 조용한 분위기에서 이루어졌습니다. 

이번 모각코 중 작성한 namespace 연습 코드입니다.
```c++
#include <iostream>

/*
int doSomething(int a, int b)
{
	return a + b;
}

int doSomething(int a, int b)
{
	return a * b;
}
*/
// => 이건 오류남 그런데 저 이름을 반드시 유지해야 한다면?
// 여러가지가 있지만 이번 강의에서는 namespace 활용법을 배울것

// namespace안 또다른 namespace가 정의가능 
namespace MySpace1
{
	namespace InnerSpace 
	{
		int doSomething(int a, int b)
		{
			return a + b;
		}
	
	}
	int doSomething(int a, int b)
	{
		return a + b;
	}
	
}

int doSomething(int a, int b)
{
	return a * b;
}

using namespace std; // iostream내 cout은 std안에서 정의됨

int main() 
{
	using namespace MySpace1;// 여기서부터는 MySpace1이라는 공간을 사용할것

	// 모든 경우마다 
	MySpace1::doSomething(3, 4); // 이건 귀찮을 수 있어

	using namespace MySpace1::InnerSpace; // 두개 이상의 namespace를 가질 때
	MySpace1::InnerSpace::doSomething(3, 4);

	//cout << MySpace1::doSomething(3, 4) << endl;
	//cout << doSomething(3,4)  << endl;

	return 0;
}
```

목표 회고 : 

제 목표는 오늘 C++ 강의를 일정량 듣고 익히는 것이었습니다. 

아직은 초반이라 그런지 빠르게 이해하고 진도를 나갈 수 있었지만, 

후반부로 갈수록 자칫 잘못하다가는 밀릴 수도 있다는 느낌이 듭니다.

이번 방학 안에 다 끝내고 싶어서 평일에도 시간을 내어 최대한 강의를 듣고 복습하는 방식으로 공부할 것입니다. 


후기 : 

오늘 처음인데 3시간은 너무 길다고 생각이 됩니다. 

아직 방학이라는 단꿈에서 벗어나지 못한 것인지 마음이 계속 붕 떠있는 기분으로 나태해져 가는 걸 막기 위해서 

천안에서 버스 타고 와서 좋은 친구들과 같이 공부하지만 힘이 드네요. 

그래도 집에서 있었다면 뒹굴뒹굴 했을 것이라, 저 혼자가 아니라 주위에 같은 사람들과 공부하니까 냉정하게 자신을 바라볼 수 

있는 기회가 되었습니다. 

오늘 처음 모각코를 잘 마쳤으니 계속해서 잘 이루어졌으면 좋겠습니다. 

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/

