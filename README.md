# [내일배움캠프 사전캠프] C++ 기초학습 1주차 과제

오늘은 C++ 기초학습의 1주차 강의 자료에 있는 과제를 해결하면서

내가 배웠던 C++의 기본 문법에 대해 다시 점검하고 응용하는 시간을 가졌다.

## 1. 오늘 학습 키워드

**Rand () 함수와 srand () 함수**

## 2. 오늘 학습 한 내용을 나만의 언어로 정리하기

C++에서 사용 가능한 변수 생성 함수를 활용하여 결과값에 약간의 랜덤성을 부여하여 

플레이어의 선택에 따라 게임의 진행이 변하게 만듫었습니다.

또한 레벨을 이용하여 기존 과제의 코드에 있던 도망 선택지의 리스크를 늘리고 리워드를 생성하여

플레이어가 적극적으로 전투에 임했을때 게임이 유리해지 보상이 주어지게 하였습니다.

## 3. 학습하며 겪었던 문제점 & 에러

과제를 만들면서 나만의 
```cpp
protected:
	int Type;
	int Level;
	int Levelcount;

int Character::random(int a, int b) 
{
	int rand = 0;
	for (int i = 0; i < a; i++)
	{
		rand += std::rand() % b;
	}

	return rand;
}

bool Character::LevelUpEvent() 
{
	int TL= 0;
	TL += random((Level + 1), 6) + (Levelcount * 6);
	if (TL > 2 * LevelArr[Level])
	{
		Level++;
		Levelcount = 0;
		return true;
	}
	else
	{
		Levelcount++;
		return false;
	}
} 


void Character::skill1(Actor* hit)
{
	int damage = 0;
	damage += random(1, 6) + LevelArr[Level];
	std::cout << "1번 스킬 데미지 : " << damage << std::endl;
	hit->Damaged(damage);
}

void Character::skill2(Actor* hit)
{
	int damage = 0;
	damage = random(LevelArr[Level], 4) + (2 * LevelArr[Level]);
	std::cout << "2번 스킬 데미지 : " << damage << std::endl;
	hit->Damaged(damage);
}

void Character::skill3(Actor* hit)
{
	int damage = 0;
	damage = 3 * (random(LevelArr[Level], 8) + LevelArr[Level]);
	std::cout << "3번 스킬 데미지 : " << damage << std::endl;
	hit->Damaged(damage);
}
```
## 4. 내일 학습 할 것은 무엇인지

내일은 C++ 기초학습 2주차 강의를 진행하면서 언리얼의 블루프린트와 언리얼 전용 C++의 기본적인 구조에 대해 공부할 생각 입니다..


#내일배움캠프 #사전캠프 #TIL 
 
