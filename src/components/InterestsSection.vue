<script setup>
const interests = [
  {
    icon: '🏸',
    title: 'Cầu lông',
    desc: 'Ngoài công việc, mình khá mê cầu lông — tuần nào cũng cố gắng ra sân 2-3 buổi cùng bạn bè. Từng đạt giải ở nội dung đôi nam nữ tại Asia Cup Hamburg 2024, một trong những kỷ niệm mình khá tự hào.',
  },
  {
    icon: '🍜',
    title: 'Nấu ăn',
    desc: 'Mình thích nấu các món ăn Việt truyền thống, vừa để đỡ nhớ nhà, vừa là dịp giới thiệu bạn bè ở đây với hương vị quê hương.',
  },
  {
    icon: '🚴',
    title: 'Đạp xe',
    desc: 'Cuối tuần rảnh mình hay đạp xe loanh quanh, vừa vận động vừa là cách thư giãn đơn giản sau một tuần làm việc.',
  },
]
</script>

<template>
  <section id="interests">
    <div class="container">
      <p class="eyebrow">Ngoài giờ làm</p>
      <h2>Sở thích</h2>

      <div class="interests-grid">
        <div v-for="interest in interests" :key="interest.title" class="interest-card">
          <span class="interest-card__icon" aria-hidden="true">{{ interest.icon }}</span>
          <div>
            <h3 class="interest-card__title">{{ interest.title }}</h3>
            <p class="interest-card__desc">{{ interest.desc }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.interests-grid {
  margin-top: 32px;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 20px;
}

.interest-card {
  display: flex;
  align-items: flex-start;
  gap: 20px;
  background: var(--color-surface);
  border: 1px solid var(--color-border);
  border-radius: 12px;
  padding: 24px;
}

.interest-card__icon {
  font-size: 2rem;
  line-height: 1;
}

.interest-card__title {
  margin: 0 0 8px;
  font-size: 1.1rem;
  color: var(--color-text);
}

.interest-card__desc {
  margin: 0;
}
</style>
