<template>
  <button class="print-btn no-print" @click="handlePrint" title="导出为 PDF（A4）">
    <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round">
      <polyline points="6 9 6 2 18 2 18 9"></polyline>
      <path d="M6 12H4a2 2 0 0 0-2 2v4a2 2 0 0 0 2 2h16a2 2 0 0 0 2-2v-4a2 2 0 0 0-2-2h-2"></path>
      <rect x="6" y="14" width="12" height="8"></rect>
    </svg>
    <span>导出 PDF</span>
  </button>
</template>

<script setup>
function handlePrint() {
  window.print()
}
</script>

<style scoped>
.print-btn {
  position: fixed;
  bottom: 28px;
  right: 28px;
  z-index: 1000;
  display: flex;
  align-items: center;
  gap: 10px;
  padding: 14px 24px;
  background: var(--accent-warm);
  color: #fff;
  border: none;
  border-radius: 40px;
  font-size: 16px;
  font-weight: 700;
  letter-spacing: 3px;
  cursor: pointer;
  box-shadow: 0 6px 24px rgba(224,123,76,0.35);
  transition: transform 0.3s, box-shadow 0.3s;
  font-family: "Noto Sans SC", sans-serif;
}
.print-btn:hover {
  transform: translateY(-3px);
  box-shadow: 0 10px 32px rgba(224,123,76,0.45);
}
.print-btn:active {
  transform: translateY(0);
}
</style>
