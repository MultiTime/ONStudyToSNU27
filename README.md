# ONStudyToSNU27
📜 Version History & Release Notes (v1.0 ~ v14.2)
v1.0 🌱 프로젝트의 시작 (Initial Setup) 
바닐라 HTML/CSS/JS를 활용하여 단순한 형태의 스터디 플래너와 실시간 시계 타이머 기능을 갖춘 기본 웹페이지 레이아웃 구조 설계 및 배포

v2.0 📚 문제집 & 할 일 관리 (Task & Library) 
JS 객체 배열을 활용해 문제집의 챕터별 진도율을 백분율(%)로 계산하는 Progress Bar 시각화 적용, 매일의 할 일(To-Do) 체크박스 상태 토글 로직 구현

v3.0 ⏱️ 모트모트 타임테이블 (Timetable) 
오전 6시부터 다음 날 새벽 6시까지 10분 단위(144칸)로 드래그 앤 드롭(onmousedown, onmouseenter)하여 색상을 채울 수 있는 세로형 타임테이블(Grid) UI 구축

v4.0 ☁️ 파이어베이스 연동 (Cloud Database) 
Firebase Firestore 데이터베이스를 연동. onSnapshot 메서드를 활용한 실시간 동기화(Real-time Sync)를 통해 기기 변경이나 새로고침 시에도 데이터 무결성 유지

v5.0 🏛️ 캠퍼스 성장 위젯 (Campus Evolution) 
학습 시간에 비례해 경험치(XP)와 레벨(Lv)이 오르는 RPG 시스템 도입. 레벨업 구간에 맞춰 서울대 샤 관문, 나무, 야경 모드 등 CSS 스타일 클래스가 동적으로 변환되는 위젯 추가

v6.0 📱 열품타 단축어 동기화 (YPT Sync) 
아이폰 '단축어(Shortcuts)' 앱의 API 통신을 활용하여, 열품타(YPT) 앱의 실제 공부 시간(HH:MM:SS)을 파이어베이스 ypt_time 필드에 쏘고 이를 웹에서 초(Seconds) 단위로 변환해 자동 XP 획득하는 시스템 구축

v7.0 📅 달력 기록 시스템 (Calendar History) 
JavaScript Date 객체를 활용해 매월 동적으로 생성되는 달력 구현. 매일의 최종 달성 레벨과 공부 시간을 calendarHistory JSON에 누적 저장하는 히스토리 로직 추가

v8.0 🌅 일일 자동 초기화 (5AM Daily Reset) 
일반적인 자정(00시) 리셋 대신, 올빼미 학습 패턴을 고려해 새벽 5시를 기준으로 lastDate를 판별하고 플래너와 타임테이블을 비워주는 checkDailyReset() 로직 알고리즘 구현

v9.0 ✨ UI 폴리싱 (Design Polish) 
화면 배경에 떠다니는 애니메이션 도형 배치. 유리 질감을 살린 Glassmorphism 패널 디자인과 Pretendard 폰트, 반응형 모달(Modal) 창 애니메이션을 도입하여 모던 웹 디자인 규격 완성

v10.0 📐 황금 비율 레이아웃 (Golden Ratio Grid) 
CSS Grid를 활용해 대시보드의 좌/중/우 3단 패널 비율을 [4 : 2.6 : 4.2]의 황금 비율로 미세 조정하여 시각적 밸런스 및 컴포넌트 간 간섭(Overflow) 현상 해결

v10.1 🚑 긴급 데이터 복구 스크립트 (Data Rescue) 
초기 버전에서 발생한 '데이터 덮어쓰기 사고'로 유실된 17~19일의 캘린더 데이터를 강제로 주입(setDoc)하여 살려내는 하드코딩 복구 스크립트 긴급 배포

v10.2 🧹 복구 스크립트 제거 (Clean Up) 
과거 데이터가 안전하게 DB에 정착된 것을 확인한 후, 보안 및 코드 최적화를 위해 불필요해진 임시 복구 버튼과 주입 코드를 완전히 제거

v10.3 🔍 미니멀 위젯 최적화 (Bold Stats & No Comment) 
UI 공간 효율을 위해 불필요한 코멘트 입력창 삭제. 상단 위젯(DATE, D-DAY, TOTAL TIME)의 타이포그래피 크기를 1.4rem으로 대폭 키우고 폰트 웨이트를 조정해 시인성 극대화

v10.4 👻 유령 데이터 박멸 (Time Sync Fix) 
사용자가 '초기화(Reset)' 버튼을 눌렀을 때, 로컬 데이터만 지워지고 아이폰 단축어가 쏜 DB 상단의 ypt_time 껍데기가 남아 무한 부활하는 현상(Ghosting)을 서버 단 덮어쓰기로 완벽 차단

