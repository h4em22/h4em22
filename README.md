# 안녕하세요, 김혜미입니다 👋

취약점 하나를 발견했을 때, 거기서 멈추지 않습니다.
'왜 이 지점이 공격에 노출됐는가'를 끝까지 추적하는 **김혜미**입니다.

**💡 강점**

- **웹 취약점 11건 직접 모의해킹·실증, CWE 기준 분류**: 2·3차 프로젝트 모의해킹을 직접 맡아 웹 취약점 11건을 실증하고 근본 원인을 CWE로 분류했으며, XSS+Session Fixation 연계로 무인증 관리자 세션 탈취까지 증명했습니다. 워게임 문제 5종도 CWE 유형에 맞춰 직접 출제했습니다.
- **BPFDoor 백도어 동적 분석 → 탐지 권고안 작성**: 매직 패킷 1회로 리버스쉘이 열리는 과정을 격리 환경에서 재현하고, 포트 점검에 안 보이는 백도어를 raw 소켓·프로세스·패킷 레벨에서 직접 찾아내 IDS 시그니처·auditd 감시 권고안까지 작성했습니다.
- **팀 프로젝트 3회 전부 팀장**: 매번 일정 관리·보고서 작성·최종 발표를 직접 맡아 총괄했고, 2·3차 프로젝트 모두 10팀 중 1등으로 우수상을 받았습니다.

---

## 🧑‍💻 About Me

- 🎓 대학교 컴퓨터공학과 전공 / 경찰학과 복수전공 (2026.02 3년 조기졸업)
- 🛡️ 이스트소프트 [10기] 인프라 보안 부트캠프(국비) 수료 — **우수수료생 선정**

---

## 🚀 Projects

