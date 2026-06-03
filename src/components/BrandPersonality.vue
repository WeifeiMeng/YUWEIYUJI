<template>
  <section class="section bg-warm">
    <div class="blob blob-warm" style="width:340px;height:340px;top:-80px;right:-80px;"></div>

    <div class="section-inner">
      <div class="fade-in" style="margin-bottom:48px;">
        <div class="section-tag">品牌人格</div>
        <h2 class="section-title">如果屿尾与季是一个人</h2>
      </div>

      <div class="persona-grid fade-in">
        <div class="persona-quote">
          <span class="quote-mark">"</span>
          <p>她<strong>不是专家</strong>，不是医生，不是营养学教授。</p>
          <p>而是一位<strong>认真生活的养宠人</strong>。</p>
          <p>她会记录猫咪成长，收藏日常瞬间，认真挑选食材，享受陪伴过程。</p>
        </div>
        <div class="persona-right">
          <p class="keywords-label">品牌人格关键词</p>
          <div class="persona-words">
            <span class="persona-word" v-for="(w, i) in words" :key="i" :class="'pw-' + (i + 1)">{{ w }}</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const words = ['温暖', '真诚', '治愈', '自然', '有生活感']
</script>

<style scoped>
.persona-grid {
  display: grid;
  grid-template-columns: 1.1fr 0.9fr;
  gap: 56px;
  align-items: start;
}

.persona-quote {
  background: linear-gradient(145deg, #FFF5EE 0%, #FFFDF9 100%);
  padding: 44px 36px;
  font-size: 18px;
  color: var(--text-mid);
  line-height: 2.5;
  border-radius: var(--card-radius);
  border-left: 6px solid var(--accent-warm);
  box-shadow: var(--card-shadow);
  position: relative;
}
.persona-quote p { margin-bottom: 10px; }
.persona-quote p:last-child { margin-bottom: 0; }
.persona-quote strong { color: var(--text); font-weight: 700; }

.quote-mark {
  position: absolute;
  top: 12px; right: 24px;
  font-family: "Noto Serif SC", serif;
  font-size: 90px;
  color: rgba(224,123,76,0.08);
  line-height: 1;
  pointer-events: none;
}

.persona-right { padding-top: 8px; }

.keywords-label {
  font-size: 17px;
  color: var(--text-mid);
  margin-bottom: 20px;
  letter-spacing: 2px;
}

.persona-words {
  display: flex;
  flex-wrap: wrap;
  gap: 14px;
}

.persona-word {
  font-family: "Noto Serif SC", serif;
  padding: 14px 28px;
  font-size: 24px;
  letter-spacing: 4px;
  border-radius: 40px;
  font-weight: 700;
  box-shadow: var(--card-shadow);
  transition: transform 0.3s;
}
.persona-word:hover { transform: scale(1.06); }

.pw-1 { background: #FFF5EE; color: var(--accent-warm); border: 2px solid rgba(224,123,76,0.25); }
.pw-2 { background: #FFFDF8; color: var(--accent-deep); border: 2px solid rgba(194,104,58,0.20); }
.pw-3 { background: #FDFAF5; color: #B89360; border: 2px solid rgba(217,185,145,0.30); }
.pw-4 { background: #F7FAF3; color: #7A8E6A; border: 2px solid rgba(165,185,140,0.30); }
.pw-5 { background: #FFFBF5; color: var(--text-mid); border: 2px solid rgba(180,160,140,0.25); }

@media (max-width: 768px) {
  .persona-grid { grid-template-columns: 1fr; }
  .persona-quote { font-size: 16px; padding: 32px 24px; }
}
</style>
