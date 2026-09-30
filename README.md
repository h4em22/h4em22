# 안녕하세요, 김혜미입니다 👋

취약점 하나를 발견했을 때, 거기서 멈추지 않습니다.
'왜 이 지점이 공격에 노출됐는가'를 끝까지 추적하는 **김혜미**입니다.

**💡 강점**

- **웹 취약점 11건 직접 모의해킹·실증, CWE 기준 분류**: 2·3차 프로젝트 모의해킹을 직접 맡아 웹 취약점 11건을 실증하고 근본 원인을 CWE로 분류했으며, XSS+Session Fixation 연계로 무인증 관리자 세션 탈취까지 증명했습니다. 워게임 문제 5종도 CWE 유형에 맞춰 직접 출제했습니다.
- **BPFDoor 백도어 동적 분석 → 탐지 권고안 작성**: 매직 패킷 1회로 리버스쉘이 열리는 과정을 격리 환경에서 재현하고, 포트 점검에 안 보이는 백도어를 raw 소켓·프로세스·패킷 레벨에서 직접 찾아내 IDS 시그니처·auditd 감시 권고안까지 작성했습니다.
- **팀 프로젝트 3회 전부 팀장(PM)**: 매번 일정 관리·보고서 작성·최종 발표를 직접 맡아 총괄했고, 2·3차 프로젝트 모두 10팀 중 1등으로 우수상을 받았습니다.

---

## 🧑‍💻 About Me

- 🎓 대학교 컴퓨터공학과 전공 / 경찰학과 복수전공 (2026.02 3년 조기졸업)
- 🛡️ 이스트소프트 [10기] 인프라 보안 부트캠프(국비) 수료 — **우수수료생 선정**
- 🎯 목표: 정보보안기사 취득 (필기 준비 중 2026.10.07 응시), 모의해킹 · 악성코드 분석 분야 취업

---

## 🚀 Projects

### 🥇 3차(최종) 프로젝트 — Operation Follow Me (FM 8+)
> 5인 팀 프로젝트 (팀장) · 2026.07.23 ~ 08.04 · **팀 1등 수상** (10팀 中)
> 🔗 [저장소 바로가기](https://github.com/hyemya/3rd_project)

- 2025년 4월 **S사 HSS 침해사고**(USIM 인증키 평문 저장, 탐지까지 22시간 지연 등)를 근본원인 관점으로 재구성해 가상 통신사 인프라(FM 8+) 설계에 반영
- **pfSense(FW) → Suricata(IDS/IPS) → ModSecurity(WAF) → ELK Stack(SIEM)** 실시간 탐지·차단·통합관제 파이프라인 구축
- Red Team 모의해킹으로 SQL Injection, Session Fixation, Stored XSS, IDOR, Unrestricted File Upload **5건 취약점 발견, 전건(100%) 실증** (Critical 3 · High 2)
- Blue Team 관제 검증: 커스텀 탐지·차단 룰 18종 적용 중 **16종 실제 차단 확인**, SIEM 대시보드로 공격 탐지 전 과정 가시화 및 탐지 사각지대 분석
- KISA 가이드 기반 **U-01~U-67 서버 점검 자동화 스크립트** 직접 개발, 발견된 취약점 9건 **전건 조치(100%)**
- **BPFDoor 기반 리버스쉘 백도어** 정적/동적 분석(Ghidra, VirusTotal, Wireshark, strace)으로 행위·IOC 도출 및 대응방안 수립

### 🏴 워게임
> 🔗 [저장소 바로가기](https://github.com/hyemya/3rd_project_wargame)

- 팀 자체 제작 워게임에 직접 문제 5개 출제 (Android Pattern Lock, Guide NPC, ALZ 파일 검증기 File Upload, Hidden Keys, Reflected XSS)
- 타 팀 + 멘토 출제 문제 총 100문제 전체 풀이, **팀 순위 2등**
- 워게임 파트 배점 20% **만점 획득**

### 🥇 2차 프로젝트 — Hotel Reservation Security Monitoring System (HRSMS)
> 5인 팀 프로젝트 (팀장) · 2026.06.01 ~ 06.19 · **팀 1등 수상** (10팀 中)
> 🔗 [저장소 바로가기](https://github.com/hyemya/2nd_project)

- DMZ / Internal Subzone / SOC 관제망으로 분리된 인프라 설계 및 구축
- **GNS3, pfSense, Suricata**로 경계 방어 및 침입 탐지 체계 구성
- **rsyslog → Graylog** 로그 통합, **GoAccess / PMM**으로 웹·인프라 시각화
- 모의해킹으로 SQL Injection(인증우회), Open Redirection, 세션 고정, Stored XSS, IDOR, SSRF 등 **6건 취약점 발견 및 전건 조치**
- KISA 가이드 기반 67개 항목 점검 → 9건 취약점 발견 후 전건 조치, **최종 양호 67/67 달성**
- cron 기반 보안 점검 자동화 스크립트 운영 (매일 13시 실행)

### 🚩 2차 프로젝트 팀 자체 제작 CTF — EasyHajo CTF
> 🔗 [저장소 바로가기](https://github.com/hyemya/2nd_project_CTF)

- 9개 팀 출제 문제(팀당 User/Root 2플래그, 총 18점) 중 **15점 획득**

### 🏥 1차 프로젝트 — 차세대 통합 병원 정보 시스템 (S-HIS)
> 4인 팀 프로젝트 (팀장) · 2026.04.13 ~ 04.23
> 🔗 [저장소 바로가기](https://github.com/hyemya/1st_project)

- 망 분리(의료진/행정/DB로그/DMZ) 기반 3-Tier 아키텍처 설계
- **IPsec VPN** 및 ACL 보안 정책 수립, 최소 권한 계정 관리
- **LogAnalyzer(rsyslog)** 기반 실시간 침입 탐지(로그인 성공/실패 이벤트 등) 구현

---

## 🏆 Certificates & Awards
> 🔗 [저장소 바로가기](https://github.com/h4em22/certificates)

- [이스트캠프] 가디언즈 정보보호 및 보안 인프라 운영 관리 10기 과정 **우수수료생 선정** (2026.08.07)
- [이스트캠프] 가디언즈 정보보호 및 보안 인프라 운영 관리 10기 과정 **수료증** (2026.08.07)
- 3차(최종) 프로젝트 **우수상** (2026.08.07)
- 워게임 **2등** (2026.07.16)
- 2차 프로젝트 **우수상** (2026.06.22)

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
