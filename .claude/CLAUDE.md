# Project

Website giới thiệu bản thân của Vũ Thị Hương Ly, xây bằng Vue 3 + Vite.

## Tech stack
- Vue 3 (`<script setup>` SFC), bundler Vite
- Không có router/state library — trang đơn (single page), điều hướng bằng anchor `#id`

## Node version — QUAN TRỌNG
- Máy dev mặc định Node v14 (không được đổi global). Project cần **Node 20** (xem `.nvmrc`).
- Luôn chạy lệnh qua nvm scoped cho project, không đổi default toàn máy:
  `export NVM_DIR="$HOME/.nvm" && source "$NVM_DIR/nvm.sh" && nvm exec 20 -- <lệnh>`
- Preview qua Browser tool dùng `.claude/launch.json`, đã cấu hình sẵn để chạy `npm run dev` với Node 20.

## Cấu trúc
- `src/App.vue` — ráp các section lại
- `src/components/TheHeader.vue` — nav sticky
- `src/components/HeroSection.vue` — giới thiệu bản thân
- `src/components/SkillsSection.vue` — kỹ năng & học vấn
- `src/components/ExperienceSection.vue` — kinh nghiệm & dự án
- `src/components/InterestsSection.vue` — sở thích ngoài giờ làm
- `src/components/ContactSection.vue` — liên hệ
- `src/style.css` — biến CSS toàn cục (dark theme), section nào cũng dùng `.container`

## Nguồn nội dung
- [REQUIREMENTS.md](../REQUIREMENTS.md) ở root: nội dung trích từ CV thật của Ly (`~/Downloads/Lys_CV.pdf`), map theo từng component + checklist triển khai. Dùng file này làm nguồn khi điền nội dung thay placeholder.

## Quy tắc riêng tư — bắt buộc
Không đăng công khai lên website: **số điện thoại, email cá nhân, ngày sinh, địa chỉ nhà cụ thể**. Thông tin liên hệ công khai chỉ gồm LinkedIn và tên thành phố (Hamburg).

## Git workflow — bắt buộc
- Chỉ được làm việc trên **feature branch**, không commit/push trực tiếp lên `main`.
- Trước khi bắt đầu thay đổi, tạo branch mới từ `main` (đặt tên mô tả ngắn gọn, ví dụ `feature/xxx`).
- Sau khi hoàn thành, tự push feature branch lên remote và tạo Pull Request để chờ human review — không tự merge vào `main`.

## Deploy
- Remote: `git@github.com:lyvth/lyvth.github.io.git`, nhánh `main`
- `.github/workflows/deploy.yml`: tự động `npm run build` rồi deploy `dist/` lên GitHub Pages mỗi khi push lên `main`
- Trên GitHub, repo Settings → Pages → Source phải để **"GitHub Actions"**
- Không push hay force-push trực tiếp vào `main` (xem Git workflow ở trên) — mọi thay đổi vào `main` phải qua PR đã được review
