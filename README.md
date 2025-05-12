🖥️ VDI 가상환경 자원 모니터링 시스템 구축 프로젝트
📌 프로젝트 개요
본 프로젝트는 **VDI(가상 데스크탑 인프라) 환경의 VM 자원(CPU, Memory, Disk I/O, Network)**을 실시간으로 수집하고,
Zabbix + Grafana + Slack 연동을 통해 이상 상황을 탐지 및 알림하는 모니터링 시스템을 구축한 프로젝트입니다.

상용 솔루션인 vROPS 없이도, 오픈소스 기반의 자원 추적 및 시각화 시스템을 설계하여
실시간 운영 대응과 사용자 이슈 개선이 가능한 구조를 목표로 했습니다.

⚙️ 시스템 구성
Zabbix Server: 자원 수집 및 트리거/알림 설정 담당

Grafana: 시각화 대시보드 (Zabbix 데이터 연동)

Slack Webhook: 이상 감지 시 실시간 알림

VM 대상: Ubuntu 및 Windows VM 다수 구성 (VDI 시뮬레이션)

Zabbix Agent: 각 VM에 설치, 자원 메트릭 전송

🛠️ 주요 기능
CPU, 메모리, 디스크, 네트워크 자원 실시간 모니터링

Trigger 설정으로 특정 기준 초과 시 Slack 알림 전송

Grafana 기반 대시보드 시각화 및 히스토리 분석

Slack 메시지 템플릿 구성으로 운영팀 신속 대응

사용자 불만과 자원 병목 간의 상관관계 분석 리포트 작성

🧪 핵심 기술 스택
Zabbix 6.x (Server & Agent)

Grafana OSS 10.x

Slack Incoming Webhook

Ubuntu 20.04 / Windows 10 VM

PowerShell / Bash (설정 자동화 일부 포함)

📈 결과 및 시사점
vROPS 같은 상용툴 없이도 실시간 자원 관제 및 알림 체계 구축 가능

Slack 알림 및 사용자 로그와 연결하여 사용자 민원 대응 자동화 실현

향후 VM 배포 자동화, GPO 설정 자동화와 연계하여 통합 VDI 운영 플랫폼으로 확장 가능
