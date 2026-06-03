<template>
  <!-- Page A: Pyramid -->
  <section class="product print-page">
    <div class="blob blob-gold"></div>
    <div class="section-header fade-in">
      <span class="sec-num">07</span>
      <span class="sec-tag">✦ 产品战略</span>
      <h2 class="sec-title">品牌产品金字塔</h2>
      <p class="sec-desc">每一层对应毛孩子成长的不同需求</p>
    </div>

    <div class="pyramid fade-in">
      <div class="py-level py-l3">
        <span class="py-tag">第三层</span>
        <span class="py-name">成长守护</span>
        <span class="py-desc">负责健康管理</span>
      </div>
      <div class="py-level py-l2">
        <span class="py-tag">第二层</span>
        <span class="py-name">每日奖励</span>
        <span class="py-desc">负责互动</span>
      </div>
      <div class="py-level py-l1">
        <span class="py-tag">第一层</span>
        <span class="py-name">每日主食</span>
        <span class="py-desc">负责成长</span>
      </div>
    </div>
  </section>

  <!-- Page B: Product Matrix -->
  <section class="product product-matrix print-page">
    <div class="blob blob-pink"></div>
    <div class="section-header fade-in">
      <span class="sec-num sec-num-sm">08</span>
      <span class="sec-tag">✦ 产品矩阵</span>
    </div>

    <div class="overview-img fade-in">
      <img src="/产品总图.jpg" alt="产品总览" />
    </div>

    <div class="product-tier fade-in">
      <span class="series-badge">成长系列</span>
      <h3 class="tier-title">每日主食 — 负责成长</h3>
      <div class="tier-cards">
        <div class="tier-card" v-for="(p, i) in growthProducts" :key="p.name" :class="'tc-' + (i + 1)">
          <div class="tc-name">{{ p.name }}</div>
          <div class="tc-pos">{{ p.position }}</div>
          <div class="tc-kw">
            <span class="kw-tag" v-for="k in p.keywords" :key="k">{{ k }}</span>
          </div>
        </div>
      </div>
      <div class="product-imgs">
        <img src="/主食餐盒.jpg" alt="主食餐盒" />
        <img src="/主食餐盒2.jpg" alt="主食餐盒" />
        <img src="/主食冻干.jpg" alt="主食冻干" />
      </div>
    </div>

    <div class="product-tier fade-in">
      <span class="series-badge sb-2">陪伴系列</span>
      <h3 class="tier-title">彩虹吊卡冻干 — 互动奖励</h3>
      <div class="companion-tags">
        <span class="ctag" v-for="(c, i) in companionProducts" :key="c" :class="'ct-' + (i + 1)">{{ c }}</span>
      </div>
      <div class="product-imgs imgs-2">
        <img src="/零食冻干.jpg" alt="彩虹吊卡冻干" />
      </div>
    </div>
  </section>
</template>

<script setup>
const growthProducts = [
  { name: '哒哒布丁主食餐盒', position: '定位：成长的一餐', keywords: ['鲜肉', '慕斯', '双层口感'] },
  { name: '全价主食夹心冻干', position: '定位：成长能量', keywords: ['鲜肉', '主食', '夹心'] },
]
const companionProducts = ['莓莓鸡', '虾虾圆子', '排毛小饼', '蓝莓奶豆腐', '爱心兔血']
</script>

<style scoped>
.product {
  padding: 12mm 14mm;
  position: relative;
  overflow: hidden;
}
.product-matrix {
  padding: 10mm 14mm;
}

.blob-gold, .blob-pink {
  position: absolute;
  width: 160px; height: 160px;
  border-radius: 50%;
  pointer-events: none;
}
.blob-gold {
  background: radial-gradient(circle, rgba(217,185,145,0.11) 0%, transparent 70%);
  top: -40px; right: -40px;
}
.blob-pink {
  background: radial-gradient(circle, rgba(242,217,205,0.12) 0%, transparent 70%);
  bottom: -40px; left: -40px;
}

.section-header { position: relative; z-index: 1; margin-bottom: 8mm; }
.sec-num {
  font-family: "Noto Serif SC", serif;
  font-size: 56px; font-weight: 900;
  color: rgba(217,185,145,0.07);
  position: absolute; top: -16px; right: 0;
  line-height: 1;
}
.sec-num-sm { font-size: 50px; }
.sec-tag { font-size: 10px; letter-spacing: 5px; color: var(--accent-warm); font-weight: 700; display: block; margin-bottom: 4mm; }
.sec-title { font-family: "Noto Serif SC", serif; font-size: 30px; font-weight: 900; letter-spacing: 3px; color: var(--text); line-height: 1.2; }
.sec-desc { font-size: 13px; color: var(--text-mid); letter-spacing: 2px; margin-top: 2mm; }

