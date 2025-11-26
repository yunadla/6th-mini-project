#업무 정의서 (Work Definition) — 세탁실 예약·이용 관리
1. 개요/목표
기숙사/동아리의 세탁기·건조기 사용을 예약 기반으로 관리한다.
예약 충돌 방지, 체크인/노쇼 처리, 기기 고장·점검, 알림/정산(선택)을 장부/목록으로 추적한다.
2. 범위
사용자(학생): 기기·시간대 조회 → 예약/취소 → 현장 체크인/체크아웃 → 내 이용내역 확인
관리자: 기기 등록·상태 변경(정상/고장/점검), 고장 신고 처리, 사용량 통계/로그 조회
스케줄러/알림: 시작 전 리마인드, 미체크인 노쇼 자동 판정, 종료 알림
3. 액터(Actors)
학생(사용자): 예약·이용 주체
관리자(Admin): 기기/정책/로그 관리
스케줄러/알림 서비스: 예약 시간 기반 배치 처리(SMS/푸시)
(선택)시설팀(수리 담당): 고장 접수 시 처리
4. 주요 업무 흐름(End-to-End)
가용성 확인: 사용자가 날짜/기기 유형으로 시간대 조회
예약/취소: 시간대 선택 → ①예약장부에 기록(충돌 방지) / 필요 시 취소
체크인/체크아웃: 시작 전후 허용창 내 체크인 → 기기 상태 IN_USE → 체크아웃 시 사용 종료, ②이용이력장부 기록
노쇼 처리(자동): 시작+X분 경과 & 미체크인 → ③노쇼장부 기록, 패널티(옵션)
고장/점검: 사용자 고장 신고 → 관리자가 확인 후 ④고장신고장부 기록, 기기 상태 BROKEN/MAINT 전환 → ⑤기기점검/수리 이력 업데이트
알림: ⑥알림이력(리마인드/노쇼/고장) 기록
현황/통계: 관리자용 ⑦기기현황목록(상태·위치·이용률), ⑧통계리포트(노쇼율, 피크시간, 고장빈도)






#USECASE
<img width="630" height="791" alt="TPFVQXf15CRlvoaENfaBi_LFOfgB45l82uGym7QT9WkRNT3rgXHCdDZG20qKgQQQ6h2sWIrOOybUs9i-ZdFc7Jfcri4bAuXySxxVdFCTXjsl-cR5hvqwv9Nt1Z9xK79iYy8kd537yGXnw5iVV0ygzl693sMxGYtVzbnYMhvNWHIU1tXpZxVNQT7kOgE_aGAp2aTBUpwjyr6mi4lbKzjLRabV" src="https://github.com/user-attachments/assets/cea18773-85eb-4732-b3f8-c994f3d763ff" />
