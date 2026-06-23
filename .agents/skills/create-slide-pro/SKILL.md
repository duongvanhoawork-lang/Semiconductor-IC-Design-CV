---
name: create-slide-pro
description: "create slides"
---

Dưới đây là phiên bản đồng bộ và tổng hợp từ hai Prompt trên, được tinh chỉnh và loại bỏ yếu tố chuyên biệt của ngành Networking (Mạng máy tính) để trở thành một **Khung Thiết kế và Giảng dạy Đa năng (Universal Presentation & Instructional Design Spec)**.

Hệ thống này có thể áp dụng cho mọi lĩnh vực (Công nghệ thông tin, Kinh tế, Y học, Ngôn ngữ, Kỹ thuật...) nhờ sự kết hợp giữa **Tư duy thiết kế tối giản Nhật Bản (Minimalism)** và **Phương pháp giảng dạy trực quan, thực tế**.

---

# 📑 KHUNG THIẾT KẾ VÀ GIẢNG DẠY ĐA NĂNG

`# presentation_design_spec_universal.yaml`

## Ⅰ. GLOBAL DESIGN SETTINGS (CẤU HÌNH THIẾT KẾ TỐI GIẢN)

* **Tone:** Chuyên nghiệp, mang tính cấu trúc cao, sắc nét, tối giản kiểu kiến trúc (Sharp-edged minimalism).
* **Color Palette:**
* *Base:* `#E9E9E9` (Xám nhạt) hoặc `#FFFFFF` (Trắng).
* *Text:* `#000000` (Đen tuyền) hoặc `#333333` (Xám đậm).
* *Accent:* `#000000` (Đen) – Dùng cho các đường kẻ border bold và text cần nhấn mạnh.
* *Special:* Dark mode (Nền đen chữ trắng) – Chỉ dùng cho các slide cần tạo điểm nhấn cực mạnh hoặc sơ đồ phức tạp.


* **Typography:**
* *Headings:* Phông Sans-serif tiếng Anh (e.g., Helvetica Now, Inter). Cỡ chữ lớn, đậm, bố trí phá cách hoặc căn lề nghiêm ngặt.
* *Body:* Phông Gothic (hoặc tương đương tùy ngôn ngữ yêu cầu). Cỡ chữ nhỏ, khoảng cách giãn chữ (letter spacing) và giãn dòng (line height) rộng rãi.


* **Common Layout Rules:**
* *Navigation:* Hiển thị số slide và tên mục nhỏ ở góc trên bên trái (e.g., `01. INTRODUCTION`).
* *Grid:* Sử dụng hệ thống lưới (Strict grid system) để căn chỉnh tuyệt đối các phần tử.
* *Whitespace:* Cố tình để lại các khoảng trống lớn (Không gian âm) để tạo cảm giác sang trọng, thoáng đãng.



---

## Ⅱ. LAYOUT VARIATIONS CATALOG (THƯ VIỆN BỐ CỤC SLIDE)

Giảng viên/Người thiết kế sẽ chọn 1 trong các bố cục dưới đây cho từng slide cụ thể:

