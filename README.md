# Baro Bao — Landing Page (GitHub Pages, 100% free)

Landing page tĩnh để test thị trường: hero + lead magnet (bộ prompt) + form email + link YouTube/TikTok/LinkedIn. Tất cả miễn phí.

---

## A. Đưa lên GitHub Pages (free) — 5 phút

> Dùng account **barobaonguyen** (xem note git identity cuối file).

### Cách nhanh nhất: repo mới dưới account cũ → `barobaonguyen.github.io/barobao`

1. Tạo repo `barobao` (public) trên GitHub.
2. Trong thư mục này:
   ```bash
   git init
   git add index.html README.md
   git commit -m "Landing page Baro Bao v1"
   git branch -M main
   git remote add origin git@github.com:barobaonguyen/barobao.git
   git push -u origin main
   ```
3. GitHub → repo `barobao` → **Settings → Pages** → Source: `Deploy from a branch` → Branch: `main` / `/ (root)` → Save.
4. Đợi 1-2 phút → trang live tại: **https://barobaonguyen.github.io/barobao/**

### (Tùy chọn) URL sạch `barobao.github.io`
- Tạo **account GitHub mới tên `barobao`** → tạo repo tên đúng `barobao.github.io` → push file vào → live tại `https://barobao.github.io`.

### (Sau khi validate) Gắn domain riêng `barobao.com` — ~$10/năm
- Mua domain (Namecheap/Porkbun) → Settings → Pages → Custom domain → nhập `barobao.com` → thêm bản ghi DNS theo hướng dẫn GitHub. **Không phải build lại trang.**

---

## B. Bắt email + tự gửi lead magnet (free) — MailerLite

> GitHub Pages không tự lưu email → cần form của công cụ email. **MailerLite free**: tới 1.000 subscriber + automation.

1. Đăng ký mailerlite.com (free).
2. **Forms → Embedded form** → tạo form "Nhận bộ prompt" → bấm **Embed** → copy đoạn mã HTML.
3. Mở `index.html`, tìm khối:
   ```
   <!-- CHÈN FORM EMAIL Ở ĐÂY -->
   <form onsubmit=...>...</form>
   ```
   → **xóa cả khối `<form>` demo**, dán mã MailerLite vào đúng chỗ đó.
4. **Automation** trong MailerLite: trigger "khi đăng ký form này" → gửi email kèm link PDF lead magnet.
   - Nội dung email: dùng **Email 1** trong `ideas-vault/007-jp-skills-academy/PHASE0/04_tech_studio.md`.
5. Commit + push lại.

> Thay MailerLite bằng **Kit (ConvertKit) free** cũng được — bước tương tự (Forms → Embed HTML).

---

## C. Host PDF lead magnet (free)
- Cách 1: bỏ file `leadmagnet.pdf` vào repo này → link `https://barobaonguyen.github.io/barobao/leadmagnet.pdf`.
- Cách 2: upload Google Drive → share "ai có link" → dán link vào email automation.
- Nội dung PDF: lấy từ `PHASE0/07_lead_magnet_AI.md`, format bằng Canva free.

---

## D. Cần thay trong `index.html`
- [ ] `avatar.jpg`: bỏ 1 ảnh chân dung vào thư mục này (hoặc xóa dòng `<img>` nếu chưa có).
- [ ] 3 link `href="#"` ở mục "Theo dõi mình" → link YouTube / TikTok / LinkedIn thật.
- [ ] Khối `<form>` demo → mã nhúng MailerLite/Kit.

---

## E. Analytics free (tùy chọn)
- **Cloudflare Web Analytics** (free, không cần cookie banner): thêm 1 đoạn script vào `<head>`.
- Hoặc Google Analytics 4 (free).

---

## Git identity (quan trọng — theo convention của anh)
- Commit phải dùng **barobaonguyen** + email noreply:
  ```bash
  git config user.name "barobaonguyen"
  git config user.email "265752715+barobaonguyen@users.noreply.github.com"
  ```
- Nếu dùng gh CLI: `gh auth switch -u barobaonguyen` trước khi thao tác.
- KHÔNG commit email/PII riêng tư; trang này public.
