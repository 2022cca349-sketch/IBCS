# IBCS
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>프라하에서 떠나는 종교개혁의 길 — 비텐베르크 & 드레스덴</title>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=IM+Fell+English:ital@0;1&family=Noto+Serif+KR:wght@300;400;600&family=Noto+Sans+KR:wght@300;400&display=swap" rel="stylesheet" />
  <style>
    /* ── Token System ───────────────────────────────────────────── */
    :root {
      --ink:        #1a1410;
      --vellum:     #f7f2e8;
      --aged:       #e8dfc8;
      --rust:       #8b3a2a;
      --gold:       #b8922a;
      --stone:      #6b6356;
      --pale-stone: #c4bdb0;
      --shadow:     rgba(26, 20, 16, 0.12);

      --ff-display: 'IM Fell English', serif;
      --ff-body:    'Noto Serif KR', serif;
      --ff-ui:      'Noto Sans KR', sans-serif;
    }

    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    html { scroll-behavior: smooth; }

    body {
      background: var(--vellum);
      color: var(--ink);
      font-family: var(--ff-body);
      font-size: 16px;
      line-height: 1.8;
    }

    /* ── Wax Seal Loader (signature element) ────────────────────── */
    .seal {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      width: 72px; height: 72px;
      border-radius: 50%;
      background: var(--rust);
      color: #fff;
      font-family: var(--ff-display);
      font-size: 1.5rem;
      font-style: italic;
      box-shadow: 0 4px 18px rgba(139,58,42,.45), inset 0 -3px 8px rgba(0,0,0,.25);
      flex-shrink: 0;
    }

    /* ── Header / Hero ──────────────────────────────────────────── */
    .hero {
      position: relative;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 6rem 2rem 4rem;
      overflow: hidden;
      background: var(--ink);
    }

    .hero::after {
      content: '';
      position: absolute; inset: 0;
      background-image: url('6377525081872117370.jpg');
      background-size: cover;
      background-position: center;
      opacity: .18;
      z-index: 0;
    }

    /* Parchment texture overlay via SVG filter */
    .hero::before {
      content: '';
      position: absolute; inset: 0;
      background:
        repeating-linear-gradient(
          0deg,
          transparent, transparent 2px,
          rgba(255,255,255,.018) 2px, rgba(255,255,255,.018) 3px
        ),
        radial-gradient(ellipse 80% 60% at 50% 40%, #2d1f14 0%, #0d0a07 100%);
      z-index: 0;
    }

    .hero > * { position: relative; z-index: 1; }

    .hero-eyebrow {
      font-family: var(--ff-ui);
      font-size: .75rem;
      font-weight: 300;
      letter-spacing: .25em;
      text-transform: uppercase;
      color: var(--pale-stone);
      margin-bottom: 2rem;
    }

    .hero-title {
      font-family: var(--ff-display);
      font-size: clamp(2.4rem, 6vw, 5rem);
      font-style: italic;
      line-height: 1.1;
      color: var(--vellum);
      max-width: 800px;
    }

    .hero-title em {
      font-style: normal;
      color: var(--gold);
    }

    .hero-subtitle {
      margin-top: 1.5rem;
      font-family: var(--ff-ui);
      font-size: 1rem;
      font-weight: 300;
      color: var(--pale-stone);
      letter-spacing: .05em;
    }

    .hero-divider {
      width: 120px;
      height: 1px;
      background: linear-gradient(to right, transparent, var(--gold), transparent);
      margin: 2.5rem auto;
    }

    .hero-quote {
      font-family: var(--ff-display);
      font-style: italic;
      font-size: 1.15rem;
      color: var(--aged);
      max-width: 600px;
      line-height: 1.7;
    }

    .hero-quote cite {
      display: block;
      margin-top: .75rem;
      font-size: .8rem;
      font-style: normal;
      font-family: var(--ff-ui);
      letter-spacing: .12em;
      text-transform: uppercase;
      color: var(--gold);
    }

    /* ── Nav ────────────────────────────────────────────────────── */
    .sticky-nav {
      position: sticky;
      top: 0;
      z-index: 100;
      background: rgba(26, 20, 16, .96);
      backdrop-filter: blur(6px);
      border-bottom: 1px solid rgba(184,146,42,.3);
    }

    .nav-inner {
      max-width: 1100px;
      margin: 0 auto;
      display: flex;
      align-items: center;
      gap: 2rem;
      padding: .9rem 2rem;
      overflow-x: auto;
    }

    .nav-inner a {
      font-family: var(--ff-ui);
      font-size: .8rem;
      font-weight: 300;
      letter-spacing: .12em;
      text-transform: uppercase;
      text-decoration: none;
      color: var(--pale-stone);
      white-space: nowrap;
      transition: color .2s;
    }

    .nav-inner a:hover { color: var(--gold); }
    .nav-inner .nav-logo {
      font-family: var(--ff-display);
      font-style: italic;
      font-size: 1rem;
      color: var(--vellum);
      margin-right: auto;
      white-space: nowrap;
    }

    /* ── Sections ───────────────────────────────────────────────── */
    .section {
      max-width: 900px;
      margin: 0 auto;
      padding: 5rem 2rem;
    }

    .section-label {
      font-family: var(--ff-ui);
      font-size: .72rem;
      font-weight: 400;
      letter-spacing: .22em;
      text-transform: uppercase;
      color: var(--rust);
      display: flex;
      align-items: center;
      gap: .75rem;
      margin-bottom: 1rem;
    }

    .section-label::after {
      content: '';
      flex: 1;
      max-width: 60px;
      height: 1px;
      background: var(--rust);
      opacity: .5;
    }

    .section-title {
      font-family: var(--ff-display);
      font-size: clamp(1.8rem, 4vw, 2.8rem);
      font-style: italic;
      line-height: 1.2;
      color: var(--ink);
      margin-bottom: .5rem;
    }

    .section-intro {
      font-size: 1rem;
      color: var(--stone);
      margin-bottom: 3rem;
      max-width: 640px;
    }

    /* ── Landmark photo ─────────────────────────────────────────── */
    .landmark-photo {
      width: 100%;
      height: auto;
      max-height: 500px;
      object-fit: cover;
      display: block;
      margin-bottom: 1.8rem;
      border-left: 3px solid var(--gold);
      filter: sepia(5%) contrast(1.02);
    }

    .photo-placeholder {
      width: 100%;
      height: 260px;
      display: flex;
      align-items: center;
      justify-content: center;
      background: var(--aged);
      border-left: 3px solid var(--gold);
      margin-bottom: 1.8rem;
      font-family: var(--ff-ui);
      font-size: .8rem;
      letter-spacing: .1em;
      color: var(--stone);
      text-transform: uppercase;
    }

    /* ── City Band ──────────────────────────────────────────────── */
    .city-band {
      position: relative;
      color: var(--vellum);
      padding: 4rem 2rem;
      text-align: center;
      overflow: hidden;
    }

    .city-band::before {
      content: '';
      position: absolute; inset: 0;
      background-size: cover;
      background-position: center;
      opacity: .22;
      z-index: 0;
    }

    .city-band::after {
      content: '';
      position: absolute; inset: 0;
      background: var(--ink);
      z-index: 0;
    }

    .city-band > * { position: relative; z-index: 1; }

    .city-band.wittenberg-band::before {
      background-image: url('꾸미기_SAM_5409.jpeg');
    }

    .city-band.dresden-band::before {
      background-image: url('6377525081872117370.jpg');
    }

    .city-band .city-name {
      font-family: var(--ff-display);
      font-size: clamp(1.4rem, 3.5vw, 2.2rem);
      font-style: italic;
      color: var(--gold);
    }

    .city-band .city-desc {
      font-family: var(--ff-ui);
      font-weight: 300;
      font-size: .88rem;
      letter-spacing: .08em;
      color: var(--pale-stone);
      margin-top: .4rem;
    }

    /* ── Landmark Card ──────────────────────────────────────────── */
    .landmark-card {
      border-left: 3px solid var(--gold);
      padding: 0 0 0 2rem;
      margin-bottom: 3.5rem;
    }

    .landmark-card + .landmark-card {
      padding-top: 3.5rem;
      border-top: 1px solid var(--aged);
    }

    .landmark-name {
      font-family: var(--ff-display);
      font-size: 1.6rem;
      font-style: italic;
      color: var(--ink);
      margin-bottom: .3rem;
    }

    .landmark-name-en {
      font-family: var(--ff-ui);
      font-size: .78rem;
      letter-spacing: .15em;
      text-transform: uppercase;
      color: var(--stone);
      margin-bottom: 1.2rem;
    }

    /* Sub-sections inside a card */
    .card-block {
      margin-bottom: 1.6rem;
    }

    .card-block-label {
      font-family: var(--ff-ui);
      font-size: .72rem;
      font-weight: 400;
      letter-spacing: .18em;
      text-transform: uppercase;
      color: var(--rust);
      margin-bottom: .4rem;
    }

    .card-block p {
      font-size: .97rem;
      color: #2e2620;
      line-height: 1.85;
    }

    /* Tip box */
    .tip-box {
      background: var(--aged);
      border: 1px solid var(--pale-stone);
      border-radius: 2px;
      padding: 1.1rem 1.4rem;
      margin-top: .5rem;
    }

    .tip-box p {
      font-size: .9rem !important;
      color: var(--ink) !important;
    }

    /* Route pill */
    .route-steps {
      display: flex;
      flex-wrap: wrap;
      gap: .6rem;
      margin-top: .6rem;
    }

    .route-step {
      display: inline-flex;
      align-items: center;
      gap: .4rem;
      background: var(--ink);
      color: var(--vellum);
      font-family: var(--ff-ui);
      font-size: .78rem;
      font-weight: 300;
      letter-spacing: .06em;
      padding: .35rem .9rem;
      border-radius: 2px;
    }

    .route-step .icon { font-size: 1rem; }

    /* ── Reflection Banner ──────────────────────────────────────── */
    .reflection {
      background: #1e1208;
      color: var(--vellum);
      padding: 4rem 2rem;
      text-align: center;
      border-top: 1px solid rgba(184,146,42,.25);
      border-bottom: 1px solid rgba(184,146,42,.25);
    }

    .reflection blockquote {
      font-family: var(--ff-display);
      font-style: italic;
      font-size: clamp(1.2rem, 2.8vw, 1.8rem);
      line-height: 1.5;
      max-width: 680px;
      margin: 0 auto 1rem;
    }

    .reflection cite {
      font-family: var(--ff-ui);
      font-size: .78rem;
      letter-spacing: .15em;
      text-transform: uppercase;
      color: var(--gold);
      opacity: .9;
    }

    /* ── Transport Strip ────────────────────────────────────────── */
    .route-overview {
      display: flex;
      flex-direction: column;
      gap: .75rem;
      margin-top: 2rem;
    }

    .route-row {
      display: flex;
      align-items: center;
      gap: 1rem;
      padding: .9rem 1.2rem;
      background: var(--vellum);
      border-left: 3px solid var(--gold);
      flex-wrap: wrap;
    }

    .route-city {
      font-family: var(--ff-body);
      font-size: .95rem;
      font-weight: 600;
      color: var(--ink);
      white-space: nowrap;
    }

    .route-city.highlight { color: var(--rust); }

    .route-arrow {
      color: var(--gold);
      font-size: 1.1rem;
      flex-shrink: 0;
    }

    .route-detail {
      font-family: var(--ff-ui);
      font-size: .82rem;
      font-weight: 300;
      color: var(--stone);
      flex: 1;
    }

    /* ── Footer ─────────────────────────────────────────────────── */
    footer {
      background: var(--ink);
      color: var(--stone);
      text-align: center;
      padding: 3rem 2rem;
      font-family: var(--ff-ui);
      font-size: .78rem;
      letter-spacing: .1em;
    }

    footer .footer-logo {
      font-family: var(--ff-display);
      font-style: italic;
      font-size: 1.4rem;
      color: var(--gold);
      display: block;
      margin-bottom: .75rem;
    }

    /* ── Scroll reveal ──────────────────────────────────────────── */
    .reveal {
      opacity: 0;
      transform: translateY(24px);
      transition: opacity .65s ease, transform .65s ease;
    }

    .reveal.visible {
      opacity: 1;
      transform: none;
    }

    /* ── Responsive ─────────────────────────────────────────────── */
    @media (max-width: 600px) {
      .landmark-card { padding-left: 1.2rem; }
      .nav-inner { gap: 1.2rem; }
    }

    @media (prefers-reduced-motion: reduce) {
      .reveal { opacity: 1; transform: none; transition: none; }
    }
  </style>
</head>
<body>

  <section class="hero">
    <p class="hero-eyebrow">프라하 출발 · 종교개혁 역사 순례</p>
    <h1 class="hero-title">
      종교개혁의 길<br><em>비텐베르크 & 드레스덴</em>
    </h1>
    <p class="hero-subtitle">Wittenberg &amp; Dresden — Reformation Heritage Trail from Prague</p>
    <div class="hero-divider"></div>
    <p class="hero-quote">
      "내 양심은 하나님의 말씀에 사로잡혀 있습니다.<br>
      나는 철회할 수도, 철회하지도 않겠습니다."
      <cite>— 마르틴 루터, 1521</cite>
    </p>
  </section>

  <nav class="sticky-nav">
    <div class="nav-inner">
      <span class="nav-logo">종교개혁의 길</span>
      <a href="#wittenberg">비텐베르크</a>
      <a href="#luther-museum">루터 뮤지엄</a>
      <a href="#schlosskirche">성교회</a>
      <a href="#dresden">드레스덴</a>
      <a href="#zwinger">츠빙거 궁전</a>
      <a href="#stallhof">슈탈호프</a>
      <a href="#semper">젬퍼 오페라</a>
      <a href="#practical">실전 정보</a>
    </div>
  </nav>

  <div class="city-band wittenberg-band" id="wittenberg">
    <p class="city-name">비텐베르크 Wittenberg</p>
    <p class="city-desc">종교개혁의 진원지 · 루터가 95개조 반박문을 게시한 도시</p>
  </div>

  <section class="section" id="luther-museum">
    <p class="section-label">비텐베르크 첫 번째 명소</p>
    <h2 class="section-title">루터하우스 — 루터 뮤지엄</h2>
    <p class="section-intro">
      세계에서 가장 중요한 종교개혁 박물관. 루터가 실제로 살았던 아우구스티누스 수도원 건물 그 자체입니다.
    </p>

    <div class="landmark-card reveal">
      <img src="1640518635_K8u_Lutherhaus.jpg" alt="루터하우스 비텐베르크" class="landmark-photo" />
      <h3 class="landmark-name">루터하우스 (루터 뮤지엄)</h3>
      <p class="landmark-name-en">Lutherhaus · Lutherstadt Wittenberg</p>

      <div class="card-block">
        <p class="card-block-label">장소 소개</p>
        <p>
          루터하우스는 1504년 아우구스티누스 수도원으로 세워진 건물로, 마르틴 루터가 1508년 처음 입주한 뒤
          평생 거주한 곳입니다. 그는 이 집에서 성경을 독일어로 번역하고, 수많은 신학 논문을 저술했습니다.
          현재 유네스코 세계문화유산으로 등재되어 있으며, 루터의 친필 원고·초상화·개인 유품이
          원래 방에 전시되어 있어 "살아있는 박물관"이라 불립니다.
        </p>
      </div>

      <div class="card-block">
        <p class="card-block-label">종교개혁 · 기독교적 의미</p>
        <p>
          이 집은 단순한 주거 공간이 아니라 <strong>종교개혁의 지적 심장부</strong>였습니다.
          루터는 이 서재에서 "오직 성경(Sola Scriptura)", "오직 믿음(Sola Fide)"이라는 개혁 신학의 핵심 원리를 정립했습니다.
          그의 아내 카타리나 폰 보라와 함께 구축한 가정 공동체는 수도원적 금욕주의를 벗어나
          복음적 가정의 모델을 제시했습니다. 중세 가톨릭 수도원이 개신교 가정의 공간으로 변모한
          그 자체가 종교개혁의 상징입니다.
        </p>
      </div>

      <div class="card-block">
        <p class="card-block-label">관광 팁</p>
        <div class="tip-box">
          <p>
            ✦ 반드시 루터의 <strong>서재(Lutherstube)</strong>와 대형 강의실(Hörsaal)을 놓치지 마세요.<br>
            ✦ 한국어 오디오 가이드는 없으나 영어 오디오 가이드 이용 가능합니다.<br>
            ✦ 뮤지엄 숍에서 95개조 반박문 복제본(라틴어·독일어)을 구입할 수 있습니다.<br>
            ✦ 입장료 약 €10 / 개관 시간 10:00–18:00 (월요일 휴관, 11–3월 단축 운영).<br>
            ✦ 루터의 장미(Luther Rose) 문양이 새겨진 기념품은 역사적 의미도 큽니다.
          </p>
        </div>
      </div>

      <div class="card-block">
        <p class="card-block-label">가는 길 — 프라하 출발</p>
        <div class="route-steps">
          <span class="route-step"><span class="icon">🚂</span> 프라하 중앙역 출발</span>
          <span class="route-step"><span class="icon">➜</span> EC/ICE 열차 드레스덴 환승</span>
          <span class="route-step"><span class="icon">➜</span> 비텐베르크 중앙역 도착 (총 약 2.5–3시간)</span>
          <span class="route-step"><span class="icon">🚶</span> 역에서 도보 15분</span>
        </div>
        <p style="margin-top:.8rem; font-size:.88rem; color:var(--stone);">
          직행은 없으며 드레스덴 혹은 라이프치히 경유가 일반적입니다.
          독일 DB 앱으로 예매 시 조기 할인(Sparpreis) 가능. 비텐베르크 시내는 걷기 좋아 렌터카 불필요합니다.
        </p>
      </div>
    </div>
  </section>

  <section class="section" id="schlosskirche" style="padding-top:0;">
    <p class="section-label">비텐베르크 두 번째 명소</p>
    <h2 class="section-title">성교회 — 95개조 반박문의 문</h2>
    <p class="section-intro">
      1517년 10월 31일, 루터가 그 문에 반박문을 못 박아 서방 기독교 역사를 바꾼 바로 그 장소입니다.
    </p>

    <div class="landmark-card reveal">
      <img src="꾸미기_SAM_5409.jpeg" alt="비텐베르크 성교회" class="landmark-photo" />
      <h3 class="landmark-name">비텐베르크 슐로스키르헤 (성교회)</h3>
      <p class="landmark-name-en">Schlosskirche · Castle Church of Wittenberg</p>

      <div class="card-block">
        <p class="card-block-label">장소 소개</p>
        <p>
          1503년 선제후 프리드리히 3세가 세운 궁정 교회로, 원래 로마 가톨릭 예배당이었습니다.
          1517년 루터가 95개조 반박문을 게시했던 원래의 나무 문은 7년 전쟁(1760) 당시 소실되었고,
          현재의 <strong>청동 문(1858년 제작)</strong>은 프리드리히 빌헬름 4세의 명으로 반박문 전문이 라틴어로 새겨져 있습니다.
          루터와 멜란히톤의 묘가 제단 앞에 안치되어 있습니다.
        </p>
      </div>

      <div class="card-block">
        <p class="card-block-label">종교개혁 · 기독교적 의미</p>
        <p>
          10월 31일은 오늘날 전 세계 개신교가 지키는 <strong>종교개혁 기념일(Reformation Day)</strong>입니다.
          루터의 행동은 단순한 신학 논쟁이 아니라, 당시 면죄부 판매를 통해 구원을 상품화하던 중세 교회 시스템에
          정면으로 맞선 역사적 저항이었습니다. "성경으로 돌아가라"는 그의 외침은
          개신교(루터교·칼뱅주의·성공회 등)의 탄생을 불러왔고, 오늘날 세계 기독교의 절반이 그 유산 위에 서 있습니다.
          청동 문 앞에서 기도하는 순례자들의 모습은 지금도 일상적으로 볼 수 있습니다.
        </p>
      </div>

      <div class="card-block">
        <p class="card-block-label">관광 팁</p>
        <div class="tip-box">
          <p>
            ✦ 청동 문은 외부에서 언제든 자유롭게 볼 수 있습니다 (무료).<br>
            ✦ 교회 내부(루터·멜란히톤 묘 포함) 입장료 약 €5.<br>
            ✦ <strong>10월 31일 종교개혁 기념일</strong>에는 대규모 예배와 행사가 열립니다 — 강렬한 경험을 원한다면 이 날을 맞추세요.<br>
            ✦ 교회 탑(Kirchturm) 전망대에서 비텐베르크 구시가지 전경을 감상할 수 있습니다.<br>
            ✦ 루터하우스에서 도보 10분 거리로, 두 곳을 묶어 반나절 코스로 구성하면 좋습니다.
          </p>
        </div>
      </div>

      <div class="card-block">
        <p class="card-block-label">가는 길 — 루터하우스에서</p>
        <div class="route-steps">
          <span class="route-step"><span class="icon">🚶</span> 루터하우스에서 도보 10분</span>
          <span class="route-step"><span class="icon">📍</span> Schlossplatz 1, 06886 Lutherstadt Wittenberg</span>
        </div>
        <p style="margin-top:.8rem; font-size:.88rem; color:var(--stone);">
          루터하우스 → 마르크트 광장(루터 동상) → 성교회 순으로 걷는 코스가 역사적 맥락을 따라가기에 가장 이상적입니다.
        </p>
      </div>
    </div>
  </section>

  <div class="reflection">
    <blockquote>
      "여기 내가 섰습니다. 나는 달리 어찌 할 수 없습니다.<br>
      하나님이여, 나를 도우소서."
    </blockquote>
    <cite>— 마르틴 루터, 보름스 제국의회, 1521</cite>
  </div>

  <div class="city-band dresden-band" id="dresden">
    <p class="city-name">드레스덴 Dresden</p>
    <p class="city-desc">엘베강의 피렌체 · 바로크 예술의 수도 · 프라하에서 가장 가까운 독일 대도시</p>
  </div>

  <section class="section" id="zwinger">
    <p class="section-label">드레스덴 첫 번째 명소</p>
    <h2 class="section-title">츠빙거 궁전</h2>
    <p class="section-intro">
      작센 선제후의 영광을 담은 후기 바로크 걸작. 라파엘로의 「시스티나의 성모」를 소장한 유럽 최고 박물관 단지입니다.
    </p>

    <div class="landmark-card reveal">
      <img src="6377525081872117370.jpg" alt="드레스덴 츠빙거 궁전" class="landmark-photo" />
      <h3 class="landmark-name">드레스더 츠빙거</h3>
      <p class="landmark-name-en">Dresdner Zwinger · 1710–1732</p>

      <div class="card-block">
        <p class="card-block-label">장소 소개</p>
        <p>
          작센 선제후 아우구스트 2세(강왕)의 명으로 건축가 마테우스 다니엘 푀펠만이 설계한 후기 바로크 걸작입니다.
          원래는 궁정 축제와 토너먼트를 위한 공간이었으나, 이후 유럽 최고의 박물관 단지로 변모했습니다.
          내부에는 <strong>라파엘로의 「시스티나의 성모」</strong>를 소장한 회화관(Gemäldegalerie Alte Meister),
          도자기 컬렉션, 수학·물리학 박물관이 있습니다.
        </p>
      </div>

      <div class="card-block">
        <p class="card-block-label">종교개혁 · 기독교적 관점</p>
        <p>
          아우구스트 2세는 폴란드 왕위를 얻기 위해 가톨릭으로 개종했지만, 드레스덴 시민 대부분은 루터교 신자였습니다.
          츠빙거 내 회화관에 소장된 라파엘로의 「시스티나의 성모」는 가톨릭 성화이지만,
          당시 개신교 예술가들에게도 깊은 영향을 준 작품입니다.
          종교개혁 이후 예술이 어떻게 세속적·종교적 공간을 동시에 채워나갔는지를 보여주는 공간입니다.
        </p>
      </div>

      <div class="card-block">
        <p class="card-block-label">관광 팁</p>
        <div class="tip-box">
          <p>
            ✦ 회화관 단독 입장 약 €14 / 츠빙거 종합권 €24.<br>
            ✦ 「시스티나의 성모」는 1관 입구에 가까운 별도 공간에 전시 — 줄이 길 수 있으니 개관 직후(10:00) 방문 추천.<br>
            ✦ 안뜰(Innenhof)은 무료 입장이며 분수와 바로크 조각 감상 가능.<br>
            ✦ 박물관 내 카페테리아보다 안뜰 내 카페가 분위기가 좋습니다.<br>
            ✦ 개관 시간: 화–일 10:00–18:00 (월요일 휴관).
          </p>
        </div>
      </div>

      <div class="card-block">
        <p class="card-block-label">가는 길 — 프라하 출발</p>
        <div class="route-steps">
          <span class="route-step"><span class="icon">🚂</span> 프라하 중앙역 → 드레스덴 중앙역 (약 2–2.5시간, EC/RE 열차)</span>
          <span class="route-step"><span class="icon">🚋</span> 트램 8번 Theaterplatz 하차</span>
          <span class="route-step"><span class="icon">🚶</span> 도보 2분</span>
        </div>
        <p style="margin-top:.8rem; font-size:.88rem; color:var(--stone);">
          프라하↔드레스덴 구간은 하루 여러 편 운행. 체코 CD사와 독일 DB사 모두 예매 가능.
          드레스덴 중앙역에서 츠빙거까지 트램으로 10분 내외입니다.
        </p>
      </div>
    </div>
  </section>

  <section class="section" id="stallhof" style="padding-top:0;">
    <p class="section-label">드레스덴 두 번째 명소</p>
    <h2 class="section-title">슈탈호프 & 군주의 행렬</h2>
    <p class="section-intro">
      마이센 도자기 타일 25,000장으로 이루어진 세계 최대의 벽화. 루터를 보호한 작센 군주들의 역사가 102m에 걸쳐 펼쳐집니다.
    </p>

    <div class="landmark-card reveal">
      <img src="IE002164600_STD.jpg" alt="슈탈호프 군주의 행렬 드레스덴" class="landmark-photo" />
      <h3 class="landmark-name">슈탈호프 &amp; 퓌르스텐추크</h3>
      <p class="landmark-name-en">Stallhof · Fürstenzug (Procession of Princes)</p>

      <div class="card-block">
        <p class="card-block-label">장소 소개</p>
        <p>
          슈탈호프(옛 마구간 뜰)는 1591년 르네상스 양식으로 완성된 궁정 마구간 단지입니다.
          외벽에는 세계 최대의 도자기 벽화 <strong>「퓌르스텐추크(군주의 행렬)」</strong>가 펼쳐져 있습니다.
          마이센 도자기 타일 25,000장으로 이루어진 이 102m 길이 벽화는
          1127년부터 1904년까지 작센을 다스린 35명의 군주를 기마 행렬로 묘사합니다.
        </p>
      </div>

      <div class="card-block">
        <p class="card-block-label">종교개혁 · 기독교적 관점</p>
        <p>
          행렬에는 루터의 열렬한 후원자였던 <strong>선제후 프리드리히 3세(현명공)</strong>와
          종교개혁 이후 작센을 루터교 국가로 확립한 군주들이 포함되어 있습니다.
          작센이 없었다면 루터는 보름스 제국의회 이후 처형되었을 가능성이 높습니다.
          프리드리히 3세가 루터를 바르트부르크 성에 숨겨주고 보호한 결정이
          종교개혁을 살아남게 했습니다. 이 벽화는 그 역사의 증인입니다.
        </p>
      </div>

      <div class="card-block">
        <p class="card-block-label">관광 팁</p>
        <div class="tip-box">
          <p>
            ✦ 외벽 벽화(퓌르스텐추크)는 <strong>무료</strong>로 감상 가능 — 오거스투스 거리(Augustusstraße)를 걸으며 볼 수 있습니다.<br>
            ✦ 슈탈호프 안뜰 내부는 이벤트 시즌에만 개방됩니다 (드레스덴 크리스마스 마켓 등).<br>
            ✦ 벽화 앞에서 군주들을 하나씩 찾아보는 "작센 역사 퀴즈"를 해보세요.<br>
            ✦ 인근 레지덴츠 궁전(Residenzschloss)과 묶어 방문하면 효율적입니다 (도보 2분).
          </p>
        </div>
      </div>

      <div class="card-block">
        <p class="card-block-label">가는 길 — 츠빙거에서</p>
        <div class="route-steps">
          <span class="route-step"><span class="icon">🚶</span> 츠빙거에서 도보 5분</span>
          <span class="route-step"><span class="icon">📍</span> Augustusstraße, 01067 Dresden</span>
        </div>
        <p style="margin-top:.8rem; font-size:.88rem; color:var(--stone);">
          츠빙거 → 슈탈호프 → 젬퍼 오페라 → 엘베 강변 산책으로 이어지는 코스가 드레스덴 역사지구를 가장 효율적으로 돌아볼 수 있는 루트입니다.
        </p>
      </div>
    </div>
  </section>

  <section class="section" id="semper" style="padding-top:0;">
    <p class="section-label">드레스덴 세 번째 명소</p>
    <h2 class="section-title">젬퍼 오페라</h2>
    <p class="section-intro">
      바그너와 슈트라우스가 초연을 올린 무대. 루터교 음악 전통이 꽃피운 드레스덴 문화의 정점입니다.
    </p>

    <div class="landmark-card reveal">
      <img src="e2add96b-831e-475b-bd0f-5dafeb5dc346.webp" alt="젬퍼 오페라 드레스덴" class="landmark-photo" />
      <h3 class="landmark-name">젬퍼오퍼</h3>
      <p class="landmark-name-en">Semperoper Dresden · 작센 주립 오페라 극장</p>

      <div class="card-block">
        <p class="card-block-label">장소 소개</p>
        <p>
          건축가 고트프리트 젬퍼가 설계한 신르네상스 양식의 오페라 극장으로, 1841년 초연 이후
          리하르트 바그너, 리하르트 슈트라우스의 주요 작품들이 세계 초연된 무대입니다.
          2차 대전 폭격으로 전소된 뒤 1985년 원래 설계대로 복원되어 오늘에 이릅니다.
          츠빙거 광장과 엘베 강변 사이에 위치하여 드레스덴 스카이라인의 핵심을 이룹니다.
        </p>
      </div>

      <div class="card-block">
        <p class="card-block-label">종교개혁 · 기독교적 관점</p>
        <p>
          젬퍼오퍼는 종교개혁의 직접적 유산은 아니지만, 루터교가 독일 음악 문화에 미친 영향의 결실입니다.
          루터 자신이 음악을 "신학 다음으로 중요한 것"이라 불렀고, 코랄(찬송) 전통을 개신교 예배에 도입했습니다.
          그 전통은 J.S. 바흐와 헨델을 거쳐 독일 오페라·교향악으로 이어집니다.
          같은 역사지구 내 <strong>호프키르헤(가톨릭 궁정 교회)</strong>와 
          <strong>프라우엔키르헤(루터교 성모 교회)</strong>가 젬퍼오퍼 인근에 있어 
          두 신앙의 공존을 직접 목격할 수 있습니다.
        </p>
      </div>

      <div class="card-block">
        <p class="card-block-label">관광 팁</p>
        <div class="tip-box">
          <p>
            ✦ 공연이 없어도 <strong>낮 투어(Führungen)</strong>를 통해 내부를 볼 수 있습니다 — 약 €14, 영어 투어 매일 운영.<br>
            ✦ 공연 티켓은 드레스덴 필하모닉과 국립 오케스트라 모두 추천. 특히 슈트라우스 작품은 이 무대에서 들어야 합니다.<br>
            ✦ 공연 관람 전후로 엘베 강변 테라체(Brühlsche Terrasse)에서 일몰을 감상하세요 — "유럽의 발코니"라 불리는 곳입니다.<br>
            ✦ 건물 외관만 보아도 충분히 아름다우며, 광장에서 사진 촬영 명소입니다.<br>
            ✦ 인근 프라우엔키르헤(재건된 루터교 교회)를 반드시 함께 방문하세요.
          </p>
        </div>
      </div>

      <div class="card-block">
        <p class="card-block-label">가는 길 — 슈탈호프에서</p>
        <div class="route-steps">
          <span class="route-step"><span class="icon">🚶</span> 슈탈호프에서 도보 3분</span>
          <span class="route-step"><span class="icon">📍</span> Theaterplatz 2, 01067 Dresden</span>
        </div>
        <p style="margin-top:.8rem; font-size:.88rem; color:var(--stone);">
          드레스덴 역사지구 전체가 반경 500m 내에 위치해 있어 모든 명소를 걸어서 이동 가능합니다.
        </p>
      </div>
    </div>
  </section>

  <div style="background:var(--aged); padding:1px 0;">
    <section class="section" id="practical">
      <p class="section-label">출발 전 확인</p>
      <h2 class="section-title">프라하에서 가는 길</h2>

      <div class="route-overview">
        <div class="route-row">
          <span class="route-city">프라하</span>
          <span class="route-arrow">→</span>
          <span class="route-city highlight">드레스덴</span>
          <span class="route-detail">EC 열차 · 약 2시간 · db.de 또는 cd.cz 예매</span>
        </div>
        <div class="route-row">
          <span class="route-city">드레스덴</span>
          <span class="route-arrow">→</span>
          <span class="route-city highlight">비텐베르크</span>
          <span class="route-detail">RE 열차 · 약 1시간 30분 · 드레스덴 당일치기 후 이동 추천</span>
        </div>
        <div class="route-row">
          <span class="route-city">드레스덴 중앙역</span>
          <span class="route-arrow">→</span>
          <span class="route-city highlight">츠빙거·젬퍼</span>
          <span class="route-detail">트램 8번 Theaterplatz 하차 · 약 10분</span>
        </div>
        <div class="route-row">
          <span class="route-city">비텐베르크 역</span>
          <span class="route-arrow">→</span>
          <span class="route-city highlight">루터하우스·성교회</span>
          <span class="route-detail">도보 15분 · 구시가 전체 도보 이동 가능</span>
        </div>
      </div>
    </section>
  </div>

  <footer>
    <span class="footer-logo">종교개혁의 길</span>
    <p>프라하에서 떠나는 비텐베르크 &amp; 드레스덴 역사 순례 가이드</p>
    <p style="margin-top:.5rem; opacity:.5;">
      Wittenberg · Dresden · Praha — Reformation Heritage Trail
    </p>
  </footer>

  <script>
    /* Scroll reveal */
    const observer = new IntersectionObserver(
      entries => entries.forEach(e => {
        if (e.isIntersecting) {
          e.target.classList.add('visible');
          observer.unobserve(e.target);
        }
      }),
      { threshold: 0.1 }
    );
    document.querySelectorAll('.reveal').forEach(el => observer.observe(el));

    /* Image fallback — if local images fail, try alternate local images */
    const fallbacks = {
      '루터하우스':  '1640518635_K8u_Lutherhaus.jpg',
      '비텐베르크 성교회': '꾸미기_SAM_5409.jpeg',
      '드레스덴 츠빙거': '6377525081872117370.jpg',
      '슈탈호프':    'IE002164600_STD.jpg',
      '젬퍼 오페라': 'e2add96b-831e-475b-bd0f-5dafeb5dc346.webp',
    };

    document.querySelectorAll('.landmark-photo').forEach(img => {
      img.addEventListener('error', function () {
        const alt = this.alt;
        const key = Object.keys(fallbacks).find(k => alt.includes(k.split(' ')[0]));
        if (key && this.src !== fallbacks[key]) {
          this.src = fallbacks[key];
        } else {
          /* Final fallback: styled placeholder */
          this.style.display = 'none';
          const ph = document.createElement('div');
          ph.className = 'photo-placeholder';
          ph.textContent = this.alt;
          this.parentNode.insertBefore(ph, this);
        }
      });
    });
  </script>

</body>
</html>
