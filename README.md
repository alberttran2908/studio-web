# not bad — studio website

Website "PLAYABLE": danh thiếp của studio là một **sort puzzle chơi được thật** — các tile con trỏ (đỏ chớp mắt) xếp theo luật water-sort: 4 màu × 4 tile, 2 cột trống, gom cùng màu về một cột. Thắng → confetti + popup contact. Có undo, new deal, SFX synth WebAudio, đếm moves. Deal ngẫu nhiên đã được verify luôn giải được (BFS solver, 20/20).

- 1 file `index.html`, **không build, không framework** — vanilla JS, 1 vòng rAF, chỉ animate transform/opacity.
- Font: JetBrains Mono (Google Fonts). Màu brand: đỏ `#E0312A` / đen `#0b0b0d`.
- Có fallback `prefers-reduced-motion` + `noscript`.

## Chạy thử local
Mở thẳng `index.html` bằng trình duyệt là được (không cần server).

## Đẩy lên GitHub (repo alberttran2908/studio-web)
```bash
cd studio-web
git init
git add .
git commit -m "playable studio website v1"
git branch -M main
git remote add origin git@github.com:alberttran2908/studio-web.git
git push -u origin main
```

## Bật GitHub Pages
Repo → Settings → Pages → Source: **Deploy from a branch** → Branch `main` / folder `/ (root)` → Save.
Vài phút sau web sống ở `https://alberttran2908.github.io/studio-web/`.

Khi mua domain (vd `notbad.games`): Settings → Pages → Custom domain → điền domain, rồi ở registrar thêm CNAME `www` → `alberttran2908.github.io` (+ A records apex theo docs GitHub Pages).

## Chỉnh nội dung
- Text các level: tìm `qualityZone / techZone / uxZone` trong `index.html`.
- Games: `bonusZone` — thay card "COMING SOON" bằng card game thật (ảnh + link store).
- Email liên hệ: tìm `mailto:hello@notbad.games`.
- Độ dài màn chơi: `#track{height:1000vh}`. Mốc nhảy: mảng `HOPS`.
