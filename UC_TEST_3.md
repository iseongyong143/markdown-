## Hw 상태
### Hw 상태 확인
[Interface 확인](#interface)  
[Route Table 확인](#route-table)  
[NTP 동기화 확인](ntp)  

```




































```
#### Interface
    - ifconfig -a
    - netstat -i
  <blockquote>ifconfig -a 명령어를 이용하여 사용하는 interface가 모두 up 이 되어 있는지 여부를 확인한다.<br>netstat -i 명령어를 이용하여 Cable 연결상태 확인 errs가 모두 0을 확인한다.</blockquote>  
  
  ```
  특이사항 작성
  ```
  
#### Route Table
    - netstat -rn
    - cat /etc/sysconfig/network-scripts/ifcfg-bond0
  <blockquote>Default gateway가 정상적으로 설정되어 있음을 확인한다.<br>Bond 구성 정보를 확인한다.</blockquote>    

  ```
  특이사항 작성
  ```
  
#### NTP
    - ntpq -p
  <blockquote>Time Server와 동기화 되는지 확인한다.</blockquote> 
  
  ```
  특이사항 작성
  ```

## 서비스 블록 상태 확인
### Configuration
  - **block configuration 정보 확인**
    - cd ~/etc/ini
    - cat block_config.ini
  <blockquote>- ini폴더에 각각의 block 별 Configuration 정보가 적절하게 설정되어 있는지 확인한다.</blockquote>

  ```
 이상 있음
 이상 있음
  이상 있음
 이상 있음
 이상 있음
 이상 있음
 이상 있음
  ```
  
### Block
  - **Main Process 상태 확인**
    - disMP
  <blockquote>- 각각의 프로세스가 정상 동작중인지 확인한다.</blockquote>

  ```
  특이사항 작성
  ```

  - **Main Process 상태 확인**
    - ocl 1
    - dis-proc
  <blockquote>- 각각의 프로세스의 status 및 기동시간, Run_count 등 block 별 상세 정보를 확인한다.</blockquote>

  ```
  특이사항 작성
  ```
  
  - **Block 별 stack 확인**
    - pstack `{PID}`
  <blockquote>- 각 블록별 프로세스 스택을 추적한다.<br>- wait, fail, fault 등의 상태가 존재하는지 확인한다.</blockquote>

  ```
  특이사항 작성
  ```
  
  