### 🥇 3차(최종) 프로젝트 — Operation Follow Me (FM 8+)
> 5인 팀 프로젝트 (팀장) · 2026.07.23 ~ 08.04 · **팀 1등 수상** (10팀 中)
> 🔗 [View Repository](https://github.com/hyemya/3rd_project)

- **개요**: 2025년 4월 S사 HSS 침해사고를 근본 원인 관점으로 재구성해, 가상 통신사 인프라(FM 8+)를 대상으로 모의해킹(Red Team)과 보안 관제(Blue Team)를 수행한 정보보호 진단 프로젝트
- **담당**: 모의해킹 수행, BPFDoor 동적 분석, 전체 일정·보고서·발표 총괄
- OWASP Top 10 기반 SQL Injection, Session Fixation, Stored XSS, IDOR, Unrestricted File Upload **5건 선정 및 전건(100%) 실증**, CWE 기준 근본 원인 분석 (Prepared Statement 미적용, `session_regenerate_id` 누락, 출력 인코딩 부재, 인가 검증 부재, 서버측 파일 검증 부재)
- **Session Fixation + Stored XSS 공격 체인**으로 무인증 관리자 세션 탈취 실증 → 개별 취약점보다 연계 시 피해가 증폭됨을 증명
- **BPFDoor 동적 분석**: VirtualBox 격리망(피해자 Ubuntu / 공격자 Kali, 스냅샷 확보)에서 백도어 행위 재현·탐지 검증
  - `AF_PACKET`/`SOCK_RAW`로 리스닝 포트 없이 잠복하는 구조 확인, Scapy로 TCP 옵션을 제거해 페이로드 오프셋을 54바이트로 고정한 매직 패킷 1회 전송으로 root 리버스쉘 획득 재현
  - `ss -tlnp`/`netstat`에는 안 잡히는 백도어를 `ss -0pb`(raw 소켓)·`ps`·tcpdump/Wireshark(매직 바이트 `MAGIC`)·strace(시스템콜 흐름)로 탐지 — 포트 점검의 사각지대를 소켓·프로세스·트래픽·시스템콜 레벨에서 보완
  - 대응 권고안 작성: IDS 시그니처(`content:"MAGIC"; offset:54;`), auditd/eBPF raw 소켓 생성 감시, IoC 해시 기반 YARA 주기 스캔, 최소 권한 원칙

### 🏴 워게임
> 🔗 [View Repository](https://github.com/hyemya/3rd_project_wargame)

- 팀 워게임 10문제 중 **Problem 05~09, 5문제 직접 설계·출제** — 각 문제를 실제 CWE 유형에 대응하도록 설계
  - Android Pattern Lock · Guide NPC 쿠키 변조 · ALZ 파일 검증기 · Hidden Keys LSB 스테가노그래피 · Reflected XSS 클라이언트 검증 우회
- 타 팀 + 멘토 출제 문제 총 100문제 전체 풀이, **팀 순위 2등**
- 워게임 파트 배점 20% **만점 획득**

### 🥇 2차 프로젝트 — Hotel Reservation Security Monitoring System (HRSMS)
> 5인 팀 프로젝트 (팀장) · 2026.06.01 ~ 06.19 · **팀 1등 수상** (10팀 中)
> 🔗 [View Repository](https://github.com/hyemya/2nd_project)

- **개요**: 호텔 예약 웹 서비스를 대상으로 경계 방어·로그 통합 관제 인프라를 구축하고, 모의해킹으로 취약점을 진단한 보안 관제 프로젝트
- **담당**: 취약점 설계·모의해킹, PMM 구축, 전체 일정 관리·보고서·발표
- 모의해킹으로 SQL Injection(인증우회), Open Redirection, Session Fixation, Stored XSS, IDOR, SSRF **6건 발견·근본 원인 분석 후 전건 조치·재검증** — 매개변수화 질의(Prepared Statement), 로그인 시 세션 재발급, HTML 엔티티 인코딩, 소유자 기반 인가 검증, URL 스킴·도메인 화이트리스트 적용
- 공통 근본 원인을 "클라이언트 입력을 신뢰한 설계"(입력 검증·출력 인코딩·인가 검증 누락)로 정리하고 **모의해킹 결과보고서·시스템 점검보고서 직접 작성**
- KISA 가이드 U-01~U-67 서버 점검을 **직접 실행해 취약 9건 전건 조치 → 최종 양호 67/67 달성** (점검·조치·보고서 담당)
- **PMM(Percona Monitoring)** 구축으로 DB·인프라 성능 관제

### 🚩 2차 프로젝트 팀 자체 제작 CTF — EasyHajo CTF
> 🔗 [View Repository](https://github.com/hyemya/2nd_project_CTF)

- **출제(환경 구축 담당)**: 팀이 공동 설계한 EasyHajo 취약 VM의 환경 구축을 맡아 초기 침투부터 root 권한 획득까지 이어지는 5단계 시나리오 구현 — 백업 파일(`upload.php.bak`) 노출 → 쿠키 검증 우회(Burp Intruder 무차별 대입) → 파일 업로드 웹쉘 → `helper.php` OS 커맨드 인젝션 → NOPASSWD sudo 오용으로 Root
- **풀이(대회 참가)**: 본인 팀 문제를 제외한 9개 팀 출제 문제(팀당 User/Root 2플래그, 총 18점) 중 **15점 획득**

### 🏥 1차 프로젝트 — 차세대 통합 병원 정보 시스템 (S-HIS)
> 4인 팀 프로젝트 (팀장) · 2026.04.13 ~ 04.23
> 🔗 [View Repository](https://github.com/hyemya/1st_project)

- **개요**: 망 분리 기반 3-Tier 구조의 병원 정보 시스템을 설계·구축하고, 접근 통제·로그 관제로 보안을 적용한 인프라 구축 프로젝트
- **담당**: 인프라 아키텍처 및 로그 엔지니어링, 프로젝트 총괄
- 망 분리(의료진/행정/DB로그/DMZ) 기반 3-Tier 구조 설계 주도
- Apache–MariaDB 연동: DB 접근을 Web 서버 IP의 SELECT/INSERT로만 허용, admin/doctor/medical 계정 분리로 **최소 권한 원칙** 적용
- **rsyslog 기반 LogAnalyzer** 로그 서버 구축: WEB/DB/VPN/방화벽 로그 통합, 로그인 성공(INFO)/실패(WARNING) 구분 및 5회 실패 시 ALERT 자동 생성
- 관리자/의료진 **권한(u_group) 기반 접근 제어** 로그인과 실시간 모니터링 대시보드(접속 IP·활성 사용자 수·강제 로그아웃) 구현
- DNS 구축, LogAnalyzer–포털 연동, UI/UX 디자인 및 발표

---

## 🏆 Certificates & Awards
> 🔗 [View Repository](https://github.com/h4em22/certificates)

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
