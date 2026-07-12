<script setup>
// TODO: điền email, mạng xã hội thật để thay cho placeholder bên dưới
const contacts = [
  { label: 'Email', value: 'email-cua-ban@example.com', href: 'mailto:email-cua-ban@example.com' },
  { label: 'LinkedIn', value: 'linkedin.com/in/ten-cua-ban', href: '#' },
  { label: 'GitHub', value: 'github.com/ten-cua-ban', href: '#' },
]
</script>

<template>
  <section id="contact">
    <div class="container">
      <p class="eyebrow">Kết nối</p>
      <h2>Liên hệ</h2>
      <p class="contact__desc">
        Nếu bạn muốn trao đổi công việc hoặc hợp tác, đừng ngần ngại liên hệ với mình qua các kênh dưới đây.
      </p>

      <ul class="contact-list">
        <li v-for="contact in contacts" :key="contact.label">
          <span class="contact-list__label">{{ contact.label }}</span>
          <a :href="contact.href">{{ contact.value }}</a>
        </li>
      </ul>
    </div>
  </section>
</template>

<style scoped>
.contact__desc {
  max-width: 480px;
}

.contact-list {
  list-style: none;
  padding: 0;
  margin-top: 32px;
  display: flex;
  flex-direction: column;
  gap: 16px;
}

.contact-list li {
  display: flex;
  gap: 16px;
  align-items: baseline;
  padding-bottom: 16px;
  border-bottom: 1px solid var(--color-border);
}

.contact-list__label {
  width: 100px;
  flex-shrink: 0;
  color: var(--color-text-muted);
  font-size: 0.9rem;
  text-transform: uppercase;
  letter-spacing: 0.05em;
}
</style>