v10.5 🔗 단일 진실 공급원 (Single Source of Truth) 
플래너 패널과 달력 패널이 서로 다른 시간 변수를 참조하여 발생하는 데이터 불일치 해결. 모든 시간 표시가 오직 calendarHistory 데이터만을 참조하도록 아키텍처 일원화

v11.0 📱 반응형 웹 최적화 (Tablet Optimization) 
태블릿 및 소형 디스플레이(1300px, 1024px 이하) 환경에서 가로 스크롤바가 생기고 패널이 깨지는 현상 해결. CSS Media Queries를 적용해 폰트, 여백, 그리드 간격을 동적으로 축소하는 반응형 렌더링 적용

v11.1 🛡️ 완벽한 새벽 5시 리셋 (Perfect 5AM Reset) 
새벽 5시 일일 리셋이 동작할 때, 서버에 남아있는 전날의 ypt_time 찌꺼기를 강제로 "00:00:00"으로 초기화하고, 갱신된 단축어 시간을 즉시 캘린더 히스토리로 병합(Merge)하는 무결성 패치

v12.0 💊 데이터 자가 치유 (Self-Healing Sync) 
서버 최상단의 ypt_time과 calendarHistory 내부의 시간이 엇갈렸을 때, 코드가 스스로 최상단 시간을 정답으로 간주하고 내부 JSON 찌꺼기를 알아서 덮어쓰며 고치는 자가 치유 알고리즘 적용

v12.1 💾 백업 & 복원 시스템 (Backup & Restore) 
DB 사고에 대비한 궁극의 안전장치 도입. 현재 상태의 전체 JSON 트리를 복사하여 파이어베이스 내 backup_data 컬렉션에 스냅샷으로 보관하고, 필요시 덮어쓰는 구조 설계

v12.2 🚫 레이스 컨디션 1차 방어 (Anti-Race Condition) 
복원 버튼을 누르는 찰나의 순간, 켜져 있던 파이어베이스 실시간 감지 센서(onSnapshot)가 예전 화면 데이터를 다시 DB로 쏴버려 복원 데이터를 오염시키는 충돌 현상 발견. 복원 직전 unsubSnapshot()을 호출해 센서를 강제 차단

v12.3 🔒 철벽 방어막 적용 (Ironclad Restore) 
복원 프로세스가 진행되는 짧은 시간 동안 타이머 기반의 자동 저장 로직(saveTimeoutTT)이 개입하지 못하도록, 전역 상태 변수 isRestoring을 도입해 saveDataToCloud의 실행을 원천 봉쇄

v12.4 ⚡ 즉각 렌더링 시도 (No-Reload Attempt) 
복원 직후 location.reload() 시 브라우저가 통신을 끊어버리는 네트워크 증발 현상을 막기 위해, 새로고침 없이 로컬 메모리(appData)만 교체하여 화면을 즉시 갈아끼우는 DOM 리렌더링 최적화 도입

v12.5 ⏳ 시간 역주행 방지 (Anti-Downgrade) 
복원 데이터가 덮어씌워질 때 로직이 꼬여 공부 시간이 0초로 깎이는 치명적 버그 수정. 새로 들어오는 시간이 기존 달력 시간보다 '클 때(Upgrade)'만 덮어쓰도록 incomingCalSec > existingCalSec 안전장치 로직 추가

v12.6 🕰️ 타임머신 버그 보정 (Anti-Reset Lock) 
과거(예: 18일)의 백업 데이터를 불러오면, 코드가 '어제 데이터'로 인식해 복원 즉시 새벽 5시 리셋을 발동시키는 모순 발생. 복원 직전 backupData.lastDate를 오늘 날짜로 강제 변환하여 리셋 발동을 회피하는 트릭 적용

v14.0 🚦 실행 순서 완전 교정 (Execution Order Fix) 
복원 후 0.2초 만에 화면이 다시 초기화되는 충격적 버그 수정. DB에서 데이터를 끌어오기 전에 시간 동기화 함수가 텅 빈 appData를 저장해 버리는 '자폭(Self-Destruct)' 현상을 막기 위해, 데이터를 메모리에 할당하는 순서를 최상단으로 재배치

v14.1 🔄 렌더링 무결성 개선 (Instant Render Final) 
백그라운드에서 복원 데이터를 서버로 안전하게 넘기고 로컬을 동기화하는 비동기(async/await) 처리 로직 강화. 로딩 스크린 오버레이를 고도화하여 사용자 조작을 물리적으로 차단

v14.2 👑 진정한 마스터 빌드 (The Real Final - By Minchan) 
복원 시 Firebase 내부 캐시 꼬임과 실시간 센서 재시작 과정에서 발생하는 잔상 버그를 완벽히 통제하기 위해, 유저(개발자)가 직접 강제 새로고침(window.location.reload())을 최적의 타이밍에 복구. 전역 상태 isAfterRestore 플래그를 추가하여 복원 직후의 엉뚱한 동기화를 완벽히 억제한 궁극의 최종 버전
