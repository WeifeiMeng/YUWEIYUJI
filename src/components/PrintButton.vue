<template>
  <button class="print-btn no-print" @click="handlePrint" title="打印页面">
    <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round">
      <polyline points="6 9 6 2 18 2 18 9"></polyline>
      <path d="M6 12H4a2 2 0 0 0-2 2v4a2 2 0 0 0 2 2h16a2 2 0 0 0 2-2v-4a2 2 0 0 0-2-2h-2"></path>
      <rect x="6" y="14" width="12" height="8"></rect>
    </svg>
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
  justify-content: center;
  width: 48px;
  height: 48px;
  padding: 0;
  background: var(--accent-warm);
  color: #fff;
  border: none;
  border-radius: 50%;
  cursor: pointer;
  box-shadow: 0 4px 20px rgba(224,123,76,0.35);
  transition: transform 0.3s, box-shadow 0.3s;
}
.print-btn:hover {
  transform: translateY(-3px);
  box-shadow: 0 8px 28px rgba(224,123,76,0.45);
}
.print-btn:active { transform: translateY(0); }
</style>
