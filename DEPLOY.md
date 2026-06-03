# Hướng dẫn deploy & setup (nội bộ) — trang giới thiệu

Trang giới thiệu bản thân (link-in-bio) tĩnh trên GitHub Pages, 100% free. (Phần công khai ở `README.md`.)

> 🔁 Trang **nhận quà / nhập email** đã tách sang repo riêng **`prompt_workflow_gift`**
> (`e:/Indie Hacker/prompt_workflow_gift/` · live `https://baronguyen001.github.io/prompt_workflow_gift/`).
> Trang `home` này chỉ giới thiệu + 1 nút CTA 🎁 dẫn sang trang nhận quà.

---

## A. Deploy lên GitHub Pages

> Repo: `baronguyen001/home` → live tại https://baronguyen001.github.io/home/

```bash
git add . && git commit -m "update landing" && git push
```
(Thư mục đã pin identity **baronguyen001** + SSH alias `git@baronguyen001:` — không cần switch account thủ công.)

### Gắn domain riêng (sau khi validate, ~$10/năm)
- Mua domain → repo Settings → Pages → Custom domain → thêm DNS theo hướng dẫn GitHub. Không phải build lại.

---

## B. Cần thay trong `index.html`
- [ ] `avatar.jpg`: bỏ ảnh chân dung vào thư mục (hoặc xóa dòng `<img>`).
- [x] Link social (YouTube/TikTok/LinkedIn) đã là `@baronguyen001`.
- [x] Nút CTA 🎁 trỏ sang `https://baronguyen001.github.io/prompt_workflow_gift/`.

## C. Analytics free (tùy chọn)
- Cloudflare Web Analytics (free, không cookie banner) hoặc GA4.

---

## Git identity (quan trọng)
- Thư mục này MUST dùng **baronguyen001**, KHÔNG dùng bao-mk1.
- Đã set: local `user.name=baronguyen001`, `user.email=265752715+baronguyen001@users.noreply.github.com`, remote `git@baronguyen001:baronguyen001/home.git`.
