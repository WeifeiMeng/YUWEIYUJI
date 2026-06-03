<template>
  <section class="strategy print-page">
    <div class="blob blob-pink"></div>
    <div class="section-header fade-in">
      <span class="sec-num">01</span>
      <span class="sec-tag">✦ 品牌战略</span>
      <h2 class="sec-title">品牌释义</h2>
      <p class="sec-desc">一座可以停靠的小岛 ✦ 毛孩子开心摇动的尾巴 ✦ 一年四季的陪伴</p>
    </div>

    <div class="name-meaning fade-in">
      <div class="name-char" v-for="(item, i) in nameChars" :key="i" :class="'char-' + (i + 1)">
        <span class="char-big">{{ item.char }}</span>
        <span class="char-desc" v-html="item.desc"></span>
      </div>
    </div>

    <div class="strategy-grid fade-in">
      <div class="strategy-card" v-for="(card, i) in strategyCards" :key="i" :class="'card-' + (i + 1)">
        <div class="card-label">{{ card.label }}</div>
        <div class="card-title" v-html="card.title"></div>
        <div class="card-body" v-if="card.body" v-html="card.body"></div>
      </div>
    </div>
  </section>
</template>

<script setup>
const nameChars = [
  { char: '屿', desc: '一座可以停靠的小岛<br>毛孩子的安心港湾' },
  { char: '尾', desc: '毛孩子开心摇动的尾巴<br>快乐与满足的表达' },
  { char: '季', desc: '一年四季<br>陪伴成长的时间刻度' },
]

const strategyCards = [
  { label: '品牌定位', title: '宠物成长<br>生活方式品牌', body: '区别于传统宠物食品品牌——屿尾与季卖的不是产品，而是成长、陪伴与日常生活。' },
  { label: '品牌使命', title: '让毛孩子<br>吃得健康<br>也吃得开心', body: '' },
  { label: '品牌愿景', title: '成为中国最具温度的<br>宠物成长生活方式品牌', body: '' },
  { label: '品牌 Slogan', title: '', body: '<strong>主</strong>：陪伴毛孩子的每一个四季<br><strong>副</strong>：伴成长朝夕 · 守健康四季<br><strong>电商</strong>：吃得开心，成长更安心' },
]
</script>

<style scoped>
.strategy {
  background: linear-gradient(180deg, #FFFBF7 0%, #FFF5EE 100%);
  padding: 6mm 14mm;
  position: relative;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.blob-pink {
  position: absolute;
  width: 140px; height: 140px;
  background: radial-gradient(circle, rgba(242,217,205,0.14) 0%, transparent 70%);
  top: -30px; right: -40px;
  border-radius: 50%;
  pointer-events: none;
}

.section-header { position: relative; z-index: 1; margin-bottom: 4mm; }
.sec-num {
  font-family: "Noto Serif SC", serif;
  font-size: 48px; font-weight: 900;
  color: rgba(224,123,76,0.05);
  position: absolute; top: -12px; right: 0;
  line-height: 1;
}
.sec-tag { font-size: 9px; letter-spacing: 5px; color: var(--accent-warm); font-weight: 700; display: block; margin-bottom: 2mm; }
.sec-title { font-family: "Noto Serif SC", serif; font-size: 26px; font-weight: 900; letter-spacing: 3px; color: var(--text); margin-bottom: 1mm; line-height: 1.2; }
.sec-desc { font-size: 12px; color: var(--text-mid); letter-spacing: 1px; }

.name-meaning {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 4mm;
  margin-bottom: 4mm;
  position: relative;
  z-index: 1;
}

.name-char {
  text-align: center;
  padding: 5mm 4mm;
  border-radius: 10px;
  position: relative;
  overflow: hidden;
  background: var(--white);
  box-shadow: var(--card-shadow);
  border: 2px solid transparent;
}
.char-1 { border-color: var(--accent-warm); background: linear-gradient(180deg, #FFF5EE 0%, #FFF 100%); }
.char-2 { border-color: var(--khaki); background: linear-gradient(180deg, #FFFBF3 0%, #FFF 100%); }
.char-3 { border-color: var(--accent); background: linear-gradient(180deg, #FFF8F2 0%, #FFF 100%); }

.char-big {
  font-family: "Noto Serif SC", serif;
  font-size: 38px; font-weight: 900;
  line-height: 1;
  display: block;
  margin-bottom: 3mm;
}
.char-1 .char-big { color: var(--accent-warm); }
.char-2 .char-big { color: var(--khaki); }
.char-3 .char-big { color: var(--accent); }

.char-desc { font-size: 11px; color: var(--text-mid); line-height: 1.7; }

.strategy-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 3mm;
  position: relative;
  z-index: 1;
}

.strategy-card {
  padding: 4mm 5mm;
  border-radius: 10px;
  position: relative;
  overflow: hidden;
  box-shadow: var(--card-shadow);
  border: 2px solid transparent;
}

.card-1, .card-2, .card-3, .card-4 {
  background: linear-gradient(140deg, #FFFDF9 0%, #FFF5EB 100%);
}
.card-1 { border-color: rgba(224,123,76,0.16); }
.card-2 { border-color: rgba(217,185,145,0.20); }
.card-3 { border-color: rgba(212,145,94,0.16); }
.card-4 { border-color: rgba(217,185,145,0.20); }

.card-label { font-size: 8px; letter-spacing: 4px; color: var(--accent-warm); margin-bottom: 1.5mm; font-weight: 700; }
.card-title { font-family: "Noto Serif SC", serif; font-size: 13px; font-weight: 900; letter-spacing: 1px; color: var(--text); line-height: 1.35; margin-bottom: 1.5mm; min-height: auto; }
.card-body { font-size: 10px; color: var(--text-mid); line-height: 1.65; }

@media (max-width: 900px) {
  .name-meaning, .strategy-grid { grid-template-columns: 1fr 1fr; }
}
@media (max-width: 600px) {
  .strategy { padding: 6mm 4mm; }
  .name-meaning, .strategy-grid { grid-template-columns: 1fr; }
  .sec-title { font-size: 22px; }
}
</style>
