<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Sopaan · Algebraic Expressions and Identities</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,500;9..144,700&family=Source+Sans+3:wght@400;600;700&family=IBM+Plex+Mono:wght@500;600&display=swap">
<style>
  html,body{margin:0;} img{max-width:100%;} [hidden]{display:none !important;}
  :root{
    --navy:#16264A; --navy-2:#1F3B6B; --gold:#C79A3E; --gold-soft:#F3E7C9;
    --paper:#FBF9F4; --paper-2:#F1EAD8; --card:#FFFFFF;
    --ink:#211E1A; --ink-soft:#655D4C; --rule:#E4DCC8;
    --success:#2E8B57; --success-soft:#E1F2E7;
    --danger:#BF4B45; --danger-soft:#FAE3E1;
    --locked:#C7BEA9;
    --focus:#1F3B6B;
    --accent-text:#1F3B6B; --retry-text:#8A661F;
    color-scheme:light;
  }
  @media (prefers-color-scheme: dark){
    :root:not([data-theme="light"]){
      --navy:#0E1830; --navy-2:#16264A; --gold:#E0B75B; --gold-soft:#3A2F16;
      --paper:#141210; --paper-2:#1C1914; --card:#1C1914;
      --ink:#EDE7DA; --ink-soft:#B2A996; --rule:#3A342A;
      --success:#7BC79A; --success-soft:#1B2E22;
      --danger:#E38884; --danger-soft:#331D1B;
      --locked:#4A4436;
      --focus:#E0B75B;
      --accent-text:#E0B75B; --retry-text:#E0B75B;
      color-scheme:dark;
    }
  }
  :root[data-theme="dark"]{
    --navy:#0E1830; --navy-2:#16264A; --gold:#E0B75B; --gold-soft:#3A2F16;
    --paper:#141210; --paper-2:#1C1914; --card:#1C1914;
    --ink:#EDE7DA; --ink-soft:#B2A996; --rule:#3A342A;
    --success:#7BC79A; --success-soft:#1B2E22;
    --danger:#E38884; --danger-soft:#331D1B;
    --locked:#4A4436;
    --focus:#E0B75B;
    --accent-text:#E0B75B; --retry-text:#E0B75B;
    color-scheme:dark;
  }

  *{box-sizing:border-box;}
  body{background:var(--paper); color:var(--ink); font-family:'Source Sans 3',-apple-system,'Segoe UI',sans-serif; padding-inline:0; padding-block:0;}
  h1,h2,h3{font-family:'Fraunces',Georgia,serif; text-wrap:balance; margin:0;}
  .num{font-family:'IBM Plex Mono',ui-monospace,monospace; font-variant-numeric:tabular-nums;}

  header.brand{
    background:linear-gradient(155deg,var(--navy) 0%, var(--navy-2) 100%);
    color:#F4EFDF; padding-block:calc(20px + env(safe-area-inset-top,0px)) 18px; padding-inline:20px;
  }
  .brand-row{display:flex; align-items:center; gap:12px; max-width:900px; margin:0 auto;}
  .crest{
    width:42px; height:42px; border-radius:10px; background:var(--gold); color:var(--navy);
    display:flex; align-items:center; justify-content:center; font-family:'Fraunces',serif; font-weight:700; font-size:18px; flex-shrink:0;
  }
  .brand-name{font-size:12px; letter-spacing:.08em; text-transform:uppercase; color:var(--gold); font-weight:700;}
  .series-name{font-size:19px; font-weight:700; font-family:'Fraunces',serif;}
  .chapter-eyebrow{max-width:900px; margin:14px auto 0; font-size:12px; letter-spacing:.06em; text-transform:uppercase; color:#AEB9D6;}
  .chapter-title{font-size:28px; max-width:900px; margin:2px auto 0;}
  .chapter-sub{font-size:14.5px; color:var(--gold); font-weight:700; max-width:900px; margin:3px auto 0;}

  .chapter-progress{max-width:900px; margin:14px auto 0; display:flex; align-items:center; gap:10px;}
  .cp-track{flex:1; height:6px; border-radius:99px; background:rgba(255,255,255,.18); overflow:hidden;}
  .cp-fill{height:100%; background:var(--gold); border-radius:99px; transition:width .3s ease;}
  .cp-label{font-size:11.5px; color:#CFD7EA; white-space:nowrap;}

  .tabbar{position:sticky; top:env(safe-area-inset-top,0px); z-index:15; background:var(--paper); border-bottom:1px solid var(--rule); overflow-x:auto; white-space:nowrap;}
  .tabbar-inner{max-width:900px; margin:0 auto; display:flex; padding-inline:16px;}
  .tab-btn{font-family:inherit; font-size:14px; font-weight:600; color:var(--ink-soft); background:none; border:none; padding:13px 16px; cursor:pointer; position:relative; flex-shrink:0;}
  .tab-btn.active{color:var(--accent-text);}
  .tab-btn.active::after{content:''; position:absolute; left:12px; right:12px; bottom:0; height:3px; background:var(--gold); border-radius:3px 3px 0 0;}
  .tab-count{font-size:11px; color:var(--ink-soft); margin-left:5px;}

  .slide-progress{max-width:900px; margin:0 auto; padding:10px 16px 0; display:flex; align-items:center; gap:10px;}
  .sp-track{flex:1; height:5px; border-radius:99px; background:var(--rule); overflow:hidden;}
  .sp-fill{height:100%; background:var(--accent-text); border-radius:99px; transition:width .3s ease;}
  .sp-label{font-size:12px; color:var(--ink-soft); white-space:nowrap; font-weight:600;}

  .wrap{max-width:900px; margin:0 auto; padding:16px 16px calc(110px + env(safe-area-inset-bottom,0px));}

  .qcard{background:var(--card); border:1px solid var(--rule); border-radius:14px; padding:18px;}
  .qhead{display:flex; align-items:flex-start; gap:10px; margin-bottom:10px;}
  .qnum{width:32px; height:32px; border-radius:8px; background:var(--gold-soft); color:var(--accent-text); display:flex; align-items:center; justify-content:center; font-weight:700; font-family:'Fraunces',serif; flex-shrink:0; font-size:14px;}
  .qtext{font-size:16px; line-height:1.55; flex:1;}
  .qtag{font-size:10.5px; color:var(--gold); background:var(--gold-soft); padding:2px 7px; border-radius:99px; font-weight:700; margin-left:6px; white-space:nowrap;}
  .marks-pill{font-size:11px; font-weight:700; color:var(--ink-soft); border:1px solid var(--rule); padding:3px 9px; border-radius:99px; margin-left:auto; flex-shrink:0; white-space:nowrap;}
  .step-badge{font-size:11px; font-weight:700; color:var(--accent-text); background:var(--paper-2); border:1px solid var(--rule); padding:3px 9px; border-radius:99px; display:inline-block; margin-bottom:12px;}

  .options{display:flex; flex-direction:column; gap:8px; margin-top:10px;}
  .opt{display:flex; align-items:center; gap:10px; padding:11px 12px; border:1.5px solid var(--rule); border-radius:10px; cursor:pointer; font-size:15px; background:var(--paper);}
  .opt input{accent-color:var(--navy-2);}
  .opt.is-correct{border-color:var(--success); background:var(--success-soft);}
  .opt.is-wrong{border-color:var(--danger); background:var(--danger-soft);}
  .opt.locked{cursor:not-allowed;}

  .subpart-label{font-weight:700; font-size:12.5px; color:var(--accent-text); text-transform:uppercase; letter-spacing:.03em; margin:14px 0 6px;}
  .or-divider{text-align:center; font-size:11px; font-weight:700; letter-spacing:.08em; color:var(--ink-soft); margin:8px 0;}

  .steps{display:flex; flex-direction:column; gap:10px;}
  .step-line{font-size:14.5px; line-height:1.9; background:var(--paper); border:1px dashed var(--rule); border-radius:10px; padding:9px 12px;}
  .step-line.resolved{opacity:.9;}
  .blank-input{font-family:'IBM Plex Mono',monospace; font-size:14px; border:1.5px solid var(--rule); border-radius:6px; padding:3px 8px; width:120px; background:var(--card); color:var(--ink); margin:0 2px;}
  .blank-input:focus{outline:none; border-color:var(--focus); box-shadow:0 0 0 3px var(--gold-soft);}
  .blank-input.is-correct{border-color:var(--success); background:var(--success-soft);}
  .blank-input.is-wrong{border-color:var(--danger); background:var(--danger-soft);}
  .blank-input[disabled]{opacity:.85;}
  .reveal-note{font-size:12px; color:var(--danger); padding-left:2px; margin-top:-2px;}

  .feedback{font-size:13.5px; padding:10px 12px; border-radius:9px; margin-top:14px; display:none;}
  .feedback.show{display:block;}
  .feedback.ok{background:var(--success-soft); color:var(--success);}
  .feedback.retry{background:var(--gold-soft); color:var(--retry-text);}
  .feedback.reveal{background:var(--danger-soft); color:var(--danger);}
  .feedback.err{background:var(--danger-soft); color:var(--danger);}
  .attempts-dots{display:inline-flex; gap:4px; margin-left:2px;}
  .attempts-dots span{width:6px; height:6px; border-radius:50%; background:var(--ink-soft); opacity:.3; display:inline-block;}
  .attempts-dots span.used{opacity:1; background:var(--danger);}

  .ar-box{background:var(--paper-2); border-radius:10px; padding:10px 12px; margin-bottom:12px; font-size:13px; color:var(--ink-soft);}

  .navbar{
    position:fixed; left:0; right:0; bottom:0; z-index:30; background:var(--paper);
    border-top:1px solid var(--rule); padding:10px 16px calc(10px + env(safe-area-inset-bottom,0px));
  }
  .navbar-inner{max-width:900px; margin:0 auto; display:flex; gap:8px; flex-wrap:wrap; align-items:center;}
  .btn{font-family:inherit; font-size:13.5px; font-weight:700; padding:10px 14px; border-radius:9px; border:1.5px solid var(--rule); background:var(--card); color:var(--ink); cursor:pointer;}
  .btn:hover{border-color:var(--navy-2);}
  .btn:disabled{opacity:.4; cursor:not-allowed;}
  .btn-primary{background:var(--navy-2); color:#fff; border-color:var(--navy-2);}
  .navbar .spacer{flex:1;}

  .fab{position:fixed; right:16px; bottom:calc(74px + env(safe-area-inset-bottom,0px)); background:var(--gold); color:var(--navy); border:none; border-radius:999px; padding:11px 16px; font-family:inherit; font-weight:700; font-size:13px; display:flex; align-items:center; gap:7px; cursor:pointer; box-shadow:0 6px 16px rgba(0,0,0,.18); z-index:35;}
  .fab-badge{background:rgba(255,255,255,.55); border-radius:99px; padding:1px 7px; font-size:11px;}

  .overlay{position:fixed; inset:0; background:rgba(20,18,14,.45); z-index:50; display:none; align-items:flex-end; justify-content:center;}
  .overlay.show{display:flex;}
  .palette{background:var(--card); width:min(480px,100%); max-height:78vh; overflow-y:auto; border-radius:18px 18px 0 0; padding:18px 18px calc(18px + env(safe-area-inset-bottom,0px)); border:1px solid var(--rule); border-bottom:none;}
  @media (min-width:640px){ .overlay{align-items:center;} .palette{border-radius:18px; border-bottom:1px solid var(--rule); max-height:74vh;} }
  .palette-head{display:flex; align-items:center; justify-content:space-between; margin-bottom:6px;}
  .palette-head h2{font-size:16px;}
  .palette-close{background:none; border:none; font-size:20px; color:var(--ink-soft); cursor:pointer; padding:4px;}
  .palette-legend{display:flex; gap:12px; flex-wrap:wrap; font-size:11px; color:var(--ink-soft); margin:10px 0 14px;}
  .palette-legend span{display:inline-flex; align-items:center; gap:5px;}
  .dot{width:9px; height:9px; border-radius:50%; display:inline-block;}
  .dot.correct{background:var(--success);} .dot.revealed{background:var(--danger);}
  .dot.skipped{background:var(--gold);} .dot.locked{background:var(--locked);}
  .dot.current{background:var(--navy-2);}
  .chip-grid{display:grid; grid-template-columns:repeat(auto-fill,minmax(48px,1fr)); gap:8px;}
  .chip{border:1.5px solid var(--rule); border-radius:9px; padding:8px 4px; text-align:center; font-family:'IBM Plex Mono',monospace; font-size:12.5px; font-weight:600; cursor:pointer; background:var(--paper); color:var(--ink);}
  .chip[data-status="correct"]{border-color:var(--success); background:var(--success-soft); color:var(--success);}
  .chip[data-status="revealed"]{border-color:var(--danger); background:var(--danger-soft); color:var(--danger);}
  .chip[data-status="skipped"]{border-color:var(--gold); background:var(--gold-soft); color:var(--retry-text);}
  .chip[data-status="locked"]{border-color:var(--rule); color:var(--locked); cursor:not-allowed; background:var(--paper-2);}
  .chip[data-status="current"]{outline:2px solid var(--navy-2); outline-offset:1px;}

  .toast{position:fixed; left:50%; bottom:calc(140px + env(safe-area-inset-bottom,0px)); transform:translateX(-50%); background:var(--ink); color:var(--paper); padding:9px 16px; border-radius:99px; font-size:13px; opacity:0; pointer-events:none; transition:opacity .25s ease; z-index:60;}
  .toast.show{opacity:1;}

  .done-card{text-align:center; padding:36px 20px;}
  .done-card .big{font-size:38px; margin-bottom:6px;}
  .score-pills{display:flex; gap:10px; justify-content:center; flex-wrap:wrap; margin:16px 0;}
  .score-pill{padding:8px 16px; border-radius:99px; font-size:13px; font-weight:700;}

  footer.brandfoot{max-width:900px; margin:14px auto 0; padding:0 16px calc(110px + env(safe-area-inset-bottom,0px)); text-align:center; font-size:12px; color:var(--ink-soft);}

  .mode-pill{font-family:inherit; font-size:12.5px; font-weight:700; color:var(--navy); background:var(--gold); border:none; border-radius:99px; padding:6px 14px; cursor:pointer; margin-top:12px; display:inline-flex; align-items:center; gap:6px;}
  .mode-pick{display:flex; flex-direction:column; gap:14px; padding:8px 0 24px;}
  .mode-card{background:var(--card); border:1.5px solid var(--rule); border-radius:16px; padding:22px; cursor:pointer; text-align:left;}
  .mode-card:hover{border-color:var(--navy-2);}
  .mode-card .mode-icon{font-size:26px; margin-bottom:8px;}
  .mode-card h3{font-size:18px; margin-bottom:6px;}
  .mode-card p{font-size:13.5px; color:var(--ink-soft); line-height:1.5; margin:0;}
  .quiz-hint{font-size:12.5px; color:var(--ink-soft); background:var(--paper-2); border-radius:9px; padding:8px 12px; margin-bottom:14px;}
  .review-row{border:1px solid var(--rule); border-radius:10px; padding:11px 13px; margin-bottom:10px;}
  .review-tag{font-size:11.5px; font-weight:700; margin-bottom:4px; display:block;}
  .review-tag.ok{color:var(--success);} .review-tag.bad{color:var(--danger);} .review-tag.na{color:var(--ink-soft);}
  .review-q{font-size:13.5px; margin-bottom:6px; color:var(--ink-soft);}
  .review-ans{font-size:13px; margin-bottom:2px;}

  .who-row{max-width:900px; margin:12px auto 0; display:flex; flex-wrap:wrap; gap:8px; align-items:center;}
  .who-row .mode-pill{margin-top:0;}
  .who{display:inline-flex; flex-wrap:wrap; align-items:center; gap:6px; font-size:12.5px; color:#CFD7EA;}
  .who b{color:#F4EFDF;}
  .who button{font-family:inherit; font-size:12px; font-weight:700; color:#F4EFDF; background:rgba(255,255,255,.12); border:1px solid rgba(255,255,255,.22); border-radius:99px; padding:5px 11px; cursor:pointer;}
  .who button:hover{background:rgba(255,255,255,.2);}
  .login-card{max-width:460px; margin:8px auto 0; background:var(--card); border:1px solid var(--rule); border-radius:16px; padding:22px;}
  .login-card h2{font-size:21px; margin-bottom:4px;}
  .login-card p.lead{font-size:13.5px; color:var(--ink-soft); margin:0 0 16px; line-height:1.5;}
  .fld{display:flex; flex-direction:column; gap:5px; margin-bottom:12px;}
  .fld label{font-size:12px; font-weight:700; letter-spacing:.04em; text-transform:uppercase; color:var(--ink-soft);}
  .fld input{font-family:inherit; font-size:15px; padding:10px 12px; border:1.5px solid var(--rule); border-radius:9px; background:var(--paper); color:var(--ink);}
  .fld input:focus{outline:none; border-color:var(--focus); box-shadow:0 0 0 3px var(--gold-soft);}
  .fld-row{display:grid; grid-template-columns:1fr 1fr; gap:10px;}
  .login-err{font-size:13px; color:var(--danger); background:var(--danger-soft); border-radius:8px; padding:8px 10px; margin-bottom:12px;}
  .login-note{font-size:12px; color:var(--ink-soft); margin-top:12px; line-height:1.5;}
  .known{margin:0 0 16px; display:flex; flex-direction:column; gap:6px;}
  .known-label{font-size:12px; font-weight:700; letter-spacing:.04em; text-transform:uppercase; color:var(--ink-soft);}
  .known-btn{display:flex; justify-content:space-between; align-items:center; gap:10px; text-align:left; font-family:inherit; font-size:14.5px; padding:10px 12px; border:1.5px solid var(--rule); border-radius:10px; background:var(--paper); color:var(--ink); cursor:pointer;}
  .known-btn:hover{border-color:var(--navy-2);}
  .known-btn small{font-size:12px; color:var(--ink-soft);}
  .rec-card{background:var(--card); border:1px solid var(--rule); border-radius:14px; padding:18px; margin-bottom:14px;}
  .rec-card h2{font-size:19px; margin-bottom:10px;}
  .rec-card h3{font-size:15px; margin:4px 0 8px;}
  .rec-table-wrap{overflow-x:auto;}
  .rec-table{width:100%; border-collapse:collapse; font-size:13.5px; font-variant-numeric:tabular-nums;}
  .rec-table th{text-align:left; font-size:11.5px; text-transform:uppercase; letter-spacing:.04em; color:var(--ink-soft); padding:6px 8px; border-bottom:1px solid var(--rule); white-space:nowrap;}
  .rec-table td{padding:8px; border-bottom:1px solid var(--rule); white-space:nowrap;}
  .rec-bar{display:inline-block; width:70px; height:6px; border-radius:99px; background:var(--rule); overflow:hidden; vertical-align:middle; margin-right:6px;}
  .rec-bar i{display:block; height:100%; background:var(--success);}
  .rec-empty{font-size:13.5px; color:var(--ink-soft);}
  .sec-sub{max-width:900px; margin:0 auto; padding:10px 16px 0; font-size:12.5px; font-weight:700; color:var(--accent-text); letter-spacing:.02em;}
  .opt{flex-wrap:wrap;}
  .opt-l{font-family:'IBM Plex Mono',monospace; font-size:13px; font-weight:600; color:var(--ink-soft);}
  .opt-t{flex:1; min-width:0;}
  .opt.is-chosen:not(.is-correct):not(.is-wrong){border-color:var(--navy-2); background:var(--gold-soft);}
  .opt-tag{font-size:11px; font-weight:700; padding:2px 8px; border-radius:99px; background:var(--card); border:1px solid currentColor; white-space:nowrap;}
  .opt.is-correct .opt-tag{color:var(--success);} .opt.is-wrong .opt-tag{color:var(--danger);} .opt.is-chosen:not(.is-correct):not(.is-wrong) .opt-tag{color:var(--accent-text);}
  .chosen{font-size:13.5px; margin-top:10px; padding:8px 12px; border-radius:9px;}
  .chosen.ok{background:var(--success-soft); color:var(--success);} .chosen.bad{background:var(--danger-soft); color:var(--danger);}
  .chosen + .chosen{margin-top:6px;}
  .solution{margin-top:14px; border:1px solid var(--rule); border-left:4px solid var(--gold); background:var(--paper-2); border-radius:10px; padding:12px 14px;}
  .sol-h{font-family:'Fraunces',Georgia,serif; font-weight:700; font-size:14px; color:var(--accent-text); margin-bottom:6px;}
  .sol-line{font-size:14.5px; line-height:1.7;}
  .rev-sol summary{cursor:pointer; font-size:12.5px; font-weight:700; color:var(--accent-text); margin-top:6px;}
  .rev-sol .solution{margin-top:8px;}
  .chapter-credit{max-width:900px; margin:4px auto 0; font-size:12px; color:#CFD7EA;}
  footer.brandfoot a{color:inherit;}
  .blank-input.wide{width:260px; max-width:100%; font-family:'Source Sans 3',sans-serif;}
  .blank-input.expr{width:170px; max-width:100%;}
  /*fix-layout*/ .cp-fill,.sp-fill{width:0;} .fld{min-width:0;} .fld input{width:100%; min-width:0; box-sizing:border-box;}
  .fig{margin:6px 0 10px; display:flex; justify-content:center;}
  .figsvg{width:100%; max-width:340px; height:auto; overflow:visible;}
  .figsvg .ln,.figsvg .arm{stroke:var(--ink); stroke-width:1.6; fill:none;}
  .figsvg .arm{stroke:var(--accent-text); stroke-width:2;}
  .figsvg .pt{fill:var(--ink);}
  .figsvg .lb{fill:var(--ink); font:600 13px 'Source Sans 3',sans-serif;}
  .figsvg .al{fill:var(--accent-text); font:700 12px 'Source Sans 3',sans-serif;}
  .figsvg .wg{fill:var(--gold-soft); stroke:var(--gold); stroke-width:1.2;}
  .figsvg .wg2{fill:rgba(199,154,62,.35); stroke:var(--gold); stroke-width:1.2;}
  .figsvg .ra{fill:none; stroke:var(--ink); stroke-width:1.2;}
  .figsvg .ahd{fill:var(--ink);}
  .figsvg .pr{fill:var(--paper-2); stroke:var(--ink-soft); stroke-width:1.2;}
  .figsvg .tk{stroke:var(--ink-soft); stroke-width:.8;}
  .figsvg .po{fill:var(--ink); font:600 8.5px 'IBM Plex Mono',monospace;}
  .figsvg .pi{fill:var(--danger); font:600 7.5px 'IBM Plex Mono',monospace;}
  .figsvg .sh{fill:var(--gold-soft); stroke:var(--ink); stroke-width:1.5; stroke-linejoin:round;}
  .figsvg .sh2{fill:rgba(199,154,62,.38); stroke:var(--ink); stroke-width:1.5; stroke-linejoin:round;}
  .figsvg .sh3{fill:rgba(199,154,62,.22); stroke:var(--ink); stroke-width:1.5; stroke-linejoin:round;}
  .figsvg .none{fill:none;}
  .figsvg .hid{stroke-dasharray:5 4; fill:none;}
  .figsvg .tick{stroke:var(--ink); stroke-width:1.4; fill:none;}
  .figsvg .shd{fill:var(--accent-text); fill-opacity:.55;}
  .figsvg .cell{fill:var(--card); stroke:var(--ink); stroke-width:1.1;}
  .figsvg .dr{fill:var(--danger);} .figsvg .dw{fill:var(--card); stroke:var(--ink); stroke-width:1.2;}
  .figsvg .dotfill{fill:var(--danger);}
  .tt{border-collapse:collapse; font-size:13.5px; margin:4px auto; font-variant-numeric:tabular-nums;} .tt th,.tt td{border:1px solid var(--rule); padding:4px 9px; text-align:left;} .tt th{background:var(--paper-2); font-weight:700;} .ttw{overflow-x:auto; max-width:100%;}
  .fq{display:inline-flex; flex-direction:column; vertical-align:middle; text-align:center; font-size:.82em; line-height:1.12; margin:0 2px;}
  .fq>span:first-child{border-bottom:1.5px solid currentColor; padding:0 2px;}
  .fq>span:last-child{padding:0 2px;}
  .mx{white-space:nowrap;}
  .blank-input.fr{width:110px;}
  @media (prefers-reduced-motion:reduce){ *{transition:none !important;} }
.datline{display:block;margin-top:8px;padding:8px 10px;border-radius:8px;background:var(--paper-2);font:500 14px/1.7 'IBM Plex Mono',monospace;word-spacing:2px;overflow-wrap:anywhere;}

  .theory{display:flex;flex-direction:column;gap:16px;padding-bottom:40px;}
  .hub{display:grid;grid-template-columns:1fr;gap:12px;}
  @media (min-width:640px){ .hub{grid-template-columns:repeat(3,1fr);} }
  .hub-card{background:var(--card);border:1px solid var(--rule);border-radius:14px;padding:16px;display:flex;flex-direction:column;gap:8px;}
  .hub-card h3{font-family:'Fraunces',serif;font-size:18px;margin:0;color:var(--accent-text);}
  .hub-card p{margin:0;font-size:14px;color:var(--ink-soft);line-height:1.5;}
  .hub-btns{display:flex;flex-wrap:wrap;gap:8px;margin-top:auto;}
  .hub-btn{min-height:40px;border:1.5px solid var(--rule);background:var(--paper-2);color:var(--ink);border-radius:10px;padding:8px 12px;font:600 14px 'Source Sans 3',sans-serif;cursor:pointer;text-align:left;}
  .hub-btn:hover{border-color:var(--gold);}
  .hub-btn.primary{background:var(--navy);color:#F4EFDF;border-color:var(--navy);}
  .note{background:var(--card);border:1px solid var(--rule);border-radius:14px;padding:18px;scroll-margin-top:120px;}
  .note h2{font-family:'Fraunces',serif;font-size:22px;margin:0 0 4px;color:var(--ink);}
  .note .lt{font-size:13.5px;color:var(--ink-soft);margin:0 0 12px;}
  .note .lt b{color:var(--accent-text);}
  .note h4{font:700 15px 'Source Sans 3',sans-serif;margin:16px 0 6px;color:var(--accent-text);}
  .note p,.note li{font-size:15.5px;line-height:1.6;}
  .note ul{padding-left:20px;margin:6px 0;}
  .keybox{background:var(--gold-soft);border-left:4px solid var(--gold);border-radius:8px;padding:10px 12px;margin:10px 0;font-size:15px;line-height:1.6;}
  .keybox b{color:var(--ink);}
  .ex{background:var(--paper-2);border-radius:10px;padding:12px;margin:10px 0;}
  .ex .exh{font-family:'Fraunces',serif;font-weight:700;color:var(--accent-text);margin-bottom:4px;}
  .ex .exl{font-size:15px;line-height:1.7;}
  .ttab{width:100%;border-collapse:collapse;font-size:14.5px;margin:8px 0;}
  .ttab th,.ttab td{border:1px solid var(--rule);padding:7px 8px;text-align:left;vertical-align:top;}
  .ttab th{background:var(--paper-2);}
  .tscroll{overflow-x:auto;}
  .mono{font-family:'IBM Plex Mono',monospace;font-size:.92em;}
  @media (max-width:480px){ .ttab{font-size:13.5px;} .ttab th,.ttab td{padding:6px;} }
  .note .figsvg{max-width:100%;height:auto;display:block;margin:8px auto;}


  .rep-top{display:flex;flex-wrap:wrap;gap:18px;align-items:center;justify-content:center;margin-top:8px;}
  .rep-legend{flex:1;min-width:220px;display:flex;flex-direction:column;gap:8px;}
  .rep-cap{font:700 13px 'Source Sans 3',sans-serif;color:var(--ink-soft);text-transform:uppercase;letter-spacing:.05em;}
  .rep-li{display:flex;align-items:center;gap:6px;font-size:15px;}
  .rep-n{margin-left:auto;white-space:nowrap;padding-left:8px;font-family:'IBM Plex Mono',monospace;font-weight:600;}
  .sw{display:inline-block;width:12px;height:12px;border-radius:3px;flex:none;}
  .rep-grid{display:grid;grid-template-columns:1fr;gap:12px;}
  @media (min-width:640px){ .rep-grid{grid-template-columns:1fr 1fr;} }
  .rep-card{background:var(--card);border:1px solid var(--rule);border-radius:14px;padding:14px;display:flex;flex-direction:column;gap:10px;}
  .rep-h{display:flex;align-items:center;gap:8px;font:700 16px 'Source Sans 3',sans-serif;}
  .crit{display:inline-grid;place-items:center;width:28px;height:28px;border-radius:50%;color:var(--card);font:700 15px Fraunces,serif;flex:none;}
  .rep-row{display:flex;gap:14px;align-items:center;}
  .rep-stats{display:flex;flex-direction:column;gap:5px;font-size:14.5px;}
  .rep-stats div{display:flex;align-items:center;gap:6px;}
  .rep-lvl{margin-top:4px;color:var(--accent-text);} .rep-lvl span{color:var(--ink-soft);font-size:13px;}
  .rep-note{font-size:13px;color:var(--ink-soft);}


  .skip-chips{display:flex;flex-wrap:wrap;gap:8px;justify-content:center;margin:12px 0;}
  .skip-chips .chip{min-width:48px;min-height:40px;cursor:pointer;border:1.5px solid var(--gold);background:var(--gold-soft);color:var(--retry-text);border-radius:10px;font:600 14px 'IBM Plex Mono',monospace;}
  .skip-btns{display:flex;flex-wrap:wrap;gap:10px;justify-content:center;margin-top:12px;}


  .kb-toggle{border:none;background:transparent;font-size:15px;cursor:pointer;padding:0 2px;vertical-align:middle;opacity:.7;}
  .vkb{position:fixed;left:0;right:0;bottom:0;z-index:80;background:var(--paper-2);border-top:1px solid var(--rule);box-shadow:0 -6px 20px rgba(0,0,0,.12);padding:6px 6px 8px;display:none;}
  .vkb.show{display:block;}
  .vkb-top{display:flex;justify-content:space-between;align-items:center;max-width:640px;margin:0 auto 4px;font:600 12px 'Source Sans 3',sans-serif;color:var(--ink-soft);}
  .vkb-link{border:none;background:none;color:var(--accent-text);font:600 12px 'Source Sans 3',sans-serif;cursor:pointer;text-decoration:underline;}
  .vkb-row{display:flex;gap:5px;max-width:640px;margin:0 auto 5px;}
  .vkb-k{flex:1;min-height:42px;border:1px solid var(--rule);border-radius:8px;background:var(--card);color:var(--ink);font:600 17px 'IBM Plex Mono',monospace;cursor:pointer;padding:0;}
  .vkb-k.fn{font:600 13px 'Source Sans 3',sans-serif;background:var(--gold-soft);}
  .vkb-k.done{background:var(--navy);color:#F4EFDF;border-color:var(--navy);}
  .vkb-k:active{transform:scale(.96);}
  body.kb-open .wrap{padding-bottom:360px;}
  body.kb-open .fab{display:none;}
  .tool-bar{display:flex;gap:8px;flex-wrap:wrap;margin:-4px 0 10px;}
  .tool-btn{min-height:36px;border:1.5px solid var(--gold);background:var(--gold-soft);color:var(--ink);border-radius:18px;padding:4px 12px;font:600 13.5px 'Source Sans 3',sans-serif;cursor:pointer;}
  .tool-panel{position:fixed;z-index:85;background:var(--card);border:1px solid var(--rule);border-radius:14px;box-shadow:0 10px 30px rgba(0,0,0,.25);display:none;}
  .tool-panel.show{display:block;}
  .tp-head{display:flex;align-items:center;gap:8px;padding:8px 10px;border-bottom:1px solid var(--rule);font:600 14px 'Source Sans 3',sans-serif;}
  .tp-note{font-size:12px;color:var(--ink-soft);font-weight:500;}
  .tp-x{margin-left:auto;border:1px solid var(--rule);background:var(--paper-2);color:var(--ink);border-radius:8px;min-height:32px;padding:2px 10px;cursor:pointer;font:600 13px 'Source Sans 3',sans-serif;}
  .tp-x + .tp-x{margin-left:0;}
  .calc{right:12px;bottom:84px;width:min(330px,calc(100vw - 24px));}
  body.calc-open .wrap{padding-bottom:440px;}
  body.calc-open .fab{display:none;}
  @media (max-width:640px){ .calc{left:6px;right:6px;width:auto;} .calc-keys button{min-height:36px;} }
  .calc-disp{padding:8px 12px;text-align:right;background:var(--paper-2);}
  .calc-expr{font:500 13px 'IBM Plex Mono',monospace;color:var(--ink-soft);min-height:18px;word-break:break-all;}
  .calc-res{font:600 24px 'IBM Plex Mono',monospace;color:var(--ink);word-break:break-all;}
  .calc-keys{display:grid;grid-template-columns:repeat(6,1fr);gap:5px;padding:8px;}
  .calc-keys button{min-height:40px;border:1px solid var(--rule);border-radius:8px;background:var(--card);color:var(--ink);font:600 14px 'IBM Plex Mono',monospace;cursor:pointer;padding:0;}
  .calc-keys button.fn{background:var(--gold-soft);font-family:'Source Sans 3',sans-serif;font-size:13px;}
  .calc-keys button.eq{grid-column:span 2;background:var(--navy);color:#F4EFDF;border-color:var(--navy);}
  .desmos{left:50%;top:50%;transform:translate(-50%,-50%);width:min(760px,calc(100vw - 16px));height:min(560px,calc(100vh - 90px));flex-direction:column;}
  .desmos.show{display:flex;}
  #desmosBox{flex:1;min-height:0;border-radius:0 0 14px 14px;overflow:hidden;}
  .desmos-msg{padding:24px;text-align:center;color:var(--ink-soft);}
  .chip[data-status="skipped"]{cursor:pointer;}
  .chip[data-status="answered"]{border-color:var(--accent-text);color:var(--accent-text);}


  button.crest-home{border:none;padding:0;position:relative;cursor:pointer;transition:transform .15s ease;}
  button.crest-home:hover,button.crest-home:focus-visible{transform:scale(1.06);outline:2px solid var(--gold);outline-offset:2px;}
  .crest-h{position:absolute;right:-7px;bottom:-7px;width:18px;height:18px;border-radius:50%;background:#F4EFDF;color:var(--navy);font:700 12px/18px 'Source Sans 3',sans-serif;text-align:center;box-shadow:0 1px 3px rgba(0,0,0,.3);}
  .brand .brand-row{position:relative;}
  .bmasw{position:absolute;left:50%;top:50%;transform:translate(-50%,-50%);display:flex;flex-shrink:0;white-space:nowrap;align-items:center;gap:6px;background:rgba(255,255,255,.12);border:1px solid rgba(255,255,255,.25);border-radius:99px;padding:5px 14px;color:#F4EFDF;}
  .bmasw-ic{font-size:16px;} .bmasw-t{font:600 20px 'IBM Plex Mono',monospace;letter-spacing:.02em;min-width:62px;text-align:center;}
  .bmasw-b{border:none;background:rgba(255,255,255,.18);color:#F4EFDF;border-radius:50%;width:30px;height:30px;cursor:pointer;font-size:13px;}
  .bmasw.off{display:none;}
  @media (max-width:560px){ .bmasw{position:static;transform:none;margin-left:auto;padding:4px 5px 4px 8px;gap:4px;} .bmasw-ic{display:none;} .bmasw-t{font-size:16px;min-width:48px;} .bmasw-b{width:26px;height:26px;} .brand .series-name{font-size:15px;} .brand .brand-name{font-size:10.5px;} .brand .brand-row>div:not(.bmasw){min-width:0;} }
  .bmasw-done{font:600 15px 'IBM Plex Mono',monospace;color:var(--accent-text);margin:4px 0 8px;}
  .sp-fab{position:fixed;left:14px;bottom:84px;z-index:60;border:1.5px solid var(--navy-2);background:var(--card);color:var(--ink);border-radius:99px;padding:9px 14px;font:700 14px 'Source Sans 3',sans-serif;box-shadow:0 4px 14px rgba(0,0,0,.15);cursor:pointer;}
  .sp-fab.on{background:var(--navy);color:#F4EFDF;}
  body.kb-open .sp-fab{display:none;}
  .sp-canvas{position:absolute;z-index:55;display:none;touch-action:none;cursor:crosshair;}
  .sp-canvas.passive{pointer-events:none;cursor:default;}
  .sp-bar{position:fixed;top:8px;left:8px;right:8px;margin:0 auto;width:max-content;z-index:90;display:none;align-items:center;gap:6px;background:var(--card);border:1px solid var(--rule);border-radius:14px;padding:6px 8px;box-shadow:0 6px 20px rgba(0,0,0,.2);max-width:calc(100vw - 16px);flex-wrap:wrap;justify-content:center;}
  .sp-lbl{font:700 13px 'Source Sans 3',sans-serif;color:var(--ink-soft);margin-right:2px;}
  .sp-pen,.sp-tool{width:38px;height:38px;border-radius:10px;border:1.5px solid var(--rule);background:var(--paper);cursor:pointer;display:inline-flex;align-items:center;justify-content:center;font-size:17px;padding:0;color:var(--ink);}
  .sp-pen i{width:20px;height:20px;border-radius:50%;display:block;}
  .sp-pen.on,.sp-tool.on{border-color:var(--navy-2);box-shadow:0 0 0 3px var(--gold-soft);}
  @media (max-width:560px){ .sp-lbl{display:none;} .sp-pen,.sp-tool{width:34px;height:34px;} .sp-fab span{display:none;} }

  /* larger reading sizes */
  .chapter-eyebrow{font-size:13.5px;}
  .chapter-title{font-size:36px;line-height:1.15;}
  .chapter-sub{font-size:16.5px;}
  .tab-btn{font-size:15.5px;}
  .sec-sub{font-size:15px;}
  .qtext{font-size:19px;line-height:1.55;}
  .qnum{width:36px;height:36px;font-size:16px;}
  .opt{font-size:17.5px;padding:12px 14px;}
  .step-line{font-size:17.5px;line-height:2;}
  .blank-input{font-size:16px;}
  .sol-line{font-size:16.5px;}
  .feedback{font-size:15px;}
  .note h2{font-size:28px;}
  .note h4{font-size:19px;}
  .note p,.note li{font-size:17.5px;line-height:1.65;}
  .note .lt{font-size:15.5px;}
  .ex .exh{font-size:18px;} .ex .exl{font-size:16.5px;}
  .keybox{font-size:16.5px;}
  .ttab{font-size:15.5px;}
  .hub-card h3{font-size:21px;} .hub-card p{font-size:15.5px;} .hub-btn{font-size:15px;}
  @media (max-width:480px){ .chapter-title{font-size:30px;} .qtext{font-size:18px;} .opt,.step-line{font-size:16.5px;} .note h2{font-size:24px;} .note p,.note li{font-size:16.5px;} }
</style>
</head>
<body>
<header class="brand">
  <div class="brand-row">
    <div class="crest">BM</div>
    <div>
      <div class="brand-name">Brain &amp; Mind Academy</div>
      <div class="series-name">Sopaan <span style="font-weight:400;font-size:14px;color:#CFD7EA;">Practice Series</span></div>
    </div>
  </div>
  <div class="chapter-eyebrow">Class 8 Mathematics · Chapter 7</div>
  <div class="chapter-title">Algebraic Expressions and Identities</div>
  <div class="chapter-sub">Theory Notes · Practice by Learning Objective · Learning Assessment</div><div class="chapter-credit">Mixed multiple-choice and fill-in-the-blank practice · Chapter 7</div>
  <div class="chapter-progress">
    <div class="cp-track"><div class="cp-fill" id="cpFill"></div></div>
    <div class="cp-label" id="cpLabel">0% complete</div>
  </div>
  <div class="who-row"><button class="mode-pill" id="modePill" hidden>Choose a mode</button><span class="who" id="whoBar" hidden></span></div>
</header>

<nav class="tabbar"><div class="tabbar-inner" id="tabbar"></div></nav>
<div class="sec-sub" id="secSub"></div><div class="slide-progress"><div class="sp-track"><div class="sp-fill" id="spFill"></div></div><div class="sp-label" id="spLabel">Question 1 of 49</div></div>
<div class="wrap" id="wrap"></div>
<footer class="brandfoot">Brain &amp; Mind Academy · Sopaan Practice Series · Class 8 Mathematics · Chapter 7<br>Chapter follows the Class 8 mathematics syllabus (New Enjoying Mathematics, Class 8). Theory notes, questions, learning assessments and worked solutions are written by Brain &amp; Mind Academy.</footer>

<div class="navbar"><div class="navbar-inner" id="navbarInner"></div></div>
<button class="fab" id="paletteFab"><span>Questions</span><span class="fab-badge" id="fabBadge">0/49</span></button>

<div class="overlay" id="overlay">
  <div class="palette" role="dialog" aria-label="Question palette">
    <div class="palette-head"><h2 id="paletteTitle">Question palette</h2><button class="palette-close" id="paletteClose">&times;</button></div>
    <div class="palette-legend">
      <span><i class="dot current"></i>Current</span><span><i class="dot correct"></i>Correct</span>
      <span><i class="dot revealed"></i>Revealed</span><span><i class="dot skipped"></i>Skipped</span>
      <span><i class="dot locked"></i>Locked</span>
    </div>
    <div class="chip-grid" id="paletteBody"></div>
  </div>
</div>
<div class="toast" id="toast"></div>

<script>
(function(){
"use strict";

/* ================= audio ================= */
var audioCtx=null;
function ensureAudio(){ if(!audioCtx){ try{ audioCtx=new (window.AudioContext||window.webkitAudioContext)(); }catch(e){} } return audioCtx; }
function playTone(freqs,dur,type){
  var ctx=ensureAudio(); if(!ctx) return;
  try{
    var t0=ctx.currentTime;
    freqs.forEach(function(f,i){
      var o=ctx.createOscillator(), g=ctx.createGain();
      o.type=type||'sine'; o.frequency.value=f;
      var start=t0+i*dur;
      g.gain.setValueAtTime(0.0001,start);
      g.gain.exponentialRampToValueAtTime(0.16,start+0.02);
      g.gain.exponentialRampToValueAtTime(0.0001,start+dur);
      o.connect(g); g.connect(ctx.destination);
      o.start(start); o.stop(start+dur+0.02);
    });
  }catch(e){}
}
function playSuccess(){ playTone([523.25,659.25,783.99],0.11,'sine'); }
function playWrong(){ playTone([220,185],0.14,'square'); }
function playReveal(){ playTone([300,220],0.16,'triangle'); }

/* ================= helpers ================= */
function norm(s){
  return String(s===undefined||s===null?'':s).trim().toLowerCase().replace(/\s+/g,'')
    .replace(/[×∗*·]/g,'x').replace(/÷/g,'/').replace(/–|—|−/g,'-')
    .replace(/[²]/g,'^2').replace(/[³]/g,'^3').replace(/[⁴]/g,'^4').replace(/[⁵]/g,'^5')
    .replace(/[⁶]/g,'^6').replace(/[⁷]/g,'^7').replace(/[⁸]/g,'^8').replace(/[⁹]/g,'^9')
    .replace(/\^/g,'');
}
function parseNum(s){
  if(s===undefined||s===null) return null;
  var t=String(s).trim().replace(/,/g,'').replace(/[−–—]/g,'-').replace(/\s+/g,''); if(t==='') return null;
  var neg=false; if(t[0]==='-'){neg=true;t=t.slice(1);}
  var m=t.match(/^(\d+)\/(\d+)$/);
  if(m){ var v=parseInt(m[1],10)/parseInt(m[2],10); return neg?-v:v; }
  if(/^\d+(\.\d+)?$/.test(t)){ var v2=parseFloat(t); return neg?-v2:v2; }
  return null;
}
/* ---- expression checker: compares answers like (P-2w)/2 and P/2-w at random values ---- */
function exprPrep(s){
  return String(s).toLowerCase().replace(/\s+/g,'').replace(/^[a-z]\(x\)=/i,'').replace(/^y=/i,'').replace(/[×∗·]/g,'*').replace(/÷/g,'/').replace(/[−–—]/g,'-')
    .replace(/²/g,'^2').replace(/³/g,'^3').replace(/⁴/g,'^4').replace(/⁵/g,'^5').replace(/⁶/g,'^6').replace(/⁷/g,'^7').replace(/⁸/g,'^8').replace(/⁹/g,'^9').replace(/π/g,'#').replace(/pi/gi,'#').replace(/½/g,'(1/2)');
}
function exprCompile(src){
  var s=exprPrep(src), i=0, toks=[], absDepth=0;
  while(i<s.length){
    var ch=s[i];
    if(/[0-9.]/.test(ch)){ var j=i; while(j<s.length && /[0-9.]/.test(s[j])) j++; toks.push({k:'n',v:parseFloat(s.slice(i,j))}); i=j; continue; }
    if(/[a-zA-Z#]/.test(ch)){ toks.push({k:'v',v:ch}); i++; continue; }
    if(ch==='|'){ var pv=toks[toks.length-1]; var opn=(absDepth===0)||!pv||('+-*/^(['.indexOf(pv.k)>=0); if(opn){ absDepth++; toks.push({k:'['}); } else { absDepth--; toks.push({k:']'}); } i++; continue; }
    if('+-*/^()'.indexOf(ch)>=0){ toks.push({k:ch}); i++; continue; }
    return null;
  }
  var out=[];
  for(var t=0;t<toks.length;t++){
    var a=toks[t], b=out[out.length-1];
    if(b && (b.k==='n'||b.k==='v'||b.k===')'||b.k===']') && (a.k==='n'||a.k==='v'||a.k==='('||a.k==='[')) out.push({k:'&'});
    out.push(a);
  }
  var p=0;
  function peek(){ return out[p]; }
  function parseE(){ var n=parseT(); while(peek() && (peek().k==='+'||peek().k==='-')){ var o=out[p++].k, r=parseT(); n=(function(l,r,o){return function(e){ return o==='+'?l(e)+r(e):l(e)-r(e); };})(n,r,o); } return n; }
  function parseI(){ var n=parseU(); while(peek() && peek().k==='&'){ p++; var r=parseP(); n=(function(l,r){return function(e){ return l(e)*r(e); };})(n,r); } return n; }
  function parseT(){ var n=parseI(); while(peek() && (peek().k==='*'||peek().k==='/')){ var o=out[p++].k, r=parseI(); n=(function(l,r,o){return function(e){ return o==='*'?l(e)*r(e):l(e)/r(e); };})(n,r,o); } return n; }
  function parseU(){ if(peek() && peek().k==='-'){ p++; var u=parseU(); return function(e){ return -u(e); }; } if(peek() && peek().k==='+'){ p++; return parseU(); } return parseP(); }
  function parseP(){ var b=parseA(); if(peek() && peek().k==='^'){ p++; var x=parseU(); return function(e){ return Math.pow(b(e),x(e)); }; } return b; }
  function parseA(){
    var t=out[p++]; if(!t) throw 0;
    if(t.k==='n') return function(){ return t.v; };
    if(t.k==='v') return t.v==='#' ? function(){ return Math.PI; } : function(e){ return e[t.v]; };
    if(t.k==='('){ var n=parseE(); if(!peek()||peek().k!==')') throw 0; p++; return n; }
    if(t.k==='['){ var m=parseE(); if(!peek()||peek().k!==']') throw 0; p++; return function(e){ return Math.abs(m(e)); }; }
    throw 0;
  }
  try{ var f=parseE(); if(p!==out.length) return null; return f; }catch(e){ return null; }
}
function exprEqual(input,answer){
  var f=exprCompile(input), g=exprCompile(answer); if(!f||!g) return false;
  var hits=0;
  for(var trial=0;trial<8;trial++){
    var env={}; 'abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ'.split('').forEach(function(c){ env[c]=1.3+Math.random()*4.1; });
    var x=f(env), y=g(env);
    if(!isFinite(x)||!isFinite(y)) continue;
    if(Math.abs(x-y)>1e-7*Math.max(1,Math.abs(x),Math.abs(y))) return false;
    hits++;
  }
  return hits>=3;
}
function wordsNorm(s){ return String(s||'').toLowerCase().replace(/\band\b/g,' ').replace(/[^a-z]/g,''); }
function listNorm(s){ return (String(s||'').replace(/[−–—]/g,'-').replace(/(\d) (?=\d{3}\b)/g,'$1').match(/-?\d+(\.\d+)?/g)||[]).join(','); }
function powNorm(s){ return String(s||'').toLowerCase().replace(/\s+/g,'').replace(/[×∗*·.]/g,'x').replace(/[⁰¹²³⁴⁵⁶⁷⁸⁹]+/g,function(m){ return '^'+m.split('').map(function(c){ return '⁰¹²³⁴⁵⁶⁷⁸⁹'.indexOf(c); }).join(''); }).replace(/\^1(?!\d)/g,''); }
function fr(s){ return String(s).replace(/\{(\d+) (\d+)\/(\d+)\}/g,'<span class="mx">$1<span class="fq"><span>$2</span><span>$3</span></span></span>').replace(/\{(\d+)\/(\d+)\}/g,'<span class="fq"><span>$1</span><span>$2</span></span>'); }
function gcdI(a,b){ a=Math.abs(a); b=Math.abs(b); while(b){ var t=a%b; a=b; b=t; } return a; }
function fracParse(s){ s=String(s===undefined||s===null?'':s).trim().replace(/[\u2044\u2215\u00f7]/g,'/').replace(/\s+/g,' ').replace(/\s*\/\s*/g,'/'); var m;
  if((m=s.match(/^(-?\d+)$/))) return {v:+m[1],form:'int',n:+m[1],d:1};
  if((m=s.match(/^(-?\d+)\/(\d+)$/))){ if(+m[2]===0) return null; return {v:m[1]/m[2],form:'frac',n:+m[1],d:+m[2]}; }
  if((m=s.match(/^(-?)(\d+)(?: |\+)(\d+)\/(\d+)$/))){ if(+m[4]===0) return null; var sg=m[1]?-1:1; return {v:sg*(+m[2]+m[3]/m[4]),form:'mixed',w:sg*m[2],n:+m[3],d:+m[4]}; }
  if((m=s.match(/^-?\d*\.\d+$/))) return {v:parseFloat(s),form:'dec'};
  return null; }
function fracOK(mode,input,answer){
  if(mode==='flist'){ var A=String(input).split(/[,;]/).map(function(x){return x.trim();}).filter(Boolean), K=String(answer).split(/[,;]/).map(function(x){return x.trim();});
    if(A.length!==K.length) return false; return A.every(function(x,i){ var a=fracParse(x), k=fracParse(K[i]); return a&&k&&Math.abs(a.v-k.v)<1e-9; }); }
  var a=fracParse(input), k=fracParse(answer); if(!a||!k) return false;
  var same=Math.abs(a.v-k.v)<1e-9; if(!same) return false;
  if(mode==='fv') return true;
  if(mode==='dec') return a.form==='dec'||a.form==='int';
  if(mode==='fe') return (a.form==='frac'&&k.form==='frac'&&a.n===k.n&&a.d===k.d)||(a.form==='int'&&k.form==='int');
  if(mode==='fi') return a.form==='frac'||(a.form==='int'&&k.form==='int');
  if(mode==='fl') return a.form==='int'||(a.form==='frac'&&gcdI(a.n,a.d)===1)||(a.form==='mixed'&&a.n<a.d&&gcdI(a.n,a.d)===1);
  if(mode==='fm') return a.form==='int'||(a.form==='mixed'&&a.n>0&&a.n<a.d&&gcdI(a.n,a.d)===1);
  return false; }
function answerMatches(input,answer,accept,expr){
  if(expr==='dec'||expr==='fv'||expr==='fe'||expr==='fl'||expr==='fm'||expr==='fi'||expr==='flist'){ if(input===undefined||input===null||String(input).trim()==='') return false; return fracOK(expr,input,answer); }
  if(input===undefined||input===null||String(input).trim()==='') return false;
  if(expr==='words'){ return [answer].concat(accept||[]).some(function(a){ if(/\d/.test(a)) return norm(a)===norm(input); var w=wordsNorm(a); return w!=='' && w===wordsNorm(input); }); }
  if(expr==='list'){ return [answer].concat(accept||[]).some(function(a){ return listNorm(a)===listNorm(input); }); }
  if(expr==='pow'){ return [answer].concat(accept||[]).some(function(a){ return powNorm(a)===powNorm(input); }); }
  if(expr==='time'){ var tn=function(x){ var t=String(x).toLowerCase().replace(/[\s.]/g,'').replace(/[:h]/g,''); if(/^\d{3}(am|pm)?$/.test(t)) t='0'+t; return t; }; return [answer].concat(accept||[]).some(function(a){ return tn(a)===tn(input); }); }
  if(expr==='glist'){ var gn=function(x){ return String(x).toUpperCase().split(/[\s,;]+/).filter(Boolean).sort().join(','); }; return [answer].concat(accept||[]).some(function(a){ return gn(a)===gn(input); }); }
  if(expr==='coord'){ var cn=function(x){ return String(x).replace(/[\u2212\u2013\u2014]/g,'-').replace(/[\s()\[\]]/g,''); }; return [answer].concat(accept||[]).some(function(a){ return cn(a)===cn(input); }); }
  if(expr==='dlist'){ var dn=function(x){ return (String(x).replace(/[−–—]/g,'-').match(/-?\d*\.?\d+/g)||[]).map(Number).join(','); }; return [answer].concat(accept||[]).some(function(a){ return dn(a)===dn(input); }); }
  if(expr==='set'){ var sn=function(x){ return (String(x).match(/-?\d+/g)||[]).map(Number).sort(function(a,b){return a-b;}).join(','); }; return [answer].concat(accept||[]).some(function(a){ return sn(a)===sn(input); }); }
  if(expr==='primes'){ var pn=function(x){ var t=powNorm(x).replace(/[^0-9x^]/g,''); var out=[]; t.split('x').forEach(function(tok){ if(!tok) return; var m=tok.split('^'); var b=+m[0], e=m[1]?+m[1]:1; for(var i=0;i<e;i++) out.push(b); }); return out.sort(function(a,b){return a-b;}).join(','); }; return [answer].concat(accept||[]).some(function(a){ return pn(a)===pn(input); }); }
  if(expr==='angle'){ var an=function(x){ return String(x).toUpperCase().replace(/[^A-Z]/g,''); }; var k=an(answer), v=an(input); return v===k || v===k.split('').reverse().join(''); }
  if(expr==='trans'){ var tv=function(x){ var s=String(x).toLowerCase().replace(/[−–—]/g,'-').replace(/\b(units?|squares?|and|then|steps?|to|the|a)\b/g,' ').replace(/[,;.]/g,' '); var re=/(\d+)\s*(right|left|up|down|r|l|u|d)\b/g, m, dx=0, dy=0, n=0; while((m=re.exec(s))){ var v=+m[1], d=m[2][0]; if(d==='r')dx+=v; else if(d==='l')dx-=v; else if(d==='u')dy+=v; else dy-=v; n++; } if(!n||s.replace(re,'').replace(/\s+/g,'')!=='') return null; return dx+','+dy; }; var ti=tv(input); return ti!==null && [answer].concat(accept||[]).some(function(a){ return tv(a)===ti; }); }
  if(expr==='rot'){ var rv=function(x){ var s=String(x).toLowerCase().replace(/quarter[\s-]*turn/g,'90').replace(/half[\s-]*turn/g,'180').replace(/three[\s-]*quarter[\s-]*turn/g,'270'); var m=s.match(/\b(90|180|270)\b/); if(!m) return null; var a=+m[1]; if(a===180) return '180'; var dir=/anti|counter|acw|ccw/.test(s)?-1:(/clockwise|\bcw\b/.test(s)?1:0); if(!dir) return null; return String(((a*dir)%360+360)%360); }; var ri=rv(input); return ri!==null && ri===rv(answer); }
  if(expr==='expanded'){ var f=function(x){ return String(x).replace(/\s+/g,'').replace(/,/g,''); }; return [answer].concat(accept||[]).some(function(a){ return f(a)===f(input); }); }
  if(expr===true && input!==undefined && input!==null && String(input).trim()!==''){
    if(exprEqual(input,answer)) return true;
    var alt=String(input).replace(/\/\s*(\d+(?:\.\d+)?)\s*([a-zA-Z(])/g,'/$1*$2'); if(alt!==String(input) && exprEqual(alt,answer)) return true;
    return (accept||[]).some(function(a){ return exprEqual(input,a); });
  }
  if(input===undefined||input===null||String(input).trim()==='') return false;
  var n1=parseNum(input), n2=parseNum(answer);
  if(n1!==null && n2!==null){ if(Math.abs(n1-n2)<1e-3) return true; return (accept||[]).some(function(a){ var n3=parseNum(a); return n3!==null && Math.abs(n1-n3)<1e-3; }); }
  var cands=[answer].concat(accept||[]); var ni=norm(input);
  for(var i=0;i<cands.length;i++){ if(norm(cands[i])===ni) return true; }
  return false;
}
function esc(s){ return String(s).replace(/&/g,'&amp;').replace(/</g,'&lt;'); }

/* ================= DATA ================= */
var AR_OPTIONS = ["Both A and R are true, and R is the correct explanation of A","Both A and R are true, but R is NOT the correct explanation of A","A is true but R is false","A is false but R is true"];
var THEORY = "<div class=\"hub\"><div class=\"hub-card\"><h3>📖 Theory notes</h3><p>Explained notes for every part of the chapter, following the book, with rules, area models and solved examples.</p><div class=\"hub-btns\"><button class=\"hub-btn\" data-jump=\"n71\">7.1 notes</button><button class=\"hub-btn\" data-jump=\"n72\">7.2 notes</button><button class=\"hub-btn\" data-jump=\"n73\">7.3 notes</button><button class=\"hub-btn\" data-jump=\"n74\">7.4 notes</button><button class=\"hub-btn\" data-jump=\"n75\">7.5 notes</button><button class=\"hub-btn\" data-jump=\"n76\">7.6 notes</button></div></div><div class=\"hub-card\"><h3>🎯 Practice by learning objective</h3><p>Every Looking Back, Example, Try This and Exercise question of the chapter, one sheet per objective, mixing multiple-choice and fill-in-the-blank questions. The bold tag shows where each question is in the book.</p><div class=\"hub-btns\"><button class=\"hub-btn\" data-go=\"s1\">7.1 · Expressions and polynomials</button><button class=\"hub-btn\" data-go=\"s2\">7.2 · Addition and subtraction</button><button class=\"hub-btn\" data-go=\"s3\">7.3 · Multiplication of polynomials</button><button class=\"hub-btn\" data-go=\"s4\">7.4 · Division by a monomial</button><button class=\"hub-btn\" data-go=\"s5\">7.5 · Division by a polynomial</button><button class=\"hub-btn\" data-go=\"s6\">7.6 · Algebraic identities</button></div></div><div class=\"hub-card\"><h3>📝 Learning assessment</h3><p>Four short assessments built from the Chapter Check-up, one per skill area. Take them in Quiz mode and open the report to see your results as pie charts.</p><div class=\"hub-btns\"><button class=\"hub-btn\" data-go=\"s7\">A · Knowing and understanding</button><button class=\"hub-btn\" data-go=\"s8\">B · Investigating patterns</button><button class=\"hub-btn\" data-go=\"s9\">C · Communicating</button><button class=\"hub-btn\" data-go=\"s10\">D · Applying mathematics in real-life contexts</button><button class=\"hub-btn primary\" data-go=\"report\">📊 View my report</button></div></div></div><section class=\"note\" id=\"nintro\"><h2>About this chapter</h2><p>Letters such as x, y, a, b stand for numbers (<b>variables</b>); numbers such as 3, 5, −2 are <b>constants</b>. Combining them with +, −, × and ÷ gives <b>algebraic expressions</b>. This chapter classifies expressions, adds, subtracts, multiplies and divides polynomials, and uses four <b>identities</b> to expand products quickly.</p><p>The practice sheets contain <b>all</b> the questions of the chapter in book order. Each question starts with a tag such as <b>Example 7</b>, <b>Try This</b>, <b>Ex 7C · Q4(b)</b> or <b>Check-up · Q12</b>.</p><div class=\"tscroll\"><table class=\"ttab\"><tr><th>Assessment</th><th>Skill area</th><th>What it checks</th></tr><tr><td>A</td><td>Knowing and understanding</td><td>Simplifying, multiplying and dividing correctly.</td></tr><tr><td>B</td><td>Investigating patterns</td><td>Using the identities and long division.</td></tr><tr><td>C</td><td>Communicating</td><td>Degrees, correct notation, spotting errors.</td></tr><tr><td>D</td><td>Applying mathematics in real-life contexts</td><td>Perimeter, area, cost and wages written as polynomials.</td></tr></table></div><p><b>Tools:</b> ⏱ at the top times each tab (pause or reset it). ✏️ opens a scratchpad with four pens for rough work. Tap the BM badge to go back to the home page.</p><p><b>Typing answers:</b> type powers with ^ and write products side by side: <span class=\"mono\">3x<sup>2</sup> − 2xy + y<sup>2</sup></span>. Fraction coefficients can be typed as <span class=\"mono\">3x/4</span> or <span class=\"mono\">(3/4)x</span>; a term like {1/x} is typed <span class=\"mono\">1/x</span>. Any equivalent form of an expression is accepted, but always simplify fully.</p></section><section class=\"note\" id=\"n71\"><h2>7.1 Expressions and polynomials</h2><p class=\"lt\"><b>Objective:</b> Identify terms, coefficients and like terms; classify monomials, binomials, trinomials and polynomials; find the degree of a polynomial.</p><p>A <b>term</b> is a variable, a constant, or a product of variables and constants: 3x<sup>2</sup> = 3 × x × x, 4xy, −5y<sup>2</sup>. Terms are joined by + or − to make an expression; 3x<sup>2</sup> + 4xy − 5y<sup>2</sup> has the terms 3x<sup>2</sup>, 4xy and −5y<sup>2</sup>. The numerical factor of a term is its <b>coefficient</b>: in 2x<sup>3</sup> + 4x<sup>2</sup> + x the coefficients are 2, 4 and 1.</p><p><b>Like terms</b> have the same variables with the same powers (7x, −8x, 3x; 20x<sup>2</sup>y and 5x<sup>2</sup>y; 7yx and 5xy). <b>Unlike terms</b> differ in a variable or a power (2x<sup>2</sup>y and 3xy).</p><h4>Polynomials</h4><p>An expression is a <b>polynomial</b> only when every variable in every term has a <b>non-negative integer</b> power. {4x/y}, 4/x (= 4x<sup>−1</sup>) and √x (= x<sup>1/2</sup>) are not allowed; a constant under a root, as in √7 xy, is fine.</p><div class=\"tscroll\"><table class=\"ttab\"><tr><th>Name</th><th>Number of terms</th><th>Examples</th></tr><tr><td>Monomial</td><td>1</td><td>3xy, p<sup>2</sup>q<sup>3</sup>, 4, {3/4}xy</td></tr><tr><td>Binomial</td><td>2</td><td>a + b, bx<sup>2</sup> + y, √6 ab − a<sup>2</sup>b/5</td></tr><tr><td>Trinomial</td><td>3</td><td>x<sup>2</sup> + x + 3, a<sup>2</sup> + 2ab + b<sup>2</sup></td></tr></table></div><div class=\"ex\"><div class=\"exh\">Book Example 1 · Which are polynomials?</div><div class=\"exl\">f) 5 and h) x<sup>3</sup> are monomials; a) x<sup>2</sup> + 1 and i) {2/3}x<sup>3</sup> − y<sup>3</sup> are binomials; d) x<sup>2</sup> + x + 1 and g) x + y + z are trinomials.<br>b) x/y + 3, c) x<sup>2</sup> + y<sup>−2</sup> and j) x + y<sup>−2</sup> + 1 have a negative power; e) √x has a fractional power. They are not polynomials.</div></div><h4>Degree</h4><p>For one variable, the <b>degree</b> is the highest power of the variable: 4x<sup>6</sup> + x has degree 6, and a constant such as 5 has degree 0. For several variables, add the powers in each term; the highest sum is the degree: 3x<sup>2</sup> + 5x<sup>2</sup>y<sup>3</sup> + xy → sums 2, 5, 2 → degree 5.</p><p>Degree 1: <b>linear</b> (3x + 7); degree 2: <b>quadratic</b> (x<sup>2</sup> + 5x + 6); degree 3: <b>cubic</b> (4y<sup>3</sup> − 2).</p><div class=\"ex\"><div class=\"exh\">Book Example 2 · Degrees</div><div class=\"exl\">a) 7y<sup>2</sup> + √8 y + 9 → 2.  b) 21z<sup>4</sup> + z<sup>3</sup> + 2z<sup>2</sup> + 3 → 4.<br>c) 9x<sup>5</sup>y<sup>6</sup> + 4x<sup>2</sup>y<sup>3</sup> − 17xy → 5 + 6 = 11.  d) 11a<sup>2</sup>b<sup>7</sup> + 5a<sup>4</sup>b<sup>6</sup> − 5a<sup>2</sup>b<sup>4</sup> + 4ab − 25 → 4 + 6 = 10.</div></div><div class=\"keybox\"><b>Descending order:</b> write the terms from the highest power to the lowest: 6x<sup>2</sup> + 4x<sup>3</sup> − 7x<sup>4</sup> + 3x + 4 = −7x<sup>4</sup> + 4x<sup>3</sup> + 6x<sup>2</sup> + 3x + 4.</div><div class=\"hub-btns\" style=\"margin-top:12px\"><button class=\"hub-btn primary\" data-go=\"s1\">Practise 7.1 →</button></div></section><section class=\"note\" id=\"n72\"><h2>7.2 Addition and subtraction</h2><p class=\"lt\"><b>Objective:</b> Add and subtract polynomials by collecting like terms, and solve problems that need addition or subtraction of polynomials.</p><p>Only like terms can be combined: 7x + 8x + 3x = 18x and 35xy − 3xy = 32xy, but 7x + 7y stays as it is. To add polynomials, write like terms one below the other and add each column.</p><div class=\"ex\"><div class=\"exh\">Book Example 3 · Add 7x<sup>2</sup> − 4xy + 8y<sup>2</sup>, 3xy + 4x<sup>2</sup> + 3y<sup>2</sup> and −3x<sup>2</sup> + 6xy − 7y<sup>2</sup></div><div class=\"exl\">x<sup>2</sup>: 7 + 4 − 3 = 8;  xy: −4 + 3 + 6 = 5;  y<sup>2</sup>: 8 + 3 − 7 = 4.<br>Sum = <b>8x<sup>2</sup> + 5xy + 4y<sup>2</sup></b>.</div></div><h4>Subtraction</h4><p>Write the polynomial you subtract <b>from</b> on top. Change the sign of every term of the polynomial being subtracted (its additive inverse) and add.</p><div class=\"ex\"><div class=\"exh\">Book Example 5 · Subtract 3x<sup>2</sup> + 4x<sup>2</sup>y − 5xy<sup>2</sup> − y<sup>2</sup> from 7x<sup>2</sup> + 4x<sup>2</sup>y − 7xy<sup>2</sup> − 5y<sup>2</sup></div><div class=\"exl\">Change signs: −3x<sup>2</sup> − 4x<sup>2</sup>y + 5xy<sup>2</sup> + y<sup>2</sup>.<br>Add: 4x<sup>2</sup> + 0x<sup>2</sup>y − 2xy<sup>2</sup> − 4y<sup>2</sup> = <b>4x<sup>2</sup> − 2xy<sup>2</sup> − 4y<sup>2</sup></b>.</div></div><div class=\"keybox\"><b>“Subtract A from B”</b> means B − A. “How much smaller is A than B?” and “What must be taken away from B to get A?” also mean B − A.</div><div class=\"hub-btns\" style=\"margin-top:12px\"><button class=\"hub-btn primary\" data-go=\"s2\">Practise 7.2 →</button></div></section><section class=\"note\" id=\"n73\"><h2>7.3 Multiplication of polynomials</h2><p class=\"lt\"><b>Objective:</b> Multiply a monomial, binomial or trinomial by another monomial, binomial or trinomial.</p><p>Multiply the coefficients and add the powers of the same variable (x<sup>m</sup> × x<sup>n</sup> = x<sup>m+n</sup>): 3xy × 4x<sup>2</sup>y = 12x<sup>3</sup>y<sup>2</sup> and 8x<sup>3</sup>y<sup>5</sup> × 4x<sup>4</sup>y<sup>3</sup> = 32x<sup>7</sup>y<sup>8</sup>.</p><p>To multiply a polynomial by a monomial, multiply <b>each term</b>: 3x(3x + y) = 9x<sup>2</sup> + 3xy. To multiply two polynomials, multiply every term of one by every term of the other, then collect like terms.</p><div class=\"ex\"><div class=\"exh\">Book Example 11 · (2x + 3y)(5x − y)</div><div class=\"exl\">= 2x(5x − y) + 3y(5x − y) = 10x<sup>2</sup> − 2xy + 15xy − 3y<sup>2</sup><br>= <b>10x<sup>2</sup> + 13xy − 3y<sup>2</sup></b>.</div></div><div class=\"ex\"><div class=\"exh\">Book Example 14 · (x<sup>2</sup> − 5x + 3)(5x<sup>2</sup> + 3x − 4)</div><div class=\"exl\">× 5x<sup>2</sup>: 5x<sup>4</sup> − 25x<sup>3</sup> + 15x<sup>2</sup>;  × 3x: 3x<sup>3</sup> − 15x<sup>2</sup> + 9x;  × (−4): −4x<sup>2</sup> + 20x − 12.<br>Add: <b>5x<sup>4</sup> − 22x<sup>3</sup> − 4x<sup>2</sup> + 29x − 12</b>.</div></div><div class=\"keybox\"><b>Signs:</b> (+)(+) and (−)(−) give +; (+)(−) gives −. Check the number of products: a binomial × trinomial has 2 × 3 = 6 products before collecting.</div><div class=\"hub-btns\" style=\"margin-top:12px\"><button class=\"hub-btn primary\" data-go=\"s3\">Practise 7.3 →</button></div></section><section class=\"note\" id=\"n74\"><h2>7.4 Division by a monomial</h2><p class=\"lt\"><b>Objective:</b> Divide a monomial or a polynomial by a monomial using the laws of exponents.</p><p>Division is the opposite of multiplication. Divide the coefficients and subtract the powers: a<sup>6</sup> ÷ a<sup>3</sup> = a<sup>6−3</sup> = a<sup>3</sup>, 10x<sup>7</sup> ÷ 2x<sup>4</sup> = 5x<sup>3</sup>, x<sup>4</sup> ÷ x<sup>4</sup> = x<sup>0</sup> = 1.</p><div class=\"ex\"><div class=\"exh\">Book Example 18</div><div class=\"exl\">a) <span class=\"fq\"><span>−100a<sup>3</sup></span><span>20a</span></span> = −5a<sup>2</sup>.<br>b) <span class=\"fq\"><span>−35x<sup>5</sup>y<sup>2</sup></span><span>−7x<sup>3</sup>y</span></span> = +5x<sup>2</sup>y (the two negative signs give +).</div></div><h4>Polynomial ÷ monomial</h4><p>Split the polynomial into its terms, divide each term by the monomial and add the quotients: (px + py + pz) ÷ p = x + y + z.</p><div class=\"ex\"><div class=\"exh\">Book Example 19 · (32x<sup>4</sup>y<sup>3</sup> − 16x<sup>3</sup>y<sup>4</sup>) ÷ (−8x<sup>2</sup>y)</div><div class=\"exl\">32x<sup>4</sup>y<sup>3</sup> ÷ (−8x<sup>2</sup>y) = −4x<sup>2</sup>y<sup>2</sup>.<br>−16x<sup>3</sup>y<sup>4</sup> ÷ (−8x<sup>2</sup>y) = +2xy<sup>3</sup>.<br>Quotient = <b>−4x<sup>2</sup>y<sup>2</sup> + 2xy<sup>3</sup></b>.</div></div><div class=\"keybox\"><b>Careful:</b> a ÷ a = 1, not 0; and a<sup>2</sup> ÷ a = a. Every term must be divided, not just the first one.</div><div class=\"hub-btns\" style=\"margin-top:12px\"><button class=\"hub-btn primary\" data-go=\"s4\">Practise 7.4 →</button></div></section><section class=\"note\" id=\"n75\"><h2>7.5 Division by a polynomial</h2><p class=\"lt\"><b>Objective:</b> Divide a polynomial by a binomial using long division and find the quotient and remainder.</p><p>Arrange the dividend and the divisor in descending powers (leave a gap, or write 0, for a missing power). Then repeat: divide the first term of what is left by the first term of the divisor, write this in the quotient, multiply the divisor by it and subtract. Stop when the degree of what is left is less than the degree of the divisor: that is the remainder.</p><div class=\"ex\"><div class=\"exh\">Book Example 22 · (−5 − 7a + 6a<sup>2</sup>) ÷ (2a + 1)</div><div class=\"exl\">Rearrange: 6a<sup>2</sup> − 7a − 5.<br>6a<sup>2</sup> ÷ 2a = 3a; 3a(2a + 1) = 6a<sup>2</sup> + 3a; subtract → −10a − 5.<br>−10a ÷ 2a = −5; −5(2a + 1) = −10a − 5; subtract → 0.<br>Quotient <b>3a − 5</b>, remainder 0. Check: (2a + 1)(3a − 5) = 6a<sup>2</sup> − 7a − 5.</div></div><div class=\"ex\"><div class=\"exh\">Book Example 23 · (5y<sup>3</sup> + y − 3) ÷ (y − 1)</div><div class=\"exl\">Write 5y<sup>3</sup> + 0y<sup>2</sup> + y − 3.<br>Quotient <b>5y<sup>2</sup> + 5y + 6</b>, remainder <b>3</b>.</div></div><div class=\"keybox\"><b>Check:</b> divisor × quotient + remainder = dividend. For Example 26: (2x − 5y)(7x + 3y) + (−3y<sup>2</sup>) = 14x<sup>2</sup> − 29xy − 18y<sup>2</sup>.</div><div class=\"hub-btns\" style=\"margin-top:12px\"><button class=\"hub-btn primary\" data-go=\"s5\">Practise 7.5 →</button></div></section><section class=\"note\" id=\"n76\"><h2>7.6 Algebraic identities</h2><p class=\"lt\"><b>Objective:</b> Use the four standard identities, and their area models, to expand products and to multiply numbers quickly.</p><p>3x + 5 = 20 is true only when x = 5 (a conditional equation). 5x + 3x = 8x is true for every x: an equation that is true for all values of its variables is an <b>identity</b>.</p><div class=\"tscroll\"><table class=\"ttab\"><tr><th>Identity</th><th>Statement</th></tr><tr><td>1</td><td>(x + a)(x + b) = x<sup>2</sup> + (a + b)x + ab</td></tr><tr><td>2</td><td>(a + b)<sup>2</sup> = a<sup>2</sup> + 2ab + b<sup>2</sup></td></tr><tr><td>3</td><td>(a − b)<sup>2</sup> = a<sup>2</sup> − 2ab + b<sup>2</sup></td></tr><tr><td>4</td><td>(a + b)(a − b) = a<sup>2</sup> − b<sup>2</sup></td></tr></table></div><p><b>Area models.</b> A product of two factors is the area of a rectangle with those sides. The rectangle with sides (x + a) and (x + b) splits into x<sup>2</sup>, ax, bx and ab, so (x + a)(x + b) = x<sup>2</sup> + (a + b)x + ab. The square of side (a + b) splits into a<sup>2</sup>, two rectangles ab and b<sup>2</sup>.</p><svg class=\"figsvg\" viewBox=\"0 0 286 216\" role=\"img\"><defs><marker id=\"ah\" viewBox=\"0 0 10 10\" refX=\"9\" refY=\"5\" markerWidth=\"7\" markerHeight=\"7\" orient=\"auto\"><path d=\"M0,1 L10,5 L0,9 z\" class=\"ahd\"/></marker><marker id=\"ahs\" viewBox=\"0 0 10 10\" refX=\"1\" refY=\"5\" markerWidth=\"7\" markerHeight=\"7\" orient=\"auto\"><path d=\"M10,1 L0,5 L10,9 z\" class=\"ahd\"/></marker></defs><text class=\"lb\" x=\"156.0\" y=\"10.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">Fig. 7.2 · sides (x + a) and (x + b)</text><rect class=\"sh3\" x=\"46\" y=\"40\" width=\"220\" height=\"160\"/><text class=\"al\" x=\"121.0\" y=\"30.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">x</text><text class=\"al\" x=\"231.0\" y=\"30.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">a</text><line class=\"ln\" x1=\"196.0\" y1=\"40.0\" x2=\"196.0\" y2=\"200.0\"/><text class=\"al\" x=\"30.0\" y=\"95.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">x</text><text class=\"al\" x=\"30.0\" y=\"175.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">b</text><line class=\"ln\" x1=\"46.0\" y1=\"150.0\" x2=\"266.0\" y2=\"150.0\"/><text class=\"lb\" x=\"121.0\" y=\"95.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">x²</text><text class=\"lb\" x=\"231.0\" y=\"95.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">ax</text><text class=\"lb\" x=\"121.0\" y=\"175.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">bx</text><text class=\"lb\" x=\"231.0\" y=\"175.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">ab</text></svg><svg class=\"figsvg\" viewBox=\"0 0 276 266\" role=\"img\"><defs><marker id=\"ah\" viewBox=\"0 0 10 10\" refX=\"9\" refY=\"5\" markerWidth=\"7\" markerHeight=\"7\" orient=\"auto\"><path d=\"M0,1 L10,5 L0,9 z\" class=\"ahd\"/></marker><marker id=\"ahs\" viewBox=\"0 0 10 10\" refX=\"1\" refY=\"5\" markerWidth=\"7\" markerHeight=\"7\" orient=\"auto\"><path d=\"M10,1 L0,5 L10,9 z\" class=\"ahd\"/></marker></defs><text class=\"lb\" x=\"151.0\" y=\"10.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">Fig. 7.3 · square of side (a + b)</text><rect class=\"sh3\" x=\"46\" y=\"40\" width=\"210\" height=\"210\"/><text class=\"al\" x=\"116.0\" y=\"30.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">a</text><text class=\"al\" x=\"221.0\" y=\"30.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">b</text><line class=\"ln\" x1=\"186.0\" y1=\"40.0\" x2=\"186.0\" y2=\"250.0\"/><text class=\"al\" x=\"30.0\" y=\"110.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">a</text><text class=\"al\" x=\"30.0\" y=\"215.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">b</text><line class=\"ln\" x1=\"46.0\" y1=\"180.0\" x2=\"256.0\" y2=\"180.0\"/><text class=\"lb\" x=\"116.0\" y=\"110.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">a²</text><text class=\"lb\" x=\"221.0\" y=\"110.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">ab</text><text class=\"lb\" x=\"116.0\" y=\"215.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">ab</text><text class=\"lb\" x=\"221.0\" y=\"215.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">b²</text></svg><p>For (a + b)(a − b) (Fig. 7.5): start with a square of side a (area a<sup>2</sup>). Remove the strip of width b on the right (area ab) and add a strip of height b and length (a − b) at the bottom (area b(a − b) = ab − b<sup>2</sup>). The result is a rectangle with sides (a − b) and (a + b), so (a + b)(a − b) = a<sup>2</sup> − ab + ab − b<sup>2</sup> = a<sup>2</sup> − b<sup>2</sup>.</p><svg class=\"figsvg\" viewBox=\"0 0 276 266\" role=\"img\"><defs><marker id=\"ah\" viewBox=\"0 0 10 10\" refX=\"9\" refY=\"5\" markerWidth=\"7\" markerHeight=\"7\" orient=\"auto\"><path d=\"M0,1 L10,5 L0,9 z\" class=\"ahd\"/></marker><marker id=\"ahs\" viewBox=\"0 0 10 10\" refX=\"1\" refY=\"5\" markerWidth=\"7\" markerHeight=\"7\" orient=\"auto\"><path d=\"M10,1 L0,5 L10,9 z\" class=\"ahd\"/></marker></defs><text class=\"lb\" x=\"151.0\" y=\"10.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">Fig. 7.5 · (a + b)(a − b)</text><rect class=\"sh3\" x=\"46\" y=\"40\" width=\"210\" height=\"210\"/><text class=\"al\" x=\"116.0\" y=\"30.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">a − b</text><text class=\"al\" x=\"221.0\" y=\"30.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">b</text><line class=\"ln\" x1=\"186.0\" y1=\"40.0\" x2=\"186.0\" y2=\"250.0\"/><text class=\"al\" x=\"30.0\" y=\"115.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">a</text><text class=\"al\" x=\"30.0\" y=\"220.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">b</text><line class=\"ln\" x1=\"46.0\" y1=\"190.0\" x2=\"256.0\" y2=\"190.0\"/><text class=\"lb\" x=\"221.0\" y=\"115.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">ab</text><text class=\"lb\" x=\"116.0\" y=\"220.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">b(a − b)</text><text class=\"lb\" x=\"221.0\" y=\"220.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">b²</text></svg><div class=\"ex\"><div class=\"exh\">Book Examples 27–30 · Using the identities</div><div class=\"exl\">(x + 3)(x + 5) = x<sup>2</sup> + 8x + 15;  (x − 3)(x + 8) = x<sup>2</sup> + 5x − 24.<br>(103)<sup>2</sup> = (100 + 3)<sup>2</sup> = 10000 + 600 + 9 = 10609.<br>(96)<sup>2</sup> = (100 − 4)<sup>2</sup> = 10000 − 800 + 16 = 9216.<br>97 × 103 = (100 − 3)(100 + 3) = 10000 − 9 = 9991.</div></div><div class=\"keybox\"><b>Common mistake:</b> (a + b)<sup>2</sup> is <b>not</b> a<sup>2</sup> + b<sup>2</sup>; the middle term 2ab must not be forgotten. Likewise (a − b)<sup>2</sup> ≠ a<sup>2</sup> − b<sup>2</sup>.</div><div class=\"hub-btns\" style=\"margin-top:12px\"><button class=\"hub-btn primary\" data-go=\"s6\">Practise 7.6 →</button></div></section><section class=\"note\" id=\"nsum\"><h2>Chapter checklist</h2><ul><li>Identify terms, coefficients and like terms; classify monomials, binomials, trinomials and polynomials; find the degree of a polynomial.</li><li>Add and subtract polynomials by collecting like terms, and solve problems that need addition or subtraction of polynomials.</li><li>Multiply a monomial, binomial or trinomial by another monomial, binomial or trinomial.</li><li>Divide a monomial or a polynomial by a monomial using the laws of exponents.</li><li>Divide a polynomial by a binomial using long division and find the quotient and remainder.</li><li>Use the four standard identities, and their area models, to expand products and to multiply numbers quickly.</li></ul><div class=\"hub-btns\" style=\"margin-top:10px\"><button class=\"hub-btn\" data-go=\"s7\">Assessment A</button><button class=\"hub-btn\" data-go=\"s8\">Assessment B</button><button class=\"hub-btn\" data-go=\"s9\">Assessment C</button><button class=\"hub-btn\" data-go=\"s10\">Assessment D</button><button class=\"hub-btn primary\" data-go=\"report\">📊 Report</button></div></section>";
var REPORT = [["s7", "A", "Knowing and understanding"], ["s8", "B", "Investigating patterns"], ["s9", "C", "Communicating"], ["s10", "D", "Applying mathematics in real-life contexts"]];
var SECTIONS = [{"id": "s1", "label": "7.1 Polynomials", "sub": "Terms, like terms, polynomials and degree", "slides": [{"kind": "blank", "p": "<b>Looking Back · Q1</b> · Write the number of terms in each of the following expressions.", "tag": "", "marks": "", "flat": [{"t": "a) 2x → __B1__", "a": {"B1": "1"}}, {"t": "b) 3p + 5q → __B1__", "a": {"B1": "2"}}, {"t": "c) a<sup>2</sup> + 5a + 4 → __B1__", "a": {"B1": "3"}}, {"t": "d) 4p − 3m → __B1__", "a": {"B1": "2"}}, {"t": "e) 7a + 3b → __B1__", "a": {"B1": "2"}}, {"t": "f) xyz → __B1__", "a": {"B1": "1"}}], "sol": "2x is a single product: 1 term.\n3p and 5q: 2 terms.\na<sup>2</sup>, 5a and 4: 3 terms.\n4p and −3m: 2 terms.\n7a and 3b: 2 terms.\nxyz = x × y × z is one product: 1 term."}, {"kind": "mcq", "text": "<b>Looking Back · Q2</b> · State which of the following are not polynomials.  a) a<sup>2</sup> + b<sup>2</sup>   b) x<sup>2</sup>/y<sup>2</sup> − y<sup>2</sup>/x<sup>2</sup>   c) 2ax + 5by − 7cz   d) ax − by − 3   e) 3pq<sup>2</sup> − 4xy + 2zy", "opts": ["None of them", "b only", "b and e", "a and b"], "correct": 1, "tag": "", "sol": "In b), x<sup>2</sup>/y<sup>2</sup> = x<sup>2</sup>y<sup>−2</sup> and y<sup>2</sup>/x<sup>2</sup> = y<sup>2</sup>x<sup>−2</sup> have negative powers, so b) is not a polynomial. All the other expressions have only non-negative integer powers."}, {"kind": "blank", "p": "<b>Looking Back · Q3</b> · From each expression, list the terms with variables and the terms that are only constants.", "tag": "", "marks": "", "flat": [{"t": "a) 9a<sup>2</sup>b<sup>3</sup> − 2ab<sup>2</sup> + 45: number of terms with variables = __B1__", "a": {"B1": "2"}}, {"t": "constant term = __B1__", "a": {"B1": "45"}}, {"t": "b) 35xy<sup>2</sup> + 4x + 5y − 25: number of terms with variables = __B1__", "a": {"B1": "3"}}, {"t": "constant term = __B1__", "a": {"B1": "-25"}}], "sol": "Terms with variables: 9a<sup>2</sup>b<sup>3</sup> and −2ab<sup>2</sup>.\nThe constant term is 45.\nTerms with variables: 35xy<sup>2</sup>, 4x and 5y.\nThe constant term is −25."}, {"kind": "mcq", "text": "<b>Looking Back · Q4</b> · Classify as monomials, binomials or trinomials:  a) 2x + 1   b) y + 4y   c) 3x<sup>2</sup> + 5xy + y<sup>2</sup>   d) 7a + 2b − 1   e) 7abc", "opts": ["a) binomial  b) monomial  c) trinomial  d) binomial  e) monomial", "a) binomial  b) monomial  c) binomial  d) trinomial  e) monomial", "a) monomial  b) monomial  c) trinomial  d) trinomial  e) trinomial", "a) binomial  b) monomial  c) trinomial  d) trinomial  e) monomial"], "correct": 3, "tag": "", "sol": "a) 2 terms: binomial. b) y and 4y are like terms, y + 4y = 5y: one term, a monomial. c) and d) 3 terms each: trinomials. e) 7abc is one product: monomial."}, {"kind": "mcq", "text": "<b>Looking Back · Q5</b> · Are 2ab<sup>2</sup> and 5b<sup>2</sup>a like terms?", "opts": ["Yes: both have a to the power 1 and b to the power 2", "No: the variables are written in a different order", "Yes: all terms containing a and b are like terms", "No: the coefficients 2 and 5 are different"], "correct": 0, "tag": "", "sol": "b<sup>2</sup>a = ab<sup>2</sup>, so both terms have the same variables with the same powers. The order of the variables and the coefficients do not matter."}, {"kind": "blank", "p": "<b>Example 1</b> · State which of these are polynomials:  a) x<sup>2</sup> + 1   b) {x/y} + 3   c) x<sup>2</sup> + y<sup>−2</sup>   d) x<sup>2</sup> + x + 1   e) √x   f) 5   g) x + y + z   h) x<sup>3</sup>   i) {2/3}x<sup>3</sup> − y<sup>3</sup>   j) x + y<sup>−2</sup> + 1. (Type letters separated by commas.)", "tag": "", "marks": "", "flat": [{"t": "Monomials: __B1__", "a": {"B1": "f,h"}, "expr": "glist"}, {"t": "Binomials: __B1__", "a": {"B1": "a,i"}, "expr": "glist"}, {"t": "Trinomials: __B1__", "a": {"B1": "d,g"}, "expr": "glist"}, {"t": "Not polynomials: __B1__", "a": {"B1": "b,c,e,j"}, "expr": "glist"}], "sol": "f) 5 and h) x<sup>3</sup> have one term.\na) and i) have two terms with whole-number powers.\nd) and g) have three terms.\nb) {x/y} = xy<sup>−1</sup> and c), j) contain y<sup>−2</sup> (negative powers); e) √x = x<sup>1/2</sup> (fractional power)."}, {"kind": "mcq", "text": "<b>Example 1</b> · Why is j) x + y<sup>−2</sup> + 1 not a trinomial, although it has three terms?", "opts": ["The power of y is −2, which is negative", "It has two different variables", "It contains a constant term", "Its degree is more than 2"], "correct": 0, "tag": "", "sol": "A trinomial must have non-negative integer powers for every variable. In y<sup>−2</sup> the power is −2, so the expression is not a polynomial at all."}, {"kind": "blank", "p": "<b>Example 2</b> · Find the degree of each polynomial.", "tag": "", "marks": "", "flat": [{"t": "a) 7y<sup>2</sup> + √8 y + 9 → __B1__", "a": {"B1": "2"}}, {"t": "b) 21z<sup>4</sup> + z<sup>3</sup> + 2z<sup>2</sup> + 3 → __B1__", "a": {"B1": "4"}}, {"t": "c) 9x<sup>5</sup>y<sup>6</sup> + 4x<sup>2</sup>y<sup>3</sup> − 17xy → __B1__", "a": {"B1": "11"}}, {"t": "d) 11a<sup>2</sup>b<sup>7</sup> + 5a<sup>4</sup>b<sup>6</sup> − 5a<sup>2</sup>b<sup>4</sup> + 4ab − 25 → __B1__", "a": {"B1": "10"}}], "sol": "Highest power of y is 2 (√8 is only a constant).\nHighest power of z is 4.\nSums of powers: 11, 5, 2 → degree 11.\nSums of powers: 9, 10, 6, 2, 0 → degree 10."}, {"kind": "blank", "p": "<b>Ex 7A · Q1</b> · Which of the following are polynomials?  a) x<sup>2</sup> + 7x + 12   b) x<sup>2/3</sup> + x<sup>3</sup>   c) y<sup>3</sup>   d) 5   e) 4x<sup>−3</sup> − x<sup>2</sup> + x + 3   f) 4x − y<sup>−1</sup>   g) 7x<sup>2</sup>y<sup>1/2</sup> − 5xy   h) x<sup>2</sup> + 4x<sup>3</sup> − x + 1   i) {5/x} + x + 3   j) x<sup>2</sup>y<sup>2</sup> + y<sup>2</sup>z<sup>2</sup> + z<sup>2</sup>x<sup>2</sup>   k) 3x<sup>2</sup> − {1/y}   l) x<sup>2/3</sup>y − 4x<sup>3</sup>y<sup>2/3</sup>   m) x<sup>2</sup> + ∛x − 9   n) 2√x + 3   o) x<sup>2</sup> + 2/√x + 1", "tag": "", "marks": "", "flat": [{"t": "Polynomials (letters separated by commas): __B1__", "a": {"B1": "a,c,d,h,j"}, "expr": "glist"}], "sol": "a), c), d), h) and j) have only non-negative integer powers. b), g), l), m), n), o) have fractional powers (x<sup>2/3</sup>, y<sup>1/2</sup>, ∛x = x<sup>1/3</sup>, √x = x<sup>1/2</sup>); e), f), i), k) have negative powers (x<sup>−3</sup>, y<sup>−1</sup>, 5x<sup>−1</sup>, y<sup>−1</sup>)."}, {"kind": "mcq", "text": "<b>Ex 7A · Q2(b)</b> · Which of the expressions in Question 1 are binomials?", "opts": ["b, f, g and k", "b and n only", "f and k only", "None of them"], "correct": 3, "tag": "", "sol": "A binomial must be a polynomial with two terms. The two-term expressions b), f), g), k), n) all have a negative or fractional power, so none of the expressions in Question 1 is a binomial."}, {"kind": "blank", "p": "<b>Ex 7A · Q2(a, c–e)</b> · State which of the expressions in Question 1 are the following. (Type letters separated by commas.)", "tag": "", "marks": "", "flat": [{"t": "a) monomials: __B1__", "a": {"B1": "c,d"}, "expr": "glist"}, {"t": "c) trinomials: __B1__", "a": {"B1": "a,j"}, "expr": "glist"}, {"t": "d) polynomials: __B1__", "a": {"B1": "a,c,d,h,j"}, "expr": "glist"}, {"t": "e) not polynomials: __B1__", "a": {"B1": "b,e,f,g,i,k,l,m,n,o"}, "expr": "glist"}], "sol": "c) y<sup>3</sup> and d) 5 have one term.\na) x<sup>2</sup> + 7x + 12 and j) x<sup>2</sup>y<sup>2</sup> + y<sup>2</sup>z<sup>2</sup> + z<sup>2</sup>x<sup>2</sup> have three terms. (h) has four terms, so it is a polynomial but not a trinomial.)\nFrom Question 1: a, c, d, h, j.\nAll the others have a negative or fractional power."}, {"kind": "blank", "p": "<b>Ex 7A · Q3(a–e)</b> · State the degrees of the following polynomials.", "tag": "", "marks": "", "flat": [{"t": "a) 3x → __B1__", "a": {"B1": "1"}}, {"t": "b) 5x<sup>2</sup> + 3x + 4 → __B1__", "a": {"B1": "2"}}, {"t": "c) 3x + 5y → __B1__", "a": {"B1": "1"}}, {"t": "d) 5xy + 3 → __B1__", "a": {"B1": "2"}}, {"t": "e) 7x<sup>3</sup> + 8x<sup>2</sup>y − 9xy<sup>2</sup> → __B1__", "a": {"B1": "3"}}], "sol": "Power of x is 1.\nHighest power 2.\nEach term has degree 1.\nxy has degree 1 + 1 = 2.\nEach term has degree 3."}, {"kind": "mcq", "text": "<b>Ex 7A · Q3(f–j)</b> · State the degrees of the polynomials:  f) {3/5}x<sup>4</sup> + xy   g) x<sup>6</sup> + x<sup>4</sup>y<sup>2</sup> + xy<sup>4</sup> + y<sup>3</sup>   h) 8a<sup>3</sup> + 3ab − 6a<sup>4</sup>b + 4b   i) 3x<sup>3</sup> + x<sup>2</sup>y + y<sup>3</sup>   j) 4x<sup>6</sup> − 4x<sup>4</sup> − 2x<sup>2</sup> + 3", "opts": ["f) 5  g) 6  h) 5  i) 3  j) 6", "f) 4  g) 6  h) 5  i) 3  j) 6", "f) 4  g) 6  h) 4  i) 3  j) 6", "f) 4  g) 5  h) 5  i) 3  j) 6"], "correct": 1, "tag": "", "sol": "f) degrees 4 and 2 → 4. g) 6, 6, 5, 3 → 6. h) 3, 2, 4 + 1 = 5, 1 → 5 (add the powers of a and b in −6a<sup>4</sup>b). i) every term has degree 3. j) highest power 6."}, {"kind": "mcq", "text": "<b>Ex 7A · Q4(a)</b> · Arrange the terms of 6x<sup>2</sup> + 4x<sup>3</sup> − 7x<sup>4</sup> + 3x + 4 in descending order of their degrees.", "opts": ["4 + 3x + 6x<sup>2</sup> + 4x<sup>3</sup> − 7x<sup>4</sup>", "−7x<sup>4</sup> + 4x<sup>3</sup> + 6x<sup>2</sup> + 3x + 4", "4x<sup>3</sup> − 7x<sup>4</sup> + 6x<sup>2</sup> + 3x + 4", "7x<sup>4</sup> + 4x<sup>3</sup> + 6x<sup>2</sup> + 3x + 4"], "correct": 1, "tag": "", "sol": "Start with the highest power, x<sup>4</sup>, and keep each term's sign: −7x<sup>4</sup> + 4x<sup>3</sup> + 6x<sup>2</sup> + 3x + 4."}, {"kind": "blank", "p": "<b>Ex 7A · Q4(b–e)</b> · Arrange the terms in descending order of their degrees. Type the coefficients in that order, separated by commas (use 0 for a missing power).", "tag": "", "marks": "", "flat": [{"t": "b) 7x + 8x<sup>4</sup> − 8x<sup>2</sup> + 4x<sup>5</sup> + x<sup>3</sup> + 5 → __B1__", "a": {"B1": "4, 8, 1, -8, 7, 5"}, "expr": "dlist"}, {"t": "c) 6 + 2x<sup>3</sup> − x<sup>2</sup> + 4x → __B1__", "a": {"B1": "2, -1, 4, 6"}, "expr": "dlist"}, {"t": "d) 6 + 4x − 5x<sup>2</sup> + x<sup>3</sup> → __B1__", "a": {"B1": "1, -5, 4, 6"}, "expr": "dlist"}, {"t": "e) 3x<sup>2</sup> + 4x + 5x<sup>3</sup> − 7 → __B1__", "a": {"B1": "5, 3, 4, -7"}, "expr": "dlist"}], "sol": "4x<sup>5</sup> + 8x<sup>4</sup> + x<sup>3</sup> − 8x<sup>2</sup> + 7x + 5.\n2x<sup>3</sup> − x<sup>2</sup> + 4x + 6.\nx<sup>3</sup> − 5x<sup>2</sup> + 4x + 6.\n5x<sup>3</sup> + 3x<sup>2</sup> + 4x − 7."}]}, {"id": "s2", "label": "7.2 Add & subtract", "sub": "Adding and subtracting polynomials", "slides": [{"kind": "blank", "p": "<b>Example 3</b> · Add 7x<sup>2</sup> − 4xy + 8y<sup>2</sup>, 3xy + 4x<sup>2</sup> + 3y<sup>2</sup> and −3x<sup>2</sup> + 6xy − 7y<sup>2</sup>.", "tag": "", "marks": "", "flat": [{"t": "Coefficient of x<sup>2</sup> in the sum = __B1__", "a": {"B1": "8"}}, {"t": "Sum = __B1__", "a": {"B1": "8x^2+5xy+4y^2"}, "expr": true}], "sol": "7 + 4 − 3 = 8.\nxy: −4 + 3 + 6 = 5; y<sup>2</sup>: 8 + 3 − 7 = 4. Sum = 8x<sup>2</sup> + 5xy + 4y<sup>2</sup>."}, {"kind": "mcq", "text": "<b>Example 4</b> · Add x<sup>3</sup> + 3x<sup>2</sup>y + 3xy<sup>2</sup> + y<sup>3</sup>, 2x<sup>2</sup>y + 2xy<sup>2</sup>, x<sup>2</sup> + 3x<sup>3</sup> + y<sup>2</sup> and −2y<sup>3</sup> − 3x<sup>2</sup>y + y<sup>2</sup>.", "opts": ["4x<sup>3</sup> + 2x<sup>2</sup>y + 5xy<sup>2</sup> − y<sup>3</sup> + x<sup>2</sup> + 2y<sup>2</sup>", "4x<sup>3</sup> + 2x<sup>2</sup>y + 5xy<sup>2</sup> + 3y<sup>3</sup> + x<sup>2</sup> + 2y<sup>2</sup>", "4x<sup>3</sup> + 8x<sup>2</sup>y + 5xy<sup>2</sup> − y<sup>3</sup> + x<sup>2</sup> + 2y<sup>2</sup>", "x<sup>3</sup> + 2x<sup>2</sup>y + 5xy<sup>2</sup> − y<sup>3</sup> + 4x<sup>2</sup> + 2y<sup>2</sup>"], "correct": 0, "tag": "", "sol": "Collect like terms: x<sup>3</sup>: 1 + 3 = 4; x<sup>2</sup>y: 3 + 2 − 3 = 2; xy<sup>2</sup>: 3 + 2 = 5; y<sup>3</sup>: 1 − 2 = −1; x<sup>2</sup>: 1; y<sup>2</sup>: 1 + 1 = 2."}, {"kind": "blank", "p": "<b>Example 5</b> · Subtract 3x<sup>2</sup> + 4x<sup>2</sup>y − 5xy<sup>2</sup> − y<sup>2</sup> from −5y<sup>2</sup> + 7x<sup>2</sup> + 4x<sup>2</sup>y − 7xy<sup>2</sup>.", "tag": "", "marks": "", "flat": [{"t": "Additive inverse of the polynomial being subtracted = __B1__", "a": {"B1": "-3x^2-4x^2y+5xy^2+y^2"}, "expr": true}, {"t": "Difference = __B1__", "a": {"B1": "4x^2-2xy^2-4y^2"}, "expr": true}], "sol": "Change the sign of every term: −3x<sup>2</sup> − 4x<sup>2</sup>y + 5xy<sup>2</sup> + y<sup>2</sup>.\n7x<sup>2</sup> − 3x<sup>2</sup> = 4x<sup>2</sup>; 4x<sup>2</sup>y − 4x<sup>2</sup>y = 0; −7xy<sup>2</sup> + 5xy<sup>2</sup> = −2xy<sup>2</sup>; −5y<sup>2</sup> + y<sup>2</sup> = −4y<sup>2</sup>."}, {"kind": "mcq", "text": "<b>Example 6</b> · Subtract 8x<sup>3</sup> + 4x<sup>2</sup> + 2x from 7x<sup>4</sup> + 4x<sup>3</sup> − 3x<sup>2</sup> + 2.", "opts": ["7x<sup>4</sup> + 12x<sup>3</sup> + x<sup>2</sup> + 2x + 2", "−7x<sup>4</sup> + 4x<sup>3</sup> + 7x<sup>2</sup> + 2x − 2", "7x<sup>4</sup> − 4x<sup>3</sup> − 7x<sup>2</sup> − 2x + 2", "7x<sup>4</sup> − 4x<sup>3</sup> + x<sup>2</sup> − 2x + 2"], "correct": 2, "tag": "", "sol": "7x<sup>4</sup> + (4 − 8)x<sup>3</sup> + (−3 − 4)x<sup>2</sup> − 2x + 2 = 7x<sup>4</sup> − 4x<sup>3</sup> − 7x<sup>2</sup> − 2x + 2."}, {"kind": "blank", "p": "<b>Try This · Q1</b> · Subtract.", "tag": "", "marks": "", "flat": [{"t": "a) a<sup>2</sup> + ab + c from 2a<sup>2</sup> + ab + 3c: __B1__", "a": {"B1": "a^2+2c"}, "expr": true}, {"t": "b) 2xy + 3y − 4z from xy + 5y + z: __B1__", "a": {"B1": "-xy+2y+5z"}, "expr": true}], "sol": "2a<sup>2</sup> − a<sup>2</sup> = a<sup>2</sup>; ab − ab = 0; 3c − c = 2c.\nxy − 2xy = −xy; 5y − 3y = 2y; z + 4z = 5z."}, {"kind": "mcq", "text": "<b>Try This · Q2</b> · Add:  a) x<sup>3</sup> + x + x<sup>2</sup> + 1, x + x<sup>3</sup> + 6, x<sup>2</sup> + x + 3   b) x<sup>2</sup>y<sup>3</sup> + xy<sup>2</sup>, 2xy<sup>2</sup> + xy", "opts": ["a) 2x<sup>3</sup> + x<sup>2</sup> + 3x + 10   b) x<sup>2</sup>y<sup>3</sup> + 3xy<sup>2</sup> + xy", "a) 2x<sup>3</sup> + 2x<sup>2</sup> + 3x + 10   b) x<sup>2</sup>y<sup>3</sup> + 3xy<sup>2</sup> + xy", "a) 2x<sup>3</sup> + 2x<sup>2</sup> + 2x + 10   b) 3x<sup>2</sup>y<sup>3</sup> + xy<sup>2</sup> + xy", "a) 2x<sup>3</sup> + 2x<sup>2</sup> + 3x + 10   b) x<sup>2</sup>y<sup>3</sup> + 3xy<sup>2</sup>"], "correct": 1, "tag": "", "sol": "a) x<sup>3</sup>: 1 + 1 = 2; x<sup>2</sup>: 1 + 1 = 2; x: 1 + 1 + 1 = 3; constants 1 + 6 + 3 = 10. b) xy<sup>2</sup> + 2xy<sup>2</sup> = 3xy<sup>2</sup>; x<sup>2</sup>y<sup>3</sup> and xy are unlike terms and stay as they are."}, {"kind": "blank", "p": "<b>Ex 7B · Q1(a–d)</b> · Add the following polynomials.", "tag": "", "marks": "", "flat": [{"t": "a) 4x<sup>2</sup> + 5x + 6; x<sup>2</sup> + 1; 5x<sup>3</sup> + 4x + 3 → __B1__", "a": {"B1": "5x^3+5x^2+9x+10"}, "expr": true}, {"t": "b) 4x + 3x<sup>2</sup> + 5x<sup>3</sup>; 4x<sup>2</sup> − 7x + 5; x<sup>3</sup> − 1 → __B1__", "a": {"B1": "6x^3+7x^2-3x+4"}, "expr": true}, {"t": "c) 3a + 2b; 6a + 9b → __B1__", "a": {"B1": "9a+11b"}, "expr": true}, {"t": "d) 5x<sup>2</sup> + 7x + 3; 12x<sup>2</sup> − 3x + 8; 6x<sup>2</sup> − 4x + 9 → __B1__", "a": {"B1": "23x^2+20"}, "expr": true}], "sol": "x<sup>3</sup>: 5; x<sup>2</sup>: 4 + 1 = 5; x: 5 + 4 = 9; constants 6 + 1 + 3 = 10.\nx<sup>3</sup>: 5 + 1 = 6; x<sup>2</sup>: 3 + 4 = 7; x: 4 − 7 = −3; constants 5 − 1 = 4.\n3a + 6a = 9a; 2b + 9b = 11b.\nx<sup>2</sup>: 5 + 12 + 6 = 23; x: 7 − 3 − 4 = 0; constants 3 + 8 + 9 = 20."}, {"kind": "mcq", "text": "<b>Ex 7B · Q1(e)</b> · Add x<sup>2</sup> − 6xy + y<sup>2</sup>; −x<sup>2</sup> − 6xy + y<sup>2</sup>; x<sup>2</sup> − 6xy − y<sup>2</sup>.", "opts": ["x<sup>2</sup> − 6xy + y<sup>2</sup>", "x<sup>2</sup> − 18xy + 3y<sup>2</sup>", "x<sup>2</sup> − 18xy + y<sup>2</sup>", "3x<sup>2</sup> − 18xy + y<sup>2</sup>"], "correct": 2, "tag": "", "sol": "x<sup>2</sup>: 1 − 1 + 1 = 1; xy: −6 − 6 − 6 = −18; y<sup>2</sup>: 1 + 1 − 1 = 1. Sum = x<sup>2</sup> − 18xy + y<sup>2</sup>."}, {"kind": "blank", "p": "<b>Ex 7B · Q1(f–h)</b> · Add the following polynomials.", "tag": "", "marks": "", "flat": [{"t": "f) 4x<sup>2</sup> − 7xy + 6y<sup>2</sup>; 4x<sup>2</sup> + 7xy − 6y<sup>2</sup> + 4xy − 8y<sup>2</sup> → __B1__", "a": {"B1": "8x^2+4xy-8y^2"}, "expr": true}, {"t": "g) 2 − x − x<sup>2</sup>; x<sup>2</sup> + x + 3; 4x<sup>2</sup> + 5x + 7 → __B1__", "a": {"B1": "4x^2+5x+12"}, "expr": true}, {"t": "h) x<sup>3</sup> + 2x<sup>4</sup> + 4x<sup>2</sup>; 4x<sup>4</sup> − 4x<sup>2</sup> + x<sup>8</sup>; x<sup>7</sup> + x<sup>5</sup> → __B1__", "a": {"B1": "x^8+x^7+x^5+6x^4+x^3"}, "expr": true}], "sol": "x<sup>2</sup>: 4 + 4 = 8; xy: −7 + 7 + 4 = 4; y<sup>2</sup>: 6 − 6 − 8 = −8.\nx<sup>2</sup>: −1 + 1 + 4 = 4; x: −1 + 1 + 5 = 5; constants 2 + 3 + 7 = 12.\nx<sup>4</sup>: 2 + 4 = 6; x<sup>2</sup>: 4 − 4 = 0. Sum = x<sup>8</sup> + x<sup>7</sup> + x<sup>5</sup> + 6x<sup>4</sup> + x<sup>3</sup>."}, {"kind": "blank", "p": "<b>Ex 7B · Q2</b> · The sides of a triangle are 3x<sup>2</sup> − y<sup>2</sup>; 4x<sup>2</sup> − 7xy + 4y<sup>2</sup> and −3x<sup>2</sup> + 7xy + 8y<sup>2</sup>. Find its perimeter.", "tag": "", "marks": "", "flat": [{"t": "Perimeter = __B1__", "a": {"B1": "4x^2+11y^2"}, "expr": true}], "sol": "Perimeter = sum of the sides. x<sup>2</sup>: 3 + 4 − 3 = 4; xy: −7 + 7 = 0; y<sup>2</sup>: −1 + 4 + 8 = 11. Perimeter = 4x<sup>2</sup> + 11y<sup>2</sup>."}, {"kind": "mcq", "text": "<b>Ex 7B · Q3</b> · The sides of a rectangle are x<sup>2</sup> + 3y<sup>2</sup> and x<sup>3</sup> − y<sup>2</sup>. Find its perimeter.", "opts": ["2x<sup>3</sup> + 2x<sup>2</sup> + 8y<sup>2</sup>", "2x<sup>3</sup> + 2x<sup>2</sup> + 4y<sup>2</sup>", "2x<sup>3</sup> + 2x<sup>2</sup> − 4y<sup>2</sup>", "x<sup>3</sup> + x<sup>2</sup> + 2y<sup>2</sup>"], "correct": 1, "tag": "", "sol": "Perimeter = 2(length + breadth) = 2(x<sup>3</sup> + x<sup>2</sup> + 2y<sup>2</sup>) = 2x<sup>3</sup> + 2x<sup>2</sup> + 4y<sup>2</sup>."}, {"kind": "blank", "p": "<b>Ex 7B · Q4</b> · Do the following subtractions (subtract the second line from the first).", "tag": "", "marks": "", "flat": [{"t": "a) (−3x − 4z) − (−9x − 7z) = __B1__", "a": {"B1": "6x+3z"}, "expr": true}, {"t": "b) (14r − 30s) − (16r + 12s) = __B1__", "a": {"B1": "-2r-42s"}, "expr": true}, {"t": "c) (m<sup>2</sup> − 9) − (3m<sup>2</sup> − 3 + 6m) = __B1__", "a": {"B1": "-2m^2-6m-6"}, "expr": true}, {"t": "d) (9a + 8b − 9c) − (3a − 4c) = __B1__", "a": {"B1": "6a+8b-5c"}, "expr": true}], "sol": "−3x + 9x = 6x; −4z + 7z = 3z.\n14r − 16r = −2r; −30s − 12s = −42s.\nm<sup>2</sup> − 3m<sup>2</sup> = −2m<sup>2</sup>; −6m; −9 + 3 = −6.\n9a − 3a = 6a; 8b; −9c + 4c = −5c."}, {"kind": "blank", "p": "<b>Ex 7B · Q5</b> · Subtract.", "tag": "", "marks": "", "flat": [{"t": "a) 3x + 4x<sup>2</sup> − 7 from x<sup>4</sup> + 3x<sup>2</sup> − 4x + 4: __B1__", "a": {"B1": "x^4-x^2-7x+11"}, "expr": true}, {"t": "b) 30 − 4x + 5x<sup>2</sup> from 7x<sup>2</sup> − 5x + 70: __B1__", "a": {"B1": "2x^2-x+40"}, "expr": true}], "sol": "x<sup>4</sup> + (3 − 4)x<sup>2</sup> + (−4 − 3)x + (4 + 7) = x<sup>4</sup> − x<sup>2</sup> − 7x + 11.\n(7 − 5)x<sup>2</sup> + (−5 + 4)x + (70 − 30) = 2x<sup>2</sup> − x + 40."}, {"kind": "mcq", "text": "<b>Ex 7B · Q6</b> · From 8x<sup>3</sup> − 7x + 8x<sup>2</sup> − 3, take away 7 + 8x<sup>2</sup> + 7x + x<sup>3</sup>.", "opts": ["7x<sup>3</sup> − 14x − 10", "7x<sup>3</sup> − 10", "7x<sup>3</sup> + 16x<sup>2</sup> − 14x − 10", "9x<sup>3</sup> − 14x + 4"], "correct": 0, "tag": "", "sol": "x<sup>3</sup>: 8 − 1 = 7; x<sup>2</sup>: 8 − 8 = 0; x: −7 − 7 = −14; constants −3 − 7 = −10."}, {"kind": "blank", "p": "<b>Ex 7B · Q7</b> · From 3x<sup>2</sup> − 4x<sup>3</sup> + 3x + 7, take away 1 − x + x<sup>2</sup> − x<sup>3</sup>.", "tag": "", "marks": "", "flat": [{"t": "Result = __B1__", "a": {"B1": "-3x^3+2x^2+4x+6"}, "expr": true}], "sol": "x<sup>3</sup>: −4 + 1 = −3; x<sup>2</sup>: 3 − 1 = 2; x: 3 + 1 = 4; constants 7 − 1 = 6. Result = −3x<sup>3</sup> + 2x<sup>2</sup> + 4x + 6."}, {"kind": "blank", "p": "<b>Ex 7B · Q8</b> · How much smaller is 2x<sup>3</sup> − 2x + 5 than 7 + 5x<sup>2</sup> + 3x?", "tag": "", "marks": "", "flat": [{"t": "Difference = __B1__", "a": {"B1": "-2x^3+5x^2+5x+2"}, "expr": true}], "sol": "Subtract the smaller one from the other: (7 + 5x<sup>2</sup> + 3x) − (2x<sup>3</sup> − 2x + 5) = −2x<sup>3</sup> + 5x<sup>2</sup> + 5x + 2."}, {"kind": "mcq", "text": "<b>Ex 7B · Q9</b> · How much larger is 8x<sup>2</sup> − 9y<sup>2</sup> than 3x<sup>2</sup> − 2y<sup>2</sup>?", "opts": ["5x<sup>2</sup> − 11y<sup>2</sup>", "11x<sup>2</sup> − 11y<sup>2</sup>", "5x<sup>2</sup> − 7y<sup>2</sup>", "−5x<sup>2</sup> + 7y<sup>2</sup>"], "correct": 2, "tag": "", "sol": "(8x<sup>2</sup> − 9y<sup>2</sup>) − (3x<sup>2</sup> − 2y<sup>2</sup>) = 5x<sup>2</sup> − 7y<sup>2</sup>."}, {"kind": "blank", "p": "<b>Ex 7B · Q10</b> · Leo bought a shirt for ₹ (5x + 20) and a belt for ₹ (2x − 10). How much did he spend?", "tag": "", "marks": "", "flat": [{"t": "Amount spent = ₹ __B1__", "a": {"B1": "7x+10"}, "expr": true}], "sol": "(5x + 20) + (2x − 10) = 7x + 10, so he spent ₹ (7x + 10)."}, {"kind": "blank", "p": "<b>Ex 7B · Q11</b> · Lakshmi bought bread for ₹ (7x + 9) and butter for ₹ (3x − 5). She gave a ₹ 100 note. How much will she get back?", "tag": "", "marks": "", "flat": [{"t": "Total cost = ₹ __B1__", "a": {"B1": "10x+4"}, "expr": true}, {"t": "Money returned = ₹ __B1__", "a": {"B1": "96-10x"}, "expr": true}], "sol": "(7x + 9) + (3x − 5) = 10x + 4.\n100 − (10x + 4) = 96 − 10x. She gets back ₹ (96 − 10x)."}, {"kind": "mcq", "text": "<b>Ex 7B · Q12</b> · What should be taken away from 3x<sup>2</sup> + 4x + 1 to get 2x<sup>2</sup> − 4x + 35?", "opts": ["x<sup>2</sup> − 8x + 36", "x<sup>2</sup> + 8x − 34", "−x<sup>2</sup> − 8x + 34", "5x<sup>2</sup> + 36"], "correct": 1, "tag": "", "sol": "Required = (3x<sup>2</sup> + 4x + 1) − (2x<sup>2</sup> − 4x + 35) = x<sup>2</sup> + 8x − 34."}]}, {"id": "s3", "label": "7.3 Multiplication", "sub": "Multiplying monomials, binomials and trinomials", "slides": [{"kind": "blank", "p": "<b>Example 7</b> · Multiply.", "tag": "", "marks": "", "flat": [{"t": "a) x × x = __B1__", "a": {"B1": "x^2"}, "expr": true}, {"t": "b) x<sup>2</sup> × x<sup>3</sup> = __B1__", "a": {"B1": "x^5"}, "expr": true}, {"t": "c) 3xy × 4x<sup>2</sup>y = __B1__", "a": {"B1": "12x^3y^2"}, "expr": true}, {"t": "d) 8x<sup>3</sup>y<sup>5</sup> × 4x<sup>4</sup>y<sup>3</sup> = __B1__", "a": {"B1": "32x^7y^8"}, "expr": true}], "sol": "x<sup>1+1</sup> = x<sup>2</sup>.\nx<sup>2+3</sup> = x<sup>5</sup>.\n3 × 4 = 12; x<sup>1+2</sup> = x<sup>3</sup>; y<sup>1+1</sup> = y<sup>2</sup>.\n8 × 4 = 32; x<sup>3+4</sup> = x<sup>7</sup>; y<sup>5+3</sup> = y<sup>8</sup>."}, {"kind": "mcq", "text": "<b>Example 8(a)</b> · Multiply 3x × (3x + y).", "opts": ["9x<sup>2</sup> + 3xy", "9x + 3xy", "6x + 3xy", "9x<sup>2</sup> + y"], "correct": 0, "tag": "", "sol": "Multiply each term by 3x: 3x × 3x = 9x<sup>2</sup> and 3x × y = 3xy."}, {"kind": "blank", "p": "<b>Example 8(b)</b> · Multiply (5x<sup>3</sup>y<sup>2</sup> + 4x<sup>2</sup>y<sup>3</sup>) × 3x<sup>2</sup>y<sup>2</sup>.", "tag": "", "marks": "", "flat": [{"t": "Product = __B1__", "a": {"B1": "15x^5y^4+12x^4y^5"}, "expr": true}], "sol": "5x<sup>3</sup>y<sup>2</sup> × 3x<sup>2</sup>y<sup>2</sup> = 15x<sup>5</sup>y<sup>4</sup> and 4x<sup>2</sup>y<sup>3</sup> × 3x<sup>2</sup>y<sup>2</sup> = 12x<sup>4</sup>y<sup>5</sup>."}, {"kind": "blank", "p": "<b>Example 9</b> · Multiply x<sup>3</sup> + 7x<sup>2</sup> − 4x + 3 by 2x<sup>2</sup>.", "tag": "", "marks": "", "flat": [{"t": "Product = __B1__", "a": {"B1": "2x^5+14x^4-8x^3+6x^2"}, "expr": true}], "sol": "Multiply each term by 2x<sup>2</sup>: 2x<sup>5</sup> + 14x<sup>4</sup> − 8x<sup>3</sup> + 6x<sup>2</sup>."}, {"kind": "mcq", "text": "<b>Example 10</b> · Multiply 2x<sup>2</sup>y − {4/3}xy<sup>2</sup> + {4/9}y<sup>3</sup> by ({−2/3}x<sup>2</sup>y).", "opts": ["(4/3)x<sup>4</sup>y<sup>2</sup> − (8/9)x<sup>3</sup>y<sup>3</sup> + (8/27)x<sup>2</sup>y<sup>4</sup>", "−(4/3)x<sup>4</sup>y<sup>2</sup> + (8/9)x<sup>3</sup>y<sup>3</sup> − (8/27)x<sup>2</sup>y<sup>4</sup>", "−(4/3)x<sup>4</sup>y<sup>2</sup> + (8/9)x<sup>3</sup>y<sup>3</sup> + (8/27)x<sup>2</sup>y<sup>4</sup>", "−(4/3)x<sup>4</sup>y<sup>2</sup> − (8/9)x<sup>3</sup>y<sup>3</sup> − (8/27)x<sup>2</sup>y<sup>4</sup>"], "correct": 1, "tag": "", "sol": "2x<sup>2</sup>y × ({−2/3}x<sup>2</sup>y) = {−4/3}x<sup>4</sup>y<sup>2</sup>; ({−4/3}xy<sup>2</sup>) × ({−2/3}x<sup>2</sup>y) = +{8/9}x<sup>3</sup>y<sup>3</sup>; {4/9}y<sup>3</sup> × ({−2/3}x<sup>2</sup>y) = {−8/27}x<sup>2</sup>y<sup>4</sup>."}, {"kind": "blank", "p": "<b>Example 11</b> · Multiply 2x + 3y by 5x − y.", "tag": "", "marks": "", "flat": [{"t": "Multiplying by −y gives __B1__", "a": {"B1": "-2xy-3y^2"}, "expr": true}, {"t": "Multiplying by 5x gives __B1__", "a": {"B1": "10x^2+15xy"}, "expr": true}, {"t": "Product = __B1__", "a": {"B1": "10x^2+13xy-3y^2"}, "expr": true}], "sol": "2x × (−y) = −2xy; 3y × (−y) = −3y<sup>2</sup>.\n2x × 5x = 10x<sup>2</sup>; 3y × 5x = 15xy.\nAdd: 10x<sup>2</sup> + (15 − 2)xy − 3y<sup>2</sup> = 10x<sup>2</sup> + 13xy − 3y<sup>2</sup> (−2xy and 15yx are like terms)."}, {"kind": "blank", "p": "<b>Example 12</b> · Multiply x<sup>2</sup> + 2xy − 3y by (x<sup>2</sup> − y<sup>2</sup>).", "tag": "", "marks": "", "flat": [{"t": "Product = __B1__", "a": {"B1": "x^4+2x^3y-3x^2y-x^2y^2-2xy^3+3y^3"}, "expr": true}], "sol": "× x<sup>2</sup>: x<sup>4</sup> + 2x<sup>3</sup>y − 3x<sup>2</sup>y; × (−y<sup>2</sup>): −x<sup>2</sup>y<sup>2</sup> − 2xy<sup>3</sup> + 3y<sup>3</sup>. There are no like terms, so the product is x<sup>4</sup> + 2x<sup>3</sup>y − 3x<sup>2</sup>y − x<sup>2</sup>y<sup>2</sup> − 2xy<sup>3</sup> + 3y<sup>3</sup>."}, {"kind": "mcq", "text": "<b>Example 13</b> · Multiply 4x<sup>2</sup> − 5xy + 3y<sup>2</sup> by (3x − 4y).", "opts": ["12x<sup>3</sup> − 15x<sup>2</sup>y + 29xy<sup>2</sup> + 12y<sup>3</sup>", "12x<sup>3</sup> + x<sup>2</sup>y − 11xy<sup>2</sup> − 12y<sup>3</sup>", "12x<sup>3</sup> − 31x<sup>2</sup>y + 9xy<sup>2</sup> − 12y<sup>3</sup>", "12x<sup>3</sup> − 31x<sup>2</sup>y + 29xy<sup>2</sup> − 12y<sup>3</sup>"], "correct": 3, "tag": "", "sol": "× 3x: 12x<sup>3</sup> − 15x<sup>2</sup>y + 9xy<sup>2</sup>; × (−4y): −16x<sup>2</sup>y + 20xy<sup>2</sup> − 12y<sup>3</sup>. Add: 12x<sup>3</sup> − 31x<sup>2</sup>y + 29xy<sup>2</sup> − 12y<sup>3</sup>."}, {"kind": "blank", "p": "<b>Example 14</b> · Multiply x<sup>2</sup> − 5x + 3 by (5x<sup>2</sup> + 3x − 4).", "tag": "", "marks": "", "flat": [{"t": "× 5x<sup>2</sup> gives __B1__", "a": {"B1": "5x^4-25x^3+15x^2"}, "expr": true}, {"t": "× 3x gives __B1__", "a": {"B1": "3x^3-15x^2+9x"}, "expr": true}, {"t": "× (−4) gives __B1__", "a": {"B1": "-4x^2+20x-12"}, "expr": true}, {"t": "Product = __B1__", "a": {"B1": "5x^4-22x^3-4x^2+29x-12"}, "expr": true}], "sol": "5x<sup>4</sup> − 25x<sup>3</sup> + 15x<sup>2</sup>.\n3x<sup>3</sup> − 15x<sup>2</sup> + 9x.\n−4x<sup>2</sup> + 20x − 12.\nx<sup>3</sup>: −25 + 3 = −22; x<sup>2</sup>: 15 − 15 − 4 = −4; x: 9 + 20 = 29: 5x<sup>4</sup> − 22x<sup>3</sup> − 4x<sup>2</sup> + 29x − 12."}, {"kind": "mcq", "text": "<b>Try This</b> · Find:  a) 15xy<sup>6</sup> × 2x<sup>2</sup>y   b) 15xy × (2x + 3y)", "opts": ["a) 30x<sup>2</sup>y<sup>6</sup>   b) 30x<sup>2</sup>y + 45xy<sup>2</sup>", "a) 30x<sup>3</sup>y<sup>7</sup>   b) 30x<sup>2</sup>y + 45xy<sup>2</sup>", "a) 17x<sup>3</sup>y<sup>7</sup>   b) 30xy + 45xy", "a) 30x<sup>3</sup>y<sup>7</sup>   b) 30x<sup>2</sup>y + 3y"], "correct": 1, "tag": "", "sol": "a) 15 × 2 = 30; x<sup>1+2</sup> = x<sup>3</sup>; y<sup>6+1</sup> = y<sup>7</sup>. b) 15xy × 2x = 30x<sup>2</sup>y and 15xy × 3y = 45xy<sup>2</sup>: multiply each term of the bracket."}, {"kind": "blank", "p": "<b>Ex 7C · Q1</b> · Perform the following multiplications.", "tag": "", "marks": "", "flat": [{"t": "a) x × x × x × x = __B1__", "a": {"B1": "x^4"}, "expr": true}, {"t": "b) (−x) × (−x) = __B1__", "a": {"B1": "x^2"}, "expr": true}, {"t": "c) 2ab × 2ab = __B1__", "a": {"B1": "4a^2b^2"}, "expr": true}, {"t": "d) 2a<sup>2</sup>b<sup>3</sup> × 4a<sup>3</sup>b<sup>2</sup> = __B1__", "a": {"B1": "8a^5b^5"}, "expr": true}], "sol": "Four factors of x: x<sup>4</sup>.\n(−) × (−) = +: x<sup>2</sup>.\n2 × 2 = 4: 4a<sup>2</sup>b<sup>2</sup>.\n2 × 4 = 8; a<sup>2+3</sup> = a<sup>5</sup>; b<sup>3+2</sup> = b<sup>5</sup>."}, {"kind": "mcq", "text": "<b>Ex 7C · Q2(g)</b> · Find the product ({1/3}x<sup>3</sup>y)({1/8}xy).", "opts": ["(1/24)x<sup>3</sup>y", "(1/24)x<sup>4</sup>y<sup>2</sup>", "(3/8)x<sup>4</sup>y<sup>2</sup>", "(1/11)x<sup>4</sup>y<sup>2</sup>"], "correct": 1, "tag": "", "sol": "{1/3} × {1/8} = {1/24}; x<sup>3+1</sup> = x<sup>4</sup>; y<sup>1+1</sup> = y<sup>2</sup>. Product = {1/24}x<sup>4</sup>y<sup>2</sup>."}, {"kind": "blank", "p": "<b>Ex 7C · Q2</b> · Find the product.", "tag": "", "marks": "", "flat": [{"t": "a) (3x<sup>2</sup>y) × (5x) = __B1__", "a": {"B1": "15x^3y"}, "expr": true}, {"t": "b) (√(3x))(√(3x)) = __B1__ x", "a": {"B1": "3"}}, {"t": "c) 5x<sup>2</sup>y(−4xy) = __B1__", "a": {"B1": "-20x^3y^2"}, "expr": true}, {"t": "d) (ab)(4a<sup>2</sup>b)(5ab<sup>2</sup>) = __B1__", "a": {"B1": "20a^4b^4"}, "expr": true}, {"t": "e) (ax<sup>2</sup>)(ay<sup>2</sup>)(axy) = __B1__", "a": {"B1": "a^3x^3y^3"}, "expr": true}, {"t": "f) (7xy<sup>10</sup>)(xy) = __B1__", "a": {"B1": "7x^2y^11"}, "expr": true}, {"t": "h) (a<sup>2</sup>b)(5ab<sup>2</sup>)(−3) = __B1__", "a": {"B1": "-15a^3b^3"}, "expr": true}], "sol": "15x<sup>3</sup>y.\n√(3x) × √(3x) = 3x.\n5 × (−4) = −20: −20x<sup>3</sup>y<sup>2</sup>.\n1 × 4 × 5 = 20; a<sup>1+2+1</sup> = a<sup>4</sup>; b<sup>1+1+2</sup> = b<sup>4</sup>.\na<sup>3</sup>x<sup>3</sup>y<sup>3</sup>.\n7x<sup>2</sup>y<sup>11</sup>.\n5 × (−3) = −15: −15a<sup>3</sup>b<sup>3</sup>."}, {"kind": "mcq", "text": "<b>Ex 7C · Q3(a–c)</b> · Find the product:  a) a(a − b)   b) 2(x + 3)   c) 5(x<sup>2</sup> − y<sup>2</sup>)", "opts": ["a) a<sup>2</sup> − ab   b) 2x + 3   c) 5x<sup>2</sup> − 5y<sup>2</sup>", "a) 2a − ab   b) 2x + 6   c) 5x<sup>2</sup> − 5y<sup>2</sup>", "a) a<sup>2</sup> − b   b) 2x + 6   c) 5x<sup>2</sup> − y<sup>2</sup>", "a) a<sup>2</sup> − ab   b) 2x + 6   c) 5x<sup>2</sup> − 5y<sup>2</sup>"], "correct": 3, "tag": "", "sol": "Multiply every term inside the bracket: a) a × a − a × b = a<sup>2</sup> − ab. b) 2 × x + 2 × 3 = 2x + 6. c) 5 × x<sup>2</sup> − 5 × y<sup>2</sup> = 5x<sup>2</sup> − 5y<sup>2</sup>."}, {"kind": "blank", "p": "<b>Ex 7C · Q3(d–f)</b> · Find the product.", "tag": "", "marks": "", "flat": [{"t": "d) 3x<sup>2</sup>y(4x + 5y) = __B1__", "a": {"B1": "12x^3y+15x^2y^2"}, "expr": true}, {"t": "e) 3ab(a<sup>2</sup>b − ab<sup>2</sup>) = __B1__", "a": {"B1": "3a^3b^2-3a^2b^3"}, "expr": true}, {"t": "f) 5a<sup>2</sup>b<sup>3</sup>(4a<sup>3</sup>b + 2ab<sup>3</sup>) = __B1__", "a": {"B1": "20a^5b^4+10a^3b^6"}, "expr": true}], "sol": "12x<sup>3</sup>y + 15x<sup>2</sup>y<sup>2</sup>.\n3a<sup>3</sup>b<sup>2</sup> − 3a<sup>2</sup>b<sup>3</sup>.\n5a<sup>2</sup>b<sup>3</sup> × 4a<sup>3</sup>b = 20a<sup>5</sup>b<sup>4</sup>; 5a<sup>2</sup>b<sup>3</sup> × 2ab<sup>3</sup> = 10a<sup>3</sup>b<sup>6</sup>."}, {"kind": "mcq", "text": "<b>Ex 7C · Q4(e)</b> · Multiply (2x<sup>2</sup>y − 3y)(3xy − x).", "opts": ["6x<sup>3</sup>y<sup>2</sup> + 2x<sup>3</sup>y − 9xy<sup>2</sup> + 3xy", "6x<sup>3</sup>y<sup>2</sup> − 2x<sup>3</sup>y − 9xy<sup>2</sup> + 3xy", "6x<sup>2</sup>y<sup>2</sup> − 2x<sup>3</sup>y − 9xy<sup>2</sup> + 3xy", "6x<sup>3</sup>y<sup>2</sup> − 2x<sup>3</sup>y − 9xy<sup>2</sup> − 3xy"], "correct": 1, "tag": "", "sol": "2x<sup>2</sup>y × 3xy = 6x<sup>3</sup>y<sup>2</sup>; 2x<sup>2</sup>y × (−x) = −2x<sup>3</sup>y; −3y × 3xy = −9xy<sup>2</sup>; −3y × (−x) = +3xy."}, {"kind": "blank", "p": "<b>Ex 7C · Q4</b> · Multiply.", "tag": "", "marks": "", "flat": [{"t": "a) (y + 2)(y − 4) = __B1__", "a": {"B1": "y^2-2y-8"}, "expr": true}, {"t": "b) (x − 7)(x − 6) = __B1__", "a": {"B1": "x^2-13x+42"}, "expr": true}, {"t": "c) (x<sup>2</sup> + 5)(x<sup>2</sup> + 10) = __B1__", "a": {"B1": "x^4+15x^2+50"}, "expr": true}, {"t": "d) (7x + 3y)(2x − 5y) = __B1__", "a": {"B1": "14x^2-29xy-15y^2"}, "expr": true}, {"t": "f) (x − y)(x − 2y) = __B1__", "a": {"B1": "x^2-3xy+2y^2"}, "expr": true}], "sol": "y<sup>2</sup> − 4y + 2y − 8 = y<sup>2</sup> − 2y − 8.\nx<sup>2</sup> − 6x − 7x + 42 = x<sup>2</sup> − 13x + 42.\nx<sup>4</sup> + 10x<sup>2</sup> + 5x<sup>2</sup> + 50 = x<sup>4</sup> + 15x<sup>2</sup> + 50.\n14x<sup>2</sup> − 35xy + 6xy − 15y<sup>2</sup> = 14x<sup>2</sup> − 29xy − 15y<sup>2</sup>.\nx<sup>2</sup> − 2xy − xy + 2y<sup>2</sup> = x<sup>2</sup> − 3xy + 2y<sup>2</sup>."}, {"kind": "blank", "p": "<b>Ex 7C · Q5(a–c)</b> · Find the product.", "tag": "", "marks": "", "flat": [{"t": "a) (5 − 2d − d<sup>2</sup>)(3 − 2d) = __B1__", "a": {"B1": "2d^3+d^2-16d+15"}, "expr": true}, {"t": "b) (a<sup>2</sup> + ab + b<sup>2</sup>)(a − b) = __B1__", "a": {"B1": "a^3-b^3"}, "expr": true}, {"t": "c) (x<sup>2</sup> + x + 1)(1 − x) = __B1__", "a": {"B1": "1-x^3"}, "expr": true}], "sol": "15 − 10d − 6d + 4d<sup>2</sup> − 3d<sup>2</sup> + 2d<sup>3</sup> = 2d<sup>3</sup> + d<sup>2</sup> − 16d + 15.\na<sup>3</sup> − a<sup>2</sup>b + a<sup>2</sup>b − ab<sup>2</sup> + ab<sup>2</sup> − b<sup>3</sup> = a<sup>3</sup> − b<sup>3</sup>.\nx<sup>2</sup> − x<sup>3</sup> + x − x<sup>2</sup> + 1 − x = 1 − x<sup>3</sup>."}, {"kind": "mcq", "text": "<b>Ex 7C · Q5(g)</b> · Find the product (3x + 4y + 5z)(4x + 3y + 4z).", "opts": ["12x<sup>2</sup> + 25xy + 31xz + 12y<sup>2</sup> + 32yz + 20z<sup>2</sup>", "12x<sup>2</sup> + 25xy + 32xz + 12y<sup>2</sup> + 16yz + 20z<sup>2</sup>", "12x<sup>2</sup> + 12xy + 20xz + 12y<sup>2</sup> + 31yz + 20z<sup>2</sup>", "12x<sup>2</sup> + 25xy + 32xz + 12y<sup>2</sup> + 31yz + 20z<sup>2</sup>"], "correct": 3, "tag": "", "sol": "× 4x: 12x<sup>2</sup> + 16xy + 20xz; × 3y: 9xy + 12y<sup>2</sup> + 15yz; × 4z: 12xz + 16yz + 20z<sup>2</sup>. Collect: 12x<sup>2</sup> + 25xy + 32xz + 12y<sup>2</sup> + 31yz + 20z<sup>2</sup>."}, {"kind": "blank", "p": "<b>Ex 7C · Q5(d–f)</b> · Find the product.", "tag": "", "marks": "", "flat": [{"t": "d) (a<sup>2</sup>b<sup>2</sup> − 2ab + 4)(a + 2) = __B1__", "a": {"B1": "a^3b^2+2a^2b^2-2a^2b-4ab+4a+8"}, "expr": true}, {"t": "e) (x<sup>2</sup> − y<sup>2</sup>)(4x<sup>3</sup> − y<sup>3</sup>) = __B1__", "a": {"B1": "4x^5-x^2y^3-4x^3y^2+y^5"}, "expr": true}, {"t": "f) (x<sup>2</sup> + y<sup>2</sup>)(x<sup>2</sup> + xy + y<sup>2</sup>) = __B1__", "a": {"B1": "x^4+x^3y+2x^2y^2+xy^3+y^4"}, "expr": true}], "sol": "a<sup>3</sup>b<sup>2</sup> + 2a<sup>2</sup>b<sup>2</sup> − 2a<sup>2</sup>b − 4ab + 4a + 8 (no like terms).\n4x<sup>5</sup> − x<sup>2</sup>y<sup>3</sup> − 4x<sup>3</sup>y<sup>2</sup> + y<sup>5</sup>.\nx<sup>4</sup> + x<sup>3</sup>y + x<sup>2</sup>y<sup>2</sup> + x<sup>2</sup>y<sup>2</sup> + xy<sup>3</sup> + y<sup>4</sup> = x<sup>4</sup> + x<sup>3</sup>y + 2x<sup>2</sup>y<sup>2</sup> + xy<sup>3</sup> + y<sup>4</sup>."}, {"kind": "blank", "p": "<b>Ex 7C · Q5(h, i)</b> · Find the product.", "tag": "", "marks": "", "flat": [{"t": "h) (4x − 2y + z)(5x − 5y + z) = __B1__", "a": {"B1": "20x^2-30xy+9xz+10y^2-7yz+z^2"}, "expr": true}, {"t": "i) (x<sup>2</sup> + y<sup>2</sup> + z<sup>2</sup>)(x + y + z) = __B1__", "a": {"B1": "x^3+y^3+z^3+x^2y+x^2z+xy^2+y^2z+xz^2+yz^2"}, "expr": true}], "sol": "× 5x: 20x<sup>2</sup> − 10xy + 5xz; × (−5y): −20xy + 10y<sup>2</sup> − 5yz; × z: 4xz − 2yz + z<sup>2</sup>. Collect: 20x<sup>2</sup> − 30xy + 9xz + 10y<sup>2</sup> − 7yz + z<sup>2</sup>.\nNine products, no like terms: x<sup>3</sup> + x<sup>2</sup>y + x<sup>2</sup>z + xy<sup>2</sup> + y<sup>3</sup> + y<sup>2</sup>z + xz<sup>2</sup> + yz<sup>2</sup> + z<sup>3</sup>."}, {"kind": "mcq", "text": "<b>Ex 7C · Q6</b> · If the length and breadth of a rectangle are (2a + 3ab + b) units and (a + 3b) units, what is its area in polynomial form?", "opts": ["2a<sup>2</sup> + 7ab + 3b<sup>2</sup> + 3a<sup>2</sup>b + 9ab<sup>2</sup>", "2a<sup>2</sup> + 7ab + 3b<sup>2</sup> + 3a<sup>2</sup>b + 3ab<sup>2</sup>", "2a<sup>2</sup> + 6ab + 3b<sup>2</sup> + 3a<sup>2</sup>b + 9ab<sup>2</sup>", "3a + 3ab + 4b"], "correct": 0, "tag": "", "sol": "Area = (2a + 3ab + b)(a + 3b) = 2a<sup>2</sup> + 6ab + 3a<sup>2</sup>b + 9ab<sup>2</sup> + ab + 3b<sup>2</sup> = 2a<sup>2</sup> + 7ab + 3b<sup>2</sup> + 3a<sup>2</sup>b + 9ab<sup>2</sup> square units."}]}, {"id": "s4", "label": "7.4 Divide by monomial", "sub": "Dividing by a monomial", "slides": [{"kind": "blank", "p": "<b>Examples 15–17</b> · Simplify.", "tag": "", "marks": "", "flat": [{"t": "Example 15: a<sup>6</sup> ÷ a<sup>3</sup> = __B1__", "a": {"B1": "a^3"}, "expr": true}, {"t": "Example 16: 10x<sup>7</sup> ÷ 2x<sup>4</sup> = __B1__", "a": {"B1": "5x^3"}, "expr": true}, {"t": "Example 17: x<sup>4</sup> ÷ x<sup>4</sup> = __B1__", "a": {"B1": "1"}}], "sol": "(a × a × a × a × a × a)/(a × a × a) = a<sup>6−3</sup> = a<sup>3</sup>.\n{10/2} = 5 and x<sup>7−4</sup> = x<sup>3</sup>.\nx<sup>4−4</sup> = x<sup>0</sup> = 1: any number divided by itself gives 1."}, {"kind": "mcq", "text": "<b>Example 18</b> · Simplify:  a) −100a<sup>3</sup> ÷ 20a   b) −35x<sup>5</sup>y<sup>2</sup> ÷ (−7x<sup>3</sup>y)", "opts": ["a) −5a<sup>2</sup>  b) 5x<sup>2</sup>y<sup>2</sup>", "a) 5a<sup>2</sup>  b) −5x<sup>2</sup>y", "a) −5a<sup>3</sup>  b) 5x<sup>2</sup>y", "a) −5a<sup>2</sup>  b) 5x<sup>2</sup>y"], "correct": 3, "tag": "", "sol": "a) −100 ÷ 20 = −5 and a<sup>3−1</sup> = a<sup>2</sup>. b) (−35) ÷ (−7) = +5, x<sup>5−3</sup> = x<sup>2</sup>, y<sup>2−1</sup> = y."}, {"kind": "blank", "p": "<b>Example 19</b> · Divide (32x<sup>4</sup>y<sup>3</sup> − 16x<sup>3</sup>y<sup>4</sup>) by (−8x<sup>2</sup>y).", "tag": "", "marks": "", "flat": [{"t": "32x<sup>4</sup>y<sup>3</sup> ÷ (−8x<sup>2</sup>y) = __B1__", "a": {"B1": "-4x^2y^2"}, "expr": true}, {"t": "−16x<sup>3</sup>y<sup>4</sup> ÷ (−8x<sup>2</sup>y) = __B1__", "a": {"B1": "2xy^3"}, "expr": true}, {"t": "Quotient = __B1__", "a": {"B1": "-4x^2y^2+2xy^3"}, "expr": true}], "sol": "32 ÷ (−8) = −4; x<sup>2</sup>y<sup>2</sup>.\n(−16) ÷ (−8) = +2; xy<sup>3</sup>.\n−4x<sup>2</sup>y<sup>2</sup> + 2xy<sup>3</sup>."}, {"kind": "mcq", "text": "<b>Example 20</b> · Divide 4ax<sup>2</sup> + 8a<sup>2</sup>x by 2ax.", "opts": ["2ax + 4a", "2x + 4a", "4x + 2a", "2x + 4a<sup>2</sup>x"], "correct": 1, "tag": "", "sol": "Divide each term: 4ax<sup>2</sup>/(2ax) = 2x and 8a<sup>2</sup>x/(2ax) = 4a. Quotient 2x + 4a."}, {"kind": "blank", "p": "<b>Example 21</b> · Divide (38a<sup>3</sup>b<sup>3</sup>c<sup>2</sup> − 19a<sup>4</sup>b<sup>2</sup>c) by 19a<sup>2</sup>bc.", "tag": "", "marks": "", "flat": [{"t": "Quotient = __B1__", "a": {"B1": "2ab^2c-a^2b"}, "expr": true}], "sol": "38a<sup>3</sup>b<sup>3</sup>c<sup>2</sup> ÷ 19a<sup>2</sup>bc = 2ab<sup>2</sup>c; 19a<sup>4</sup>b<sup>2</sup>c ÷ 19a<sup>2</sup>bc = a<sup>2</sup>b. Quotient 2ab<sup>2</sup>c − a<sup>2</sup>b."}, {"kind": "blank", "p": "<b>Try This</b> · Divide.", "tag": "", "marks": "", "flat": [{"t": "a) x<sup>6</sup> ÷ x<sup>2</sup> = __B1__", "a": {"B1": "x^4"}, "expr": true}, {"t": "b) (8m<sup>3</sup> + 2m<sup>2</sup>) ÷ 2m = __B1__", "a": {"B1": "4m^2+m"}, "expr": true}, {"t": "c) 2p<sup>3</sup> ÷ p<sup>3</sup> = __B1__", "a": {"B1": "2"}}, {"t": "d) (25y<sup>2</sup> + 5y) ÷ 5y = __B1__", "a": {"B1": "5y+1"}, "expr": true}], "sol": "x<sup>6−2</sup> = x<sup>4</sup>.\n4m<sup>2</sup> + m.\n2p<sup>3</sup>/p<sup>3</sup> = 2.\n5y + 1 (5y ÷ 5y = 1, not 0)."}, {"kind": "mcq", "text": "<b>Ex 7D · Q1(f)</b> · Simplify (−6<sup>3</sup>) ÷ (−6<sup>3</sup>).", "opts": ["1", "6", "0", "−1"], "correct": 0, "tag": "", "sol": "Any non-zero number divided by itself is 1."}, {"kind": "blank", "p": "<b>Ex 7D · Q1(a–e)</b> · Simplify.", "tag": "", "marks": "", "flat": [{"t": "a) p<sup>100</sup> ÷ p<sup>2</sup> = __B1__", "a": {"B1": "p^98"}, "expr": true}, {"t": "b) m<sup>6</sup> ÷ m<sup>3</sup> = __B1__", "a": {"B1": "m^3"}, "expr": true}, {"t": "c) x<sup>20</sup>y<sup>5</sup> ÷ x<sup>4</sup>y<sup>3</sup> = __B1__", "a": {"B1": "x^16y^2"}, "expr": true}, {"t": "d) 8x<sup>9</sup>y<sup>5</sup> ÷ 2x<sup>2</sup>y<sup>3</sup> = __B1__", "a": {"B1": "4x^7y^2"}, "expr": true}, {"t": "e) 49a<sup>4</sup>b<sup>6</sup>c<sup>8</sup> ÷ 7a<sup>2</sup>b<sup>2</sup>c<sup>2</sup> = __B1__", "a": {"B1": "7a^2b^4c^6"}, "expr": true}], "sol": "p<sup>100−2</sup> = p<sup>98</sup>.\nm<sup>3</sup>.\nx<sup>16</sup>y<sup>2</sup>.\n4x<sup>7</sup>y<sup>2</sup>.\n49 ÷ 7 = 7; a<sup>4−2</sup>b<sup>6−2</sup>c<sup>8−2</sup> = a<sup>2</sup>b<sup>4</sup>c<sup>6</sup>."}, {"kind": "blank", "p": "<b>Ex 7D · Q2(a–e)</b> · Simplify.", "tag": "", "marks": "", "flat": [{"t": "a) (8x + 8y) ÷ 8 = __B1__", "a": {"B1": "x+y"}, "expr": true}, {"t": "b) (100x − 60y) ÷ (−4) = __B1__", "a": {"B1": "-25x+15y"}, "expr": true}, {"t": "c) (−6y<sup>2</sup> − 24z<sup>2</sup>) ÷ 6 = __B1__", "a": {"B1": "-y^2-4z^2"}, "expr": true}, {"t": "d) (64y<sup>4</sup> + 8y<sup>3</sup>) ÷ 4y<sup>3</sup> = __B1__", "a": {"B1": "16y+2"}, "expr": true}, {"t": "e) (−14x<sup>12</sup>y + 8x<sup>5</sup>z) ÷ 2x<sup>2</sup> = __B1__", "a": {"B1": "-7x^10y+4x^3z"}, "expr": true}], "sol": "x + y.\n100 ÷ (−4) = −25; −60 ÷ (−4) = +15.\n−y<sup>2</sup> − 4z<sup>2</sup>.\n16y + 2.\n−7x<sup>10</sup>y + 4x<sup>3</sup>z."}, {"kind": "mcq", "text": "<b>Ex 7D · Q2(f)</b> · Simplify (36q<sup>5</sup> + 48q<sup>9</sup>) ÷ (−12q<sup>3</sup>).", "opts": ["−3q<sup>8</sup> − 4q<sup>12</sup>", "−3q<sup>2</sup> − 4q<sup>6</sup>", "−3q<sup>2</sup> + 4q<sup>6</sup>", "3q<sup>2</sup> + 4q<sup>6</sup>"], "correct": 1, "tag": "", "sol": "36q<sup>5</sup> ÷ (−12q<sup>3</sup>) = −3q<sup>2</sup>; 48q<sup>9</sup> ÷ (−12q<sup>3</sup>) = −4q<sup>6</sup>."}, {"kind": "blank", "p": "<b>Ex 7D · Q2(g–j)</b> · Simplify.", "tag": "", "marks": "", "flat": [{"t": "g) (−14a<sup>12</sup>c + 8a<sup>2</sup>c) ÷ 2a<sup>2</sup>c = __B1__", "a": {"B1": "-7a^10+4"}, "expr": true}, {"t": "h) (−81a<sup>9</sup>b<sup>14</sup> + 27a<sup>5</sup>b<sup>3</sup>) ÷ 9a<sup>3</sup>b<sup>2</sup> = __B1__", "a": {"B1": "-9a^6b^12+3a^2b"}, "expr": true}, {"t": "i) (−15x<sup>3</sup> + 12x<sup>7</sup>) ÷ 3x = __B1__", "a": {"B1": "-5x^2+4x^6"}, "expr": true}, {"t": "j) (100k<sup>5</sup> + 16k<sup>4</sup>) ÷ 4k<sup>3</sup> = __B1__", "a": {"B1": "25k^2+4k"}, "expr": true}], "sol": "−7a<sup>10</sup> + 4.\n−9a<sup>6</sup>b<sup>12</sup> + 3a<sup>2</sup>b.\n−5x<sup>2</sup> + 4x<sup>6</sup>.\n25k<sup>2</sup> + 4k."}, {"kind": "blank", "p": "<b>Ex 7D · Q2(k–m)</b> · Simplify.", "tag": "", "marks": "", "flat": [{"t": "k) (34y<sup>3</sup>z<sup>2</sup> + 51y<sup>5</sup>z<sup>3</sup>) ÷ 17y<sup>2</sup>z<sup>2</sup> = __B1__", "a": {"B1": "2y+3y^3z"}, "expr": true}, {"t": "l) (−30a<sup>6</sup> − 6a<sup>3</sup>) ÷ (−6a<sup>3</sup>) = __B1__", "a": {"B1": "5a^3+1"}, "expr": true}, {"t": "m) (−60a<sup>3</sup> + 80a<sup>5</sup>) ÷ 20a<sup>3</sup> = __B1__", "a": {"B1": "-3+4a^2"}, "expr": true}], "sol": "2y + 3y<sup>3</sup>z.\n5a<sup>3</sup> + 1.\n−3 + 4a<sup>2</sup>."}, {"kind": "mcq", "text": "<b>Ex 7D · Q3</b> · If 5x books cost ₹ (10x<sup>2</sup> + 20x), what is the cost of one book?", "opts": ["2x + 20x", "2x + 4", "10x + 4", "50x<sup>3</sup> + 100x<sup>2</sup>"], "correct": 1, "tag": "", "sol": "Cost of one book = (10x<sup>2</sup> + 20x) ÷ 5x = ₹ (2x + 4)."}, {"kind": "blank", "p": "<b>Ex 7D · Q4</b> · If the area of a rectangular field is (21x<sup>2</sup> − 7x) sq. units and one of its sides is 7x units, what is its other side?", "tag": "", "marks": "", "flat": [{"t": "Other side = __B1__ units", "a": {"B1": "3x-1"}, "expr": true}], "sol": "Other side = area ÷ side = (21x<sup>2</sup> − 7x) ÷ 7x = 3x − 1 units."}, {"kind": "mcq", "text": "<b>Ex 7D · Q5</b> · If a train travels (30a<sup>2</sup> + 15a − 10) kilometres in 10 hours, what is its average speed (in km/h)?", "opts": ["300a<sup>2</sup> + 150a − 100", "3a<sup>2</sup> + 1.5a − 1", "3a<sup>2</sup> + 1.5a − 10", "3a<sup>2</sup> + 15a − 1"], "correct": 1, "tag": "", "sol": "Speed = distance ÷ time = (30a<sup>2</sup> + 15a − 10) ÷ 10 = 3a<sup>2</sup> + {3/2}a − 1 km/h."}]}, {"id": "s5", "label": "7.5 Long division", "sub": "Dividing a polynomial by a polynomial", "slides": [{"kind": "blank", "p": "<b>Example 22</b> · Divide (−5 − 7a + 6a<sup>2</sup>) by (2a + 1).", "tag": "", "marks": "", "flat": [{"t": "First term of the quotient: 6a<sup>2</sup> ÷ 2a = __B1__", "a": {"B1": "3a"}, "expr": true}, {"t": "After subtracting 3a(2a + 1) = 6a<sup>2</sup> + 3a, what is left = __B1__", "a": {"B1": "-10a-5"}, "expr": true}, {"t": "Quotient = __B1__", "a": {"B1": "3a-5"}, "expr": true}, {"t": "Remainder = __B1__", "a": {"B1": "0"}}], "sol": "Arrange as 6a<sup>2</sup> − 7a − 5; 6a<sup>2</sup> ÷ 2a = 3a.\n6a<sup>2</sup> − 7a − 5 − (6a<sup>2</sup> + 3a) = −10a − 5 (bring down −5).\n−10a ÷ 2a = −5, so the quotient is 3a − 5.\n−5(2a + 1) = −10a − 5; subtracting leaves 0. Check: (2a + 1)(3a − 5) = 6a<sup>2</sup> − 7a − 5."}, {"kind": "mcq", "text": "<b>Example 23</b> · Divide (5y<sup>3</sup> + y − 3) by (y − 1).", "opts": ["Quotient 5y<sup>2</sup> − 5y + 6, remainder −9", "Quotient 5y<sup>2</sup> + 5y + 6, remainder 0", "Quotient 5y<sup>2</sup> + 5y + 6, remainder 3", "Quotient 5y<sup>2</sup> + 6, remainder 3"], "correct": 2, "tag": "", "sol": "Write 5y<sup>3</sup> + 0y<sup>2</sup> + y − 3. 5y<sup>3</sup> ÷ y = 5y<sup>2</sup> → leaves 5y<sup>2</sup> + y; 5y<sup>2</sup> ÷ y = 5y → leaves 6y − 3; 6y ÷ y = 6 → leaves 3. Quotient 5y<sup>2</sup> + 5y + 6, remainder 3."}, {"kind": "blank", "p": "<b>Example 24</b> · Find (4a<sup>2</sup> + 4a + 1) ÷ (2a + 1).", "tag": "", "marks": "", "flat": [{"t": "Quotient = __B1__", "a": {"B1": "2a+1"}, "expr": true}, {"t": "Remainder = __B1__", "a": {"B1": "0"}}], "sol": "4a<sup>2</sup> ÷ 2a = 2a; 4a<sup>2</sup> + 4a + 1 − (4a<sup>2</sup> + 2a) = 2a + 1; 2a ÷ 2a = 1.\n2a + 1 − (2a + 1) = 0."}, {"kind": "blank", "p": "<b>Example 25</b> · Find (x<sup>2</sup> − 7xy + 12y<sup>2</sup>) ÷ (x − 3y).", "tag": "", "marks": "", "flat": [{"t": "Quotient = __B1__", "a": {"B1": "x-4y"}, "expr": true}, {"t": "Remainder = __B1__", "a": {"B1": "0"}}], "sol": "x<sup>2</sup> ÷ x = x; subtract x<sup>2</sup> − 3xy → −4xy + 12y<sup>2</sup>; −4xy ÷ x = −4y.\n−4y(x − 3y) = −4xy + 12y<sup>2</sup>; remainder 0."}, {"kind": "mcq", "text": "<b>Example 26</b> · Find (14x<sup>2</sup> − 29xy − 18y<sup>2</sup>) ÷ (2x − 5y).", "opts": ["Quotient 7x + 3y, remainder 3y<sup>2</sup>", "Quotient 7x + 3y, remainder 0", "Quotient 7x + 3y, remainder −3y<sup>2</sup>", "Quotient 7x − 3y, remainder −3y<sup>2</sup>"], "correct": 2, "tag": "", "sol": "14x<sup>2</sup> ÷ 2x = 7x; subtract 14x<sup>2</sup> − 35xy → 6xy − 18y<sup>2</sup>; 6xy ÷ 2x = 3y; subtract 6xy − 15y<sup>2</sup> → −3y<sup>2</sup>. Check: (2x − 5y)(7x + 3y) − 3y<sup>2</sup> = 14x<sup>2</sup> − 29xy − 18y<sup>2</sup>."}, {"kind": "mcq", "text": "<b>Try This</b> · Find the following:  a) (x<sup>2</sup> − 169) ÷ (x − 13)   b) (x<sup>2</sup> + 2x + 1) ÷ (x + 1)", "opts": ["a) x + 13   b) x + 2", "a) x − 13   b) x + 1", "a) x + 13   b) x + 1", "a) x + 13, remainder 169   b) x + 1"], "correct": 2, "tag": "", "sol": "a) Write x<sup>2</sup> + 0x − 169. x<sup>2</sup> ÷ x = x; x(x − 13) = x<sup>2</sup> − 13x; left 13x − 169; 13x ÷ x = 13; 13(x − 13) = 13x − 169; remainder 0. b) x<sup>2</sup> ÷ x = x; left x + 1; (x + 1) ÷ (x + 1) = 1; remainder 0."}, {"kind": "blank", "p": "<b>Ex 7E · Q1(a–c)</b> · Simplify.", "tag": "", "marks": "", "flat": [{"t": "a) (x<sup>2</sup> + 7x + 10) ÷ (x + 5) = __B1__", "a": {"B1": "x+2"}, "expr": true}, {"t": "b) (a<sup>2</sup> − 13a + 30) ÷ (a − 10) = __B1__", "a": {"B1": "a-3"}, "expr": true}, {"t": "c) (p<sup>2</sup> − 7p − 18) ÷ (p − 9) = __B1__", "a": {"B1": "p+2"}, "expr": true}], "sol": "x<sup>2</sup> ÷ x = x, left 2x + 10 = 2(x + 5): x + 2.\na<sup>2</sup> ÷ a = a, left −3a + 30 = −3(a − 10): a − 3.\np<sup>2</sup> ÷ p = p, left 2p − 18 = 2(p − 9): p + 2."}, {"kind": "blank", "p": "<b>Ex 7E · Q1(d–f)</b> · Simplify.", "tag": "", "marks": "", "flat": [{"t": "d) (p<sup>2</sup> − p − 6)/(p − 3) = __B1__", "a": {"B1": "p+2"}, "expr": true}, {"t": "e) (y<sup>2</sup> − 90y + 2000)/(y − 50) = __B1__", "a": {"B1": "y-40"}, "expr": true}, {"t": "f) (6x<sup>2</sup> + 15x + 9)/(2x + 3) = __B1__", "a": {"B1": "3x+3"}, "expr": true}], "sol": "p<sup>2</sup> ÷ p = p, left 2p − 6 = 2(p − 3): p + 2.\ny<sup>2</sup> ÷ y = y, left −40y + 2000 = −40(y − 50): y − 40.\n6x<sup>2</sup> ÷ 2x = 3x, left 6x + 9 = 3(2x + 3): 3x + 3."}, {"kind": "mcq", "text": "<b>Ex 7E · Q2(a)</b> · Simplify (6x<sup>2</sup> − 7x − 5) ÷ (2x + 1).", "opts": ["2x − 5", "3x − 2", "3x + 5", "3x − 5"], "correct": 3, "tag": "", "sol": "6x<sup>2</sup> ÷ 2x = 3x; 6x<sup>2</sup> − 7x − 5 − (6x<sup>2</sup> + 3x) = −10x − 5 = −5(2x + 1). Quotient 3x − 5."}, {"kind": "blank", "p": "<b>Ex 7E · Q2(b, c)</b> · Simplify.", "tag": "", "marks": "", "flat": [{"t": "b) (x<sup>2</sup> − 7xy − 18y<sup>2</sup>) ÷ (x − 9y) = __B1__", "a": {"B1": "x+2y"}, "expr": true}, {"t": "c) (9x<sup>2</sup> + 6x + 1)/(3x + 1) = __B1__", "a": {"B1": "3x+1"}, "expr": true}], "sol": "x<sup>2</sup> ÷ x = x; left 2xy − 18y<sup>2</sup> = 2y(x − 9y): x + 2y.\n9x<sup>2</sup> ÷ 3x = 3x; left 3x + 1: 3x + 1."}, {"kind": "blank", "p": "<b>Ex 7E · Q3(a, b)</b> · Find the quotient and remainder.", "tag": "", "marks": "", "flat": [{"t": "a) (2p<sup>2</sup> + 7p − 9) ÷ (p − 6): quotient = __B1__", "a": {"B1": "2p+19"}, "expr": true}, {"t": "remainder = __B1__", "a": {"B1": "105"}}, {"t": "b) (a<sup>2</sup> + 8a − 9)/(a − 7): quotient = __B1__", "a": {"B1": "a+15"}, "expr": true}, {"t": "remainder = __B1__", "a": {"B1": "96"}}], "sol": "2p<sup>2</sup> ÷ p = 2p; left 19p − 9; 19p ÷ p = 19.\n19(p − 6) = 19p − 114; −9 + 114 = 105. Check: (p − 6)(2p + 19) + 105 = 2p<sup>2</sup> + 7p − 9.\na<sup>2</sup> ÷ a = a; left 15a − 9; 15a ÷ a = 15.\n15(a − 7) = 15a − 105; −9 + 105 = 96."}, {"kind": "mcq", "text": "<b>Ex 7E · Q3(c)</b> · Find the quotient and remainder: (x<sup>2</sup> + 6x + 11)/(x − 3).", "opts": ["Quotient x + 3, remainder 20", "Quotient x − 9, remainder 38", "Quotient x + 9, remainder 38", "Quotient x + 9, remainder −16"], "correct": 2, "tag": "", "sol": "x<sup>2</sup> ÷ x = x; left 9x + 11; 9x ÷ x = 9; 9(x − 3) = 9x − 27; 11 + 27 = 38."}, {"kind": "blank", "p": "<b>Ex 7E · Q3(d)</b> · Find the quotient and remainder: (3p<sup>3</sup> − 7)/(p − 1).", "tag": "", "marks": "", "flat": [{"t": "Quotient = __B1__", "a": {"B1": "3p^2+3p+3"}, "expr": true}, {"t": "Remainder = __B1__", "a": {"B1": "-4"}}], "sol": "Write 3p<sup>3</sup> + 0p<sup>2</sup> + 0p − 7. 3p<sup>3</sup> ÷ p = 3p<sup>2</sup> → left 3p<sup>2</sup>; ÷ p = 3p → left 3p − 7; ÷ p = 3.\n3(p − 1) = 3p − 3; −7 + 3 = −4. Check: (p − 1)(3p<sup>2</sup> + 3p + 3) − 4 = 3p<sup>3</sup> − 7."}, {"kind": "mcq", "text": "<b>Ex 7E · Q4</b> · The area of a rectangular field is (a<sup>2</sup> − 19a + 90) square units. Find the width of the rectangle if its length is (a − 9) units.", "opts": ["a − 19", "a − 10", "a − 9", "a + 10"], "correct": 1, "tag": "", "sol": "Width = area ÷ length: a<sup>2</sup> ÷ a = a; left −10a + 90 = −10(a − 9). Width = (a − 10) units."}]}, {"id": "s6", "label": "7.6 Identities", "sub": "The four standard identities and their uses", "slides": [{"kind": "mcq", "text": "<b>Identity 1 · Fig. 7.2</b> · A rectangle with sides (x + a) and (x + b) is split into four parts. Which list gives the areas of the four parts?", "opts": ["x<sup>2</sup>, a<sup>2</sup>, b<sup>2</sup>, ab", "x<sup>2</sup>, ax, bx, ab", "x<sup>2</sup>, ax, bx, a + b", "2x, ax, bx, ab"], "correct": 1, "tag": "", "sol": "The parts are x × x, a × x, b × x and a × b. So (x + a)(x + b) = x<sup>2</sup> + ax + bx + ab = x<sup>2</sup> + (a + b)x + ab.", "fig": "<svg class=\"figsvg\" viewBox=\"0 0 286 216\" role=\"img\"><defs><marker id=\"ah\" viewBox=\"0 0 10 10\" refX=\"9\" refY=\"5\" markerWidth=\"7\" markerHeight=\"7\" orient=\"auto\"><path d=\"M0,1 L10,5 L0,9 z\" class=\"ahd\"/></marker><marker id=\"ahs\" viewBox=\"0 0 10 10\" refX=\"1\" refY=\"5\" markerWidth=\"7\" markerHeight=\"7\" orient=\"auto\"><path d=\"M10,1 L0,5 L10,9 z\" class=\"ahd\"/></marker></defs><text class=\"lb\" x=\"156.0\" y=\"10.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">Fig. 7.2</text><rect class=\"sh3\" x=\"46\" y=\"40\" width=\"220\" height=\"160\"/><text class=\"al\" x=\"121.0\" y=\"30.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">x</text><text class=\"al\" x=\"231.0\" y=\"30.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">a</text><line class=\"ln\" x1=\"196.0\" y1=\"40.0\" x2=\"196.0\" y2=\"200.0\"/><text class=\"al\" x=\"30.0\" y=\"95.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">x</text><text class=\"al\" x=\"30.0\" y=\"175.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">b</text><line class=\"ln\" x1=\"46.0\" y1=\"150.0\" x2=\"266.0\" y2=\"150.0\"/></svg>"}, {"kind": "blank", "p": "<b>Example 27(a–d)</b> · Use (x + a)(x + b) = x<sup>2</sup> + x(a + b) + ab.", "tag": "", "marks": "", "flat": [{"t": "a) (x + 3)(x + 5) = __B1__", "a": {"B1": "x^2+8x+15"}, "expr": true}, {"t": "b) (3x + 5)(3x + 4) = __B1__", "a": {"B1": "9x^2+27x+20"}, "expr": true}, {"t": "c) (x − 3)(x − 8) = __B1__", "a": {"B1": "x^2-11x+24"}, "expr": true}, {"t": "d) (x − 3)(x + 8) = __B1__", "a": {"B1": "x^2+5x-24"}, "expr": true}], "sol": "x<sup>2</sup> + x(3 + 5) + 5 × 3 = x<sup>2</sup> + 8x + 15.\n(3x)<sup>2</sup> + 3x(5 + 4) + 5 × 4 = 9x<sup>2</sup> + 27x + 20.\nx<sup>2</sup> + x[(−3) + (−8)] + (−3)(−8) = x<sup>2</sup> − 11x + 24.\nx<sup>2</sup> + x(−3 + 8) + (−3 × 8) = x<sup>2</sup> + 5x − 24."}, {"kind": "blank", "p": "<b>Example 27(e, f)</b> · Use the same identity to multiply numbers.", "tag": "", "marks": "", "flat": [{"t": "e) 102 × 104 = (100 + 2)(100 + 4) = __B1__", "a": {"B1": "10608"}}, {"t": "f) 101 × 98 = (100 + 1)(100 − 2) = __B1__", "a": {"B1": "9898"}}], "sol": "100<sup>2</sup> + 100(2 + 4) + 2 × 4 = 10000 + 600 + 8 = 10608.\n100<sup>2</sup> + 100(1 − 2) + 1 × (−2) = 10000 − 100 − 2 = 9898."}, {"kind": "mcq", "text": "<b>Example 28(a)</b> · Use (a + b)<sup>2</sup> = a<sup>2</sup> + 2ab + b<sup>2</sup> to find (x + 3)<sup>2</sup>.", "opts": ["x<sup>2</sup> + 6x + 9", "x<sup>2</sup> + 9", "x<sup>2</sup> + 6x + 6", "x<sup>2</sup> + 3x + 9"], "correct": 0, "tag": "", "sol": "x<sup>2</sup> + 2 × 3 × x + 3<sup>2</sup> = x<sup>2</sup> + 6x + 9."}, {"kind": "blank", "p": "<b>Example 28(b, c)</b> · Use (a + b)<sup>2</sup> = a<sup>2</sup> + 2ab + b<sup>2</sup>.", "tag": "", "marks": "", "flat": [{"t": "b) (103)<sup>2</sup> = (100 + 3)<sup>2</sup> = __B1__", "a": {"B1": "10609"}}, {"t": "c) (52)<sup>2</sup> = (50 + 2)<sup>2</sup> = __B1__", "a": {"B1": "2704"}}], "sol": "10000 + 2 × 3 × 100 + 9 = 10000 + 600 + 9 = 10609.\n2500 + 2 × 2 × 50 + 4 = 2500 + 200 + 4 = 2704."}, {"kind": "blank", "p": "<b>Example 29</b> · Use (a − b)<sup>2</sup> = a<sup>2</sup> − 2ab + b<sup>2</sup>.", "tag": "", "marks": "", "flat": [{"t": "a) (x − 5)<sup>2</sup> = __B1__", "a": {"B1": "x^2-10x+25"}, "expr": true}, {"t": "b) (96)<sup>2</sup> = (100 − 4)<sup>2</sup> = __B1__", "a": {"B1": "9216"}}, {"t": "c) (23)<sup>2</sup> = (25 − 2)<sup>2</sup> = __B1__", "a": {"B1": "529"}}], "sol": "x<sup>2</sup> − 2 × x × 5 + 5<sup>2</sup> = x<sup>2</sup> − 10x + 25.\n10000 − 800 + 16 = 9216.\n625 − 100 + 4 = 529."}, {"kind": "mcq", "text": "<b>Example 30(a)</b> · Use (a + b)(a − b) = a<sup>2</sup> − b<sup>2</sup> to find (x + 3)(x − 3).", "opts": ["x<sup>2</sup> − 6x − 9", "x<sup>2</sup> − 9", "x<sup>2</sup> − 3", "x<sup>2</sup> + 9"], "correct": 1, "tag": "", "sol": "x<sup>2</sup> − 3<sup>2</sup> = x<sup>2</sup> − 9."}, {"kind": "blank", "p": "<b>Example 30(b, c)</b> · Use (a + b)(a − b) = a<sup>2</sup> − b<sup>2</sup>.", "tag": "", "marks": "", "flat": [{"t": "b) 97 × 103 = (100 − 3)(100 + 3) = __B1__", "a": {"B1": "9991"}}, {"t": "c) 26 × 34 = (30 − 4)(30 + 4) = __B1__", "a": {"B1": "884"}}], "sol": "100<sup>2</sup> − 3<sup>2</sup> = 10000 − 9 = 9991.\n30<sup>2</sup> − 4<sup>2</sup> = 900 − 16 = 884."}, {"kind": "blank", "p": "<b>Try This</b> · Find the following using a suitable identity.", "tag": "", "marks": "", "flat": [{"t": "a) (101)<sup>2</sup> = __B1__", "a": {"B1": "10201"}}, {"t": "b) (99)<sup>2</sup> = __B1__", "a": {"B1": "9801"}}, {"t": "c) 103 × 97 = __B1__", "a": {"B1": "9991"}}, {"t": "d) (x + 1)(x + 3) = __B1__", "a": {"B1": "x^2+4x+3"}, "expr": true}], "sol": "(100 + 1)<sup>2</sup> = 10000 + 200 + 1 = 10201.\n(100 − 1)<sup>2</sup> = 10000 − 200 + 1 = 9801.\n(100 + 3)(100 − 3) = 10000 − 9 = 9991.\nx<sup>2</sup> + (1 + 3)x + 1 × 3 = x<sup>2</sup> + 4x + 3."}, {"kind": "mcq", "text": "<b>Ex 7F · Q1(a)</b> · Give the product (x + c)(x + d) using (x + a)(x + b) = x<sup>2</sup> + (a + b)x + ab.", "opts": ["x<sup>2</sup> + cdx + (c + d)", "x<sup>2</sup> + (c + d)x + cd", "x<sup>2</sup> + c<sup>2</sup> + d<sup>2</sup>", "x<sup>2</sup> + 2cdx + cd"], "correct": 1, "tag": "", "sol": "Put a = c and b = d: x<sup>2</sup> + (c + d)x + cd."}, {"kind": "blank", "p": "<b>Ex 7F · Q1(b–d)</b> · Give the product using (x + a)(x + b) = x<sup>2</sup> + (a + b)x + ab.", "tag": "", "marks": "", "flat": [{"t": "b) (x + 2)(x + 3) = __B1__", "a": {"B1": "x^2+5x+6"}, "expr": true}, {"t": "c) (x − 3)(x − 3) = __B1__", "a": {"B1": "x^2-6x+9"}, "expr": true}, {"t": "d) (x + 7)(x − 5) = __B1__", "a": {"B1": "x^2+2x-35"}, "expr": true}], "sol": "x<sup>2</sup> + 5x + 6.\nx<sup>2</sup> + (−3 − 3)x + 9 = x<sup>2</sup> − 6x + 9.\nx<sup>2</sup> + (7 − 5)x + 7 × (−5) = x<sup>2</sup> + 2x − 35."}, {"kind": "blank", "p": "<b>Ex 7F · Q1(e–h)</b> · Multiply using (x + a)(x + b) = x<sup>2</sup> + (a + b)x + ab.", "tag": "", "marks": "", "flat": [{"t": "e) 12 × 18 = (10 + 2)(10 + 8) = __B1__", "a": {"B1": "216"}}, {"t": "f) 104 × 103 = __B1__", "a": {"B1": "10712"}}, {"t": "g) 95 × 102 = (100 − 5)(100 + 2) = __B1__", "a": {"B1": "9690"}}, {"t": "h) 198 × 209 = (200 − 2)(200 + 9) = __B1__", "a": {"B1": "41382"}}], "sol": "100 + 10 × 10 + 16 = 216.\n(100 + 4)(100 + 3) = 10000 + 700 + 12 = 10712.\n10000 + 100 × (−3) + (−10) = 10000 − 300 − 10 = 9690.\n40000 + 200 × 7 + (−18) = 40000 + 1400 − 18 = 41382."}, {"kind": "mcq", "text": "<b>Ex 7F · Q2(c)</b> · Find ({3x/4} + 1)<sup>2</sup> using (a + b)<sup>2</sup> = a<sup>2</sup> + 2ab + b<sup>2</sup>.", "opts": ["(9/4)x<sup>2</sup> + (3/2)x + 1", "(9/16)x<sup>2</sup> + (3/2)x + 1", "(9/16)x<sup>2</sup> + 1", "(9/16)x<sup>2</sup> + (3/4)x + 1"], "correct": 1, "tag": "", "sol": "({3x/4})<sup>2</sup> + 2 × {3x/4} × 1 + 1<sup>2</sup> = {9/16}x<sup>2</sup> + {3/2}x + 1."}, {"kind": "blank", "p": "<b>Ex 7F · Q2(a, b, d)</b> · Find the products using (a + b)<sup>2</sup> = a<sup>2</sup> + 2ab + b<sup>2</sup>.", "tag": "", "marks": "", "flat": [{"t": "a) (x + 3)<sup>2</sup> = __B1__", "a": {"B1": "x^2+6x+9"}, "expr": true}, {"t": "b) (3x + 2y)<sup>2</sup> = __B1__", "a": {"B1": "9x^2+12xy+4y^2"}, "expr": true}, {"t": "d) (2x<sup>2</sup>y + 3xy<sup>2</sup>)<sup>2</sup> = __B1__", "a": {"B1": "4x^4y^2+12x^3y^3+9x^2y^4"}, "expr": true}], "sol": "x<sup>2</sup> + 6x + 9.\n9x<sup>2</sup> + 2 × 3x × 2y + 4y<sup>2</sup> = 9x<sup>2</sup> + 12xy + 4y<sup>2</sup>.\n4x<sup>4</sup>y<sup>2</sup> + 2 × 2x<sup>2</sup>y × 3xy<sup>2</sup> + 9x<sup>2</sup>y<sup>4</sup> = 4x<sup>4</sup>y<sup>2</sup> + 12x<sup>3</sup>y<sup>3</sup> + 9x<sup>2</sup>y<sup>4</sup>."}, {"kind": "blank", "p": "<b>Ex 7F · Q3(a, c, d)</b> · Find the products using (a − b)<sup>2</sup> = a<sup>2</sup> − 2ab + b<sup>2</sup>.", "tag": "", "marks": "", "flat": [{"t": "a) (3x − 5y)<sup>2</sup> = __B1__", "a": {"B1": "9x^2-30xy+25y^2"}, "expr": true}, {"t": "c) (3x<sup>2</sup> − 2y<sup>2</sup>)<sup>2</sup> = __B1__", "a": {"B1": "9x^4-12x^2y^2+4y^4"}, "expr": true}, {"t": "d) 47<sup>2</sup> = (50 − 3)<sup>2</sup> = __B1__", "a": {"B1": "2209"}}], "sol": "9x<sup>2</sup> − 2 × 3x × 5y + 25y<sup>2</sup> = 9x<sup>2</sup> − 30xy + 25y<sup>2</sup>.\n9x<sup>4</sup> − 2 × 3x<sup>2</sup> × 2y<sup>2</sup> + 4y<sup>4</sup> = 9x<sup>4</sup> − 12x<sup>2</sup>y<sup>2</sup> + 4y<sup>4</sup>.\n2500 − 300 + 9 = 2209."}, {"kind": "mcq", "text": "<b>Ex 7F · Q3(b)</b> · Find ({3x/2} − {4y/3})<sup>2</sup> using (a − b)<sup>2</sup> = a<sup>2</sup> − 2ab + b<sup>2</sup>.", "opts": ["(9/4)x<sup>2</sup> − 2xy + (16/9)y<sup>2</sup>", "(9/4)x<sup>2</sup> + 4xy + (16/9)y<sup>2</sup>", "(9/4)x<sup>2</sup> − (16/9)y<sup>2</sup>", "(9/4)x<sup>2</sup> − 4xy + (16/9)y<sup>2</sup>"], "correct": 3, "tag": "", "sol": "({3x/2})<sup>2</sup> − 2 × {3x/2} × {4y/3} + ({4y/3})<sup>2</sup> = {9/4}x<sup>2</sup> − 4xy + {16/9}y<sup>2</sup>."}, {"kind": "blank", "p": "<b>Ex 7F · Q4</b> · Find the products using (a + b)(a − b) = a<sup>2</sup> − b<sup>2</sup>.", "tag": "", "marks": "", "flat": [{"t": "a) (m − 6)(m + 6) = __B1__", "a": {"B1": "m^2-36"}, "expr": true}, {"t": "b) (5xy − 7)(5xy + 7) = __B1__", "a": {"B1": "25x^2y^2-49"}, "expr": true}, {"t": "c) (x<sup>2</sup> + y<sup>2</sup>)(x<sup>2</sup> − y<sup>2</sup>) = __B1__", "a": {"B1": "x^4-y^4"}, "expr": true}, {"t": "d) 390 × 410 = (400 − 10)(400 + 10) = __B1__", "a": {"B1": "159900"}}], "sol": "m<sup>2</sup> − 36.\n(5xy)<sup>2</sup> − 7<sup>2</sup> = 25x<sup>2</sup>y<sup>2</sup> − 49.\n(x<sup>2</sup>)<sup>2</sup> − (y<sup>2</sup>)<sup>2</sup> = x<sup>4</sup> − y<sup>4</sup>.\n160000 − 100 = 159900."}, {"kind": "blank", "p": "<b>HOTS · Q1</b> · The area of a rectangular field is 3a<sup>2</sup> + 5ab + 2b<sup>2</sup>. One of its sides is (a + b). Find the length of the fence around the field.", "tag": "", "marks": "", "flat": [{"t": "Other side = __B1__", "a": {"B1": "3a+2b"}, "expr": true}, {"t": "Length of the fence (perimeter) = __B1__", "a": {"B1": "8a+6b"}, "expr": true}], "sol": "(3a<sup>2</sup> + 5ab + 2b<sup>2</sup>) ÷ (a + b): 3a<sup>2</sup> ÷ a = 3a, left 2ab + 2b<sup>2</sup> = 2b(a + b); other side 3a + 2b.\n2[(a + b) + (3a + 2b)] = 2(4a + 3b) = 8a + 6b."}, {"kind": "mcq", "text": "<b>HOTS · Q2</b> · A shirt costs ₹ (a<sup>2</sup> − ab − b<sup>2</sup>), trousers ₹ (2a<sup>2</sup> + 8ab − 2b<sup>2</sup>) and shoes ₹ (a<sup>2</sup> − 3ab + 4b<sup>2</sup>). Ranjan paid ₹ (2a + b)<sup>2</sup>. What balance will he receive?", "opts": ["₹ (4a<sup>2</sup> + 4ab + b<sup>2</sup>)", "₹ 0", "₹ 2b<sup>2</sup>", "₹ 2ab"], "correct": 1, "tag": "", "sol": "Total = (1 + 2 + 1)a<sup>2</sup> + (−1 + 8 − 3)ab + (−1 − 2 + 4)b<sup>2</sup> = 4a<sup>2</sup> + 4ab + b<sup>2</sup> = (2a + b)<sup>2</sup>. He paid exactly this, so the balance is ₹ 0."}]}, {"id": "s7", "label": "Assessment A", "sub": "Knowing and understanding", "slides": [{"kind": "mcq", "text": "<b>Check-up · MCQ 1</b> · Number of factors of (a + b)<sup>2</sup> is ______.", "opts": ["2", "1", "4", "3"], "correct": 0, "tag": "", "sol": "(a + b)<sup>2</sup> = (a + b)(a + b): it is the product of two factors, (a + b) and (a + b)."}, {"kind": "mcq", "text": "<b>Check-up · MCQ 2</b> · The factorised form of 4p − 24 is ______.", "opts": ["4(p − 8)", "24(p − 4)", "4(p − 6)", "4p × 24"], "correct": 2, "tag": "", "sol": "4p − 24 = 4 × p − 4 × 6 = 4(p − 6)."}, {"kind": "blank", "p": "<b>Check-up · Q5</b> · Simplify the following.", "tag": "", "marks": "", "flat": [{"t": "a) (−x<sup>2</sup>) + (−x<sup>2</sup>) + (−6x<sup>2</sup>) = __B1__", "a": {"B1": "-8x^2"}, "expr": true}, {"t": "b) (4 + x) − (4 − x) = __B1__", "a": {"B1": "2x"}, "expr": true}, {"t": "c) 3(m − 6) + 2(4 + 5m) = __B1__", "a": {"B1": "13m-10"}, "expr": true}, {"t": "d) −(−2x − 5y) − 4(2y − 4x) = __B1__", "a": {"B1": "18x-3y"}, "expr": true}], "sol": "−1 − 1 − 6 = −8: −8x<sup>2</sup>.\n4 + x − 4 + x = 2x.\n3m − 18 + 8 + 10m = 13m − 10.\n2x + 5y − 8y + 16x = 18x − 3y."}, {"kind": "blank", "p": "<b>Check-up · Q6</b> · Find the value of each expression when p = −1, q = −2, r = 3, s = −2.", "tag": "", "marks": "", "flat": [{"t": "a) 2p + 2r = __B1__", "a": {"B1": "4"}}, {"t": "b) (p − 3)(s + r) = __B1__", "a": {"B1": "-4"}}, {"t": "c) (p + q)(p<sup>2</sup> + 3) = __B1__", "a": {"B1": "-12"}}], "sol": "2(−1) + 2(3) = −2 + 6 = 4.\n(−1 − 3)(−2 + 3) = (−4)(1) = −4.\n(−1 − 2)((−1)<sup>2</sup> + 3) = (−3)(4) = −12."}, {"kind": "mcq", "text": "<b>Check-up · Q7(d, e)</b> · Find the products:  d) {1/4}ab({1/3}ab − 1)   e) a<sup>2</sup>b<sup>2</sup>({3ab/4} + ab<sup>2</sup>/3 + 1)", "opts": ["d) (1/12)a<sup>2</sup>b<sup>2</sup> − 1   e) (3/4)a<sup>3</sup>b<sup>3</sup> + (1/3)a<sup>3</sup>b<sup>4</sup> + a<sup>2</sup>b<sup>2</sup>", "d) (1/7)a<sup>2</sup>b<sup>2</sup> − (1/4)ab   e) (3/4)a<sup>3</sup>b<sup>3</sup> + (1/3)a<sup>3</sup>b<sup>4</sup> + 1", "d) (1/12)a<sup>2</sup>b<sup>2</sup> − (1/4)ab   e) (3/4)a<sup>2</sup>b<sup>3</sup> + (1/3)a<sup>2</sup>b<sup>4</sup> + a<sup>2</sup>b<sup>2</sup>", "d) (1/12)a<sup>2</sup>b<sup>2</sup> − (1/4)ab   e) (3/4)a<sup>3</sup>b<sup>3</sup> + (1/3)a<sup>3</sup>b<sup>4</sup> + a<sup>2</sup>b<sup>2</sup>"], "correct": 3, "tag": "", "sol": "d) {1/4}ab × {1/3}ab = {1/12}a<sup>2</sup>b<sup>2</sup> and {1/4}ab × (−1) = {−1/4}ab. e) a<sup>2</sup>b<sup>2</sup> × {3ab/4} = {3/4}a<sup>3</sup>b<sup>3</sup>; a<sup>2</sup>b<sup>2</sup> × ab<sup>2</sup>/3 = {1/3}a<sup>3</sup>b<sup>4</sup>; a<sup>2</sup>b<sup>2</sup> × 1 = a<sup>2</sup>b<sup>2</sup>."}, {"kind": "blank", "p": "<b>Check-up · Q7</b> · Find the product.", "tag": "", "marks": "", "flat": [{"t": "a) 4x(3x − 5) = __B1__", "a": {"B1": "12x^2-20x"}, "expr": true}, {"t": "b) 8xy(x − y + 3) = __B1__", "a": {"B1": "8x^2y-8xy^2+24xy"}, "expr": true}, {"t": "c) 10pq(1 − 12pq + p<sup>2</sup>q<sup>2</sup>) = __B1__", "a": {"B1": "10pq-120p^2q^2+10p^3q^3"}, "expr": true}, {"t": "f) (5x − 2y)(8x + 3y) = __B1__", "a": {"B1": "40x^2-xy-6y^2"}, "expr": true}, {"t": "g) (z + 3b)(z + 6b) = __B1__", "a": {"B1": "z^2+9bz+18b^2"}, "expr": true}, {"t": "h) (p<sup>2</sup> + pq + q<sup>2</sup>)(p − q) = __B1__", "a": {"B1": "p^3-q^3"}, "expr": true}], "sol": "12x<sup>2</sup> − 20x.\n8x<sup>2</sup>y − 8xy<sup>2</sup> + 24xy.\n10pq − 120p<sup>2</sup>q<sup>2</sup> + 10p<sup>3</sup>q<sup>3</sup>.\n40x<sup>2</sup> + 15xy − 16xy − 6y<sup>2</sup> = 40x<sup>2</sup> − xy − 6y<sup>2</sup>.\nz<sup>2</sup> + 6bz + 3bz + 18b<sup>2</sup> = z<sup>2</sup> + 9bz + 18b<sup>2</sup>.\np<sup>3</sup> − p<sup>2</sup>q + p<sup>2</sup>q − pq<sup>2</sup> + pq<sup>2</sup> − q<sup>3</sup> = p<sup>3</sup> − q<sup>3</sup>."}, {"kind": "blank", "p": "<b>Check-up · Q8</b> · Simplify.", "tag": "", "marks": "", "flat": [{"t": "a) a<sup>42</sup> ÷ a<sup>20</sup> = __B1__", "a": {"B1": "a^22"}, "expr": true}, {"t": "b) (−x<sup>2</sup>) ÷ (−x<sup>2</sup>) = __B1__", "a": {"B1": "1"}}, {"t": "c) 63a<sup>3</sup>b<sup>2</sup>c<sup>5</sup> ÷ (−7a<sup>2</sup>b<sup>2</sup>c<sup>2</sup>) = __B1__", "a": {"B1": "-9ac^3"}, "expr": true}, {"t": "d) −54g<sup>2</sup>h<sup>4</sup> ÷ 9gh = __B1__", "a": {"B1": "-6gh^3"}, "expr": true}, {"t": "e) 120x<sup>7</sup>y<sup>8</sup>z<sup>9</sup> ÷ 40x<sup>4</sup>y<sup>3</sup>z<sup>2</sup> = __B1__", "a": {"B1": "3x^3y^5z^7"}, "expr": true}], "sol": "a<sup>42−20</sup> = a<sup>22</sup>.\nA number divided by itself is 1.\n63 ÷ (−7) = −9; a; b<sup>0</sup> = 1; c<sup>3</sup>.\n−54 ÷ 9 = −6; g h<sup>3</sup>.\n120 ÷ 40 = 3; x<sup>3</sup>y<sup>5</sup>z<sup>7</sup>."}, {"kind": "mcq", "text": "<b>Check-up · Q9</b> · Simplify:  a) (20a − 20b)/10   b) (−49y<sup>2</sup> − 14x<sup>3</sup>)/(−7x<sup>2</sup>)   c) (−20m<sup>10</sup> − 5m<sup>3</sup>)/(−5m<sup>3</sup>)   d) (−34m<sup>5</sup>p<sup>12</sup> − 17m<sup>4</sup>p)/(17m<sup>2</sup>p)", "opts": ["a) 2a − 2b  b) 7y<sup>2</sup> + 2x  c) 4m<sup>7</sup>  d) −2m<sup>3</sup>p<sup>11</sup> − m<sup>2</sup>", "a) 2a − 2b  b) 7y<sup>2</sup>/x<sup>2</sup> + 2x  c) 4m<sup>7</sup> + 1  d) −2m<sup>3</sup>p<sup>11</sup> − m<sup>2</sup>", "a) 2a − 2b  b) 7y<sup>2</sup>/x<sup>2</sup> − 2x  c) 4m<sup>7</sup> + 1  d) −2m<sup>3</sup>p<sup>12</sup> − m<sup>2</sup>", "a) 2a − 20b  b) 7y<sup>2</sup>/x<sup>2</sup> + 2x  c) 4m<sup>7</sup> + 1  d) −2m<sup>3</sup>p<sup>11</sup> − m<sup>2</sup>"], "correct": 1, "tag": "", "sol": "a) 20a ÷ 10 = 2a, 20b ÷ 10 = 2b. b) −49y<sup>2</sup> ÷ (−7x<sup>2</sup>) = 7y<sup>2</sup>/x<sup>2</sup> and −14x<sup>3</sup> ÷ (−7x<sup>2</sup>) = 2x. c) −20m<sup>10</sup> ÷ (−5m<sup>3</sup>) = 4m<sup>7</sup> and −5m<sup>3</sup> ÷ (−5m<sup>3</sup>) = 1. d) −34m<sup>5</sup>p<sup>12</sup> ÷ 17m<sup>2</sup>p = −2m<sup>3</sup>p<sup>11</sup> and −17m<sup>4</sup>p ÷ 17m<sup>2</sup>p = −m<sup>2</sup>."}, {"kind": "blank", "p": "<b>Check-up · Q10(a–c)</b> · Divide.", "tag": "", "marks": "", "flat": [{"t": "a) (x<sup>2</sup> + 6x + 8) ÷ (x + 2) = __B1__", "a": {"B1": "x+4"}, "expr": true}, {"t": "b) (x<sup>2</sup> + 10x + 25) ÷ (x + 5) = __B1__", "a": {"B1": "x+5"}, "expr": true}, {"t": "c) (x<sup>2</sup> − 14x + 49) ÷ (x − 7) = __B1__", "a": {"B1": "x-7"}, "expr": true}], "sol": "x<sup>2</sup> ÷ x = x; left 4x + 8 = 4(x + 2): x + 4.\nx<sup>2</sup> ÷ x = x; left 5x + 25: x + 5.\nx<sup>2</sup> ÷ x = x; left −7x + 49 = −7(x − 7): x − 7."}, {"kind": "mcq", "text": "<b>Check-up · Q10(d–f)</b> · Divide:  d) (x<sup>2</sup> − 12x + 36) ÷ (x − 6)   e) (x<sup>2</sup> + 10x − 24) ÷ (x − 2)   f) (x<sup>2</sup> − 9x − 90) ÷ (x + 6)", "opts": ["d) x − 6  e) x + 12  f) x − 15", "d) x − 6  e) x + 12  f) x + 15", "d) x + 6  e) x + 12  f) x − 15", "d) x − 6  e) x − 12  f) x − 15"], "correct": 0, "tag": "", "sol": "d) (x − 6)(x − 6) = x<sup>2</sup> − 12x + 36. e) (x − 2)(x + 12) = x<sup>2</sup> + 10x − 24. f) (x + 6)(x − 15) = x<sup>2</sup> − 9x − 90."}]}, {"id": "s8", "label": "Assessment B", "sub": "Investigating patterns", "slides": [{"kind": "blank", "p": "<b>Check-up · Q11(a–e)</b> · Give the product using (x + a)(x + b) = x<sup>2</sup> + (a + b)x + ab.", "tag": "", "marks": "", "flat": [{"t": "a) (x + 10)(x − 3) = __B1__", "a": {"B1": "x^2+7x-30"}, "expr": true}, {"t": "b) (x − 3)(x − 5) = __B1__", "a": {"B1": "x^2-8x+15"}, "expr": true}, {"t": "c) (x − 9)(x + 6) = __B1__", "a": {"B1": "x^2-3x-54"}, "expr": true}, {"t": "d) (x − 7)(x + 5) = __B1__", "a": {"B1": "x^2-2x-35"}, "expr": true}, {"t": "e) (x + 7)(x − 7) = __B1__", "a": {"B1": "x^2-49"}, "expr": true}], "sol": "a + b = 7, ab = −30.\na + b = −8, ab = 15.\na + b = −3, ab = −54.\na + b = −2, ab = −35.\na + b = 0, ab = −49."}, {"kind": "blank", "p": "<b>Check-up · Q11(f–i)</b> · Give the product using (x + a)(x + b) = x<sup>2</sup> + (a + b)x + ab.", "tag": "", "marks": "", "flat": [{"t": "f) (p + a)(p + b) = __B1__", "a": {"B1": "p^2+(a+b)p+ab"}, "expr": true}, {"t": "g) (x − 3)(x + 7) = __B1__", "a": {"B1": "x^2+4x-21"}, "expr": true}, {"t": "h) (x − 8)(x − 2) = __B1__", "a": {"B1": "x^2-10x+16"}, "expr": true}, {"t": "i) (p + 3)(p − 6) = __B1__", "a": {"B1": "p^2-3p-18"}, "expr": true}], "sol": "p<sup>2</sup> + (a + b)p + ab.\na + b = 4, ab = −21.\na + b = −10, ab = 16.\na + b = −3, ab = −18."}, {"kind": "mcq", "text": "<b>Check-up · Q12(c, h)</b> · Find the products using (a + b)<sup>2</sup> = a<sup>2</sup> + 2ab + b<sup>2</sup>:  c) (x + {1/x})<sup>2</sup>   h) ({a/b} + 1)<sup>2</sup>", "opts": ["c) x<sup>2</sup> + 2 + 1/x<sup>2</sup>   h) a<sup>2</sup>/b + 2a/b + 1", "c) x<sup>2</sup> + 2x + 1/x<sup>2</sup>   h) a<sup>2</sup>/b<sup>2</sup> + 2a/b + 1", "c) x<sup>2</sup> + 2 + 1/x<sup>2</sup>   h) a<sup>2</sup>/b<sup>2</sup> + 2a/b + 1", "c) x<sup>2</sup> + 1/x<sup>2</sup>   h) a<sup>2</sup>/b<sup>2</sup> + 1"], "correct": 2, "tag": "", "sol": "c) x<sup>2</sup> + 2 × x × {1/x} + 1/x<sup>2</sup> = x<sup>2</sup> + 2 + 1/x<sup>2</sup>. h) a<sup>2</sup>/b<sup>2</sup> + 2 × {a/b} × 1 + 1 = a<sup>2</sup>/b<sup>2</sup> + 2a/b + 1."}, {"kind": "blank", "p": "<b>Check-up · Q12</b> · Find the products using (a + b)<sup>2</sup> = a<sup>2</sup> + 2ab + b<sup>2</sup>.", "tag": "", "marks": "", "flat": [{"t": "a) (2p + 4y)<sup>2</sup> = __B1__", "a": {"B1": "4p^2+16py+16y^2"}, "expr": true}, {"t": "b) (9x<sup>2</sup> + 4y<sup>2</sup>)<sup>2</sup> = __B1__", "a": {"B1": "81x^4+72x^2y^2+16y^4"}, "expr": true}, {"t": "d) (105)<sup>2</sup> = __B1__", "a": {"B1": "11025"}}, {"t": "e) (x + c)<sup>2</sup> = __B1__", "a": {"B1": "x^2+2cx+c^2"}, "expr": true}, {"t": "f) (x + y)<sup>2</sup> = __B1__", "a": {"B1": "x^2+2xy+y^2"}, "expr": true}, {"t": "g) (x + 3y)<sup>2</sup> = __B1__", "a": {"B1": "x^2+6xy+9y^2"}, "expr": true}], "sol": "4p<sup>2</sup> + 2 × 2p × 4y + 16y<sup>2</sup> = 4p<sup>2</sup> + 16py + 16y<sup>2</sup>.\n81x<sup>4</sup> + 2 × 9x<sup>2</sup> × 4y<sup>2</sup> + 16y<sup>4</sup> = 81x<sup>4</sup> + 72x<sup>2</sup>y<sup>2</sup> + 16y<sup>4</sup>.\n(100 + 5)<sup>2</sup> = 10000 + 1000 + 25 = 11025.\nx<sup>2</sup> + 2cx + c<sup>2</sup>.\nx<sup>2</sup> + 2xy + y<sup>2</sup>.\nx<sup>2</sup> + 6xy + 9y<sup>2</sup>."}, {"kind": "mcq", "text": "<b>Check-up · Q13(d, i)</b> · Find the products using (a − b)<sup>2</sup> = a<sup>2</sup> − 2ab + b<sup>2</sup>:  d) (p − {1/p})<sup>2</sup>   i) (x − {1/x})<sup>2</sup>", "opts": ["d) p<sup>2</sup> − 2 + 1/p<sup>2</sup>   i) x<sup>2</sup> − 2 + 1/x<sup>2</sup>", "d) p<sup>2</sup> − 1/p<sup>2</sup>   i) x<sup>2</sup> − 1/x<sup>2</sup>", "d) p<sup>2</sup> − 2p + 1/p<sup>2</sup>   i) x<sup>2</sup> − 2x + 1/x<sup>2</sup>", "d) p<sup>2</sup> + 2 + 1/p<sup>2</sup>   i) x<sup>2</sup> + 2 + 1/x<sup>2</sup>"], "correct": 0, "tag": "", "sol": "The middle term is 2 × p × {1/p} = 2 (and 2 × x × {1/x} = 2): p<sup>2</sup> − 2 + 1/p<sup>2</sup> and x<sup>2</sup> − 2 + 1/x<sup>2</sup>."}, {"kind": "blank", "p": "<b>Check-up · Q13</b> · Find the products using (a − b)<sup>2</sup> = a<sup>2</sup> − 2ab + b<sup>2</sup>.", "tag": "", "marks": "", "flat": [{"t": "a) (x − 4y)<sup>2</sup> = __B1__", "a": {"B1": "x^2-8xy+16y^2"}, "expr": true}, {"t": "b) (4x − 3y)<sup>2</sup> = __B1__", "a": {"B1": "16x^2-24xy+9y^2"}, "expr": true}, {"t": "c) (2xy − 1)<sup>2</sup> = __B1__", "a": {"B1": "4x^2y^2-4xy+1"}, "expr": true}, {"t": "g) (x − b)<sup>2</sup> = __B1__", "a": {"B1": "x^2-2bx+b^2"}, "expr": true}, {"t": "h) (2p − 3y)<sup>2</sup> = __B1__", "a": {"B1": "4p^2-12py+9y^2"}, "expr": true}], "sol": "x<sup>2</sup> − 8xy + 16y<sup>2</sup>.\n16x<sup>2</sup> − 24xy + 9y<sup>2</sup>.\n4x<sup>2</sup>y<sup>2</sup> − 4xy + 1.\nx<sup>2</sup> − 2bx + b<sup>2</sup>.\n4p<sup>2</sup> − 12py + 9y<sup>2</sup>."}, {"kind": "blank", "p": "<b>Check-up · Q13(e, f, j)</b> · Find the squares using (a − b)<sup>2</sup> = a<sup>2</sup> − 2ab + b<sup>2</sup>.", "tag": "", "marks": "", "flat": [{"t": "e) 98<sup>2</sup> = (100 − 2)<sup>2</sup> = __B1__", "a": {"B1": "9604"}}, {"t": "f) 390<sup>2</sup> = (400 − 10)<sup>2</sup> = __B1__", "a": {"B1": "152100"}}, {"t": "j) 59<sup>2</sup> = (60 − 1)<sup>2</sup> = __B1__", "a": {"B1": "3481"}}], "sol": "10000 − 400 + 4 = 9604.\n160000 − 8000 + 100 = 152100.\n3600 − 120 + 1 = 3481."}, {"kind": "mcq", "text": "<b>Check-up · Q14(a, b, d, g)</b> · Find the products using (a + b)(a − b) = a<sup>2</sup> − b<sup>2</sup>:  a) ({x/y} + {y/x})({x/y} − {y/x})   b) ({x/2} + 1)({x/2} − 1)   d) (p + {1/p})(p − {1/p})   g) (x + {1/x})(x − {1/x})", "opts": ["a) x<sup>2</sup>/y<sup>2</sup> + y<sup>2</sup>/x<sup>2</sup>  b) x<sup>2</sup>/4 − 1  d) p<sup>2</sup> − 1/p<sup>2</sup>  g) x<sup>2</sup> − 1/x<sup>2</sup>", "a) x<sup>2</sup>/y<sup>2</sup> − y<sup>2</sup>/x<sup>2</sup>  b) x<sup>2</sup>/2 − 1  d) p<sup>2</sup> − 1/p<sup>2</sup>  g) x<sup>2</sup> − 1/x<sup>2</sup>", "a) x<sup>2</sup>/y<sup>2</sup> − y<sup>2</sup>/x<sup>2</sup>  b) x<sup>2</sup>/4 − 1  d) p<sup>2</sup> − 1/p<sup>2</sup>  g) x<sup>2</sup> − 1/x<sup>2</sup>", "a) x<sup>2</sup>/y<sup>2</sup> − y<sup>2</sup>/x<sup>2</sup>  b) x<sup>2</sup>/4 − 1  d) p<sup>2</sup> − 2 − 1/p<sup>2</sup>  g) x<sup>2</sup> − 1/x<sup>2</sup>"], "correct": 2, "tag": "", "sol": "Square the first term and subtract the square of the second: a) x<sup>2</sup>/y<sup>2</sup> − y<sup>2</sup>/x<sup>2</sup>, b) x<sup>2</sup>/4 − 1, d) p<sup>2</sup> − 1/p<sup>2</sup>, g) x<sup>2</sup> − 1/x<sup>2</sup>."}, {"kind": "blank", "p": "<b>Check-up · Q14(c, e, f, h)</b> · Find the products using (a + b)(a − b) = a<sup>2</sup> − b<sup>2</sup>.", "tag": "", "marks": "", "flat": [{"t": "c) (x<sup>4</sup> + y<sup>4</sup>)(x<sup>4</sup> − y<sup>4</sup>) = __B1__", "a": {"B1": "x^8-y^8"}, "expr": true}, {"t": "e) (x + p)(x − p) = __B1__", "a": {"B1": "x^2-p^2"}, "expr": true}, {"t": "f) (3x − 4y)(3x + 4y) = __B1__", "a": {"B1": "9x^2-16y^2"}, "expr": true}, {"t": "h) 105 × 95 = __B1__", "a": {"B1": "9975"}}], "sol": "(x<sup>4</sup>)<sup>2</sup> − (y<sup>4</sup>)<sup>2</sup> = x<sup>8</sup> − y<sup>8</sup>.\nx<sup>2</sup> − p<sup>2</sup>.\n9x<sup>2</sup> − 16y<sup>2</sup>.\n(100 + 5)(100 − 5) = 10000 − 25 = 9975."}, {"kind": "blank", "p": "<b>Maths Lab Activity</b> · Verifying (a + b)<sup>2</sup> = a<sup>2</sup> + 2ab + b<sup>2</sup> with base-ten material (see the pieces below). To show 12<sup>2</sup> = (10 + 2)<sup>2</sup>, a hundreds square is placed on the table, tens strips are laid along two adjacent sides, and unit squares fill the empty corner. Then the same is done for 13<sup>2</sup> = (10 + 3)<sup>2</sup>.", "tag": "", "marks": "", "flat": [{"t": "12<sup>2</sup>: number of tens strips (10 × 1) placed = __B1__", "a": {"B1": "4"}}, {"t": "12<sup>2</sup>: unit squares needed to fill the corner = __B1__", "a": {"B1": "4"}}, {"t": "12<sup>2</sup>: total unit squares = 100 + 40 + 4 = __B1__", "a": {"B1": "144"}}, {"t": "13<sup>2</sup>: number of tens strips placed = __B1__", "a": {"B1": "6"}}, {"t": "13<sup>2</sup>: unit squares needed to fill the corner = __B1__", "a": {"B1": "9"}}, {"t": "13<sup>2</sup> = 100 + 60 + 9 = __B1__", "a": {"B1": "169"}}], "sol": "b = 2, so 2 strips go on each of the two adjacent sides: 2 × 2 = 4 strips (this is 2ab = 2 × 10 × 2 = 40).\nThe empty corner is 2 × 2, so 4 unit squares (b<sup>2</sup> = 2<sup>2</sup> = 4) complete the square.\n(10 + 2)<sup>2</sup> = 10<sup>2</sup> + 2 × 10 × 2 + 2<sup>2</sup> = 100 + 40 + 4 = 144.\nb = 3: 3 strips on each side, 6 strips in all (2ab = 2 × 10 × 3 = 60).\nThe corner is 3 × 3: 9 unit squares (b<sup>2</sup> = 9).\n(10 + 3)<sup>2</sup> = 100 + 60 + 9 = 169 = 13 × 13.", "fig": "<svg class=\"figsvg\" viewBox=\"0 0 320 190\" role=\"img\"><defs><marker id=\"ah\" viewBox=\"0 0 10 10\" refX=\"9\" refY=\"5\" markerWidth=\"7\" markerHeight=\"7\" orient=\"auto\"><path d=\"M0,1 L10,5 L0,9 z\" class=\"ahd\"/></marker><marker id=\"ahs\" viewBox=\"0 0 10 10\" refX=\"1\" refY=\"5\" markerWidth=\"7\" markerHeight=\"7\" orient=\"auto\"><path d=\"M10,1 L0,5 L10,9 z\" class=\"ahd\"/></marker></defs><rect class=\"sh3\" x=\"30\" y=\"120\" width=\"11\" height=\"11\"/><text class=\"al\" x=\"36.0\" y=\"152.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">1 × 1 = 1</text><text class=\"lb\" x=\"36.0\" y=\"166.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">unit square</text><rect class=\"sh3\" x=\"100\" y=\"20\" width=\"11\" height=\"110\"/><line class=\"ln\" x1=\"100.0\" y1=\"31.0\" x2=\"111.0\" y2=\"31.0\"/><line class=\"ln\" x1=\"100.0\" y1=\"42.0\" x2=\"111.0\" y2=\"42.0\"/><line class=\"ln\" x1=\"100.0\" y1=\"53.0\" x2=\"111.0\" y2=\"53.0\"/><line class=\"ln\" x1=\"100.0\" y1=\"64.0\" x2=\"111.0\" y2=\"64.0\"/><line class=\"ln\" x1=\"100.0\" y1=\"75.0\" x2=\"111.0\" y2=\"75.0\"/><line class=\"ln\" x1=\"100.0\" y1=\"86.0\" x2=\"111.0\" y2=\"86.0\"/><line class=\"ln\" x1=\"100.0\" y1=\"97.0\" x2=\"111.0\" y2=\"97.0\"/><line class=\"ln\" x1=\"100.0\" y1=\"108.0\" x2=\"111.0\" y2=\"108.0\"/><line class=\"ln\" x1=\"100.0\" y1=\"119.0\" x2=\"111.0\" y2=\"119.0\"/><text class=\"al\" x=\"106.0\" y=\"142.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">10 × 1 = 10</text><text class=\"lb\" x=\"106.0\" y=\"156.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">tens strip</text><rect class=\"sh3\" x=\"170\" y=\"20\" width=\"110\" height=\"110\"/><line class=\"ln\" x1=\"181.0\" y1=\"20.0\" x2=\"181.0\" y2=\"130.0\"/><line class=\"ln\" x1=\"192.0\" y1=\"20.0\" x2=\"192.0\" y2=\"130.0\"/><line class=\"ln\" x1=\"203.0\" y1=\"20.0\" x2=\"203.0\" y2=\"130.0\"/><line class=\"ln\" x1=\"214.0\" y1=\"20.0\" x2=\"214.0\" y2=\"130.0\"/><line class=\"ln\" x1=\"225.0\" y1=\"20.0\" x2=\"225.0\" y2=\"130.0\"/><line class=\"ln\" x1=\"236.0\" y1=\"20.0\" x2=\"236.0\" y2=\"130.0\"/><line class=\"ln\" x1=\"247.0\" y1=\"20.0\" x2=\"247.0\" y2=\"130.0\"/><line class=\"ln\" x1=\"258.0\" y1=\"20.0\" x2=\"258.0\" y2=\"130.0\"/><line class=\"ln\" x1=\"269.0\" y1=\"20.0\" x2=\"269.0\" y2=\"130.0\"/><line class=\"ln\" x1=\"170.0\" y1=\"31.0\" x2=\"280.0\" y2=\"31.0\"/><line class=\"ln\" x1=\"170.0\" y1=\"42.0\" x2=\"280.0\" y2=\"42.0\"/><line class=\"ln\" x1=\"170.0\" y1=\"53.0\" x2=\"280.0\" y2=\"53.0\"/><line class=\"ln\" x1=\"170.0\" y1=\"64.0\" x2=\"280.0\" y2=\"64.0\"/><line class=\"ln\" x1=\"170.0\" y1=\"75.0\" x2=\"280.0\" y2=\"75.0\"/><line class=\"ln\" x1=\"170.0\" y1=\"86.0\" x2=\"280.0\" y2=\"86.0\"/><line class=\"ln\" x1=\"170.0\" y1=\"97.0\" x2=\"280.0\" y2=\"97.0\"/><line class=\"ln\" x1=\"170.0\" y1=\"108.0\" x2=\"280.0\" y2=\"108.0\"/><line class=\"ln\" x1=\"170.0\" y1=\"119.0\" x2=\"280.0\" y2=\"119.0\"/><text class=\"al\" x=\"225.0\" y=\"142.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">10 × 10 = 100</text><text class=\"lb\" x=\"225.0\" y=\"156.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">hundreds square</text></svg>"}]}, {"id": "s9", "label": "Assessment C", "sub": "Communicating", "slides": [{"kind": "mcq", "text": "<b>Journal</b> · How is an algebraic expression different from a variable?", "opts": ["An expression uses only numbers and signs, while a variable uses only letters", "A variable is one letter for a number; an expression joins variables and constants with operations", "They are the same: a variable and an expression are both just letters for numbers", "A variable always has one fixed value, while an expression can change its value"], "correct": 1, "tag": "", "sol": "A variable (x) stands for an unknown number. An algebraic expression such as 3x + 5 or 2l + 2b combines variables and constants with +, −, ×, ÷. In data handling, for example, the total of n marks with mean m is the expression nm."}, {"kind": "blank", "p": "<b>Mental Maths · Q3</b> · State the degrees of the four terms of 7x<sup>3</sup>y<sup>3</sup> − 45x<sup>2</sup>y<sup>2</sup>z + 8x − 15, and the degree of the polynomial.", "tag": "", "marks": "", "flat": [{"t": "Degrees of the four terms, in order: __B1__", "a": {"B1": "6, 5, 1, 0"}, "expr": "dlist"}, {"t": "Degree of the polynomial = __B1__", "a": {"B1": "6"}}], "sol": "7x<sup>3</sup>y<sup>3</sup>: 3 + 3 = 6; −45x<sup>2</sup>y<sup>2</sup>z: 2 + 2 + 1 = 5; 8x: 1; −15: 0.\nThe highest is 6."}, {"kind": "mcq", "text": "Riya writes 3x + 4y = 7xy and 2x + 3x = 5x<sup>2</sup>. What is wrong?", "opts": ["Only the second is wrong: 3x + 4y = 7xy, but 2x + 3x = 5x", "Both are wrong: 3x + 4y stays as it is, and 2x + 3x = 5x", "Only the first is wrong: 3x + 4y = 12xy, and 2x + 3x = 5x<sup>2</sup>", "Both are right: like and unlike terms are added the same way"], "correct": 1, "tag": "", "sol": "Only like terms can be added, and adding like terms adds the coefficients but keeps the same power: 2x + 3x = 5x."}, {"kind": "blank", "p": "<b>Mental Maths · Q1</b> · If x = 2 and y = −8, find the value of (x − y)<sup>3</sup>.", "tag": "", "marks": "", "flat": [{"t": "x − y = __B1__", "a": {"B1": "10"}}, {"t": "(x − y)<sup>3</sup> = __B1__", "a": {"B1": "1000"}}], "sol": "2 − (−8) = 2 + 8 = 10.\n10<sup>3</sup> = 1000."}, {"kind": "mcq", "text": "<b>Mental Maths · Q2</b> · Find 103 × 97.", "opts": ["9900", "9991", "9909", "10009"], "correct": 1, "tag": "", "sol": "(100 + 3)(100 − 3) = 100<sup>2</sup> − 3<sup>2</sup> = 10000 − 9 = 9991."}, {"kind": "mcq", "text": "Aman says: “a ÷ a = 0 and a<sup>2</sup> ÷ a = a<sup>2</sup>.” Which correction is right?", "opts": ["a ÷ a = a and a<sup>2</sup> ÷ a = 1", "a ÷ a = 1 and a<sup>2</sup> ÷ a = a", "Both are right", "a ÷ a = 0 is right, but a<sup>2</sup> ÷ a = a"], "correct": 1, "tag": "", "sol": "Any non-zero number divided by itself is 1, and a<sup>2</sup> ÷ a = a<sup>2−1</sup> = a (Common Mistakes 6: a − a = 0, a ÷ a = 1, a<sup>2</sup> ÷ a = a)."}, {"kind": "blank", "p": "Complete the description of the first step of dividing 6a<sup>2</sup> − 7a − 5 by 2a + 1.", "tag": "", "marks": "", "flat": [{"t": "Arrange both polynomials in __B1__ order of powers (ascending / descending).", "a": {"B1": "descending"}, "expr": "words"}, {"t": "Divide the first term of the dividend by the first term of the divisor: __B1__", "a": {"B1": "3a"}, "expr": true}, {"t": "Multiply the divisor by this and subtract; the result is __B1__", "a": {"B1": "-10a-5"}, "expr": true}], "sol": "Both are written with the highest power first.\n6a<sup>2</sup> ÷ 2a = 3a.\n6a<sup>2</sup> − 7a − 5 − (6a<sup>2</sup> + 3a) = −10a − 5."}, {"kind": "mcq", "text": "Which statement is correct?", "opts": ["5 is not a polynomial because it has no variable", "x<sup>2</sup> + {1/x} is not a polynomial because 1/x = x<sup>−1</sup> has a negative power", "x<sup>2</sup> + 3x<sup>3</sup> is a trinomial because its degree is 3", "√7 xy is not a polynomial because it contains a square root"], "correct": 1, "tag": "", "sol": "A polynomial needs non-negative integer powers of the variables. 1/x = x<sup>−1</sup> breaks this. √7 is only a constant, 5 is a polynomial of degree 0, and x<sup>2</sup> + 3x<sup>3</sup> has two terms (binomial)."}, {"kind": "blank", "p": "Neha expands (a + b)<sup>2</sup> as a<sup>2</sup> + b<sup>2</sup>. Correct her work for (x + 4)<sup>2</sup>.", "tag": "", "marks": "", "flat": [{"t": "Correct expansion: (x + 4)<sup>2</sup> = __B1__", "a": {"B1": "x^2+8x+16"}, "expr": true}, {"t": "The term she left out = __B1__", "a": {"B1": "8x"}, "expr": true}], "sol": "(a + b)<sup>2</sup> = a<sup>2</sup> + 2ab + b<sup>2</sup>: x<sup>2</sup> + 2 × x × 4 + 16 = x<sup>2</sup> + 8x + 16.\nShe forgot the middle term 2ab = 8x."}, {"kind": "mcq", "text": "<b>Maths Lab Activity</b> · In step 3 of the lab activity, the hundreds square with two tens strips on each of two adjacent sides is not yet (10 + 2)<sup>2</sup>. Which explanation is correct?", "opts": ["Nothing is missing: 100 + 40 = 144", "The 2 × 2 corner is still empty: the b<sup>2</sup> = 4 unit squares are missing", "The strips should be placed on only one side, so 2ab is wrong", "The hundreds square should be 12 × 12, so a<sup>2</sup> is wrong"], "correct": 1, "tag": "", "sol": "The hundreds square is a<sup>2</sup> = 100 and the four tens strips are 2ab = 40, but the 2 × 2 corner is empty. Adding b<sup>2</sup> = 4 unit squares completes the 12 × 12 square: 100 + 40 + 4 = 144. So (a + b)<sup>2</sup> = a<sup>2</sup> + 2ab + b<sup>2</sup>, not a<sup>2</sup> + 2ab and not a<sup>2</sup> + b<sup>2</sup>."}]}, {"id": "s10", "label": "Assessment D", "sub": "Applying mathematics in real-life contexts", "slides": [{"kind": "blank", "p": "<b>Check-up · Q3</b> · Find the perimeter of each triangle whose sides are given.", "tag": "", "marks": "", "flat": [{"t": "a) 2x + 3y + 3z, 4x − 4y + 2z, 6x + y − 2z → __B1__", "a": {"B1": "12x+3z"}, "expr": true}, {"t": "b) 7x<sup>2</sup> + 6x + 3, 8x<sup>2</sup> − 4x + 7, 6x<sup>2</sup> − 4x + 9 → __B1__", "a": {"B1": "21x^2-2x+19"}, "expr": true}], "sol": "x: 2 + 4 + 6 = 12; y: 3 − 4 + 1 = 0; z: 3 + 2 − 2 = 3. Perimeter 12x + 3z.\nx<sup>2</sup>: 7 + 8 + 6 = 21; x: 6 − 4 − 4 = −2; constants 3 + 7 + 9 = 19."}, {"kind": "mcq", "text": "<b>Check-up · Q4</b> · How much is 4x<sup>2</sup> − 3x + 5 smaller than 7 + 5x<sup>2</sup> − 3x?", "opts": ["x<sup>2</sup> + 2", "−x<sup>2</sup> − 2", "x<sup>2</sup> − 6x + 2", "9x<sup>2</sup> − 6x + 12"], "correct": 0, "tag": "", "sol": "(7 + 5x<sup>2</sup> − 3x) − (4x<sup>2</sup> − 3x + 5) = x<sup>2</sup> + 0x + 2 = x<sup>2</sup> + 2."}, {"kind": "blank", "p": "<b>Check-up · Q15</b> · (32x<sup>2</sup> − 16x + 48) kilograms of sugar is stored in 8 bags in equal quantities. How many kilograms of sugar are there in each bag?", "tag": "", "marks": "", "flat": [{"t": "Sugar in each bag = __B1__ kg", "a": {"B1": "4x^2-2x+6"}, "expr": true}], "sol": "Divide each term by 8: 4x<sup>2</sup> − 2x + 6 kg."}, {"kind": "mcq", "text": "<b>Check-up · Q16</b> · If (x − 5) notebooks cost ₹ (x<sup>2</sup> − 13x + 40), what is the cost of one notebook?", "opts": ["x − 8", "x − 13", "x − 5", "x + 8"], "correct": 0, "tag": "", "sol": "(x<sup>2</sup> − 13x + 40) ÷ (x − 5): x<sup>2</sup> ÷ x = x, left −8x + 40 = −8(x − 5). One notebook costs ₹ (x − 8)."}, {"kind": "mcq", "text": "<b>Check-up · Q17(a)</b> · A worker is paid ₹ m per hour, and twice the normal pay for every hour of overtime. Mayank works 8 hours a day plus 2 hours of overtime, for 26 days. Which polynomial gives his monthly wage?", "opts": ["₹ 312m", "₹ 260m", "₹ 364m", "₹ 208m"], "correct": 0, "tag": "", "sol": "One day: 8 × m + 2 × 2m = 12m. For 26 days: 26 × 12m = 312m."}, {"kind": "blank", "p": "<b>Check-up · Q17(b)</b> · (Same case study: 8 normal hours and 2 overtime hours a day, for 26 days.) If the hourly pay is ₹ 100, find his total earnings for the month.", "tag": "", "marks": "", "flat": [{"t": "Total earnings = ₹ __B1__", "a": {"B1": "31200"}}], "sol": "Monthly wage = 26 × (8m + 2 × 2m) = 312m; with m = 100: 312 × 100 = ₹ 31,200."}, {"kind": "blank", "p": "<b>Check-up · Creative Thinking</b> · A webpage is 2m inches wide and m inches high. A pop-up advertisement of height 3.5 inches runs across the top; below it, on the right, is a research menu 4 inches wide. Give an expression for the area of the webpage excluding the advertisement and the menu.", "tag": "", "marks": "", "flat": [{"t": "Height of the remaining part = __B1__ inches", "a": {"B1": "m-3.5"}, "expr": true}, {"t": "Width of the remaining part = __B1__ inches", "a": {"B1": "2m-4"}, "expr": true}, {"t": "Area = __B1__ sq. inches", "a": {"B1": "2m^2-11m+14"}, "expr": true}], "sol": "m − 3.5 (the pop-up takes 3.5 inches of the height).\n2m − 4 (the menu takes 4 inches of the width).\n(2m − 4)(m − 3.5) = 2m<sup>2</sup> − 7m − 4m + 14 = 2m<sup>2</sup> − 11m + 14.", "fig": "<svg class=\"figsvg\" viewBox=\"0 0 320 190\" role=\"img\"><defs><marker id=\"ah\" viewBox=\"0 0 10 10\" refX=\"9\" refY=\"5\" markerWidth=\"7\" markerHeight=\"7\" orient=\"auto\"><path d=\"M0,1 L10,5 L0,9 z\" class=\"ahd\"/></marker><marker id=\"ahs\" viewBox=\"0 0 10 10\" refX=\"1\" refY=\"5\" markerWidth=\"7\" markerHeight=\"7\" orient=\"auto\"><path d=\"M10,1 L0,5 L10,9 z\" class=\"ahd\"/></marker></defs><rect class=\"sh3\" x=\"40\" y=\"20\" width=\"250\" height=\"150\"/><line class=\"ln\" x1=\"40.0\" y1=\"62.0\" x2=\"290.0\" y2=\"62.0\"/><line class=\"ln\" x1=\"210.0\" y1=\"62.0\" x2=\"210.0\" y2=\"170.0\"/><text class=\"lb\" x=\"100.0\" y=\"41.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">Pop-up</text><text class=\"lb\" x=\"250.0\" y=\"148.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">Research</text><line class=\"ln\" x1=\"274.0\" y1=\"24.0\" x2=\"274.0\" y2=\"58.0\" marker-end=\"url(#ah)\" marker-start=\"url(#ahs)\"/><text class=\"al\" x=\"256.0\" y=\"41.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">3.5</text><line class=\"ln\" x1=\"214.0\" y1=\"92.0\" x2=\"286.0\" y2=\"92.0\" marker-end=\"url(#ah)\" marker-start=\"url(#ahs)\"/><text class=\"al\" x=\"250.0\" y=\"80.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">4</text><text class=\"al\" x=\"24.0\" y=\"95.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">m</text><text class=\"al\" x=\"165.0\" y=\"184.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">2m</text></svg>"}, {"kind": "mcq", "text": "<b>Check-up · Everyday Maths</b> · A wall is (6p + 2) by 5p. It has a door 2p by 4p and a window 3p by p. Which expression gives the area of the wall to be painted?", "opts": ["19p<sup>2</sup> + 2", "19p<sup>2</sup> + 10p", "41p<sup>2</sup> + 10p", "30p<sup>2</sup> + 10p"], "correct": 1, "tag": "", "sol": "Wall = 5p(6p + 2) = 30p<sup>2</sup> + 10p. Door = 8p<sup>2</sup>, window = 3p<sup>2</sup>. Painted area = 30p<sup>2</sup> + 10p − 8p<sup>2</sup> − 3p<sup>2</sup> = 19p<sup>2</sup> + 10p.", "fig": "<svg class=\"figsvg\" viewBox=\"0 0 330 200\" role=\"img\"><defs><marker id=\"ah\" viewBox=\"0 0 10 10\" refX=\"9\" refY=\"5\" markerWidth=\"7\" markerHeight=\"7\" orient=\"auto\"><path d=\"M0,1 L10,5 L0,9 z\" class=\"ahd\"/></marker><marker id=\"ahs\" viewBox=\"0 0 10 10\" refX=\"1\" refY=\"5\" markerWidth=\"7\" markerHeight=\"7\" orient=\"auto\"><path d=\"M10,1 L0,5 L10,9 z\" class=\"ahd\"/></marker></defs><rect class=\"sh3\" x=\"30\" y=\"30\" width=\"260\" height=\"150\"/><line class=\"ln\" x1=\"30.0\" y1=\"16.0\" x2=\"290.0\" y2=\"16.0\" marker-end=\"url(#ah)\" marker-start=\"url(#ahs)\"/><text class=\"al\" x=\"160.0\" y=\"6.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">6p + 2</text><line class=\"ln\" x1=\"304.0\" y1=\"30.0\" x2=\"304.0\" y2=\"180.0\" marker-end=\"url(#ah)\" marker-start=\"url(#ahs)\"/><text class=\"al\" x=\"316.0\" y=\"105.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">5p</text><rect class=\"cell\" x=\"70\" y=\"76\" width=\"52\" height=\"104\"/><text class=\"lb\" x=\"96.0\" y=\"66.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">Door</text><text class=\"al\" x=\"56.0\" y=\"128.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">4p</text><text class=\"al\" x=\"96.0\" y=\"192.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">2p</text><rect class=\"cell\" x=\"180\" y=\"70\" width=\"78\" height=\"26\"/><text class=\"lb\" x=\"219.0\" y=\"110.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">Window</text><text class=\"al\" x=\"219.0\" y=\"60.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">3p</text><text class=\"al\" x=\"268.0\" y=\"83.0\" text-anchor=\"middle\" dominant-baseline=\"middle\">p</text></svg>"}, {"kind": "blank", "p": "<b>Unit II · Let's Solve · Q1, Q2</b> · Fit India: on Day 1 Yusuf's tracker showed twice Neha's steps. On Day 2 Yusuf took {3/4} of Neha's Day 1 steps, and Neha took 1000 more than Yusuf's Day 1 steps. On Day 3 Yusuf took 1500 more steps than on Day 1, and Neha took twice her Day 2 steps. Let Neha's steps on Day 1 be x.", "tag": "", "marks": "", "flat": [{"t": "Q1) Yusuf's total steps for the 3 days = __B1__", "a": {"B1": "19x/4+1500"}, "expr": true}, {"t": "Q2) Yusuf took 20,500 steps in all, so x = __B1__", "a": {"B1": "4000"}}, {"t": "Yusuf's steps on Days 1, 2, 3 (in order, separated by commas): __B1__", "a": {"B1": "8000, 3000, 9500"}, "expr": "dlist"}, {"t": "Neha's steps on Days 1, 2, 3 (in order, separated by commas): __B1__", "a": {"B1": "4000, 9000, 18000"}, "expr": "dlist"}], "sol": "Day 1: 2x; Day 2: {3/4}x; Day 3: 2x + 1500. Total = 2x + {3/4}x + 2x + 1500 = {19/4}x + 1500.\n{19/4}x + 1500 = 20500 → {19/4}x = 19000 → x = 19000 × {4/19} = 4000.\nDay 1: 2 × 4000 = 8000; Day 2: {3/4} × 4000 = 3000; Day 3: 8000 + 1500 = 9500 (8000 + 3000 + 9500 = 20500 ✓).\nDay 1: 4000; Day 2: 8000 + 1000 = 9000; Day 3: 2 × 9000 = 18000."}, {"kind": "mcq", "text": "<b>Unit II · Let's Solve · Q3</b> · (Same story, Neha's Day 1 steps = x, so her Day 2 steps = 2x + 1000.) At the end of the month Neha's steps equal her Day 2 steps raised to the power 2. Which expression, found with an identity, gives this?", "opts": ["4x<sup>2</sup> + 2000x + 1000000", "4x<sup>2</sup> + 4000x + 1000000", "4x<sup>2</sup> + 1000000", "2x<sup>2</sup> + 4000x + 1000000"], "correct": 1, "tag": "", "sol": "Use (a + b)<sup>2</sup> = a<sup>2</sup> + 2ab + b<sup>2</sup> with a = 2x, b = 1000: (2x)<sup>2</sup> + 2 × 2x × 1000 + 1000<sup>2</sup> = 4x<sup>2</sup> + 4000x + 1000000. (With x = 4000: 9000<sup>2</sup> = 81,000,000.)"}]}];
/* ================= build slide lists ================= */
var SLIDES = {}; SECTIONS.forEach(function(sec){ SLIDES[sec.id]=sec.slides; });
var TAB_DEFS = SECTIONS.map(function(sec){ return {id:sec.id, label:sec.label, sub:sec.sub}; });

/* ================= state ================= */
function blankItem(slide){
  if(slide.kind==='mcq'||slide.kind==='ar'){
    return {status:'unanswered', attempts:0, choice:undefined};
  }
  return {status:'unanswered', curStep:0, stepStates: slide.flat.map(function(){ return {status:'unanswered', attempts:0, inputs:{}}; })};
}
function defaultState(){
  var s={tabs:{}};
  TAB_DEFS.forEach(function(td){
    s.tabs[td.id] = { idx:0, maxReached:0, items: SLIDES[td.id].map(function(sl){ return blankItem(sl); }) };
  });
  return s;
}
var appState = {mode:null, learning:null, quiz:null};
var state = null;      // alias for appState[appState.mode]
var MODE = null;
var activeTab=TAB_DEFS[0].id;

function setMode(m){
  appState.mode = m;
  if(!appState[m]) appState[m] = defaultState();
  state = appState[m];
  MODE = m;
}
/* ================= student accounts (saved on this device) ================= */
var SHEET_KEY='sopaan-c8-ch7';
var ACC_KEY='sopaan-students-v1';
var storageOK=true;
var MEM={};
function lsGet(k){ var r=null; try{ r=localStorage.getItem(k); }catch(e){ storageOK=false; }
  if(r===null||r===undefined) r=MEM[k]||null; try{ return r?JSON.parse(r):null; }catch(e){ return null; } }
function lsSet(k,v){ var j=JSON.stringify(v); MEM[k]=j; try{ localStorage.setItem(k,j); return true; }catch(e){ storageOK=false; return false; } }
try{ localStorage.setItem('sopaan-probe','1'); localStorage.removeItem('sopaan-probe'); }catch(e){ storageOK=false; }
function hashPin(pin,salt){ var h=2166136261, str=salt+'|'+pin; for(var i=0;i<str.length;i++){ h^=str.charCodeAt(i); h=Math.imul(h,16777619)>>>0; } return h.toString(36); }
function accKey(name,roll){ return (name.trim().toLowerCase().replace(/\s+/g,' ')+'#'+roll.trim().toLowerCase()); }
function accounts(){ return lsGet(ACC_KEY)||{students:{}}; }
var student=null; // {key,name,roll}
var records=[];   // finished-tab history for this student on this sheet
function progKey(){ return SHEET_KEY+'::'+student.key; }

function loadState(){
  appState = {mode:null, learning:null, quiz:null}; records=[]; activeTab=TAB_DEFS[0].id;
  var saved=lsGet(progKey());
  if(!saved) return;
  try{
    ['learning','quiz'].forEach(function(m){
      if(saved[m] && saved[m].tabs){
        var fresh = defaultState();
        TAB_DEFS.forEach(function(td){
          if(saved[m].tabs[td.id] && saved[m].tabs[td.id].items && saved[m].tabs[td.id].items.length===SLIDES[td.id].length){
            fresh.tabs[td.id] = saved[m].tabs[td.id];
          }
        });
        appState[m] = fresh;
      }
    });
    if(saved.mode==='learning' || saved.mode==='quiz') appState.mode = saved.mode;
    if(saved.activeTab && TAB_DEFS.some(function(t){ return t.id===saved.activeTab; })) activeTab = saved.activeTab;
    if(Array.isArray(saved.records)) records = saved.records;
  }catch(e){}
}
function saveState(){
  if(!student) return;
  lsSet(progKey(), {mode:appState.mode, learning:appState.learning, quiz:appState.quiz, activeTab:activeTab, records:records, updated:Date.now()});
  var acc=accounts(); if(acc.students[student.key]){ acc.students[student.key].last=Date.now(); lsSet(ACC_KEY,acc); }
}
function addRecord(mode, tabId, correct, revealed, skipped, total){
  records.unshift({at:Date.now(), mode:mode, tab:tabId, correct:correct, revealed:revealed, skipped:skipped, total:total});
  if(records.length>60) records.length=60;
  saveState();
}
function fmtDate(ms){ try{ return new Date(ms).toLocaleString(undefined,{day:'numeric',month:'short',hour:'2-digit',minute:'2-digit'}); }catch(e){ return ''; } }

function renderWho(){
  var el=document.getElementById('whoBar');
  if(!student){ el.hidden=true; el.innerHTML=''; return; }
  el.hidden=false;
  el.innerHTML='Signed in as <b>'+esc(student.name)+'</b> · Roll '+esc(student.roll)+
    ' <button id="btnRecord">My record</button> <button id="btnSignOut">Sign out</button>';
  document.getElementById('btnRecord').addEventListener('click', renderRecord);
  document.getElementById('btnSignOut').addEventListener('click', signOut);
}
function signOut(){
  saveState(); student=null; state=null; MODE=null;
  var acc=accounts(); delete acc.current; lsSet(ACC_KEY,acc);
  document.getElementById('modePill').hidden=true;
  renderWho(); renderLogin();
}
function signIn(key){
  var acc=accounts(); var st=acc.students[key]; if(!st) return;
  student={key:key, name:st.name, roll:st.roll};
  acc.current=key; st.last=Date.now(); lsSet(ACC_KEY,acc);
  loadState(); renderWho();
  if(appState.mode==='learning' || appState.mode==='quiz'){
    setMode(appState.mode); document.getElementById('modePill').hidden=false; updateModePill();
    showChrome(true); buildTabbar(); renderSlide();
    showToast('Welcome back, '+st.name.split(' ')[0]+'. Picking up where you left off.');
  } else {
    renderModePicker();
  }
}
function renderLogin(msg){
  showChrome(false);
  var acc=accounts(); var keys=Object.keys(acc.students).sort(function(a,b){ return (acc.students[b].last||0)-(acc.students[a].last||0); });
  var h='<div class="login-card"><h2>Student sign-in</h2>'+
    '<p class="lead">Sign in to save your answers, see your record and continue where you left off next time.</p>';
  if(!storageOK) h+='<div class="login-err">This browser is blocking saved data (for example, a private window). You can still practise, but progress will not be kept after you close the page.</div>';
  if(msg) h+='<div class="login-err">'+esc(msg)+'</div>';
  if(keys.length){
    h+='<div class="known"><span class="known-label">Continue as</span>';
    keys.slice(0,6).forEach(function(k){ var st=acc.students[k];
      h+='<button class="known-btn" data-k="'+esc(k)+'"><span>'+esc(st.name)+' <small>· Roll '+esc(st.roll)+'</small></span><small>'+(st.last?'Last active '+fmtDate(st.last):'')+'</small></button>'; });
    h+='</div>';
  }
  h+='<form id="loginForm" novalidate>'+
    '<div class="fld"><label for="lgName">Full name</label><input id="lgName" autocomplete="name" required></div>'+
    '<div class="fld-row"><div class="fld"><label for="lgRoll">Roll no.</label><input id="lgRoll" required></div>'+
    '<div class="fld"><label for="lgPin">4-digit PIN</label><input id="lgPin" type="password" inputmode="numeric" maxlength="4" autocomplete="off" required></div></div>'+
    '<button class="btn btn-primary" type="submit" style="width:100%;">Sign in</button>'+
    '<p class="login-note">New here? Enter your name, roll no. and a PIN you will remember, and your profile is created. Progress is saved on this device, so use the same device and browser to continue.</p>'+
    '</form></div>';
  var wrap=document.getElementById('wrap'); wrap.innerHTML=h;
  wrap.querySelectorAll('.known-btn').forEach(function(b){
    b.addEventListener('click', function(){
      var st=accounts().students[b.dataset.k];
      document.getElementById('lgName').value=st.name; document.getElementById('lgRoll').value=st.roll;
      document.getElementById('lgPin').focus();
    });
  });
  document.getElementById('loginForm').addEventListener('submit', function(e){
    e.preventDefault();
    var name=document.getElementById('lgName').value.trim(), roll=document.getElementById('lgRoll').value.trim(), pin=document.getElementById('lgPin').value.trim();
    if(!name||!roll){ renderLoginErr('Enter your name and roll no.'); return; }
    if(!/^\d{4}$/.test(pin)){ renderLoginErr('Your PIN must be exactly 4 digits.'); return; }
    var k=accKey(name,roll); var acc=accounts();
    if(acc.students[k]){
      if(acc.students[k].pin!==hashPin(pin,k)){ renderLoginErr('That PIN does not match this name and roll no. Try again.'); return; }
    } else {
      acc.students[k]={name:name.replace(/\s+/g,' '), roll:roll, pin:hashPin(pin,k), created:Date.now()};
      lsSet(ACC_KEY,acc);
    }
    signIn(k);
  });
}
function renderLoginErr(m){
  var n=document.getElementById('lgName').value, r=document.getElementById('lgRoll').value;
  renderLogin(m); document.getElementById('lgName').value=n; document.getElementById('lgRoll').value=r; document.getElementById('lgPin').focus();
}
function tabSummary(m){
  var st=appState[m]; if(!st) return null;
  return TAB_DEFS.map(function(td){
    var items=st.tabs[td.id].items, n=items.length;
    var c=items.filter(function(i){return i.status==='correct';}).length;
    var done=items.filter(function(i){return i.status!=='unanswered';}).length;
    return {label:td.label, n:n, done:done, correct:c};
  });
}
function renderRecord(){
  showChrome(false);
  var tabLabel=function(id){ var t=TAB_DEFS.find(function(x){return x.id===id;}); return t?t.label:id; };
  var h='<div class="rec-card"><h2>'+esc(student.name)+'’s record</h2><p class="rec-empty" style="margin:0 0 12px;">Roll '+esc(student.roll)+' · Algebraic Expressions and Identities</p>';
  ['learning','quiz'].forEach(function(m){
    var sum=tabSummary(m);
    h+='<h3>'+(m==='learning'?'📘 Learning Sheet':'📝 Quiz Mode')+'</h3>';
    if(!sum){ h+='<p class="rec-empty">Not started yet.</p>'; return; }
    h+='<div class="rec-table-wrap"><table class="rec-table"><thead><tr><th>Section</th><th>Progress</th><th>Correct first time</th></tr></thead><tbody>';
    sum.forEach(function(r){ var pct=Math.round(r.done/r.n*100);
      h+='<tr><td>'+r.label+'</td><td><span class="rec-bar"><i style="width:'+pct+'%"></i></span>'+r.done+' / '+r.n+'</td><td>'+(m==='quiz'?'—':r.correct+' / '+r.n)+'</td></tr>'; });
    h+='</tbody></table></div>';
  });
  h+='</div><div class="rec-card"><h3>Finished sections</h3>';
  if(!records.length){ h+='<p class="rec-empty">No sections finished yet. Each time you finish a tab, your score is recorded here.</p>'; }
  else {
    h+='<div class="rec-table-wrap"><table class="rec-table"><thead><tr><th>When</th><th>Mode</th><th>Section</th><th>Score</th></tr></thead><tbody>';
    records.forEach(function(r){ h+='<tr><td>'+fmtDate(r.at)+'</td><td>'+(r.mode==='quiz'?'Quiz':'Learning')+'</td><td>'+tabLabel(r.tab)+'</td><td>'+r.correct+' / '+r.total+(r.mode==='learning'?' <span class="rec-empty">('+r.revealed+' revealed, '+r.skipped+' skipped)</span>':'')+'</td></tr>'; });
    h+='</tbody></table></div>';
  }
  h+='</div><button class="btn btn-primary" id="btnBack">'+(MODE?'Back to practice':'Choose a mode')+'</button>';
  document.getElementById('wrap').innerHTML=h;
  document.getElementById('btnBack').addEventListener('click', function(){
    if(MODE){ showChrome(true); buildTabbar(); renderSlide(); } else renderModePicker();
  });
  window.scrollTo({top:0});
}

/* ================= tab bar ================= */
function buildTabbar(){
  var el=document.getElementById('tabbar');
  el.innerHTML = '<button class="tab-btn'+(activeTab==='theory'?' active':'')+'" data-tab="theory">Theory<span class="tab-count">notes</span></button>' + TAB_DEFS.map(function(t){
    return '<button class="tab-btn'+(t.id===activeTab?' active':'')+'" data-tab="'+t.id+'">'+t.label+'<span class="tab-count">'+SLIDES[t.id].length+'</span></button>';
  }).join('') + '<button class="tab-btn'+(activeTab==='report'?' active':'')+'" data-tab="report">📊 Report<span class="tab-count">pie</span></button>';
  el.querySelectorAll('.tab-btn').forEach(function(btn){
    btn.addEventListener('click', function(){ activeTab=btn.dataset.tab; buildTabbar(); renderSlide(); window.scrollTo({top:0,behavior:'smooth'}); });
  });
}

/* ================= rendering ================= */
function canProceed(item){ return item.status==='correct'||item.status==='revealed'||item.status==='skipped'; }

function renderSlide(){
  if(!state.tabs[activeTab]){ activeTab=TAB_DEFS[0].id; }
  var ts = state.tabs[activeTab];
  var slides = SLIDES[activeTab];
  if(ts.idx>=slides.length||ts.idx<0) ts.idx=0;
  var idx = ts.idx;
  var slide = slides[idx];
  var item = ts.items[idx];

  var tdef=TAB_DEFS.find(function(t){return t.id===activeTab;});
  document.getElementById('spLabel').textContent = tdef.label+' · Question '+(idx+1)+' of '+slides.length;
  document.getElementById('secSub').textContent = tdef.label+' — '+tdef.sub;
  document.getElementById('spFill').style.width = Math.round(((idx)/(Math.max(slides.length-1,1)))*100)+'%';

  var h='<div class="qcard">';
  if(slide.kind==='mcq' || slide.kind==='ar'){
    h += renderChoiceBody(slide, item, idx);
  } else {
    h += renderBlankBody(slide, item, idx);
  }
  h += '<div class="feedback" id="feedbackBox"></div>';
  if(MODE==='learning' && (item.status==='correct'||item.status==='revealed')) h += solutionHTML(slide);
  h += '</div>';

  document.getElementById('wrap').innerHTML = h;
  wireSlideEvents(slide, item, idx);
  restoreFeedback(item);
  renderNavbar(item);
  updateFab();
  saveState();
}

function solutionHTML(slide){
  if(!slide.sol) return '';
  return '<div class="solution"><div class="sol-h">Solution</div>'+slide.sol.split('\n').map(function(l){ return '<div class="sol-line">'+fr(esc(l))+'</div>'; }).join('')+'</div>';
}
var LETTERS=['a','b','c','d','e','f'];
function chosenHTML(slide,item){
  var opts = slide.kind==='mcq' ? slide.opts : AR_OPTIONS;
  if(item.choice===undefined) return '';
  var ok=item.choice===slide.correct;
  var h='<div class="chosen '+(ok?'ok':'bad')+'"><b>Your answer:</b> ('+LETTERS[item.choice]+') '+fr(esc(opts[item.choice]))+(ok?' ✓':' ✗')+'</div>';
  if(!ok) h+='<div class="chosen ok"><b>Correct answer:</b> ('+LETTERS[slide.correct]+') '+fr(esc(opts[slide.correct]))+'</div>';
  return h;
}
function renderChoiceBody(slide, item, idx){
  var h='<div class="qhead"><div class="qnum">'+(idx+1)+'</div>';
  if(slide.kind==='mcq'){
    h += '<div class="qtext">'+fr(esc(slide.text))+(slide.tag?'<span class="qtag">'+esc(slide.tag)+'</span>':'')+'</div>';
  } else {
    h += '<div class="qtext"><span class="qtag" style="margin-left:0;margin-right:6px;">A / R</span>Assertion (A): '+fr(esc(slide.a))+'<br>Reason (R): '+fr(esc(slide.r))+(slide.tag?'<span class="qtag">'+esc(slide.tag)+'</span>':'')+'</div>';
  }
  h += '</div>';
  if(slide.fig) h += '<div class="fig">'+slide.fig+'</div>';
  var opts = slide.kind==='mcq' ? slide.opts : AR_OPTIONS;
  if(MODE==='quiz') h += '<div class="quiz-hint">Quiz mode — pick an option. The correct answer is revealed once you finish this tab.</div>';
  var locked = MODE==='learning' && (item.status==='correct' || item.status==='revealed');
  h += '<div class="options">';
  opts.forEach(function(opt,i){
    var cls='opt';
    if(locked){
      if(i===slide.correct) cls+=' is-correct';
      else if(item.choice===i) cls+=' is-wrong';
      cls+=' locked';
    }
    if(item.choice===i) cls+=' is-chosen';
    h += '<label class="'+cls+'"><input type="radio" name="choice" value="'+i+'" '+(item.choice===i?'checked':'')+' '+(locked?'disabled':'')+'> <span class="opt-l">('+LETTERS[i]+')</span> <span class="opt-t">'+fr(esc(opt))+'</span>'+(item.choice===i?'<span class="opt-tag">'+(locked?(i===slide.correct?'Your answer ✓':'Your answer ✗'):'Selected')+'</span>':'')+'</label>';
  });
  h += '</div>';
  if(locked) h += chosenHTML(slide,item);
  return h;
}

function renderBlankBody(slide, item, idx){
  var h='<div class="qhead"><div class="qnum">'+(idx+1)+'</div><div class="qtext">';
  if(slide.kind==='case'){ h += '<b>'+esc(slide.title)+'.</b> '+esc(slide.body); }
  else { var pp=fr(esc(slide.p)).split('\n'); h += pp[0]+pp.slice(1).map(function(x){return '<span class="datline">'+x+'</span>';}).join(''); }
  h += (slide.tag?'<span class="qtag">'+esc(slide.tag)+'</span>':'')+'</div>';
  if(slide.marks) h += '<div class="marks-pill">'+slide.marks+'</div>';
  h += '</div>';
  if(slide.fig) h += '<div class="fig">'+slide.fig+'</div>';

  var total = slide.flat.length;
  var hasExpr = slide.flat.some(function(s){ return s.expr===true; });
  var hasFrac = slide.flat.some(function(s){ return ['fv','fe','fl','fm','fi','flist'].indexOf(s.expr)>=0; });
  var blankCount=0; slide.flat.forEach(function(s){ blankCount+=Object.keys(s.a).length; });

  if(MODE==='quiz'){
    h += '<div class="step-badge">'+blankCount+' blank'+(blankCount===1?'':'s')+' in this question</div>';
    h += '<div class="quiz-hint">Quiz mode — fill in what you can. Correct answers are revealed once you finish this tab.</div>';
    if(hasFrac) h += '<div class="quiz-hint">Type fractions like <b>3/4</b> and mixed numbers like <b>2 3/4</b> (whole number, space, fraction).</div>';
    if(hasExpr) h += '<div class="quiz-hint">Type answers like <b>2x-5</b>, <b>x^2-4</b> or <b>3+2i</b>. Use ^ for powers, | | for absolute value and pi for π. Any equivalent form is accepted.</div>';
    h += '<div class="steps">';
    for(var qi=0; qi<total; qi++){
      var qstep = slide.flat[qi];
      var qss = item.stepStates[qi];
      if(qstep.partLabel) h += '<div class="subpart-label">'+esc(qstep.partLabel)+'</div>';
      if(qstep.orDivider) h += '<div class="or-divider">OR</div>';
      var qline = fr(qstep.t);
      Object.keys(qstep.a).forEach(function(bkey){
        var val = qss.inputs[bkey]||'';
        var inp='<input class="blank-input'+(['fv','fe','fl','fm','fi','dec'].indexOf(qstep.expr)>=0?' fr':(qstep.expr==='flist'||qstep.expr==='dlist'||qstep.expr==='glist')?' wide':qstep.expr===true?' expr':(qstep.expr==='words'||qstep.expr==='list'||qstep.expr==='expanded'||qstep.expr==='set'||qstep.expr==='primes'||qstep.expr==='trans'||qstep.expr==='rot'?' wide':''))+'" data-step="'+qi+'" data-bkey="'+bkey+'" value="'+esc(val)+'">';
        qline = qline.replace('__'+bkey+'__', inp);
      });
      if(qstep.fig) h += '<div class="fig">'+qstep.fig+'</div>';
      h += '<div class="step-line">'+qline+'</div>';
    }
    h += '</div>';
    return h;
  }

  if(hasFrac) h += '<div class="quiz-hint">Type fractions like <b>3/4</b> and mixed numbers like <b>2 3/4</b> (whole number, space, fraction).</div>';
  if(hasExpr) h += '<div class="quiz-hint">Type answers like <b>2x-5</b>, <b>x^2-4</b> or <b>3+2i</b>. Use ^ for powers, | | for absolute value and pi for π. Any equivalent form is accepted.</div>';
  var locked = item.status==='correct' || item.status==='revealed';
  var upto = locked ? total-1 : item.curStep;
  h += '<div class="step-badge">Step '+(Math.min(item.curStep,total-1)+1)+' of '+total+'</div>';
  h += '<div class="steps">';
  for(var i=0;i<=upto;i++){
    var step = slide.flat[i];
    var ss = item.stepStates[i];
    if(step.partLabel) h += '<div class="subpart-label">'+esc(step.partLabel)+'</div>';
    if(step.orDivider) h += '<div class="or-divider">OR</div>';
    var resolved = ss.status==='correct' || ss.status==='revealed';
    var line = fr(step.t);
    Object.keys(step.a).forEach(function(bkey){
      var fs = ss.inputs['fs_'+bkey];
      var cls = fs==='correct'?'is-correct':(fs==='wrong'?'is-wrong':'');
      var val = ss.inputs[bkey]||'';
      var dis = resolved ? 'disabled':'';
      var inp='<input class="blank-input '+cls+(['fv','fe','fl','fm','fi','dec'].indexOf(step.expr)>=0?' fr':(step.expr==='flist'||step.expr==='dlist'||step.expr==='glist')?' wide':step.expr===true?' expr':(step.expr==='words'||step.expr==='list'||step.expr==='expanded'||step.expr==='set'||step.expr==='primes'||step.expr==='trans'||step.expr==='rot'?' wide':''))+'" data-step="'+i+'" data-bkey="'+bkey+'" value="'+esc(val)+'" '+dis+'>';
      line = line.replace('__'+bkey+'__', inp);
    });
    if(step.fig) h += '<div class="fig">'+step.fig+'</div>';
    h += '<div class="step-line'+(resolved?' resolved':'')+'">'+line+'</div>';
    if(ss.status==='revealed'){
      var reveals=[];
      Object.keys(step.a).forEach(function(bkey){ reveals.push(bkey+' = '+esc(step.a[bkey])); });
      h += '<div class="reveal-note">correct: '+reveals.join(', ')+'</div>';
    }
  }
  h += '</div>';
  return h;
}

var __flash=null;
function restoreFeedback(item){
  var fb=document.getElementById('feedbackBox'); if(!fb) return;
  if(__flash){ fb.className='feedback show '+__flash.c; fb.innerHTML=__flash.h; __flash=null; return; }
  if(MODE==='quiz'){ fb.className='feedback'; fb.innerHTML=''; return; }
  if(item.status==='correct'){ fb.className='feedback show ok'; fb.innerHTML='<b>All done — correct!</b>'; }
  else if(item.status==='revealed'){ fb.className='feedback show reveal'; fb.innerHTML='<b>Answer revealed above.</b> Move on whenever you’re ready.'; }
  else if(item.status==='skipped'){ fb.className='feedback show retry'; fb.innerHTML='Skipped — you can answer it now and press <b>Check</b>, or come back later from the Question Palette.'; }
  else { fb.className='feedback'; fb.innerHTML=''; }
}

function slideIsAnswered(slide,item){
  if(slide.kind==='mcq'||slide.kind==='ar') return item.choice!==undefined;
  return item.stepStates.some(function(ss){ return Object.keys(ss.inputs).some(function(k){ return k.indexOf('fs_')!==0 && ss.inputs[k] && String(ss.inputs[k]).trim()!==''; }); });
}
function renderNavbar(item){
  var ts = state.tabs[activeTab];
  var slides = SLIDES[activeTab];
  var slide = slides[ts.idx];
  var isLast = ts.idx === slides.length-1;
  var h='';
  h += '<button class="btn" id="btnPrev" '+(ts.idx===0?'disabled':'')+'>&larr; Previous</button>';

  if(MODE==='quiz'){
    h += '<button class="btn" id="btnSkip">Skip</button>';
    h += '<span class="spacer"></span>';
    h += '<button class="btn btn-primary" id="btnNext">'+(isLast?'Finish':'Next →')+'</button>';
  } else {
    h += '<button class="btn" id="btnSkip" '+(item.status!=='unanswered'?'disabled':'')+'>Skip</button>';
    h += '<span class="spacer"></span>';
    h += '<button class="btn btn-primary" id="btnCheck" '+((item.status!=='unanswered'&&item.status!=='skipped')?'disabled':'')+'>Check</button>';
    h += '<button class="btn btn-primary" id="btnNext" '+(canProceed(item)?'':'disabled')+'>'+(isLast?'Finish':'Next →')+'</button>';
  }
  document.getElementById('navbarInner').innerHTML = h;

  document.getElementById('btnPrev').addEventListener('click', function(){ if(ts.idx>0){ ts.idx--; renderSlide(); } });

  if(MODE==='quiz'){
    document.getElementById('btnSkip').addEventListener('click', function(){
      item.status='skipped';
      advanceQuiz(ts, slides);
    });
    document.getElementById('btnNext').addEventListener('click', function(){
      item.status = slideIsAnswered(slide,item) ? 'answered' : 'unanswered';
      advanceQuiz(ts, slides);
    });
  } else {
    document.getElementById('btnSkip').addEventListener('click', function(){
      if(item.status==='unanswered'){ item.status='skipped'; renderSlide(); }
    });
    document.getElementById('btnNext').addEventListener('click', function(){
      if(!canProceed(item)) return;
      if(ts.idx < slides.length-1){ ts.idx++; ts.maxReached=Math.max(ts.maxReached, ts.idx); renderSlide(); }
      else { renderFinished(); }
    });
    document.getElementById('btnCheck').addEventListener('click', function(){ handleCheck(); });
  }
}
function advanceQuiz(ts, slides){
  if(ts.idx < slides.length-1){ ts.idx++; ts.maxReached=Math.max(ts.maxReached, ts.idx); renderSlide(); }
  else { renderFinished(); }
}

function wireSlideEvents(slide, item, idx){
  document.querySelectorAll('input[type="radio"][name="choice"]').forEach(function(r){
    r.addEventListener('change', function(){ item.choice=parseInt(r.value,10); saveState();
      document.querySelectorAll('.opt').forEach(function(l){ l.classList.remove('is-chosen'); var t=l.querySelector('.opt-tag'); if(t) t.remove(); });
      var lab=r.closest('.opt'); lab.classList.add('is-chosen'); var tg=document.createElement('span'); tg.className='opt-tag'; tg.textContent='Selected'; lab.appendChild(tg); });
  });
  document.querySelectorAll('.blank-input').forEach(function(inp){
    inp.addEventListener('input', function(){
      var si=parseInt(inp.dataset.step,10), bk=inp.dataset.bkey;
      item.stepStates[si].inputs[bk]=inp.value;
      saveState();
    });
  });
}

function handleCheck(){
  var ts = state.tabs[activeTab];
  var slide = SLIDES[activeTab][ts.idx];
  var item = ts.items[ts.idx];
  if(item.status==='skipped') item.status='unanswered';
  var fb = document.getElementById('feedbackBox');

  if(slide.kind==='mcq' || slide.kind==='ar'){
    if(item.choice===undefined){ fb.className='feedback show err'; fb.innerHTML='Please choose an option first.'; return; }
    var ok = item.choice===slide.correct;
    if(ok){
      item.status='correct'; playSuccess();
      fb.className='feedback show ok'; fb.innerHTML='<b>Correct!</b>';
    } else {
      item.attempts=(item.attempts||0)+1;
      if(item.attempts>=2){ item.status='revealed'; playReveal(); }
      else { playWrong(); fb.className='feedback show retry'; fb.innerHTML='<b>Not quite — try again</b> (attempt 1 of 2) <span class="attempts-dots"><span class="used"></span><span></span></span>'; __flash={c:'retry',h:'<b>Not quite — try again</b> (attempt 1 of 2) <span class="attempts-dots"><span class="used"></span><span></span></span>'}; }
    }
    renderSlide();
    return;
  }

  // blank / case
  var step = slide.flat[item.curStep];
  var ss = item.stepStates[item.curStep];
  var blanks = Object.keys(step.a);
  var missing = blanks.some(function(k){ return !ss.inputs[k] || String(ss.inputs[k]).trim()===''; });
  if(missing){ fb.className='feedback show err'; fb.innerHTML='Fill in every blank in this step before checking.'; return; }

  var allGood=true;
  blanks.forEach(function(k){
    var good=answerMatches(ss.inputs[k], step.a[k], step.accept, step.expr);
    ss.inputs['fs_'+k]=good?'correct':'wrong';
    if(!good) allGood=false;
  });

  if(allGood){
    ss.status='correct'; playSuccess();
    advanceStepOrFinish(item, slide);
  } else {
    ss.attempts=(ss.attempts||0)+1;
    if(ss.attempts>=2){
      ss.status='revealed'; playReveal();
      advanceStepOrFinish(item, slide);
    } else {
      playWrong();
      fb.className='feedback show retry';
      fb.innerHTML='<b>Not quite — try again</b> (attempt 1 of 2) <span class="attempts-dots"><span class="used"></span><span></span></span>'; __flash={c:'retry',h:'<b>Not quite — try again</b> (attempt 1 of 2) <span class="attempts-dots"><span class="used"></span><span></span></span>'};
      renderSlide();
      return;
    }
  }
  renderSlide();
}

function advanceStepOrFinish(item, slide){
  var total = slide.flat.length;
  var hasExpr = slide.flat.some(function(s){ return s.expr===true; });
  var hasFrac = slide.flat.some(function(s){ return ['fv','fe','fl','fm','fi','flist'].indexOf(s.expr)>=0; });
  if(item.curStep < total-1){
    item.curStep++;
  } else {
    var anyRevealed = item.stepStates.some(function(ss){ return ss.status==='revealed'; });
    item.status = anyRevealed ? 'revealed' : 'correct';
  }
}

/* ================= palette ================= */
var overlay=document.getElementById('overlay');
function statusOf(tabId,i){
  var ts=state.tabs[tabId];
  if(i>ts.maxReached) return 'locked';
  if(i===ts.idx) return 'current';
  return ts.items[i].status==='unanswered' ? 'locked' : ts.items[i].status;
}
function buildPalette(){
  var slides=SLIDES[activeTab];
  document.getElementById('paletteTitle').textContent = TAB_DEFS.find(function(t){return t.id===activeTab;}).label+' · Question palette';
  var body=document.getElementById('paletteBody');
  var html='';
  for(var i=0;i<slides.length;i++){
    html += '<div class="chip" data-status="'+statusOf(activeTab,i)+'" data-idx="'+i+'">'+(i+1)+'</div>';
  }
  body.innerHTML = html;
  body.querySelectorAll('.chip').forEach(function(chip){
    chip.addEventListener('click', function(){
      var i=parseInt(chip.dataset.idx,10);
      var ts=state.tabs[activeTab];
      if(i>ts.maxReached){ showToast('Finish the earlier questions to unlock this one.'); return; }
      ts.idx=i; closePalette(); renderSlide();
    });
  });
}
function openPalette(){ buildPalette(); overlay.classList.add('show'); }
function closePalette(){ overlay.classList.remove('show'); }
var toastTimer;
function showToast(msg){
  var t=document.getElementById('toast'); t.textContent=msg; t.classList.add('show');
  clearTimeout(toastTimer); toastTimer=setTimeout(function(){ t.classList.remove('show'); },2200);
}
document.getElementById('paletteFab').addEventListener('click', openPalette);
document.getElementById('paletteClose').addEventListener('click', closePalette);
overlay.addEventListener('click', function(e){ if(e.target===overlay) closePalette(); });

function updateFab(){
  var slides=SLIDES[activeTab];
  var done=state.tabs[activeTab].items.filter(function(it){ return it.status==='correct'||it.status==='revealed'||it.status==='skipped'; }).length;
  document.getElementById('fabBadge').textContent = done+'/'+slides.length;
}

/* ================= overall progress + finish ================= */
function updateChapterProgress(){
  var total=0, done=0;
  TAB_DEFS.forEach(function(td){
    state.tabs[td.id].items.forEach(function(it){
      total++;
      if(it.status==='correct'||it.status==='revealed'||it.status==='skipped') done++;
    });
  });
  var pct = total>0 ? Math.round((done/total)*100) : 0;
  document.getElementById('cpFill').style.width=pct+'%';
  document.getElementById('cpLabel').textContent=pct+'% complete';
}
function isSlideCorrect(tabId,i){
  var slide=SLIDES[tabId][i], item=state.tabs[tabId].items[i];
  if(slide.kind==='mcq'||slide.kind==='ar') return item.choice===slide.correct;
  return slide.flat.every(function(step,si){
    var ss=item.stepStates[si];
    return Object.keys(step.a).every(function(k){ return answerMatches(ss.inputs[k], step.a[k], step.accept, step.expr); });
  });
}
function isSlideAttempted(tabId,i){
  var slide=SLIDES[tabId][i], item=state.tabs[tabId].items[i];
  if(slide.kind==='mcq'||slide.kind==='ar') return item.choice!==undefined;
  return slide.flat.some(function(step,si){
    var ss=item.stepStates[si];
    return Object.keys(step.a).some(function(k){ return ss.inputs[k] && String(ss.inputs[k]).trim()!==''; });
  });
}
function slideLabel(slide){
  var t = slide.kind==='case' ? slide.title : (slide.kind==='ar' ? slide.a : (slide.p||slide.text||''));
  t = String(t);
  return t.length>90 ? t.slice(0,90)+'…' : t;
}
function slideAnswerText(slide, item, correctSide){
  if(slide.kind==='mcq'||slide.kind==='ar'){
    var opts = slide.kind==='mcq' ? slide.opts : AR_OPTIONS;
    if(correctSide) return '('+LETTERS[slide.correct]+') '+opts[slide.correct];
    return item.choice!==undefined ? '('+LETTERS[item.choice]+') '+opts[item.choice] : '— not attempted —';
  }
  return slide.flat.map(function(step,si){
    var ss=item.stepStates[si];
    return Object.keys(step.a).map(function(k){
      return correctSide ? step.a[k] : (ss.inputs[k] || '—');
    }).join(', ');
  }).join('  |  ');
}

function renderFinished(){
  if(MODE==='quiz'){ renderQuizResults(); return; }
  var ts=state.tabs[activeTab];
  var correct=ts.items.filter(function(i){return i.status==='correct';}).length;
  var revealed=ts.items.filter(function(i){return i.status==='revealed';}).length;
  var skipped=ts.items.filter(function(i){return i.status==='skipped';}).length;
  var h='<div class="qcard done-card"><div class="big">✨</div><h2>Tab complete</h2>';
  h+='<p style="color:var(--ink-soft);font-size:14px;">You worked through all '+ts.items.length+' questions in this tab.</p>';
  if(!ts.recorded){ ts.recorded=true; addRecord('learning', activeTab, correct, revealed, skipped, ts.items.length); }
  h+='<div class="score-pills">'+
     '<span class="score-pill" style="background:var(--success-soft);color:var(--success);">'+correct+' correct</span>'+
     '<span class="score-pill" style="background:var(--danger-soft);color:var(--danger);">'+revealed+' revealed</span>'+
     '<span class="score-pill" style="background:var(--gold-soft);color:var(--retry-text);">'+skipped+' skipped</span></div>'+
     '<button class="btn btn-primary" id="btnReview">Review from question 1</button></div>';
  document.getElementById('wrap').innerHTML=h;
  document.getElementById('navbarInner').innerHTML='';
  document.getElementById('btnReview').addEventListener('click', function(){ ts.idx=0; ts.recorded=false; renderSlide(); });
  updateChapterProgress(); saveState();
}

function renderQuizResults(){
  var ts=state.tabs[activeTab];
  var slides=SLIDES[activeTab];
  var correctCount=0, attemptedCount=0;
  var rowsHtml = slides.map(function(slide,i){
    var item=ts.items[i];
    var ok=isSlideCorrect(activeTab,i);
    var att=isSlideAttempted(activeTab,i);
    if(ok) correctCount++;
    if(att) attemptedCount++;
    var tagCls = ok?'ok':(att?'bad':'na');
    var tagText = ok?'Correct':(att?'Incorrect':'Not attempted');
    var row='<div class="review-row">';
    row+='<span class="review-tag '+tagCls+'">Q'+(i+1)+' · '+tagText+'</span>';
    row+='<div class="review-q">'+fr(esc(slideLabel(slide)))+'</div>';
    row+='<div class="review-ans"><b>Your answer:</b> '+fr(esc(slideAnswerText(slide,item,false)))+'</div>';
    if(!ok) row+='<div class="review-ans" style="color:var(--success);"><b>Correct answer:</b> '+fr(esc(slideAnswerText(slide,item,true)))+'</div>';
    if(slide.sol) row+='<details class="rev-sol"><summary>Show solution</summary>'+solutionHTML(slide)+'</details>';
    row+='</div>';
    return row;
  }).join('');

  addRecord('quiz', activeTab, correctCount, 0, 0, slides.length);
  var h='<div class="qcard done-card" style="text-align:left;">';
  h+='<div style="text-align:center;"><div class="big">🏁</div><h2>Quiz complete</h2>';
  h+='<p style="color:var(--ink-soft);font-size:14px;">'+correctCount+' / '+slides.length+' correct · '+attemptedCount+' attempted</p></div>';
  h+='<div style="margin-top:16px;">'+rowsHtml+'</div>';
  h+='<div style="text-align:center;margin-top:6px;"><button class="btn btn-primary" id="btnReview">Review from question 1</button></div>';
  h+='</div>';
  document.getElementById('wrap').innerHTML=h;
  document.getElementById('navbarInner').innerHTML='';
  document.getElementById('btnReview').addEventListener('click', function(){ ts.idx=0; renderSlide(); });
  playSuccess();
  updateChapterProgress(); saveState();
}

/* ================= mode picker ================= */
function updateModePill(){
  var btn=document.getElementById('modePill');
  if(!btn) return;
  btn.textContent = MODE==='quiz' ? '📝 Quiz Mode · switch' : '📘 Learning Sheet · switch';
}
function showChrome(show){
  document.querySelector('.tabbar').style.display = show?'':'none';
  document.querySelector('.slide-progress').style.display = show?'':'none';
  document.querySelector('.navbar').style.display = show?'':'none';
  document.getElementById('paletteFab').style.display = show?'':'none';
}
function renderModePicker(){
  showChrome(false);
  var wrap=document.getElementById('wrap');
  wrap.innerHTML =
    '<div class="mode-pick">'+
      '<div class="mode-card" data-pick="learning"><div class="mode-icon">📘</div><h3>Learning Sheet</h3>'+
      '<p>Work through each question step by step with instant feedback — two tries, then the correct value is revealed right there so you can keep moving.</p></div>'+
      '<div class="mode-card" data-pick="quiz"><div class="mode-icon">📝</div><h3>Quiz Mode</h3>'+
      '<p>Attempt every question with no hints along the way. Your score and the full answer key are shown together once you finish the tab — just like the real exam.</p></div>'+
    '</div>';
  wrap.querySelectorAll('[data-pick]').forEach(function(card){
    card.addEventListener('click', function(){
      setMode(card.dataset.pick); activeTab='theory';
      document.getElementById('modePill').hidden=false;
      updateModePill();
      showChrome(true);
      buildTabbar();
      renderSlide();
    });
  });
}
document.getElementById('modePill').addEventListener('click', function(){
  if(!appState.mode){ return; }
  setMode(appState.mode==='quiz' ? 'learning' : 'quiz');
  updateModePill();
  showChrome(true);
  buildTabbar();
  renderSlide();
});

/* ================= boot ================= */
var _origRenderSlide = renderSlide;
renderSlide = function(){ _origRenderSlide(); updateChapterProgress(); updateModePill(); };


/* ================= theory tab ================= */
function renderTheory(){
  var wrap=document.getElementById('wrap');
  wrap.innerHTML='<div class="theory">'+fr(THEORY)+'</div>';
  document.querySelector('.slide-progress').style.display='none';
  document.querySelector('.navbar').style.display='none';
  document.getElementById('paletteFab').style.display='none';
  document.getElementById('secSub').textContent='Theory — notes, key ideas and worked examples';
  wrap.querySelectorAll('[data-go]').forEach(function(b){ b.addEventListener('click',function(){ activeTab=b.dataset.go; buildTabbar(); renderSlide(); window.scrollTo({top:0,behavior:'smooth'}); }); });
  wrap.querySelectorAll('[data-jump]').forEach(function(b){ b.addEventListener('click',function(){ var t=document.getElementById(b.dataset.jump); if(t) t.scrollIntoView({behavior:'smooth',block:'start'}); }); });
}
var _rsTheory = renderSlide;
renderSlide = function(){
  if(activeTab==='theory'){ renderTheory(); buildTabbar(); updateChapterProgress(); updateModePill(); saveState(); return; }
  document.querySelector('.slide-progress').style.display='';
  document.querySelector('.navbar').style.display='';
  document.getElementById('paletteFab').style.display='';
  _rsTheory();
};


/* ================= MYP criterion report ================= */
var CRIT_COL={A:'var(--accent-text)',B:'var(--gold)',C:'#8A6FC4',D:'#2F9AA0'};
function critStats(){
  return REPORT.map(function(r){
    var tabId=r[0], slides=SLIDES[tabId], ts=state&&state.tabs[tabId];
    var c=0,w=0,n=0;
    slides.forEach(function(sl,i){
      if(!ts||!ts.items[i]){ n++; return; }
      var it=ts.items[i];
      if(MODE==='learning'){
        if(it.status==='correct') c++; else if(it.status==='revealed') w++; else n++;
      } else {
        if(isSlideCorrect(tabId,i)) c++; else if(isSlideAttempted(tabId,i)) w++; else n++;
      }
    });
    var tot=slides.length, pct=tot?Math.round(c/tot*100):0;
    var lvl=Math.round(c/Math.max(tot,1)*8);
    return {tab:tabId,letter:r[1],name:r[2],c:c,w:w,n:n,tot:tot,pct:pct,lvl:lvl};
  });
}
function arcPath(cx,cy,r,a0,a1){
  if(a1-a0>=Math.PI*2-1e-6){ return 'M'+(cx-r)+','+cy+' a'+r+','+r+' 0 1,0 '+(2*r)+',0 a'+r+','+r+' 0 1,0 '+(-2*r)+',0 Z'; }
  var x0=cx+r*Math.sin(a0), y0=cy-r*Math.cos(a0), x1=cx+r*Math.sin(a1), y1=cy-r*Math.cos(a1);
  return 'M'+cx+','+cy+' L'+x0.toFixed(2)+','+y0.toFixed(2)+' A'+r+','+r+' 0 '+((a1-a0)>Math.PI?1:0)+',1 '+x1.toFixed(2)+','+y1.toFixed(2)+' Z';
}
function pieSVG(parts,size,hole,center,sub){
  var tot=parts.reduce(function(s,p){return s+p.v;},0), cx=size/2, cy=size/2, r=size/2-4, a=0, h='';
  if(!tot){ h+='<circle cx="'+cx+'" cy="'+cy+'" r="'+r+'" style="fill:var(--paper-2);stroke:var(--rule)"/>'; }
  parts.forEach(function(p){ if(!p.v) return; var b=a+p.v/tot*Math.PI*2; h+='<path d="'+arcPath(cx,cy,r,a,b)+'" style="fill:'+p.col+';stroke:var(--card);stroke-width:2"><title>'+esc(p.label)+': '+p.v+'</title></path>'; a=b; });
  if(hole) h+='<circle cx="'+cx+'" cy="'+cy+'" r="'+(r*hole)+'" style="fill:var(--card)"/>';
  if(center) h+='<text x="'+cx+'" y="'+(cy-(sub?4:0))+'" text-anchor="middle" dominant-baseline="middle" style="fill:var(--ink);font:700 '+(size>150?22:15)+'px Fraunces,serif">'+center+'</text>';
  if(sub) h+='<text x="'+cx+'" y="'+(cy+16)+'" text-anchor="middle" style="fill:var(--ink-soft);font:600 11px \'Source Sans 3\',sans-serif">'+sub+'</text>';
  return '<svg viewBox="0 0 '+size+' '+size+'" width="'+size+'" height="'+size+'" role="img">'+h+'</svg>';
}
function band(l){ return l===0?'0':(l<=2?'1–2':(l<=4?'3–4':(l<=6?'5–6':'7–8'))); }
function renderReport(){
  var st=critStats(), totC=0, totQ=0;
  st.forEach(function(s){ totC+=s.c; totQ+=s.tot; });
  var h='<div class="theory">';
  h+='<section class="note"><h2>Chapter test report</h2><p class="lt">'+(MODE==='quiz'?'<b>Quiz mode</b> results: answers are marked when you finish each test tab.':'<b>Learning mode</b> results: a question counts as correct only if you got it without the answer being revealed. Switch to Quiz mode for an exam-style score.')+'</p>';
  h+='<div class="rep-top"><div class="rep-pie">'+pieSVG(st.map(function(s){return {v:s.c,col:CRIT_COL[s.letter],label:'Criterion '+s.letter};}),200,0.55,totC+'/'+totQ,'correct')+'</div>';
  h+='<div class="rep-legend"><div class="rep-cap">Marks earned, by criterion</div>'+st.map(function(s){ return '<div class="rep-li"><span class="sw" style="background:'+CRIT_COL[s.letter]+'"></span><b>'+s.letter+'</b>&nbsp;'+esc(s.name)+'<span class="rep-n">'+s.c+' / '+s.tot+'</span></div>'; }).join('')+'</div></div></section>';
  h+='<div class="rep-grid">'+st.map(function(s){
    return '<div class="rep-card"><div class="rep-h"><span class="crit" style="background:'+CRIT_COL[s.letter]+'">'+s.letter+'</span>'+esc(s.name)+'</div>'+
      '<div class="rep-row">'+pieSVG([{v:s.c,col:'var(--success)',label:'Correct'},{v:s.w,col:'var(--danger)',label:'Incorrect'},{v:s.n,col:'var(--locked)',label:'Not attempted'}],120,0.5,s.pct+'%')+
      '<div class="rep-stats"><div><span class="sw" style="background:var(--success)"></span>Correct <b>'+s.c+'</b></div><div><span class="sw" style="background:var(--danger)"></span>Incorrect <b>'+s.w+'</b></div><div><span class="sw" style="background:var(--locked)"></span>Not attempted <b>'+s.n+'</b></div>'+
      '<div class="rep-lvl">Indicative level <b>'+s.lvl+'</b> / 8 <span>(band '+band(s.lvl)+')</span></div></div></div>'+
      '<button class="hub-btn" data-go="'+s.tab+'">Open Test '+s.letter+' →</button></div>';
  }).join('')+'</div>';
  h+='<p class="rep-note">Indicative level = fraction of questions correct × 8, rounded. It is a practice guide only; your teacher awards the real MYP criterion levels.</p></div>';
  var wrap=document.getElementById('wrap'); wrap.innerHTML=h;
  document.querySelector('.slide-progress').style.display='none';
  document.querySelector('.navbar').style.display='none';
  document.getElementById('paletteFab').style.display='none';
  document.getElementById('secSub').textContent='Report — chapter test results by MYP criterion';
  wrap.querySelectorAll('[data-go]').forEach(function(b){ b.addEventListener('click',function(){ activeTab=b.dataset.go; buildTabbar(); renderSlide(); window.scrollTo({top:0,behavior:'smooth'}); }); });
}
var _rsReport = renderSlide;
renderSlide = function(){
  if(activeTab==='report'){ renderReport(); buildTabbar(); updateChapterProgress(); updateModePill(); saveState(); return; }
  _rsReport();
};


/* ================= skipped-question return ================= */
function firstSkippedIdx(ts){
  for(var i=0;i<ts.items.length;i++){
    var it=ts.items[i];
    if(MODE==='quiz'){ if(!isSlideAttempted(activeTab,i)) return i; }
    else if(it.status==='skipped'||it.status==='unanswered') return i;
  }
  return -1;
}
function skippedList(ts){
  var out=[]; for(var i=0;i<ts.items.length;i++){ var it=ts.items[i];
    if(MODE==='quiz' ? !isSlideAttempted(activeTab,i) : (it.status==='skipped'||it.status==='unanswered')) out.push(i); }
  return out;
}
function renderSkipGate(ts){
  var list=skippedList(ts);
  var h='<div class="qcard done-card"><div class="big">⏭️</div><h2>You skipped '+list.length+' question'+(list.length>1?'s':'')+'</h2>'+
    '<p style="color:var(--ink-soft);font-size:14px;">Answer them now, or submit the tab as it is. Answers are marked only when you submit.</p>'+
    '<div class="skip-chips">'+list.map(function(i){ return '<button class="chip skip-go" data-i="'+i+'">Q'+(i+1)+'</button>'; }).join('')+'</div>'+
    '<div class="skip-btns"><button class="btn btn-primary" id="btnGoSkipped">Answer skipped questions</button><button class="btn" id="btnSubmitAnyway">Submit anyway</button></div></div>';
  document.getElementById('wrap').innerHTML=h;
  document.getElementById('navbarInner').innerHTML='';
  var go=function(i){ ts.idx=i; ts.maxReached=Math.max(ts.maxReached,i); renderSlide(); window.scrollTo({top:0,behavior:'smooth'}); };
  document.getElementById('btnGoSkipped').addEventListener('click',function(){ go(list[0]); });
  document.querySelectorAll('.skip-go').forEach(function(b){ b.addEventListener('click',function(){ go(parseInt(b.dataset.i,10)); }); });
  document.getElementById('btnSubmitAnyway').addEventListener('click',function(){ ts.submitOK=true; renderFinished(); ts.submitOK=false; });
  saveState();
}
var _rfSkip = renderFinished;
renderFinished = function(){
  var ts=state.tabs[activeTab];
  if(MODE==='quiz' && !ts.submitOK && skippedList(ts).length){ renderSkipGate(ts); return; }
  _rfSkip();
  if(MODE==='learning'){
    var list=skippedList(ts);
    if(list.length){
      var card=document.querySelector('.done-card');
      if(card){ var d=document.createElement('div'); d.className='skip-btns';
        d.innerHTML='<button class="btn btn-primary" id="btnGoSkipped">Attempt skipped questions ('+list.length+')</button>';
        card.appendChild(d);
        document.getElementById('btnGoSkipped').addEventListener('click',function(){ ts.idx=list[0]; ts.recorded=false; renderSlide(); window.scrollTo({top:0,behavior:'smooth'}); }); }
    }
  }
};


/* ================= approx answers (physics: within 1%) ================= */
var _amTools = answerMatches;
answerMatches = function(input,answer,accept,expr){
  if(expr==='approx'){
    var n1=parseNum(input); if(n1===null) return false;
    return [answer].concat(accept||[]).some(function(a){ var n2=parseNum(a); if(n2===null) return false; return Math.abs(n1-n2) <= Math.max(0.011*Math.abs(n2), 1e-9); });
  }
  return _amTools(input,answer,accept,expr);
};

/* ================= palette: every question already reached can be opened ================= */
statusOf = function(tabId,i){
  var ts=state.tabs[tabId];
  if(i>ts.maxReached) return 'locked';
  if(i===ts.idx) return 'current';
  var s=ts.items[i].status;
  if(s==='unanswered') return 'skipped';
  return s;
};

/* ================= on-screen keyboard ================= */
var KB={on:true, page:'num', target:null};
try{ var kbp=localStorage.getItem('sopaan-kb-pref'); if(kbp==='off') KB.on=false; }catch(e){}
function kbSave(){ try{ localStorage.setItem('sopaan-kb-pref', KB.on?'on':'off'); }catch(e){} }
var KEYS_NUM=[['7','8','9','(',')'],['4','5','6','−','/'],['1','2','3','.',','],['0',':','%','°','⌫'],['abc','←','→','Clear','Done']];
var KEYS_FRAC=[['7','8','9','/'],['4','5','6','−'],['1','2','3','space'],['0',',','⌫','Clear'],['abc','←','→','Done']];
var KEYS_ALG=[['7','8','9','x','y','n'],['4','5','6','+','−','a'],['1','2','3','×','÷','b'],['0','.','(',')','^','²'],['/','π','|','t','⌫','Clear'],['abc','←','→','Done']];
function kbLayoutFor(inp){ try{ var ts=state.tabs[activeTab], sl=SLIDES[activeTab][ts.idx], stp=sl.flat[parseInt(inp.dataset.step,10)]; var m=stp.expr, key=String(stp.a[inp.dataset.bkey]||'');
  if(m==='words'||m==='glist'||m==='angle') return 'abc'; if(m===true||m==='pow'||m==='primes') return 'alg';
  if(['fv','fe','fl','fm','fi','flist'].indexOf(m)>=0) return 'frac'; if(m==='dec'||m==='approx'||m==='dlist'||m==='set'||m==='coord'||m==='list'||m==='time') return 'num';
  if(/^[\-−]?\d+ \d+\/\d+$/.test(key)||/^[\-−]?\d+\/\d+$/.test(key)) return 'frac'; if(/[a-df-z]/i.test(key.replace(/pi/gi,''))) return /\d/.test(key)?'alg':'abc'; return 'num'; }catch(e){ return 'num'; } }
var KEYS_ABC=[['q','w','e','r','t','y','u','i','o','p'],['a','s','d','f','g','h','j','k','l','-'],['z','x','c','v','b','n','m',',',':','/'],['123','space','←','→','⌫','Done']];
function kbBuild(){
  var el=document.getElementById('vkb'); if(!el){ el=document.createElement('div'); el.id='vkb'; el.className='vkb'; document.body.appendChild(el);
    el.addEventListener('pointerdown',function(e){ var b=e.target.closest('button[data-k]'); e.preventDefault(); if(b) kbPress(b.dataset.k); });
    el.addEventListener('mousedown',function(e){ e.preventDefault(); }); }
  var rows={num:KEYS_NUM,frac:KEYS_FRAC,alg:KEYS_ALG,abc:KEYS_ABC}[KB.page]||KEYS_NUM;
  el.innerHTML='<div class="vkb-top"><span>⌨️ Keyboard</span><button data-k="device" class="vkb-link">Use device keyboard</button></div>'+
    rows.map(function(r){ return '<div class="vkb-row">'+r.map(function(k){
      var cls='vkb-k'+(/^(abc|123|Done|Clear|⌫|←|→|space)$/.test(k)?' fn':'')+(k==='Done'?' done':'');
      return '<button type="button" class="'+cls+'" data-k="'+k+'">'+(k==='space'?'space':k)+'</button>'; }).join('')+'</div>'; }).join('');
  return el;
}
function kbShow(inp){ KB.target=inp; KB.home=kbLayoutFor(inp); KB.page=KB.home; if(!KB.on) return; var cp=document.getElementById('calcPanel'); if(cp&&cp.classList.contains('show')) return; var el=kbBuild(); var nb=document.querySelector('.navbar'); el.style.bottom=(nb?nb.getBoundingClientRect().height:0)+'px'; el.classList.add('show'); document.body.classList.add('kb-open'); setTimeout(function(){ var r=inp.getBoundingClientRect(), top=el.getBoundingClientRect().top; if(r.bottom>top-12) window.scrollBy({top:r.bottom-top+60,behavior:'smooth'}); else if(r.top<60) window.scrollBy({top:r.top-80,behavior:'smooth'}); },30); }
function kbHide(){ var el=document.getElementById('vkb'); if(el) el.classList.remove('show'); document.body.classList.remove('kb-open'); }
function kbInsert(s){
  var t=KB.target; if(!t||t.disabled) return;
  var a=t.selectionStart==null?t.value.length:t.selectionStart, b=t.selectionEnd==null?a:t.selectionEnd;
  t.value=t.value.slice(0,a)+s+t.value.slice(b); var p=a+s.length; try{ t.setSelectionRange(p,p); }catch(e){}
  t.dispatchEvent(new Event('input',{bubbles:true}));
}
function kbPress(k){
  var t=KB.target; if(k==='device'){ KB.on=false; kbSave(); kbHide(); document.querySelectorAll('.blank-input').forEach(function(i){ i.removeAttribute('inputmode'); }); if(t){ t.blur(); setTimeout(function(){ t.focus(); },50); } showToast('Device keyboard on. Tap ⌨️ on any blank to bring the on-screen keyboard back.'); return; }
  if(k==='Done'){ kbHide(); if(t) t.blur(); return; }
  if(k==='abc'||k==='123'){ KB.page=(k==='abc')?'abc':(KB.home&&KB.home!=='abc'?KB.home:'num'); kbBuild(); return; }
  if(!t) return;
  if(k==='⌫'){ var a=t.selectionStart, b=t.selectionEnd; if(a===b&&a>0){ t.value=t.value.slice(0,a-1)+t.value.slice(b); try{t.setSelectionRange(a-1,a-1);}catch(e){} } else { t.value=t.value.slice(0,a)+t.value.slice(b); try{t.setSelectionRange(a,a);}catch(e){} } t.dispatchEvent(new Event('input',{bubbles:true})); return; }
  if(k==='Clear'){ t.value=''; t.dispatchEvent(new Event('input',{bubbles:true})); return; }
  if(k==='←'||k==='→'){ var p=(t.selectionStart||0)+(k==='←'?-1:1); p=Math.max(0,Math.min(t.value.length,p)); try{t.setSelectionRange(p,p);}catch(e){} return; }
  var map={'−':'-','space':' '}; kbInsert(map[k]!==undefined?map[k]:k);
}
function kbWire(){
  document.querySelectorAll('.blank-input').forEach(function(inp){
    if(inp.dataset.kb) return; inp.dataset.kb='1';
    if(KB.on) inp.setAttribute('inputmode','none');
    inp.addEventListener('focus',function(){ kbShow(inp); });
    var btn=document.createElement('button'); btn.type='button'; btn.className='kb-toggle'; btn.title='On-screen keyboard'; btn.textContent='⌨️'; btn.tabIndex=-1;
    btn.addEventListener('mousedown',function(e){ e.preventDefault(); });
    btn.addEventListener('click',function(){ KB.on=true; kbSave(); document.querySelectorAll('.blank-input').forEach(function(i){ i.setAttribute('inputmode','none'); }); inp.focus(); kbShow(inp); });
    if(!inp.disabled) inp.insertAdjacentElement('afterend',btn);
  });
}
document.addEventListener('focusout',function(e){ setTimeout(function(){ var a=document.activeElement; if(!a||!a.classList||!a.classList.contains('blank-input')){ if(!document.querySelector('#vkb:hover')) kbHide(); } },120); });

/* ================= calculator ================= */
var CALC={expr:'', ans:0};
function calcEval(src){
  var s=String(src).replace(/×/g,'*').replace(/÷/g,'/').replace(/−/g,'-').replace(/π/g,'(PI)').replace(/Ans/g,'('+CALC.ans+')').replace(/\^/g,'**').replace(/√\(/g,'sqrt(').replace(/²/g,'**2').replace(/E/g,'*10**');
  s=s.replace(/(^|[(*\/+\-,])-/g,'$1(-1)*');
  if(/[^0-9+\-*/().,a-z A-Z]/.test(s)) throw 0;
  var ok=s.replace(/sin|cos|tan|asin|acos|atan|sqrt|log|ln|PI|abs/g,''); if(/[a-zA-Z]/.test(ok)) throw 0;
  var f=new Function('sin','cos','tan','asin','acos','atan','sqrt','log','ln','PI','abs','return ('+s+');');
  var d=Math.PI/180;
  var v=f(function(x){return Math.sin(x*d);},function(x){return Math.cos(x*d);},function(x){return Math.tan(x*d);},
    function(x){return Math.asin(x)/d;},function(x){return Math.acos(x)/d;},function(x){return Math.atan(x)/d;},Math.sqrt,Math.log10,Math.log,Math.PI,Math.abs);
  if(typeof v!=='number'||!isFinite(v)) throw 0; return v;
}
function fmtNum(v){ if(Math.abs(v)>=1e10||(Math.abs(v)<1e-6&&v!==0)) return v.toExponential(6).replace(/\.?0+e/,'e'); return String(parseFloat(v.toPrecision(10))); }
var CKEYS=[['sin(','cos(','tan(','√(','^','²'],['asin(','acos(','atan(','(',')','π'],['7','8','9','÷','⌫','AC'],['4','5','6','×','E','Ans'],['1','2','3','−','(−)','Insert'],['0','.','=','+']];
function openCalc(){
  var p=document.getElementById('calcPanel');
  if(!p){ p=document.createElement('div'); p.id='calcPanel'; p.className='tool-panel calc';
    p.innerHTML='<div class="tp-head"><b>🧮 Calculator</b><span class="tp-note">degrees · tap a blank, then Insert</span><button class="tp-x" data-c="close">✕</button></div>'+
      '<div class="calc-disp"><div class="calc-expr" id="calcExpr"></div><div class="calc-res" id="calcRes">0</div></div>'+
      '<div class="calc-keys">'+CKEYS.map(function(r){ return r.map(function(k){ return '<button type="button" data-c="'+k+'" class="'+(k==='='?'eq':(/^(AC|⌫|Insert)$/.test(k)?'fn':''))+'">'+({'sin(':'sin','cos(':'cos','tan(':'tan','asin(':'sin⁻¹','acos(':'cos⁻¹','atan(':'tan⁻¹','√(':'√'}[k]||k)+'</button>'; }).join(''); }).join('')+'</div>';
    document.body.appendChild(p);
    p.addEventListener('mousedown',function(e){ if(e.target.closest('button')) e.preventDefault(); });
    p.addEventListener('click',function(e){ var b=e.target.closest('button[data-c]'); if(!b) return; calcKey(b.dataset.c); });
  }
  kbHide(); var nb=document.querySelector('.navbar'); p.style.bottom=((nb?nb.getBoundingClientRect().height:0)+8)+'px'; p.classList.add('show'); document.body.classList.add('calc-open'); calcShow();
}
function calcShow(res){ document.getElementById('calcExpr').textContent=CALC.expr||' '; if(res!==undefined) document.getElementById('calcRes').textContent=res; }
function calcKey(k){
  if(k==='close'){ document.getElementById('calcPanel').classList.remove('show'); document.body.classList.remove('calc-open'); return; }
  if(k==='AC'){ CALC.expr=''; calcShow('0'); return; }
  if(k==='⌫'){ CALC.expr=CALC.expr.replace(/(asin\(|acos\(|atan\(|sin\(|cos\(|tan\(|√\(|Ans|.)$/,''); calcShow(); return; }
  if(k==='='){ try{ var v=calcEval(CALC.expr); CALC.ans=v; calcShow(fmtNum(v)); }catch(e){ calcShow('Error'); } return; }
  if(k==='(−)'){ CALC.expr+='−'; calcShow(); return; }
  if(k==='Insert'){ var r=document.getElementById('calcRes').textContent; if(KB.target && !KB.target.disabled && r!=='Error'){ KB.target.value=r; KB.target.dispatchEvent(new Event('input',{bubbles:true})); showToast('Inserted '+r+' into the blank.'); } else showToast('Tap a blank first, then press Insert.'); return; }
  CALC.expr+=k; calcShow();
}

/* ================= Desmos ================= */
var DESMOS_KEY='dcb31709b452b1cf9dc26972add0fda6', desmosCalc=null, desmosLoading=false;
function openDesmos(exprs){
  var p=document.getElementById('desmosPanel');
  if(!p){ p=document.createElement('div'); p.id='desmosPanel'; p.className='tool-panel desmos';
    p.innerHTML='<div class="tp-head"><b>📈 Desmos graphing calculator</b><button class="tp-x" id="desmosReset">Reset graph</button><button class="tp-x" id="desmosClose">✕</button></div><div id="desmosBox"><div class="desmos-msg">Loading Desmos…</div></div>';
    document.body.appendChild(p);
    document.getElementById('desmosClose').addEventListener('click',function(){ p.classList.remove('show'); });
    document.getElementById('desmosReset').addEventListener('click',function(){ if(desmosCalc) desmosSet(p._exprs||[]); });
  }
  p._exprs=exprs||[]; p.classList.add('show');
  if(window.Desmos){ desmosInit(); desmosSet(p._exprs); return; }
  if(desmosLoading) return; desmosLoading=true;
  var sc=document.createElement('script'); sc.src='https://www.desmos.com/api/v1.9/calculator.js?apiKey='+DESMOS_KEY;
  sc.onload=function(){ desmosInit(); desmosSet(p._exprs); };
  sc.onerror=function(){ desmosLoading=false; document.getElementById('desmosBox').innerHTML='<div class="desmos-msg">Desmos needs an internet connection. <a href="https://www.desmos.com/calculator" target="_blank" rel="noopener">Open Desmos in a new tab</a>.</div>'; };
  document.head.appendChild(sc);
}
function desmosInit(){ if(desmosCalc) return; var box=document.getElementById('desmosBox'); box.innerHTML=''; desmosCalc=Desmos.GraphingCalculator(box,{expressionsCollapsed:false,settingsMenu:false,border:false,degreeMode:true}); }
function desmosSet(exprs){ if(!desmosCalc) return; desmosCalc.setBlank(); (exprs||[]).forEach(function(e,i){ if(typeof e==='string') desmosCalc.setExpression({id:'e'+i,latex:e}); else desmosCalc.setExpression(Object.assign({id:'e'+i},e)); }); }

/* ================= toolbar on each question ================= */
var _rsTools = renderSlide;
renderSlide = function(){
  _rsTools();
  kbHide();
  if(activeTab==='theory'||activeTab==='report') return;
  var ts=state.tabs[activeTab]; if(!ts) return;
  var slide=SLIDES[activeTab][ts.idx], card=document.querySelector('#wrap .qcard');
  if(card && slide && slide.tools && slide.tools.length && !card.querySelector('.tool-bar')){
    var bar=document.createElement('div'); bar.className='tool-bar';
    bar.innerHTML=(slide.tools.indexOf('calc')>=0?'<button type="button" class="tool-btn" data-t="calc">🧮 Calculator</button>':'')+
                  (slide.tools.indexOf('desmos')>=0?'<button type="button" class="tool-btn" data-t="desmos">📈 Desmos graph</button>':'');
    card.insertBefore(bar, card.firstChild);
    bar.addEventListener('click',function(e){ var b=e.target.closest('[data-t]'); if(!b) return; if(b.dataset.t==='calc') openCalc(); else openDesmos(slide.desmos||[]); });
  }
  kbWire();
};



/* ================= signed fractions in text: {−3/4}, {3/−4}, {−2 1/3}, {p/q} ================= */
fr = function(s){ return String(s).replace(/&lt;(\/?)(b|sup|sub|i)>/g,'<$1$2>')
  .replace(/\{([−-]?\d+) (\d+)\/(\d+)\}/g,'<span class="mx">$1<span class="fq"><span>$2</span><span>$3</span></span></span>')
  .replace(/\{([−-]?[A-Za-z0-9]+)\/([−-]?[A-Za-z0-9]+)\}/g,'<span class="fq"><span>$1</span><span>$2</span></span>'); };
/* ================= BMA badge → main page of this sheet (theory hub) ================= */
(function(){
  var c=document.querySelector('.brand .crest'); if(!c) return;
  var a=document.createElement('button'); a.type='button'; a.className='crest crest-home'; a.title='Back to the main page (theory notes)'; a.setAttribute('aria-label','Main page');
  a.innerHTML='BM<span class="crest-h">⌂</span>'; c.parentNode.replaceChild(a,c);
  a.addEventListener('click',function(){
    if(!student||!MODE){ window.scrollTo({top:0,behavior:'smooth'}); return; }
    if(typeof kbHide==='function') kbHide(); if(typeof SP!=='undefined'&&SP.on) spToggle(false);
    var cp=document.getElementById('calcPanel'); if(cp) cp.classList.remove('show'); document.body.classList.remove('calc-open');
    activeTab = (typeof THEORY!=='undefined') ? 'theory' : TAB_DEFS[0].id;
    buildTabbar(); renderSlide(); window.scrollTo({top:0,behavior:'smooth'});
  });
})();

/* ================= session clock: starts at sign-in and keeps running ================= */
var CLK={t0:null};
(function(){
  var row=document.querySelector('.brand .brand-row'); if(!row) return;
  var d=document.createElement('div'); d.className='bmasw off'; d.id='swBox'; d.title='Time since you signed in';
  d.innerHTML='<span class="bmasw-ic">⏱</span><span class="bmasw-t" id="swT">00:00</span>';
  row.appendChild(d); setInterval(swTick,1000);
})();
function swFmt(s){ s=Math.floor(s||0); var h=Math.floor(s/3600), m=Math.floor(s%3600/60), x=s%60; return (h?h+':'+String(m).padStart(2,'0'):String(m).padStart(2,'0'))+':'+String(x).padStart(2,'0'); }
function swTick(){
  var box=document.getElementById('swBox'); if(!box) return;
  if(student && !CLK.t0) CLK.t0=Date.now();
  if(!student) CLK.t0=null;
  box.classList.toggle('off',!CLK.t0);
  document.getElementById('swT').textContent = CLK.t0 ? swFmt((Date.now()-CLK.t0)/1000) : '00:00';
}
function swTab(){ try{ if(!state||!state.tabs||activeTab==='theory'||activeTab==='report') return null; return state.tabs[activeTab]||null; }catch(e){ return null; } }
var _rsSW = renderSlide;
renderSlide = function(){ _rsSW(); swTick(); };
var _rfSW = renderFinished;
renderFinished = function(){ _rfSW(); var done=document.querySelector('#wrap .done-card'); if(CLK.t0 && done && !done.querySelector('.bmasw-done')){ var p=document.createElement('p'); p.className='bmasw-done'; p.textContent='⏱ Time since sign-in: '+swFmt((Date.now()-CLK.t0)/1000); var h2=done.querySelector('h2'); if(h2) h2.insertAdjacentElement('afterend',p); else done.appendChild(p); } };

/* ================= scratchpad (Khan-style, 4 pens) ================= */
var SP={on:false, draw:true, color:'ink', size:3, erase:false, store:{}, key:null, cv:null, ctx:null, down:false, last:null};
var SP_COL={ink:null, blue:'#2563EB', red:'#DC2626', green:'#16A34A'};
function spInk(){ return getComputedStyle(document.documentElement).getPropertyValue('--ink').trim()||'#211E1A'; }
function spKey(){ var ts=swTab(); return ts ? (MODE+'|'+activeTab+'|'+ts.idx) : null; }
function spBuild(){
  if(SP.cv) return;
  var cv=document.createElement('canvas'); cv.id='spCanvas'; cv.className='sp-canvas'; document.body.appendChild(cv);
  var bar=document.createElement('div'); bar.id='spBar'; bar.className='sp-bar';
  bar.innerHTML='<span class="sp-lbl">✏️ Scratchpad</span>'+
    ['ink','blue','red','green'].map(function(c){ return '<button type="button" class="sp-pen" data-c="'+c+'" title="'+(c==='ink'?'black':c)+' pen"><i style="background:'+(c==='ink'?'var(--ink)':SP_COL[c])+'"></i></button>'; }).join('')+
    '<button type="button" class="sp-tool" data-t="erase" title="Eraser">🧽</button><button type="button" class="sp-tool" data-t="size" title="Pen size">●</button><button type="button" class="sp-tool" data-t="scroll" title="Pause drawing to scroll or answer">✋</button>'+
    '<button type="button" class="sp-tool" data-t="clear" title="Clear page">🗑</button><button type="button" class="sp-tool" data-t="close" title="Close scratchpad">✕</button>';
  document.body.appendChild(bar);
  bar.addEventListener('click',function(e){ var b=e.target.closest('button'); if(!b) return;
    if(b.dataset.c){ SP.color=b.dataset.c; SP.erase=false; SP.draw=true; }
    else if(b.dataset.t==='erase'){ SP.erase=true; SP.draw=true; }
    else if(b.dataset.t==='size'){ SP.size = SP.size===3?6:(SP.size===6?1.5:3); b.textContent = SP.size===6?'⬤':(SP.size===1.5?'·':'●'); }
    else if(b.dataset.t==='scroll'){ SP.draw=!SP.draw; }
    else if(b.dataset.t==='clear'){ spClear(); }
    else if(b.dataset.t==='close'){ spToggle(false); return; }
    spUI(); });
  SP.cv=cv; SP.ctx=cv.getContext('2d');
  cv.addEventListener('pointerdown',function(e){ if(!SP.draw) return; e.preventDefault(); cv.setPointerCapture(e.pointerId); SP.down=true; SP.last=spPt(e); spDot(SP.last); });
  cv.addEventListener('pointermove',function(e){ if(!SP.down) return; e.preventDefault(); var p=spPt(e); spLine(SP.last,p); SP.last=p; });
  var up=function(){ if(SP.down){ SP.down=false; spSave(); } };
  cv.addEventListener('pointerup',up); cv.addEventListener('pointercancel',up); cv.addEventListener('pointerleave',up);
  window.addEventListener('resize',function(){ if(SP.on) spFit(true); });
}
function spPt(e){ var r=SP.cv.getBoundingClientRect(); return {x:e.clientX-r.left, y:e.clientY-r.top}; }
function spStyle(){ var c=SP.ctx; c.lineCap='round'; c.lineJoin='round'; c.globalCompositeOperation=SP.erase?'destination-out':'source-over'; c.strokeStyle=c.fillStyle=(SP.color==='ink'?spInk():SP_COL[SP.color]); c.lineWidth=SP.erase?22:SP.size; }
function spDot(p){ spStyle(); var c=SP.ctx; c.beginPath(); c.arc(p.x,p.y,(SP.erase?11:SP.size/2),0,Math.PI*2); c.fill(); }
function spLine(a,b){ spStyle(); var c=SP.ctx; c.beginPath(); c.moveTo(a.x,a.y); c.lineTo(b.x,b.y); c.stroke(); }
function spSave(){ if(SP.key&&SP.cv){ try{ SP.store[SP.key]=SP.cv.toDataURL(); }catch(e){} } }
function spClear(){ if(!SP.ctx) return; SP.ctx.save(); SP.ctx.setTransform(1,0,0,1,0,0); SP.ctx.clearRect(0,0,SP.cv.width,SP.cv.height); SP.ctx.restore(); if(SP.key) delete SP.store[SP.key]; }
function spFit(keep){
  var wrap=document.getElementById('wrap'); if(!wrap||!SP.cv) return;
  var r=wrap.getBoundingClientRect(), top=r.top+window.scrollY, h=Math.max(wrap.scrollHeight, window.innerHeight-r.top)+40, w=document.documentElement.clientWidth;
  var old=keep&&SP.key?SP.store[SP.key]:null, dpr=window.devicePixelRatio||1;
  SP.cv.style.top=top+'px'; SP.cv.style.left='0px'; SP.cv.style.width=w+'px'; SP.cv.style.height=h+'px';
  SP.cv.width=Math.round(w*dpr); SP.cv.height=Math.round(h*dpr); SP.ctx.setTransform(dpr,0,0,dpr,0,0);
  if(old){ var im=new Image(); im.onload=function(){ SP.ctx.save(); SP.ctx.setTransform(1,0,0,1,0,0); SP.ctx.drawImage(im,0,0); SP.ctx.restore(); }; im.src=old; }
}
function spLoad(){ spSave(); SP.key=spKey(); spFit(false); var d=SP.key&&SP.store[SP.key]; if(d){ var im=new Image(); im.onload=function(){ SP.ctx.save(); SP.ctx.setTransform(1,0,0,1,0,0); SP.ctx.drawImage(im,0,0); SP.ctx.restore(); }; im.src=d; } }
function spUI(){
  var bar=document.getElementById('spBar'); if(!bar) return;
  bar.querySelectorAll('.sp-pen').forEach(function(b){ b.classList.toggle('on', !SP.erase && SP.draw && b.dataset.c===SP.color); });
  bar.querySelector('[data-t=erase]').classList.toggle('on', SP.erase && SP.draw);
  bar.querySelector('[data-t=scroll]').classList.toggle('on', !SP.draw);
  SP.cv.classList.toggle('passive', !SP.draw);
  var fb=document.getElementById('spFab'); if(fb) fb.classList.toggle('on',SP.on);
}
function spToggle(on){
  spBuild(); SP.on=(on===undefined)?!SP.on:on;
  document.body.classList.toggle('sp-open',SP.on); SP.cv.style.display=SP.on?'block':'none'; document.getElementById('spBar').style.display=SP.on?'flex':'none';
  if(SP.on){ SP.draw=true; SP.erase=false; spLoad(); if(typeof kbHide==='function') kbHide(); } else { spSave(); }
  spUI();
}
(function(){ var f=document.createElement('button'); f.type='button'; f.id='spFab'; f.className='sp-fab'; f.innerHTML='✏️ <span>Scratchpad</span>'; f.title='Open a scratchpad to write your working'; f.addEventListener('click',function(){ spToggle(); }); document.body.appendChild(f); })();
var _rsSP = renderSlide;
renderSlide = function(){ _rsSP(); var fab=document.getElementById('spFab'); var q=!!swTab(); if(fab) fab.style.display=q?'':'none'; if(!q && SP.on) spToggle(false); if(SP.on) setTimeout(spLoad,30); };

renderLogin();
})();
</script>
</body>
</html>
