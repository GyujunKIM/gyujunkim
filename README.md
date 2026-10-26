<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="description" content="김규준 포트폴리오 — 디지털 마케팅, 플랫폼 운영, 크리에이터 계약, 이벤트·MD 기획">
<meta name="theme-color" content="#2946df">
<title>김규준 | Portfolio</title>

<style>
:root {
  --blue: #2946df;
  --ink: #18202f;
  --muted: #626b7a;
  --light: #f4f5fa;
  --line: #e2e5ee;
  --white: #fff;
}
* { box-sizing: border-box; }
html { scroll-padding-top: 85px; }
body {
  margin: 0;
  color: var(--ink);
  background: var(--white);
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI",
    "Apple SD Gothic Neo", "Malgun Gothic", sans-serif;
  line-height: 1.75;
  overflow-wrap: anywhere;
}
a { color: inherit; }
button, a { -webkit-tap-highlight-color: transparent; }
a:focus-visible {
  outline: 3px solid var(--blue);
  outline-offset: 5px;
}
h1, h2, h3, p, figure, blockquote { margin: 0; }
h1, h2, h3 { line-height: 1.3; word-break: keep-all; }
.container { width: min(1160px, calc(100% - 48px)); margin: auto; }
.accent { color: var(--blue); }
.eyebrow {
  color: var(--blue);
  font-size: 12px;
  font-weight: 700;
  letter-spacing: .08em;
  margin-bottom: 12px;
}
.section { padding: 96px 0; }
.section-title { margin-bottom: 40px; }
.section-title h2 { font-size: 40px; letter-spacing: -.04em; }
.section-title > p:last-child { color: var(--muted); margin-top: 16px; }
.skip {
  position: absolute;
  left: 16px;
  top: -100px;
  padding: 12px;
  background: white;
  z-index: 100;
}
.skip:focus { top: 12px; }

.nav {
  position: sticky;
  top: 0;
  z-index: 20;
  background: rgba(255,255,255,.97);
  border-bottom: 1px solid var(--line);
}
.nav-inner {
  min-height: 64px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 24px;
}
.logo {
  display: inline-flex;
  gap: 10px;
  align-items: center;
  text-decoration: none;
  font-weight: 750;
  white-space: nowrap;
}
.logo-mark {
  background: var(--blue);
  color: white;
  border-radius: 7px;
  padding: 3px 6px;
  font-size: 12px;
}
.nav-links { display: flex; gap: 26px; }
.nav-links a { font-size: 14px; text-decoration: none; }

