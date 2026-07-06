# Re:Deum

운동 전 30분, 멈춘 사람을 움직이는 서비스.
PT 등록해놓고 침대에서 안 나가는 사람을, 30분 전 리마인드 + GPS 도착 체크인으로 실제 운동 장소까지 데려간다.

## 구성
순수 정적 사이트(HTML/CSS/JS 한 파일)입니다. 빌드 과정이 없습니다.

- `index.html` — 앱 전체
- `manifest.json` — PWA 설정 (홈 화면 추가 시 아이콘·이름)
- `icon-192.png` / `icon-512.png` / `icon-maskable-512.png` — 앱 아이콘
- `vercel.json` — Vercel 배포 설정

## 로컬에서 확인
그냥 `index.html`을 브라우저로 열면 됩니다. (단, 위치 권한은 `https` 또는 `localhost`에서만 정상 동작)

## 배포 (Vercel)
1. 이 저장소를 GitHub에 올린다
2. vercel.com에서 New Project → 이 GitHub 저장소 선택 → Deploy
   (Framework Preset: **Other**, Build Command 비워둠 — 정적 파일이라 별도 빌드 불필요)
3. 배포 URL로 접속 후 아이폰 사파리 → 공유 → "홈 화면에 추가"

## 데이터 저장
현재는 브라우저 `localStorage` 기반입니다. 기기를 바꾸거나 브라우저 데이터를 지우면 초기화됩니다.
추후 여러 기기 동기화가 필요하면 Supabase 연동 단계로 넘어갑니다.
