기능 | 점검항목 | |  점검방법/결과 | 점검 시스템(TTMC /DMZ 2)  
:---: | :---: | :---: | :---: | :---:
| **시스템 확인** | 시스템 로그 확인 | OS에서 생성하는 시스템 로그 확인 | * /var/log/messages 파일을 vi 편집기를 이용하여 확인한다.<br>* dmesg 명령어 수행내역으로 fail, error , fault 등의 내역 중 특이사항이 있는지 여부를 확인한다.<br><blockquote>fail, error, fault 등의 내역을 확인함으로 시스템의 이상 유무를 판단한다. | **작성해 주세요** |				
| **HW 상태** | HW 상태 확인 | Interface 확인 | * ifconfig -a<br>* netstat -i<blockquote>ifconfig -a 명령어를 이용하여 사용하는 interface가 모두 up 이 되어 있는지 여부를 확인한다.<br>netstat -i 명령어를 이용하여 Cable 연결상태 확인 errs가 모두 0을 확인한다. | **작성해 주세요** | 
| | ㄴ | Route Table 확인  | * netstat -rn<br>* cat /etc/sysconfig/network-scripts/ifcfg-bond0<blockquote>Default gateway가 정상적으로 설정되어 있음을 확인한다.<br>Bond 구성 정보를 확인한다. |			
| | ㄴ | NTP 동기화 확인 | * ntpq -p<blockquote>Time Server와 동기화 되는지 확인한다. | **작성해 주세요** | 
| **서비스 블록 상태 확인** | Configuration | Block Configuration 정보확인 | * cd ~/etc/ini<br>* cat block_config.ini<blockquote>- ini폴더에 각각의 block 별 Configuration 정보가 적절하게 설정되어 있는지 확인한다. | **작성해 주세요** |
| ㄴ | Block 확인 | Main Process 상태 확인 | * disMP<blockquote>- 각각의 프로세스가 정상 동작중인지 확인한다. | **작성해 주세요** |
| | ㄴ | Main Process 상태 상세 확인 | * ocl 1<br>* dis-proc<blockquote>- 각각의 프로세스의 status 및 기동시간, Run_count 등 block 별 상세 정보를 확인한다. | **작성해 주세요** |
| | ㄴ | Block 별 stack 확인 | * pstack `{PID}`<blockquote>- 각 블록별 프로세스 스택을 추적한다.<br>- wait, fail, fault 등의 상태가 존재하는지 확인한다. | **작성해 주세요** |

