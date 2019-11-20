# STM32F103_Startup
Escape starter project
bulltin board in "https://cafe.naver.com/circuitsmanual" 2018 STM32 초보탈출

![](https://cafeptthumb-phinf.pstatic.net/MjAxOTAxMjJfMjE3/MDAxNTQ4MTMzODAxMzI4.YxRKotS-lNniUIa1DBTNrL_FyXryGzXYA-quMYBK1OIg.YziRtRKuiT4bcOHwL4fWEahlhOo3zNhqryihul-5d_Ig.JPEG.ultraraptor/STM32F-103C8T6-ARM-STM32-Minimum-System-Development.jpg_350x350.jpg?type=w740)
안녕하세요 STM32초보탈출 프로젝트를 진행하며, 1기 초보탈출 내용을 정리해보고자 글을 썻습니다.
이 글 말고도 아래 제 개인 Github에 간단한 문서와 글을 업로드 하였으니, 참고 하시면 될듯 합니다.

https://github.com/Baccas-Kim/STM32F103-Startup
->GitHub는 어느정도 축약버전으로 업로드 하였습니다.

몇일 인터넷상에 정보글을 올리면서, 정보의 가공과 남들이 보기 쉽게 정리하는 과정또한 만드는것 만큼이나 중요하다는걸 느꼈습니다. 

구슬이 서말이라도 꿰어야 보배라는 말을 카페에서 들었는데.. 지금까지 해놓은 것들은 만들기에 너무 급급하지 않았나? 라는 생각을 좀 해봤습니다.
이러한 이유로 지금까지 한것들을 정리하고 (개인적으로)초보탈출 1기 프로젝트 마무리 해보려고 합니다.

다음 프로젝트에는 1차 버전의 실험보드 수정보완버전 제작, 제품수준의 다른 프로젝트(FND시계, 오디오 아날라이저, RS-232통신 모터제어기)도 만들고 싶은 생각이 듭니다.
*레지스터 직접방식도 기회가 되면 글을 계속 써 보겠습니다.

혹시라도 방향성에 대한 제시라던가, 고견 제시 부탁드리겠습니다 :)



103 초보탈출 1차 리스트(37개)==========================================

00.[문서] STM32F1을 공부하며 많이 찾아보게 되는 문서 두가지 공유
https://cafe.naver.com/circuitsmanual/209330

01.[EXTI] 버튼 인터럽트로 LED 켜고끄기
https://cafe.naver.com/circuitsmanual/209332

02.[UART] Hello world 시리얼 모니터로 출력하기
https://cafe.naver.com/circuitsmanual/209346

03.[TIM] 기능을 이용한 LED토글 - (해결 중..)
https://cafe.naver.com/circuitsmanual/209397

04.[TIM] 1초마다 LED 상태 반전
https://cafe.naver.com/circuitsmanual/209404

05.[TIM] HSE, LSE 클럭(외부 발진기) 사용해 TIM 기능 사용하기
https://cafe.naver.com/circuitsmanual/209405

06.[중간점검]추가로 진행해야 할 peripheral 들
https://cafe.naver.com/circuitsmanual/209437

07.[HD44780] 1602 CLCD로 Hello World 출력하기
https://cafe.naver.com/circuitsmanual/209444

08.[TIM] PWM 으로 4개 led 밝기 변화
https://cafe.naver.com/circuitsmanual/209446

09.[ADC] USART1로 ADC 값 출력하기
https://cafe.naver.com/circuitsmanual/209510

10.[Project] Fnd 시계 만들기 - 1 
https://cafe.naver.com/circuitsmanual/209705

11.[RTC] 내부 RTC에서 시간 데이터 읽어 UART로 출력
https://cafe.naver.com/circuitsmanual/209776

12.[Motor] DC모터 정 역 방향 회전
https://cafe.naver.com/circuitsmanual/209828

13.[Motor] Stepping 모터 정역 회전 실험
https://cafe.naver.com/circuitsmanual/209829

14.[Project] 실험보드 만들기 - 1
https://cafe.naver.com/circuitsmanual/209850

15.[Project] 실험보드 만들기 - 2
https://cafe.naver.com/circuitsmanual/209865

16.[Project] 실험보드 만들기 - 3
https://cafe.naver.com/circuitsmanual/209878

17.[Project] 실험보드 만들기 - 4
https://cafe.naver.com/circuitsmanual/210026

18.개발보드에 ST-Link 연결 실패!
https://cafe.naver.com/circuitsmanual/210173

19.[Project] 실험보드 만들기 - 5
https://cafe.naver.com/circuitsmanual/210540

20.[Project] 실험보드 만들기 - 6
https://cafe.naver.com/circuitsmanual/210546

21.[Project] 실험보드 만들기 - 7
https://cafe.naver.com/circuitsmanual/210722

22.[Project] 실험보드 만들기 - 8
https://cafe.naver.com/circuitsmanual/210724

23.[Project] 실험보드 만들기 - 9
https://cafe.naver.com/circuitsmanual/210758

24.[Project] 실험보드 만들기 - 10: 하드웨어 이슈 공유
https://cafe.naver.com/circuitsmanual/210760

25.[RTC] LSE클럭을 이용한 RTC시간의 출력(USART)
https://cafe.naver.com/circuitsmanual/210777

26.[Project] 실험보드만들기 11 - 실험용 PCB(Ver0.0.1212) 무료 분양!!!
https://cafe.naver.com/circuitsmanual/210794

27.[MCU] GPIO 핀의 최대 전류허용한계
https://cafe.naver.com/circuitsmanual/210795

28.[Project] 실험보드만들기 12 - PCB받으실 분들
https://cafe.naver.com/circuitsmanual/210823

29.[I2C] MPU6050센서의 연결
https://cafe.naver.com/circuitsmanual/210827

30.[TIM] PWM기능을 활용한 Servo 모터의 구동
https://cafe.naver.com/circuitsmanual/210853

31.[TIM] 타이머의 계산(요약) 
https://cafe.naver.com/circuitsmanual/210854

32.[Project] 중간점검 2차
https://cafe.naver.com/circuitsmanual/210866

33.H/W 이슈 공유 - USBDP핀 풀업저항
https://cafe.naver.com/circuitsmanual/210870

34.[USB] USB로 문자열 송수신하기
https://cafe.naver.com/circuitsmanual/210871

35.[ADC] USART3로 ADC 값 출력하기[미완]
https://cafe.naver.com/circuitsmanual/210881

36.[ADC] NTC서미스터 및 내부 온도 센서 값 읽기
https://cafe.naver.com/circuitsmanual/210961