.hero {
  padding-top: 88px;
  padding-bottom: 96px;
  display: grid;
  grid-template-columns: 1.5fr 1fr;
  gap: 72px;
  align-items: center;
}
.hero h1 {
  font-size: clamp(36px, 4.2vw, 58px);
  font-weight: 800;
  letter-spacing: -.06em;
}
.hero-description {
  max-width: 650px;
  color: var(--muted);
  font-size: 18px;
  margin: 28px 0 24px;
}
.chips, .tags { display: flex; flex-wrap: wrap; gap: 8px; }
.chip, .tag {
  display: inline-block;
  border-radius: 999px;
  font-size: 12px;
  padding: 5px 12px;
  background: var(--light);
}
.tag { color: var(--blue); background: #edf0ff; }
.button {
  display: inline-block;
  margin-top: 28px;
  border-radius: 999px;
  background: var(--blue);
  color: white;
  padding: 12px 22px;
  text-decoration: none;
  font-size: 14px;
  font-weight: 700;
}
.hero-aside {
  display: grid;
  gap: 16px;
  padding: 30px;
  background: var(--light);
  border-radius: 28px;
}
.stat {
  background: white;
  border: 1px solid var(--line);
  border-radius: 14px;
  padding: 24px;
}
.stat strong { display: block; font-size: 28px; letter-spacing: -.04em; }
.stat span { font-size: 13px; color: var(--muted); }

.projects { background: var(--light); }
.project-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 24px;
}
.project-card {
  border-radius: 14px;
  overflow: hidden;
  background: white;
  border: 1px solid var(--line);
}
.project-card > a {
  display: flex;
  flex-direction: column;
  min-height: 100%;
  text-decoration: none;
}
.project-card > a:hover h3 { color: var(--blue); }
.card-cover {
  min-height: 172px;
  padding: 24px;
  background: #e8ecff;
  color: var(--blue);
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.card-cover .number { font-size: 12px; }
.card-cover strong { font-size: 38px; line-height: 1.1; letter-spacing: -.04em; }
.card-cover small { font-size: 12px; margin-top: 8px; display: block; }
.card-cover.neutral { background: #edf0f5; color: #344056; }
.card-body { padding: 24px; flex: 1; display: flex; flex-direction: column; }
.card-body h3 { font-size: 19px; margin-bottom: 14px; }
.card-body p { color: var(--muted); font-size: 14px; margin-bottom: 20px; }
.card-body .date { font-size: 12px; margin-bottom: 8px; }
.card-body .tags { margin-top: auto; }

.marquee {
  overflow: hidden;
  white-space: nowrap;
  font-weight: 850;
  letter-spacing: -.05em;
  font-size: clamp(36px, 7vw, 88px);
  padding: 22px 0;
  line-height: 1.2;
  border-bottom: 1px solid var(--line);
}
.marquee span { color: var(--blue); margin: 0 32px; }
.columns { display: grid; grid-template-columns: 1fr 1fr; gap: 64px; }
.cv-heading {
  color: var(--blue);
  font-size: 12px;
  padding-bottom: 14px;
  margin-top: 28px;
  border-bottom: 1px solid var(--line);
}
.cv-heading:first-child { margin-top: 0; }
.cv-row { padding: 22px 0; border-bottom: 1px solid var(--line); }
.cv-top { display: flex; justify-content: space-between; gap: 16px; }
.cv-top h3 { font-size: 17px; }
.cv-top span { flex-shrink: 0; font-size: 12px; color: var(--muted); }
.cv-row p { margin-top: 8px; font-size: 15px; color: var(--muted); }
.skills { margin-top: 22px; }
.about { background: var(--light); }
.about blockquote {
  font-size: 30px;
  font-weight: 750;
  line-height: 1.5;
  letter-spacing: -.04em;
  word-break: keep-all;
}
.about-copy p { color: var(--muted); margin-bottom: 22px; }
.about-copy h3 { color: var(--blue); font-size: 12px; margin: 30px 0 12px; }
.contact h2 {
  font-size: clamp(36px, 6vw, 72px);
  letter-spacing: -.06em;
  margin-bottom: 18px;
}
.contact .intro { font-size: 18px; color: var(--muted); }
.email {
  display: inline-block;
  color: var(--blue);
  font-size: clamp(18px, 3vw, 26px);
  margin-top: 30px;
  text-underline-offset: 6px;
}

.cases { border-top: 1px solid var(--line); }
.case {
  padding: 72px 0;
  border-top: 1px solid var(--line);
  scroll-margin-top: 90px;
}
.case:first-of-type { border-top: 0; padding-top: 8px; }
.case h3 {
  font-size: clamp(26px, 4vw, 42px);
  letter-spacing: -.05em;
  max-width: 900px;
}
.case .subtitle { color: var(--muted); font-size: 18px; margin: 18px 0 28px; }
.meta {
  display: grid;
  grid-template-columns: repeat(4, minmax(0, 1fr));
  gap: 20px;
  padding: 24px;
  margin: 0 0 36px;
  background: var(--light);
  border-radius: 14px;
}
.meta dt { color: var(--muted); font-size: 12px; margin-bottom: 6px; }
.meta dd { margin: 0; font-size: 14px; }
.case-columns {
  display: grid;
  grid-template-columns: .8fr 1.2fr;
  gap: 56px;
}
.case-label { color: var(--blue); font-size: 12px; margin-bottom: 14px; }
.background-copy { color: var(--muted); margin-bottom: 22px; }
.work-list { padding-left: 24px; margin: 0; }
.work-list li { padding: 0 0 16px 8px; }
.work-list li::marker { color: var(--blue); font-size: 13px; }
.back {
  display: inline-block;
  color: var(--blue);
  font-size: 13px;
  text-underline-offset: 4px;
  margin-top: 32px;
}
footer { border-top: 1px solid var(--line); padding: 24px 0; }
.footer-inner {
  display: flex;
  justify-content: space-between;
  gap: 20px;
  color: var(--muted);
  font-size: 12px;
}

@media (max-width: 1000px) {
  .hero { gap: 32px; }
  .hero-aside { padding: 20px; }
  .project-grid { grid-template-columns: repeat(2, minmax(0, 1fr)); }
  .columns { gap: 36px; }
  .cv-top { flex-direction: column; gap: 6px; }
  .meta { grid-template-columns: repeat(2, minmax(0, 1fr)); }
}
@media (max-width: 640px) {
  .container { width: calc(100% - 36px); }
  .nav-inner { min-height: 64px; gap: 12px; flex-wrap: wrap; padding: 12px 0; }
  .nav-links { gap: 14px; }
  .nav-links a { font-size: 12px; }
  .section { padding: 64px 0; }
  .hero { grid-template-columns: 1fr; padding-top: 56px; padding-bottom: 64px; }
  .hero-description { font-size: 16px; }
  .hero-aside { gap: 10px; }
  .stat { padding: 18px; }
  .stat strong { font-size: 24px; }
  .project-grid, .columns, .case-columns { grid-template-columns: 1fr; }
  .section-title h2 { font-size: 32px; }
  .card-cover { min-height: 150px; }
  .about blockquote { font-size: 26px; }
  .case { padding: 52px 0; }
  .case-columns { gap: 28px; }
  .meta { padding: 18px; gap: 20px 14px; }
  .footer-inner { flex-direction: column; gap: 6px; }
}
</style>
</head>

<body id="top">
<a class="skip" href="#main">본문으로 바로가기</a>

<header class="nav">
  <div class="container nav-inner">
    <a class="logo" href="#top"><span class="logo-mark">GK</span>김규준</a>
    <nav class="nav-links" aria-label="주요 메뉴">
      <a href="#projects">프로젝트</a>
      <a href="#resume">이력</a>
      <a href="#about">소개</a>
      <a href="#contact">연락처</a>
    </nav>
  </div>
</header>

<main id="main">
  <section class="container hero" aria-labelledby="hero-title">
    <div>
      <p class="eyebrow">Marketer · Creator Ops · Platform Planning</p>
      <h1 id="hero-title">
        사람의 반응을 읽고,<br>
        <span class="accent">콘텐츠와 기획으로</span><br>
        연결합니다.
      </h1>
      <p class="hero-description">
        마케팅팀에서 브랜드·행사 마케팅을 했고, 지금은 AI 콘텐츠 플랫폼
        젠잇(Genit)에서 사이트 운영, 크리에이터 계약, 이벤트,
        MD 디자인을 맡고 있습니다.
      </p>
      <div class="chips">
        <span class="chip">디지털 마케팅</span>
        <span class="chip">플랫폼 운영</span>
        <span class="chip">크리에이터 계약</span>
        <span class="chip">이벤트 기획</span>
        <span class="chip">MD·굿즈 디자인</span>
      </div>
      <a class="button" href="#projects">작업 보기 →</a>
    </div>
    <aside class="hero-aside" aria-label="주요 경험">
      <div class="stat"><strong>genit.ai</strong><span>AI 콘텐츠 플랫폼 운영</span></div>
      <div class="stat"><strong>10곳</strong><span>브랜드·기업 마케팅</span></div>
      <div class="stat"><strong>M/V 조감독</strong><span>전시 작가 데뷔</span></div>
    </aside>
  </section>

  <section class="section projects" id="projects">
    <div class="container">
      <header class="section-title">
        <p class="eyebrow">Selected Work</p>
        <h2>프로젝트</h2>
        <p>플랫폼 운영과 브랜드 마케팅, 두 현장에서 한 일을 모았습니다.</p>
      </header>

      <div class="project-grid">
        <article class="project-card">
          <a href="#genit">
            <div class="card-cover">
              <span class="number">01</span>
              <div><strong>genit.ai</strong><small>AI 콘텐츠 플랫폼</small></div>
            </div>
            <div class="card-body">
              <p class="date">젠잇 · 현재</p>
              <h3>젠잇 사이트 운영</h3>
              <p>AI 콘텐츠 플랫폼 젠잇의 이벤트 페이지와 공지를 관리하고, 작품별 구글 광고 문구와 플랫폼 태그라인을 작성했습니다. 크리에이터와 이용자 문의 대응까지 서비스 운영 전반을 맡고 있습니다.</p>
              <div class="tags"><span class="tag">플랫폼 운영</span><span class="tag">광고·카피</span></div>
            </div>
          </a>
        </article>

        <article class="project-card">
          <a href="#contracts">
            <div class="card-cover">
              <span class="number">02</span>
              <div><strong>2–30%</strong><small>계약 유형별 정산율</small></div>
            </div>
            <div class="card-body">
              <p class="date">젠잇 · 2026.07 – 08</p>
              <h3>크리에이터 계약·지원 체계 개편</h3>
              <p>채팅 수 기반이던 크리에이터 지원 프로그램을 정산율 중심의 '젠잇 퍼블리싱' 체계로 바꿨습니다. 비독점·독점·퍼블리싱 계약별 정산율과 파트너·일반 계약의 수수료 구조를 정리하고, 크리에이터별 계약 안내와 정산을 맡았습니다.</p>
              <div class="tags"><span class="tag">계약 구조 설계</span><span class="tag">정산</span></div>
            </div>
          </a>
        </article>

        <article class="project-card">
          <a href="#goods">
            <div class="card-cover">
              <span class="number">03</span>
              <div><strong>20종</strong><small>캐릭터 스페셜 포토카드</small></div>
            </div>
            <div class="card-body">
              <p class="date">젠잇 · 2026</p>
              <h3>이벤트·굿즈 기획</h3>
              <p>플랫폼 리뷰 이벤트, SF 작품 '언노운' 굿즈 이벤트, 대학 연계 원데이 클래스를 기획·운영했습니다. 작품 '강호일통'의 캐릭터 스페셜 포토카드 20종과 브랜드 봉투, 형압 박 감사 카드 등 굿즈와 인쇄물도 직접 디자인했습니다.</p>
              <div class="tags"><span class="tag">이벤트 기획</span><span class="tag">MD 디자인</span></div>
            </div>
          </a>
        </article>

        <article class="project-card">
          <a href="#fiska">
            <div class="card-cover neutral"><span class="number">04</span><strong>FISKA</strong></div>
            <div class="card-body">
              <h3>FISKA by LAFIANO</h3>
              <p>그랜드 오픈 마케팅 제안, 1억 원 규모 예산안 수립<br>오픈 기념 [옥상 천문대] 프로모션 기획·결과 보고</p>
              <div class="tags"><span class="tag">오프라인 행사</span><span class="tag">예산 기획</span></div>
            </div>
          </a>
        </article>

        <article class="project-card">
          <a href="#parnas">
            <div class="card-cover neutral"><span class="number">05</span><strong>PARNAS MALL</strong></div>
            <div class="card-body">
              <h3>파르나스몰 PARNAS MALL</h3>
              <p>SNS 계정·공식 서포터즈 운영<br>신년 온라인 프로모션 기획<br>여름 시즌 '파르나스 마블' 보드게임 이벤트 기획</p>
              <div class="tags"><span class="tag">SNS</span><span class="tag">프로모션</span></div>
            </div>
          </a>
        </article>

        <article class="project-card">
          <a href="#kyobo">
            <div class="card-cover neutral"><span class="number">06</span><strong>KYOBO</strong></div>
            <div class="card-body">
              <h3>교보문고</h3>
              <p>LP 오디오북·포토카드 굿즈 제안 (시장 조사, MD 기획)<br>MD 사은품 촬영 제품 스타일링</p>
              <div class="tags"><span class="tag">MD 기획</span><span class="tag">상품 촬영</span></div>
            </div>
          </a>
        </article>

        <article class="project-card">
          <a href="#fmk">
            <div class="card-cover neutral"><span class="number">07</span><strong>FMK</strong></div>
            <div class="card-body">
              <h3>FMK 마세라티 &amp; 페라리</h3>
              <p>마세라티 구독자용 뉴스레터 제작·발송<br>마세라티 마이크로사이트 운영<br>중고사업부 공식 블로그 운영안 기획</p>
              <div class="tags"><span class="tag">CRM</span><span class="tag">디지털 마케팅</span></div>
            </div>
          </a>
        </article>

        <article class="project-card">
          <a href="#skyline">
            <div class="card-cover neutral"><span class="number">08</span><strong>SKYLINE<br>HYFLY</strong></div>
            <div class="card-body">
              <h3>스카이라인 하이플라이</h3>
              <p>부산 짚라인 어트랙션 그랜드 오픈식 제안·실행안 기획<br>현장 프로그램, SNS 이벤트, 미디어 믹스 구성</p>
              <div class="tags"><span class="tag">행사 기획</span><span class="tag">미디어 믹스</span></div>
            </div>
          </a>
        </article>

        <article class="project-card">
          <a href="#ktown">
            <div class="card-cover neutral"><span class="number">09</span><strong>Ktown4u</strong></div>
            <div class="card-body">
              <h3>Ktown4u 팝업스토어</h3>
              <p>K-POP 팝업스토어 공간 디자인 제안<br>존·동선 설계, 네온 라이팅 팬 커뮤니티 존 기획</p>
              <div class="tags"><span class="tag">공간 기획</span><span class="tag">팝업스토어</span></div>
            </div>
          </a>
        </article>

        <article class="project-card">
          <a href="#podo">
            <div class="card-cover neutral"><span class="number">10</span><strong>PODO<br>MUSEUM</strong></div>
            <div class="card-body">
              <h3>포도뮤지엄 PODO MUSEUM</h3>
              <p>쁘띠클래스·포도퍼포먼스 퍼포먼스 마케팅 플랜<br>채널별 콘텐츠 운영안과 온라인 광고 미디어 믹스</p>
              <div class="tags"><span class="tag">퍼포먼스 마케팅</span><span class="tag">콘텐츠</span></div>
            </div>
          </a>
        </article>

        <article class="project-card">
          <a href="#playpay">
            <div class="card-cover neutral"><span class="number">11</span><strong>PlayPay</strong></div>
            <div class="card-body">
              <h3>문구야놀자 PlayPay</h3>
              <p>무인 문구점 선불카드 'PlayPay' 런칭 IMC 기획<br>매장 POP, 온라인 채널, 참여 이벤트 구성</p>
              <div class="tags"><span class="tag">IMC</span><span class="tag">런칭</span></div>
            </div>
          </a>
        </article>

        <article class="project-card">
          <a href="#klc">
            <div class="card-cover neutral"><span class="number">12</span><strong>KLC<br>Playground</strong></div>
            <div class="card-body">
              <h3>KLC Playground</h3>
              <p>Seoul Mechanical Keyboard Expo 2024 총괄 기획</p>
              <div class="tags"><span class="tag">행사 기획</span></div>
            </div>
          </a>
        </article>

        <article class="project-card">
          <a href="#dongwoo">
            <div class="card-cover neutral"><span class="number">13</span><strong>동우화인켐</strong></div>
            <div class="card-body">
              <h3>동우화인켐 Dongwoo Fine-chem</h3>
              <p>사내 방송·뉴스레터·카카오 채널 운영<br>취업 박람회 부스 기획·운영<br>30주년 행사 기획</p>
              <div class="tags"><span class="tag">사내 커뮤니케이션</span><span class="tag">행사 기획</span></div>
            </div>
          </a>
        </article>
      </div>
    </div>
  </section>

  <div class="marquee" aria-label="Marketer, Creator Ops, Planner">
    MARKETER <span>CREATOR OPS</span> PLANNER
  </div>

  <section class="section" id="resume">
    <div class="container">
      <header class="section-title">
        <p class="eyebrow">Resume</p><h2>이력</h2>
      </header>
      <div class="columns">
        <div>
          <h3 class="cv-heading">경력</h3>
          <article class="cv-row">
            <div class="cv-top"><h3>젠잇 Genit · 이모틱에이아이(주)</h3><span>현재</span></div>
            <p>사이트 운영, 크리에이터 계약·정산, 이벤트 기획, MD·굿즈 디자인</p>
          </article>
          <article class="cv-row">
            <div class="cv-top"><h3>㈜나프미디어앤디자인 · 마케팅팀 사원</h3><span>2022.09 – 2023.12</span></div>
            <p>콘텐츠 기획, 디지털 마케팅 전략 수립, 상품 기획, 온·오프라인 행사 기획, 매출 증대 전략 수립·실행</p>
          </article>

          <h3 class="cv-heading">학력</h3>
          <article class="cv-row">
            <div class="cv-top"><h3>동아방송예술대학</h3><span>2019.03 – 2026.07</span></div>
            <p>엔터테인먼트경영과 · 전문학사</p>
          </article>
          <article class="cv-row">
            <div class="cv-top"><h3>한국 검정고시 졸업</h3><span>2018</span></div>
            <p>경상북도교육청</p>
          </article>
          <article class="cv-row">
            <div class="cv-top"><h3>Pugwash District High</h3><span>2017.06 – 2018.07</span></div>
            <p>인문계열 · Nova Scotia, Canada</p>
          </article>
        </div>

        <div>
          <h3 class="cv-heading">대외활동</h3>
          <article class="cv-row">
            <div class="cv-top"><h3>[소통·공감 그리고 공존] 전시회</h3><span>2024.07 – 2025.02</span></div>
            <p>전시 총괄, 작가 데뷔 · 중앙일보 기사 · 네이버 뉴스</p>
          </article>
          <article class="cv-row">
            <div class="cv-top"><h3>동아방송예술대 제28대 시선 총학생회</h3><span>2024.11 – 2025.03</span></div>
            <p>임시 학생복지국장</p>
          </article>
          <article class="cv-row">
            <div class="cv-top"><h3>영상 프로덕션 팀 Core Production</h3><span>2025.06 – 2026.02</span></div>
            <p>학과 홍보영상 [You are Star, Your Start] 총괄 기획·미술·촬영 보조, 리젠(Rejen) M/V 촬영 보조, NUMERO UNO + MR.BULLET PROOF 조감독</p>
          </article>
          <h3 class="cv-heading">기술</h3>
          <div class="chips skills">
            <span class="chip">영어 커뮤니케이션</span>
            <span class="chip">MS Office</span>
            <span class="chip">한컴오피스</span>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section class="section about" id="about">
    <div class="container">
      <header class="section-title"><p class="eyebrow">About</p><h2>소개</h2></header>
      <div class="columns">
        <blockquote>
          같은 제품도 <span class="accent">어떻게 설명하고 어떤 맥락으로 보여주느냐</span>에 따라 반응이 달라집니다.
        </blockquote>
        <div class="about-copy">
          <p>사람들과 어울리며 그들이 무엇을 필요로 하는지 파악하는 일에 흥미가 많았습니다. 모두가 함께 즐길 수 있는 분위기를 만들고 참여를 이끌어내는 데서 보람을 느꼈고, 그 성향이 학교 행사와 여러 프로젝트를 기획·운영하는 경험으로 이어졌습니다.</p>
          <p>마케팅에 본격적으로 관심을 갖게 된 건 캐나다에서였습니다. 작은 마을의 플리마켓에서 직접 디자인한 티셔츠를 팔면서, 설명 방식과 맥락에 따라 사람들의 반응이 달라진다는 걸 직접 느꼈습니다.</p>
          <p>지금은 눈길을 끄는 아이디어에서 나아가, 사람들의 반응을 분석하고 시장의 흐름을 읽어 실제 전략과 실행으로 연결하는 일을 합니다. 음악·게임·문학 같은 문화 콘텐츠 분야에 특히 관심이 많고, 트렌드를 빠르게 파악해 구체적인 실행안으로 발전시키는 것이 강점입니다.</p>
          <h3>앞으로</h3>
          <p>마케팅은 사람을 이해하는 감각과 시장을 읽는 분석적 시선이 함께할 때 힘을 가진다고 생각합니다. 이 균형을 바탕으로 브랜드와 사람 사이를 잘 연결하는 마케터로 성장하고 싶습니다.</p>
        </div>
      </div>
    </div>
  </section>

  <section class="section contact" id="contact">
    <div class="container">
      <p class="eyebrow">Contact</p>
      <h2>함께 이야기해요.</h2>
      <p class="intro">새로운 기회나 협업 제안, 가벼운 인사도 반갑습니다.</p>
      <a class="email" href="mailto:kg397340@naver.com">kg397340@naver.com</a>
    </div>
  </section>

  <section class="section cases" aria-labelledby="cases-heading">
    <div class="container">
      <header class="section-title">
        <p class="eyebrow">Project Detail</p>
        <h2 id="cases-heading">프로젝트 상세</h2>
      </header>

      <article class="case" id="genit">
        <p class="eyebrow">젠잇 Genit · 플랫폼 운영</p>
        <h3>젠잇 사이트 운영</h3>
        <p class="subtitle">AI 캐릭터·스토리 콘텐츠 플랫폼 젠잇의 화면과 소식을 꾸준히 관리합니다.</p>
        <dl class="meta">
          <div><dt>기간</dt><dd>2026</dd></div>
          <div><dt>소속</dt><dd>젠잇 Genit</dd></div>
          <div><dt>역할</dt><dd>사이트 운영 · 광고 카피</dd></div>
          <div><dt>유형</dt><dd>플랫폼 운영</dd></div>
        </dl>
        <div class="case-columns">
          <div>
            <p class="case-label">Background</p>
            <p class="background-copy">젠잇은 이용자가 AI 캐릭터와 스토리 작품을 만들고 즐기는 플랫폼입니다. 운영마케팅 팀의 PO로, 작품과 크리에이터가 늘어나는 만큼, 이용자가 처음 만나는 페이지와 공지, 광고 문구를 제작 및 관리하는 일을 맡았습니다.</p>
            <div class="tags"><span class="tag">플랫폼 운영</span><span class="tag">광고·카피</span><span class="tag">CS</span></div>
          </div>
          <div>
            <p class="case-label">What I did</p>
            <ol class="work-list">
              <li>이벤트 페이지와 공지 등록·관리</li>
              <li>리뷰 이벤트의 우수 추천 블로거 섹션 구성</li>
              <li>작품별 구글 광고 문구 작성 (자체 규칙집 V2.2 기준)</li>
              <li>플랫폼 태그라인 카피 개발</li>
              <li>크리에이터·이용자 문의 대응</li>
            </ol>
          </div>
        </div>
        <a class="back" href="#projects">← 프로젝트 목록</a>
      </article>

      <article class="case" id="contracts">
        <p class="eyebrow">젠잇 Genit · 계약 구조 설계</p>
        <h3>크리에이터 계약·지원 체계 개편</h3>
        <p class="subtitle">채팅 수 기반 지원 프로그램을 정산율 중심의 '젠잇 퍼블리싱'으로 바꿨습니다.</p>
        <dl class="meta">
          <div><dt>기간</dt><dd>2026.07 – 08</dd></div>
          <div><dt>소속</dt><dd>젠잇 Genit</dd></div>
          <div><dt>역할</dt><dd>지원 체계 설계 · 크리에이터 커뮤니케이션</dd></div>
          <div><dt>유형</dt><dd>계약 구조 설계</dd></div>
        </dl>
        <div class="case-columns">
          <div>
            <p class="case-label">Background</p>
            <p class="background-copy">기존 크리에이터 지원은 작품의 채팅 수를 기준으로 운영됐습니다. 이를 계약 유형에 따라 정산율이 정해지는 '젠잇 퍼블리싱' 체계로 전환했습니다.</p>
            <div class="tags"><span class="tag">2–30% 정산율 구간</span><span class="tag">계약 3유형</span><span class="tag">정산</span></div>
          </div>
          <div>
            <p class="case-label">What I did</p>
            <ol class="work-list">
              <li>계약 유형별 정산율 설계: 비독점 2%, 독점 10%, 퍼블리싱 20–30%</li>
              <li>파트너 계약(수수료 25%)과 일반 계약(30%) 구분 정리</li>
              <li>전환 공지와 크리에이터별 개별 안내문 작성</li>
              <li>크리에이터별 지급액·상금·세금을 집계하는 정산 시트 제작</li>
            </ol>
          </div>
        </div>
        <a class="back" href="#projects">← 프로젝트 목록</a>
      </article>

      <article class="case" id="goods">
        <p class="eyebrow">젠잇 Genit · 이벤트 · MD</p>
        <h3>이벤트·굿즈 기획</h3>
        <p class="subtitle">플랫폼 이벤트를 기획·운영하고, 작품 굿즈와 브랜드 인쇄물을 직접 디자인했습니다.</p>
        <dl class="meta">
          <div><dt>기간</dt><dd>2026</dd></div>
          <div><dt>소속</dt><dd>젠잇 Genit</dd></div>
          <div><dt>역할</dt><dd>이벤트 기획 · 굿즈 디자인</dd></div>
          <div><dt>유형</dt><dd>이벤트 · MD</dd></div>
        </dl>
        <div class="case-columns">
          <div>
            <p class="case-label">Background</p>
            <p class="background-copy">작품 팬과 크리에이터가 플랫폼 밖에서도 젠잇을 만날 수 있도록 온·오프라인 이벤트와 굿즈를 함께 준비했습니다.</p>
            <div class="tags"><span class="tag">이벤트 기획</span><span class="tag">MD 디자인</span><span class="tag">인쇄물</span></div>
          </div>
          <div>
            <p class="case-label">What I did</p>
            <ol class="work-list">
              <li>플랫폼 리뷰 이벤트 운영</li>
              <li>SF 작품 '언노운' 굿즈 이벤트 인사말 작성과 배송 운영</li>
              <li>한성대 SW·AI 산학협력센터 연계 'AI 스토리 크리에이터' 원데이 클래스 진행</li>
              <li>작품 '강호일통' 캐릭터 스페셜 포토카드 20종 디자인 (서명 합성 포함)</li>
              <li>브랜드 봉투(220×105mm)와 형압 박 감사 카드(90×50mm) 인쇄 사양 제작</li>
            </ol>
          </div>
        </div>
        <a class="back" href="#projects">← 프로젝트 목록</a>
      </article>

      <article class="case" id="fiska">
        <p class="eyebrow">나프미디어앤디자인 · 오픈 마케팅 · 행사</p>
        <h3>FISKA by LAFIANO</h3>
        <p class="subtitle">고양 삼송 라피아노 단지 안 북유럽 감성 타운 쇼핑몰의 오픈 마케팅을 기획했습니다.</p>
        <dl class="meta">
          <div><dt>기간</dt><dd>2022.09 – 12</dd></div>
          <div><dt>소속</dt><dd>나프미디어앤디자인</dd></div>
          <div><dt>역할</dt><dd>마케팅 제안 · 프로모션 기획</dd></div>
          <div><dt>유형</dt><dd>오픈 마케팅 · 행사</dd></div>
        </dl>
        <div class="case-columns">
          <div>
            <p class="case-label">Background</p>
            <p class="background-copy">'당신이 원하는 딱 그만큼(JUST AS MUCH AS)'을 컨셉으로, 입주민과 인근 주민이 부담 없이 자주 찾는 근린 상업시설로 자리 잡는 것이 목표였습니다.</p>
            <div class="tags"><span class="tag">1 MILE SOCIETY</span><span class="tag">카카오·인스타 운영</span><span class="tag">오프라인 행사</span></div>
          </div>
          <div>
            <p class="case-label">What I did</p>
            <ol class="work-list">
              <li>사운즈한남, 더 커먼스(방콕), 츠타야 등 커뮤니티형 상업공간 리서치</li>
              <li>입주민 → 인근 주민 → 광역 방문객으로 넓혀 가는 단계별 타깃 전략</li>
              <li>카카오 채널(입주민)과 인스타그램(인근 주민) 분리 운영안</li>
              <li>입주민 대상 오픈 프로모션 '휘바! 페스타' 기획</li>
              <li>오픈 시즌 마케팅 예산안(약 1억 원) 수립</li>
              <li>그랜드 오픈 [옥상 천문대] 프로모션 디자인·현장 운영·결과 보고</li>
            </ol>
          </div>
        </div>
        <a class="back" href="#projects">← 프로젝트 목록</a>
      </article>

      <article class="case" id="parnas">
        <p class="eyebrow">나프미디어앤디자인 · SNS · 시즌 프로모션</p>
        <h3>파르나스몰 PARNAS MALL</h3>
        <p class="subtitle">삼성동 파르나스몰의 SNS와 서포터즈를 운영하고 시즌 프로모션을 기획했습니다.</p>
        <dl class="meta">
          <div><dt>기간</dt><dd>2023.01 – 06</dd></div>
          <div><dt>소속</dt><dd>나프미디어앤디자인</dd></div>
          <div><dt>역할</dt><dd>SNS 운영 · 프로모션 기획</dd></div>
          <div><dt>유형</dt><dd>SNS · 시즌 프로모션</dd></div>
        </dl>
        <div class="case-columns">
          <div>
            <p class="case-label">Background</p>
            <p class="background-copy">몰을 찾는 2030 직장인 고객의 방문과 구매를 늘리기 위해, 온라인 채널 운영과 시즌 이벤트를 함께 설계했습니다.</p>
            <div class="tags"><span class="tag">SNS 운영</span><span class="tag">시즌 프로모션</span><span class="tag">공간 연출</span></div>
          </div>
          <div>
            <p class="case-label">What I did</p>
            <ol class="work-list">
              <li>파르나스몰 SNS 계정과 공식 서포터즈 운영</li>
              <li>신년 온라인 프로모션 기획 (2023.01)</li>
              <li>여름 '파르나스 마블! SUMMER SALE Vacance!' 보드게임 이벤트 기획</li>
              <li>영수증 금액별 차등 참여 방식과 시즌 경품 구성</li>
              <li>센트럴 라운지 공간 연출, 카드뉴스·POP·배너·DID 홍보물 구성</li>
            </ol>
          </div>
        </div>
        <a class="back" href="#projects">← 프로젝트 목록</a>
      </article>

      <article class="case" id="kyobo">
        <p class="eyebrow">나프미디어앤디자인 · 굿즈 제안 · MD</p>
        <h3>교보문고</h3>
        <p class="subtitle">교보문고에서만 만날 수 있는 수집형 굿즈</p>
        <dl class="meta">
          <div><dt>기간</dt><dd>2023.04</dd></div>
          <div><dt>소속</dt><dd>나프미디어앤디자인</dd></div>
          <div><dt>역할</dt><dd>시장 조사 · 굿즈 기획</dd></div>
          <div><dt>유형</dt><dd>굿즈 제안 · MD</dd></div>
        </dl>
        <div class="case-columns">
          <div>
            <p class="case-label">Background</p>
            <p class="background-copy">책과 연결된 상징적인 굿즈로 고객의 수집 욕구와 재방문을 이끄는 것이 목표였습니다.</p>
            <div class="tags"><span class="tag">굿즈 기획</span><span class="tag">시장 조사</span><span class="tag">상품 촬영</span></div>
          </div>
          <div>
            <p class="case-label">What I did</p>
            <ol class="work-list">
              <li>LP 오디오북 제안: 아날로그 LP 외형에 오디오북 기능을 더한 홈 인테리어 굿즈</li>
              <li>홈 인테리어·LP·오디오북 시장 조사</li>
              <li>북 포토카드 제안: 읽은 책을 기억하는 수집형 카드와 부자재 구성</li>
              <li>포토카드 시장과 활용 사례 조사, 디자인 시안 구성</li>
              <li>MD 사은품 촬영 제품 스타일링</li>
            </ol>
          </div>
        </div>
        <a class="back" href="#projects">← 프로젝트 목록</a>
      </article>

      <article class="case" id="fmk">
        <p class="eyebrow">나프미디어앤디자인 · CRM · 디지털</p>
        <h3>FMK 마세라티 &amp; 페라리</h3>
        <p class="subtitle">마세라티 고객 커뮤니케이션 채널을 운영하고, 중고사업부 블로그를 기획했습니다.</p>
        <dl class="meta">
          <div><dt>기간</dt><dd>2023</dd></div>
          <div><dt>소속</dt><dd>나프미디어앤디자인</dd></div>
          <div><dt>역할</dt><dd>뉴스레터 · 디지털 채널 기획</dd></div>
          <div><dt>유형</dt><dd>CRM · 디지털</dd></div>
        </dl>
        <div class="case-columns">
          <div>
            <p class="case-label">Background</p>
            <p class="background-copy">구독 고객과 잠재 구매자에게 브랜드 소식과 차량 정보를 꾸준히 전달하는 디지털 채널이 필요했습니다.</p>
            <div class="tags"><span class="tag">CRM</span><span class="tag">블로그 기획</span><span class="tag">벤치마킹</span></div>
          </div>
          <div>
            <p class="case-label">What I did</p>
            <ol class="work-list">
              <li>마세라티 구독자용 뉴스레터 제작·발송</li>
              <li>마세라티 마이크로사이트 운영</li>
              <li>중고사업부 공식 블로그 운영안 기획 (2023.09)</li>
              <li>BMW·람보르기니·랜드로버/재규어 공식 블로그 벤치마킹</li>
              <li>엔카 내 마세라티 페이지 분석과 블로그 메인·콘텐츠 PC/모바일 화면 설계</li>
            </ol>
          </div>
        </div>
        <a class="back" href="#projects">← 프로젝트 목록</a>
      </article>

      <article class="case" id="skyline">
        <p class="eyebrow">나프미디어앤디자인 · 오픈 행사</p>
        <h3>스카이라인 하이플라이</h3>
        <p class="subtitle">부산 오시리아 짚라인 어트랙션 '하이플라이'의 그랜드 오픈식을 기획했습니다.</p>
        <dl class="meta">
          <div><dt>기간</dt><dd>2023.09</dd></div>
          <div><dt>소속</dt><dd>나프미디어앤디자인</dd></div>
          <div><dt>역할</dt><dd>행사 제안 · 실행안 기획</dd></div>
          <div><dt>유형</dt><dd>오픈 행사</dd></div>
        </dl>
        <div class="case-columns">
          <div>
            <p class="case-label">Background</p>
            <p class="background-copy">스카이라인 루지 부산에 새로 생긴 짚라인 '하이플라이'의 런칭 소식을 알리고, 부산의 랜드마크 어트랙션으로 자리 잡게 하는 것이 목표였습니다. 오픈식은 2023년 9월 13일 진행됐습니다.</p>
            <div class="tags"><span class="tag">행사 기획</span><span class="tag">미디어 믹스</span><span class="tag">VIP 의전</span></div>
          </div>
          <div>
            <p class="case-label">What I did</p>
            <ol class="work-list">
              <li>오리지널리티 강조와 랜드마크 포지셔닝 전략 수립</li>
              <li>오픈식 현장 조닝과 타임테이블 구성</li>
              <li>메인 프로그램: 오프닝 퍼포먼스, 세레모니, 탑승 체험, 축하 공연, 케이터링</li>
              <li>서브 프로그램: 인스타그램 댓글 이벤트, 사전 응모 100명 무료 탑승, 현장 뽑기</li>
              <li>온·오프라인 미디어 믹스 구성, 제안서에서 실행안까지 작성</li>
            </ol>
          </div>
        </div>
        <a class="back" href="#projects">← 프로젝트 목록</a>
      </article>

      <article class="case" id="ktown">
        <p class="eyebrow">나프미디어앤디자인 · 공간 디자인 제안</p>
        <h3>Ktown4u 팝업스토어</h3>
        <p class="subtitle">K-POP 팝업스토어 공간을 팬이 오래 머무는 곳으로 리뉴얼하는 안을 제안했습니다.</p>
        <dl class="meta">
          <div><dt>기간</dt><dd>2023.06</dd></div>
          <div><dt>소속</dt><dd>나프미디어앤디자인</dd></div>
          <div><dt>역할</dt><dd>공간 기획 · 디자인 제안</dd></div>
          <div><dt>유형</dt><dd>공간 디자인 제안</dd></div>
        </dl>
        <div class="case-columns">
          <div>
            <p class="case-label">Background</p>
            <p class="background-copy">기존 매장은 현수막과 마그넷 위주라 넓은 공간이 비어 보였습니다. 아이돌마다 바뀌는 팝업에 맞춰 쉽게 교체할 수 있는 연출 시스템이 필요했습니다.</p>
            <div class="tags"><span class="tag">공간 기획</span><span class="tag">팝업스토어</span><span class="tag">팬 경험</span></div>
          </div>
          <div>
            <p class="case-label">What I did</p>
            <ol class="work-list">
              <li>고해상도 초상 이미지와 네온·포인트 라이팅으로 공간 몰입감 강화</li>
              <li>초상 이미지만 교체하면 되는 재사용형 연출 시스템 설계</li>
              <li>입구·판매·포토존·카페로 나눈 조닝과 동선 계획</li>
              <li>팬 커뮤니티 존과 존별 세부 연출 제안</li>
              <li>설치 품목 리스트와 견적 정리</li>
            </ol>
          </div>
        </div>
        <a class="back" href="#projects">← 프로젝트 목록</a>
      </article>

      <article class="case" id="podo">
        <p class="eyebrow">나프미디어앤디자인 · 퍼포먼스 마케팅</p>
        <h3>포도뮤지엄 PODO MUSEUM</h3>
        <p class="subtitle">미술관 참여 프로그램 두 가지의 홍보와 콘텐츠 운영을 설계했습니다.</p>
        <dl class="meta">
          <div><dt>기간</dt><dd>2023.06 – 09</dd></div>
          <div><dt>소속</dt><dd>나프미디어앤디자인</dd></div>
          <div><dt>역할</dt><dd>마케팅 플랜 · 콘텐츠 운영안</dd></div>
          <div><dt>유형</dt><dd>퍼포먼스 마케팅</dd></div>
        </dl>
        <div class="case-columns">
          <div>
            <p class="case-label">Background</p>
            <p class="background-copy">7월 '쁘띠클래스'(북·시네마·드로잉, 4회)와 8–9월 '포도퍼포먼스'(안무·사운드·낭독, 4회)를 알리고 예매로 이어지게 하는 것이 목표였습니다.</p>
            <div class="tags"><span class="tag">퍼포먼스 마케팅</span><span class="tag">콘텐츠</span><span class="tag">광고 운영</span></div>
          </div>
          <div>
            <p class="case-label">What I did</p>
            <ol class="work-list">
              <li>회차별 홍보 프로세스와 일정 설계</li>
              <li>인스타그램 피드·스토리·릴스, 웹사이트 콘텐츠 운영안</li>
              <li>행사 당일 라이브 콘텐츠와 스케치 콘텐츠 기획</li>
              <li>유튜브, 네이버 GFA, 구글 GDN, 당근 등 온라인 광고 미디어 믹스와 예산 배분</li>
            </ol>
          </div>
        </div>
        <a class="back" href="#projects">← 프로젝트 목록</a>
      </article>

      <article class="case" id="playpay">
        <p class="eyebrow">나프미디어앤디자인 · 런칭 IMC</p>
        <h3>문구야놀자 PlayPay</h3>
        <p class="subtitle">무인 문구점 '문구야놀자'의 선불카드 PlayPay 런칭 캠페인을 기획했습니다.</p>
        <dl class="meta">
          <div><dt>기간</dt><dd>2023.08</dd></div>
          <div><dt>소속</dt><dd>나프미디어앤디자인</dd></div>
          <div><dt>역할</dt><dd>IMC 기획</dd></div>
          <div><dt>유형</dt><dd>런칭 IMC</dd></div>
        </dl>
        <div class="case-columns">
          <div>
            <p class="case-label">Background</p>
            <p class="background-copy">아이들에게는 놀이처럼 즐거운 카드로, 부모님에게는 믿을 수 있는 결제 수단으로 알리는 것이 핵심이었습니다.</p>
            <div class="tags"><span class="tag">IMC</span><span class="tag">런칭</span><span class="tag">매장 POP</span></div>
          </div>
          <div>
            <p class="case-label">What I did</p>
            <ol class="work-list">
              <li>아이 → 친구 → 부모로 이어지는 카드 유입 3단계 정리</li>
              <li>Plan A 런칭: 보유 채널 리뉴얼, 매장 POP·사이니지, 온라인 광고</li>
              <li>Plan B 활성화: 매달 9일 '문9데이' 정기 이벤트</li>
              <li>추천인 쌍방 복권 이벤트 등 참여형 프로모션</li>
            </ol>
          </div>
        </div>
        <a class="back" href="#projects">← 프로젝트 목록</a>
      </article>

      <article class="case" id="klc">
        <p class="eyebrow">KLC Playground · 전시 행사</p>
        <h3>KLC Playground</h3>
        <p class="subtitle">기계식 키보드 전시회 'Seoul Mechanical Keyboard Expo'를 총괄 기획했습니다.</p>
        <dl class="meta">
          <div><dt>기간</dt><dd>2024</dd></div>
          <div><dt>소속</dt><dd>KLC Playground</dd></div>
          <div><dt>역할</dt><dd>총괄 기획</dd></div>
          <div><dt>유형</dt><dd>전시 행사</dd></div>
        </dl>
        <div class="case-columns">
          <div>
            <p class="case-label">Background</p>
            <p class="background-copy">키보드 애호가와 브랜드가 한자리에 모이는 전시 행사를 처음부터 끝까지 기획했습니다.</p>
            <div class="tags"><span class="tag">행사 기획</span><span class="tag">전시</span></div>
          </div>
          <div>
            <p class="case-label">What I did</p>
            <ol class="work-list"><li>Seoul Mechanical Keyboard Expo 총괄 기획</li></ol>
          </div>
        </div>
        <a class="back" href="#projects">← 프로젝트 목록</a>
      </article>

      <article class="case" id="dongwoo">
        <p class="eyebrow">나프미디어앤디자인 · 사내 커뮤니케이션</p>
        <h3>동우화인켐 Dongwoo Fine-chem</h3>
        <p class="subtitle">임직원 대상 사내 커뮤니케이션 채널과 기업 행사를 운영했습니다.</p>
        <dl class="meta">
          <div><dt>기간</dt><dd>—</dd></div>
          <div><dt>소속</dt><dd>나프미디어앤디자인</dd></div>
          <div><dt>역할</dt><dd>사내 채널 운영 · 행사 기획</dd></div>
          <div><dt>유형</dt><dd>사내 커뮤니케이션</dd></div>
        </dl>
        <div class="case-columns">
          <div>
            <p class="case-label">Background</p>
            <p class="background-copy">임직원에게 회사 소식을 꾸준히 전하고, 채용과 기념 행사를 준비했습니다.</p>
            <div class="tags"><span class="tag">사내 커뮤니케이션</span><span class="tag">행사 기획</span></div>
          </div>
          <div>
            <p class="case-label">What I did</p>
            <ol class="work-list">
              <li>사내 방송 관리 (TTS 활용)</li>
              <li>사내 뉴스레터 콘텐츠 발행</li>
              <li>카카오 채널 운영</li>
              <li>취업 박람회 부스 기획·운영</li>
              <li>30주년 행사 기획</li>
            </ol>
          </div>
        </div>
        <a class="back" href="#projects">← 프로젝트 목록</a>
      </article>
    </div>
  </section>
</main>

<footer>
  <div class="container footer-inner">
    <p>© 2026 김규준 Gyujun Kim</p>
    <p>Marketer · Creator Ops · Platform Planning</p>
  </div>
</footer>
</body>
</html>
