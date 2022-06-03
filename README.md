# 20213031
top 명령어는 현재 OS의 상태를 나타내주는 CLI 어플리케이션입니다. 메모리 사용량, CPU 사용량 등을 나타내주며 top를 실행하는 동안에는 주기적인 업데이트로 실시간에 근접한 내용을 보여줍니다. 리눅스에서 top 명령어를 실행하면 아래와 깉이 노출됩니다. 위에는 전체의 요약이 있으며 아래에는 각 프로세스마다 구체적인 내용을 포함하고 있습니다.

[출처] <https://sabarada.tistory.com/146>
-----

ps 명령어는 현재 실행중인 프로세스 목록과 상태를 보여줍니다. ps의 옵션은 전통적인 유닉스 System V, BSD, GNU에 따라 결과가 다르게 나타나고 표기법에도 차이를 보입니다. 옵션 사용 시 System V 계열은 대시(dash, -)를 사용하고 BSD 계열은 대시(-)를 사용하지 않습니다. GNU에서의 옵션 표기는 두 개의 대시(-)를 사용합니다. 따라서 원하는 프로세스의 상태를 출력하려면 정확한 옵션 사용이 중요합니다.

ps 사용법
$ ps [option]


<img width="322" alt="오픈소스 ps" src="https://user-images.githubusercontent.com/106575901/171112107-a55b32ce-1b36-4b7b-9a72-a7656c85ba73.png">


<img width="269" alt="오픈소스 ps2" src="https://user-images.githubusercontent.com/106575901/171112853-a7b8f4c5-99e9-49aa-8fb5-f2ef1e52a025.png">


[출처] <https://jhnyang.tistory.com/268>
-----

jobs 명령어는 백그라운드에 실행되고 있는 프로세스나 중지된 프로세스의 목록을 출력해줍니다.

job 번호

job을 입력하고 결과를 보면 가장 첫 번째 열에 1,2,3,4 이런 숫자를 볼 수 있는데 이 숫자는 job 번호를 의미합니다. 중지되거나 백그라운드에서 돌고 싶은 작업이 있을 때 이 job 번호를 이용해서 앞단으로 가져와 실행시켜요.

jobs 기호

두 번째 열에 보면 +,-기호가 있는 프로세스들을 볼 수 있는데 +는 fg나 bg명령어를 쳤을 때 디폴트로 가장 먼저 가져와서 수행하게 될 프로세스를 의미합니다.
-는 현재 진행중인 job이 끝나면 바로 다음에 수행될 프로세스를 의미합니다.

상태값

|상태|설명|
|:--:|:--:|
|Running|작업이 계속 진행중임|
|Done|작업이 완료되어 0을 반환|
|Stopped|작업이 일시 중단|
|Stopped(SIGTSTP)|SIGTSTP 시그널이 작업을 일시 중단|
|Stopped(SIGSTOP)|SIGSTOP 시그널이 작업을 일시 중단|
|Stopped(SIGTTIN)|SIGTTIN 시그널이 작업을 일시 중단|
|Stopped(SIGTTOU)|SIGTTOU 시그널이 작업을 일시 중단|

옵션

|옵션|설명|
|:--:|:--:|
|-l|프로세스 그룹 ID를 state 필드 앞에 출력|
|-n|프로세스 그룹 중에 대표 프로세스 ID를 출력|
|-p|각 프로세스 ID에 대해 한 행씩 출력|
|command|지정한 명령어를 실행|

[출처]<https://hbase.tistory.com/265>
-----

kill 명령어

kill 명령어는 대개 프로세스를 죽일 때 사용합니다. 하지만 내부적으로는 프로세스에 시그널을 보내 원하는 작업을 하게 하는 명령어입니다. 이 툴을 사용하려면 다음 구문을 사용합니다.

|시그널|영어|설명|
|:--|:--|:--|
|1)SIGHUP|Hang Up|세션이 종료될 때 시스템이 내리는 시그널|
|2)SIGNT|Interrupt|Ctrl + C, 종료 요청 시그널|
|9)SIGKILL|Kill|강제 종료 시그널|
|11)SIGSEGV|Segment Violation|메모리 침범이 일어날 때 시스템이 보내는 시그널|
|15)SIGTERM|Terminate|기본 값, 종료 요청 시그널|
|20)SIGTSTP|Temporary Stop| Ctrl + Z 일시 중지 요청 시그널|

-----
vim에서의 매크로 실행
vi에서 매트로는 명령어 모드에서 
q + 알파벳을 눌러 특정 알파벳에 매크로를 저장할 수 있다

순서는
1. q + a       a키에 recording 시작
2. 반복을 위한 내가 원하는 동작
3. q             recoding 종료
4. @a          1회 실행 
or @@         방금 실행한 매크로 실행
or 10@a       매크로 10회 실행

[출처] <http://aboutmadlife.blogspot.com/2014/09/linux-vi-macro.html>