| Loại Bố Cục (Type) | Quy Cách Thiết Kế (Design Specification) |
| --- | --- |
| **Title Typography** | Bố cục rải rác. Các keyword/badge đặt ngẫu nhiên như các con dấu. Tiêu đề trung tâm nhỏ, đậm và tiết chế. |
| **Text + Data Emphasis** | Chia đôi không cân xứng. Văn bản dẫn chuyện bên trái, số liệu cực đại (Oversized) bên phải. Phân cách bằng đường kẻ mảnh. |
| **Card Grid** | Lưới ảnh/nội dung xếp sát nhau. Hiệu ứng tương tác dạng thẻ (Web-like grid). |
| **Full-Screen Graphic** | Hình ảnh thực tế chất lượng cao chiếm trọn màn hình (>50%). Giảm độ bão hòa màu (cool tone). Caption rất nhỏ ở góc dưới trái. |
| **Photo + List Split** | Chia đôi 50:50. Trái: Hình ảnh trừu tượng/thực tế. Phải: Danh sách dữ liệu (Tiêu đề bold + Mô tả light). |
| **Minimal Map / Process** | Sơ đồ/Bản đồ tối giản. Nền xám nhạt, chi tiết màu trắng. Dùng đường chỉ dẫn (callout lines) siêu mảnh. |
| **Vertical Timeline** | Trục dọc. Một đường kẻ mảnh ở giữa, nội dung rẽ nhánh sang hai bên theo thứ tự thời gian. |
| **Dark Mode Diagram** | Nền đen, các node liên kết bằng đường kẻ trắng mảnh. Tạo cảm giác công nghệ cao hoặc tư duy hệ thống sâu sắc. |
| **3-Step Columns** | 3 cột chữ dọc. Dùng số lớn (01, 02, 03) làm trụ cột. Không dùng icon, chỉ dùng độ tương phản font chữ để phân cấp. |
| **Two Columns (Problem vs Solution)** | Đường kẻ dọc đen dày phân chia đối lập giữa "Vấn đề" và "Giải pháp". Văn bản căn khối vuông vắn. |

---

## Ⅲ. INSTRUCTIONAL DESIGN ROLE & TARGET (VAI TRÒ VÀ ĐỐI TƯỢNG)

* **Vai trò người giảng dạy:** Giảng viên đại học, Chuyên gia thực chiến, Nhà thiết kế lộ trình học tập (Instructional Designer).
* **Đối tượng người học:** Sinh viên năm 2-3, người mới bắt đầu đến trung cấp của chuyên ngành; dễ mất tập trung; cần những giải thích trực quan, thực tế; cần hiểu để làm được chứ không chỉ học lý thuyết xuông.
* **Presentation Size:** `1920 × 1080 px` (16:9 Modern Widescreen).

---

## Ⅳ. LANGUAGE & CONTENT RULES (QUY TẮC NGÔN NGỮ VÀ NỘI DUNG)

* **Slide Content:** 100% bằng **Tiếng Anh** (Đơn giản, sạch sẽ, hiện đại, dễ hiểu. Không dùng từ học thuật quá nặng nề, không viết đoạn văn dài).
* *Số chữ:* 40–80 từ/slide.
* *Số bullet:* Tối đa 6 bullet/slide.
* *Độ dài bullet:* Tối đa 12 từ/bullet.


* **Teacher Notes / Explanations:** Viết bằng **Tiếng Việt** để trợ giúp giảng viên giảng bài.

---

## Ⅴ. TEACHING & VISUALIZATION METHODOLOGY (PHƯƠNG PHÁP GIẢNG DẠY VÀ TRỰC QUAN HÓA)

### 1. Công thức Giảng giải Khái niệm (7 Bước)

Đối với bất kỳ khái niệm/định lý/mô hình nào, cấu trúc bài giảng phải trả lời được:

1. **WHAT:** Nó là cái gì?
2. **WHY:** Tại sao nó lại tồn tại? (Giải quyết nỗi đau gì?)
3. **HOW:** Cách nó vận hành/hoạt động?
4. **Analogy:** Ẩn dụ/So sánh với một hệ thống vật lý trong thực tế (Ví dụ: Hệ thống đường bộ, nhà kho, quy trình sản xuất, hải quan, v.v.).
5. **Practical IT/Industry Example:** Ví dụ thực tế trong ngành/doanh nghiệp.
6. **Common Mistakes:** Lỗi sai hoặc hiểu nhầm phổ biến của sinh viên.
7. **Daily Connection:** Liên hệ với hệ thống mà sinh viên tương tác hàng ngày.

### 2. Phân cấp Giải thích (Layered Explanation)

* **Beginner Explanation:** Cách giải thích trực giác, dễ hiểu nhất cho người mới.
* **Real Engineering/Expert Explanation:** Cách triển khai, vận hành thực tế ở quy mô doanh nghiệp lớn.

---

## Ⅵ. STANDARD SLIDE STRUCTURE (HỆ THỐNG CẤU TRÚC SLIDE CHUẨN)

Bộ slide phải đi theo đúng thứ tự logic sau:

