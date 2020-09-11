Clean Code (Robert C.Martin)

규칙 없이 코딩을 하다보니 코드가 더러워지는 것을 느꼈다.

책에서 배운 내용을 토대로 내가 사용할 규칙을 명문화하려고 한다.

# 1. Name
  + 값이 의미하는 것이 무엇인지 드러낸다.
  예) cell[1] == 4  (x)       cell[STATUS_VALUE] == FLAGGED (o)
 
  + 타입으로 해석할 수 있는 단어를 함부로 쓰지 않는다.
  예) accountList (x)        accounts, accountGroup  (o)

  + 유사한 이름 사용하지 않는다.

  + 정보 없는 이름을 피한다.
  예) a2[i] = a1[i] (x)       source[i] = destination[i] (o)

  + 발음하기 쉬운 이름을 사용한다.
  예) 과도한 줄임말 (x)

  + 검색하기 쉬운 이름 사용한다.
  예) 3 (x)       MAX_CLASSES_PER_STUDENT (o)
   
  + 클래스는 명사나 명사구 사용하고 동사 쓰지 않는다.
  
  + 메서드는 동사나 동사구 사용한다.
  
  + Accessor, Mutator, Predicate 는 각각 get, set, is 붙인다(javabean)
  
  + 유머감각을 발휘하지 않는다.
  
  + 한 개념에 한 단어를 사용한다.
  예) get, fetch, retrieve     manager, controller
  
  + 다른 개념에 다른 단어를 사용한다.
  예) 집합에 값 추가하는 add 와 값 이어붙이는 add (x)
  
  + 문제 영역의 언어와 해법 영역의 언어를 적절히 사용한다.
  예) 서비스의 언어, 개발자의 언어
  
  + 맥락을 적절히 추가한다.
  예) city, state (x)        addrCity, addrState (o)
  
# 2. Function
짧게(if 안에 한줄만)
하나만
추상화 수준도 하나만
위에서 아래로 추상화 수준 한단계씩
인수 최대한 적게
인수1개 : 체크, 변환, 이벤트 발생(주의)
인수2개 : 자제
인수3개 : 인수 최대한 줄이기
