<template>
  <!-- Product Pyramid -->
  <section class="section bg-neutral">
    <div class="blob blob-gold" style="width:320px;height:320px;top:-80px;right:-80px;"></div>
    <div class="section-inner">
      <div class="fade-in" style="margin-bottom:48px;text-align:center;">
        <div class="section-tag">产品战略</div>
        <h2 class="section-title">品牌产品金字塔</h2>
        <p class="section-subtitle" style="margin:0 auto;">每一层对应毛孩子成长的不同需求</p>
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
    </div>
  </section>

  <!-- Product Matrix -->
  <section class="section bg-warm">
    <div class="blob blob-pink" style="width:260px;height:260px;bottom:-60px;left:-60px;"></div>
    <div class="section-inner">
      <div class="fade-in" style="margin-bottom:40px;">
        <div class="section-tag">产品矩阵</div>
      </div>

      <!-- Overview image -->
      <div class="overview-img fade-in">
        <img src="/产品总图.jpg" alt="产品总览" />
      </div>

      <!-- Growth Series -->
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

      <!-- Companion Series -->
      <div class="product-tier fade-in" style="margin-top:48px;">
        <span class="series-badge sb-2">陪伴系列</span>
        <h3 class="tier-title">彩虹吊卡冻干 — 互动奖励</h3>
        <div class="companion-tags">
          <span class="ctag" v-for="(c, i) in companionProducts" :key="c" :class="'ct-' + (i + 1)">{{ c }}</span>
        </div>
        <div class="product-imgs imgs-2">
          <img src="/零食冻干.jpg" alt="彩虹吊卡冻干" />
          <img src="/产品总图.jpg" alt="产品总览" />
        </div>
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
/* Pyramid */
.pyramid {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 12px;
  max-width: 600px;
  margin: 0 auto;
}
.py-level {
  text-align: center;
  border-radius: var(--card-radius);
  padding: 28px 48px;
}
.py-l3 {
  width: 52%;
  background: #FFFDF9;
  border: 2px solid rgba(217,185,145,0.22);
  box-shadow: var(--card-shadow);
}
.py-l2 {
  width: 68%;
  background: linear-gradient(140deg, var(--warm-beige), #EAD5BA);
  border: 2px solid rgba(255,255,255,0.5);
  box-shadow: var(--card-shadow);
}
.py-l1 {
  width: 86%;
  background: linear-gradient(140deg, var(--accent-warm), #C2683A);
  border: 3px solid rgba(255,255,255,0.4);
  box-shadow: var(--card-shadow-lg);
}
.py-tag { font-size: 12px; letter-spacing: 6px; opacity: 0.75; font-weight: 700; display: block; margin-bottom: 6px; }
.py-name { font-family: "Noto Serif SC", serif; font-size: 28px; font-weight: 900; letter-spacing: 4px; display: block; margin-bottom: 6px; }
.py-desc { font-size: 15px; opacity: 0.75; }
.py-l1 .py-tag, .py-l1 .py-desc { color: rgba(255,255,255,0.85); }
.py-l1 .py-name { color: #fff; }
.py-l2 .py-tag, .py-l2 .py-desc { color: rgba(90,60,30,0.55); }
.py-l2 .py-name { color: var(--text); }

/* Overview */
.overview-img {
  text-align: center;
  margin-bottom: 40px;
}
.overview-img img {
  width: 50%;
  max-width: 360px;
  border-radius: var(--card-radius);
  box-shadow: var(--card-shadow-lg);
  border: 2px solid rgba(0,0,0,0.03);
}

/* Product Tiers */
.product-tier { margin-bottom: 0; }

.series-badge {
  display: inline-block;
  background: var(--accent-warm);
  color: #fff;
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 4px;
  padding: 6px 18px;
  border-radius: 20px;
  margin-bottom: 12px;
}
.sb-2 { background: var(--accent-deep); }

.tier-title {
  font-family: "Noto Serif SC", serif;
  font-size: 24px;
  font-weight: 900;
  letter-spacing: 3px;
  color: var(--text);
  margin-bottom: 20px;
}

.tier-cards {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
  margin-bottom: 24px;
}
.tier-card {
  padding: 24px 22px;
  border-radius: var(--card-radius);
  box-shadow: var(--card-shadow);
  border: 2px solid transparent;
}
.tc-1 { background: linear-gradient(140deg, #FFF5EE, #FFFDF9); border-color: rgba(224,123,76,0.14); }
.tc-2 { background: linear-gradient(140deg, #FFFDF8, #FFF8EF); border-color: rgba(217,185,145,0.18); }
.tc-name {
  font-family: "Noto Serif SC", serif;
  font-size: 20px;
  font-weight: 900;
  letter-spacing: 2px;
  color: var(--text);
  margin-bottom: 6px;
}
.tc-pos { font-size: 14px; color: var(--text-mid); margin-bottom: 12px; }
.tc-kw { display: flex; flex-wrap: wrap; gap: 8px; }
.kw-tag {
  font-size: 13px;
  padding: 5px 16px;
  background: var(--white);
  border: 2px solid rgba(224,123,76,0.14);
  border-radius: 30px;
  color: var(--text-mid);
  font-weight: 500;
}

.product-imgs {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 16px;
}
.product-imgs img {
  width: 100%;
  border-radius: 12px;
  box-shadow: var(--card-shadow-lg);
  border: 2px solid rgba(0,0,0,0.03);
}
.imgs-2 { grid-template-columns: repeat(2, 1fr); }

.companion-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
  margin-bottom: 24px;
}
.ctag {
  font-size: 16px;
  font-weight: 700;
  padding: 10px 22px;
  border-radius: 30px;
  letter-spacing: 2px;
  box-shadow: var(--card-shadow);
  border: 2px solid transparent;
}
.ct-1 { background: #FFF5EE; color: var(--accent-warm); border-color: rgba(224,123,76,0.25); }
.ct-2 { background: #F5F8FB; color: #5A8090; border-color: rgba(150,190,210,0.30); }
.ct-3 { background: #F7FAF3; color: #6A8060; border-color: rgba(165,185,140,0.30); }
.ct-4 { background: #FAF5FB; color: #7A6A8A; border-color: rgba(170,150,190,0.30); }
.ct-5 { background: #FFF7F5; color: #A07060; border-color: rgba(200,150,140,0.30); }

@media (max-width: 768px) {
  .tier-cards { grid-template-columns: 1fr; }
  .product-imgs { grid-template-columns: 1fr 1fr; }
  .pyramid { max-width: 100%; }
  .py-level { padding: 20px 24px; }
}
</style>
