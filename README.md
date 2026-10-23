# AmselianVisuals.github.io<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>AMSELIAN VISUALS — визуалы для Minecraft</title>
<script>try{var t=localStorage.getItem('av_theme');if(t==='light'||t==='dark')document.documentElement.setAttribute('data-theme',t)}catch(e){}</script>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Onest:wght@400;500;600&family=Unbounded:wght@500;700&display=swap" rel="stylesheet">
<style>
:root{
  --bg:#ffffff; --surface:#f6f2ff; --ink:#2a1f4d; --muted:#6b5f8f; --line:#d9cff5;
  --beak:#7a5ce6; --beak-ink:#ffffff; --sheen:#b79cff;
  --sky1:#c9b8ff; --sky2:#f0e9ff; --ground:#5b4a8f;
  box-sizing:border-box;
  padding-top:env(safe-area-inset-top,0px); padding-bottom:env(safe-area-inset-bottom,0px);
  color-scheme:light dark;
}
@media (prefers-color-scheme: dark){
  :root:not([data-theme="light"]){
    --bg:#171229; --surface:#221b3d; --ink:#f1ebff; --muted:#b3a8d6; --line:#352c5c;
    --beak:#b69cff; --beak-ink:#1b1038; --sheen:#c9b8ff;
    --sky1:#2e2370; --sky2:#7a62d6; --ground:#1b1433;
  }
}
:root[data-theme="dark"]{
  --bg:#171229; --surface:#221b3d; --ink:#f1ebff; --muted:#b3a8d6; --line:#352c5c;
  --beak:#b69cff; --beak-ink:#1b1038; --sheen:#c9b8ff;
  --sky1:#2e2370; --sky2:#7a62d6; --ground:#1b1433;
}
html{scroll-padding-top:env(safe-area-inset-top,0px);scroll-behavior:smooth}
*,*::before,*::after{box-sizing:inherit}
body{margin:0;background:var(--bg);color:var(--ink);font:400 17px/1.6 Onest,system-ui,-apple-system,"Segoe UI",Roboto,sans-serif}
a{color:inherit}
:focus-visible{outline:3px solid var(--beak);outline-offset:3px}
.wrap{max-width:1040px;margin:0 auto;padding:0 20px}
h1,h2,h3{font-family:Unbounded,Onest,system-ui,sans-serif;line-height:1.15;margin:0}
nav{display:flex;align-items:center;justify-content:space-between;padding:18px 0}
.logo{font-family:Unbounded,sans-serif;font-weight:700;font-size:15px;letter-spacing:.04em;text-decoration:none}
.logo b{color:var(--beak)}
.navlinks{display:flex;gap:20px;font-size:15px}
.navlinks a{text-decoration:none;color:var(--muted)}
.navlinks a:hover{color:var(--ink)}
.hero{padding:36px 0 56px}
.hero h1{font-size:clamp(34px,8.5vw,76px);font-weight:700;letter-spacing:-.02em;max-width:14ch}
.lav{color:#9b7ff0}
@media (prefers-color-scheme: dark){:root:not([data-theme="light"]) .lav{color:#b69cff}}
:root[data-theme="dark"] .lav{color:#b69cff}
.hero p.lead{max-width:52ch;color:var(--muted);font-size:19px;margin:20px 0 28px}
.btn{display:inline-block;background:var(--beak);color:var(--beak-ink);font-weight:600;text-decoration:none;padding:14px 26px;border-radius:999px;border:0;font:600 17px Onest,sans-serif;cursor:pointer}
.btn:hover{filter:brightness(1.08)}
.btn.ghost{background:transparent;color:var(--ink);border:1.5px solid var(--line);margin-left:8px}
/* demo */
.demo{background:var(--surface);border:1px solid var(--line);border-radius:20px;overflow:hidden}
.scene{position:relative;height:320px;background:linear-gradient(var(--sky1),var(--sky2));overflow:hidden;cursor:crosshair;touch-action:manipulation}
.scene.night-off{background:linear-gradient(#e3d8ff,#faf6ff)}
.ground{position:absolute;left:0;right:0;bottom:0;height:90px;background:var(--ground);
  background-image:linear-gradient(90deg,rgba(255,255,255,.06) 1px,transparent 1px),linear-gradient(rgba(255,255,255,.06) 1px,transparent 1px);background-size:36px 36px}
.mob{position:absolute;left:58%;bottom:90px;width:44px;height:92px;background:var(--sheen);border-radius:4px;transition:transform .12s}
.mob::before{content:"";position:absolute;top:-34px;left:2px;width:40px;height:34px;background:#9a82e8;border-radius:4px}
.mob.hit{transform:translateX(10px);filter:brightness(1.8)}
.p{position:absolute;width:8px;height:8px;pointer-events:none;border-radius:1px;animation:fly .7s ease-out forwards}
@keyframes fly{to{transform:translate(var(--dx),var(--dy)) scale(.2);opacity:0}}
.hud{position:absolute;inset:0;pointer-events:none;font:500 13px/1.4 Onest,sans-serif;color:#fff;text-shadow:0 1px 3px rgba(0,0,0,.7)}
.hud>div{position:absolute}
.hud .mods{top:12px;right:14px;text-align:right}
.hud .mods span{display:block}
.hud .mods span:nth-child(1){color:#e4d9ff}.hud .mods span:nth-child(2){color:#c9b8ff}.hud .mods span:nth-child(3){color:#f0c6ff}
.hud .info{top:12px;left:14px}
.hud .bar{bottom:100px;left:50%;transform:translateX(-50%);display:flex;gap:3px}
.hud .bar i{width:14px;height:14px;background:#d66bd9;display:block;border:1px solid rgba(0,0,0,.4)}
.crosshair{position:absolute;left:50%;top:44%;width:16px;height:16px;transform:translate(-50%,-50%);pointer-events:none}
.crosshair::before,.crosshair::after{content:"";position:absolute;background:var(--beak);left:50%;top:50%;transform:translate(-50%,-50%)}
.crosshair::before{width:2px;height:16px}.crosshair::after{width:16px;height:2px}
.off{display:none!important}
.toggles{display:flex;flex-wrap:wrap;gap:10px;padding:16px}
.toggles label{display:flex;align-items:center;gap:8px;padding:9px 14px;border:1.5px solid var(--line);border-radius:999px;cursor:pointer;font-size:15px;user-select:none}
.toggles input{accent-color:var(--beak);width:18px;height:18px;margin:0}
.toggles label:has(input:checked){border-color:var(--beak)}
.hint{padding:0 16px 16px;color:var(--muted);font-size:14px;margin:0}
/* sections */
section{padding:56px 0}
section>.wrap>h2{font-size:clamp(24px,5vw,36px);margin-bottom:28px;max-width:20ch}
.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:28px 36px}
.grid h3{font-size:17px;margin-bottom:8px}
.grid p{margin:0;color:var(--muted);font-size:16px}
.rule{border-top:1px solid var(--line);padding-top:18px}
.dl{background:var(--surface);border:1px solid var(--line);border-radius:20px;padding:32px;display:flex;flex-wrap:wrap;gap:24px;align-items:center;justify-content:space-between}
.dl h2{font-size:clamp(22px,4.5vw,30px)}
.dl p{margin:8px 0 0;color:var(--muted)}
details{border-top:1px solid var(--line);padding:16px 0}
details:last-of-type{border-bottom:1px solid var(--line)}
summary{cursor:pointer;font-weight:600}
details p{color:var(--muted);margin:10px 0 0;max-width:60ch}
footer{padding:36px 0 48px;color:var(--muted);font-size:14px}
.scene{position:relative;height:auto;aspect-ratio:16/9;background:#000;overflow:hidden;cursor:crosshair;touch-action:pan-y}
.scene canvas{position:absolute;inset:0;width:100%;height:100%;display:block;image-rendering:pixelated}
#cv-b{clip-path:inset(0 0 0 50%)}
.divider{position:absolute;top:0;bottom:0;left:50%;width:3px;margin-left:-1.5px;background:#fff;box-shadow:0 0 0 1px rgba(0,0,0,.25);cursor:ew-resize;touch-action:none}
.divider::before{content:"";position:absolute;inset:0 -16px}
.divider::after{content:"";position:absolute;top:50%;left:50%;width:28px;height:28px;transform:translate(-50%,-50%);border-radius:50%;background:var(--beak);border:3px solid #fff}
.tag{position:absolute;bottom:8px;padding:4px 10px;border-radius:999px;font:600 13px Onest,system-ui,sans-serif;background:rgba(30,16,70,.7);color:#fff;pointer-events:none}
.tag.l{left:8px}.tag.r{right:8px}
.ctl{padding:14px 16px 0}.ctl input{width:100%;accent-color:var(--beak)}
.intro{position:fixed;inset:0;z-index:100;display:flex;flex-direction:column;align-items:center;justify-content:center;background:radial-gradient(circle at 50% 45%,rgba(155,127,240,.3),transparent 65%),var(--bg);cursor:pointer;animation:introOut .8s 2.5s ease forwards}
.intro .word{display:flex;font:700 clamp(30px,10vw,92px) Unbounded,system-ui,sans-serif;letter-spacing:.02em}
.intro .word span{opacity:0;transform:translateY(28px) scale(.9);filter:blur(14px);animation:letterIn .7s cubic-bezier(.2,.8,.2,1) forwards;animation-delay:calc(.15s + var(--i)*.09s)}
.intro .line{height:3px;width:0;margin-top:18px;background:linear-gradient(90deg,transparent,#b69cff,transparent);animation:lineIn .8s 1.1s ease forwards}
.intro .sub{margin-top:14px;padding-left:.5em;font:500 clamp(12px,2.6vw,16px) Onest,system-ui,sans-serif;letter-spacing:.5em;color:var(--muted);opacity:0;animation:subIn .8s 1.4s ease forwards}
@keyframes letterIn{to{opacity:1;transform:none;filter:blur(0)}}
@keyframes lineIn{to{width:min(60vw,420px)}}
@keyframes subIn{to{opacity:1}}
@keyframes introOut{to{opacity:0;visibility:hidden;transform:scale(1.04);filter:blur(6px)}}
@media (prefers-reduced-motion:reduce){.intro{display:none}}
.gui{border-radius:20px;border:1px solid var(--line);padding:18px;color:#f1ebff;background:linear-gradient(rgba(20,10,50,.62),rgba(20,10,50,.62)),linear-gradient(#b9a4ff,#ebe2ff)}
.gui-top{display:flex;align-items:center;gap:8px;margin-bottom:16px;font:700 14px Unbounded,Onest,sans-serif;letter-spacing:.03em}
.gui-top i{font-style:normal;color:#b69cff}
.gui-top span{margin-left:auto;font:500 13px Onest,system-ui,sans-serif;letter-spacing:0;color:#cdbcff;border:1px solid rgba(182,156,255,.45);padding:3px 10px;border-radius:999px}
.gui-cols{display:grid;grid-template-columns:repeat(auto-fit,minmax(170px,1fr));gap:12px}
.gp{background:rgba(24,16,52,.8);border-radius:12px;overflow:hidden}
.gp h3{margin:0;padding:10px 12px;font:600 13px Unbounded,Onest,sans-serif;border-left:3px solid #b69cff;background:rgba(182,156,255,.14)}
.gr{display:flex;align-items:center;justify-content:space-between;gap:10px;padding:9px 12px;font-size:14px;cursor:pointer}
.gr:hover{background:rgba(182,156,255,.1)}
.sw{-webkit-appearance:none;appearance:none;flex:none;width:30px;height:16px;border-radius:999px;background:rgba(255,255,255,.2);position:relative;margin:0;cursor:pointer;transition:background .2s}
.sw::after{content:"";position:absolute;top:2px;left:2px;width:12px;height:12px;border-radius:50%;background:#fff;transition:transform .2s}
.sw:checked{background:#8d70ee}.sw:checked::after{transform:translateX(14px)}
.ag{display:grid;grid-template-columns:210px 1fr;border-radius:20px;overflow:hidden;background:#15111f;border:1px solid #2a2140;color:#f1ebff;min-height:440px}
.ag-side{background:#100b19;padding:16px 12px;display:flex;flex-direction:column;gap:6px}
.ag-brand{display:flex;align-items:center;gap:10px;font:600 12px/1.25 Unbounded,Onest,sans-serif;padding:2px 6px 18px}
.ag-logo{flex:none;width:34px;height:34px;border-radius:9px;display:grid;place-items:center;background:linear-gradient(135deg,#c9b8ff,#7a5ce6);color:#1a1030;font:700 18px Unbounded,sans-serif;box-shadow:0 0 18px rgba(155,127,240,.45)}
.ag-logo.sm{width:30px;height:30px;font-size:15px}
.ag-nav{display:flex;flex-direction:column;gap:6px}
.ag-nav button{display:flex;align-items:center;gap:10px;width:100%;padding:11px 14px;border:0;border-radius:12px;background:transparent;color:#b8b0d0;font:500 15px Onest,system-ui,sans-serif;cursor:pointer;text-align:left}
.ag-nav button:hover{background:rgba(182,156,255,.1)}
.ag-nav button.on{background:linear-gradient(90deg,#8d70ee,#b69cff);color:#1a1030;box-shadow:0 4px 20px rgba(155,127,240,.4)}
.ag-user{margin-top:auto;display:flex;align-items:center;gap:10px;padding:8px 6px;font-size:14px}
.ag-user small{display:block;color:#8a82a3}
.ag-main{display:flex;flex-direction:column;min-width:0}
.ag-head{display:flex;align-items:center;gap:14px;padding:16px 24px;border-bottom:1px solid #241c34}
.ag-head b{font:600 17px Onest,system-ui,sans-serif;min-width:64px}
.ag-q{flex:1;max-width:300px;margin:0 auto;background:#1a1428;border:1px solid #2a2140;border-radius:999px;padding:8px 16px;color:#f1ebff;font:400 14px Onest,system-ui,sans-serif;text-align:center}
.ag-q::placeholder{color:#8a82a3}
.ag-list{display:grid;grid-template-columns:repeat(auto-fill,minmax(250px,1fr));gap:0 40px;padding:8px 24px 20px;align-content:start;max-height:440px;overflow-y:auto}
.ag-row{display:flex;justify-content:space-between;gap:14px;padding:16px 0;border-bottom:1px solid rgba(182,156,255,.08)}
.ag-row b{display:block;font:500 16px Onest,system-ui,sans-serif}
.ag-row small{display:block;color:#8a82a3;font-size:13px;margin-top:4px}
.ag-ctl{display:flex;align-items:flex-start;flex:none;gap:10px;padding-top:2px}
.ag-bind{color:#6f6788;font-size:12px;padding-top:3px}
.ag-sw{-webkit-appearance:none;appearance:none;width:42px;height:24px;border-radius:999px;background:#3a3450;position:relative;margin:0;cursor:pointer;transition:background .2s}
.ag-sw::after{content:"";position:absolute;top:3px;left:3px;width:18px;height:18px;border-radius:50%;background:#fff;transition:transform .2s}
.ag-sw:checked{background:linear-gradient(90deg,#8d70ee,#b69cff)}.ag-sw:checked::after{transform:translateX(18px)}
@media (max-width:640px){.ag{grid-template-columns:1fr}.ag-side{flex-direction:row;flex-wrap:wrap;align-items:center}.ag-brand{padding-bottom:2px}.ag-user{display:none}.ag-nav{flex-direction:row;overflow-x:auto;width:100%}.ag-nav button{width:auto;padding:9px 12px;white-space:nowrap}.ag-head{padding:14px 16px}.ag-list{padding:4px 16px 16px}}
.hws{display:grid;grid-template-columns:repeat(auto-fit,minmax(290px,1fr));gap:28px 24px;align-items:start;background:#0c0b10;border:1px solid #221d30;border-radius:24px;padding:30px 22px;color:#f1ebff}
.hcol{display:flex;flex-direction:column;gap:22px;min-width:0}
.hw{position:relative;padding:44px 14px 14px;border:1px solid rgba(255,255,255,.1);border-radius:6px}
.hw.nl{padding-top:14px}
.hw::before{content:"";position:absolute;inset:-3px;pointer-events:none;background:radial-gradient(circle at 3px 3px,#8a8498 2.5px,transparent 3px),radial-gradient(circle at calc(100% - 3px) 3px,#8a8498 2.5px,transparent 3px),radial-gradient(circle at 3px calc(100% - 3px),#8a8498 2.5px,transparent 3px),radial-gradient(circle at calc(100% - 3px) calc(100% - 3px),#8a8498 2.5px,transparent 3px)}
.lbl{position:absolute;top:-1px;left:26px;display:flex;align-items:center;gap:8px;padding:9px 16px 7px;background:#0c0b10;border:1px solid rgba(255,255,255,.1);border-top:0;border-radius:0 0 12px 12px;font:500 15px Onest,system-ui,sans-serif}
.hi{width:18px;height:18px;flex:none;color:#b69cff}
.hc{position:relative;background:#121016;border:1px solid rgba(255,255,255,.08);border-radius:18px;padding:14px 16px}
.hc::after{content:"";position:absolute;left:16%;bottom:-1px;width:42%;height:2px;background:linear-gradient(90deg,transparent,#c9b8ff,transparent)}
.brand{display:flex;align-items:center;gap:12px;font:600 17px Onest,sans-serif;letter-spacing:.02em}
.bl{display:grid;place-items:center;width:28px;height:28px;border-radius:8px;background:linear-gradient(135deg,#c9b8ff,#7a5ce6);color:#1a1030;font:700 15px Unbounded,sans-serif}
.stats{display:flex;flex-wrap:wrap;gap:12px 22px;font-size:17px;align-items:center}
.stats span{display:flex;align-items:center;gap:8px}
.stats b{font-weight:500}
.stats small{color:#a39fb5;font-size:15px}
.dot{width:8px;height:8px;border-radius:50%;background:#b69cff}
.r{display:flex;align-items:center;gap:12px;padding:9px 0;font-size:17px}
.pill{margin-left:auto;background:rgba(155,127,240,.15);color:#d6b8ff;padding:3px 11px;border-radius:8px;font-variant-numeric:tabular-nums}
.r sup{font-size:11px;color:#a39fb5;margin-left:2px}
.ic{width:22px;height:22px;border-radius:6px;flex:none}
.slots{display:flex;gap:10px;flex-wrap:wrap}
.slot{position:relative;width:42px;height:42px;border-radius:11px;background:#1a171f;flex:none}
.it{position:absolute;inset:8px;border-radius:5px 14px 5px 14px}
.cnt{position:absolute;right:3px;bottom:0;font:600 12px Onest,sans-serif;text-shadow:0 1px 2px #000}
.key{position:absolute;right:-2px;bottom:-4px;width:20px;height:20px;border-radius:7px;background:#1a171f;border:1px solid #302a3c;display:grid;place-items:center;font:500 12px Onest,sans-serif}
.ring{display:grid;place-items:center;position:relative;width:120px;margin:0 auto}
.ring svg{width:120px;height:120px;transform:rotate(-90deg)}
.ring span{position:absolute;font:500 19px Onest,sans-serif}
.tg{display:flex;gap:14px}
.face{position:relative;width:74px;height:74px;border-radius:16px;background:linear-gradient(#5aa03e,#478536);flex:none}
.face::before,.face::after{content:"";position:absolute;top:30px;width:14px;height:10px;background:#111}
.face::before{left:15px}.face::after{right:15px}
.tg b{font:500 19px Onest,sans-serif}
.arm{display:flex;gap:6px;align-items:center;margin:8px 0}
.arm i{width:14px;height:14px;border-radius:4px}
.arm span{margin-left:auto;font:500 20px Onest,sans-serif;color:#e4d9ff}
.bar{height:14px;border-radius:8px;background:#26212e;overflow:hidden}
.bar i{display:block;height:100%;width:78%;background:linear-gradient(90deg,#c9b8ff,#a98bff)}
.seg{display:flex;gap:3px;margin-left:auto}
.seg i{width:8px;height:15px;transform:skewX(-20deg);background:#e57bd8}.seg i.w{background:#f1ebff}
.muted{color:#8a82a3}
.inv{display:grid;grid-template-columns:repeat(9,1fr);gap:6px}
.inv .slot{width:auto;height:auto;aspect-ratio:1;border-radius:9px}
.inv .it{inset:6px}
.cover{aspect-ratio:1.15;border-radius:14px;background:radial-gradient(circle at 30% 25%,#e4d9ff,transparent 45%),linear-gradient(135deg,#7a5ce6,#2e1a66 60%,#e57bd8);display:grid;place-items:center;font:700 54px Unbounded,sans-serif;color:rgba(255,255,255,.85)}
.ctl2{display:flex;justify-content:space-around;align-items:center;margin:14px 0 10px;color:#f1ebff}
.ctl2 svg{width:24px;height:24px;fill:currentColor}
.prog{height:4px;border-radius:3px;background:#2e2938;overflow:hidden}
.prog i{display:block;height:100%;width:30%;background:#f1ebff}
.shot{display:block;width:100%;height:auto;border-radius:20px;border:1px solid var(--line)}
.tbtn{display:grid;place-items:center;width:38px;height:38px;padding:0;border-radius:50%;border:1px solid var(--line);background:var(--surface);color:var(--ink);cursor:pointer}
.tbtn:hover{border-color:var(--beak)}
.navr{display:flex;align-items:center;gap:20px}
.btn.sm{padding:9px 18px;font-size:15px}
.view{display:none;padding:24px 0 56px}.view.on{display:block}
.view h1{font-size:clamp(28px,6vw,44px);margin-bottom:24px}
.card{max-width:460px;background:var(--surface);border:1px solid var(--line);border-radius:20px;padding:28px}
.card.wide{max-width:640px}
.f{display:block;font-weight:500;font-size:15px;margin:16px 0 6px}
.t{width:100%;padding:12px 14px;border:1.5px solid var(--line);border-radius:12px;background:var(--bg);color:var(--ink);font:400 16px Onest,system-ui,sans-serif}
textarea.t{min-height:130px;resize:vertical}
.msg{font-size:14px;min-height:20px;margin:12px 0 0;color:#d6453d}
.msg.ok{color:#2f9e6a}
.card .btn{margin-top:18px}
.swap{margin:18px 0 0;color:var(--muted);font-size:15px}
.swap a{color:var(--ink);font-weight:600}
.kv{display:grid;grid-template-columns:auto 1fr;gap:10px 24px;margin:0 0 8px}
.kv dt{color:var(--muted)}.kv dd{margin:0;font-weight:500;word-break:break-all}
.lic{font-family:ui-monospace,Menlo,Consolas,monospace;letter-spacing:.04em}
.row{display:flex;flex-wrap:wrap;gap:10px;margin-top:6px}
.row .btn{margin-top:12px}
.btn.danger{background:transparent;color:#d6453d;border:1.5px solid #d6453d}
.tix{list-style:none;margin:12px 0 0;padding:0}
.tix li{border-top:1px solid var(--line);padding:12px 0}
.tix small{color:var(--muted);display:block}
.note{color:var(--muted);font-size:13px;margin:14px 0 0}
.flinks{display:flex;gap:18px;margin-top:10px}
@media (max-width:560px){.navlinks{display:none}.btn.ghost{margin:10px 0 0}}
@media (prefers-reduced-motion:reduce){*{animation:none!important;transition:none!important;scroll-behavior:auto!important}}
</style>
</head>
<body>
<div class="intro" id="intro" aria-hidden="true"><div class="word lav"><span style="--i:0">A</span><span style="--i:1">M</span><span style="--i:2">S</span><span style="--i:3">E</span><span style="--i:4">L</span><span style="--i:5">I</span><span style="--i:6">A</span><span style="--i:7">N</span></div><div class="line"></div><div class="sub">VISUALS</div></div>
<div class="wrap">
  <nav>
    <a class="logo" href="#top">AMSELIAN <b>VISUALS</b></a>
    <div class="navr"><div class="navlinks"><a href="#features">Возможности</a><a href="#download">Скачать</a><a href="#support">Поддержка</a></div><button class="tbtn" id="theme" type="button" aria-label="Сменить тему"></button><a class="btn sm" id="nav-acct" href="#login">Войти</a></div>
  </nav>

  <header class="hero" id="top">
    <h1>Будь лучше, побеждай с <span class="lav">AMSELIAN</span></h1>
    <p class="lead">AMSELIAN VISUALS меняет только внешний вид игры: эффекты ударов, интерфейс, небо и анимации. Никаких читов и преимуществ в бою.</p>
    <a class="btn" href="#download">Скачать</a><a class="btn ghost" href="#demo">Попробовать ниже</a>
  </header>

  <div class="demo" id="demo">
    <div class="scene" id="scene" aria-label="Сравнение Minecraft без визуалов и с визуалами">
      <canvas id="cv-a" width="320" height="180"></canvas>
      <canvas id="cv-b" width="320" height="180"></canvas>
      <div class="divider" id="divider"></div>
      <span class="tag l">Без визуалов</span><span class="tag r">С визуалами</span>
    </div>
    <div class="ctl"><input type="range" id="cmp" min="0" max="100" value="50" aria-label="Сравнение: без визуалов и с визуалами"></div>
    <p class="hint">Двигай ползунок или перетаскивай линию на сцене. Клик справа от линии показывает эффект удара.</p>
  </div>
</div>

<section id="features">
  <div class="wrap">
    <h2>Что меняется в игре</h2>
    <div class="grid">
      <div class="rule"><h3>Эффекты ударов</h3><p>Частицы, цветная вспышка и анимация при каждом попадании и убийстве.</p></div>
      <div class="rule"><h3>Свой интерфейс</h3><p>Список модулей, координаты, FPS, броня и эффекты в аккуратном виде.</p></div>
      <div class="rule"><h3>Анимации</h3><p>Новые анимации удара, меча и тотема. Любую можно отключить.</p></div>
      <div class="rule"><h3>Небо и атмосфера</h3><p>Своё время суток, туман и цвет неба независимо от сервера.</p></div>
      <div class="rule"><h3>Трейлы</h3><p>Следы за игроком, стрелами и жемчугом Предела.</p></div>
      <div class="rule"><h3>Лёгкий клиент</h3><p>Работает на слабых ПК, влияние на FPS минимальное.</p></div>
    </div>
  </div>
</section>

<section id="hudshot">
  <div class="wrap">
    <h2>Интерфейс AMSELIAN</h2>
    <div class="hws" id="hws" aria-label="Макет интерфейса AMSELIAN VISUALS"></div>
    <p class="note">Макет интерфейса: часть панелей уже есть в моде (вотермарк, координаты, эффекты, цель, броня), остальные добавим позже.</p>
  </div>
</section>

<section id="guishot">
  <div class="wrap">
    <h2>Меню AMSELIAN VISUALS</h2>
    <div class="ag" aria-label="Макет меню AMSELIAN VISUALS">
      <aside class="ag-side">
        <div class="ag-brand"><span class="ag-logo">A</span><span>AMSELIAN<br>VISUALS</span></div>
        <nav class="ag-nav" id="ag-nav"></nav>
        <div class="ag-user"><span class="ag-logo sm">A</span><div><b>Player</b><small>User</small></div></div>
      </aside>
      <div class="ag-main">
        <div class="ag-head"><b id="ag-title">HUD</b><input class="ag-q" id="ag-q" type="search" placeholder="Поиск" aria-label="Поиск по модулям"></div>
        <div class="ag-list" id="ag-list"></div>
      </div>
    </div>
    <p class="note">Меню открывается клавишей Right Shift. Здесь макет: вкладки, поиск и переключатели работают.</p>
  </div>
</section>

<section id="download">
  <div class="wrap">
    <div class="dl">
      <div>
        <h2>Скачать AMSELIAN VISUALS</h2>
        <p>Версия Minecraft и загрузчик: укажи свои в описании релиза.</p>
      </div>
      <a class="btn" href="#download" id="dlbtn">Скачать</a>
    </div>
  </div>
</section>

<section id="faq">
  <div class="wrap">
    <h2>Вопросы</h2>
    <details><summary>Это чит?</summary><p>Нет. Визуалы меняют только картинку и интерфейс и не дают преимущества в бою.</p></details>
    <details><summary>Можно ли получить бан?</summary><p>Правила у серверов разные. Некоторые запрещают даже косметические моды, поэтому проверь правила своего сервера.</p></details>
    <details><summary>Что-то не работает. Куда писать?</summary><p>Напиши в Discord проекта: ссылка появится здесь после релиза.</p></details>
  </div>
</section>

<div class="wrap">
  <section class="view" id="v-login">
    <h1>Вход</h1>
    <div class="card">
      <form id="f-login" novalidate>
        <label class="f" for="l-email">Почта</label><input class="t" id="l-email" type="email" autocomplete="email">
        <label class="f" for="l-pass">Пароль</label><input class="t" id="l-pass" type="password" autocomplete="current-password">
        <p class="msg" id="l-msg" role="alert"></p>
        <button class="btn" type="submit">Войти</button>
      </form>
      <p class="swap">Нет аккаунта? <a href="#register">Зарегистрироваться</a></p>
    </div>
  </section>

  <section class="view" id="v-register">
    <h1>Регистрация</h1>
    <div class="card">
      <form id="f-reg" novalidate>
        <label class="f" for="r-name">Ник</label><input class="t" id="r-name" autocomplete="username" maxlength="20">
        <label class="f" for="r-email">Почта</label><input class="t" id="r-email" type="email" autocomplete="email">
        <label class="f" for="r-pass">Пароль (от 8 символов)</label><input class="t" id="r-pass" type="password" autocomplete="new-password">
        <label class="f" for="r-pass2">Повтори пароль</label><input class="t" id="r-pass2" type="password" autocomplete="new-password">
        <p class="msg" id="r-msg" role="alert"></p>
        <button class="btn" type="submit">Создать аккаунт</button>
      </form>
      <p class="swap">Уже есть аккаунт? <a href="#login">Войти</a></p>
    </div>
  </section>

  <section class="view" id="v-cabinet">
    <h1>Личный кабинет</h1>
    <div class="card wide">
      <dl class="kv">
        <dt>Ник</dt><dd id="c-name"></dd>
        <dt>Почта</dt><dd id="c-email"></dd>
        <dt>Регистрация</dt><dd id="c-date"></dd>
        <dt>Ключ лицензии</dt><dd class="lic" id="c-lic"></dd>
      </dl>
      <div class="row">
        <button class="btn" type="button" id="c-dl">Скачать клиент</button>
        <a class="btn ghost" href="#support" style="margin-left:0">Написать в поддержку</a>
      </div>
      <h3 style="margin-top:28px;font-size:17px">Мои обращения</h3>
      <ul class="tix" id="c-tix"></ul>
      <div class="row" style="margin-top:20px">
        <button class="btn ghost" type="button" id="c-out" style="margin-left:0">Выйти</button>
        <button class="btn danger" type="button" id="c-del">Удалить аккаунт</button>
      </div>
    </div>
  </section>

  <section class="view" id="v-support">
    <h1>Поддержка</h1>
    <div class="card wide">
      <p style="margin:0;color:var(--muted)">Опиши проблему: версию Minecraft, загрузчик и что именно не работает. Быстрые ответы есть в разделе <a href="#faq">«Вопросы»</a>.</p>
      <form id="f-sup" novalidate>
        <label class="f" for="s-email">Почта для ответа</label><input class="t" id="s-email" type="email" autocomplete="email">
        <label class="f" for="s-topic">Тема</label>
        <select class="t" id="s-topic"><option>Не запускается клиент</option><option>Проблема с аккаунтом</option><option>Ошибка или вылет</option><option>Предложение</option><option>Другое</option></select>
        <label class="f" for="s-text">Сообщение</label><textarea class="t" id="s-text" maxlength="2000"></textarea>
        <p class="msg" id="s-msg" role="alert"></p>
        <button class="btn" type="submit">Отправить</button>
      </form>
    </div>
  </section>
</div>

<footer>
  <div class="wrap"><div class="flinks"><a href="#support">Поддержка</a><a href="#login">Вход</a><a href="#register">Регистрация</a></div><p style="margin:14px 0 0">© 2026 AMSELIAN VISUALS. Проект не связан с Mojang и Microsoft. Minecraft — торговая марка Mojang Synergies AB.</p></div>
</footer>

<script>
const $=id=>document.getElementById(id);
const scene=$('scene'),cmp=$('cmp'),cvB=$('cv-b'),dv=$('divider');
function rng(a){return()=>{a|=0;a=a+0x6D2B79F5|0;let t=Math.imul(a^a>>>15,1|a);t=t+Math.imul(t^t>>>7,61|t)^t;return((t^t>>>14)>>>0)/4294967296}}
function draw(cv,vis,hud){
  const W=320,H=180,c=cv.getContext('2d'),R=rng(7);
  const px=(x,y,w,h,col)=>{c.fillStyle=col;c.fillRect(x,y,w,h)};
  const fr=(x,y,w,h,col)=>{px(x,y,w,2,col);px(x,y+h-2,w,2,col);px(x,y,2,h,col);px(x+w-2,y,2,h,col)};
  const noise=(x,y,w,h,cols,s)=>{for(let j=0;j<h;j+=s)for(let i=0;i<w;i+=s)px(x+i,y+j,s,s,cols[(R()*cols.length)|0])};
  // небо
  if(vis)['#b9a4ff','#c3b0ff','#cdbcff','#d7c9ff','#e1d6ff','#ebe2ff'].forEach((col,i)=>px(0,i*20,W,20,col));
  else px(0,0,W,H,'#78a7ff');
  if(vis)px(246,10,32,32,'rgba(255,217,245,.35)');
  px(250,14,24,24,vis?'#ffd9f5':'#fff6a8');
  [[30,22,48,10],[40,16,24,6],[170,34,56,10],[180,28,28,6]].forEach(a=>px(a[0],a[1],a[2],a[3],vis?'#f8f1ff':'#ffffff'));
  // земля
  noise(0,112,W,16,vis?['#8f6bd6','#9a78e0','#855fcb']:['#5d9b3a','#6aab44','#52902f'],4);
  noise(0,128,W,32,['#866043','#79553a','#8f6a4c','#6d4c33'],4);
  noise(0,160,W,20,['#7d7d7d','#8a8a8a','#6f6f6f'],4);
  [[60,164],[64,168],[240,170]].forEach(a=>px(a[0],a[1],4,4,'#4fe3e3'));
  c.fillStyle='rgba(0,0,0,.14)';
  for(let x=0;x<W;x+=16)c.fillRect(x,112,1,68);
  for(let y=128;y<H;y+=16)c.fillRect(0,y,W,1);
  // деревья
  const leaf=vis?['#d49bf0','#e1b0f7','#c685e6']:['#3f7a2a','#4a8a33','#356b23'];
  noise(48,80,16,32,['#6b4f2a','#5a4122','#7a5b33'],4);noise(24,48,64,32,leaf,4);noise(40,32,32,16,leaf,4);
  noise(272,88,16,24,['#6b4f2a','#5a4122','#7a5b33'],4);noise(248,56,64,32,leaf,4);noise(264,40,32,16,leaf,4);
  // трейл
  if(vis)[[100,106,6],[92,100,5],[84,106,4],[78,98,3],[72,104,3]].forEach(a=>px(a[0],a[1],a[2],a[2],'rgba(182,156,255,.85)'));
  // зомби
  px(200,88,8,24,'#3b3fa0');px(208,88,8,24,'#2e3380');px(200,64,16,24,'#1f9aa0');
  px(184,64,16,6,'#4f8f3f');px(184,72,16,6,'#3f7a31');
  noise(200,48,16,16,['#4f8f3f','#478536','#58993f'],4);px(202,56,3,3,'#111');px(208,56,3,3,'#111');px(203,61,8,2,'#2e5a24');
  px(200,48,16,64,vis?'rgba(255,140,230,.35)':'rgba(255,0,0,.35)');
  // игрок
  px(112,88,8,24,'#3c44aa');px(120,88,8,24,'#2f3690');px(112,64,16,24,'#00a6a6');
  px(104,64,8,12,'#00a6a6');px(104,76,8,12,'#c68e6a');px(128,64,8,12,'#00a6a6');px(128,76,8,8,'#c68e6a');
  px(112,48,16,16,'#c68e6a');px(112,48,16,6,'#4a2f1a');px(112,54,2,4,'#4a2f1a');px(126,54,2,4,'#4a2f1a');
  px(120,58,3,2,'#fff');px(123,58,2,2,'#3a2f8a');px(120,62,4,1,'#8a5a40');
  if(vis)px(134,52,12,36,'rgba(182,156,255,.4)');
  px(138,56,4,28,vis?'#e6dcff':'#d0d0d0');px(140,56,2,28,vis?'#b69cff':'#9a9a9a');
  px(134,80,12,3,'#6b4f2a');px(138,83,4,6,'#6b4f2a');
  // эффекты удара
  if(vis){
    [[190,40,4],[222,38,3],[196,30,3],[216,26,4],[206,20,3],[226,48,3],[188,52,3]].forEach((a,i)=>px(a[0],a[1],a[2],a[2],['#b69cff','#e4d9ff','#ffffff','#f0c6ff'][i%4]));
    px(196,40,24,3,'#2b1f5a');px(196,40,14,3,'#b69cff');
    c.font='bold 10px monospace';c.fillStyle='#fff';c.shadowColor='#5b3fd0';c.shadowBlur=3;c.fillText('-7',224,34);c.shadowBlur=0;
  }
  if(hud===false)return;
  // прицел
  if(vis){const k='#b69cff';px(160,82,2,4,k);px(160,94,2,4,k);px(152,89,4,2,k);px(166,89,4,2,k);px(160,89,2,2,'#fff')}
  else{px(160,86,2,8,'#fff');px(156,89,10,2,'#fff')}
  // панель
  if(vis)px(66,154,188,28,'rgba(36,24,84,.55)');
  for(let i=0;i<9;i++){const x=70+i*20;
    if(vis){px(x+1,159,18,18,'rgba(70,48,150,.85)');fr(x+1,159,18,18,i?'#8d78e8':'#fff')}
    else{px(x,158,20,20,'#8b8b8b');fr(x,158,20,20,i?'#373737':'#fff')}
  }
  px(77,162,2,10,vis?'#e6dcff':'#d0d0d0');px(74,170,8,2,'#6b4f2a');px(77,172,2,3,'#6b4f2a');
  px(98,164,12,2,'#9a9a9a');px(103,164,2,12,'#6b4f2a');
  px(122,163,12,12,vis?'#9a78e0':'#5d9b3a');px(122,169,12,6,'#866043');
  const heart=(x,y,col)=>{px(x,y,3,2,col);px(x+4,y,3,2,col);px(x,y+2,7,3,col);px(x+1,y+5,5,1,col);px(x+2,y+6,3,1,col);px(x+1,y+1,1,1,'rgba(255,255,255,.6)')};
  for(let i=0;i<10;i++){heart(70+i*9,144,vis?'#c76ee8':'#d62323');const x=250-(i+1)*9+2;px(x+1,145,5,4,vis?'#b69cff':'#b8672a');px(x+4,148,3,3,'#e8d7b0')}
  if(vis){
    c.font='bold 8px monospace';c.textBaseline='alphabetic';
    c.fillStyle='#fff';c.fillText('AMSELIAN VISUALS',6,12);
    c.fillStyle='#e4d9ff';c.fillText('FPS 240 | 128 64 -302',6,22);
    c.textAlign='right';
    c.fillStyle='#e4d9ff';c.fillText('HitEffects',314,12);
    c.fillStyle='#c9b8ff';c.fillText('Trails',314,22);
    c.fillStyle='#f0c6ff';c.fillText('Animations',314,32);
  }
}
draw($('cv-a'),false);draw(cvB,true);
function setCmp(v){cmp.value=v;cvB.style.clipPath='inset(0 0 0 '+v+'%)';dv.style.left=v+'%'}
cmp.addEventListener('input',()=>setCmp(+cmp.value));
let drag=false;
const fromX=x=>{const r=scene.getBoundingClientRect();setCmp(Math.max(0,Math.min(100,(x-r.left)/r.width*100)))};
dv.addEventListener('pointerdown',e=>{drag=true;dv.setPointerCapture(e.pointerId);e.preventDefault()});
dv.addEventListener('pointermove',e=>{if(drag)fromX(e.clientX)});
dv.addEventListener('pointerup',()=>{drag=false});
dv.addEventListener('pointercancel',()=>{drag=false});
scene.addEventListener('click',e=>{
  if(e.target===dv)return;
  const r=scene.getBoundingClientRect(),x=e.clientX-r.left,y=e.clientY-r.top;
  if(x/r.width*100<=+cmp.value)return;
  const cols=['#b69cff','#e4d9ff','#8d80ff','#ffffff'];
  for(let i=0;i<16;i++){
    const q=document.createElement('div');q.className='p';
    q.style.left=x+'px';q.style.top=y+'px';q.style.background=cols[i%cols.length];
    q.style.setProperty('--dx',(Math.random()*160-80)+'px');
    q.style.setProperty('--dy',(Math.random()*-120-10)+'px');
    scene.appendChild(q);setTimeout(()=>q.remove(),750);
  }
});
$('dlbtn').addEventListener('click',e=>{e.preventDefault();alert('Ссылка на загрузку появится после релиза.');});
(()=>{
  const svg=p=>'<svg viewBox="0 0 24 24" width="18" height="18" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">'+p+'</svg>';
  const IC={
    Visuals:svg('<path d="M2 12s4-7 10-7 10 7 10 7-4 7-10 7S2 12 2 12z"/><circle cx="12" cy="12" r="3"/>'),
    HUD:svg('<rect x="3" y="4" width="18" height="12" rx="2"/><path d="M8 20h8M12 16v4"/>'),
    Utilities:svg('<path d="M12 3l2 5 5 2-5 2-2 5-2-5-5-2 5-2z"/>'),
    Markers:svg('<path d="M5 21V4h12l-2 4 2 4H5"/>'),
    Configs:svg('<path d="M7 18a4 4 0 010-8 5 5 0 019.6-1A4.5 4.5 0 0117 18z"/>')
  };
  const D={
    Visuals:[['Hit Effects','Частицы при попадании по цели',1],['Trails','След за игроком при движении',1],['Crosshair','Свой прицел с подсветкой цели',1],['Custom Sky','Лавандовый оттенок неба',1],['Fog','Мягкий туман в цвет интерфейса',0],['Animations','Новые анимации удара и предметов',1],['Prediction','Траектория стрел, снежков и других снарядов',1]],
    HUD:[['Armor HUD','Отображение прочности брони',1],['Target HUD','Отображение информации о цели',0],['Cooldowns HUD','Отображение кулдауна предметов',1],['Hotkeys','Отображение активных биндов',1],['Potions','Отображение активных эффектов',1],['Coordinates','Отображение координат и направления',1],['Watermark','Название, FPS и пинг',1],['Module List','Список включённых модулей',1]],
    Utilities:[['Optimization','Меньше частиц и лёгкая графика для высокого FPS',0],['Player Hitbox','Хитбокс игроков',0],['Mob Hitbox','Хитбокс мобов и животных',0],['Item Hitbox','Хитбокс лежащих предметов',0],['Fullbright','Освещает всё в темноте',0],['Target ESP','Вращающийся маркер на цели под прицелом',1],['Freelook','Свободная камера в F5 по клавише',1],['China Hat','Цветная или радужная шляпа над головой',1],['Screenshot Mode','Скрывает интерфейс для скриншота',0],['Accent Color','Выбор цвета акцента меню',1]],
    Markers:[['Waypoints','Свои метки в мире',1],['Death Marker','Место последней смерти',1]],
    Configs:[['Default','Готовый набор настроек по умолчанию',1],['Minimal','Только самое нужное',0],['Full','Все визуальные модули включены',0]]
  };
  let tab='HUD';
  const nav=$('ag-nav'),list=$('ag-list'),q=$('ag-q'),title=$('ag-title');
  Object.keys(D).forEach(t=>{
    const b=document.createElement('button');b.type='button';b.dataset.t=t;
    b.innerHTML=IC[t];const sp=document.createElement('span');sp.textContent=t;b.appendChild(sp);
    b.onclick=()=>{tab=t;q.value='';render()};nav.appendChild(b);
  });
  function render(){
    const s=q.value.trim().toLowerCase();
    title.textContent=s?'Поиск':tab;
    [...nav.children].forEach(b=>b.classList.toggle('on',!s&&b.dataset.t===tab));
    list.textContent='';
    const items=s?Object.values(D).flat().filter(m=>(m[0]+' '+m[1]).toLowerCase().includes(s)):D[tab];
    if(!items.length){const e=document.createElement('p');e.textContent='Ничего не найдено';e.style.color='#8a82a3';list.appendChild(e);return}
    items.forEach(m=>{
      const r=document.createElement('div');r.className='ag-row';
      const l=document.createElement('div');
      const n=document.createElement('b');n.textContent=m[0];
      const d=document.createElement('small');d.textContent=m[1];
      l.appendChild(n);l.appendChild(d);
      const c=document.createElement('div');c.className='ag-ctl';
      const bind=document.createElement('span');bind.className='ag-bind';bind.textContent='None';
      const sw=document.createElement('input');sw.type='checkbox';sw.className='ag-sw';sw.checked=!!m[2];
      sw.setAttribute('aria-label',m[0]);sw.onchange=()=>{m[2]=sw.checked?1:0};
      c.appendChild(bind);c.appendChild(sw);r.appendChild(l);r.appendChild(c);list.appendChild(r);
    });
  }
  q.addEventListener('input',render);
  render();
})();
(()=>{
  const root=document.documentElement,btn=$('theme');
  const ic=p=>'<svg viewBox="0 0 24 24" width="18" height="18" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">'+p+'</svg>';
  const sun=ic('<circle cx="12" cy="12" r="4"/><path d="M12 2v2M12 20v2M4.9 4.9l1.4 1.4M17.7 17.7l1.4 1.4M2 12h2M20 12h2M4.9 19.1l1.4-1.4M17.7 6.3l1.4-1.4"/>');
  const moon=ic('<path d="M21 12.8A9 9 0 1111.2 3a7 7 0 009.8 9.8z"/>');
  let saved=null;try{saved=localStorage.getItem('av_theme')}catch(e){}
  let cur=saved==='light'||saved==='dark'?saved:(matchMedia('(prefers-color-scheme: dark)').matches?'dark':'light');
  function apply(){
    root.setAttribute('data-theme',cur);
    btn.innerHTML=cur==='dark'?sun:moon;
    btn.title=cur==='dark'?'Светлая тема':'Тёмная тема';
  }
  btn.addEventListener('click',()=>{
    cur=cur==='dark'?'light':'dark';
    try{localStorage.setItem('av_theme',cur)}catch(e){}
    apply();
  });
  apply();
})();
(()=>{
  const root=$('hws');
  const ic=p=>'<svg class="hi" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">'+p+'</svg>';
  const I={
    mon:'<rect x="3" y="4" width="18" height="12" rx="2"/><path d="M8 20h8M12 16v4"/>',
    arr:'<path d="M5 8h14l-3-3M19 16H5l3 3"/>',
    bars:'<path d="M5 20V12M10 20V6M15 20V10M20 20V4"/>',
    globe:'<circle cx="12" cy="12" r="9"/><path d="M3 12h18M12 3c3 3 3 15 0 18M12 3c-3 3-3 15 0 18"/>',
    list:'<path d="M4 6h16M4 12h16M4 18h10"/>',
    box:'<rect x="4" y="7" width="16" height="12" rx="2"/><path d="M4 11h16"/>',
    tgt:'<circle cx="12" cy="12" r="8"/><circle cx="12" cy="12" r="2"/>',
    clock:'<circle cx="12" cy="12" r="8"/><path d="M12 7v5l3 2"/>',
    team:'<circle cx="9" cy="8" r="3"/><path d="M3 19c0-3 3-5 6-5s6 2 6 5"/><circle cx="17" cy="9" r="2"/>',
    inv:'<rect x="4" y="5" width="16" height="14" rx="2"/><path d="M4 12h16M12 5v14"/>',
    mus:'<path d="M9 18V6l10-2v12"/><circle cx="7" cy="18" r="2"/><circle cx="17" cy="16" r="2"/>'
  };
  const P=(t,i,b,nl)=>'<div class="hw'+(nl?' nl':'')+'">'+(t?'<div class="lbl">'+ic(I[i])+t+'</div>':'')+'<div class="hc">'+b+'</div></div>';
  const g=(a,b)=>'linear-gradient(135deg,'+a+','+b+')';
  const item=(c,n)=>'<div class="slot">'+(c?'<i class="it" style="background:'+g(c[0],c[1])+'"></i>':'')+(n?'<span class="cnt">'+n+'</span>':'')+'</div>';
  const fx=[['Огнестойкость','',222,['#ffb36b','#e0603c']],['Сила','4',101,['#c9b8ff','#7a5ce6']],['Скорость','3',42,['#ff9ad8','#c04fb0']]];
  const fx0=fx.map(e=>e[2]);
  const fmt=t=>Math.floor(t/60)+':'+String(t%60).padStart(2,'0');
  const effects=fx.map((e,i)=>'<div class="r"><i class="ic" style="background:'+g(e[3][0],e[3][1])+'"></i><span>'+e[0]+(e[1]?'<sup>'+e[1]+'</sup>':'')+'</span><span class="pill" data-fx="'+i+'">'+fmt(e[2])+'</span></div>').join('');
  const keys=[['Z',['#7fe0a0','#2e8a5a']],['X',['#b07a5a','#5a3a2a']],['C',['#ffffff','#a9c8e8']],['V',['#6a6a74','#2a2a32']]];
  const slots=keys.map(k=>'<div class="slot"><i class="it" style="background:'+g(k[1][0],k[1][1])+'"></i><span class="key">'+k[0]+'</span></div>').join('');
  const arm=['#9fe3e3','#b69cff','#8d80ff','#7a5ce6','#6a6a74'].map(c=>'<i style="background:'+c+'"></i>').join('');
  const inv=[['#ffd84a,#e0a020',24],0,['#c47a3a,#7a4a20',0],['#bfa57a,#7a6a4a',16],['#9a4a4a,#5a2a2a',3],0,['#ffd84a,#e8b020',58],0,0,
    ['#2fd5b0,#127a68',16],['#2fd5b0,#127a68',15],['#8a6a6a,#4a3a3a',0],0,0,['#7fd0ff,#3a7ab0',0],['#6a7cff,#2a3a9a',0],['#e4ecff,#9ab0d0',0],['#e4ecff,#9ab0d0',0],
    ['#2fd5b0,#127a68',16],['#e8c34a,#9a7a20',6],['#9a6a4a,#5a3a2a',64],['#ffffff,#c8d0e0',13],['#8a8a94,#4a4a54',20],['#7fd0ff,#3a7ab0',0],0,['#e4ecff,#9ab0d0',0],['#ff9ab0,#b04a6a',15]]
    .map(e=>e?item(e[0].split(','),e[1]||''):item(null,'')).join('');
  const team=[['piona',7,12],['aqich4',0,0]].map(m=>'<div class="r"><i class="dot"></i><span>'+m[0]+'</span>'+(m[1]?'<span class="seg">'+[0,1,2,3,4,5,6].map(i=>'<i'+(i>3?' class="w"':'')+'></i>').join('')+'</span><span class="muted">'+m[2]+'</span>':'<span class="pill muted" style="background:none">Мёртв</span>')+'</div>').join('');
  const sv=(d)=>'<svg viewBox="0 0 24 24"><path d="'+d+'"/></svg>';
  root.innerHTML=
   '<div class="hcol">'+
     P('','','<div class="brand"><span class="bl">A</span>AMSELIAN</div>','nl')+
     P('','','<div class="stats"><span><i class="dot"></i>AMSELIAN VISUALS</span><span>'+ic(I.mon)+'<b id="fps">215</b><small>fps</small></span><span>'+ic(I.arr)+'<b>20</b><small>tps</small></span><span>'+ic(I.bars)+'<b>15</b><small>ms</small></span></div>','nl')+
     P('','','<div class="stats"><span>'+ic(I.globe)+'<b>-200 74 50</b></span></div>','nl')+
     P('Список биндов','list','<div class="r"><span>Zoom</span><span class="pill">B</span></div><div class="r"><span>Скрыть интерфейс</span><span class="pill">V</span></div>')+
     P('Предметы','box','<div class="slots">'+slots+'</div>')+
     P('','','<div class="ring"><svg viewBox="0 0 80 80"><circle cx="40" cy="40" r="34" fill="none" stroke="#2a2534" stroke-width="6"/><circle id="rg" cx="40" cy="40" r="34" fill="none" stroke="#c9b8ff" stroke-width="6" stroke-linecap="round" stroke-dasharray="214" stroke-dashoffset="0"/></svg><span id="rgt">100%</span></div>','nl')+
   '</div>'+
   '<div class="hcol">'+
     P('Цель','tgt','<div class="tg"><div class="face"></div><div style="flex:1;min-width:0"><b>Zombie</b><div class="arm">'+arm+'<span>14.0</span></div><div class="bar"><i></i></div></div></div>')+
     P('Эффекты','clock',effects)+
     P('Команда','team',team)+
   '</div>'+
   '<div class="hcol">'+
     P('Инвентарь','inv','<div class="inv">'+inv+'</div>')+
     P('Музыка','mus','<div class="cover">A</div><div class="ctl2">'+sv('M6 6h2v12H6zM20 6v12L9.5 12z')+sv('M6 5h4v14H6zM14 5h4v14h-4z')+sv('M16 6h2v12h-2zM4 6v12l10.5-6z')+'</div><div class="prog"><i id="pg"></i></div>')+
   '</div>';
  if(matchMedia('(prefers-reduced-motion: reduce)').matches)return;
  setInterval(()=>{
    fx.forEach((e,i)=>{e[2]=e[2]>0?e[2]-1:fx0[i];const el=root.querySelector('[data-fx="'+i+'"]');if(el)el.textContent=fmt(e[2])});
    const f=$('fps');if(f)f.textContent=210+Math.floor(Math.random()*12);
  },1000);
  setInterval(()=>{
    const p=(Date.now()%4000)/4000,r=$('rg'),t=$('rgt'),pg=$('pg');
    if(r)r.setAttribute('stroke-dashoffset',String(214*(1-p)));
    if(t)t.textContent=Math.round(p*100)+'%';
    if(pg)pg.style.width=((Date.now()%30000)/300)+'%';
  },100);
})();
$('intro').addEventListener('click',e=>e.currentTarget.remove());
setTimeout(()=>{const i=$('intro');if(i)i.remove()},3500);
/* ---- аккаунты и поддержка (демо: данные только в этом браузере) ---- */
const S={get(k,d){try{const v=localStorage.getItem(k);return v?JSON.parse(v):d}catch(e){return d}},set(k,v){try{localStorage.setItem(k,JSON.stringify(v));return true}catch(e){return false}}};
const hex=b=>[...new Uint8Array(b)].map(x=>x.toString(16).padStart(2,'0')).join('');
const rnd=n=>hex(crypto.getRandomValues(new Uint8Array(n)));
const hash=async(pw,salt)=>hex(await crypto.subtle.digest('SHA-256',new TextEncoder().encode(salt+pw)));
const users=()=>S.get('av_users',{});
const me=()=>{const e=S.get('av_session',null),u=e&&users()[e];return u?Object.assign({email:e},u):null};
const fmt=ts=>new Date(ts).toLocaleDateString('ru-RU');
const EMAIL=/^[^\s@]+@[^\s@]+\.[^\s@]+$/;
const VIEWS=['login','register','cabinet','support'];
const HOME=['top','demo','features','hudshot','guishot','download','faq'];
function say(id,text,ok){const m=$(id);m.textContent=text;m.className='msg'+(ok?' ok':'')}
function renderNav(){const u=me(),a=$('nav-acct');a.textContent=u?'Кабинет':'Войти';a.href=u?'#cabinet':'#login'}
function renderCabinet(){
  const u=me();if(!u)return;
  $('c-name').textContent=u.name;$('c-email').textContent=u.email;$('c-date').textContent=fmt(u.created);$('c-lic').textContent=u.license;
  const ul=$('c-tix');ul.textContent='';
  const list=S.get('av_tickets',[]).filter(t=>t.email===u.email).reverse();
  if(!list.length){const li=document.createElement('li');li.textContent='Обращений пока нет.';ul.appendChild(li);return}
  list.forEach(t=>{const li=document.createElement('li');li.textContent=t.id+' · '+t.topic;const s=document.createElement('small');s.textContent=fmt(t.date)+' · '+t.text.slice(0,80);li.appendChild(s);ul.appendChild(li)});
}
function route(){
  let h=location.hash.slice(1);
  const u=me();
  if(h==='cabinet'&&!u){location.hash='login';return}
  if((h==='login'||h==='register')&&u){location.hash='cabinet';return}
  const isView=VIEWS.includes(h);
  VIEWS.forEach(v=>$('v-'+v).classList.toggle('on',v===h));
  HOME.forEach(i=>$(i).style.display=isView?'none':'');
  if(h==='cabinet')renderCabinet();
  if(h==='support'&&u&&!$('s-email').value)$('s-email').value=u.email;
  renderNav();
  if(isView)window.scrollTo(0,0);
  else if(h&&$(h))$(h).scrollIntoView();
}
addEventListener('hashchange',route);
$('f-reg').addEventListener('submit',async e=>{
  e.preventDefault();
  const name=$('r-name').value.trim(),email=$('r-email').value.trim().toLowerCase(),p=$('r-pass').value;
  if(name.length<3)return say('r-msg','Ник: минимум 3 символа.');
  if(!EMAIL.test(email))return say('r-msg','Введи корректную почту.');
  if(p.length<8)return say('r-msg','Пароль: минимум 8 символов.');
  if(p!==$('r-pass2').value)return say('r-msg','Пароли не совпадают.');
  const all=users();
  if(all[email])return say('r-msg','Эта почта уже зарегистрирована. Войди в аккаунт.');
  const salt=rnd(8),up=rnd(2).toUpperCase(),lo=rnd(2).toUpperCase();
  all[email]={name,salt,hash:await hash(p,salt),created:Date.now(),license:'AV-'+up+'-'+lo+'-'+rnd(2).toUpperCase()};
  if(!S.set('av_users',all)||!S.set('av_session',email))return say('r-msg','Не удалось сохранить данные: браузер блокирует хранилище.');
  e.target.reset();say('r-msg','');location.hash='cabinet';
});
$('f-login').addEventListener('submit',async e=>{
  e.preventDefault();
  const email=$('l-email').value.trim().toLowerCase(),u=users()[email];
  if(!u||u.hash!==await hash($('l-pass').value,u.salt))return say('l-msg','Неверная почта или пароль.');
  S.set('av_session',email);e.target.reset();say('l-msg','');location.hash='cabinet';
});
$('c-out').onclick=()=>{S.set('av_session',null);renderNav();location.hash='login'};
$('c-del').onclick=()=>{
  if(!confirm('Удалить аккаунт? Это действие нельзя отменить.'))return;
  const u=me(),all=users();delete all[u.email];S.set('av_users',all);S.set('av_session',null);renderNav();location.hash='register';
};
$('c-dl').onclick=()=>alert('Ссылка на загрузку появится после релиза.');
$('f-sup').addEventListener('submit',e=>{
  e.preventDefault();
  const email=$('s-email').value.trim().toLowerCase(),text=$('s-text').value.trim();
  if(!EMAIL.test(email))return say('s-msg','Введи корректную почту.');
  if(text.length<10)return say('s-msg','Опиши проблему подробнее: минимум 10 символов.');
  const t=S.get('av_tickets',[]),id='T-'+Date.now().toString(36).toUpperCase();
  t.push({id,email,topic:$('s-topic').value,text,date:Date.now()});
  if(!S.set('av_tickets',t))return say('s-msg','Не удалось сохранить обращение: браузер блокирует хранилище.');
  $('s-text').value='';say('s-msg','Обращение '+id+' сохранено.',true);
});
route();
</script>
</body>
</html>
