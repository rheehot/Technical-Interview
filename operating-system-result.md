# 알아야 되는 내용

1. 답 필요
2. File 을 실행 중일 때 해당 파일을 수정할 수 없는 이유는 무엇인가요?: 현대 운영체제는 메모리 공유를 매우 중요하게 생각한다. 만약 excutable file 인 A 를 100 번 실행한다면 어떨까? 우리는 Data(static), Code 메모리 영역을 공유함으로써 수많은 메모리를 절약할 수 있다. 하지만 문제는 여기서 발생하는 것이 아닌 다음에서 발생한다. Paging 기법을 이용해서 메모리를 관리하는 경우를 예를 들면 우리는 알맞은 페이지들의 크기를 사용할 수 없는 상황이 발생한다. daemon 이용해서 특정 페이지들을 HW 까지 swap out 을 시켜야되는데 executable file 은 항상 Disk(다른 것이 될 수 있음)에 해당 코드의 내용이 존재한다는 점을 이용할 수 있게하기 위함이다. 그러면 swap out(Disk I/O)가 없어서 성능 향상에 도움된다. Present bit 로 인한 Page fault 만 처리하면 되니까!
3. a = a + 1 이 race condition 을 발생시키는 이유는 무엇인가요? 레지스터는 여유가 없는 상황 즉, volatile variable 임을 가정합니다.: 기계어로 번역하면 load, add, store 3 개로 나눠지는데 load, add 가 실행된 후 context switch 가 되는 경우 문제가 발생한다.
4. Condition variable 은 어떠한 thread 가 sleep 상태인지 몇 개가 sleep 인지 알 수 없다. 하지만 semaphore 는 순서에 따라 ready 상태로 만들기가 쉬우며 integer 로 관리되기 때문에 간편하다. 이는 개념적인 차이로 인한 문제인데 자세한 설명은 하지 않겠다. 문제가 되는 상황은 여러 Thread 가 malloc 이 필요한 경우이다. condition variable 은 문제를 해결하기 위해 좋지 않은 broadcast 를 만듦
5. mutex lock, condition variable 은 교환법칙이 성립되지 않는다. semaphore 는 교환법칙이 성립힌다. mutex lock 은 누군가를 깨울 수 없다.
6. event handler 로 특정 이벤트들을 처리한다. 장점은 스케쥴링을 운영체제에게 맡기지 않아도 될 수 있고 nonblocking 해야되는 단점이 있다. 그래서 구현이 복잡하다. 실수하면 큰일난다. 특히 멀티 프로세서 환경이라면 효율을 내기가 어렵다.

# 알면 좋은 내용

1.  답 필요
2.  답 필요
3.  답 필요
    1.  답 필요
4.  답 필요
    1.  답 필요

# 몰라도 되는 내용

1.  답 필요
2.  답 필요
3.  답 필요
4.  답 필요
5.  답 필요
