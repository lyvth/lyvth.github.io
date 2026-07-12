# Yêu cầu nội dung website — theo CV (Lys_CV.pdf)

Nguồn: `~/Downloads/Lys_CV.pdf` (cập nhật 17.06.2026). File này dùng để theo dõi việc chuyển nội dung CV vào các component đã có ở `src/components/`.

## 1. Thông tin cá nhân (Hero)
- Họ tên: **Ly Vu** (Vũ Thị Hương Ly)
- Chức danh: Softwareentwicklerin (Lập trình viên) — Informatik B.Sc.
- Công ty hiện tại: schubwerk GmbH, Wiesbaden, Đức
- LinkedIn: linkedin.com/in/ly-vu-b80968387
- Thành phố: Hamburg
- Ảnh đại diện: có trong CV (góc trên phải)

> ⚠️ SĐT, email, địa chỉ nhà và ngày sinh là thông tin nhạy cảm — **không đưa vào yêu cầu/website**. Web chỉ hiện LinkedIn + thành phố (Hamburg).

## 2. Kinh nghiệm làm việc (Experience) — thay cho placeholder ở `ExperienceSection.vue`

| Thời gian | Vị trí | Nơi làm việc | Mô tả | Công nghệ |
|---|---|---|---|---|
| 10.2025 – nay | Softwareentwicklerin | schubwerk GmbH, Wiesbaden | Phát triển nhiều dự án PHP: (1) Schubwerk-App — giải pháp marketing nội bộ, dùng bởi nhiều khách hàng; (2) Webshop bán thiết bị y tế | HTML/CSS, TypeScript, Vue.js, Bootstrap 5, amCharts5, Laravel, Shopware 6, Docker |
| 06.2025 – 09.2025 | Praktikum Softwareentwicklung | schubwerk GmbH, Wiesbaden | Xây dựng hệ thống đặt lịch cho dịch vụ tư vấn nha khoa. Làm cả backend (TYPO3) và frontend | HTML/CSS, JavaScript, jQuery, Bootstrap 5, TYPO3, Docker |
| 11.2018 – 08.2022 | Softwareentwicklerin | MBBank, Hà Nội | Thiết kế/phát triển/viết tài liệu Backend API cho dịch vụ thanh toán bên thứ ba trong app MBBank (tiền điện, nước, nạp điện thoại); API cho hệ thống Open Banking nộp thuế; API trên nền tảng Apigee | Microservices, Spring, Swagger, Apigee, GitLab CI, Rancher |
| 06.2018 – 10.2018 | Praktikum Softwareentwicklung | MBBank, Hà Nội | Phát triển ESB services kết nối hệ thống lõi ngân hàng với app MBBank và đối tác | Software AG Designer, SQL Developer |
| 03.2018 – 05.2018 | Praktikum PHP-Entwicklung | The Online Management Training Company (OMT), Hà Nội | Phát triển module chấm công cho KidsOnline (phần mềm quản lý mẫu giáo); viết test thủ công | Laravel |
| 09.2017 – 12.2017 | Praktikum Softwaretest | Sao Khue Software and Solutions GmbH, Hà Nội | Viết và chạy test tự động cho web app lĩnh vực y tế | JavaScript, Jasmine |

## 3. Học vấn (Education) — thay cho placeholder ở `SkillsSection.vue`
- **Cử nhân Công nghệ Thông tin (B.Sc.)** — VNU University of Engineering and Technology, ĐHQG Hà Nội (08.2014 – 06.2018)
  - Bằng đã được công nhận tương đương tại Đức (ZAB/Anabin)

## 4. Đào tạo thêm (Weiterbildung) — mục mới, chưa có component
- 12.2024 – 05.2025: Khóa tiếng Đức chuyên ngành, đạt **C1** — Fremdsprachen-Institut Colón, Hamburg
- 12.2023 – 06.2024: Khóa tiếng Đức chuyên ngành, trình độ B2 — Hamburger Volkshochschule
- 04.2023 – 10.2023: Khóa tiếng Đức + chứng chỉ DTZ B1 — Estudio Español, Hamburg
- 02.2017 – 03.2017: Khóa kiểm thử phần mềm thủ công — TesterHN, Hà Nội

## 5. Kỹ năng IT — thay cho danh sách skill hiện tại ở `SkillsSection.vue`
- **Ngôn ngữ lập trình**: TypeScript, JavaScript, HTML/CSS, AngularJS, PHP, Java, SQL
- **Framework**: Vue.js, Laravel, TYPO3, Spring
- **Database**: MySQL, Oracle DB
- **IDE**: VS Code, PHPStorm, IntelliJ IDEA, Oracle SQL Developer, Software AG Designer
- **API**: Swagger UI, Apigee Edge
- **DevOps**: Git, Jenkins, Rancher, Kibana, Docker
- **Quy trình**: Scrum (Agile)
- **Văn phòng**: Microsoft Word/Excel/PowerPoint/Outlook/Teams, MindX

## 6. Ngôn ngữ (Languages) — mục mới
- Tiếng Đức: B2 (đã hoàn thành khóa C1, có thể cập nhật khi có chứng chỉ chính thức)
- Tiếng Anh: B1
- Tiếng Việt: Bản ngữ

## 7. Sở thích (Hobbys) — mục mới, tùy chọn
- Cầu lông (2–3 buổi/tuần), từng đạt giải tại **Asia Cup Hamburg 2024** (đôi nam nữ)
- Nấu món ăn Việt truyền thống
- Đạp xe

## 8. Liên hệ (Contact) — thay placeholder ở `ContactSection.vue`
- LinkedIn: linkedin.com/in/ly-vu-b80968387
- (SĐT/email/địa chỉ/ngày sinh: không đăng công khai — xem lưu ý mục 1)
- Thành phố: Hamburg

---

## Checklist triển khai
- [ ] Cập nhật `HeroSection.vue`: tên, chức danh, công ty, ảnh đại diện thật (thay avatar chữ "HL")
- [ ] Cập nhật `ExperienceSection.vue` với đầy đủ 6 kinh nghiệm làm việc ở mục 2
- [ ] Cập nhật `SkillsSection.vue`: phần "Học vấn" dùng mục 3, phần "Kỹ năng" dùng mục 5
- [ ] Thêm section mới "Đào tạo thêm" (mục 4) — có thể gộp vào phần Học vấn
- [ ] Thêm section mới "Ngôn ngữ" (mục 6)
- [ ] Thêm section "Sở thích" (mục 7) — tùy chọn, tăng tính cá nhân
- [ ] Cập nhật `ContactSection.vue` với LinkedIn thật (không dùng email/SĐT cá nhân)
- [ ] Cập nhật nav trong `TheHeader.vue` nếu có thêm section mới
