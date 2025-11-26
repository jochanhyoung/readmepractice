<img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black">
# 🐧 Linux Process Management

![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Bash](https://img.shields.io/badge/Shell_Script-4EAA25?style=for-the-badge&logo=gnu-bash&logoColor=white)
![System](https://img.shields.io/badge/System_Admin-000000?style=for-the-badge&logo=ubuntu&logoColor=white)

> **Summary**: 리눅스 시스템의 프로세스를 모니터링하고 제어하기 위한 4대 핵심 명령어(`top`, `ps`, `jobs`, `kill`) 가이드입니다.

---

## 📊 1. Commands Overview

| Icon | Command | Type | Description | Critical |
|:---:|:---:|:---:|:---|:---:|
| 📈 | **`top`** | **Real-time** | 시스템 전체 리소스(CPU/MEM) 실시간 모니터링 | ⭐⭐⭐⭐⭐ |
| 📸 | **`ps`** | **Snapshot** | 특정 순간의 프로세스 상태 및 PID 조회 | ⭐⭐⭐⭐⭐ |
| ⏯️ | **`jobs`** | **Session** | 현재 쉘 세션의 백그라운드 작업 관리 | ⭐⭐⭐ |
| 🔫 | **`kill`** | **Signal** | 프로세스에 종료/제어 시그널 전송 | ⭐⭐⭐⭐⭐ |

---

## 🛠️ 2. Detailed Usage

### 1. `top` : 시스템 리소스 실시간 모니터링
> **Real-time System Monitoring**

윈도우의 '작업 관리자'와 유사합니다. 현재 시스템의 **CPU 점유율, 메모리 사용량, 실행 중인 프로세스 상태**를 실시간(Real-time)으로 갱신하며 보여줍니다. 시스템 부하가 걸렸을 때 원인을 파악하기 위해 가장 먼저 사용합니다.

### 2. `ps` : 현재 프로세스 상태 스냅샷
> **Process Status Snapshot**

`top`과 달리 움직이지 않는 **정적(Static)인 상태**를 출력합니다. 명령어를 입력한 그 순간 실행 중인 프로세스 목록을 보여주며, 특정 데몬의 실행 여부를 확인하거나 종료할 대상을 찾기 위해 **PID(Process ID)**를 조회할 때 주로 사용합니다.

### 3. `jobs` : 현재 쉘 세션의 작업 관리
> **Job Control in Shell**

전체 시스템이 아닌, **현재 터미널(Shell Session)**에서 실행시킨 작업들의 목록을 보여줍니다. 백그라운드(Background)에서 실행 중이거나 잠시 정지된(Stopped) 작업의 번호와 상태를 확인하여 멀티태스킹을 관리합니다.

### 4. `kill` : 프로세스에 종료 신호 전송
> **Send Signals to Processes**

특정 프로세스(PID)에 **시그널(Signal)을 보내 제어**하는 명령어입니다. 단순히 강제 종료하는 것뿐만 아니라, 프로세스에게 "정상 종료(SIGTERM)", "강제 종료(SIGKILL)", "일시 정지" 등의 신호를 보내 생명 주기를 관리합니다.
