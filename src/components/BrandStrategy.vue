<template>
  <section class="section bg-warm">
    <div class="blob blob-pink" style="width:300px;height:300px;top:-80px;right:-100px;"></div>

    <div class="section-inner">
      <div class="fade-in" style="margin-bottom:48px;">
        <div class="section-tag">品牌战略</div>
        <h2 class="section-title">品牌释义</h2>
        <p class="section-subtitle">一座可以停靠的小岛 · 毛孩子开心摇动的尾巴 · 一年四季的陪伴</p>
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
.name-meaning {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
  margin-bottom: 36px;
}

.name-char {
  text-align: center;
  padding: 48px 28px 40px;
  border-radius: var(--card-radius);
  background: var(--white);
  box-shadow: var(--card-shadow);
  border: 2px solid transparent;
  transition: transform 0.3s, box-shadow 0.3s;
}
.name-char:hover { transform: translateY(-6px); box-shadow: var(--card-shadow-lg); }
.char-1 { border-color: var(--accent-warm); background: linear-gradient(180deg, #FFF5EE 0%, #FFF 100%); }
.char-2 { border-color: var(--khaki); background: linear-gradient(180deg, #FFFBF3 0%, #FFF 100%); }
.char-3 { border-color: var(--accent); background: linear-gradient(180deg, #FFF8F2 0%, #FFF 100%); }

.char-big {
  font-family: "Noto Serif SC", serif;
  font-size: 72px;
  font-weight: 900;
  line-height: 1;
  display: block;
  margin-bottom: 16px;
}
.char-1 .char-big { color: var(--accent-warm); }
.char-2 .char-big { color: var(--khaki); }
.char-3 .char-big { color: var(--accent); }

.char-desc { font-size: 16px; color: var(--text-mid); line-height: 2; }

.strategy-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
}

.strategy-card {
  padding: 32px 28px;
  border-radius: var(--card-radius);
  box-shadow: var(--card-shadow);
  border: 2px solid transparent;
  transition: transform 0.3s, box-shadow 0.3s;
}
.strategy-card:hover { transform: translateY(-4px); box-shadow: var(--card-shadow-lg); }
.card-1, .card-2, .card-3, .card-4 { background: linear-gradient(140deg, #FFFDF9 0%, #FFF5EB 100%); }
.card-1 { border-color: rgba(224,123,76,0.18); }
.card-2 { border-color: rgba(217,185,145,0.22); }
.card-3 { border-color: rgba(212,145,94,0.18); }
.card-4 { border-color: rgba(217,185,145,0.22); }

.card-label { font-size: 11px; letter-spacing: 6px; color: var(--accent-warm); margin-bottom: 12px; font-weight: 700; }
.card-title { font-family: "Noto Serif SC", serif; font-size: 24px; font-weight: 900; letter-spacing: 2px; color: var(--text); line-height: 1.4; margin-bottom: 8px; }
.card-body { font-size: 15px; color: var(--text-mid); line-height: 1.9; }

@media (max-width: 900px) {
  .name-meaning { grid-template-columns: repeat(3, 1fr); gap: 16px; }
  .strategy-grid { grid-template-columns: 1fr 1fr; }
  .char-big { font-size: 48px; }
}
@media (max-width: 640px) {
  .name-meaning { grid-template-columns: 1fr; }
  .strategy-grid { grid-template-columns: 1fr; }
}
</style>
