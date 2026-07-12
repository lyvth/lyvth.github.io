<script setup>
</script>

<template>
  <section id="interests">
    <div class="container">
      <p class="eyebrow">Ngoài giờ làm</p>
      <h2>Sở thích</h2>

      <div class="interest-card">
        <span class="interest-card__icon" aria-hidden="true">🏸</span>
        <p class="interest-card__desc">
          Ngoài công việc, mình khá mê cầu lông — tuần nào cũng cố gắng ra sân
          2-3 buổi cùng bạn bè. Đó là lúc mình xả stress, vận động sau một
          ngày ngồi máy tính, và cũng là dịp gặp gỡ mọi người ngoài công việc.
        </p>
      </div>
    </div>
  </section>
</template>

<style scoped>
.interest-card {
  margin-top: 32px;
  display: flex;
  align-items: flex-start;
  gap: 20px;
  background: var(--color-surface);
  border: 1px solid var(--color-border);
  border-radius: 12px;
  padding: 24px;
  max-width: 480px;
}

.interest-card__icon {
  font-size: 2rem;
  line-height: 1;
}

.interest-card__desc {
  margin: 0;
}
</style>
