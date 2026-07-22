# 안녕하세요, 김혜미입니다 👋

모의해킹(Penetration Testing) 및 악성코드 분석 분야 취업을 목표로 하는 보안 전공자 김혜미입니다.
이론에 머무르지 않고 VMware/VirtualBox 등 가상 환경에서 직접 취약점을 재현·검증하며, 문제가 발생하는 근본 원인을 끝까지 추적하는 것을 가장 중요하게 생각합니다.

**💡 강점**

- 🔍 **근본 원인 분석**: 취약점을 재현하는 데서 그치지 않고 CWE 기준으로 원인을 분류하고, 왜 그 구조가 뚫리는지 논리적으로 설명합니다. (워게임 자체 출제 문제 5종 등)
- ⚖️ **레드팀·블루팀 균형 감각**: 공격자 관점(익스플로잇)과 방어자 관점(탐지·대응)을 함께 프로젝트에 반영해, 공격 흐름을 이해하는 동시에 실효성 있는 탐지 로직을 설계합니다.
- 🧭 **주도적 실행력**: 4~5인 팀 프로젝트에서 팀장/PM 역할을 맡아 인프라 설계부터 발표까지 총괄했고, 팀 자체 제작 워게임·CTF에도 문제 출제자로 직접 참여했습니다.

---

## 🧑‍💻 About Me

- 🎓 서울디지털대학교 컴퓨터공학과 전공 / 경찰학과 복수전공 (2026.02 3년 조기졸업)
- 🛡️ 이스트소프트 [10기] 인프라 보안 부트캠프(국비) 수료 예정
- 🎯 목표: 정보보안기사 취득, 모의해킹 · 악성코드 분석 분야 취업
- 🖥️ VMware / VirtualBox 기반 가상 환경 실습 선호

---

## 🚀 Projects

### 🎯 3차(최종) 프로젝트
> 진행 중 (Coming soon)

### 🏴 워게임
- 팀 자체 제작 워게임에 직접 문제 5개 출제 (Android Pattern Lock, Guide NPC, ALZ 파일 검증기 File Upload, Hidden Keys, Reflected XSS)
- 타 팀 + 멘토 출제 문제 총 100문제 전체 풀이, **팀 순위 2등**
- 워게임 파트 배점 20% **만점 획득**

### 🥇 2차 프로젝트 — Hotel Reservation Security Monitoring System (HRSMS)
> 5인 팀 프로젝트 (팀장/PM) · 2026.06.01 ~ 06.19 · **팀 1등 수상** (10팀 中)

- DMZ / Internal Subzone / SOC 관제망으로 분리된 인프라 설계 및 구축
- **GNS3, pfSense, Suricata**로 경계 방어 및 침입 탐지 체계 구성
- **rsyslog → Graylog** 로그 통합, **GoAccess / PMM**으로 웹·인프라 시각화
- 모의해킹으로 SQL Injection(인증우회), Open Redirection, 세션 고정, Stored XSS, IDOR, SSRF 등 **6건 취약점 발견 및 전건 조치**
- KISA 가이드 기반 67개 항목 점검 → 9건 취약점 발견 후 전건 조치, **최종 양호 67/67 달성**
- cron 기반 보안 점검 자동화 스크립트 운영 (매일 13시 실행)

### 🚩 2차 프로젝트 팀 자체 제작 CTF VM — EasyHajo CTF
> HRSMS와는 별도로, 같은 2차 프로젝트 기간에 팀에서 제작한 CTF 취약 VM

- 팀 자체 제작 취약 VM 머신 & 워크스루: [2nd-project-ctf-vm](./2nd-project-ctf-vm)
- 9개 팀 출제 문제(팀당 User/Root 2플래그, 총 18점) 중 **15점 획득**

### 🏥 1차 프로젝트 — 차세대 통합 병원 정보 시스템 (S-HIS)
> 4인 팀 프로젝트 (팀장) · 2026.04.13 ~ 04.23

- 망 분리(의료진/행정/DB로그/DMZ) 기반 3-Tier 아키텍처 설계
- **IPsec VPN** 및 ACL 보안 정책 수립, 최소 권한 계정 관리
- **LogAnalyzer(rsyslog)** 기반 실시간 침입 탐지(로그인 성공/실패 이벤트 등) 구현

---

## 🛠️ Tools & Skills

**모의해킹 / 진단**
`Burp Suite` `sqlmap` `Nmap` `OWASP ZAP` `Metasploit(msfconsole)` `Wireshark` `Snort`

**악성코드 분석**
`OllyDbg` `PEiD` `PEStudio` `Dependency Walker` `Exeinfo PE` `HxD` `VirusTotal`

**인프라 / 시스템**
`GNS3` `pfSense` `Suricata` `Graylog` `rsyslog` `GoAccess` `PMM`
`Ubuntu / Rocky Linux` `Apache` `MariaDB`

**가상화 환경**
`VMware` `VirtualBox` `Cisco Packet Tracer`

---

## 📫 Contact
- ✉️ Email: h4em22@gmail.com
