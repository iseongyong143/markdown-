##### return  
기능 | 점검항목 | 링크 |  
:---: | :---: | :---: | 
| **시스템 확인** | 시스템 로그 확인 | OS에서 생성하는 시스템 로그 확인 | 
| **HW 상태** | HW 상태 확인 | [Interface 확인](#interface) | 
| | ㄴ | [Route Table 확인](#route-table)    | 		
| | ㄴ | [NTP 동기화 확인](#ntp) | 
| **서비스 블록 상태 확인** | Configuration | [block configuration 정보 확인](#block-configuration) | 
| ㄴ | Block 확인 | [Main Process 상태 확인_1](#main-process1) | 
| | ㄴ | [Main Process 상태 확인_2](#main-process2)  |
| | ㄴ | [Block별 Stack 확인](#block-stack) | 



## :one: Hw 상태
***Hw 상태 확인***  
[처음으로 돌아가기](#return)  
### Interface  
    - ifconfig -a
    - netstat -i
  <blockquote>ifconfig -a 명령어를 이용하여 사용하는 interface가 모두 up 이 되어 있는지 여부를 확인한다.<br>netstat -i 명령어를 이용하여 Cable 연결상태 확인 errs가 모두 0을 확인한다.</blockquote>  
  
  ```
  특이사항 작성
  ```

  
### Route Table
    - netstat -rn
    - cat /etc/sysconfig/network-scripts/ifcfg-bond0
  <blockquote>Default gateway가 정상적으로 설정되어 있음을 확인한다.<br>Bond 구성 정보를 확인한다.</blockquote>    

  ```
  특이사항 작성
  ```
  
### NTP
    - ntpq -p
  <blockquote>Time Server와 동기화 되는지 확인한다.</blockquote> 
  
  ```
  특이사항 작성
  ```


## :two: 서비스 블록 상태 확인
***Configuration***
[처음으로 돌아가기](#return)  
### block configuration
    - cd ~/etc/ini
    - cat block_config.ini
  <blockquote>- ini폴더에 각각의 block 별 Configuration 정보가 적절하게 설정되어 있는지 확인한다.</blockquote>

  ```
  특이사항 작성
  ```


***Block***
[처음으로 돌아가기](#return)  
### Main Process1
    - disMP
  <blockquote>- 각각의 프로세스가 정상 동작중인지 확인한다.</blockquote>

  ```
  특이사항 작성
  ```


### Main Process2
    - ocl 1
    - dis-proc
  <blockquote>- 각각의 프로세스의 status 및 기동시간, Run_count 등 block 별 상세 정보를 확인한다.</blockquote>

  ```
  특이사항 작성
  ```

  
### Block stack  
    - pstack `{PID}`
  <blockquote>- 각 블록별 프로세스 스택을 추적한다.<br>- wait, fail, fault 등의 상태가 존재하는지 확인한다.</blockquote>

  ```
  특이사항 작성
  ```


  
