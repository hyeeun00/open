#opensource assignment

//top = ps = jobs = kill =
***
**top**

<img width="682" alt="image" src="https://github.com/hyeeun00/open/assets/141088088/22640ee3-839c-4af4-bbdd-ef20f7897369">


1. 개념


top 명령어는 리눅스 모든 운영체제에서 실행중인 프로세스와 시스템 자원 사용량을 실시간으로 모니터링 할 수 있도록 도와주는 도구이다. 시스템의 상태를 전반적으로 가장 빠르고 파악 가능하다. CPU, Memory, Process, disk 활동 등 다양한 측면에서 시스템의 성능을 파악하는 데 도움을 준다.



옵션 없이 입력하면 interval 간격(기본 3초)으로 화면을 갱신하며 정보를 보여줌
top 실행 전 옵션
순간의 정보를 확인하려면 -b 옵션 추가(batch 모드)
-n : top 실행 주기 설정(반복 횟수)
top 실행 후 명령어
shift + p : CPU 사용률 내림차순
shit + m : 메모리 사용률 내림차순
shift + t : 프로세스가 돌아가고 있는 시간 순
k : kill. k 입력 후 PID 번호 작성. signal은 9
f : sort field 선택 화면 -> q 누르면 RES순으로 정렬
a : 메모리 사용량에 따라 정렬
b : Batch 모드로 작동
1 : CPU Core별로 사용량 보여줌
ps와 top의 차이점
ps는 ps한 시점에 proc에서 검색한 cpu 사용량
top은 proc에서 일정 주기로 합산해 cpu 사용율 출력