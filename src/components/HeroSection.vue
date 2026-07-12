<script setup>
</script>

<template>
  <section id="about" class="hero">
    <div class="container hero__inner">
      <div class="hero__avatar" aria-hidden="true">HL</div>
      <p class="eyebrow">Xin chào, mình là</p>
      <h1>Vũ Thị Hương Ly</h1>
      <p class="hero__role">Lập trình viên tại <strong>Schubwerk GmbH</strong></p>
      <p class="hero__desc">
        Mình xây dựng các ứng dụng web với sự tỉ mỉ trong từng chi tiết,
        từ giao diện đến hiệu năng. Luôn tò mò và không ngừng học hỏi công nghệ mới.
      </p>
      <div class="hero__actions">
        <a href="#contact" class="btn btn--primary">Liên hệ với mình</a>
        <a href="#experience" class="btn btn--ghost">Xem dự án</a>
      </div>
    </div>
  </section>
</template>

<style scoped>
.hero {
  padding-top: 120px;
  padding-bottom: 96px;
  text-align: center;
}

.hero__avatar {
  width: 96px;
  height: 96px;
  margin: 0 auto 24px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 700;
  font-size: 1.5rem;
  color: var(--color-bg);
  background: linear-gradient(135deg, var(--color-accent), var(--color-accent-2));
}

.hero h1 {
  font-size: 2.75rem;
}

.hero__role {
  font-size: 1.1rem;
  color: var(--color-text);
}

.hero__desc {
  max-width: 560px;
  margin-left: auto;
  margin-right: auto;
}

.hero__actions {
  display: flex;
  gap: 16px;
  justify-content: center;
  margin-top: 24px;
}

.btn {
  padding: 12px 24px;
  border-radius: 999px;
  font-weight: 600;
  font-size: 0.95rem;
}

.btn:hover {
  text-decoration: none;
}

.btn--primary {
  background: var(--color-accent);
  color: var(--color-bg);
}

.btn--primary:hover {
  opacity: 0.9;
}

.btn--ghost {
  border: 1px solid var(--color-border);
  color: var(--color-text);
}

.btn--ghost:hover {
  border-color: var(--color-accent);
  color: var(--color-accent);
}
</style>
