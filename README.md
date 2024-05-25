# opensource assignment


***
## top
-----------------------------
<img width="682" alt="image" src="https://github.com/hyeeun00/open/assets/141088088/22640ee3-839c-4af4-bbdd-ef20f7897369">

**개념**


top 명령어는 리눅스 모든 운영체제에서 실행중인 프로세스와 시스템 자원 사용량을 실시간으로 모니터링 할 수 있도록 도와주는 도구이다. 시스템의 상태를 전반적으로 가장 빠르고 파악 가능하다. CPU, Memory, Process, disk 활동 등 다양한 측면에서 시스템의 성능을 파악하는 데 도움을 준다.

**주요 기능**


| 항목 | 역할 | 세부 설명 |
|:----:|:------------:|:----------------------------------------------:|
|PID | 프로세스 식별자 | 각 프로세스의 고유한 식별번호로, 해당 프로세스를 식별하는데 사용|
| USER| 사용자 | 프로세스를 실행한 사용자 계정을 나타냄|
| PR | 우선순위 | 프로세스의 실행 우선순위를 나타냄 |
| NI | 우선순위 변경모드 | 사용자에 의해 변경된 프로세의 우선 순위를 나타냄 |
| VIRT | 가상 메모리 사용량 | 프로세스가 사용하는 가상 메모리의 크기를 킬로바이트 단위로 표시함 |
| RES | 실제 메모리 사용량 | 프로세스가 실제로 점유하고 있는 물리적 메모리의 크기를 킬로바이트 단위로 표시함 |
| SHR | 공유 메모리 사용량 | 다른 프로세스가 실제로 점유하고 있는 물리적 메모리의 크기를 킬로바트 단위로 표시함 |
| S | 상태 | 프로세스의 현재 상태를 나타내며, 'R'은 실행중, 'S'는 슬립 중'Z'는 좀비상태를 의미함
| % CPU | CPU 사용률 | 프로세스가 CPU를 사용하는 비율을 백분율로 나타냄|
| % MEM| 메모리 사용률 | 프로세스가 메모리를 사용하는 비율을 백분율로 나타냄 |
| TIME+ | 누적 CPU 시간 | 프로세스가 실행되며 사용한 누적 CPU시간을 표시함 |
| COMMAND | 명령어 | 프로세스를 실행한 명령어 또는 프로그램을 나타냄 |


**top 실행 전 옵션**

순간의 정보를 확인하려면 -b 옵션 추가(batch 모드)

-n : top 실행 주기 설정(반복 횟수)

**top 실행 후 명령어**

shift + p : CPU 사용률 내림차순

shit + m : 메모리 사용률 내림차순

shift + t : 프로세스가 돌아가고 있는 시간 순

k : kill. k 입력 후 PID 번호 작성. signal은 9

f : sort field 선택 화면 -> q 누르면 RES순으로 정렬

a : 메모리 사용량에 따라 정렬

b : Batch 모드로 작동

1 : CPU Core별로 사용량 보여줌
