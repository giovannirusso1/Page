[landing_page_consultoria_v2.html](https://github.com/user-attachments/files/27408526/landing_page_consultoria_v2.html)
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
* { margin:0; padding:0; box-sizing:border-box; }
body { font-family:'Inter',sans-serif; background:#0a1a0e; color:#fff; font-size:15px; line-height:1.6; }

.wrap { max-width:640px; margin:0 auto; padding:0 20px; }

/* HERO */
.hero { padding:52px 20px 44px; text-align:center; background:radial-gradient(ellipse at 70% 0%, #1a3a1a 0%, #0a1a0e 60%); }
.badge { display:inline-block; background:rgba(125,217,88,0.12); border:1px solid rgba(125,217,88,0.28); color:#7dd958; font-size:11px; font-weight:700; letter-spacing:1.5px; text-transform:uppercase; padding:6px 16px; border-radius:100px; margin-bottom:22px; }
.hero h1 { font-family:'Bebas Neue',sans-serif; font-size:clamp(48px,11vw,88px); line-height:0.92; margin-bottom:14px; }
.hero h1 span { color:#7dd958; }
.hero p { font-size:15px; color:rgba(255,255,255,0.6); max-width:460px; margin:0 auto 28px; }
.hero p strong { color:#fff; }

.price-pill { display:inline-flex; align-items:center; gap:14px; background:#f0b429; border-radius:14px; padding:14px 28px; margin-bottom:20px; }
.price-pill .pp-label { font-size:12px; font-weight:700; color:rgba(26,26,26,0.6); text-transform:uppercase; letter-spacing:1px; }
.price-pill .pp-price { font-family:'Bebas Neue',sans-serif; font-size:64px; color:#1a1a1a; line-height:1; }
.price-pill .pp-once { font-size:11px; font-weight:700; color:rgba(26,26,26,0.5); text-transform:uppercase; }

.cta { display:inline-flex; align-items:center; gap:10px; background:#25d366; color:#fff; font-size:16px; font-weight:700; padding:16px 32px; border-radius:100px; border:none; cursor:pointer; text-decoration:none; box-shadow:0 4px 32px rgba(37,211,102,0.28); transition:transform 0.18s; }
.cta:hover { transform:translateY(-2px); }
.cta svg { width:20px; height:20px; flex-shrink:0; }
.urgency { margin-top:10px; font-size:12px; color:rgba(255,255,255,0.4); }
.urgency b { color:#f0b429; }

.proof { display:flex; align-items:center; justify-content:center; gap:10px; margin-top:28px; padding-top:24px; border-top:1px solid rgba(255,255,255,0.07); }
.avatars { display:flex; }
.av { width:32px; height:32px; border-radius:50%; border:2px solid #0a1a0e; background:#1e3d1e; display:flex; align-items:center; justify-content:center; font-size:10px; font-weight:700; color:#7dd958; margin-left:-7px; }
.av:first-child { margin-left:0; }
.proof-txt { font-size:13px; color:rgba(255,255,255,0.5); text-align:left; }
.proof-txt strong { color:#fff; }
.stars { color:#f0b429; font-size:13px; }

/* SECTIONS */
.sec { padding:44px 20px; }
.sec-alt { background:#0d1f10; }
.sec-label { font-size:11px; font-weight:700; letter-spacing:2px; text-transform:uppercase; color:#7dd958; margin-bottom:8px; }
.sec-title { font-family:'Bebas Neue',sans-serif; font-size:clamp(32px,7vw,52px); line-height:0.96; margin-bottom:20px; }
.sec-title span { color:#7dd958; }

/* PAIN */
.pain-list { list-style:none; display:flex; flex-direction:column; gap:8px; }
.pain-list li { display:flex; align-items:flex-start; gap:12px; background:rgba(255,255,255,0.03); border:1px solid rgba(255,255,255,0.07); border-radius:10px; padding:12px 16px; font-size:14px; color:rgba(255,255,255,0.7); }
.pain-list li .ico { font-size:16px; flex-shrink:0; margin-top:1px; }
.pain-quote { margin-top:20px; font-size:14px; color:rgba(255,255,255,0.6); line-height:1.65; border-left:3px solid #7dd958; padding-left:16px; }
.pain-quote strong { color:#fff; }

/* INCLUDES */
.inc-grid { display:grid; grid-template-columns:1fr 1fr; gap:10px; margin-top:20px; }
.inc-card { background:rgba(125,217,88,0.05); border:1px solid rgba(125,217,88,0.18); border-radius:12px; padding:18px 16px; }
.inc-icon { font-size:22px; margin-bottom:8px; display:block; }
.inc-title { font-size:14px; font-weight:700; color:#fff; margin-bottom:4px; }
.inc-desc { font-size:12px; color:rgba(255,255,255,0.45); line-height:1.5; }
.inc-tag { display:inline-block; margin-top:8px; background:#f0b429; color:#1a1a1a; font-size:10px; font-weight:700; text-transform:uppercase; padding:3px 8px; border-radius:5px; }

/* STEPS */
.steps { display:flex; flex-direction:column; gap:0; margin-top:24px; }
.step { display:flex; gap:16px; padding-bottom:24px; position:relative; }
.step:not(:last-child)::after { content:''; position:absolute; left:15px; top:36px; width:2px; bottom:0; background:rgba(125,217,88,0.18); }
.step-num { width:32px; height:32px; border-radius:50%; flex-shrink:0; background:#7dd958; color:#0a1a0e; display:flex; align-items:center; justify-content:center; font-size:14px; font-weight:700; }
.step-title { font-size:15px; font-weight:700; margin-bottom:3px; }
.step-desc { font-size:13px; color:rgba(255,255,255,0.48); line-height:1.55; }

/* GUARANTEE */
.guarantee { background:rgba(240,180,41,0.07); border:1px solid rgba(240,180,41,0.22); border-radius:14px; padding:24px; margin:0 20px; display:flex; gap:16px; align-items:flex-start; }
.g-icon { font-size:32px; flex-shrink:0; }
.g-title { font-size:16px; font-weight:700; color:#f0b429; margin-bottom:5px; }
.g-desc { font-size:13px; color:rgba(255,255,255,0.55); line-height:1.6; }

/* FINAL CTA */
.final { padding:44px 20px; text-align:center; background:#0d1f10; }
.final-title { font-family:'Bebas Neue',sans-serif; font-size:clamp(36px,8vw,68px); line-height:0.95; margin-bottom:8px; }
.final-title span { color:#7dd958; }
.final-sub { font-size:14px; color:rgba(255,255,255,0.45); margin-bottom:24px; }
.price-from { font-size:13px; color:rgba(255,255,255,0.25); text-decoration:line-through; }
.price-big { font-family:'Bebas Neue',sans-serif; font-size:80px; color:#f0b429; line-height:1; }
.price-once { font-size:12px; color:rgba(255,255,255,0.35); text-transform:uppercase; letter-spacing:1px; margin-bottom:24px; }
.trust { margin-top:12px; font-size:12px; color:rgba(255,255,255,0.25); }

footer { padding:18px 20px; text-align:center; border-top:1px solid rgba(255,255,255,0.06); font-size:11px; color:rgba(255,255,255,0.2); }
</style>
</head>
<body>

<!-- HERO -->
<div class="hero">
  <div class="wrap">
    <div class="badge">Consultoria · App · Acompanhamento</div>
    <h1>Chega de viver<br><span>apertado</span><br>todo mês.</h1>
    <p>Eu te ajudo a organizar suas finanças em <strong>7 dias</strong> e fazer seu dinheiro finalmente sobrar — com plano personalizado e acompanhamento individual.</p>

    <div class="price-pill">
      <div>
        <div class="pp-label">Tudo isso por</div>
        <div class="pp-price">R$97</div>
        <div class="pp-once">Investimento único</div>
      </div>
    </div><br>

    <a class="cta" href="https://wa.me/5551999999999" target="_blank">
      <svg viewBox="0 0 24 24" fill="currentColor"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347z"/><path d="M12 0C5.373 0 0 5.373 0 12c0 2.123.558 4.116 1.532 5.845L.072 23.999l6.284-1.648A11.94 11.94 0 0012 24c6.627 0 12-5.373 12-12S18.627 0 12 0zm0 21.818a9.806 9.806 0 01-5.032-1.387l-.361-.214-3.731.978.996-3.648-.235-.374A9.794 9.794 0 012.182 12C2.182 6.57 6.57 2.182 12 2.182S21.818 6.57 21.818 12 17.43 21.818 12 21.818z"/></svg>
      Quero começar agora — WhatsApp
    </a>
    <p class="urgency"><b>⚠ Vagas limitadas</b> — atendimento individual e personalizado</p>

    <div class="proof">
      <div class="avatars">
        <div class="av">MC</div><div class="av">RS</div><div class="av">LP</div><div class="av">TF</div><div class="av">+</div>
      </div>
      <div class="proof-txt">
        <div class="stars">★★★★★</div>
        <strong>+250 pessoas</strong> já mudaram de vida
      </div>
    </div>
  </div>
</div>

<!-- DOR -->
<div class="sec sec-alt">
  <div class="wrap">
    <div class="sec-label">Você se identifica?</div>
    <div class="sec-title">Você trabalha o mês inteiro e<br><span>o dinheiro some.</span></div>
    <ul class="pain-list">
      <li><span class="ico">💸</span>Chega no fim do mês e não sobra nada, mesmo trabalhando muito</li>
      <li><span class="ico">😰</span>Não sabe exatamente para onde vai seu dinheiro</li>
      <li><span class="ico">😓</span>Tem dívidas que parecem não acabar nunca</li>
      <li><span class="ico">🔄</span>Já tentou planilhas e apps, mas abandonou em poucos dias</li>
    </ul>
    <p class="pain-quote">Sem método e sem acompanhamento, o ciclo não muda. <strong>A diferença é ter alguém te guiando passo a passo.</strong></p>
  </div>
</div>

<!-- INCLUSO -->
<div class="sec">
  <div class="wrap">
    <div class="sec-label">O que está incluso</div>
    <div class="sec-title">Tudo para você <span>virar o jogo</span></div>
    <div class="inc-grid">
      <div class="inc-card">
        <span class="inc-icon">📋</span>
        <div class="inc-title">Plano personalizado</div>
        <div class="inc-desc">Feito para sua realidade e seus objetivos</div>
      </div>
      <div class="inc-card">
        <span class="inc-icon">💬</span>
        <div class="inc-title">7 dias de acompanhamento</div>
        <div class="inc-desc">Acesso direto comigo durante toda a consultoria</div>
      </div>
      <div class="inc-card">
        <span class="inc-icon">📊</span>
        <div class="inc-title">Organização completa</div>
        <div class="inc-desc">Gastos, receitas e metas sob controle</div>
      </div>
      <div class="inc-card">
        <span class="inc-icon">📱</span>
        <div class="inc-title">App de controle</div>
        <div class="inc-desc">1 mês de acesso ao app financeiro</div>
        <span class="inc-tag">Grátis</span>
      </div>
    </div>
  </div>
</div>

<!-- COMO FUNCIONA -->
<div class="sec sec-alt">
  <div class="wrap">
    <div class="sec-label">Como funciona</div>
    <div class="sec-title">Em 7 dias você já <span>sente a diferença</span></div>
    <div class="steps">
      <div class="step">
        <div class="step-num">1</div>
        <div>
          <div class="step-title">Você entra em contato pelo WhatsApp</div>
          <div class="step-desc">Conversamos sobre sua situação, seus gastos e seus objetivos.</div>
        </div>
      </div>
      <div class="step">
        <div class="step-num">2</div>
        <div>
          <div class="step-title">Eu monto seu plano personalizado</div>
          <div class="step-desc">Um plano prático e realista para a sua rotina.</div>
        </div>
      </div>
      <div class="step">
        <div class="step-num">3</div>
        <div>
          <div class="step-title">7 dias de acompanhamento individual</div>
          <div class="step-desc">Tiro dúvidas, ajusto o plano e te mantenho no caminho.</div>
        </div>
      </div>
      <div class="step" style="padding-bottom:0;">
        <div class="step-num">4</div>
        <div>
          <div class="step-title">Resultado: dinheiro sobrando todo mês</div>
          <div class="step-desc">Com método e controle, você toma decisões com confiança.</div>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- GARANTIA -->
<div style="padding:32px 0;">
  <div class="guarantee" style="max-width:600px; margin:0 auto;">
    <div class="g-icon">🛡️</div>
    <div>
      <div class="g-title">Garantia de 7 dias</div>
      <div class="g-desc">Se não sentir que valeu cada centavo, eu devolvo seu dinheiro. Sem perguntas, sem burocracia. O risco é todo meu.</div>
    </div>
  </div>
</div>

<!-- FINAL CTA -->
<div class="final">
  <div class="wrap">
    <div class="sec-label">Pronto para mudar?</div>
    <div class="final-title">Pare de viver<br><span>apertado</span> agora.</div>
    <p class="final-sub">Uma decisão de R$97 pode mudar sua vida financeira para sempre.</p>
    <div class="price-from">De R$ 297</div>
    <div class="price-big">R$97</div>
    <div class="price-once">Investimento único</div>
    <a class="cta" href="https://wa.me/5551999999999" target="_blank" style="display:inline-flex;">
      <svg viewBox="0 0 24 24" fill="currentColor" style="width:20px;height:20px"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347z"/><path d="M12 0C5.373 0 0 5.373 0 12c0 2.123.558 4.116 1.532 5.845L.072 23.999l6.284-1.648A11.94 11.94 0 0012 24c6.627 0 12-5.373 12-12S18.627 0 12 0zm0 21.818a9.806 9.806 0 01-5.032-1.387l-.361-.214-3.731.978.996-3.648-.235-.374A9.794 9.794 0 012.182 12C2.182 6.57 6.57 2.182 12 2.182S21.818 6.57 21.818 12 17.43 21.818 12 21.818z"/></svg>
      Quero começar agora — WhatsApp
    </a>
    <p class="trust">🔒 Garantia de 7 dias · Vagas limitadas · Atendimento individual</p>
  </div>
</div>

<footer>© 2026 Consultoria Financeira · Todos os direitos reservados</footer>

</body>
</html>
