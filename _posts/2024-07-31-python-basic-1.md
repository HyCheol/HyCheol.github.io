---
title: "[파이썬/Python] 기초 강좌-1"
excerpt: "주석, 변수, 연산자, 입출력" #부제
header:
  overlay_image: "/assets/header.jpg"
  overlay_filter: 0.3 # same as adding an opacity of 0.5 to a black background
  teaser: "/assets/teaser_python.png"
last_modified_at: 2024-07-31
categories:
  - python
tags:
  - python
toc: true
toc_sticky: true
toc_label: "Table of content"
---
## 요약
* Python 개요
* 주석, 변수, 연산자, 입출력

## Python 개요
* 1989년 귀도 반 로섬이 개발
* 인터프리터 프로그래밍 언어이다.
  * 컴파일 베이스 언어  
    * C, C++, JAVA 등 
    * 코드 전체를 컴파일(2진수로 변환) 후 프로그램 실행
    * 컴파일 중 코드 중간에 문제가 있으면 아예 실행되지 않는다.  
  * 인터프리터 언어  
    * Python
    * 코드를 한 줄씩 컴파일(2진수로 변환) 및 실행
    * 코드에 문제가 있더라도 그 직전까지는 실행된다.
* 타입이 없는 클래스나 함수를 모두 객체로 취급
* 속도는 느리지만 다루기 편함

## 주석
* 코드에 대한 설명을 작성하거나 범위 주석을 통한 디버그 시 사용한다.
* 인터프리터 언어인 Python은 한 줄씩 실행되다가 주석처리된 코드는 건너뛴다.
* 주석 적용법
  * 한 줄 주석 : 코드 앞 # 작성
    * 범위 드래그 후 ctrl + / 입력 시 해당 범위 전체 줄 주석 처리
  * 범위 주석 : 범위의 시작과 끝에 큰 따옴표 또는 작은 따옴표 3개 작성

## 변수
* 변수 선언 : 변수명 = 값
  * 세미콜론이 없다.
* 파이썬은 변수를 선언할 때 내부적으로 다른언어와 다르게 작동한다.
* 다른 언어(C, Cpp, Java 등) : 메모리에 변수를 위한 공간 할당 후 그 공간에 값 저장
* 파이썬 : 메모리에 값(숫자, 리터럴 등)을 저장 후 변수가 해당 메모리 주소를 참조(바인딩)  
* 메모리 공간에 같은 값(리터럴)을 중복해서 저장하지 않는 파이썬의 특성
* 아무런 변수가 참조하지 않고 있는 변수는 가비지 컬렉터가 삭제한다.  
![변수](https://1drv.ms/i/c/e3d35b35c4a6215d/IQOFmCxw_dK6RKgy8N11JiGzAazEGFoIKDzUX8Vx2cQHjiY?width=660)  
* 변수의 형태
  * 정수형
  * 실수형 : 지수 형태로 작성하는 Scientific Notation 존재 (a = 3.42e-5)
  * 문자형
  * 논리형 : True, False가 있으며, True는 메모리에 저장된 정수 1을 참조하고,  False는 정수 0을 참조한다.

## 연산자
* \+ : 더하기
  * 문자열 더하기 가능  

```py
a = 'abc'
b = 'def'
c = a + b
print(c) #abcdef
```
* \- : 빼기
* \* : 곱하기
  * 문자열 곱하기 가능  

```py
a = 'abc'
b = 3
c = a * b 
d = a*(b-True)
print(c) #abcabcabc
print(d) #abcabc
```
* \/ : 나누기 - 다른 언어와 다르게 정수/정수 시 나머지에 상관없이 결과값이 무조건 실수
* // : 몫 - 무조건 정수
* % : 나머지 - 무조건 정수
* ** : 제곱 - 루트 표현 가능(0.5승)
* <, >, <=, >=, ==, != : 비교연산
* and, or : and, or 연산
* not() : 매개변수의 True, False를 반대로 출력하는 함수

## 출력
* print 함수
  * print(변수 또는 값, ..., end='')
    * end 사용 시 기본값인 개행문자 대신 다른 문자를 넣을 수 있음  

```py
a = 4, b = 5
print(a,b) #4 5\n
print('ab',b) #ab 5\n
print(a,end='*')
print(b,end='=') #4*5=
```
  * print('%포멧'%(값))
    * 포멧에 따라 출력값 형태 변경  

```py
a = 47.12579
print(a) #47.12579
print('%.2f'%(a)) #47.13
print('%.3e'%(a)) #4.713e1
print('%d'%(a)) #47

b = 51.123
print('a:%f이고, b:%f이다'%(a,b)) #a:47.12579이고, b:51.123이다
```
  * print(f'문자열{변수값}')  
  
```py
a = 4, b = 4.8
print(f'a의값{a}이고 b의값{b}') #a의값4이고 b의값4.8
```

## 입력
* input 함수
  * 변수 = input('입력값')
  * 입력값은 변수에 무조건 문자 형태로 들어가므로, 상황에 따라 캐스팅 필요

<!--
왼쪽 정렬 (Default).
{: .text-left}
중앙 정렬
{: .text-center}
오른쪽 정렬
{: .text-right}

마크다운은 줄바꿈을 인식하지 않는다.

줄바꿈을 하기 위해서는 라인 끝에 스페이스를 2번 표기해야 한다.

여러가지 강조 표시 
(기울이기) *single asterisks*, _single underscores_, (굵은글씨) **double asterisks**, __double underscores__, (삭선) ~~cancelline~~

글머리 달기 # 문자 사용
# This is a H1
## This is a H2
### This is a H3

인용문 (단계별 깊이) > 블럭 인용 문자를 사용
ex)
> This is a first blockqute.
>> This is a second blockqute.
>>> This is a third blockqute.

줄바꿈 특수문자 (검은원, 흰색원, 검은네모순서 줄바꿈 특수문자로 출력됨, * 말고 +, -로 써도됨)
* 과자
  * 라면
    * 사탕

코드 인용

일반 코드
```
function test() {
  console.log("notice the blank line before this function?");
}
```
언어별 하이라이트 적용 코드
(루비)
```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```
(C)
```c
int main() {
  int y = SOME_MACRO_REFERENCE;
  int x = 5 + 6;
  cout << "Hello World! " << x << std::endl();
}
```

(C++)
```cpp
int main() {
  int y = SOME_MACRO_REFERENCE;
  int x = 5 + 6;
  cout << "Hello World! " << x << std::endl();
}
```

(Python)
```python
s = "Python syntax highlighting"
print s
```

수평선 만들기 (아무거나 다됨)
* * *
***
*****
- - -
---------------------------------------

링크
- 링크 표시법 : [Title](link)
ex)
[Google 페이지 링크](https://google.com)
문장 : Google 페이지 링크, 실제 하이퍼링크 : https://google.com로 출력

- 주소 직접 표시법
ex)
<https://google.com>
링크에 하이퍼링크된 후 출력

이미지 삽입
ex)
![](https://devinlife.com/assets/images/bio-photo-keyboard-small.jpg)

이미지 정렬
-가운데 정렬
![](https://devinlife.com/assets/images/bio-photo-keyboard-small.jpg){: .align-center}

표만들기
- 내용 가운데 정렬
| 항목 | 가격 | 개수 |
|:---:|:----:|:----|
| 라면 | 800원 | 10개 |
| 과자 | 900원 | 20개 |

- 내용 좌측/중앙/우측 정렬
| 항목 | 가격 | 개수 |
|:----|:----:|----:|
| 라면 | 800원 | 10개 |
| 과자 | 900원 | 20개 |

-->