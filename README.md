# LIGHT WAVE DEHAZE

Slide thuyết trình giữa kỳ (Midterm Presentation) cho đề tài **LIGHT WAVE DEHAZE** tại Trường Đại học Công nghệ, ĐHQGHN (VNU-UET).

## 👥 Thành viên nhóm (Team Members)
- **Lương Duy Quân**
- **Lê Minh Sơn**
- **Nguyễn Khánh Việt**

---

## 📂 Cấu trúc thư mục (Repository Structure)

```
.
├── slides/
│   ├── main.tex                 # Source LaTeX Beamer chính
│   ├── beamerthemeUET.sty       # Custom theme UET Beamer
│   ├── figures/                 # Các hình vẽ TikZ / sơ đồ kiến trúc
│   ├── assets/                  # Hình ảnh, logo UET & FIT, minh họa
│   └── README.md                # Tài liệu chi tiết và nguồn tham khảo
├── output/
│   ├── pdf/                     # File PDF slide hoàn chỉnh
│   └── source/                  # File ZIP mã nguồn LaTeX để nộp hoặc tải lên Overleaf
└── README.md
```

## 🛠️ Biên dịch (Build Instructions)

Di chuyển vào thư mục `slides` và chạy lệnh biên dịch hai lần:

```bash
cd slides
pdflatex -interaction=nonstopmode -halt-on-error main.tex
pdflatex -interaction=nonstopmode -halt-on-error main.tex
```

Hoặc nén thư mục `slides/` và tải lên [Overleaf](https://www.overleaf.com/) với trình biên dịch **pdfLaTeX**.

## 📄 File PDF hoàn chỉnh

Xem hoặc tải trực tiếp bản trình chiếu PDF tại [output/pdf/slide-edge-camera-dehazing-uet-en.pdf](output/pdf/slide-edge-camera-dehazing-uet-en.pdf).
