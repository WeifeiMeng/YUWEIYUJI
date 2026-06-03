<template>
  <section class="language">
    <div class="blob blob-warm"></div>
    <div class="section-header fade-in">
      <span class="sec-num">09</span>
      <span class="sec-tag">✦ 品牌语言体系</span>
      <h2 class="sec-title">品牌说话方式</h2>
    </div>

    <div class="lang-compare fade-in">
      <div class="lang-box avoid">
        <div class="lang-box-label">✕ 避免</div>
        <ul>
          <li>功效导向</li>
          <li>夸张宣传</li>
          <li>医疗化表达</li>
        </ul>
      </div>
      <div class="lang-box use">
        <div class="lang-box-label">✓ 采用</div>
        <ul>
          <li>陪伴式表达</li>
          <li>场景式表达</li>
          <li>情绪式表达</li>
        </ul>
      </div>
    </div>

    <div class="fade-in transform-section">
      <h3 class="sub-head">表达示例</h3>
      <div class="transform-list">
        <div class="transform-item" v-for="(item, i) in examples" :key="i">
          <span class="ti-before">{{ item.before }}</span>
          <span class="ti-arrow">→</span>
          <span class="ti-after">{{ item.after }}</span>
        </div>
      </div>
    </div>

    <div class="fade-in naming-section">
      <h3 class="sub-head">产品命名体系</h3>
      <p class="naming-principle">原则：<strong>食材 × 情绪 × 场景</strong></p>
      <div class="naming-tags">
        <span class="n-tag" v-for="n in namings" :key="n.name" :class="{ future: n.future }">{{ n.name }}</span>
      </div>
    </div>
  </section>
</template>

<script setup>
const examples = [
  { before: '高适口性', after: '今天也吃得很开心' },
  { before: '功能零食', after: '属于它的小奖励' },
  { before: '营养补充', after: '成长路上的小能量' },
]

const namings = [
  { name: '莓莓鸡', future: false },
  { name: '虾虾圆子', future: false },
  { name: '奶豆腐', future: false },
  { name: '南瓜小派', future: true },
  { name: '椰椰鱼球', future: true },
  { name: '莓果鸭鸭', future: true },
  { name: '牛乳松松', future: true },
]
</script>

<style scoped>
.language {
  padding: 6mm 12mm;
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
  background: radial-gradient(circle, rgba(224,123,76,0.07) 0%, transparent 70%);
  top: -30px; right: -40px;
  border-radius: 50%;
  pointer-events: none;
}

.section-header { position: relative; z-index: 1; margin-bottom: 4mm; }
.sec-num {
  font-family: "Noto Serif SC", serif;
  font-size: 50px; font-weight: 900;
  color: rgba(217,185,145,0.07);
  position: absolute; top: -14px; right: 0;
  line-height: 1;
}
.sec-tag { font-size: 10px; letter-spacing: 6px; color: var(--accent-warm); font-weight: 700; display: block; margin-bottom: 2mm; }
.sec-title { font-family: "Noto Serif SC", serif; font-size: 24px; font-weight: 900; letter-spacing: 3px; color: var(--text); line-height: 1.2; }

/* Compare */
.lang-compare {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 3mm;
  position: relative; z-index: 1;
}
.lang-box {
  padding: 4mm;
  border-radius: 10px;
}
.lang-box.avoid { background: #F9F6F2; border: 2px solid #E8E2D8; }
.lang-box.use {
  background: linear-gradient(145deg, #FFF5EE 0%, #FFFDF9 100%);
  border: 2px solid rgba(224,123,76,0.18);
  box-shadow: var(--card-shadow);
}
.lang-box-label {
  font-family: "Noto Serif SC", serif;
  font-size: 15px; font-weight: 700;
  letter-spacing: 3px;
  margin-bottom: 3mm;
}
.avoid .lang-box-label { color: #B5ACA0; }
.use .lang-box-label { color: var(--accent-warm); }
.lang-box ul { list-style: none; }
.lang-box ul li { font-size: 13px; line-height: 2.2; }
.avoid ul li { color: #B5ACA0; }
.use ul li { color: var(--text); }

/* Transform */
.transform-section { margin-top: 4mm; position: relative; z-index: 1; }
.sub-head {
  font-family: "Noto Serif SC", serif;
  font-size: 16px; font-weight: 900;
  letter-spacing: 2px;
  color: var(--text);
  margin-bottom: 2mm;
}

.transform-list {
  display: flex;
  gap: 2mm;
  position: relative; z-index: 1;
}
.transform-item {
  flex: 1;
  display: flex;
  align-items: center;
  gap: 2mm;
  padding: 3mm 4mm;
  border-radius: 10px;
  background: #FFFDF9;
  border: 2px solid rgba(217,185,145,0.10);
  box-shadow: var(--card-shadow);
}
.ti-before {
  font-size: 13px; color: #B5ACA0;
  text-decoration: line-through;
  white-space: nowrap;
}
.ti-arrow {
  color: var(--accent-warm);
  font-family: "Noto Serif SC", serif;
  font-size: 16px;
  font-weight: 700;
  flex-shrink: 0;
}
.ti-after {
  font-family: "Noto Serif SC", serif;
  font-size: 13px; color: var(--text); font-weight: 700;
  background: linear-gradient(180deg, transparent 55%, rgba(224,123,76,0.12) 55%);
  padding: 0 2px;
  white-space: nowrap;
}

/* Naming */
.naming-section { margin-top: 4mm; position: relative; z-index: 1; }
.naming-principle {
  font-family: "Noto Serif SC", serif;
  font-size: 15px; color: var(--text);
  margin-bottom: 3mm;
  letter-spacing: 2px;
  font-weight: 700;
}
.naming-principle strong { color: var(--accent-warm); font-weight: 900; }

.naming-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 2mm;
}
.n-tag {
  display: inline-block;
  padding: 2mm 5mm;
  border-radius: 20px;
  font-size: 13px;
  letter-spacing: 2px;
  font-weight: 700;
  box-shadow: var(--card-shadow);
  border: 2px solid rgba(224,123,76,0.18);
  background: #FFFDF8;
  color: var(--text);
}
.n-tag.future {
  color: var(--text-light);
  border-color: rgba(200,180,160,0.12);
  font-weight: 400;
  background: #FAFAF7;
  box-shadow: none;
}

@media (max-width: 768px) {
  .lang-compare { grid-template-columns: 1fr; }
  .transform-list { flex-direction: column; }
}
</style>
