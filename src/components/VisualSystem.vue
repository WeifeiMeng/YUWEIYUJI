<template>
  <section class="section bg-warm">
    <div class="blob blob-pink" style="width:280px;height:280px;top:-60px;right:-80px;"></div>

    <div class="section-inner">
      <div class="fade-in" style="margin-bottom:48px;">
        <div class="section-tag">品牌视觉体系</div>
        <h2 class="section-title">品牌色彩</h2>
        <p class="section-subtitle">自然 · 留白 · 温暖 · 治愈 · 真实 · 生活方式</p>
      </div>

      <!-- Main colors -->
      <div class="fade-in" style="margin-bottom:40px;">
        <h3 class="sub-head">品牌主色</h3>
        <div class="color-palette">
          <div class="color-swatch" v-for="c in mainColors" :key="c.hex" :style="{ background: c.hex }">
            <div class="swatch-info">
              <div class="swatch-label">{{ c.name }}</div>
              <div class="swatch-hex">{{ c.hex }} · {{ c.role }}</div>
            </div>
          </div>
        </div>
        <div class="accent-dot">
          <span class="accent-circle"></span> 强调色 #E07B4C
        </div>
      </div>

      <!-- Series colors -->
      <div class="fade-in" style="margin-bottom:40px;">
        <h3 class="sub-head">系列辅助色</h3>
        <div class="series-grid">
          <div class="series-color" v-for="s in seriesColors" :key="s.name" :style="{ background: s.hex }">
            {{ s.name }} · {{ s.label }}
          </div>
        </div>
      </div>

      <!-- Photo style -->
      <div class="fade-in" style="margin-bottom:40px;">
        <h3 class="sub-head">摄影风格</h3>
        <div class="photo-tags">
          <span class="photo-tag" v-for="(t, i) in photoStyles" :key="t" :class="'pt-' + (i + 1)">{{ t }}</span>
        </div>
      </div>

      <!-- Ref brands -->
      <div class="fade-in" style="margin-bottom:40px;">
        <h3 class="sub-head">参考品牌</h3>
        <div class="ref-brands">
          <span class="ref-brand" v-for="r in refBrands" :key="r">{{ r }}</span>
        </div>
      </div>

      <!-- Trademark -->
      <div class="trademark fade-in">
        <img src="/商标.jpg" alt="注册商标" />
      </div>
    </div>
  </section>
</template>

<script setup>
const mainColors = [
  { name: '奶油白', hex: '#FEFAF4', role: '品牌底色' },
  { name: '米杏色', hex: '#F4E5D1', role: '辅助背景' },
  { name: '浅卡其', hex: '#D9B991', role: '点缀色' },
]
const seriesColors = [
  { name: '莓莓鸡', hex: '#F2D9CD', label: '奶油粉' },
  { name: '虾虾圆子', hex: '#D2DFE8', label: '海盐蓝' },
  { name: '排毛小饼', hex: '#D5E2CD', label: '鼠尾草绿' },
  { name: '蓝莓奶豆腐', hex: '#DFD7E8', label: '雾霾紫' },
  { name: '爱心兔血', hex: '#E8D4D4', label: '豆沙红' },
]
const photoStyles = ['自然光', '真实食材', '生活化场景', '大量留白', '弱商业感', '强生活感']
const refBrands = ['共我生活', '尾巴生活', 'MUJI', '观夏']
</script>

<style scoped>
.sub-head {
  font-family: "Noto Serif SC", serif;
  font-size: 20px;
  font-weight: 900;
  letter-spacing: 3px;
  margin-bottom: 16px;
  color: var(--text);
}

.color-palette {
  display: flex;
  gap: 20px;
}
.color-swatch {
  flex: 1;
  height: 120px;
  border-radius: var(--card-radius);
  display: flex;
  align-items: flex-end;
  padding: 16px;
  box-shadow: var(--card-shadow-lg);
  border: 2px solid rgba(0,0,0,0.03);
}
.swatch-info { width: 100%; }
.swatch-label { font-size: 14px; font-weight: 700; color: var(--text); background: rgba(255,255,255,0.78); padding: 3px 12px; border-radius: 6px; display: inline-block; }
.swatch-hex { font-size: 11px; color: var(--text-mid); margin-top: 4px; }

.accent-dot {
  text-align: center;
  margin-top: 16px;
  font-size: 14px;
  color: var(--text-mid);
  font-weight: 700;
}
.accent-circle {
  display: inline-block;
  width: 22px; height: 22px;
  border-radius: 50%;
  background: var(--accent-warm);
  vertical-align: middle;
  margin-right: 6px;
}

.series-grid {
  display: flex;
  gap: 14px;
}
.series-color {
  flex: 1;
  height: 60px;
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 14px;
  letter-spacing: 2px;
  color: #fff;
  font-weight: 700;
  box-shadow: var(--card-shadow);
  border: 3px solid rgba(255,255,255,0.4);
  text-align: center;
  line-height: 1.4;
}

.photo-tags {
  display: flex;
  gap: 12px;
  flex-wrap: wrap;
}
.photo-tag {
  padding: 10px 22px;
  border-radius: 30px;
  font-size: 15px;
  font-weight: 700;
  background: #FFFDF9;
  border: 2px solid rgba(217,185,145,0.18);
  color: var(--text-mid);
}
.pt-1 { border-color: rgba(224,123,76,0.20); background: #FFFBF7; }
.pt-2 { border-color: rgba(150,185,130,0.20); background: #FAFCF9; }
.pt-3 { border-color: rgba(217,185,145,0.20); background: #FFFDF8; }

.ref-brands {
  display: flex;
  gap: 16px;
  flex-wrap: wrap;
}
.ref-brand {
  font-family: "Noto Serif SC", serif;
  font-size: 18px;
  color: var(--text-mid);
  letter-spacing: 3px;
  padding: 10px 24px;
  border: 2px solid rgba(217,185,145,0.20);
  border-radius: 30px;
  font-weight: 700;
  background: #FFFDF9;
}

.trademark {
  display: flex;
  justify-content: center;
  margin-top: 48px;
}
.trademark img { height: 60px; opacity: 0.75; }

@media (max-width: 640px) {
  .color-palette { flex-direction: column; }
  .color-swatch { height: 80px; }
  .series-grid { flex-wrap: wrap; }
  .series-color { flex: none; width: calc(33% - 10px); height: 48px; font-size: 12px; }
}
</style>
