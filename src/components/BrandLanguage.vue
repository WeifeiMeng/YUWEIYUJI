<template>
  <section class="section bg-neutral">
    <div class="blob blob-warm" style="width:340px;height:340px;top:-80px;right:-100px;"></div>

    <div class="section-inner">
      <div class="fade-in" style="margin-bottom:48px;">
        <div class="section-tag">品牌语言体系</div>
        <h2 class="section-title">品牌说话方式</h2>
      </div>

      <!-- Side-by-side -->
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

      <!-- Transform examples -->
      <div class="fade-in" style="margin-top:48px;">
        <h3 class="sub-head">表达示例</h3>
        <p class="sub-desc">从功效语言到陪伴语言的转变</p>
        <div class="transform-list">
          <div class="transform-item" v-for="(item, i) in examples" :key="i">
            <span class="ti-before">{{ item.before }}</span>
            <span class="ti-arrow">→</span>
            <span class="ti-after">{{ item.after }}</span>
          </div>
        </div>
      </div>

      <!-- Naming -->
      <div class="fade-in" style="margin-top:48px;">
        <h3 class="sub-head">产品命名体系</h3>
        <p class="naming-principle">原则：<strong>食材 × 情绪 × 场景</strong></p>
        <div class="naming-tags">
          <span class="n-tag" v-for="n in namings" :key="n.name" :class="{ future: n.future }">{{ n.name }}</span>
        </div>
        <p class="naming-note">浅色标签为未来新品规划</p>
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
.lang-compare {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 24px;
}
.lang-box {
  padding: 36px 32px;
  border-radius: var(--card-radius);
}
.lang-box.avoid { background: #F9F6F2; border: 2px solid #E8E2D8; }
.lang-box.use {
  background: linear-gradient(145deg, #FFF5EE 0%, #FFFDF9 100%);
  border: 2px solid rgba(224,123,76,0.20);
  box-shadow: var(--card-shadow);
}
.lang-box-label {
  font-family: "Noto Serif SC", serif;
  font-size: 22px;
  font-weight: 700;
  letter-spacing: 4px;
  margin-bottom: 20px;
}
.avoid .lang-box-label { color: #B5ACA0; }
.use .lang-box-label { color: var(--accent-warm); }
.lang-box ul { list-style: none; }
.lang-box ul li { font-size: 17px; line-height: 2.6; }
.avoid ul li { color: #B5ACA0; }
.use ul li { color: var(--text); }

.sub-head {
  font-family: "Noto Serif SC", serif;
  font-size: 24px;
  font-weight: 900;
  letter-spacing: 3px;
  color: var(--text);
  margin-bottom: 8px;
}
.sub-desc { font-size: 15px; color: var(--text-light); margin-bottom: 24px; }

.transform-list {
  display: flex;
  flex-direction: column;
  gap: 16px;
}
.transform-item {
  display: grid;
  grid-template-columns: 1fr auto 1fr;
  align-items: center;
  gap: 20px;
  padding: 24px 28px;
  border-radius: var(--card-radius);
  background: #FFFDF9;
  border: 2px solid rgba(217,185,145,0.10);
  box-shadow: var(--card-shadow);
  transition: transform 0.3s, box-shadow 0.3s;
}
.transform-item:hover { transform: translateX(6px); box-shadow: var(--card-shadow-lg); }

.ti-before {
  text-align: right;
  font-size: 18px;
  color: #B5ACA0;
  text-decoration: line-through;
  font-weight: 500;
}
.ti-arrow {
  color: var(--accent-warm);
  font-family: "Noto Serif SC", serif;
  font-size: 24px;
  font-weight: 700;
  flex-shrink: 0;
}
.ti-after {
  font-family: "Noto Serif SC", serif;
  font-size: 20px;
  color: var(--text);
  font-weight: 700;
  background: linear-gradient(180deg, transparent 55%, rgba(224,123,76,0.14) 55%);
  padding: 0 4px;
}

.naming-principle {
  font-family: "Noto Serif SC", serif;
  font-size: 22px;
  color: var(--text);
  margin-bottom: 20px;
  letter-spacing: 3px;
  font-weight: 700;
}
.naming-principle strong { color: var(--accent-warm); font-weight: 900; }

.naming-tags { display: flex; flex-wrap: wrap; gap: 12px; }
.n-tag {
  display: inline-block;
  padding: 12px 26px;
  border-radius: 30px;
  font-size: 18px;
  letter-spacing: 2px;
  font-weight: 700;
  box-shadow: var(--card-shadow);
  border: 2px solid rgba(224,123,76,0.20);
  background: #FFFDF8;
  color: var(--text);
}
.n-tag.future {
  color: var(--text-light);
  border-color: rgba(200,180,160,0.14);
  font-weight: 400;
  background: #FAFAF7;
  box-shadow: none;
}
.naming-note { font-size: 14px; color: var(--text-light); margin-top: 12px; }

@media (max-width: 768px) {
  .lang-compare { grid-template-columns: 1fr; }
  .transform-item { grid-template-columns: 1fr; gap: 8px; }
  .ti-before { text-align: left; }
  .ti-arrow { transform: rotate(90deg); }
}
</style>
