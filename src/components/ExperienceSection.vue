<script setup>
// TODO: chỉnh lại thông tin kinh nghiệm và dự án cho đúng thực tế
const experience = [
  {
    role: 'Lập trình viên',
    company: 'Schubwerk GmbH',
    time: 'Hiện tại',
    desc: 'Phát triển và bảo trì các ứng dụng web, phối hợp cùng đội ngũ để triển khai tính năng mới.',
  },
]

const projects = [
  {
    name: 'Tên dự án (điền sau)',
    desc: 'Mô tả ngắn về dự án, vai trò và công nghệ đã sử dụng.',
    link: '',
  },
]
</script>

<template>
  <section id="experience">
    <div class="container">
      <p class="eyebrow">Hành trình</p>
      <h2>Kinh nghiệm &amp; Dự án</h2>

      <div class="timeline">
        <div v-for="job in experience" :key="job.company" class="timeline__item">
          <h3>{{ job.role }} · {{ job.company }}</h3>
          <div class="muted">{{ job.time }}</div>
          <p>{{ job.desc }}</p>
        </div>
      </div>

      <h3 class="projects__title">Dự án nổi bật</h3>
      <div class="projects-grid">
        <div v-for="project in projects" :key="project.name" class="project-card">
          <h4>{{ project.name }}</h4>
          <p>{{ project.desc }}</p>
          <a v-if="project.link" :href="project.link" target="_blank" rel="noopener">Xem chi tiết →</a>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.timeline {
  margin-top: 32px;
  display: flex;
  flex-direction: column;
  gap: 24px;
}

.timeline__item {
  padding-left: 20px;
  border-left: 2px solid var(--color-accent);
}

.timeline__item h3 {
  font-size: 1.1rem;
  color: var(--color-text);
  margin-bottom: 4px;
}

.muted {
  color: var(--color-text-muted);
  font-size: 0.9rem;
}

.projects__title {
  margin-top: 56px;
  font-size: 1.3rem;
  color: var(--color-text);
}

.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 20px;
  margin-top: 24px;
}

.project-card {
  background: var(--color-surface);
  border: 1px solid var(--color-border);
  border-radius: 12px;
  padding: 24px;
}

.project-card h4 {
  color: var(--color-text);
  margin: 0 0 8px;
}
</style>
