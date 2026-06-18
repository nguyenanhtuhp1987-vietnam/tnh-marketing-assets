# 📚 Thư viện ảnh sản phẩm — The Nest House

Nguồn ảnh **gốc, chuẩn brand** để đội AI marketing (Read) lấy tư liệu + `brand-post.py` chèn logo/headline. Lưu trong vault → git backup tự động (private).

## Cấu trúc thư mục
| Thư mục | Chứa |
|---|---|
| `yen-tinh-che/` | Yến tinh chế sợi dài/ngắn (SD100, SD50, SN100, SN50, RL100) |
| `yen-chung/` | Yến chưng các vị (YC6, YC20, YCHK15) — đường phèn, đông trùng, tam vị… |
| `set-qua-tang/` | Hộp quà, set biếu, bao bì cao cấp (Tết, lễ, B2B) |
| `nguyen-lieu-hau-truong/` | Sợi yến cận cảnh, quy trình, hậu trường nghề yến |
| `khach-hang-review/` | Ảnh khách, review, feedback (đã xin phép) |

## Quy ước đặt tên
`<SKU hoặc chủ đề>-<mô tả ngắn>-<số thứ tự>.jpg`
- VD: `YC6-hop-qua-trang-1.jpg` · `SD100-hu-soi-dai-2.jpg` · `hau-truong-nhat-yen-1.jpg`
- Chữ thường, không dấu, nối bằng `-`. Ưu tiên cạnh dài ≥1500px, nền sạch.

## Agent dùng thế nào
- **Tư liệu mô tả:** agent đọc tên/đường dẫn để đặt prompt sát thực tế.
- **Nền thật cho post:** `python3 ../brand-post.py thu-vien-san-pham/set-qua-tang/<ảnh>.jpg ra.png --headline "…"` → chèn logo + headline lên ảnh THẬT (chuẩn hơn ảnh AI cho hộp quà).
- **Đăng IG:** ảnh thật tránh được lỗi AI bịa brand.

## Lớp phát hành — URL public (GitHub)
Đăng qua aitoearn/IG cần URL công khai. Chạy `bash ../push-assets.sh` để đồng bộ cả thư viện này lên repo PUBLIC `nguyenanhtuhp1987-vietnam/tnh-marketing-assets` và in URL raw từng ảnh.
- Mẫu URL: `https://raw.githubusercontent.com/nguyenanhtuhp1987-vietnam/tnh-marketing-assets/main/san-pham/<nhóm>/<ảnh>`
- Quy trình: bỏ ảnh vào nhóm tương ứng → `push-assets.sh` → copy URL → đưa cho aitoearn (`createChannelPublishFlow` / `createMedia`).
- ⚠️ Repo công khai: chỉ đẩy ảnh marketing được phép public; không để ảnh nhạy cảm.

> Liên quan: [[../README|🛠️ Bộ công cụ tạo ảnh]] · [[../index|🎨 Brand Kit]] · agent [[brand-visual-tnh]]
