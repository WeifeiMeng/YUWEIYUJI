<template>
  <section class="persona">
    <div class="blob blob-warm"></div>
    <div class="section-header fade-in">
      <span class="sec-num">04</span>
      <span class="sec-tag">✦ 品牌人格</span>
      <h2 class="sec-title">如果屿尾与季是一个人</h2>
    </div>

    <div class="persona-grid fade-in">
      <div class="persona-quote">
        <span class="quote-mark">"</span>
        <p>她<strong>不是专家</strong>，不是医生，不是营养学教授。</p>
        <p>而是一位<strong>认真生活的养宠人</strong>。</p>
        <p>她会记录猫咪成长，收藏日常瞬间，认真挑选食材，享受陪伴过程。</p>
      </div>
      <div>
        <p class="keywords-label">品牌人格关键词</p>
        <div class="persona-words">
          <span class="persona-word" v-for="(w, i) in words" :key="i" :class="'pw-' + (i + 1)">{{ w }}</span>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const words = ['温暖', '真诚', '治愈', '自然', '有生活感']
</script>

<style scoped>
.persona {
  padding: 7mm 12mm;
  position: relative;
  overflow: hidden;
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.blob-warm {
  position: absolute;
  width: 160px; height: 160px;
  background: radial-gradient(circle, rgba(224,123,76,0.08) 0%, transparent 70%);
  top: -30px; right: -30px;
  border-radius: 50%;
  pointer-events: none;
}

.section-header { position: relative; z-index: 1; margin-bottom: 6mm; }
.sec-num {
  font-family: "Noto Serif SC", serif;
  font-size: 50px; font-weight: 900;
  color: rgba(224,123,76,0.06);
  position: absolute; top: -14px; right: 0;
  line-height: 1;
}
.sec-tag { font-size: 11px; letter-spacing: 6px; color: var(--accent-warm); font-weight: 700; display: block; margin-bottom: 3mm; }
.sec-title { font-family: "Noto Serif SC", serif; font-size: 28px; font-weight: 900; letter-spacing: 3px; color: var(--text); line-height: 1.2; }

.persona-grid {
  display: grid;
  grid-template-columns: 1.1fr 0.9fr;
  gap: 6mm;
  align-items: start;
  position: relative;
  z-index: 1;
}

.persona-quote {
  background: linear-gradient(145deg, #FFF5EE 0%, #FFFDF9 100%);
  padding: 6mm;
  font-size: 14px;
  color: var(--text-mid);
  line-height: 2.2;
  border-radius: 12px;
  border-left: 4px solid var(--accent-warm);
  box-shadow: var(--card-shadow);
  position: relative;
}
.persona-quote p { margin-bottom: 2mm; }
.persona-quote strong { color: var(--text); font-weight: 700; }

.quote-mark {
  position: absolute;
  top: 2mm; right: 4mm;
  font-family: "Noto Serif SC", serif;
  font-size: 48px;
  color: rgba(224,123,76,0.07);
  line-height: 1;
  pointer-events: none;
}

.keywords-label {
  font-size: 13px; color: var(--text-mid);
  margin-bottom: 4mm; letter-spacing: 2px;
}

.persona-words {
  display: flex;
  flex-wrap: wrap;
  gap: 3mm;
}

.persona-word {
  font-family: "Noto Serif SC", serif;
  padding: 3mm 6mm;
  font-size: 17px;
  letter-spacing: 3px;
  border-radius: 30px;
  font-weight: 700;
  box-shadow: var(--card-shadow);
  transition: transform 0.3s;
}
.persona-word:hover { transform: scale(1.05); }

.pw-1 { background: #FFF5EE; color: var(--accent-warm); border: 2px solid rgba(224,123,76,0.25); }
.pw-2 { background: #FFFDF8; color: var(--accent-deep); border: 2px solid rgba(194,104,58,0.20); }
.pw-3 { background: #FDFAF5; color: #B89360; border: 2px solid rgba(217,185,145,0.30); }
.pw-4 { background: #F7FAF3; color: #7A8E6A; border: 2px solid rgba(165,185,140,0.30); }
.pw-5 { background: #FFFBF5; color: var(--text-mid); border: 2px solid rgba(180,160,140,0.25); }

@media (max-width: 768px) {
  .persona-grid { grid-template-columns: 1fr; }
}
</style>
