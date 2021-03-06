# Binary Search Tree 의 특징

삽입, 삭제, 검색의 성능을 모두 좋게 만들어주는 자료구조가 있으면 좋겠다는 아이디어에서 만들어진 자료구조이다.

고급 테크닉이 적용되지 않은 경우 모든 동작은 greedy 하게 동작하기 때문에 최악의 경우 skewed tree 가 될 수 있다.

skewed tree 일 때의 검색 알고리즘은 어떻게 동작할 것인가?

skewed tree 는 모두 알고있는 것처럼 리스트처럼 동작하게 될 것이기 때문에 일반적인 리스트 자료구조를 사용하는 것보다 overhead 가 더 있을 것이다.

삽입, 삭제, 탐색은 많은 레퍼런스가 있으니 그 것들을 참고하자

# ArrayList 의 add 의 단점

ArrayList 는 element 를 추가할 때 이미 추가된 요소들을 뒤로 밀어주는 작업이 필요하다.

또한 배열의 크기가 부족하다면 새로 만들어서 복사하는 작업이 필요하다.

## 보완법

옮겨야되는 요소들의 메모리영역을 copy and paste 하면 O(1) 로 해결 가능하다.

그렇게되면 메모리의 used space 가 일시적으로 증가하겠지만 LinkedList 를 사용하는 것보다 locality 가 좋기 때문에 성능상으로 좋을 것이라고 판단된다.

실제로 c++ 는 realloc 을 통해 위와같은 방법으로 내부 구현이 돼있다.
