<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Phòng Thí Nghiệm — Ghép Chất</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=JetBrains+Mono:wght@400;500;700&display=swap" rel="stylesheet">
<style>
  .home-origin-btn{
    position:relative;
    display:flex;
    align-items:center;
    gap:12px;

    padding:10px 18px;
    margin-left:14px;

    border:none;
    border-radius:999px;

    background:
        linear-gradient(135deg,#b02b27,#8d221f);

    color:#f7eed7;
    cursor:pointer;

    font-family:'Be Vietnam Pro',sans-serif;

    box-shadow:
        0 10px 24px rgba(156,42,37,.28),
        inset 0 1px 0 rgba(255,255,255,.15);

    transition:
        transform .28s,
        box-shadow .28s,
        background .28s;
}

.home-origin-btn::before{
    content:"";
    position:absolute;
    inset:2px;
    border-radius:999px;
    border:1px solid rgba(255,215,120,.45);
    pointer-events:none;
}

.home-origin-btn:hover{
    transform:translateY(-3px);
    background:linear-gradient(135deg,#c53a35,#a42a25);
    box-shadow:
        0 16px 32px rgba(156,42,37,.4),
        inset 0 1px 0 rgba(255,255,255,.2);
}

.home-origin-btn:active{
    transform:scale(.96);
}

.btn-icon{
    width:42px;
    height:42px;
    border-radius:50%;
    display:flex;
    align-items:center;
    justify-content:center;

    background:
        radial-gradient(circle,#e8c574,#e5c88c);

    color:#2d2118;
    font-size:22px;

    box-shadow:
        inset 0 2px 5px rgba(255,255,255,.3),
        0 5px 10px rgba(0,0,0,.18);
}

.btn-text{
    display:flex;
    flex-direction:column;
    line-height:1.1;
    text-align:left;
}

.btn-text small{
    font-size:9px;
    letter-spacing:.35em;
    opacity:.75;
    font-weight:700;
}

.btn-text strong{
    font-size:15px;
    font-weight:700;
    font-family:'Cormorant Garamond',serif;
    letter-spacing:.05em;
}

@media(max-width:768px){

    .home-origin-btn{
        padding:10px;
        border-radius:50%;
        width:52px;
        height:52px;
        justify-content:center;
        margin-left:8px;
    }

    .btn-text{
        display:none;
    }

    .btn-icon{
        width:36px;
        height:36px;
        font-size:20px;
    }
}
:root{
  /* Màu nền */
  --bg:#f6efe2;          /* nền be */
  --panel:#fffaf2;       /* panel sáng */
  --panel2:#f4ead8;      /* panel phụ */
  --line:#d9c6a6;        /* đường viền */

  /* Chữ */
  --ink:#3a2418;         /* nâu đậm */
  --dim:#8b6b56;         /* nâu nhạt */

  /* Màu chủ đạo */
  --phos:#b02b27;        /* đỏ KOIFISH */
  --phos-dim:#f6efe6;    /* đỏ đậm */

  /* Các màu phụ */
  --amber:#d19b45;       /* vàng be */
  --red:#cf3c38;
  --violet:#8d4d79;
  --cyan:#8f5b46;
  --slate:#8b7566;
  --sand:#d7b987;
}
*{box-sizing:border-box;}
html,body{margin:0;padding:0;}
body{
  background:
      radial-gradient(circle at top left,
      rgba(176,43,39,.12), transparent 45%),
      radial-gradient(circle at bottom right,
      rgba(209,155,69,.12), transparent 40%),
      var(--bg);

  color:var(--ink);
  font-family:'Space Grotesk',sans-serif;
}
::selection{background:var(--phos-dim);}
.wrap{max-width:1400px;margin:0 auto;padding:20px 22px 60px;}

/* header */
header{display:flex;align-items:flex-end;justify-content:space-between;flex-wrap:wrap;gap:14px;padding-bottom:18px;border-bottom:1px solid var(--line);margin-bottom:18px;}
.brand{display:flex;align-items:center;gap:14px;}
.flaskmark{width:44px;height:44px;flex-shrink:0;}
h1{font-size:1.5rem;margin:0;font-weight:700;letter-spacing:.2px;}
h1 span{color:var(--phos);}
.sub{color:var(--dim);font-size:.82rem;margin-top:2px;}
.stats{display:flex;gap:22px;font-family:'JetBrains Mono',monospace;font-size:.78rem;color:var(--dim);}
.stats b{color:var(--phos);font-size:1.05rem;display:block;font-family:'Space Grotesk',sans-serif;font-weight:700;}

/* layout */
.grid{display:grid;grid-template-columns:1.3fr 1fr;gap:20px;}
@media(max-width:980px){.grid{grid-template-columns:1fr;}}

.panel{background:linear-gradient(180deg,var(--panel),var(--panel2));border:1px solid var(--line);border-radius:14px;padding:16px;}
.panel h2{font-size:.72rem;text-transform:uppercase;letter-spacing:1.5px;color:var(--dim);margin:0 0 12px;font-weight:600;}

/* tabs */
.tabs{display:flex;flex-wrap:wrap;gap:6px;margin-bottom:12px;}
.tab{background:transparent;border:1px solid var(--line);color:var(--dim);font-family:'JetBrains Mono',monospace;font-size:.7rem;padding:5px 10px;border-radius:20px;cursor:pointer;transition:.15s;}
.tab.active{background:var(--phos-dim);border-color:var(--phos);color:var(--ink);}
.tab:hover{border-color:var(--phos);}

.searchbox{width:100%;background:var(--bg);border:1px solid var(--line);border-radius:8px;color:var(--ink);padding:8px 10px;font-family:'JetBrains Mono',monospace;font-size:.8rem;margin-bottom:12px;}
.searchbox:focus{outline:none;border-color:var(--phos);}

.tiles{display:grid;grid-template-columns:repeat(auto-fill,minmax(84px,1fr));gap:8px;max-height:520px;overflow-y:auto;padding-right:4px;}
.tiles::-webkit-scrollbar{width:6px;}
.tiles::-webkit-scrollbar-thumb{background:var(--line);border-radius:3px;}

.tile{background:var(--bg);border:1px solid var(--line);border-radius:10px;padding:8px 6px;text-align:center;cursor:pointer;transition:.12s;position:relative;overflow:hidden;}
.tile:hover{transform:translateY(-2px);  border-color:#b02b27;
    box-shadow:0 6px 18px rgba(176,43,39,.18)}
.tile .f{font-family:'JetBrains Mono',monospace;font-size:.86rem;font-weight:700;display:block;}
.tile .n{font-size:.6rem;color:var(--dim);display:block;margin-top:2px;line-height:1.15;}
.tile .catbar{position:absolute;top:0;left:0;right:0;height:3px;}

.locked{opacity:.16;filter:grayscale(1);cursor:not-allowed;}
.locked:hover{transform:none;box-shadow:none;border-color:var(--line);}

/* category colors */
.c-element .catbar{background:#a65c39;}
.c-element .f{color:#a65c39;}
.c-oxide .catbar{background:var(--amber);} .c-oxide .f{color:var(--amber);}
.c-base .catbar{background:#b02b27;}
.c-base .f{color:#b02b27;}
.c-acid .catbar{background:var(--red);} .c-acid .f{color:var(--red);}
.c-salt .catbar{background:var(--sand);} .c-salt .f{color:var(--sand);}
.c-organic .catbar{background:var(--violet);} .c-organic .f{color:var(--violet);}
.c-other .catbar{background:var(--slate);} .c-other .f{color:var(--slate);}

/* flask panel */
.flaskzone{min-height:110px;      background:#fffaf5;  border:2px dashed #c8aa86;;border-radius:10px;padding:12px;display:flex;flex-wrap:wrap;gap:8px;align-content:flex-start;margin-bottom:12px;}
.flaskzone.empty::before{content:"Chọn chất ở bên trái để thêm vào bình phản ứng…";color:var(--dim);font-size:.78rem;font-style:italic;}
.chip{background:var(--panel2);border:1px solid var(--phos-dim);border-radius:20px;padding:6px 12px 6px 12px;font-family:'JetBrains Mono',monospace;font-size:.82rem;display:flex;align-items:center;gap:8px;cursor:pointer;}
.chip:hover{border-color:var(--red);}
.chip .x{color:var(--dim);font-size:.7rem;}

.actions{display:flex;gap:10px;margin-bottom:16px;}
.btn{flex:1;    background:#b02b27;
    color:#fffaf2;;border:none;border-radius:8px;padding:12px;font-family:'Space Grotesk',sans-serif;font-weight:700;font-size:.88rem;cursor:pointer;letter-spacing:.3px;transition:.15s;}
.btn:hover{   background:#c53a35;}
.btn:disabled{background:var(--line);color:var(--dim);cursor:not-allowed;}
.btn.ghost{background:transparent;border:1px solid var(--line);color:var(--dim);flex:0 0 auto;padding:12px 16px;}
.btn.ghost:hover{border-color:var(--red);color:var(--red);}

/* result / log */
.result{border-radius:10px;padding:14px;margin-bottom:12px;font-family:'JetBrains Mono',monospace;}
.result.ok{
    background:#fff4ef;
    border:1px solid #c53a35;
}

.result.ok .eqline{
    color:#b02b27;
}

.result.no{
    background:#f9ece6;
    border:1px solid #cf3c38;
}

.result.no .eqline{
    color:#cf3c38;
}
.result .eqline{font-size:1.05rem;font-weight:700;color:var(--phos);margin-bottom:4px;word-break:break-word;}
.result.no .eqline{color:var(--red);font-weight:400;font-style:italic;font-size:.85rem;}
.result .cond{color:var(--amber);font-size:.72rem;}
.result .unlockline{color:var(--sand);font-size:.75rem;margin-top:6px;}

.log{max-height:300px;overflow-y:auto;display:flex;flex-direction:column-reverse;gap:8px;}
.logitem{border-left:2px solid var(--phos-dim);padding:6px 0 6px 10px;font-family:'JetBrains Mono',monospace;font-size:.76rem;color:var(--dim);}
.logitem b{color:var(--ink);display:block;font-size:.82rem;margin-bottom:2px;}
.logitem .lcond{color:var(--amber);}

footer{margin-top:26px;color:var(--dim);font-size:.72rem;text-align:center;line-height:1.7;}
footer b{color:var(--phos);}
</style>
</head>
<body>
  <header class="topbar"> 
    <button class="home-origin-btn" onclick="window.location.href='https://2410phongnguyen-eng.github.io/Koi/'">
    <span class="btn-icon">🏯</span>
    <span class="btn-text">
        <small>TRANG CHỦ</small>
        <strong>Nishiki Hub</strong>
    </span>
</button>
  </header>
<div class="wrap">

<header>
  <div class="brand">
    <svg class="flaskmark" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
      <path d="M40 10 L60 10 L60 38 L82 78 Q86 86 76 86 L24 86 Q14 86 18 78 L40 38 Z" fill="none" stroke="#2b1a15" stroke-width="4"/>
      <path d="M27 66 L73 66 L76 78 Q78 82 74 82 L26 82 Q22 82 24 78 Z" fill="#b02b27" opacity="0.35"/>
      <circle cx="50" cy="52" r="3" fill="#b02b27"/>
      <circle cx="42" cy="60" r="2" fill="#b02b27"/>
      <circle cx="58" cy="58" r="2.2" fill="##b02b27"/>
    </svg>
    <div>
      <h1>Phòng Thí Nghiệm <span>Ghép Chất</span></h1>
      <div class="sub">Chọn các chất, thả vào bình, và xem phản ứng xảy ra theo đúng phương trình hoá học.</div>
    </div>
  </div>
  <div class="stats">
    <div>Đã mở khoá<b id="statUnlocked">0/0</b></div>
    <div>Phản ứng đã xảy ra<b id="statReactions">0</b></div>
  </div>
</header>

<div class="grid">

  <!-- LEFT: substances -->
  <div class="panel">
    <h2>Kho chất — bấm để thêm vào bình</h2>
    <input class="searchbox" id="search" placeholder="Tìm theo công thức hoặc tên… (vd: Na, sắt, axit)">
    <div class="tabs" id="tabs"></div>
    <div class="tiles" id="tiles"></div>
  </div>

  <!-- RIGHT: flask + result -->
  <div>
    <div class="panel" style="margin-bottom:16px;">
      <h2>Bình phản ứng</h2>
      <div class="flaskzone empty" id="flask"></div>
      <div class="actions">
        <button class="btn" id="reactBtn" disabled> Thực hiện phản ứng</button>
        <button class="btn ghost" id="clearBtn">Đổ bỏ</button>
      </div>
      <div id="resultArea"></div>
    </div>

    <div class="panel">
      <h2>Nhật ký phản ứng</h2>
      <div class="log" id="log"><div class="logitem" style="border:none;color:var(--dim);font-style:italic;">Chưa có phản ứng nào được thực hiện.</div></div>
    </div>
  </div>

</div>

<footer>
  Cơ sở dữ liệu gồm <b id="fCount">0</b> chất và <b id="fReact">0</b> phương trình phản ứng vô cơ &amp; hữu cơ (đủ để khám phá dây chuyền phản ứng từ đơn chất đến hợp chất phức tạp).<br>
  Trộn nhiều chất trong bình rồi bấm "Thực hiện phản ứng" — engine sẽ tự tìm phương trình phù hợp nhất với tổ hợp chất bạn chọn.
</footer>

</div>

<script>
/* =========================================================
   DATABASE — substances
   c: category -> element | oxide | base | acid | salt | organic | other
   ========================================================= */
const S = {


Na:{f:"Na",n:"Natri",c:"element"}, K:{f:"K",n:"Kali",c:"element"}, Ca:{f:"Ca",n:"Canxi",c:"element"},
Ba:{f:"Ba",n:"Bari",c:"element"}, Mg:{f:"Mg",n:"Magie",c:"element"}, Al:{f:"Al",n:"Nhôm",c:"element"},
Zn:{f:"Zn",n:"Kẽm",c:"element"}, Fe:{f:"Fe",n:"Sắt",c:"element"}, Ni:{f:"Ni",n:"Niken",c:"element"},
Sn:{f:"Sn",n:"Thiếc",c:"element"}, Pb:{f:"Pb",n:"Chì",c:"element"}, Cu:{f:"Cu",n:"Đồng",c:"element"},
Ag:{f:"Ag",n:"Bạc",c:"element"}, Hg:{f:"Hg",n:"Thủy ngân",c:"element"}, Au:{f:"Au",n:"Vàng",c:"element"},
H2:{f:"H<sub>2</sub>",n:"Hiđro",c:"element"},O3:{f:"O₃",n:"Ozon",c:"element"}, O2:{f:"O<sub>2</sub>",n:"Oxi",c:"element"}, N2:{f:"N<sub>2</sub>",n:"Nitơ",c:"element"},
Cl2:{f:"Cl<sub>2</sub>",n:"Clo",c:"element"}, Br2:{f:"Br<sub>2</sub>",n:"Brom",c:"element"}, I2:{f:"I<sub>2</sub>",n:"Iot",c:"element"},
F2:{f:"F<sub>2</sub>",n:"Flo",c:"element"}, S:{f:"S",n:"Lưu huỳnh",c:"element"}, C:{f:"C",n:"Cacbon",c:"element"},
P:{f:"P",n:"Photpho",c:"element"},
 Si:{f:"Si",n:"Silic",c:"element"},
Mn:{f:"Mn",n:"Mangan",c:"element"},
Cr:{f:"Cr",n:"Crôm",c:"element"},
  Li:{f:"Li",n:"Liti",c:"element"},
Be:{f:"Be",n:"Berili",c:"element"},
Sr:{f:"Sr",n:"Stronti",c:"element"},
Cd:{f:"Cd",n:"Cadimi",c:"element"},
Co:{f:"Co",n:"Coban",c:"element"},
Li2O:{f:"Li₂O",n:"Liti oxit",c:"oxide"},
BeO:{f:"BeO",n:"Berili oxit",c:"oxide"},
SrO:{f:"SrO",n:"Stronti oxit",c:"oxide"},
CdO:{f:"CdO",n:"Cadimi oxit",c:"oxide"},
CoO:{f:"CoO",n:"Coban(II) oxit",c:"oxide"},
Co2O3:{f:"Co₂O₃",n:"Coban(III) oxit",c:"oxide"},

LiOH:{f:"LiOH",n:"Liti hiđroxit",c:"base"},
BeOH2:{f:"Be(OH)₂",n:"Berili hiđroxit",c:"base"},
SrOH2:{f:"Sr(OH)₂",n:"Stronti hiđroxit",c:"base"},
CdOH2:{f:"Cd(OH)₂",n:"Cadimi hiđroxit",c:"base"},
CoOH2:{f:"Co(OH)₂",n:"Coban(II) hiđroxit",c:"base"},

LiCl:{f:"LiCl",n:"Liti clorua",c:"salt"},
LiBr:{f:"LiBr",n:"Liti bromua",c:"salt"},
LiI:{f:"LiI",n:"Liti iodua",c:"salt"},
LiF:{f:"LiF",n:"Liti florua",c:"salt"},

BeCl2:{f:"BeCl₂",n:"Berili clorua",c:"salt"},
SrCl2:{f:"SrCl₂",n:"Stronti clorua",c:"salt"},
CdCl2:{f:"CdCl₂",n:"Cadimi clorua",c:"salt"},
CoCl2:{f:"CoCl₂",n:"Coban(II) clorua",c:"salt"},

Li2CO3:{f:"Li₂CO₃",n:"Liti cacbonat",c:"salt"},
Li2SO4:{f:"Li₂SO₄",n:"Liti sunfat",c:"salt"},
LiNO3:{f:"LiNO₃",n:"Liti nitrat",c:"salt"},
Li3PO4:{f:"Li₃PO₄",n:"Liti photphat",c:"salt"},
Li2S:{f:"Li₂S",n:"Liti sunfua",c:"salt"},

BeSO4:{f:"BeSO₄",n:"Berili sunfat",c:"salt"},
SrSO4:{f:"SrSO₄",n:"Stronti sunfat",c:"salt"},
CdSO4:{f:"CdSO₄",n:"Cadimi sunfat",c:"salt"},
CoSO4:{f:"CoSO₄",n:"Coban(II) sunfat",c:"salt"},

Na2O2:{f:"Na<sub>2</sub>O<sub>2</sub>",n:"Natri peroxit",c:"oxide"},
K2O2:{f:"K<sub>2</sub>O<sub>2</sub>",n:"Kali peroxit",c:"oxide"},
CaO2:{f:"CaO<sub>2</sub>",n:"Canxi peroxit",c:"oxide"},
BaO2:{f:"BaO<sub>2</sub>",n:"Bari peroxit",c:"oxide"},
MnO2:{f:"MnO<sub>2</sub>",n:"Mangan(IV) oxit",c:"oxide"},
Na2O:{f:"Na<sub>2</sub>O",n:"Natri oxit",c:"oxide"}, K2O:{f:"K<sub>2</sub>O",n:"Kali oxit",c:"oxide"},
CaO:{f:"CaO",n:"Canxi oxit (vôi sống)",c:"oxide"}, BaO:{f:"BaO",n:"Bari oxit",c:"oxide"},
MgO:{f:"MgO",n:"Magie oxit",c:"oxide"}, Al2O3:{f:"Al<sub>2</sub>O<sub>3</sub>",n:"Nhôm oxit",c:"oxide"},
ZnO:{f:"ZnO",n:"Kẽm oxit",c:"oxide"}, FeO:{f:"FeO",n:"Sắt(II) oxit",c:"oxide"},
Fe2O3:{f:"Fe<sub>2</sub>O<sub>3</sub>",n:"Sắt(III) oxit",c:"oxide"},
FeO:{f:"FeO",n:"Sắt(II) oxit",c:"oxide"},
 Fe3O4:{f:"Fe<sub>3</sub>O<sub>4</sub>",n:"Oxit sắt từ",c:"oxide"},
CuO:{f:"CuO",n:"Đồng(II) oxit",c:"oxide"}, Cu2O:{f:"Cu<sub>2</sub>O",n:"Đồng(I) oxit",c:"oxide"},
CO2:{f:"CO<sub>2</sub>",n:"Cacbon đioxit",c:"oxide"}, CO:{f:"CO",n:"Cacbon monoxit",c:"oxide"},
SO2:{f:"SO<sub>2</sub>",n:"Lưu huỳnh đioxit",c:"oxide"}, SO3:{f:"SO<sub>3</sub>",n:"Lưu huỳnh trioxit",c:"oxide"},
NO:{f:"NO",n:"Nitơ monoxit",c:"oxide"}, NO2:{f:"NO<sub>2</sub>",n:"Nitơ đioxit",c:"oxide"},
N2O5:{f:"N<sub>2</sub>O<sub>5</sub>",n:"Đinitơ pentaoxit",c:"oxide"}, P2O5:{f:"P<sub>2</sub>O<sub>5</sub>",n:"Điphotpho pentaoxit",c:"oxide"},
SiO2:{f:"SiO<sub>2</sub>",n:"Silic đioxit",c:"oxide"}, H2O:{f:"H<sub>2</sub>O",n:"Nước",c:"oxide"},
H2O2:{f:"H<sub>2</sub>O<sub>2</sub>",n:"Oxi già",c:"oxide"},
Cr2O3:{f:"Cr<sub>2</sub>O<sub>3</sub>",n:"Crôm(III) oxit",c:"oxide"},
Ag2O:{f:"Ag<sub>2</sub>O",n:"Bạc oxit",c:"oxide"},



NaOH:{f:"NaOH",n:"Natri hiđroxit",c:"base"}, KOH:{f:"KOH",n:"Kali hiđroxit",c:"base"},
CaOH2:{f:"Ca(OH)<sub>2</sub>",n:"Canxi hiđroxit",c:"base"}, BaOH2:{f:"Ba(OH)<sub>2</sub>",n:"Bari hiđroxit",c:"base"},
MgOH2:{f:"Mg(OH)<sub>2</sub>",n:"Magie hiđroxit",c:"base"}, AlOH3:{f:"Al(OH)<sub>3</sub>",n:"Nhôm hiđroxit",c:"base"},
ZnOH2:{f:"Zn(OH)<sub>2</sub>",n:"Kẽm hiđroxit",c:"base"}, FeOH2:{f:"Fe(OH)<sub>2</sub>",n:"Sắt(II) hiđroxit",c:"base"},
FeOH3:{f:"Fe(OH)<sub>3</sub>",n:"Sắt(III) hiđroxit",c:"base"}, CuOH2:{f:"Cu(OH)<sub>2</sub>",n:"Đồng(II) hiđroxit",c:"base"},
NH3H2O:{f:"NH<sub>3</sub>·H<sub>2</sub>O",n:"Amoniac (dd)",c:"base"},

HCl:{f:"HCl",n:"Axit clohiđric",c:"acid"},
"H2SO4 loãng":{f:"H<sub>2</sub>SO<sub>4</sub> loãng",n:"Axit sunfuric loãng",c:"acid"},
"H2SO4 đặc":{f:"H<sub>2</sub>SO<sub>4</sub> đặc",n:"Axit sunfuric đặc",c:"acid"},
"H2SO4.nSO3":{f:"H<sub>2</sub>SO<sub>4</sub>.nSO<sub>3</sub>",n:"Oleum",c:"other"},
H2S2O8:{f:"H<sub>2</sub>S<sub>2</sub>O<sub>8</sub>",n:"Axit peroxydisulfuric",c:"acid"},

H2SO3:{f:"H<sub>2</sub>SO<sub>3</sub>",n:"Axit sunfurơ",c:"acid"}, HNO3:{f:"HNO<sub>3</sub>",n:"Axit nitric",c:"acid"},
H2CO3:{f:"H<sub>2</sub>CO<sub>3</sub>",n:"Axit cacbonic",c:"acid"}, H3PO4:{f:"H<sub>3</sub>PO<sub>4</sub>",n:"Axit photphoric",c:"acid"},
H2S:{f:"H<sub>2</sub>S",n:"Axit sunfuhiđric",c:"acid"}, HF:{f:"HF",n:"Axit flohiđric",c:"acid"},
HBr:{f:"HBr",n:"Axit bromhiđric",c:"acid"}, HI:{f:"HI",n:"Axit iothiđric",c:"acid"},
HIO:{f:"HIO",n:"Axit iot",c:"acid"},HClO:{f:"HClO",n:"Axit hipoclorit",c:"acid"},HBrO:{f:"HBrO",n:"Axit bromit",c:"acid"},
K2MnO4:{f:"K₂MnO₄",n:"Kali manganat",c:"salt"},
KMnO4:{f:"KMnO₄",n:"Kali pemanganat",c:"salt"},
K2CrO7:{f:"K₂CrO₇",n:"Kali cromat",c:"salt"},
NaCl:{f:"NaCl",n:"Natri clorua",c:"salt"}, KCl:{f:"KCl",n:"Kali clorua",c:"salt"},
CaCl2:{f:"CaCl<sub>2</sub>",n:"Canxi clorua",c:"salt"}, BaCl2:{f:"BaCl<sub>2</sub>",n:"Bari clorua",c:"salt"},
MgCl2:{f:"MgCl<sub>2</sub>",n:"Magie clorua",c:"salt"},
 AlCl3:{f:"AlCl<sub>3</sub>",n:"Nhôm clorua",c:"salt"},
  AlBr3:{f:"AlBr<sub>3</sub>",n:"Nhôm bromua",c:"salt"},
   AlI3:{f:"AlI<sub>3</sub>",n:"Nhôm iodide",c:"salt"},
    AlF3:{f:"AlF<sub>3</sub>",n:"Nhôm fluorua",c:"salt"},
ZnCl2:{f:"ZnCl<sub>2</sub>",n:"Kẽm clorua",c:"salt"}, FeCl2:{f:"FeCl<sub>2</sub>",n:"Sắt(II) clorua",c:"salt"},
FeCl3:{f:"FeCl<sub>3</sub>",n:"Sắt(III) clorua",c:"salt"},
 FeBr3:{f:"FeBr<sub>3</sub>",n:"Sắt(III) bromua",c:"salt"}, 
 FeI3:{f:"FeI<sub>3</sub>",n:"Sắt(III) iodide",c:"salt"}, 
 FeF3:{f:"FeF<sub>3</sub>",n:"Sắt(III) fluorua",c:"salt"},

CuCl2:{f:"CuCl<sub>2</sub>",n:"Đồng(II) clorua",c:"salt"},
CuBr2:{f:"CuBr<sub>2</sub>",n:"Đồng(II) bromua",c:"salt"},
CuI2:{f:"CuI<sub>2</sub>",n:"Đồng(II) iodide",c:"salt"},
CuF2:{f:"CuF<sub>2</sub>",n:"Đồng(II) fluorua",c:"salt"},
AgCl:{f:"AgCl",n:"Bạc clorua (↓trắng)",c:"salt"}, 
HgCl2:{f:"HgCl<sub>2</sub>",n:"Thuỷ ngân(II) clorua",c:"salt"},
NH4Cl:{f:"NH<sub>4</sub>Cl",n:"Amoni clorua",c:"salt"},
 NiCl2:{f:"NiCl<sub>2</sub>",n:"Niken clorua",c:"salt"},
SnCl2:{f:"SnCl<sub>2</sub>",n:"Thiếc(II) clorua",c:"salt"}, 
PbCl2:{f:"PbCl<sub>2</sub>",n:"Chì(II) clorua",c:"salt"},


 NaClO:{f:"NaClO",n:"Natri hipoclorit",c:"salt"},
KClO3:{f:"KClO₃",n:"Kali clorat",c:"salt"},
CaOCl2:{f:"CaOCl₂",n:"Canxi hipoclorit",c:"salt"},
BaOCl2:{f:"BaOCl₂",n:"Bari hipoclorit",c:"salt"},
Na2SO4:{f:"Na<sub>2</sub>SO<sub>4</sub>",n:"Natri sunfat",c:"salt"}, 
K2SO4:{f:"K<sub>2</sub>SO<sub>4</sub>",n:"Kali sunfat",c:"salt"},
CaSO4:{f:"CaSO<sub>4</sub>",n:"Canxi sunfat",c:"salt"}, 
BaSO4:{f:"BaSO<sub>4</sub>",n:"Bari sunfat (↓trắng)",c:"salt"},
MgSO4:{f:"MgSO<sub>4</sub>",n:"Magie sunfat",c:"salt"},
 Al2SO43:{f:"Al<sub>2</sub>(SO<sub>4</sub>)<sub>3</sub>",n:"Nhôm sunfat",c:"salt"},
ZnSO4:{f:"ZnSO<sub>4</sub>",n:"Kẽm sunfat",c:"salt"},
 FeSO4:{f:"FeSO<sub>4</sub>",n:"Sắt(II) sunfat",c:"salt"},
Fe2SO43:{f:"Fe<sub>2</sub>(SO<sub>4</sub>)<sub>3</sub>",n:"Sắt(III) sunfat",c:"salt"},
 CuSO4:{f:"CuSO<sub>4</sub>",n:"Đồng(II) sunfat",c:"salt"},
Ag2SO4:{f:"Ag<sub>2</sub>SO<sub>4</sub>",n:"Bạc sunfat (↓)",c:"salt"}, 
NH42SO4:{f:"(NH<sub>4</sub>)<sub>2</sub>SO<sub>4</sub>",n:"Amoni sunfat",c:"salt"},

Na2SO3:{f:"Na<sub>2</sub>SO<sub>3</sub>",n:"Natri sunfit",c:"salt"},

Na2CO3:{f:"Na<sub>2</sub>CO<sub>3</sub>",n:"Natri cacbonat",c:"salt"}, 
K2CO3:{f:"K<sub>2</sub>CO<sub>3</sub>",n:"Kali cacbonat",c:"salt"},
CaCO3:{f:"CaCO<sub>3</sub>",n:"Canxi cacbonat (đá vôi)",c:"salt"},
 BaCO3:{f:"BaCO<sub>3</sub>",n:"Bari cacbonat",c:"salt"},
MgCO3:{f:"MgCO<sub>3</sub>",n:"Magie cacbonat",c:"salt"},
 NaHCO3:{f:"NaHCO<sub>3</sub>",n:"Natri hiđrocacbonat",c:"salt"},
KHCO3:{f:"KHCO<sub>3</sub>",n:"Kali hiđrocacbonat",c:"salt"}, 
CaHCO32:{f:"Ca(HCO<sub>3</sub>)<sub>2</sub>",n:"Canxi hiđrocacbonat",c:"salt"},
NH4HCO3:{f:"NH<sub>4</sub>HCO<sub>3</sub>",n:"Amoni hiđrocacbonat",c:"salt"},
K2SO3:{f:"K<sub>2</sub>SO<sub>3</sub>",n:"Kali sunfit",c:"salt"},
CaSO3:{f:"CaSO<sub>3</sub>",n:"Canxi sunfit",c:"salt"},
 BaSO3:{f:"BaSO<sub>3</sub>",n:"Bari sunfit",c:"salt"},
 NaHSO3:{f:"NaHSO<sub>3</sub>",n:"Natri hiđrosunfit",c:"salt"},
KHSO3:{f:"KHSO<sub>3</sub>",n:"Kali hiđrosunfit",c:"salt"}, 
CaHSO32:{f:"Ca(HSO<sub>3</sub>)<sub>2</sub>",n:"Canxi hiđrosunfit",c:"salt"},
NH4HSO3:{f:"NH<sub>4</sub>HSO<sub>3</sub>",n:"Amoni hiđrosunfit",c:"salt"},


NaNO3:{f:"NaNO<sub>3</sub>",n:"Natri nitrat",c:"salt"}, 
KNO3:{f:"KNO<sub>3</sub>",n:"Kali nitrat",c:"salt"},
CaNO32:{f:"Ca(NO<sub>3</sub>)<sub>2</sub>",n:"Canxi nitrat",c:"salt"}, 
AgNO3:{f:"AgNO<sub>3</sub>",n:"Bạc nitrat",c:"salt"},
CuNO32:{f:"Cu(NO<sub>3</sub>)<sub>2</sub>",n:"Đồng(II) nitrat",c:"salt"}, 
FeNO32:{f:"Fe(NO<sub>3</sub>)<sub>2</sub>",n:"Sắt(II) nitrat",c:"salt"},
FeNO33:{f:"Fe(NO<sub>3</sub>)<sub>3</sub>",n:"Sắt(III) nitrat",c:"salt"},
 ZnNO32:{f:"Zn(NO<sub>3</sub>)<sub>2</sub>",n:"Kẽm nitrat",c:"salt"},
AlNO33:{f:"Al(NO<sub>3</sub>)<sub>3</sub>",n:"Nhôm nitrat",c:"salt"}, 
NH4NO3:{f:"NH<sub>4</sub>NO<sub>3</sub>",n:"Amoni nitrat",c:"salt"},

Na3PO4:{f:"Na<sub>3</sub>PO<sub>4</sub>",n:"Natri photphat",c:"salt"},
 Ca3PO42:{f:"Ca<sub>3</sub>(PO<sub>4</sub>)<sub>2</sub>",n:"Canxi photphat",c:"salt"},
Ag3PO4:{f:"Ag<sub>3</sub>PO<sub>4</sub>",n:"Bạc photphat (↓vàng)",c:"salt"},
 Ba3PO42:{f:"Ba<sub>3</sub>(PO<sub>4</sub>)<sub>2</sub>",n:"Bari photphat",c:"salt"},
 Na3PO4:{f:"Na<sub>3</sub>PO<sub>4</sub>",n:"Natri photphat",c:"salt"},
 K3PO4:{f:"K<sub>3</sub>PO<sub>4</sub>",n:"Kali photphat",c:"salt"},
 Cu3PO42:{f:"Cu<sub>3</sub>(PO<sub>4</sub>)<sub>2</sub>",n:"Đồng(II) photphat",c:"salt"},
 Fe3PO42:{f:"Fe<sub>3</sub>(PO<sub>4</sub>)<sub>2</sub>",n:"Sắt(II) photphat",c:"salt"},
 FePO4:{f:"Fe<sub>3</sub>PO<sub>4</sub>",n:"Sắt(III) photphat",c:"salt"},
 Mg3PO42:{f:"Mg<sub>3</sub>(PO<sub>4</sub>)<sub>2</sub>",n:"Magie photphat",c:"salt"},
 Zn3PO42:{f:"Zn<sub>3</sub>(PO<sub>4</sub>)<sub>2</sub>",n:"Kẽm photphat",c:"salt"},
 AlPO4:{f:"AlPO<sub>4</sub>",n:"Nhôm photphat",c:"salt"},


Na2S:{f:"Na<sub>2</sub>S",n:"Natri sunfua",c:"salt"}, FeS:{f:"FeS",n:"Sắt(II) sunfua",c:"salt"},
CuS:{f:"CuS",n:"Đồng(II) sunfua (↓đen)",c:"salt"}, ZnS:{f:"ZnS",n:"Kẽm sunfua",c:"salt"},
Ag2S:{f:"Ag<sub>2</sub>S",n:"Bạc sunfua (↓đen)",c:"salt"}, PbS:{f:"PbS",n:"Chì(II) sunfua",c:"salt"},

NaBr:{f:"NaBr",n:"Natri bromua",c:"salt"}, NaI:{f:"NaI",n:"Natri iotua",c:"salt"},
KI:{f:"KI",n:"Kali iotua",c:"salt"}, KBr:{f:"KBr",n:"Kali bromua",c:"salt"},
NaClO:{f:"NaClO",n:"Natri hipoclorit (nước Gia-ven)",c:"salt"},
NaAlO2:{f:"NaAlO₂",n:"Natri aluminat",c:"salt"},
KAlO2:{f:"KAlO₂",n:"Kali aluminat",c:"salt"},
CaAlO22:{f:"Ca(AlO₂)₂",n:"Canxi aluminat",c:"salt"},
BaAlO22:{f:"Ba(AlO₂)₂",n:"Barium aluminat",c:"salt"},
Na2ZnO2:{f:"Na2ZnO2",n:"Natri zincat",c:"salt"},
K2ZnO2:{f:"K2ZnO2",n:"Kali zincat",c:"salt"},
CaZnO2:{f:"CaZnO2",n:"Canxi zincat",c:"salt"},
BaZnO2:{f:"BaZnO2",n:"Barium zincat",c:"salt"},

CH4:{f:"CH<sub>4</sub>",n:"Metan",c:"organic"}, C2H2:{f:"C<sub>2</sub>H<sub>2</sub>",n:"Axetilen",c:"organic"},
C2H4:{f:"C<sub>2</sub>H<sub>4</sub>",n:"Etilen",c:"organic"}, C2H6:{f:"C<sub>2</sub>H<sub>6</sub>",n:"Etan",c:"organic"},
C6H6:{f:"C<sub>6</sub>H<sub>6</sub>",n:"Benzen",c:"organic"}, C2H5OH:{f:"C<sub>2</sub>H<sub>5</sub>OH",n:"Ancol etylic",c:"organic"},
CH3OH:{f:"CH<sub>3</sub>OH",n:"Ancol metylic",c:"organic"}, HCHO:{f:"HCHO",n:"Fomanđehit",c:"organic"},
CH3CHO:{f:"CH<sub>3</sub>CHO",n:"Axetanđehit",c:"organic"}, CH3COOH:{f:"CH<sub>3</sub>COOH",n:"Axit axetic",c:"organic"},
CH3COONa:{f:"CH<sub>3</sub>COONa",n:"Natri axetat",c:"organic"}, CH3COOC2H5:{f:"CH<sub>3</sub>COOC<sub>2</sub>H<sub>5</sub>",n:"Etyl axetat",c:"organic"},
C6H12O6:{f:"C<sub>6</sub>H<sub>12</sub>O<sub>6</sub>",n:"Glucozơ",c:"organic"}, CaC2:{f:"CaC<sub>2</sub>",n:"Canxi cacbua",c:"organic"},
Al4C3:{f:"Al<sub>4</sub>C<sub>3</sub>",n:"Nhôm cacbua",c:"organic"}, CH3Cl:{f:"CH<sub>3</sub>Cl",n:"Clometan",c:"organic"},
C2H5Cl:{f:"C<sub>2</sub>H<sub>5</sub>Cl",n:"Cloetan",c:"organic"}, C2H5ONa:{f:"C<sub>2</sub>H<sub>5</sub>ONa",n:"Natri etylat",c:"organic"},
CH4:{f:"CH₄",n:"Metan",c:"organic"},
CH3OH:{f:"CH₃OH",n:"Metanol",c:"organic"},
CH2O:{f:"CH₂O",n:"Fomanđehit",c:"organic"},
HCOOH:{f:"HCOOH",n:"Axit fomic",c:"organic"},
HCOONa:{f:"HCOONa",n:"Natri fomat",c:"salt"},
CH3Cl:{f:"CH₃Cl",n:"Clometan",c:"organic"},
C2H5Cl:{f:"C₂H₅Cl",n:"Cloetan",c:"organic"},
C2H5OC2H5:{f:"C₂H₅OC₂H₅",n:"Đietyl ete",c:"organic"},
CH3COOCH3:{f:"CH₃COOCH₃",n:"Metyl axetat",c:"organic"},
HCOOC2H5:{f:"HCOOC₂H₅",n:"Etyl fomat",c:"organic"},
C3H8:{f:"C₃H₈",n:"Propan",c:"organic"},
C3H8O:{f:"C₃H₈O",n:"Propanol",c:"organic"},
CH3COCH3:{f:"CH₃COCH₃",n:"Axeton",c:"organic"},
C3H8O3:{f:"C₃H₈O₃",n:"Glixerol",c:"organic"},
C3H5N3O9:{f:"C₃H₅N₃O₉",n:"Nitroglixerin",c:"organic"},
C12H22O11:{f:"C₁₂H₂₂O₁₁",n:"Saccarozơ",c:"organic"},
NH2CONH2:{f:"NH₂CONH₂",n:"Urê",c:"organic"},
CH2CHCl:{f:"CH₂=CHCl",n:"Vinyl clorua",c:"organic"},
PP:{f:"PP",n:"Polipropilen",c:"polymer"},
CH3CHO:{f:"CH₃CHO",n:"Anđehit axetic",c:"organic"},
CH3COOH:{f:"CH₃COOH",n:"Axit axetic",c:"organic"},
CH3COONa:{f:"CH₃COONa",n:"Natri axetat",c:"salt"},
C2F4:{f:"CF₂=CF₂",n:"Tetrafloetylen",c:"organic"},
PTFE:{f:"PTFE",n:"Politetrafluoroetylen (Teflon)",c:"polymer"},

MMA:{f:"MMA",n:"Metyl metacrylat",c:"organic"},
PMMA:{f:"PMMA",n:"Polymetyl metacrylat",c:"polymer"},

VAc:{f:"VAc",n:"Vinyl axetat",c:"organic"},
PVAc:{f:"PVAc",n:"Polyvinyl axetat",c:"polymer"},
PVA:{f:"PVA",n:"Polyvinyl ancol",c:"polymer"},

AN:{f:"CH₂=CHCN",n:"Acrylonitril",c:"organic"},
PAN:{f:"PAN",n:"Polyacrylonitril",c:"polymer"},

Butadien:{f:"CH₂=CHCH=CH₂",n:"Buta-1,3-đien",c:"organic"},
PB:{f:"PB",n:"Polybutadien",c:"polymer"},

Isopren:{f:"C₅H₈",n:"Isopren",c:"organic"},
PI:{f:"PI",n:"Polyisopren",c:"polymer"},

Styren:{f:"C₈H₈",n:"Stiren",c:"organic"},
SBR:{f:"SBR",n:"Cao su Buna-S",c:"polymer"},
NBR:{f:"NBR",n:"Cao su Buna-N",c:"polymer"},

EG:{f:"HOCH₂CH₂OH",n:"Etylen glicol",c:"organic"},
TPA:{f:"HOOC-C₆H₄-COOH",n:"Axit terephtalic",c:"organic"},
PET:{f:"PET",n:"Polietilen terephtalat",c:"polymer"},

Caprolactam:{f:"Caprolactam",n:"Caprolactam",c:"organic"},
Nylon6:{f:"Nylon-6",n:"Nylon-6",c:"polymer"},

HMDA:{f:"H₂N(CH₂)₆NH₂",n:"Hexametylenđiamin",c:"organic"},
AdipicAcid:{f:"HOOC(CH₂)₄COOH",n:"Axit adipic",c:"organic"},
Nylon66:{f:"Nylon-6,6",n:"Nylon-6,6",c:"polymer"},

Phenol:{f:"C₆H₅OH",n:"Phenol",c:"organic"},
Bakelite:{f:"Bakelite",n:"Nhựa Bakelit",c:"polymer"},

BisphenolA:{f:"Bisphenol A",n:"Bisphenol A",c:"organic"},
Phosgene:{f:"COCl₂",n:"Photgen",c:"organic"},
PC:{f:"PC",n:"Polycarbonate",c:"polymer"},

POM:{f:"POM",n:"Polyoxymetylen",c:"polymer"},

LacticAcid:{f:"CH₃CH(OH)COOH",n:"Axit lactic",c:"organic"},
PLA:{f:"PLA",n:"Polylactic acid",c:"polymer"},

Diisocyanate:{f:"Diisocyanate",n:"Điisoxianat",c:"organic"},
Polyol:{f:"Polyol",n:"Polyol",c:"organic"},
PU:{f:"PU",n:"Polyurethane",c:"polymer"},

Epichlorohydrin:{f:"Epichlorohydrin",n:"Epiclohiđrin",c:"organic"},
Epoxy:{f:"Epoxy",n:"Nhựa epoxy",c:"polymer"},

Dimethyldichlorosilane:{f:"(CH₃)₂SiCl₂",n:"Đimetyl điclo silan",c:"organic"},
Silicone:{f:"Silicone",n:"Silicone",c:"polymer"},

PPD:{f:"PPD",n:"p-Phenylenediamine",c:"organic"},
TPC:{f:"TPC",n:"Terephthaloyl chloride",c:"organic"},
Kevlar:{f:"Kevlar",n:"Kevlar",c:"polymer"},
CH3COOC2H5:{f:"CH₃COOC₂H₅",n:"Etyl axetat",c:"organic"},

C6H12O6:{f:"C₆H₁₂O₆",n:"Glucozơ",c:"organic"},

C6H12:{f:"C₆H₁₂",n:"Xiclohexan",c:"organic"},
C6H5Cl:{f:"C₆H₅Cl",n:"Clobenzen",c:"organic"},

PE:{f:"PE",n:"Polietilen",c:"polymer"},
PVC:{f:"PVC",n:"Polivinyl clorua",c:"polymer"},
PS:{f:"PS",n:"Polistiren",c:"polymer"},

BeBr2:{f:"BeBr₂",n:"Berili bromua",c:"salt"},
SrBr2:{f:"SrBr₂",n:"Stronti bromua",c:"salt"},
CdBr2:{f:"CdBr₂",n:"Cadimi bromua",c:"salt"},
CoBr2:{f:"CoBr₂",n:"Coban(II) bromua",c:"salt"},

BeI2:{f:"BeI₂",n:"Berili iodua",c:"salt"},
SrI2:{f:"SrI₂",n:"Stronti iodua",c:"salt"},
CdI2:{f:"CdI₂",n:"Cadimi iodua",c:"salt"},
CoI2:{f:"CoI₂",n:"Coban(II) iodua",c:"salt"},

BeF2:{f:"BeF₂",n:"Berili florua",c:"salt"},
SrF2:{f:"SrF₂",n:"Stronti florua",c:"salt"},
CdF2:{f:"CdF₂",n:"Cadimi florua",c:"salt"},
CoF2:{f:"CoF₂",n:"Coban(II) florua",c:"salt"},

BeS:{f:"BeS",n:"Berili sunfua",c:"salt"},
SrS:{f:"SrS",n:"Stronti sunfua",c:"salt"},
CdS:{f:"CdS",n:"Cadimi sunfua",c:"salt"},
CoS:{f:"CoS",n:"Coban(II) sunfua",c:"salt"},

SrNO32:{f:"Sr(NO₃)₂",n:"Stronti nitrat",c:"salt"},
CdNO32:{f:"Cd(NO₃)₂",n:"Cadimi nitrat",c:"salt"},
CoNO32:{f:"Co(NO₃)₂",n:"Coban(II) nitrat",c:"salt"},

Sr3PO42:{f:"Sr₃(PO₄)₂",n:"Stronti photphat",c:"salt"},
Cd3PO42:{f:"Cd₃(PO₄)₂",n:"Cadimi photphat",c:"salt"},
Co3PO42:{f:"Co₃(PO₄)₂",n:"Coban(II) photphat",c:"salt"},
//==================== KHÍ ĐẶC BIỆT ====================


ClO2:{f:"ClO₂",n:"Clo đioxit",c:"other"},

NH2OH:{f:"NH₂OH",n:"Hiđroxylamin",c:"other"},
PH3:{f:"PH₃",n:"Photphin",c:"other"},
SiH4:{f:"SiH₄",n:"Silan",c:"other"},
B2H6:{f:"B₂H₆",n:"Điboran",c:"other"},

//==================== PEROXIT ====================

ZnO2:{f:"ZnO₂",n:"Kẽm peoxit",c:"oxide"},
MgO2:{f:"MgO₂",n:"Magie peoxit",c:"oxide"},
SrO2:{f:"SrO₂",n:"Stronti peoxit",c:"oxide"},

//==================== MUỐI KHÁC ====================

Na2S2O3:{f:"Na₂S₂O₃",n:"Natri thiosunfat",c:"salt"},
K2S2O3:{f:"K₂S₂O₃",n:"Kali thiosunfat",c:"salt"},
Na2Cr2O7:{f:"Na₂Cr₂O₇",n:"Natri đicromat",c:"salt"},
K2Cr2O7:{f:"K₂Cr₂O₇",n:"Kali đicromat",c:"salt"},
Na2B4O7:{f:"Na₂B₄O₇",n:"Hàn the",c:"salt"},
NH4ClO4:{f:"NH₄ClO₄",n:"Amoni peclorat",c:"salt"},
KClO4:{f:"KClO₄",n:"Kali peclorat",c:"salt"},
NaClO4:{f:"NaClO₄",n:"Natri peclorat",c:"salt"},
CuCN:{f:"CuCN",n:"Đồng(I) xyanua",c:"salt"},
AgCN:{f:"AgCN",n:"Bạc xyanua",c:"salt"},
KCN:{f:"KCN",n:"Kali xyanua",c:"salt"},
NaCN:{f:"NaCN",n:"Natri xyanua",c:"salt"},

//==================== SILICAT ====================

Na2SiO3:{f:"Na₂SiO₃",n:"Natri silicat",c:"salt"},
K2SiO3:{f:"K₂SiO₃",n:"Kali silicat",c:"salt"},
CaSiO3:{f:"CaSiO₃",n:"Canxi silicat",c:"salt"},
MgSiO3:{f:"MgSiO₃",n:"Magie silicat",c:"salt"},

//==================== BORAT ====================

H3BO3:{f:"H₃BO₃",n:"Axit boric",c:"acid"},
NaBO2:{f:"NaBO₂",n:"Natri metaborat",c:"salt"},
B2O3:{f:"B₂O₃",n:"Bo oxit",c:"oxide"},

//==================== HỢP CHẤT SILIC ====================

SiC:{f:"SiC",n:"Silic cacbua",c:"salt"},
Si3N4:{f:"Si₃N₄",n:"Silic nitrua",c:"salt"},
SiCl4:{f:"SiCl₄",n:"Silic tetraclorua",c:"salt"},

//==================== CACBUA ====================

TiC:{f:"TiC",n:"Titan cacbua",c:"salt"},

//==================== NITRUA ====================

BN:{f:"BN",n:"Bo nitrua",c:"salt"},
AlN:{f:"AlN",n:"Nhôm nitrua",c:"salt"},
Mg3N2:{f:"Mg₃N₂",n:"Magie nitrua",c:"salt"},

//==================== SUNFUA MỚI ====================

MoS2:{f:"MoS₂",n:"Molypden đisunfua",c:"compound"},
CS2:{f:"CS₂",n:"Cacbon đisunfua",c:"organic"},
NH3:{f:"NH<sub>3</sub>",n:"Amoniac",c:"other"},
NaH:{f:"NaH",n:"Natri hydrua",c:"other"},
KH:{f:"KH",n:"Kali hydrua",c:"other"},
BaH2:{f:"BaH₂",n:"Barium hydrua",c:"other"},
CaH2:{f:"CaH₂",n:"Canxi hydrua",c:"other"}
};

/* =========================================================
   REACTIONS
   r: reactant ids, p: product ids, cond: condition text ("" = không cần điều kiện)
   eq: full display equation
   ========================================================= */
const R = [

{r:["Na2SO3","S"],p:["Na2S2O3"],cond:"",eq:"Na₂SO₃ + S → Na₂S₂O₃"},

{r:["SiO2","NaOH"],p:["Na2SiO3","H2O"],cond:"t°",eq:"SiO₂ + 2NaOH → Na₂SiO₃ + H₂O"},

{r:["SiO2","KOH"],p:["K2SiO3","H2O"],cond:"t°",eq:"SiO₂ + 2KOH → K₂SiO₃ + H₂O"},

{r:["CaO","SiO2"],p:["CaSiO3"],cond:"t°",eq:"CaO + SiO₂ → CaSiO₃"},

{r:["MgO","SiO2"],p:["MgSiO3"],cond:"t°",eq:"MgO + SiO₂ → MgSiO₃"},

{r:["B","O2"],p:["B2O3"],cond:"t°",eq:"4B + 3O₂ → 2B₂O₃"},

{r:["B2O3","H2O"],p:["H3BO3"],cond:"",eq:"B₂O₃ + 3H₂O → 2H₃BO₃"},

{r:["Si","C"],p:["SiC"],cond:"2000°C",eq:"Si + C → SiC"},

{r:["Si","Cl2"],p:["SiCl4"],cond:"t°",eq:"Si + 2Cl₂ → SiCl₄"},

{r:["Si","N2"],p:["Si3N4"],cond:"t°",eq:"3Si + 2N₂ → Si₃N₄"},


{r:["Mg","N2"],p:["Mg3N2"],cond:"t°",eq:"3Mg + N₂ → Mg₃N₂"},

{r:["Al","N2"],p:["AlN"],cond:"t°",eq:"2Al + N₂ → 2AlN"},

{r:["B","N2"],p:["BN"],cond:"t°",eq:"2B + N₂ → 2BN"},

{r:["C","S"],p:["CS2"],cond:"t°",eq:"C + 2S → CS₂"},
  // --- kim loại + oxi ---
{r:["Li","O2"],p:["Li2O"],cond:"t°",eq:"4Li + O₂ → 2Li₂O"},
{r:["Be","O2"],p:["BeO"],cond:"t°",eq:"2Be + O₂ → 2BeO"},
{r:["Sr","O2"],p:["SrO"],cond:"t°",eq:"2Sr + O₂ → 2SrO"},
{r:["Cd","O2"],p:["CdO"],cond:"t°",eq:"2Cd + O₂ → 2CdO"},
{r:["Co","O2"],p:["CoO"],cond:"t°",eq:"2Co + O₂ → 2CoO"},
{r:["CoO","O2"],p:["Co2O3"],cond:"t°",eq:"4CoO + O₂ → 2Co₂O₃"},

// --- oxit + nước ---
{r:["Li2O","H2O"],p:["LiOH"],cond:"",eq:"Li₂O + H₂O → 2LiOH"},
{r:["SrO","H2O"],p:["SrOH2"],cond:"",eq:"SrO + H₂O → Sr(OH)₂"},

// --- kim loại + nước ---
{r:["Li","H2O"],p:["LiOH","H2"],cond:"",eq:"2Li + 2H₂O → 2LiOH + H₂↑"},
{r:["Sr","H2O"],p:["SrOH2","H2"],cond:"",eq:"Sr + 2H₂O → Sr(OH)₂ + H₂↑"},

// --- kim loại + clo ---
{r:["Li","Cl2"],p:["LiCl"],cond:"t°",eq:"2Li + Cl₂ → 2LiCl"},
{r:["Be","Cl2"],p:["BeCl2"],cond:"t°",eq:"Be + Cl₂ → BeCl₂"},
{r:["Sr","Cl2"],p:["SrCl2"],cond:"t°",eq:"Sr + Cl₂ → SrCl₂"},
{r:["Cd","Cl2"],p:["CdCl2"],cond:"t°",eq:"Cd + Cl₂ → CdCl₂"},
{r:["Co","Cl2"],p:["CoCl2"],cond:"t°",eq:"Co + Cl₂ → CoCl₂"},

// --- liti + halogen ---
{r:["Li","Br2"],p:["LiBr"],cond:"t°",eq:"2Li + Br₂ → 2LiBr"},
{r:["Li","I2"],p:["LiI"],cond:"t°",eq:"2Li + I₂ → 2LiI"},
{r:["Li","F2"],p:["LiF"],cond:"",eq:"2Li + F₂ → 2LiF"},

// --- axit + kim loại ---
{r:["HCl","Li"],p:["LiCl","H2"],cond:"",eq:"2Li + 2HCl → 2LiCl + H₂↑"},
{r:["HCl","Be"],p:["BeCl2","H2"],cond:"",eq:"Be + 2HCl → BeCl₂ + H₂↑"},
{r:["HCl","Cd"],p:["CdCl2","H2"],cond:"",eq:"Cd + 2HCl → CdCl₂ + H₂↑"},
{r:["HCl","Co"],p:["CoCl2","H2"],cond:"",eq:"Co + 2HCl → CoCl₂ + H₂↑"},

{r:["Li","H2SO4 loãng"],p:["Li2SO4","H2"],cond:"",eq:"2Li + H₂SO₄ loãng → Li₂SO₄ + H₂↑"},
{r:["Be","H2SO4 loãng"],p:["BeSO4","H2"],cond:"",eq:"Be + H₂SO₄ loãng → BeSO₄ + H₂↑"},
{r:["Cd","H2SO4 loãng"],p:["CdSO4","H2"],cond:"",eq:"Cd + H₂SO₄ loãng → CdSO₄ + H₂↑"},
{r:["Co","H2SO4 loãng"],p:["CoSO4","H2"],cond:"",eq:"Co + H₂SO₄ loãng → CoSO₄ + H₂↑"},

// --- bazơ + axit ---
{r:["LiOH","HCl"],p:["LiCl","H2O"],cond:"",eq:"LiOH + HCl → LiCl + H₂O"},
{r:["SrOH2","HCl"],p:["SrCl2","H2O"],cond:"",eq:"Sr(OH)₂ + 2HCl → SrCl₂ + 2H₂O"},
{r:["CdOH2","HCl"],p:["CdCl2","H2O"],cond:"",eq:"Cd(OH)₂ + 2HCl → CdCl₂ + 2H₂O"},
{r:["CoOH2","HCl"],p:["CoCl2","H2O"],cond:"",eq:"Co(OH)₂ + 2HCl → CoCl₂ + 2H₂O"},

// --- oxit + axit ---
{r:["Li2O","HCl"],p:["LiCl","H2O"],cond:"",eq:"Li₂O + 2HCl → 2LiCl + H₂O"},
{r:["BeO","HCl"],p:["BeCl2","H2O"],cond:"",eq:"BeO + 2HCl → BeCl₂ + H₂O"},
{r:["SrO","HCl"],p:["SrCl2","H2O"],cond:"",eq:"SrO + 2HCl → SrCl₂ + H₂O"},
{r:["CdO","HCl"],p:["CdCl2","H2O"],cond:"",eq:"CdO + 2HCl → CdCl₂ + H₂O"},
{r:["CoO","HCl"],p:["CoCl2","H2O"],cond:"",eq:"CoO + 2HCl → CoCl₂ + H₂O"},
// --- kim loại + brom ---
{r:["Be","Br2"],p:["BeBr2"],cond:"t°",eq:"Be + Br₂ → BeBr₂"},
{r:["Sr","Br2"],p:["SrBr2"],cond:"t°",eq:"Sr + Br₂ → SrBr₂"},
{r:["Cd","Br2"],p:["CdBr2"],cond:"t°",eq:"Cd + Br₂ → CdBr₂"},
{r:["Co","Br2"],p:["CoBr2"],cond:"t°",eq:"Co + Br₂ → CoBr₂"},

// --- kim loại + iot ---
{r:["Be","I2"],p:["BeI2"],cond:"t°",eq:"Be + I₂ → BeI₂"},
{r:["Sr","I2"],p:["SrI2"],cond:"t°",eq:"Sr + I₂ → SrI₂"},
{r:["Cd","I2"],p:["CdI2"],cond:"t°",eq:"Cd + I₂ → CdI₂"},
{r:["Co","I2"],p:["CoI2"],cond:"t°",eq:"Co + I₂ → CoI₂"},

// --- kim loại + flo ---
{r:["Be","F2"],p:["BeF2"],cond:"",eq:"Be + F₂ → BeF₂"},
{r:["Sr","F2"],p:["SrF2"],cond:"",eq:"Sr + F₂ → SrF₂"},
{r:["Cd","F2"],p:["CdF2"],cond:"",eq:"Cd + F₂ → CdF₂"},
{r:["Co","F2"],p:["CoF2"],cond:"",eq:"Co + F₂ → CoF₂"},

// --- kim loại + lưu huỳnh ---
{r:["Li","S"],p:["Li2S"],cond:"t°",eq:"2Li + S → Li₂S"},
{r:["Be","S"],p:["BeS"],cond:"t°",eq:"Be + S → BeS"},
{r:["Sr","S"],p:["SrS"],cond:"t°",eq:"Sr + S → SrS"},
{r:["Cd","S"],p:["CdS"],cond:"t°",eq:"Cd + S → CdS"},
{r:["Co","S"],p:["CoS"],cond:"t°",eq:"Co + S → CoS"},

// --- oxit + H2SO4 loãng ---
{r:["Li2O","H2SO4 loãng"],p:["Li2SO4","H2O"],cond:"",eq:"Li₂O + H₂SO₄ → Li₂SO₄ + H₂O"},
{r:["BeO","H2SO4 loãng"],p:["BeSO4","H2O"],cond:"",eq:"BeO + H₂SO₄ → BeSO₄ + H₂O"},
{r:["SrO","H2SO4 loãng"],p:["SrSO4","H2O"],cond:"",eq:"SrO + H₂SO₄ → SrSO₄ + H₂O"},
{r:["CdO","H2SO4 loãng"],p:["CdSO4","H2O"],cond:"",eq:"CdO + H₂SO₄ → CdSO₄ + H₂O"},
{r:["CoO","H2SO4 loãng"],p:["CoSO4","H2O"],cond:"",eq:"CoO + H₂SO₄ → CoSO₄ + H₂O"},

// --- bazơ + H2SO4 ---
{r:["LiOH","H2SO4 loãng"],p:["Li2SO4","H2O"],cond:"",eq:"2LiOH + H₂SO₄ → Li₂SO₄ + 2H₂O"},
{r:["SrOH2","H2SO4 loãng"],p:["SrSO4","H2O"],cond:"",eq:"Sr(OH)₂ + H₂SO₄ → SrSO₄ + 2H₂O"},
{r:["CdOH2","H2SO4 loãng"],p:["CdSO4","H2O"],cond:"",eq:"Cd(OH)₂ + H₂SO₄ → CdSO₄ + 2H₂O"},
{r:["CoOH2","H2SO4 loãng"],p:["CoSO4","H2O"],cond:"",eq:"Co(OH)₂ + H₂SO₄ → CoSO₄ + 2H₂O"},

// --- bazơ + HNO3 ---
{r:["LiOH","HNO3"],p:["LiNO3","H2O"],cond:"",eq:"LiOH + HNO₃ → LiNO₃ + H₂O"},
{r:["SrOH2","HNO3"],p:["SrNO32","H2O"],cond:"",eq:"Sr(OH)₂ + 2HNO₃ → Sr(NO₃)₂ + 2H₂O"},
{r:["CdOH2","HNO3"],p:["CdNO32","H2O"],cond:"",eq:"Cd(OH)₂ + 2HNO₃ → Cd(NO₃)₂ + 2H₂O"},
{r:["CoOH2","HNO3"],p:["CoNO32","H2O"],cond:"",eq:"Co(OH)₂ + 2HNO₃ → Co(NO₃)₂ + 2H₂O"},

// --- bazơ + H3PO4 ---
{r:["LiOH","H3PO4"],p:["Li3PO4","H2O"],cond:"",eq:"3LiOH + H₃PO₄ → Li₃PO₄ + 3H₂O"},
{r:["SrOH2","H3PO4"],p:["Sr3PO42","H2O"],cond:"",eq:"3Sr(OH)₂ + 2H₃PO₄ → Sr₃(PO₄)₂ + 6H₂O"},
{r:["CdOH2","H3PO4"],p:["Cd3PO42","H2O"],cond:"",eq:"3Cd(OH)₂ + 2H₃PO₄ → Cd₃(PO₄)₂ + 6H₂O"},
{r:["CoOH2","H3PO4"],p:["Co3PO42","H2O"],cond:"",eq:"3Co(OH)₂ + 2H₃PO₄ → Co₃(PO₄)₂ + 6H₂O"},

//==================== DẪN XUẤT HALOGEN ====================

{r:["CH4","Cl2"],p:["CH3Cl","HCl"],cond:"ánh sáng",eq:"CH₄ + Cl₂ → CH₃Cl + HCl"},
{r:["CH3Cl","NaOH"],p:["CH3OH","NaCl"],cond:"dd,t°",eq:"CH₃Cl + NaOH → CH₃OH + NaCl"},
{r:["C2H6","Cl2"],p:["C2H5Cl","HCl"],cond:"ánh sáng",eq:"C₂H₆ + Cl₂ → C₂H₅Cl + HCl"},
{r:["C2H5Cl","NaOH"],p:["C2H5OH","NaCl"],cond:"dd,t°",eq:"C₂H₅Cl + NaOH → C₂H₅OH + NaCl"},

//==================== ETE ====================

{r:["C2H5OH"],p:["C2H5OC2H5","H2O"],cond:"H₂SO₄ đặc,140°C",eq:"2C₂H₅OH → C₂H₅OC₂H₅ + H₂O"},
{r:["C2H5OC2H5","H2O"],p:["C2H5OH"],cond:"H⁺",eq:"C₂H₅OC₂H₅ + H₂O → 2C₂H₅OH"},

//==================== AXIT HỮU CƠ ====================

{r:["CH3COOH","CH3OH"],p:["CH3COOCH3","H2O"],cond:"H₂SO₄ đặc",eq:"CH₃COOH + CH₃OH ⇌ CH₃COOCH₃ + H₂O"},
{r:["HCOOH","C2H5OH"],p:["HCOOC2H5","H2O"],cond:"H₂SO₄ đặc",eq:"HCOOH + C₂H₅OH ⇌ HCOOC₂H₅ + H₂O"},

//==================== GLIXEROL ====================

{r:["C3H8","O2"],p:["C3H8O3"],cond:"xt",eq:"2C₃H₈ + 3O₂ → 2C₃H₈O₃"},
{r:["C3H8O3","HNO3"],p:["C3H5N3O9","H2O"],cond:"H₂SO₄ đặc",eq:"C₃H₈O₃ + 3HNO₃ → C₃H₅N₃O₉ + 3H₂O"},

//==================== ĐƯỜNG ====================

{r:["C6H12O6"],p:["C12H22O11","H2O"],cond:"xt",eq:"2C₆H₁₂O₆ → C₁₂H₂₂O₁₁ + H₂O"},
{r:["C12H22O11","H2O"],p:["C6H12O6"],cond:"H⁺",eq:"C₁₂H₂₂O₁₁ + H₂O → 2C₆H₁₂O₆"},

//==================== AXETON ====================

{r:["C3H8O"],p:["CH3COCH3","H2"],cond:"Cu,t°",eq:"C₃H₈O → CH₃COCH₃ + H₂"},
{r:["CH3COCH3","H2"],p:["C3H8O"],cond:"Ni",eq:"CH₃COCH₃ + H₂ → C₃H₈O"},

//==================== URE ====================

{r:["NH3","CO2"],p:["NH2CONH2","H2O"],cond:"t°,p",eq:"2NH₃ + CO₂ → NH₂CONH₂ + H₂O"},



//==================== POLYME ====================

// Politetrafluoroetylen (Teflon)
{r:["C2F4"],p:["PTFE"],cond:"xt,p",eq:"nCF₂=CF₂ → PTFE"},

// Polymetyl metacrylat (Mica hữu cơ)
{r:["MMA"],p:["PMMA"],cond:"xt",eq:"nCH₂=C(CH₃)COOCH₃ → PMMA"},

// Polyvinyl axetat
{r:["VAc"],p:["PVAc"],cond:"xt",eq:"nCH₂=CHOCOCH₃ → PVAc"},

// Polyvinyl ancol
{r:["PVAc","NaOH"],p:["PVA","CH3COONa"],cond:"dd",eq:"PVAc + NaOH → PVA + CH₃COONa"},

// Polyacrylonitril
{r:["AN"],p:["PAN"],cond:"xt",eq:"nCH₂=CHCN → PAN"},

// Polybutadien
{r:["Butadien"],p:["PB"],cond:"xt",eq:"nCH₂=CH−CH=CH₂ → PB"},

// Polyisopren (cao su thiên nhiên)
{r:["Isopren"],p:["PI"],cond:"xt",eq:"nC₅H₈ → PI"},

// Cao su Buna-S
{r:["Butadien","Styren"],p:["SBR"],cond:"xt",eq:"Butadien + Styren → SBR"},

// Cao su Buna-N
{r:["Butadien","AN"],p:["NBR"],cond:"xt",eq:"Butadien + Acrylonitril → NBR"},

// PET
{r:["EG","TPA"],p:["PET","H2O"],cond:"t°",eq:"nHOCH₂CH₂OH + nHOOCC₆H₄COOH → PET + 2nH₂O"},

// Nylon-6
{r:["Caprolactam"],p:["Nylon6"],cond:"t°",eq:"nCaprolactam → Nylon-6"},

// Nylon-6,6
{r:["HMDA","AdipicAcid"],p:["Nylon66","H2O"],cond:"t°",eq:"nHMDA + nAdipic Acid → Nylon-6,6 + H₂O"},

// Bakelit
{r:["Phenol","CH2O"],p:["Bakelite","H2O"],cond:"xt",eq:"Phenol + Formaldehyde → Bakelite"},

// Polycarbonate
{r:["BisphenolA","Phosgene"],p:["PC"],cond:"xt",eq:"Bisphenol A + COCl₂ → PC"},

// Polyoxymetylen
{r:["CH2O"],p:["POM"],cond:"xt",eq:"nCH₂O → POM"},

// Polylactic acid
{r:["LacticAcid"],p:["PLA","H2O"],cond:"xt",eq:"nLactic Acid → PLA + H₂O"},

// Polyurethane
{r:["Diisocyanate","Polyol"],p:["PU"],cond:"xt",eq:"Diisocyanate + Polyol → PU"},

// Nhựa epoxy
{r:["Epichlorohydrin","BisphenolA"],p:["Epoxy"],cond:"xt",eq:"Epichlorohydrin + Bisphenol A → Epoxy"},

// Silicone
{r:["Dimethyldichlorosilane","H2O"],p:["Silicone","HCl"],cond:"",eq:"(CH₃)₂SiCl₂ + H₂O → Silicone + HCl"},

// Kevlar
{r:["PPD","TPC"],p:["Kevlar","HCl"],cond:"",eq:"PPD + TPC → Kevlar + HCl"},
{r:["C2H4"],p:["PP"],cond:"xt",eq:"nC₃H₆ → PP"},
{r:["C2H4","Cl2"],p:["CH2CHCl"],cond:"xt",eq:"C₂H₄ + Cl₂ → CH₂CHCl + HCl"},
{r:["CH2CHCl"],p:["PVC"],cond:"xt",eq:"nCH₂CHCl → PVC"},
// --- đốt cháy với O2 ---

{r:["Ag","O2"],p:["Ag2O"],cond:"t°",eq:"4Ag + O₂ → 2Ag₂O"},
{r:["Mn","O2"],p:["MnO2"],cond:"t°",eq:"Mn + O₂ → MnO₂"},
{r:["Cr","O2"],p:["Cr2O3"],cond:"t°",eq:"4Cr + 3O₂ → 2Cr₂O₃"},
{r:["Na","O2"],p:["Na2O"],cond:"t°",eq:"4Na + O₂ → 2Na₂O"},
{r:["K","O2"],p:["K2O"],cond:"t°",eq:"4K + O₂ → 2K₂O"},
{r:["Ca","O2"],p:["CaO"],cond:"t°",eq:"2Ca + O₂ → 2CaO"},
{r:["Ba","O2"],p:["BaO"],cond:"t°",eq:"2Ba + O₂ → 2BaO"},
{r:["Mg","O2"],p:["MgO"],cond:"t°",eq:"2Mg + O₂ → 2MgO"},
{r:["Al","O2"],p:["Al2O3"],cond:"t°",eq:"4Al + 3O₂ → 2Al₂O₃"},
{r:["Zn","O2"],p:["ZnO"],cond:"t°",eq:"2Zn + O₂ → 2ZnO"},
{r:["FeO","O2"],p:["Fe2O3"],cond:"t°",eq:"4FeO + O₂ → 2Fe₂O₃"},
{r:["Fe","O2"],p:["FeO"],cond:"t°",eq:"2Fe + O₂ → 2FeO"},
{r:["FeO","Fe2O3"],p:["Fe3O4"],cond:"t°",eq:"FeO + Fe₂O₃ → Fe₃O₄"},
{r:["Cu","O2"],p:["CuO"],cond:"t°",eq:"2Cu + O₂ → 2CuO"},
{r:["S","O2"],p:["SO2"],cond:"t°",eq:"S + O₂ → SO₂"},
{r:["SO2","O2"],p:["SO3"],cond:"V₂O₅/t°",eq:"2SO₂ + O₂ → 2SO₃"},
{r:["C","O2"],p:["CO2"],cond:"t°",eq:"C + O₂ → CO₂"},
{r:["P","O2"],p:["P2O5"],cond:"t°",eq:"4P + 5O₂ → 2P₂O₅"},
{r:["Si","O2"],p:["SiO2"],cond:"t°",eq:"Si + O₂ → SiO₂"},
{r:["H2","O2"],p:["H2O"],cond:"tia lửa",eq:"2H₂ + O₂ → 2H₂O"},
{r:["CO","O2"],p:["CO2"],cond:"t°",eq:"2CO + O₂ → 2CO₂"},
{r:["CH4","O2"],p:["CO2","H2O"],cond:"t°",eq:"CH₄ + 2O₂ → CO₂ + 2H₂O"},
{r:["C2H2","O2"],p:["CO2","H2O"],cond:"t°",eq:"2C₂H₂ + 5O₂ → 4CO₂ + 2H₂O"},
{r:["C2H4","O2"],p:["CO2","H2O"],cond:"t°",eq:"C₂H₄ + 3O₂ → 2CO₂ + 2H₂O"},
{r:["C2H6","O2"],p:["CO2","H2O"],cond:"t°",eq:"2C₂H₆ + 7O₂ → 4CO₂ + 6H₂O"},
{r:["C2H5OH","O2"],p:["CO2","H2O"],cond:"t°",eq:"C₂H₅OH + 3O₂ → 2CO₂ + 3H₂O"},
{r:["C6H6","O2"],p:["CO2","H2O"],cond:"t°",eq:"2C₆H₆ + 15O₂ → 12CO₂ + 6H₂O"},
{r:["CaO","O2"],p:["CaO2"],cond:"t°",eq:"2CaO + O₂ → 2CaO₂"},
{r:["BaO","O2"],p:["BaO2"],cond:"t°",eq:"2BaO + O₂ → 2BaO₂"},
{r:["K2O","O2"],p:["K2O2"],cond:"t°",eq:"2K₂O + O₂ → 2K₂O₂"},
{r:["NaO","O2"],p:["Na2O2"],cond:"t°",eq:"2NaO + O₂ → 2Na₂O₂"},


// --- muối acid ---
{r:["Na2CO3","H2O","CO2"],p:["NaHCO3"],cond:"",eq:"Na₂CO₃ + H₂O + CO₂ → 2NaHCO₃"},
{r:["CaCO3","H2O","CO2"],p:["CaHCO32"],cond:"",eq:"CaCO₃ + H₂O + CO₂ → Ca(HCO₃)₂"},
{r:["K2CO3","H2O","CO2"],p:["KHCO3"],cond:"",eq:"K₂CO₃ + H₂O + CO₂ → 2KHCO₃"},
{r:["BaCO3","H2O","CO2"],p:["BaHCO32"],cond:"",eq:"BaCO₃ + H₂O + CO₂ → Ba(HCO₃)₂"},
{r:["Na2SO3","H2O","SO2"],p:["NaHSO3"],cond:"",eq:"Na₂SO₃ + H₂O + SO₂ → 2NaHSO₃"},
{r:["CaSO3","H2O","SO2"],p:["CaHSO32"],cond:"",eq:"CaSO₃ + H₂O + SO₂ → Ca(HSO₃)₂"},
{r:["BaSO3","H2O","SO2"],p:["BaHSO32"],cond:"",eq:"BaSO₃ + H₂O + SO₂ → Ba(HSO₃)₂"},
{r:["K2SO3","H2O","SO2"],p:["KHSO3"],cond:"",eq:"K₂SO₃ + H₂O + SO₂ → 2KHSO₃"},
{r:["Na2SO4","H2SO4 loãng"],p:["NaHSO4"],cond:"",eq:"Na₂SO₄ + H₂SO₄ loãng → 2NaHSO₄"},
{r:["CaSO4","H2SO4 loãng"],p:["CaHSO42"],cond:"",eq:"CaSO₄ + H₂SO₄ loãng → Ca(HSO₄)₂"},
{r:["BaSO4","H2SO4 loãng"],p:["BaHSO42"],cond:"",eq:"BaSO₄ + H₂SO₄ loãng → Ba(HSO₄)₂"},
{r:["K2SO4","H2SO4 loãng"],p:["KHSO4"],cond:"",eq:"K₂SO₄ + H₂SO₄ loãng → 2KHSO₄"},
{r:["Na2SO4","H2SO4 đặc"],p:["NaHSO4"],cond:"",eq:"Na₂SO₄ + H₂SO₄ đặc → 2NaHSO₄"},
{r:["CaSO4","H2SO4 đặc"],p:["CaHSO42"],cond:"",eq:"CaSO₄ + H₂SO₄ đặc → Ca(HSO₄)₂"},
{r:["BaSO4","H2SO4 đặc"],p:["BaHSO42"],cond:"",eq:"BaSO₄ + H₂SO₄ đặc → Ba(HSO₄)₂"},
{r:["K2SO4","H2SO4 đặc"],p:["KHSO4"],cond:"",eq:"K₂SO₄ + H₂SO₄ đặc → 2KHSO₄"},


// --- base + halogen ---
{r:["NaOH","Cl2"],p:["NaCl","NaClO"],cond:"t°",eq:"2NaOH + Cl₂ → NaCl + NaClO + H₂O"},
{r:["KOH","Cl2"],p:["KCl","KClO3"],cond:"t°",eq:"6KOH + 3Cl₂ → 5KCl + KClO₃+ 3H₂O"},
{r:["Ca(OH)2","Cl2"],p:["CaCl2","CaOCl2"],cond:"",eq:"2Ca(OH)₂ + 2Cl₂ → CaCl₂ + CaOCl₂ + 2H₂O"},
{r:["Ba(OH)2","Cl2"],p:["BaCl2","BaOCl2"],cond:"",eq:"2Ba(OH)₂ + 2Cl₂ → BaCl₂ + BaOCl₂ + 2H₂O"},
// --- kim loại + halogen ---
{r:["Na","Cl2"],p:["NaCl"],cond:"t°",eq:"2Na + Cl₂ → 2NaCl"},
{r:["K","Cl2"],p:["KCl"],cond:"t°",eq:"2K + Cl₂ → 2KCl"},
{r:["Ca","Cl2"],p:["CaCl2"],cond:"t°",eq:"Ca + Cl₂ → CaCl₂"},
{r:["Mg","Cl2"],p:["MgCl2"],cond:"t°",eq:"Mg + Cl₂ → MgCl₂"},
{r:["Mg","I2"],p:["MgI2"],cond:"t°",eq:"Mg + I₂ → MgI₂"},
{r:["Mg","Br2"],p:["MgBr2"],cond:"t°",eq:"Mg + Br₂ → MgBr₂"},
{r:["Mg","F2"],p:["MgF2"],cond:"t°",eq:"Mg + F₂ → MgF₂"},
{r:["Al","I2"],p:["AlI3"],cond:"t°",eq:"2Al + 3I₂ → 2AlI₃"},
{r:["Al","F2"],p:["AlF3"],cond:"t°",eq:"2Al + 3F₂ → 2AlF₃"},
{r:["Al","Br2"],p:["AlBr3"],cond:"t°",eq:"2Al + 3Br₂ → 2AlBr₃"},
{r:["Al","Cl2"],p:["AlCl3"],cond:"t°",eq:"2Al + 3Cl₂ → 2AlCl₃"},
{r:["Fe","Cl2"],p:["FeCl3"],cond:"t°",eq:"2Fe + 3Cl₂ → 2FeCl₃"},
{r:["Fe","I2"],p:["FeI3"],cond:"t°",eq:"2Fe + 3I₂ → 2FeI₃"},
{r:["Fe","F2"],p:["FeF3"],cond:"t°",eq:"2Fe + 3F₂ → 2FeF₃"},
{r:["Fe","Br2"],p:["FeBr3"],cond:"t°",eq:"2Fe + 3Br₂ → 2FeBr₃"},
{r:["Cu","Cl2"],p:["CuCl2"],cond:"t°",eq:"Cu + Cl₂ → CuCl₂"},
{r:["Cu","I2"],p:["CuI2"],cond:"t°",eq:"Cu + I₂ → CuI₂"},
{r:["Cu","Br2"],p:["CuBr2"],cond:"t°",eq:"Cu + Br₂ → CuBr₂"},
{r:["Cu","F2"],p:["CuF2"],cond:"t°",eq:"Cu + F₂ → CuF₂"},
{r:["Zn","Cl2"],p:["ZnCl2"],cond:"t°",eq:"Zn + Cl₂ → ZnCl₂"},
{r:["Hg","Cl2"],p:["HgCl2"],cond:"t°",eq:"Hg + Cl₂ → HgCl₂"},
{r:["H2","Cl2"],p:["HCl"],cond:"ánh sáng",eq:"H₂ + Cl₂ → 2HCl"},
{r:["Na","Br2"],p:["NaBr"],cond:"t°",eq:"2Na + Br₂ → 2NaBr"},
{r:["Na","I2"],p:["NaI"],cond:"t°",eq:"2Na + I₂ → 2NaI"},
{r:["K","Br2"],p:["KBr"],cond:"t°",eq:"2K + Br₂ → 2KBr"},
{r:["K","I2"],p:["KI"],cond:"t°",eq:"2K + I₂ → 2KI"},

{r:["H2","I2"],p:["HI"],cond:"t°",eq:"H₂ + I₂ ⇌ 2HI"},
{r:["H2","F2"],p:["HF"],cond:"",eq:"H₂ + F₂ → 2HF"},
{r:["H2","Br2"],p:["HBr"],cond:"t°",eq:"H₂ + Br₂ → 2HBr"},
// --- kim loại + lưu huỳnh ---
{r:["Fe","S"],p:["FeS"],cond:"t°",eq:"Fe + S → FeS"},
{r:["Cu","S"],p:["CuS"],cond:"t°",eq:"Cu + S → CuS"},
{r:["Zn","S"],p:["ZnS"],cond:"t°",eq:"Zn + S → ZnS"},
{r:["Ag","S"],p:["Ag2S"],cond:"t°",eq:"2Ag + S → Ag₂S"},
{r:["Pb","S"],p:["PbS"],cond:"t°",eq:"Pb + S → PbS"},
{r:["H2","S"],p:["H2S"],cond:"t°",eq:"H₂ + S → H₂S"},

// --- kim loại + nước ---
{r:["Na","H2O"],p:["NaOH","H2"],cond:"",eq:"2Na + 2H₂O → 2NaOH + H₂↑"},
{r:["K","H2O"],p:["KOH","H2"],cond:"",eq:"2K + 2H₂O → 2KOH + H₂↑"},
{r:["Ca","H2O"],p:["CaOH2","H2"],cond:"",eq:"Ca + 2H₂O → Ca(OH)₂ + H₂↑"},
{r:["Ba","H2O"],p:["BaOH2","H2"],cond:"",eq:"Ba + 2H₂O → Ba(OH)₂ + H₂↑"},

// ---  nước ---
{r:["Na2O","H2O"],p:["NaOH"],cond:"",eq:"Na₂O + H₂O → 2NaOH"},
{r:["K2O","H2O"],p:["KOH"],cond:"",eq:"K₂O + H₂O → 2KOH"},
{r:["CaO","H2O"],p:["CaOH2"],cond:"",eq:"CaO + H₂O → Ca(OH)₂"},
{r:["BaO","H2O"],p:["BaOH2"],cond:"",eq:"BaO + H₂O → Ba(OH)₂"},
{r:["CO2","H2O"],p:["H2CO3"],cond:"",eq:"CO₂ + H₂O ⇌ H₂CO₃"},
{r:["SO2","H2O"],p:["H2SO3"],cond:"",eq:"SO₂ + H₂O ⇌ H₂SO₃"},
{r:["SO3","H2O"],p:["H2SO4 đặc"],cond:"",eq:"SO₃ + H₂O → H₂SO₄ đặc"},
{r:["H2SO4 đặc","H2O"],p:["H2SO4 loãng"],cond:"",eq:"H₂SO₄ đặc + H₂O → H₂SO₄ loãng"},
{r:["H2SO4 đặc","SO3"],p:["H2SO4.nSO3"],cond:"",eq:"H₂SO₄ đặc + SO₃ → H2SO4.nSO3"},
{r:["H2SO4.nSO3","H2O"],p:["H2SO4 đặc"],cond:"",eq:"H2SO4.nSO3 + nH₂O → (n+1)H₂SO₄ đặc "},
{r:["N2O5","H2O"],p:["HNO3"],cond:"",eq:"N₂O₅ + H₂O → 2HNO₃"},
{r:["P2O5","H2O"],p:["H3PO4"],cond:"",eq:"P₂O₅ + 3H₂O → 2H₃PO₄"},
{r:["NO2","H2O"],p:["HNO3","NO"],cond:"",eq:"3NO₂ + H₂O → 2HNO₃ + NO"},
{r:["NO2","O2","H2O"],p:["HNO3"],cond:"",eq:"4NO₂ + O₂ + 2H₂O → 4HNO₃"},

{r:["Br2","SO2","H2O"],p:["HBr","H2SO4"],cond:"",eq:"Br₂ + SO₂ + 2H₂O → 2HBr + H₂SO₄"},
{r:["F2","H2O"],p:["HF","O2"],cond:"",eq:"2F₂ + 2H₂O → 4HF + O₂"},
{r:["I2","H2O"],p:["HI","HIO"],cond:"",eq:"I₂ + H₂O ⇌ HI + HIO"},
{r:["Cl2","H2O"],p:["HCl","HClO"],cond:"",eq:"Cl₂ + H₂O ⇌ HCl + HClO"},
{r:["Br2","H2O"],p:["HBr","HBrO"],cond:"",eq:"Br₂ + H₂O ⇌ HBr + HBrO"},

{r:["CaO2","H2O"],p:["CaOH2","H2O2"],cond:"0°C",eq:"CaO₂ + H₂O → Ca(OH)₂ + H₂O₂"},
{r:["BaO2","H2O"],p:["BaOH2","H2O2"],cond:"0°C",eq:"BaO₂ a+ H₂O → Ba(OH)₂ + H₂O₂"},
{r:["K2O2","H2O"],p:["KOH","H2O2"],cond:"0°C",eq:"K₂O₂ + H₂O → 2KOH + H₂O₂"},
{r:["NaO2","H2O"],p:["NaOH","H2O2"],cond:"0°C",eq:"NaO₂ + H₂O → NaOH + H₂O₂"},

  {r:["NaH","H2O"],p:["NaOH","H2O"],cond:"0°C",eq:"NaH + H₂O → NaOH + H₂"},
  {r:["KH","H2O"],p:["KOH","H2O"],cond:"0°C",eq:"KH + H₂O → KOH + H₂"},
  {r:["CaH2","H2O"],p:["CaOH2","H2O"],cond:"0°C",eq:"CaH₂ + H₂O → CaOH + H₂"},
   {r:["BaH2","H2O"],p:["BaOH2","H2O"],cond:"0°C",eq:"BaH₂ + H₂O → BaOH + H₂"},
// --- nitơ / amoniac ---
{r:["N2","H2"],p:["NH3"],cond:"t°, p, xt Fe",eq:"N₂ + 3H₂ ⇌ 2NH₃"},
{r:["N2","O2"],p:["NO"],cond:"tia lửa điện / 3000°C",eq:"N₂ + O₂ → 2NO"},
{r:["NO","O2"],p:["NO2"],cond:"",eq:"2NO + O₂ → 2NO₂"},
{r:["NH3","O2"],p:["NO","H2O"],cond:"xt, t°",eq:"4NH₃ + 5O₂ → 4NO + 6H₂O"},
{r:["NH3","H2O"],p:["NH3H2O"],cond:"",eq:"NH₃ + H₂O ⇌ NH₃·H₂O"},
{r:["NH3","HCl"],p:["NH4Cl"],cond:"",eq:"NH₃ + HCl → NH₄Cl"},
{r:["NH3","HNO3"],p:["NH4NO3"],cond:"",eq:"NH₃ + HNO₃ → NH₄NO₃"},
{r:["NH3","H2SO4 đặc"],p:["NH42SO4"],cond:"",eq:"2NH₃ + H₂SO₄ đặc → (NH₄)₂SO₄"},
{r:["NH3","H2SO4 loãng"],p:["NH42SO4"],cond:"",eq:"2NH₃ + H₂SO₄ loãng → (NH₄)₂SO₄"},
{r:["NH3","H2O","SO2"],p:["NH4HSO3"],cond:"",eq:"NH₃ + H₂O + SO₂ → NH₄HSO₃"},
{r:["NH3","H2O","CO2"],p:["NH4HCO3"],cond:"",eq:"NH₃ + H₂O + CO₂ → NH₄HCO₃"},

// --- axit + bazơ (trung hoà) ---
{r:["HCl","NaOH"],p:["NaCl","H2O"],cond:"",eq:"HCl + NaOH → NaCl + H₂O"},
{r:["HCl","KOH"],p:["KCl","H2O"],cond:"",eq:"HCl + KOH → KCl + H₂O"},
{r:["HCl","CaOH2"],p:["CaCl2","H2O"],cond:"",eq:"2HCl + Ca(OH)₂ → CaCl₂ + 2H₂O"},
{r:["HCl","BaOH2"],p:["BaCl2","H2O"],cond:"",eq:"2HCl + Ba(OH)₂ → BaCl₂ + 2H₂O"},
{r:["HCl","MgOH2"],p:["MgCl2","H2O"],cond:"",eq:"2HCl + Mg(OH)₂ → MgCl₂ + 2H₂O"},
{r:["HCl","AlOH3"],p:["AlCl3","H2O"],cond:"",eq:"3HCl + Al(OH)₃ → AlCl₃ + 3H₂O"},
{r:["HCl","ZnOH2"],p:["ZnCl2","H2O"],cond:"",eq:"2HCl + Zn(OH)₂ → ZnCl₂ + 2H₂O"},
{r:["HCl","FeOH2"],p:["FeCl2","H2O"],cond:"",eq:"2HCl + Fe(OH)₂ → FeCl₂ + 2H₂O"},
{r:["HCl","FeOH3"],p:["FeCl3","H2O"],cond:"",eq:"3HCl + Fe(OH)₃ → FeCl₃ + 3H₂O"},
{r:["HCl","CuOH2"],p:["CuCl2","H2O"],cond:"",eq:"2HCl + Cu(OH)₂ → CuCl₂ + 2H₂O"},
{r:["H2SO4 loãng","NaOH"],p:["Na2SO4","H2O"],cond:"",eq:"H₂SO₄ + 2NaOH → Na₂SO₄ + 2H₂O"},
{r:["H2SO4 loãng","KOH"],p:["K2SO4","H2O"],cond:"",eq:"H₂SO₄ + 2KOH → K₂SO₄ + 2H₂O"},
{r:["H2SO4 loãng","CaOH2"],p:["CaSO4","H2O"],cond:"",eq:"H₂SO₄ + Ca(OH)₂ → CaSO₄ + 2H₂O"},
{r:["H2SO4 loãng","BaOH2"],p:["BaSO4","H2O"],cond:"",eq:"H₂SO₄ + Ba(OH)₂ → BaSO₄↓ + 2H₂O"},
{r:["H2SO4 loãng","MgOH2"],p:["MgSO4","H2O"],cond:"",eq:"H₂SO₄ + Mg(OH)₂ → MgSO₄ + 2H₂O"},
{r:["H2SO4 loãng","AlOH3"],p:["Al2SO43","H2O"],cond:"",eq:"3H₂SO₄ + 2Al(OH)₃ → Al₂(SO₄)₃ + 6H₂O"},
{r:["H2SO4 loãng","ZnOH2"],p:["ZnSO4","H2O"],cond:"",eq:"H₂SO₄ + Zn(OH)₂ → ZnSO₄ + 2H₂O"},
{r:["H2SO4 loãng","FeOH2"],p:["FeSO4","H2O"],cond:"",eq:"H₂SO₄ + Fe(OH)₂ → FeSO₄ + 2H₂O"},
{r:["H2SO4 loãng","FeOH3"],p:["Fe2SO43","H2O"],cond:"",eq:"3H₂SO₄ + 2Fe(OH)₃ → Fe₂(SO₄)₃ + 6H₂O"},
{r:["H2SO4 loãng","CuOH2"],p:["CuSO4","H2O"],cond:"",eq:"H₂SO₄ + Cu(OH)₂ → CuSO₄ + 2H₂O"},

{r:["H2SO4 đặc","NaOH"],p:["Na2SO4","H2O"],cond:"",eq:"H₂SO₄ + 2NaOH → Na₂SO₄ + 2H₂O"},
{r:["H2SO4 đặc","KOH"],p:["K2SO4","H2O"],cond:"",eq:"H₂SO₄ + 2KOH → K₂SO₄ + 2H₂O"},
{r:["H2SO4 đặc","CaOH2"],p:["CaSO4","H2O"],cond:"",eq:"H₂SO₄ + Ca(OH)₂ → CaSO₄ + 2H₂O"},
{r:["H2SO4 đặc","BaOH2"],p:["BaSO4","H2O"],cond:"",eq:"H₂SO₄ + Ba(OH)₂ → BaSO₄↓ + 2H₂O"},
{r:["H2SO4 đặc","MgOH2"],p:["MgSO4","H2O"],cond:"",eq:"H₂SO₄ + Mg(OH)₂ → MgSO₄ + 2H₂O"},
{r:["H2SO4 đặc","AlOH3"],p:["Al2SO43","H2O"],cond:"",eq:"3H₂SO₄ + 2Al(OH)₃ → Al₂(SO₄)₃ + 6H₂O"},
{r:["H2SO4 đặc","ZnOH2"],p:["ZnSO4","H2O"],cond:"",eq:"H₂SO₄ + Zn(OH)₂ → ZnSO₄ + 2H₂O"},
{r:["H2SO4 đặc","FeOH2"],p:["FeSO4","H2O"],cond:"",eq:"H₂SO₄ + Fe(OH)₂ → FeSO₄ + 2H₂O"},
{r:["H2SO4 đặc","FeOH3"],p:["Fe2SO43","H2O"],cond:"",eq:"3H₂SO₄ + 2Fe(OH)₃ → Fe₂(SO₄)₃ + 6H₂O"},
{r:["H2SO4 đặc","CuOH2"],p:["CuSO4","H2O"],cond:"",eq:"H₂SO₄ + Cu(OH)₂ → CuSO₄ + 2H₂O"},

{r:["HNO3","NaOH"],p:["NaNO3","H2O"],cond:"",eq:"HNO₃ + NaOH → NaNO₃ + H₂O"},
{r:["HNO3","KOH"],p:["KNO3","H2O"],cond:"",eq:"HNO₃ + KOH → KNO₃ + H₂O"},
{r:["HNO3","CaOH2"],p:["CaNO32","H2O"],cond:"",eq:"2HNO₃ + Ca(OH)₂ → Ca(NO₃)₂ + 2H₂O"},
{r:["HNO3","CuOH2"],p:["CuNO32","H2O"],cond:"",eq:"2HNO₃ + Cu(OH)₂ → Cu(NO₃)₂ + 2H₂O"},
{r:["H3PO4","NaOH"],p:["Na3PO4","H2O"],cond:"",eq:"H₃PO₄ + 3NaOH → Na₃PO₄ + 3H₂O"},
{r:["H3PO4","CaOH2"],p:["Ca3PO42","H2O"],cond:"",eq:"2H₃PO₄ + 3Ca(OH)₂ → Ca₃(PO₄)₂↓ + 6H₂O"},
{r:["CH3COOH","NaOH"],p:["CH3COONa","H2O"],cond:"",eq:"CH₃COOH + NaOH → CH₃COONa + H₂O"},

// --- axit + kim loại đứng trước H ---
{r:["HCl","K"],p:["KCl","H2"],cond:"",eq:"2K + 2HCl → 2KCl + H₂↑"},
{r:["HCl","Na"],p:["NaCl","H2"],cond:"",eq:"2Na + 2HCl → 2NaCl + H₂↑"},
{r:["HCl","Ca"],p:["CaCl2","H2"],cond:"",eq:"Ca + 2HCl → CaCl₂ + H₂↑"},
{r:["HCl","Ba"],p:["BaCl2","H2"],cond:"",eq:"Ba + 2HCl → BaCl₂ + H₂↑"},
{r:["HCl","Mg"],p:["MgCl2","H2"],cond:"",eq:"Mg + 2HCl → MgCl₂ + H₂↑"},
{r:["HCl","Al"],p:["AlCl3","H2"],cond:"",eq:"2Al + 6HCl → 2AlCl₃ + 3H₂↑"},
{r:["HCl","Zn"],p:["ZnCl2","H2"],cond:"",eq:"Zn + 2HCl → ZnCl₂ + H₂↑"},
{r:["HCl","Fe"],p:["FeCl2","H2"],cond:"",eq:"Fe + 2HCl → FeCl₂ + H₂↑"},
{r:["HCl","Ni"],p:["NiCl2","H2"],cond:"",eq:"Ni + 2HCl → NiCl₂ + H₂↑"},
{r:["HCl","Sn"],p:["SnCl2","H2"],cond:"",eq:"Sn + 2HCl → SnCl₂ + H₂↑"},
{r:["HCl","Pb"],p:["PbCl2","H2"],cond:"",eq:"Pb + 2HCl → PbCl₂ + H₂↑"},

{r:["K","H2SO4 loãng"],p:["K2SO4","H2"],cond:"",eq:"2K + H₂SO₄ loãng → K₂SO₄ + H₂↑"},
{r:["Ca","H2SO4 loãng"],p:["CaSO4","H2"],cond:"",eq:"Ca + H₂SO₄ loãng → CaSO₄ + H₂↑"},
{r:["Na","H2SO4 loãng"],p:["Na2SO4","H2"],cond:"",eq:"2Na + H₂SO₄ loãng → Na₂SO₄ + H₂↑"},
{r:["Ba","H2SO4 loãng"],p:["BaSO4","H2"],cond:"",eq:"Ba + H₂SO₄ loãng → BaSO₄↓ + H₂↑"},
{r:["Al","H2SO4 loãng"],p:["Al2SO43","H2"],cond:"",eq:"2Al + 3H₂SO₄ loãng → Al₂(SO₄)₃ + 3H₂↑"},
{r:["Fe","H2SO4 loãng"],p:["FeSO4","H2"],cond:"",eq:"Fe + H₂SO₄ loãng → FeSO₄ + H₂↑"},
{r:["Zn","H2SO4 loãng"],p:["ZnSO4","H2"],cond:"",eq:"Zn + H₂SO₄ loãng → ZnSO₄ + H₂↑"},
{r:["Mg","H2SO4 loãng"],p:["MgSO4","H2"],cond:"",eq:"Mg + H₂SO₄ loãng → MgSO₄ + H₂↑"},
{r:["H2SO4 loãng","Ni"],p:["NiSO4","H2"],cond:"",eq:"Ni + H₂SO₄ loãng → NiSO₄ + H₂↑"},
{r:["H2SO4 loãng","Sn"],p:["SnSO4","H2"],cond:"",eq:"Sn + H₂SO₄ loãng → SnSO₄ + H₂↑"},
{r:["H2SO4 loãng","Pb"],p:["PbSO4","H2"],cond:"",eq:"Pb + H₂SO₄ loãng → PbSO₄↓ + H₂↑"},

{r:["K","H2SO4 đặc"],p:["K2SO4","SO2","H2O"],cond:"nóng",eq:"2K + 2H₂SO₄ đặc → K₂SO₄ + SO₂↑ + 2H₂O"},
{r:["Ca","H2SO4 đặc"],p:["CaSO4","SO2","H2O"],cond:"nóng",eq:"Ca + 2H₂SO₄ đặc → CaSO₄ + SO₂↑ + 2H₂O"},
{r:["Na","H2SO4 đặc"],p:["Na2SO4","SO2","H2O"],cond:"nóng",eq:"2Na + 2H₂SO₄ đặc → Na₂SO₄ + SO₂↑ + 2H₂O"},
{r:["Ba","H2SO4 đặc"],p:["BaSO4","SO2","H2O"],cond:"nóng",eq:"Ba + 2H₂SO₄ đặc → BaSO₄ + SO₂↑ + 2H₂O"},
{r:["Al","H2SO4 đặc"],p:["Al2SO43","SO2","H2O"],cond:"nóng",eq:"2Al + 6H₂SO₄ đặc → Al₂(SO₄)₃ + 3SO₂↑ + 6H₂O"},
{r:["Cu","H2SO4 đặc"],p:["CuSO4","SO2","H2O"],cond:"nóng",eq:"Cu + 2H₂SO₄ đặc → CuSO₄ + SO₂↑ + 2H₂O"},
{r:["Ag","H2SO4 đặc"],p:["Ag2SO4","SO2","H2O"],cond:"nóng",eq:"2Ag + 2H₂SO₄ đặc → Ag₂SO₄ + SO₂↑ + 2H₂O"},
{r:["Fe","H2SO4 đặc"],p:["Fe2SO43","SO2","H2O"],cond:"nóng",eq:"2Fe + 6H₂SO₄ đặc → Fe₂(SO₄)₃ + 3SO₂↑ + 6H₂O"},
{r:["Zn","H2SO4 đặc"],p:["ZnSO4","SO2","H2O"],cond:"nóng",eq:"Zn + 2H₂SO₄ đặc → ZnSO₄ + SO₂↑ + 2H₂O"},
{r:["Mg","H2SO4 đặc"],p:["MgSO4","SO2","H2O"],cond:"nóng",eq:"Mg + 2H₂SO₄ đặc → MgSO₄ + SO₂↑ + 2H₂O"},


{r:["K","H3PO4"],p:["K3PO4","H2"],cond:"",eq:"6K + 2H₃PO₄ → 2K₃PO₄ + 3H₂↑"},
{r:["Ca","H3PO4"],p:["Ca3PO42","H2"],cond:"",eq:"3Ca + 2H₃PO₄ → Ca₃(PO₄)₂↓ + 3H₂↑"},
{r:["Na","H3PO4"],p:["Na3PO4","H2"],cond:"",eq:"6Na + 2H₃PO₄ → 2Na₃PO₄ + 3H₂↑"},
{r:["Ba","H3PO4"],p:["Ba3PO42","H2"],cond:"",eq:"3Ba + 2H₃PO₄ → Ba₃(PO₄)₂↓ + 3H₂↑"},
{r:["Al","H3PO4"],p:["AlPO4","H2"],cond:"",eq:"2Al + 2H₃PO₄ → 2AlPO₄↓ + 3H₂↑"},
{r:["Fe","H3PO4"],p:["Fe3PO42","H2"],cond:"",eq:"3Fe + 2H₃PO₄ → Fe₃(PO₄)₂↓ + 3H₂↑"},
{r:["Zn","H3PO4"],p:["Zn3PO42","H2"],cond:"",eq:"3Zn + 2H₃PO₄ → Zn₃(PO₄)₂↓ + 3H₂↑"},
{r:["Mg","H3PO4"],p:["Mg3PO42","H2"],cond:"",eq:"3Mg + 2H₃PO₄ → Mg₃(PO₄)₂↓ + 3H₂↑"},
{r:["H3PO4","Ni"],p:["Ni3(PO4)2","H2"],cond:"",eq:"3Ni + 2H₃PO₄ → Ni₃(PO₄)₂↓ + 3H₂↑"},
{r:["H3PO4","Sn"],p:["Sn3(PO4)2","H2"],cond:"",eq:"3Sn + 2H₃PO₄ → Sn₃(PO₄)₂↓ + 3H₂↑"},
{r:["H3PO4","Pb"],p:["Pb3(PO4)2","H2"],cond:"",eq:"3Pb + 2H₃PO₄ → Pb₃(PO₄)₂↓ + 3H₂↑"},

{r:["K","HNO3"],p:["KNO3","NO2","H2O"],cond:"",eq:"K + 2HNO₃ → KNO₃ + NO₂↑ + H₂O"},
{r:["Ca","HNO3"],p:["CaNO32","NO2","H2O"],cond:"",eq:"Ca + 2HNO₃ → Ca(NO₃)₂ + NO₂↑ + H₂O"},
{r:["Na","HNO3"],p:["NaNO3","NO2","H2O"],cond:"",eq:"Na + 2HNO₃ → NaNO₃ + NO₂↑ + H₂O"},
{r:["Ba","HNO3"],p:["BaNO32","NO2","H2O"],cond:"",eq:"Ba + 2HNO₃ → Ba(NO₃)₂ + NO₂↑ + H₂O"},
{r:["Al","HNO3"],p:["AlNO33","NO2","H2O"],cond:"",eq:"Al + 6HNO₃ → Al(NO₃)₃ + 3NO₂↑ + 3H₂O"},
{r:["Cu","HNO3"],p:["CuNO32","NO2","H2O"],cond:"",eq:"Cu + 4HNO₃ → Cu(NO₃)₂ + 2NO₂↑ + 2H₂O"},
{r:["Ag","HNO3"],p:["AgNO3","NO2","H2O"],cond:"",eq:"Ag + 2HNO₃ → AgNO₃ + NO₂↑ + H₂O"},
{r:["Fe","HNO3"],p:["FeNO33","NO2","H2O"],cond:"",eq:"Fe + 6HNO₃ → Fe(NO₃)₃ + 3NO₂↑ + 3H₂O"},
{r:["Zn","HNO3"],p:["ZnNO32","NO2","H2O"],cond:"",eq:"Zn + 4HNO₃ → Zn(NO₃)₂ + 2NO₂↑ + 2H₂O"},
{r:["Mg","HNO3 "],p:["MgNO32","NO2","H2O"],cond:"",eq:"Mg + 4HNO₃ → Mg(NO₃)₂ + 2NO₂↑ + 2H₂O"},
// ---  bazơ  ---
{r:["NaOH","AlOH3"],p:["NaAlO2","H2O"],cond:"",eq:"NaOH + Al(OH)₃ → NaAlO₂ + 2H₂O"},
{r:["KOH","AlOH3"],p:["KAlO2","H2O"],cond:"",eq:"KOH + Al(OH)₃ → KAlO₂ + 2H₂O"},
{r:["NaOH","Al2O3"],p:["NaAlO2","H2O"],cond:"",eq:"NaOH + Al₂O₃ → NaAlO₂ + 3H₂O"},
{r:["NaOH","Al","H2O"],p:["NaAlO2","H2"],cond:"",eq:"2NaOH + 2Al + 2H₂O → 2NaAlO₂ + 3H₂"},
{r:["CaOH2","AlOH3"],p:["CaAlO22","H2O"],cond:"",eq:"Ca(OH)₂ + 2Al(OH)₃ → Ca(AlO₂)₂ + 4H₂O"},
{r:["BaOH2","AlOH3"],p:["BaAlO22","H2O"],cond:"",eq:"Ba(OH)₂ + 2Al(OH)₃ → Ba(AlO₂)₂ + 4H₂O"},
{r:["KOH","Al2O3"],p:["KAlO2","H2O"],cond:"",eq:"KOH + Al₂O₃ → KAlO₂ + 3H₂O"},
{r:["CaOH2","Al2O3"],p:["CaAlO22","H2O"],cond:"",eq:"Ca(OH)₂ + Al₂O₃ → Ca(AlO₂)₂ + 3H₂O"},
{r:["BaOH2","Al2O3"],p:["BaAlO22","H2O"],cond:"",eq:"Ba(OH)₂ + Al₂O₃ → Ba(AlO₂)₂ + 3H₂O"},
{r:["KOH","Al","H2O"],p:["KAlO2","H2"],cond:"",eq:"2KOH + 2Al + 2H₂O → 2KAlO₂ + 3H₂"},
{r:["CaOH2","Al","H2O"],p:["CaAlO22","H2"],cond:"",eq:"Ca(OH)₂ + 2Al + 2H₂O → Ca(AlO₂)₂ + 3H₂"},
{r:["BaOH2","Al","H2O"],p:["BaAlO22","H2"],cond:"",eq:"Ba(OH)₂ + 2Al + 2H₂O → Ba(AlO₂)₂ + 3H₂"},

{r:["NaOH","Zn(OH)2"],p:["Na2ZnO2","H2O"],cond:"",eq:"2NaOH + Zn(OH)₂ → Na₂ZnO₂ + 2H₂O"},
{r:["KOH","Zn(OH)2"],p:["K2ZnO2","H2O"],cond:"",eq:"2KOH + Zn(OH)₂ → K₂ZnO₂ + 2H₂O"},
{r:["NaOH","ZnO"],p:["Na2ZnO2","H2O"],cond:"",eq:"2NaOH + ZnO → Na₂ZnO₂ + H₂O"},
{r:["NaOH","Zn"],p:["Na2ZnO2","H2"],cond:"",eq:"2NaOH + Zn → Na₂ZnO₂ + H₂"},
{r:["Ca(OH)2","Zn(OH)2"],p:["CaZnO2","H2O"],cond:"",eq:"Ca(OH)₂ + Zn(OH)₂ → CaZnO₂ + 2H₂O"},
{r:["Ba(OH)2","Zn(OH)2"],p:["BaZnO2","H2O"],cond:"",eq:"Ba(OH)₂ + Zn(OH)₂ → BaZnO₂ + 2H₂O"},
{r:["KOH","ZnO"],p:["K2ZnO2","H2O"],cond:"",eq:"2KOH + ZnO → K₂ZnO₂ + H₂O"},
{r:["KOH","Zn"],p:["K2ZnO2","H2"],cond:"",eq:"2KOH + Zn → K₂ZnO₂ + H₂"},
{r:["Ba(OH)2","ZnO"],p:["BaZnO2","H2O"],cond:"",eq:"Ba(OH)₂ + ZnO → BaZnO₂ + H₂O"},
{r:["Ca(OH)2","ZnO"],p:["CaZnO2","H2O"],cond:"",eq:"Ca(OH)₂ + ZnO → CaZnO₂ + H₂O"},
{r:["Ca(OH)2","Zn"],p:["CaZnO2","H2"],cond:"",eq:"Ca(OH)₂ + Zn  → CaZnO₂ + H₂"},
{r:["Ba(OH)2","Zn"],p:["BaZnO2","H2"],cond:"",eq:"Ba(OH)₂ + Zn  → BaZnO₂ + H₂"},

// --- oxit bazơ + axit ---
{r:["BaO2","HCl"],p:["BaCl2","H2O2"],cond:"",eq:"BaO₂ + 2HCl → BaCl₂ + H₂O₂"},
{r:["CaO2","HCl "],p:["CaCl2","H2O2"],cond:"",eq:"CaO₂ + 2HCl → CaCl₂ + H₂O₂"},
{r:["CaO22","HCl"],p:["NaCl","H2O2"],cond:"",eq:"Na₂O₂ + 2HCl → 2NaCl + H₂O₂"},
{r:["K2O2","HCl"],p:["KCl","H2O2"],cond:"",eq:"K₂O₂ + 2HCl → 2KCl + H₂O₂"},
{r:["BaO","HCl"],p:["BaCl2","H2O"],cond:"",eq:"BaO + 2HCl → BaCl₂ + H₂O"},
{r:["CaO","HCl "],p:["CaCl2","H2O"],cond:"",eq:"CaO + 2HCl → CaCl₂ + H₂O"},
{r:["Na2O","HCl"],p:["NaCl","H2O"],cond:"",eq:"Na₂O + 2HCl → 2NaCl + H₂O"},
{r:["K2O","HCl"],p:["KCl","H2O"],cond:"",eq:"K₂O + 2HCl → 2KCl + H₂O"},
{r:["MgO","HCl"],p:["MgCl2","H2O"],cond:"",eq:"MgO + 2HCl → MgCl₂ + H₂O"},
{r:["CuO","HCl"],p:["CuCl2","H2O"],cond:"",eq:"CuO + 2HCl → CuCl₂ + H₂O"},
{r:["Fe3O4","HCl"],p:["FeCl3","FeCl2","H2O"],cond:"",eq:"Fe₃O₄ + 8HCl → 2FeCl₃ + FeCl₂ + 4H₂O"},
{r:["FeO","HCl"],p:["FeCl2","H2O"],cond:"",eq:"FeO + 2HCl → FeCl₂ + H₂O"},
{r:["Fe2O3","HCl"],p:["FeCl3","H2O"],cond:"",eq:"Fe₂O₃ + 6HCl → 2FeCl₃ + 3H₂O"},
{r:["Ag2O","HCl"],p:["AgCl","H2O"],cond:"",eq:"Ag₂O + 2HCl → 2AgCl + H₂O"},
{r:["ZnO","HCl"],p:["ZnCl2","H2O"],cond:"",eq:"ZnO + 2HCl → ZnCl₂ + H₂O"},
{r:["Al2O3","HCl"],p:["AlCl3","H2O"],cond:"",eq:"Al₂O₃ + 6HCl → 2AlCl₃ + 3H₂O"},

{r:["BaO2","H2SO4 loãng"],p:["BaSO4","H2O2"],cond:"",eq:"BaO₂ + H₂SO₄ loãng → BaSO₄ + H₂O₂"},
{r:["CaO2","H2SO4 loãng "],p:["CaSO4","H2O2"],cond:"",eq:"CaO₂ + H₂SO₄ loãng → CaSO₄ + H₂O₂"},
{r:["Na2O2","H2SO4 loãng"],p:["Na2SO4","H2O2"],cond:"",eq:"Na₂O₂ + H₂SO₄ loãng → Na₂SO₄ + H₂O₂"},
{r:["K2O2","H2SO4 loãng"],p:["K2SO4","H2O2"],cond:"",eq:"K₂O₂ + H₂SO₄ loãng → K₂SO₄ + H₂O₂"},
{r:["BaO","H2SO4 loãng"],p:["BaSO4","H2O"],cond:"",eq:"BaO + H₂SO₄ loãng → BaSO₄ + H₂O"},
{r:["CaO","H2SO4 loãng "],p:["CaSO4","H2O"],cond:"",eq:"CaO + H₂SO₄ loãng → CaSO₄ + H₂O"},
{r:["Na2O","H2SO4 loãng"],p:["Na2SO4","H2O"],cond:"",eq:"Na₂O + H₂SO₄ loãng → Na₂SO₄ + H₂O"},
{r:["K2O","H2SO4 loãng"],p:["K2SO4","H2O"],cond:"",eq:"K₂O + H₂SO₄ loãng → K₂SO₄ + H₂O"},
{r:["Fe3O4","H2SO4 loãng"],p:["Fe2SO43","H2O","SO2"],cond:"",eq:"Fe3O4 + 4H2SO4 loãng → Fe2(SO4)3 + FeSO4 + 4H2O"},
{r:["CuO","H2SO4 loãng"],p:["CuSO4","H2O"],cond:"",eq:"CuO + H₂SO₄ loãng → CuSO₄ + H₂O"},
{r:["MgO","H2SO4 loãng"],p:["MgSO4","H2O"],cond:"",eq:"MgO + H₂SO₄ loãng → MgSO₄ + H₂O"},
{r:["Fe2O3","H2SO4 loãng"],p:["Fe2SO43","H2O"],cond:"",eq:"Fe₂O₃ + 3H₂SO₄ loãng → Fe₂(SO₄)₃ + 3H₂O"},
{r:["FeO","H2SO4 loãng"],p:["FeSO4","H2O"],cond:"",eq:"FeO + H₂SO₄ loãng → FeSO₄ + 4H₂O"},
{r:["Ag2O","H2SO4 loãng"],p:["AgSO4","H2O"],cond:"",eq:"Ag₂O + H₂SO₄ loãng → 2AgSO₄ + H₂O"},
{r:["ZnO","H2SO4 loãng"],p:["ZnSO4","H2O"],cond:"",eq:"ZnO + H₂SO₄ loãng → ZnSO₄ + H₂O"},
{r:["Al2O3","H2SO4 loãng"],p:["Al2(SO4)3","H2O"],cond:"",eq:"Al₂O₃ + 3H₂SO₄ loãng → Al₂(SO₄)₃ + 3H₂O"},

{r:["BaO","H2SO4 đặc"],p:["BaSO4","H2O"],cond:"",eq:"BaO + H₂SO₄ đặc → BaSO₄ + H₂O"},
{r:["CaO","H2SO4 đặc"],p:["CaSO4","H2O"],cond:"",eq:"CaO + H₂SO₄ đặc → CaSO₄ + H₂O"},
{r:["Na2O","H2SO4 đặc"],p:["Na2SO4","H2O"],cond:"",eq:"Na₂O + H₂SO₄ đặc → Na₂SO₄ + H₂O"},
{r:["K2O","H2SO4 đặc"],p:["K2SO4","H2O"],cond:"",eq:"K₂O + H₂SO₄ đặc → K₂SO₄ + H₂O"},
{r:["Fe3O4","H2SO4 đặc"],p:["Fe2SO43","H2O","SO2"],cond:"",eq:"Fe₃O₄ + 10H₂SO₄ đặc → 3Fe(SO₄)₃ + SO₂↑ + 10H₂O"},
{r:["CuO","H2SO4 đặc"],p:["CuSO4","H2O"],cond:"",eq:"CuO + H₂SO₄ đặc → CuSO₄ + H₂O"},
{r:["MgO","H2SO4 đặc"],p:["MgSO4","H2O"],cond:"",eq:"MgO + H₂SO₄ đặc → MgSO₄ + H₂O"},
{r:["Fe2O3","H2SO4 đặc"],p:["Fe2SO43","H2O"],cond:"",eq:"Fe₂O₃ + 3H₂SO₄ đặc → Fe₂(SO₄)₃ + 3H₂O"},
{r:["FeO","H2SO4 đặc"],p:["Fe2SO43","H2O","SO2"],cond:"",eq:"3FeO + 4H₂SO₄ đặc → Fe₂(SO₄)₃ + SO₂↑ + 4H₂O"},
{r:["Ag2O","H2SO4 đặc"],p:["AgSO4","H2O"],cond:"",eq:"Ag₂O + H₂SO₄ đặc → 2AgSO₄ + H₂O"},
{r:["ZnO","H2SO4 đặc"],p:["ZnSO4","H2O"],cond:"",eq:"ZnO + H₂SO₄ đặc → ZnSO₄ + H₂O"},
{r:["Al2O3","H2SO4 đặc"],p:["Al2(SO4)3","H2O"],cond:"",eq:"Al₂O₃ + 3H₂SO₄ đặc → Al₂(SO₄)₃ + 3H₂O"},

{r:["BaO2","HNO3"],p:["BaNO32","H2O2"],cond:"",eq:"BaO₂ + 2HNO₃ → Ba(NO₃)₂ + H₂O₂"},
{r:["CaO2","HNO3"],p:["CaNO32","H2O2"],cond:"",eq:"CaO₂ + 2HNO₃ → Ca(NO₃)₂ + H₂O₂"},
{r:["Na2O2","HNO3"],p:["NaNO3","H2O2"],cond:"",eq:"Na₂O₂ + 2HNO₃ → 2NaNO₃ + H₂O₂"},
{r:["K2O2","HNO3"],p:["KNO3","H2O2"],cond:"",eq:"K₂O₂ + 2HNO₃ → 2KNO₃ + H₂O₂"},
{r:["BaO","HNO3"],p:["BaNO32","H2O"],cond:"",eq:"BaO + 2HNO₃ → Ba(NO₃)₂ + H₂O"},
{r:["CaO","HNO3"],p:["CaNO32","H2O"],cond:"",eq:"CaO + 2HNO₃ → Ca(NO₃)₂ + H₂O"},
{r:["Na2O","HNO3"],p:["NaNO3","H2O"],cond:"",eq:"Na₂O + 2HNO₃ → 2NaNO₃ + H₂O"},
{r:["K2O","HNO3"],p:["KNO3","H2O"],cond:"",eq:"K₂O + 2HNO₃ → 2KNO₃ + H₂O"},
{r:["Fe3O4","HNO3"],p:["FeNO33","H2O","NO2"],cond:"",eq:"Fe₃O₄ + 10HNO₃ → 3Fe(NO₃)₃ + NO₂↑ + 5H₂O"},
{r:["CuO","HNO3"],p:["CuNO32","H2O"],cond:"",eq:"CuO + 2HNO₃ → Cu(NO₃)₂ + H₂O"},
{r:["MgO","HNO3"],p:["MgNO32","H2O"],cond:"",eq:"MgO + 2HNO₃ → Mg(NO₃)₂ + H₂O"},
{r:["Fe2O3","HNO3"],p:["FeNO33","H2O"],cond:"",eq:"Fe₂O₃ + 6HNO₃ → 2Fe(NO₃)₃ + 3H₂O"},
{r:["FeO","HNO3"],p:["FeNO33","H2O","NO2"],cond:"",eq:"3FeO + 4HNO₃ → Fe(NO₃)₃ +NO₂↑ + 2H₂O"},
{r:["Ag2O","HNO3"],p:["AgNO3","H2O"],cond:"",eq:"Ag₂O + 2HNO₃ → 2AgNO₃ + H₂O"},
{r:["ZnO","HNO3"],p:["ZnNO32","H2O"],cond:"",eq:"ZnO + 2HNO₃ → Zn(NO₃)₂ + H₂O"},
{r:["Al2O3","HNO3"],p:["AlNO33","H2O"],cond:"",eq:"Al₂O₃ + 6HNO₃ → 2Al(NO₃)₃ + 3H₂O"},

{r:["BaO2","H3PO4"],p:["Ba3PO42","H2O2"],cond:"",eq:"3BaO₂ + 2H₃PO₄ → Ba₃(PO₄)₂ + 3H₂O₂"},
{r:["CaO2","H3PO4"],p:["Ca3PO42","H2O2"],cond:"",eq:"3CaO₂ + 2H₃PO₄ → Ca₃(PO₄)₂ + 3H₂O₂"},
{r:["Na2O2","H3PO4"],p:["Na3PO4","H2O2"],cond:"",eq:"3Na₂O₂ + 2H₃PO₄ → 2Na₃PO₄ + 3H₂O₂"},
{r:["K2O2","H3PO4"],p:["K3PO4","H2O2"],cond:"",eq:"3K₂O₂ + 2H₃PO₄ → 2K₃PO₄ + 3H₂O₂"},
{r:["Na2O","H3PO4"],p:["Na3PO4","H2O"],cond:"",eq:"3Na₂O + 2H₃PO₄ → 2Na₃PO₄ + 3H₂O"},
{r:["K2O","H3PO4"],p:["K3PO4","H2O"],cond:"",eq:"3K₂O + 2H₃PO₄ → 2K₃PO₄ + 3H₂O"},
{r:["CaO","H3PO4"],p:["Ca3PO42","H2O"],cond:"",eq:"3CaO + 2H₃PO₄ → Ca₃(PO₄)₂ + 3H₂O"},
{r:["BaO","H3PO4"],p:["Ba3PO42","H2O"],cond:"",eq:"3BaO + 2H₃PO₄ → Ba₃(PO₄)₂ + 3H₂O"},
{r:["Fe3O4","H3PO4"],p:["Fe3PO43","H2O","NO2"],cond:"",eq:"Fe₃O₄ + 8H₃PO₄ → Fe₃(PO₄)₂ + 2FePO₄ + 4H₂O"},
{r:["FeO","H3PO4"],p:["Fe3PO42","H2O","NO2"],cond:"",eq:"3FeO + 2H₃PO₄ → Fe₃(PO₄)₂ + 3H₂O"},
{r:["Fe2O3","H3PO4"],p:["FePO4","H2O"],cond:"",eq:"Fe₂O₃ + 2H₃PO₄ → 2FePO₄ + 3H₂O"},
{r:["Ag2O","H3PO4"],p:["Ag3PO4","H2O"],cond:"",eq:"3Ag₂O + 2H₃PO₄ → 2Ag₃PO₄ + 3H₂O"},
{r:["ZnO","H3PO4"],p:["Zn3PO42","H2O"],cond:"",eq:"3ZnO + 2H₃PO₄ → Zn₃(PO₄)₂ + 3H₂O"},
{r:["Al2O3","H3PO4"],p:["AlPO4","H2O"],cond:"",eq:"Al₂O₃ + 2H₃PO₄ → 2AlPO₄ + 3H₂O"},
{r:["MgO","H3PO4"],p:["Mg3PO42","H2O"],cond:"",eq:"3MgO + 2H₃PO₄ → Mg₃(PO₄)₂ + 3H₂O"},
{r:["CuO","H3PO4"],p:["Cu3PO42","H2O"],cond:"",eq:"3CuO + 2H₃PO₄ → Cu₃(PO₄)₂ + 3H₂O"},

// --- axit + muối cacbonat ---
{r:["HCl","CaCO3"],p:["CaCl2","CO2","H2O"],cond:"",eq:"CaCO₃ + 2HCl → CaCl₂ + CO₂↑ + H₂O"},
{r:["HCl","Na2CO3"],p:["NaCl","CO2","H2O"],cond:"",eq:"Na₂CO₃ + 2HCl → 2NaCl + CO₂↑ + H₂O"},
{r:["HCl","NaHCO3"],p:["NaCl","CO2","H2O"],cond:"",eq:"NaHCO₃ + HCl → NaCl + CO₂↑ + H₂O"},
{r:["H2SO4","Na2CO3"],p:["Na2SO4","CO2","H2O"],cond:"",eq:"Na₂CO₃ + H₂SO₄ → Na₂SO₄ + CO₂↑ + H₂O"},
{r:["H2SO4","BaCO3"],p:["BaSO4","CO2","H2O"],cond:"",eq:"BaCO₃ + H₂SO₄ → BaSO₄↓ + CO₂↑ + H₂O"},

// --- kim loại đẩy kim loại khỏi muối ---
{r:["Fe","CuSO4"],p:["FeSO4","Cu"],cond:"",eq:"Fe + CuSO₄ → FeSO₄ + Cu"},
{r:["Cu","AgNO3"],p:["CuNO32","Ag"],cond:"",eq:"Cu + 2AgNO₃ → Cu(NO₃)₂ + 2Ag"},
{r:["Zn","CuSO4"],p:["ZnSO4","Cu"],cond:"",eq:"Zn + CuSO₄ → ZnSO₄ + Cu"},
{r:["Fe","AgNO3"],p:["FeNO32","Ag"],cond:"",eq:"Fe + 2AgNO₃ → Fe(NO₃)₂ + 2Ag"},
{r:["Al","CuSO4"],p:["Al2SO43","Cu"],cond:"",eq:"2Al + 3CuSO₄ → Al₂(SO₄)₃ + 3Cu"},
{r:["Mg","CuSO4"],p:["MgSO4","Cu"],cond:"",eq:"Mg + CuSO₄ → MgSO₄ + Cu"},




// --- bazơ + muối (kết tủa hiđroxit) ---
{r:["NaOH","FeCl3"],p:["FeOH3","NaCl"],cond:"",eq:"3NaOH + FeCl₃ → Fe(OH)₃↓ + 3NaCl"},
{r:["NaOH","FeCl2"],p:["FeOH2","NaCl"],cond:"",eq:"2NaOH + FeCl₂ → Fe(OH)₂↓ + 2NaCl"},
{r:["NaOH","CuSO4"],p:["CuOH2","Na2SO4"],cond:"",eq:"2NaOH + CuSO₄ → Cu(OH)₂↓ + Na₂SO₄"},
{r:["NaOH","MgCl2"],p:["MgOH2","NaCl"],cond:"",eq:"2NaOH + MgCl₂ → Mg(OH)₂↓ + 2NaCl"},
{r:["NaOH","AlCl3"],p:["AlOH3","NaCl"],cond:"",eq:"3NaOH + AlCl₃ → Al(OH)₃↓ + 3NaCl"},
{r:["NaOH","ZnCl2"],p:["ZnOH2","NaCl"],cond:"",eq:"2NaOH + ZnCl₂ → Zn(OH)₂↓ + 2NaCl"},
{r:["NaOH","NH4Cl"],p:["NaCl","NH3","H2O"],cond:"t°",eq:"NaOH + NH₄Cl → NaCl + NH₃↑ + H₂O"},
{r:["Ca(OH)2","FeCl3"],p:["FeOH3","CaCl2"],cond:"",eq:"3Ca(OH)2 + 2FeCl3 → 2Fe(OH)3↓ + 3CaCl2"},
{r:["Ca(OH)2","FeCl2"],p:["FeOH2","CaCl2"],cond:"",eq:"Ca(OH)2 + FeCl2 → Fe(OH)2↓ + CaCl2"},
{r:["Ca(OH)2","CuSO4"],p:["CuOH2","CaSO4"],cond:"",eq:"Ca(OH)2 + CuSO4 → Cu(OH)2↓ + CaSO4"},
{r:["Ca(OH)2","MgCl2"],p:["MgOH2","CaCl2"],cond:"",eq:"Ca(OH)2 + MgCl2 → Mg(OH)2↓ + CaCl2"},
{r:["Ca(OH)2","AlCl3"],p:["AlOH3","CaCl3"],cond:"",eq:"3Ca(OH)2 + 2AlCl3 → 2Al(OH)3↓ + 3CaCl3"},
{r:["Ca(OH)2","ZnCl2"],p:["ZnOH2","CaCl2"],cond:"",eq:"Ca(OH)2 + ZnCl2 → Zn(OH)2↓ + CaCl2"},
{r:["Ca(OH)2","NH4Cl"],p:["CaCl2","NH3","H2O"],cond:"t°",eq:"Ca(OH)2 + 2NH4Cl → CaCl2 + 2NH3↑ + 2H2O"},
{r:["Ba(OH)2","FeCl3"],p:["FeOH3","BaCl2"],cond:"",eq:"3Ba(OH)2 + 2FeCl3 → 2Fe(OH)3↓ + 3BaCl2"},
{r:["Ba(OH)2","FeCl2"],p:["FeOH2","BaCl2"],cond:"",eq:"Ba(OH)2 + FeCl2 → Fe(OH)2↓ + BaCl2"},
{r:["Ba(OH)2","CuSO4"],p:["CuOH2","BaSO4"],cond:"",eq:"Ba(OH)2 + CuSO4 → Cu(OH)2↓ + BaSO4"},
{r:["Ba(OH)2","MgCl2"],p:["MgOH2","BaCl2"],cond:"",eq:"Ba(OH)2 + MgCl2 → Mg(OH)2↓ + BaCl2"},
{r:["Ba(OH)2","AlCl3"],p:["AlOH3","BaCl3"],cond:"",eq:"3Ba(OH)2 + 2AlCl3 → 2Al(OH)3↓ + 3BaCl3"},
{r:["Ba(OH)2","ZnCl2"],p:["ZnOH2","BaCl2"],cond:"",eq:"Ba(OH)2 + ZnCl2 → Zn(OH)2↓ + BaCl2"},
{r:["Ba(OH)2","NH4Cl"],p:["BaCl2","NH3","H2O"],cond:"t°",eq:"Ba(OH)2 + 2NH4Cl → BaCl2 + 2NH3↑ + 2H2O"},
{r:["KOH","FeCl3"],p:["FeOH3","KCl"],cond:"",eq:"3KOH + FeCl₃ → Fe(OH)₃↓ + 3KCl"},
{r:["KOH","FeCl2"],p:["FeOH2","KCl"],cond:"",eq:"2KOH + FeCl₂ → Fe(OH)₂↓ + 2KCl"},
{r:["KOH","CuSO4"],p:["CuOH2","K2SO4"],cond:"",eq:"2KOH + CuSO₄ → Cu(OH)₂↓ + K₂SO₄"},
{r:["KOH","MgCl2"],p:["MgOH2","KCl"],cond:"",eq:"2KOH + MgCl₂ → Mg(OH)₂↓ + 2KCl"},
{r:["KOH","AlCl3"],p:["AlOH3","KCl"],cond:"",eq:"3KOH + AlCl₃ → Al(OH)₃↓ + 3KCl"},
{r:["KOH","ZnCl2"],p:["ZnOH2","KCl"],cond:"",eq:"2KOH + ZnCl₂ → Zn(OH)₂↓ + 2KCl"},
{r:["KOH","NH4Cl"],p:["KCl","NH3","H2O"],cond:"t°",eq:"KOH + NH₄Cl → KCl + NH₃↑ + H₂O"},







// --- muối + muối (kết tủa) ---
{r:["AgNO3","NaCl"],p:["AgCl","NaNO3"],cond:"",eq:"AgNO₃ + NaCl → AgCl↓ + NaNO₃"},
{r:["AgNO3","KCl"],p:["AgCl","KNO3"],cond:"",eq:"AgNO₃ + KCl → AgCl↓ + KNO₃"},
{r:["AgNO3","CaCl2"],p:["AgCl","CaNO32"],cond:"",eq:"2AgNO₃ + CaCl₂ → 2AgCl↓ + Ca(NO₃)₂"},
{r:["AgNO3","Na2SO4"],p:["Ag2SO4","NaNO3"],cond:"",eq:"2AgNO₃ + Na₂SO₄ → Ag₂SO₄↓ + 2NaNO₃"},
{r:["BaCl2","Na2SO4"],p:["BaSO4","NaCl"],cond:"",eq:"BaCl₂ + Na₂SO₄ → BaSO₄↓ + 2NaCl"},
{r:["BaCl2","K2SO4"],p:["BaSO4","KCl"],cond:"",eq:"BaCl₂ + K₂SO₄ → BaSO₄↓ + 2KCl"},
{r:["AgNO3","Na2S"],p:["Ag2S","NaNO3"],cond:"",eq:"2AgNO₃ + Na₂S → Ag₂S↓ + 2NaNO₃"},
{r:["AgNO3","Na3PO4"],p:["Ag3PO4","NaNO3"],cond:"",eq:"3AgNO₃ + Na₃PO₄ → Ag₃PO₄↓ + 3NaNO₃"},
{r:["Na2CO3","CaCl2"],p:["CaCO3","NaCl"],cond:"",eq:"Na₂CO₃ + CaCl₂ → CaCO₃↓ + 2NaCl"},
{r:["Na2CO3","BaCl2"],p:["BaCO3","NaCl"],cond:"",eq:"Na₂CO₃ + BaCl₂ → BaCO₃↓ + 2NaCl"},
{r:["Na2S","CuSO4"],p:["CuS","Na2SO4"],cond:"",eq:"Na₂S + CuSO₄ → CuS↓ + Na₂SO₄"},
{r:["Na2S","ZnSO4"],p:["ZnS","Na2SO4"],cond:"",eq:"Na₂S + ZnSO₄ → ZnS↓ + Na₂SO₄"},

// --- halogen đẩy nhau ---
{r:["Cl2","NaBr"],p:["NaCl","Br2"],cond:"",eq:"Cl₂ + 2NaBr → 2NaCl + Br₂"},
{r:["Cl2","KI"],p:["KCl","I2"],cond:"",eq:"Cl₂ + 2KI → 2KCl + I₂"},
{r:["Br2","NaI"],p:["NaBr","I2"],cond:"",eq:"Br₂ + 2NaI → 2NaBr + I₂"},


// --- phân huỷ nhiệt ---
{r:["CaCO3"],p:["CaO","CO2"],cond:"t° cao",eq:"CaCO₃ → CaO + CO₂↑"},
{r:["NaHCO3"],p:["Na2CO3","CO2","H2O"],cond:"t°",eq:"2NaHCO₃ → Na₂CO₃ + CO₂↑ + H₂O"},
{r:["CaHCO32"],p:["CaCO3","CO2","H2O"],cond:"t°",eq:"Ca(HCO₃)₂ → CaCO₃↓ + CO₂↑ + H₂O"},
{r:["CuOH2"],p:["CuO","H2O"],cond:"t°",eq:"Cu(OH)₂ → CuO + H₂O"},
{r:["FeOH3"],p:["Fe2O3","H2O"],cond:"t°",eq:"2Fe(OH)₃ → Fe₂O₃ + 3H₂O"},
{r:["NH4Cl"],p:["NH3","HCl"],cond:"t°",eq:"NH₄Cl → NH₃↑ + HCl↑"},
{r:["KMnO4"],p:["K2MnO4","O2"],cond:"t°",eq:"2KMnO₄ → K₂MnO₄ + O₂↑"},

// --- điện phân ---
{r:["H2O"],p:["H2","O2"],cond:"điện phân",eq:"2H₂O → 2H₂↑ + O₂↑"},
{r:["NaCl","H2O"],p:["NaOH","Cl2","H2"],cond:"điện phân dd, màng ngăn",eq:"2NaCl + 2H₂O → 2NaOH + Cl₂↑ + H₂↑"},
{r:["Al2O3"],p:["Al","O2"],cond:"điện phân nóng chảy, criolit",eq:"2Al₂O₃ → 4Al + 3O₂↑"},
{r:["CuCl2"],p:["Cu","Cl2"],cond:"điện phân",eq:"CuCl₂ → Cu + Cl₂↑"},
{r:["H2SO4 loãng"],p:["H2S2O8","H2"],cond:"điện phân dung dịch",eq:"2H₂SO₄ loãng → H₂S₂O₈ + H₂↑"},

// --- khử oxit kim loại ---
{r:["H2","CuO"],p:["Cu","H2O"],cond:"t°",eq:"H₂ + CuO → Cu + H₂O"},
{r:["H2","Fe2O3"],p:["Fe","H2O"],cond:"t°",eq:"3H₂ + Fe₂O₃ → 2Fe + 3H₂O"},
{r:["CO","CuO"],p:["Cu","CO2"],cond:"t°",eq:"CO + CuO → Cu + CO₂"},
{r:["CO","Fe2O3"],p:["Fe","CO2"],cond:"t°",eq:"3CO + Fe₂O₃ → 2Fe + 3CO₂"},
{r:["CO","Fe3O4"],p:["Fe","CO2"],cond:"t°",eq:"4CO + Fe₃O₄ → 3Fe + 4CO₂"},
{r:["C","CO2"],p:["CO"],cond:"t° cao",eq:"C + CO₂ → 2CO"},
{r:["C","Fe2O3"],p:["Fe","CO2"],cond:"t° cao",eq:"3C + 2Fe₂O₃ → 4Fe + 3CO₂"},
{r:["C","CuO"],p:["Cu","CO2"],cond:"t°",eq:"2CuO + C → 2Cu + CO₂"},
{r:["C","SiO2"],p:["Si","CO"],cond:"t° cao",eq:"SiO₂ + 2C → Si + 2CO"},

// --- điều chế cacbua & hoá hữu cơ ---
{r:["CaO","C"],p:["CaC2","CO"],cond:"lò điện, ~2000°C",eq:"CaO + 3C → CaC₂ + CO"},
{r:["Al","C"],p:["Al4C3"],cond:"t° cao",eq:"4Al + 3C → Al₄C₃"},
{r:["CaC2","H2O"],p:["C2H2","CaOH2"],cond:"",eq:"CaC₂ + 2H₂O → C₂H₂↑ + Ca(OH)₂"},
{r:["Al4C3","H2O"],p:["CH4","AlOH3"],cond:"",eq:"Al₄C₃ + 12H₂O → 3CH₄↑ + 4Al(OH)₃"},
{r:["C2H2","H2"],p:["C2H4"],cond:"xt Pd, t°",eq:"C₂H₂ + H₂ → C₂H₄"},
{r:["C2H4","H2"],p:["C2H6"],cond:"xt Ni, t°",eq:"C₂H₄ + H₂ → C₂H₆"},
{r:["C2H4","H2O"],p:["C2H5OH"],cond:"xt axit, t°",eq:"C₂H₄ + H₂O → C₂H₅OH"},
{r:["C2H2","H2O"],p:["CH3CHO"],cond:"xt HgSO₄, t°",eq:"C₂H₂ + H₂O → CH₃CHO"},
{r:["CH3CHO","H2"],p:["C2H5OH"],cond:"xt Ni, t°",eq:"CH₃CHO + H₂ → C₂H₅OH"},
{r:["CH3CHO","O2"],p:["CH3COOH"],cond:"xt Mn²⁺",eq:"2CH₃CHO + O₂ → 2CH₃COOH"},
{r:["C2H5OH","O2"],p:["CH3COOH","H2O"],cond:"men giấm",eq:"C₂H₅OH + O₂ → CH₃COOH + H₂O"},
{r:["C2H5OH","Na"],p:["C2H5ONa","H2"],cond:"",eq:"2C₂H₅OH + 2Na → 2C₂H₅ONa + H₂↑"},
{r:["CH3COOH","Na"],p:["CH3COONa","H2"],cond:"",eq:"2CH₃COOH + 2Na → 2CH₃COONa + H₂↑"},
{r:["CH3COOH","C2H5OH"],p:["CH3COOC2H5","H2O"],cond:"H₂SO₄ đặc, t°",eq:"CH₃COOH + C₂H₅OH ⇌ CH₃COOC₂H₅ + H₂O"},
{r:["CH3COONa","NaOH"],p:["CH4","Na2CO3"],cond:"CaO, t°",eq:"CH₃COONa + NaOH → CH₄↑ + Na₂CO₃"},
{r:["CH4","Cl2"],p:["CH3Cl","HCl"],cond:"ánh sáng",eq:"CH₄ + Cl₂ → CH₃Cl + HCl"},
{r:["C2H6","Cl2"],p:["C2H5Cl","HCl"],cond:"ánh sáng",eq:"C₂H₆ + Cl₂ → C₂H₅Cl + HCl"},
{r:["C6H12O6"],p:["C2H5OH","CO2"],cond:"men rượu, 30-35°C",eq:"C₆H₁₂O₆ → 2C₂H₅OH + 2CO₂↑"},
{r:["C2H2"],p:["C6H6"],cond:"xt, t° cao",eq:"3C₂H₂ → C₆H₆"},
{r:["C2H5OH"],p:["C2H4","H2O"],cond:"H₂SO₄ đặc, 170°C",eq:"C₂H₅OH → C₂H₄↑ + H₂O"},
{r:["CO","H2"],p:["CH3OH"],cond:"xt, t°, p",eq:"CO + 2H₂ → CH₃OH"},
{r:["CH3OH","O2"],p:["HCHO","H2O"],cond:"xt Cu, t°",eq:"2CH₃OH + O₂ → 2HCHO + 2H₂O"},

//==================== HỮU CƠ CƠ BẢN ====================

{r:["C","H2"],p:["CH4"],cond:"xt Ni,t°",eq:"C + 2H₂ → CH₄"},
{r:["CH4","O2"],p:["CH3OH"],cond:"xt",eq:"2CH₄ + O₂ → 2CH₃OH"},
{r:["CH3OH"],p:["CH2O","H2"],cond:"Cu,t°",eq:"CH₃OH → CH₂O + H₂"},
{r:["CH2O","H2"],p:["CH3OH"],cond:"Ni",eq:"CH₂O + H₂ → CH₃OH"},
{r:["CH2O","O2"],p:["HCOOH"],cond:"",eq:"2CH₂O + O₂ → 2HCOOH"},
{r:["HCOOH","NaOH"],p:["HCOONa","H2O"],cond:"",eq:"HCOOH + NaOH → HCOONa + H₂O"},

//==================== ETAN ====================

{r:["CH4"],p:["C2H6","H2"],cond:"t°",eq:"2CH₄ → C₂H₆ + H₂"},
{r:["C2H6"],p:["C2H4","H2"],cond:"xt,t°",eq:"C₂H₆ → C₂H₄ + H₂"},
{r:["C2H4"],p:["C2H2","H2"],cond:"xt,t°",eq:"C₂H₄ → C₂H₂ + H₂"},
{r:["C2H4","H2O"],p:["C2H5OH"],cond:"H₃PO₄",eq:"C₂H₄ + H₂O → C₂H₅OH"},
{r:["C2H5OH"],p:["CH3CHO","H2"],cond:"Cu,t°",eq:"C₂H₅OH → CH₃CHO + H₂"},
{r:["CH3CHO","O2"],p:["CH3COOH"],cond:"",eq:"2CH₃CHO + O₂ → 2CH₃COOH"},
{r:["CH3COOH","NaOH"],p:["CH3COONa","H2O"],cond:"",eq:"CH₃COOH + NaOH → CH₃COONa + H₂O"},

//==================== ESTE ====================

{r:["CH3COOH","C2H5OH"],p:["CH3COOC2H5","H2O"],cond:"H₂SO₄ đặc",eq:"CH₃COOH + C₂H₅OH ⇌ CH₃COOC₂H₅ + H₂O"},
{r:["CH3COOC2H5","H2O"],p:["CH3COOH","C2H5OH"],cond:"H⁺",eq:"CH₃COOC₂H₅ + H₂O ⇌ CH₃COOH + C₂H₅OH"},

//==================== GLUCO ====================

{r:["CO2","H2O"],p:["C6H12O6","O2"],cond:"ánh sáng",eq:"6CO₂ + 6H₂O → C₆H₁₂O₆ + 6O₂"},
{r:["C6H12O6"],p:["C2H5OH","CO2"],cond:"men",eq:"C₆H₁₂O₆ → 2C₂H₅OH + 2CO₂"},
{r:["C6H12O6","O2"],p:["CO2","H2O"],cond:"",eq:"C₆H₁₂O₆ + 6O₂ → 6CO₂ + 6H₂O"},

//==================== BENZEN ====================

{r:["C2H2"],p:["C6H6"],cond:"xt,t°",eq:"3C₂H₂ → C₆H₆"},
{r:["C6H6","H2"],p:["C6H12"],cond:"Ni",eq:"C₆H₆ + 3H₂ → C₆H₁₂"},
{r:["C6H6","Cl2"],p:["C6H5Cl","HCl"],cond:"FeCl₃",eq:"C₆H₆ + Cl₂ → C₆H₅Cl + HCl"},

//==================== POLIME ====================

{r:["C2H4"],p:["PE"],cond:"xt,p",eq:"nC₂H₄ → (–CH₂–CH₂–)ₙ"},
{r:["C2H2"],p:["PVC"],cond:"xt",eq:"nCH₂=CHCl → PVC"},
{r:["C6H5Cl"],p:["PS"],cond:"xt",eq:"nC₈H₈ → PS"},
// --- điều chế khác ---
{r:["MnO2","KClO3","KOH"],p:["K2MnO4","KCl","H2O"],cond:"t° cao",eq:" 3MnO₂ + KClO₃ + 6KOH → 3K₂MnO₄ + KCl + 3H₂O"},
{r:["K2MnO4","Cl2"],p:["KMnO4","KCl"],cond:"t° cao",eq:" 2K₂MnO₄ + Cl₂ → 2KMnO₄ + 2KCl"},
{r:["H2S2O8","H2O"],p:["H2SO4","H2O2"],cond:"t° cao",eq:" H2S2O8 + H2O → H2SO4 + H2O2"},
{r:["Na","H"],p:["NaH"],cond:"t° cao",eq:" 2Na + H₂ → 2NaH"},
{r:["K","H"],p:["KH"],cond:"t° cao",eq:" 2K + H₂ → 2KH"},
{r:["Ba","H"],p:["BaH2"],cond:"t° cao",eq:" 2Ba + H₂ → 2BaH₂"},
{r:["Ca","H"],p:["CaH2"],cond:"t° cao",eq:" 2Ca + H₂ → 2CaH₂"},


];






/* =========================================================
   ENGINE
   ========================================================= */
const CATS = [
  {id:"all",label:"Tất cả"},
  {id:"element",label:"Đơn chất"},
  {id:"oxide",label:"Oxit"},
  {id:"base",label:"Bazơ"},
  {id:"acid",label:"Axit"},
  {id:"salt",label:"Muối"},
  {id:"organic",label:"Hữu cơ"},
    {id:"polymer",label:"Polymer"},
  {id:"other",label:"Khác"}
];
const allIds = Object.keys(S);
const elementIds = allIds.filter(id=>S[id].c==="element");

let unlocked = new Set(elementIds);
let flask = [];
let activeCat = "all";
let reactionCount = 0;

const elTiles = document.getElementById("tiles");
const elTabs = document.getElementById("tabs");
const elFlask = document.getElementById("flask");
const elResult = document.getElementById("resultArea");
const elLog = document.getElementById("log");
const elSearch = document.getElementById("search");
const reactBtn = document.getElementById("reactBtn");
const clearBtn = document.getElementById("clearBtn");

document.getElementById("fCount").textContent = allIds.length;
document.getElementById("fReact").textContent = R.length;

function renderTabs(){
  elTabs.innerHTML = "";
  CATS.forEach(cat=>{
    const b = document.createElement("button");
    b.className = "tab" + (cat.id===activeCat ? " active":"");
    b.textContent = cat.label;
    b.onclick = ()=>{ activeCat = cat.id; renderTabs(); renderTiles(); };
    elTabs.appendChild(b);
  });
}

function renderTiles(){
  const q = elSearch.value.trim().toLowerCase();
  elTiles.innerHTML = "";
  allIds.forEach(id=>{
    const sub = S[id];
    if(activeCat!=="all" && sub.c!==activeCat) return;
    if(q){
      const plain = sub.f.replace(/<[^>]+>/g,"").toLowerCase();
      if(!plain.includes(q) && !sub.n.toLowerCase().includes(q)) return;
    }
    const isUnlocked = unlocked.has(id);
    const div = document.createElement("div");
    div.className = "tile c-"+sub.c + (isUnlocked?"":" locked");
    div.innerHTML = `<div class="catbar"></div><span class="f">${sub.f}</span><span class="n">${sub.n}</span>`;
    if(isUnlocked){
      div.onclick = ()=>addToFlask(id);
      div.title = "Thêm "+sub.n+" vào bình";
    } else {
      div.title = "Chưa được khám phá";
    }
    elTiles.appendChild(div);
  });
}

function addToFlask(id){
  flask.push(id);
  renderFlask();
}
function removeFromFlask(idx){
  flask.splice(idx,1);
  renderFlask();
}
function renderFlask(){
  elFlask.classList.toggle("empty", flask.length===0);
  elFlask.innerHTML = "";
  flask.forEach((id,idx)=>{
    const sub = S[id];
    const chip = document.createElement("div");
    chip.className = "chip";
    chip.innerHTML = `<span class="f" style="font-weight:700">${sub.f}</span><span class="x">✕</span>`;
    chip.onclick = ()=>removeFromFlask(idx);
    elFlask.appendChild(chip);
  });
  reactBtn.disabled = flask.length < 1;
}

function findReaction(flaskSet){
  let best = null;
  for(const rx of R){
    const need = rx.r;
    const ok = need.every(id=>flaskSet.has(id));
    if(!ok) continue;
    if(!best || need.length > best.r.length) best = rx;
  }
  return best;
}

function doReaction(){
  const flaskSet = new Set(flask);
  const rx = findReaction(flaskSet);
  if(!rx){
    elResult.innerHTML = `<div class="result no"><div class="eqline">Không có phản ứng nào xảy ra giữa các chất đã chọn.</div></div>`;
    return;
  }
  // consume matched reactants (one occurrence each)
  rx.r.forEach(id=>{
    const idx = flask.indexOf(id);
    if(idx>-1) flask.splice(idx,1);
  });
  // unlock + add products back to flask
  const newlyUnlocked = [];
  rx.p.forEach(id=>{
    if(!unlocked.has(id)){ unlocked.add(id); newlyUnlocked.push(id); }
    flask.push(id);
  });
  reactionCount++;

  const condHtml = rx.cond ? `<div class="cond">Điều kiện: ${rx.cond}</div>` : `<div class="cond">Điều kiện: không cần (phản ứng xảy ra ngay khi trộn)</div>`;
  const unlockHtml = newlyUnlocked.length
    ? `<div class="unlockline">🔓 Mở khoá chất mới: ${newlyUnlocked.map(id=>S[id].f+" ("+S[id].n+")").join(", ")}</div>`
    : "";
  elResult.innerHTML = `<div class="result ok"><div class="eqline">${rx.eq}</div>${condHtml}${unlockHtml}</div>`;

  const li = document.createElement("div");
  li.className = "logitem";
  li.innerHTML = `<b>${rx.eq}</b><span class="lcond">${rx.cond || "không cần điều kiện"}</span>`;
  if(elLog.children.length===1 && elLog.children[0].style.border==="none"){ elLog.innerHTML=""; }
  elLog.appendChild(li);

  renderFlask();
  renderTiles();
  updateStats();
}

function updateStats(){
  document.getElementById("statUnlocked").textContent = unlocked.size+"/"+allIds.length;
  document.getElementById("statReactions").textContent = reactionCount;
}

reactBtn.onclick = doReaction;
clearBtn.onclick = ()=>{ flask=[]; renderFlask(); elResult.innerHTML=""; };
elSearch.oninput = renderTiles;

renderTabs();
renderTiles();
renderFlask();
updateStats();
</script>
<script>
const blockedLink = "https://2410phongnguyen-eng.github.io/KOILABORATORY/";

document.addEventListener("DOMContentLoaded", () => {
    document.querySelectorAll("a").forEach(link => {
        if (
            link.href === blockedLink ||
            link.href.startsWith(blockedLink)
        ) {
            link.remove(); // Xóa hoàn toàn khỏi trang
        }
    });
});
</script>
</body>
</html>
