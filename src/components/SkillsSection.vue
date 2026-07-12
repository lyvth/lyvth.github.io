<script setup>
// TODO: chỉnh lại danh sách kỹ năng và học vấn cho đúng thực tế
const skills = [
  'JavaScript / TypeScript',
  'Vue.js',
  'HTML / CSS',
  'Git',
  'REST API',
]

const education = [
  {
    title: 'Chứng chỉ / Bằng cấp (điền sau)',
    place: 'Tên trường / tổ chức',
    time: '20xx - 20xx',
  },
]
</script>

<template>
  <section id="skills">
    <div class="container">
      <p class="eyebrow">Năng lực</p>
      <h2>Kỹ năng &amp; Học vấn</h2>

      <div class="skills-grid">
        <div>
          <h3>Kỹ năng</h3>
          <ul class="skills-list">
            <li v-for="skill in skills" :key="skill">{{ skill }}</li>
          </ul>
        </div>

        <div>
          <h3>Học vấn</h3>
          <ul class="education-list">
            <li v-for="item in education" :key="item.title">
              <strong>{{ item.title }}</strong>
              <div class="muted">{{ item.place }} · {{ item.time }}</div>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.skills-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 48px;
  margin-top: 32px;
}

@media (max-width: 640px) {
  .skills-grid {
    grid-template-columns: 1fr;
  }
}

.skills-list {
  list-style: none;
  padding: 0;
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
}

.skills-list li {
  padding: 8px 16px;
  border-radius: 999px;
  background: var(--color-surface);
  border: 1px solid var(--color-border);
  font-size: 0.9rem;
  color: var(--color-text);
}

.education-list {
  list-style: none;
  padding: 0;
  display: flex;
  flex-direction: column;
  gap: 16px;
}

.education-list li {
  color: var(--color-text);
}

.muted {
  color: var(--color-text-muted);
  font-size: 0.9rem;
  margin-top: 4px;
}
</style>