1. **Title Slide** (Slide tiêu đề, thông tin nhóm/thành viên: MSSV, Họ tên).
2. **Learning Objectives** (Mục tiêu chuẩn đầu ra).
3. **Why This Topic Matters** (Lý do chủ đề này quan trọng).
4. **Core Concepts** (Các khái niệm cốt lõi).
5. **Step-by-Step Mechanism** (Cơ chế vận hành từng bước).
6. **Technical/Deep Dive** (Đi sâu vào kỹ thuật/bản chất hệ thống).
7. **Quick Recap** (Củng cố nhanh sau phần khó).
8. **Real-world Applications / Real Company Scenario** (Ứng dụng thực tế/Kịch bản doanh nghiệp).
9. **What Students Usually Confuse / Common Problems** (Những gì học sinh hay nhầm lẫn).
10. **Security / Performance Considerations** (Lưu ý về an toàn hoặc hiệu suất).
11. **Interview Knowledge / Common Exam Questions** (Kiến thức phỏng vấn xin việc/Câu hỏi thi).
12. **Hands-on / Lab / Demo Ideas** (Ý tưởng thực hành/Lab).
13. **Mini Quiz** (Trắc nghiệm nhanh).
14. **Summary & Key Takeaways** (Tóm tắt và thông điệp cốt lõi).
15. **Thank You** (Slide kết thúc).

---

## Ⅶ. REQUIRED SLIDE OUTPUT FORMAT (MẪU ĐẦU RA CỦA MỖI SLIDE)

Mỗi slide khi được tạo ra phải tuân thủ **CHÍNH XÁC** phom định dạng (Template) sau đây:

```markdown
Slide X: [Tên Tiêu Đề Slide]

[Mã Layout áp dụng, ví dụ: Layout Type: Photo + List Split]

* Bullet point 1 (English, max 12 words)
* Bullet point 2 (English, max 12 words)
* Bullet point 3 (English, max 12 words)

Expected speaking time: 
2–3 minutes

### Visual Suggestion
* Diagram type: [Tên loại sơ đồ, ví dụ: Flowchart/Venn Diagram...]
* Icon list: [Danh sách icon cần dùng]
* Image search keywords: [Từ khóa tìm ảnh]
* Animation sequence: [Thứ tự xuất hiện của các phần tử khi click]
* Layout recommendation: [Gợi ý sắp xếp bố cục]
* Diagram Idea: [Mô tả chi tiết ý tưởng thiết kế sơ đồ trực quan]

### Speaker Notes (Vietnamese)
[Nội dung bài giảng bằng tiếng Việt sinh động, phong cách mentor, hướng dẫn giảng viên cách dẫn dắt]

### Memory Tip
[Mẹo hoặc câu thần chú giúp sinh viên ghi nhớ bài học ngay lập tức]

### Logo Placement
Location: Top-left corner (0X. SECTION TITLE)

### Real-world Example
[Ví dụ thực tế trực quan từ các công ty lớn hoặc đời sống]

```

---

## Ⅷ. AUTO-GENERATION MATRIX (HỆ THỐNG TỰ ĐỘNG HÓA PHỤ TRỢ)

Cuối bài giảng, hệ thống phải tự động tạo ra các phần sau dựa trên chủ đề:

1. **Auto Diagram Generation:** Bản mô tả thiết kế sơ đồ (Flowchart cấu trúc hoặc Topology minh họa).
2. **Auto Lab Creation:** Bài thực hành thực tế bước-bước (Step-by-step).
3. **Auto Exam Creation:** Ngân hàng đề thi (Trắc nghiệm + Tự luận).
4. **Auto PPT Theme System:** Định nghĩa bộ mã màu CSS/Hex và chỉ định Font Family cụ thể cho chủ đề đó.
5. **Bloom Taxonomy Mapping:** Định vị các phần của bài học tương ứng với các cấp độ nhận thức (Remember, Understand, Apply, Analyze, Evaluate, Create).
6. **ABET Outcome Mapping:** Ánh xạ chuẩn đầu ra kỹ thuật/công nghệ quốc tế (ABET).

*Tên file đầu ra mặc định:* `"keyword_of_the_topic".pptx`