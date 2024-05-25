# opensource assignment

>20243095 임혜은
-----------------------


## top

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


## ps

<img width="682" alt="image" src="https://github.com/hyeeun00/open/assets/141088088/1b7c57a7-13a1-438f-bbb6-578b4dca24e4">

**개념**

리눅스에서는 여러 개의 프로세스가 동시에 실행되기 때문에 현재 실행 중인 프로세스의 정보를 얻기 위해 사용되는 명령어

프로세스 중에서 CPU, 메모리 등등을 많이 점유하고 있거나, 지나치게 많은 자식 프로세스를 생성하는 등등에 시스템에 속도가 느려지는 경우 ps 명령어로 분석하여 시스템 오류를 감지할 수 있음

**주요 기능**
|항목| 의미 |	세부설명|
|:-----:|:------:|:-------:|
|PID|process ID	|프로세스마다 주어지는 번호 입니다|
|TTY|TeleTypewriter	|명령어가 실행되는 터미널의 번호, 할당된 것이 없는 경우 물음표(?) 출력 합니다|
|STAT| 	|실행되고 있는 프로세스 상태 입니다(R, S, D, T, Z, W, N)|
|START| |	프로세스가 시작된 시간 입니다|
|TIME	| |CPU가 사용한 시간 입니다|
|USER|USER	|사용자 이름 입니다.|
|COMMAND|COMMAND	|사용자가 실행한 명령어 입니다|
|UID|User ID	|사용자의 ID 입니다.|
|PGID|Parent Group ID|	사용자 부모 프로세스이 그룹 ID 입니다|
|SID|Session ID	|세션 ID 입니다|
|PRI|PRIority	|실행하는 우선순위에 따른 프로세스 입니다|
|NI|NIce	|nice에 의한 우선순위에 따른 프로세스 입니다.|
|RSS|Resident Set Size|	프로세스가 사용하는 메모리의 크기 입니다.|
|SZ|SiZe	|프로세스가 사용하는 자료와 스택의 크기 입니다.|
|SHRD|SHareD	|프로세스가 사용하는 공유 메모리|
|%CPU	||프로세스가 사용하는 CPU 점유율|
|%MEM	||프로세스가 사용하고 있는 메모리 점유율|
|WCHAN||	프로세스가 실행하고 있는 커널 루틴|
|VSZ	||KiB 단위(1024 바이트 단위)의 프로세스의 버추얼 메모리 크기(vsize와 동일한 의미)|





**명령어**
| 옵션 |	의미|
|:------:|:--------:|
|-a	|세션 리더와 터미널과 연관이 없는 프로세스를 제외한 모든 프로세스를 출력|
|a	|BSD 스타일로서 터미널과 연관된 모든 프로세스를 출력하거나, x 옵션과 함께 사용되어 모든 프로세스를 출력|
|-d	|세션 리더를 제외한 모든 프로세스들을 출력|
|r	|실행 프로세스만 출력|
|x	|BSD 스타일로서 혼자 사용되면 사용자에 의해 소유된 모든 프로세스를 출력하고 a 옵션과 함께 사용되어 모든 프로세스를 출력|
|-l	|상세한 내용을 출력|
|-f	|완전한 형식의 목록을 출력|
|-h	|메뉴는 보여주지 않음(PID, TTY, STAT, TIME, COMMAND 등)|
|-j	|작업에 관련된 ID를 출력|
|-l	-j |옵션보다 자세하게 정보를 출력|
|u	|사용자 친화적인 형식으로 출력|
|f	|프로세스 간 상속관계를 트리구조로 출력|
|n	|사용자의 정보를(모든 형식의 UID와 GID를 포함하여) 숫자로 표시|
|-w	|출력결과를 생략하지 않고 넓게 출력|

## jobs

<img width="682" alt="image" src="https://github.com/hyeeun00/open/assets/141088088/0bb19c8a-2e46-4fbc-a486-07e5c079c9e5">

**개념**

백그라운드로 실행 중인 프로세스나 현재 중지된 프로세스의 목록을 출력해 주는 명령

사용법 : jobs [옵션] [작업명]

**명령어**
-l : 프로세스 ID와 함께 잡 목록을 출력

-n : 마지막로 알림 이후 변경된 잡만 출력

-p : job의 프로세스 ID만 출력

-r : 실행 중인 job만 출력

-s : 중지된 job만 출력

## kills

<img width="249" alt="image" src="https://github.com/hyeeun00/open/assets/141088088/f78ae6ff-a846-4712-aa10-a4d7568eceb2">


<img width="697" alt="image" src="https://github.com/hyeeun00/open/assets/141088088/2874c52a-764a-48b2-8680-cf605c569c45">


**개념**

주로 프로세스를 종료하는 용도로 많이 사용

사용법 : kill [옵션] [PID]

**옵션**


| 옵션 | 의미 |
|:----:|:-----:|
|-9	|프로세스아이디(PID)를 직접 지정하여 종료시 사용|
|-l	|신호(Signal)로 사용할 수 있는 신호(Signal) 이름들을 보여줌|

**명령어**

| 번호 | 신호(Signal 이름 | 신호(Signal)	| 의미 |
|:----:|:----:|:------:|:-------:|
|1|	SIGHUP	|HUP	|hangup, 로그아웃등의 접속이 끊을 때 발생하는 신호(Signal)로 특정 실행 중인 프로그램이 사용하는 설정 파일을 변경시키고 변화된 내용을 적용할때 사용|
|2|	SIGINT	|INT	|현재 작동중인 프로그램의 동작을 멈출때 사용되며, 일반적인 값은 <CTRL>+<c>|
|9|	SIGKILL	|KILL	|프로그램을 무조건 종료할 경우 사용|
|11|	SIGSEGV	|SEGV	|잘못된 메모리 관리시 생기는 신호(Signal)|
|15	|SIGTERM	|TERM	|실행중인 프로그램을 정상적인 종료방법으로 프로그램을 종료하는 신호(Signal)로 kill 명령에서 신호(Signal)를 지정하지 않으면 이 신호(Signal)를 사용하여 프로그램을 종료|
|18	|SIGCONT	|CONT	|중지 되어 있는 프로그램을 재실행 하는데 사용되는 신호(Signal)|
|19	|SIGSTOP	|STOP	|프로그램을 중지 하는데 사용되는 신호(Signal)|
|20	|SIGTSTP	|TSTP	|터미널에서 중지되어 있는 신호(Signal)|
