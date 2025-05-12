# zabbix-grafana-vdi-dashboard
## 🖥️ VDI 가상환경 자원 모니터링 시스템 구축 프로젝트
📌 프로젝트 개요
본 프로젝트는 **VDI(가상 데스크탑 인프라) 환경의 VM 자원(CPU, Memory, Disk I/O, Network)**을 실시간으로 수집하고,
Zabbix + Grafana + Slack 연동을 통해 이상 상황을 탐지 및 알림하는 모니터링 시스템을 구축한 프로젝트입니다.

### 1주차

VDI 가상환경 VM 3대 구성 (Ubuntu/Windows 혼합)

Zabbix Server 설치 및 DB 연동 구성

Zabbix Agent 설치 및 대상 VM 연결
→ 기본 자원 수집 구조 구현 완료 |

### 2주차

Trigger 설정: CPU/Memory/Network 임계치 경보 조건 생성

Slack Webhook 생성 및 Zabbix 알림 연동

사용자 시나리오 테스트: CPU 90% 이상 시 알림 발생
→ 실시간 경보 체계 작동 확인 |

### 3주차
Grafana 설치 및 Zabbix 데이터소스 연동

VM 리소스 통합 대시보드 구축

사용자 피드백/불만 사례(느림, 지연)와 자원 사용 추이 비교
→ 자원 시각화 및 사용자 이슈 매핑 구조 구현 |

### 4주차

Slack 메시지 템플릿 구성 (Host명, Item, Value 등 포함)

보고서 작성: VM별 리소스 패턴, 병목 구간 분석, 개선 제안

프로젝트 문서화 및 GitHub 정리
→ 운영 보고서 기반 개선 루프 완성 + 포트폴리오 제출형 마감 |

상용 솔루션인 vROPS 없이도, 오픈소스 기반의 자원 추적 및 시각화 시스템을 설계하여
실시간 운영 대응과 사용자 이슈 개선이 가능한 구조를 목표로 했습니다.

## ⚙️ 시스템 구성
Zabbix Server: 자원 수집 및 트리거/알림 설정 담당

Grafana: 시각화 대시보드 (Zabbix 데이터 연동)

Slack Webhook: 이상 감지 시 실시간 알림

VM 대상: Ubuntu 및 Windows VM 다수 구성 (VDI 시뮬레이션)

Zabbix Agent: 각 VM에 설치, 자원 메트릭 전송

## 🛠️ 주요 기능
CPU, 메모리, 디스크, 네트워크 자원 실시간 모니터링

Trigger 설정으로 특정 기준 초과 시 Slack 알림 전송

Grafana 기반 대시보드 시각화 및 히스토리 분석

Slack 메시지 템플릿 구성으로 운영팀 신속 대응

사용자 불만과 자원 병목 간의 상관관계 분석 리포트 작성

## 🧪 핵심 기술 스택
Zabbix 6.x (Server & Agent)

Grafana OSS 10.x

Slack Incoming Webhook

Ubuntu 20.04 / Windows 10 VM

PowerShell / Bash (설정 자동화 일부 포함)

## 📈 결과 및 시사점
vROPS 같은 상용툴 없이도 실시간 자원 관제 및 알림 체계 구축 가능

Slack 알림 및 사용자 로그와 연결하여 사용자 민원 대응 자동화 실현

향후 VM 배포 자동화, GPO 설정 자동화와 연계하여 통합 VDI 운영 플랫폼으로 확장 가능
