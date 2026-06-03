<template>
  <section class="visual print-page">
    <div class="blob blob-pink"></div>
    <div class="blob blob-green2"></div>
    <div class="section-header fade-in">
      <span class="sec-num">06</span>
      <span class="sec-tag">✦ 品牌视觉体系</span>
      <h2 class="sec-title">品牌色彩</h2>
      <p class="sec-desc">自然 · 留白 · 温暖 · 治愈 · 真实 · 生活方式</p>
    </div>

    <div class="fade-in">
      <h3 class="sub-head">品牌主色</h3>
      <div class="color-palette">
        <div class="color-swatch" v-for="c in mainColors" :key="c.hex" :style="{ background: c.hex }">
          <div>
            <div class="swatch-label">{{ c.name }}</div>
            <div class="swatch-hex">{{ c.hex }} · {{ c.role }}</div>
          </div>
        </div>
      </div>
      <div class="accent-dot">
        <span class="accent-circle"></span>
        强调色 #E07B4C
      </div>
    </div>

    <div class="fade-in" style="margin-top:6mm;">
      <h3 class="sub-head">系列辅助色</h3>
      <div class="series-grid">
        <div class="series-color" v-for="s in seriesColors" :key="s.name" :style="{ background: s.hex }">
          {{ s.name }} · {{ s.label }}
        </div>
      </div>
    </div>

    <div class="fade-in" style="margin-top:6mm;">
      <h3 class="sub-head">摄影风格</h3>
      <div class="photo-tags">
        <span class="photo-tag" v-for="(t, i) in photoStyles" :key="t" :class="'pt-' + (i + 1)">{{ t }}</span>
      </div>
    </div>

    <div class="fade-in" style="margin-top:6mm;">
      <h3 class="sub-head">参考品牌</h3>
      <div class="ref-brands">
        <span class="ref-brand" v-for="r in refBrands" :key="r">{{ r }}</span>
      </div>
    </div>

    <div class="trademark fade-in">
      <img src="/商标.jpg" alt="注册商标" />
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
.visual {
  background: linear-gradient(180deg, #FFFBF7 0%, #FFF5EE 100%);
  padding: 10mm 14mm;
  position: relative;
  overflow: hidden;
}

.blob-pink {
  position: absolute;
  width: 160px; height: 160px;
  background: radial-gradient(circle, rgba(242,217,205,0.16) 0%, transparent 70%);
  top: -40px; right: -50px;
  border-radius: 50%;
  pointer-events: none;
}
.blob-green2 {
  position: absolute;
  width: 120px; height: 120px;
  background: radial-gradient(circle, rgba(213,226,205,0.14) 0%, transparent 70%);
  bottom: -20px; left: -30px;
  border-radius: 50%;
  pointer-events: none;
}

.section-header { position: relative; z-index: 1; margin-bottom: 6mm; }
.sec-num {
  font-family: "Noto Serif SC", serif;
  font-size: 56px; font-weight: 900;
  color: rgba(224,123,76,0.06);
  position: absolute; top: -16px; right: 0;
  line-height: 1;
}
.sec-tag { font-size: 10px; letter-spacing: 5px; color: var(--accent-warm); font-weight: 700; display: block; margin-bottom: 4mm; }
.sec-title { font-family: "Noto Serif SC", serif; font-size: 30px; font-weight: 900; letter-spacing: 3px; color: var(--text); line-height: 1.2; }
.sec-desc { font-size: 13px; color: var(--text-mid); letter-spacing: 2px; margin-top: 2mm; }

.sub-head {
  font-family: "Noto Serif SC", serif;
  font-size: 16px; font-weight: 900;
  letter-spacing: 2px;
  margin-bottom: 3mm;
  color: var(--text);
  position: relative; z-index: 1;
}

.color-palette {
  display: flex;
  gap: 5mm;
  position: relative; z-index: 1;
}
.color-swatch {
  flex: 1;
  height: 44mm;
  border-radius: 12px;
  display: flex;
  align-items: flex-end;
  padding: 5mm;
  box-shadow: var(--card-shadow-lg);
  border: 2px solid rgba(0,0,0,0.03);
}
.swatch-label { font-size: 12px; font-weight: 700; color: var(--text); background: rgba(255,255,255,0.78); padding: 1mm 5mm; border-radius: 4px; display: inline-block; }
.swatch-hex { font-size: 9px; color: var(--text-mid); margin-top: 1mm; }

.accent-dot {
  text-align: center; margin-top: 3mm;
  font-size: 11px; color: var(--text-mid); font-weight: 700;
  position: relative; z-index: 1;
}
.accent-circle {
  display: inline-block;
  width: 16px; height: 16px;
  border-radius: 50%;
  background: var(--accent-warm);
  vertical-align: middle;
  margin-right: 4px;
}

.series-grid {
  display: flex;
  gap: 4mm;
  position: relative; z-index: 1;
}
.series-color {
  flex: 1;
  height: 28mm;
  border-radius: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 11px; letter-spacing: 1px;
  color: #fff; font-weight: 700;
  box-shadow: var(--card-shadow);
  border: 3px solid rgba(255,255,255,0.4);
}

.photo-tags {
  display: flex; gap: 3mm; flex-wrap: wrap;
  position: relative; z-index: 1;
}
.photo-tag {
  padding: 2mm 5mm;
  border-radius: 20px;
  font-size: 12px; font-weight: 700;
  background: #FFFDF9;
  border: 2px solid rgba(217,185,145,0.18);
  color: var(--text-mid);
}
.pt-1 { border-color: rgba(224,123,76,0.18); background: #FFFBF7; }
.pt-2 { border-color: rgba(150,185,130,0.18); background: #FAFCF9; }
.pt-3 { border-color: rgba(217,185,145,0.18); background: #FFFDF8; }

.ref-brands {
  display: flex; gap: 4mm; flex-wrap: wrap;
  position: relative; z-index: 1;
}
.ref-brand {
  font-family: "Noto Serif SC", serif;
  font-size: 15px; color: var(--text-mid);
  letter-spacing: 2px;
  padding: 2mm 6mm;
  border: 2px solid rgba(217,185,145,0.18);
  border-radius: 20px;
  font-weight: 700;
  background: #FFFDF9;
}

.trademark {
  display: flex;
  justify-content: center;
  margin-top: 8mm;
  position: relative; z-index: 1;
}
.trademark img { height: 30mm; opacity: 0.75; }
</style>
