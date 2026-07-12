<script setup>
const links = [
  { href: '#about', label: 'Giới thiệu' },
  { href: '#skills', label: 'Kỹ năng' },
  { href: '#experience', label: 'Kinh nghiệm' },
  { href: '#contact', label: 'Liên hệ' },
]
</script>

<template>
  <header class="header">
    <div class="container header__inner">
      <a href="#" class="header__logo">Hương Ly</a>
      <nav class="header__nav">
        <a v-for="link in links" :key="link.href" :href="link.href">{{ link.label }}</a>
      </nav>
    </div>
  </header>
</template>

<style scoped>
.header {
  position: sticky;
  top: 0;
  z-index: 10;
  backdrop-filter: blur(8px);
  background: rgba(15, 17, 21, 0.8);
  border-bottom: 1px solid var(--color-border);
}

.header__inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding-top: 16px;
  padding-bottom: 16px;
}

.header__logo {
  font-weight: 700;
  font-size: 1.1rem;
  color: var(--color-text);
}

.header__logo:hover {
  text-decoration: none;
  color: var(--color-accent);
}

.header__nav {
  display: flex;
  gap: 24px;
}

.header__nav a {
  color: var(--color-text-muted);
  font-size: 0.95rem;
}

.header__nav a:hover {
  color: var(--color-accent);
  text-decoration: none;
}
</style>