/* Pyramid */
.pyramid {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 4mm;
  margin-top: 6mm;
  position: relative; z-index: 1;
}
.py-level {
  text-align: center;
  border-radius: 12px;
  padding: 8mm;
}
.py-l3 {
  width: 46%;
  background: #FFFDF9;
  border: 2px solid rgba(217,185,145,0.20);
  box-shadow: var(--card-shadow);
}
.py-l2 {
  width: 62%;
  background: linear-gradient(140deg, var(--warm-beige), #EAD5BA);
  border: 2px solid rgba(255,255,255,0.5);
  box-shadow: var(--card-shadow);
}
.py-l1 {
  width: 80%;
  background: linear-gradient(140deg, var(--accent-warm), #C2683A);
  border: 3px solid rgba(255,255,255,0.4);
  box-shadow: var(--card-shadow-lg);
}
.py-tag { font-size: 10px; letter-spacing: 5px; opacity: 0.75; font-weight: 700; display: block; margin-bottom: 2mm; }
.py-name { font-family: "Noto Serif SC", serif; font-size: 22px; font-weight: 900; letter-spacing: 3px; display: block; margin-bottom: 2mm; }
.py-desc { font-size: 12px; opacity: 0.75; }
.py-l1 .py-tag, .py-l1 .py-desc { color: rgba(255,255,255,0.85); }
.py-l1 .py-name { color: #fff; }
.py-l2 .py-tag, .py-l2 .py-desc { color: rgba(90,60,30,0.55); }
.py-l2 .py-name { color: var(--text); }

/* Overview image */
.overview-img {
  position: relative; z-index: 1;
  margin-bottom: 6mm;
  text-align: center;
}
.overview-img img {
  width: 50%;
  max-width: 260px;
  border-radius: 10px;
  box-shadow: var(--card-shadow);
  border: 2px solid rgba(0,0,0,0.03);
}

/* Product tier */
.product-tier { position: relative; z-index: 1; margin-bottom: 6mm; }
.product-tier:last-child { margin-bottom: 0; }

.series-badge {
  display: inline-block;
  background: var(--accent-warm);
  color: #fff;
  font-size: 10px; font-weight: 700;
  letter-spacing: 3px;
  padding: 2mm 5mm;
  border-radius: 14px;
  margin-bottom: 3mm;
}
.sb-2 { background: var(--accent-deep); }

.tier-title {
  font-family: "Noto Serif SC", serif;
  font-size: 18px; font-weight: 900;
  letter-spacing: 2px;
  color: var(--text);
  margin-bottom: 4mm;
}

.tier-cards {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 4mm;
  margin-bottom: 5mm;
}
.tier-card {
  padding: 5mm;
  border-radius: 12px;
  box-shadow: var(--card-shadow);
  border: 2px solid transparent;
}
.tc-1 { background: linear-gradient(140deg, #FFF5EE, #FFFDF9); border-color: rgba(224,123,76,0.13); }
.tc-2 { background: linear-gradient(140deg, #FFFDF8, #FFF8EF); border-color: rgba(217,185,145,0.18); }
.tc-name {
  font-family: "Noto Serif SC", serif;
  font-size: 15px; font-weight: 900;
  letter-spacing: 2px;
  color: var(--text);
  margin-bottom: 2mm;
}
.tc-pos { font-size: 11px; color: var(--text-mid); margin-bottom: 3mm; }
.tc-kw { display: flex; flex-wrap: wrap; gap: 3mm; }
.kw-tag {
  font-size: 11px;
  padding: 1.5mm 5mm;
  background: var(--white);
  border: 2px solid rgba(224,123,76,0.13);
  border-radius: 20px;
  color: var(--text-mid);
  font-weight: 500;
}

.product-imgs {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 3mm;
}
.product-imgs img {
  width: 100%;
  border-radius: 8px;
  box-shadow: var(--card-shadow);
  border: 2px solid rgba(0,0,0,0.03);
  max-height: 40mm;
  object-fit: cover;
}
.imgs-2 { grid-template-columns: 1fr; }
.imgs-2 img { max-width: 240px; max-height: 45mm; margin: 0 auto; }

.companion-tags {
  display: flex; flex-wrap: wrap; gap: 3mm; margin-bottom: 5mm;
}
.ctag {
  font-size: 13px; font-weight: 700;
  padding: 2mm 5mm;
  border-radius: 20px;
  letter-spacing: 2px;
  box-shadow: var(--card-shadow);
  border: 2px solid transparent;
}
.ct-1 { background: #FFF5EE; color: var(--accent-warm); border-color: rgba(224,123,76,0.23); }
.ct-2 { background: #F5F8FB; color: #5A8090; border-color: rgba(150,190,210,0.28); }
.ct-3 { background: #F7FAF3; color: #6A8060; border-color: rgba(165,185,140,0.28); }
.ct-4 { background: #FAF5FB; color: #7A6A8A; border-color: rgba(170,150,190,0.28); }
.ct-5 { background: #FFF7F5; color: #A07060; border-color: rgba(200,150,140,0.28); }
</style>
