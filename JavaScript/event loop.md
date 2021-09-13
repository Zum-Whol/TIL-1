
code를 Stack에 넣고 순서대로 실행
stack은 하나밖에 없고 한 번에 1개의 코드 실행 가능 (싱글스레드). 병렬처리 못함

비동기 요청은 (ajax 요청, 이벤트리스너, setTimeout)는 대기실에 있음

대기실(예시 : web API)에서 작업이 마쳐지면 콜백 큐, 이벤트 큐로 이동 (callback Queue)
stack이 비어있으면 큐에 있는 내용이 stack에 올라감

스택(Call Stack)을 바쁘게 만들지 말기
큐를 바쁘게 만들지 말기
(task queue라는 용어도 있네)

event loop : queue에 있는 콜백을 stack에 넣어줌

자바스크립트는 동기적으로 처리가 됨
비동기적 처리도 가능 : setTimeout, eventListenr 

