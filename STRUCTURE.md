# STRUCTURE — 한입당 (HANNIPDANG)

춘천 가연길 마카롱·디저트 카페 실고객 시안. 단일 HTML 원페이지.

```
/ (배포 루트, CF [assets] directory="./")
├─ index.html            단일 파일 (인라인 CSS/JS, 한글 위주)
├─ hp-logo.png           하트 마스코트 로고 (헤더·히어로·푸터·파비콘)
├─ favicon.png           연분홍 배경 패딩 파비콘 (180px)
├─ og-hannipdang.jpg     OG 썸네일 1200×630 (히어로 박스세트 크롭)
├─ hp-hero.webp          빨간 리본 디저트 선물박스 (히어로)
├─ hp-cup-strawberry.webp 딸기 크림 컵 디저트 (소개)
├─ hp-ott-caramel.webp   캐러멜 뚱카롱 (시그니처 01)
├─ hp-dubai.webp         두바이 디저트 (시그니처 02)
├─ hp-gift-bouquet.webp  마카롱 꽃다발 (시그니처 03)
├─ hp-ott-orange.webp    오렌지크림 뚱카롱 단면 (갤러리)
├─ hp-ott-strawberry.webp 딸기크림 뚱카롱 (갤러리)
├─ hp-ott-redvelvet.webp 레드벨벳 하트 마카롱 (갤러리, 세로 span)
├─ hp-ott-rainbow.webp   무지개 마카롱 (갤러리)
├─ hp-ott-oreo.webp      오레오 뚱카롱 (갤러리)
├─ hp-gift-box.webp      리본 마카롱 선물박스 (오시는길)
├─ wrangler.toml         name=hannipdang-sample, [assets] ./
├─ .assetsignore         .git·문서·img·_qa 제외
├─ CHANGELOG.md / STRUCTURE.md
└─ img/                  원본 202장 + logo.png + slug webp 사본 (배포 제외)
```

## 섹션 앵커
`#top` 히어로 · `#intro` 소개 · `#signature` 시그니처 3카드 · `#gallery` 갤러리 5장 · `#howto` 쫀득 베이글샌드 먹는법 · `#visit` 오시는길 · `#channels` 채널

## 디자인 (소프트 감성 미니멀 큐트)
- **팔레트**: 연분홍 바탕 `--blush #FCEDF0` · 살짝 진한 섹션 `--blush-deep #F7DCE3` · 크림 카드 `#FFFAFB` · 기본 진분홍 `--pink #E58BA5`/`--pink-deep #D96A8A` · **포인트 빨강 `--red #D6231F`(로고 하트, AA 보정)** · 잉크 플럼 `#3A2930` · 푸터 로즈 `--foot #A82F59`.
- **폰트(시안=CDN)**: Gowun Batang(고운바탕, 헤딩 소프트 명조) + Gaegu(개구, 손글씨 키커·포인트) + Pretendard(본문). ⚠️납품 시 사용 글리프 서브셋 self-host 전환 예정.
- 넉넉한 여백, 라운드 코너(22~34px), 소프트 그림자, 살짝 기울인 사진 프레임(rotate), 하트 마스코트 bob 애니메이션.
- 강제 리빌(IntersectionObserver + 2.6s 타임아웃 + noscript 폴백), rAF 강제 스무스 앵커 스크롤(헤더 오프셋 70px).

## ⚠️ 교체/확인 대상 (납품 전)
- **베이글샌드 실물 사진 없음**: 제공된 IG 원본 202장에 쫀득 베이글샌드(신상) 단면컷이 없어 `#howto`를 텍스트 단계로 구성. 사장님께 단면/실물 사진 받으면 시그니처 카드 또는 howto에 사진 추가 권장.
- **영업시간**: 종료 19:00만 확보(오픈 시각·요일별 미확보, 네이버 펼쳐보기 가려짐). 실제 오픈 시각 확정 시 Visit·푸터 갱신.
- **네이버 place**: 링크 place ID 1693771707 사용. 확인 필요.
- **도메인/OG**: og:image·favicon 상대경로. 실배포 도메인 확정 시 canonical/og 절대경로 필요 시 치환.
- **폰트**: 현재 Google Fonts + jsDelivr Pretendard CDN(시안). 납품 시 self-host + 서브셋(jsDelivr CF 이슈 회피).
