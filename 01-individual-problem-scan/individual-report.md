# 01 — Individual Problem Scan

> Bối cảnh: Marketing/Product/Sales tại một công ty làm sản phẩm (SaaS/App), quan sát các vấn đề lặp lại trong công việc hằng ngày/tuần.

---

## Scan rộng
Scan 10 problems theo 4 lăng kính: Lặp lại, Tốn thời gian, AI có thể tốt hơn, Pain từ người khác.

| # | Lăng kính | Problem quan sát được | Ai chịu ảnh hưởng? | Dấu hiệu thật |
|---|---|---|---|---|
| 1 | Lặp lại | Viết caption/content cho social media mỗi ngày theo lịch đăng | Marketing exec | 30-45 phút/post |
| 2 | Lặp lại | Tổng hợp báo cáo hiệu suất campaign (CTR, CPC, conversion) từ nhiều nền tảng (FB Ads, Google Ads, TikTok) | Marketing/Growth | 1-2 giờ/tuần |
| 3 | Tốn thời gian | Đọc feedback/review khách hàng để tìm insight (App Store, khảo sát, support ticket) | Product Manager | 45-60 phút/tuần |
| 4 | Tốn thời gian | Viết proposal/pitch deck cho khách hàng mới | Sales/BD | 2-3 giờ/proposal |
| 5 | AI có thể tốt hơn | Không có cách nhanh để biết đối thủ vừa launch tính năng/campaign gì | Product, Marketing | Phát hiện trễ, chỉ biết qua tình cờ |
| 6 | AI có thể tốt hơn | CRM có data khách hàng nhưng không tự gợi ý ai nên follow-up trước | Sales | Bỏ lỡ lead nóng |
| 7 | Pain từ người khác | Support team nhận câu hỏi khách hàng lặp lại (đã có trong FAQ) nhưng khách không tự tìm được | Support, khách hàng | 20-30% ticket là câu hỏi lặp |
| 8 | Pain từ người khác | Sales hỏi lại Product liên tục về tính năng/roadmap vì tài liệu chưa rõ | Sales, Product | 5-10 câu hỏi/tuần |
| 9 | Tốn thời gian | Tổng hợp meeting notes + action items sau các buổi họp cross-team | PM, mọi người dự họp | 20-30 phút/buổi |
| 10 | Lặp lại | Viết email follow-up cho khách hàng/lead theo từng giai đoạn funnel | Sales | 10-15 phút/email |
---

## Top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---|---|---|---|
| 1 | Tổng hợp báo cáo campaign | Workflow rõ, metric thời gian dễ đo, có thể so sánh Rule/Workflow/Agent | Có phải tất cả campaign đều dùng 3 nền tảng này không |
| 2 | Đọc feedback tìm insight | Pain thật, AI phân loại/tóm tắt rất hợp | Đo "không bỏ sót insight" khó định lượng chính xác |
| 3 | Support trả lời câu hỏi lặp | Impact rộng, có % đo được rõ | Cần data ticket thật để verify con số 25% |

---

## Problem Card #1 — Tổng hợp báo cáo campaign

**Problem 1 câu:**
Mỗi thứ Hai, Marketing Executive mất khoảng 90 phút tổng hợp số liệu hiệu suất campaign (CTR, CPC, conversion, spend) từ Facebook Ads, Google Ads và TikTok Ads để làm báo cáo tuần cho Marketing Manager.

**Actor:**
Marketing Executive phụ trách chạy và báo cáo hiệu suất quảng cáo hằng tuần.

**Thời điểm / bối cảnh:**
Sáng thứ Hai hằng tuần, trước buổi review với Marketing Manager.

**Current workflow:**

```
1. Export báo cáo từ Facebook Ads Manager (~15 phút)
2. Export báo cáo từ Google Ads (~15 phút)
3. Export báo cáo từ TikTok Ads Manager (~10 phút)
4. Chuẩn hóa 3 file vào 1 Google Sheet, tính tổng/so sánh tuần trước (~25 phút)
5. Viết nhận xét (kênh nào hiệu quả, đề xuất điều chỉnh ngân sách) + gửi report (~25 phút)
```

**Bottleneck:**
Bước 4 và 5 — chuẩn hóa dữ liệu từ 3 định dạng khác nhau và viết nhận xét/insight, chiếm 50/90 phút vì phải tự đối chiếu số liệu và diễn giải ý nghĩa.

**Impact:**
90 phút/tuần cho 1 người. Nếu công ty có 2-3 Marketing Exec chạy campaign riêng, tổng công sức có thể 180-270 phút/tuần. Report trễ khiến Manager quyết định phân bổ ngân sách chậm.

**Success metric:**
Giảm tổng thời gian từ 90 phút xuống dưới 30 phút/tuần; số liệu vẫn chính xác 100% so với nguồn gốc

**Quick gut:**
Workflow

### Draft current workflow

```
CURRENT STATE — 90 phút

[1 Export Facebook Ads: 15']
→ [2 Export Google Ads: 15']
→ [3 Export TikTok Ads: 10']
→ [4 Chuẩn hóa vào Sheet: 25']  <-- bottleneck
→ [5 Viết nhận xét + gửi: 25']  <-- bottleneck
```

### Draft future workflow

```
FUTURE STATE — ~25 phút

[1 Dashboard tự pull data (Looker/Supermetrics): 3']  
→ [2 AI đọc bảng số, tính diff tuần trước: 2']         
→ [3 AI draft nhận xét/insight: 2']                    
→ [4 Marketing Exec review + edit: 15']                
→ [5 Gửi report: 3']

Fallback: AI draft insight sai/thiếu ngữ cảnh → Exec tự viết lại phần đó.
```
---

## Problem Cards #2 và #3 — tóm tắt
| Card | Actor | Bottleneck | Metric | Quick gut | Vì sao chưa chọn làm #1 |
|---|---|---|---|---|---|
| Đọc feedback tìm insight | Product Manager | Đọc + phân loại thủ công feedback từ nhiều nguồn | 60 phút → 20 phút | Workflow | Đo "không bỏ sót insight" khó định lượng |
| Support trả lời câu hỏi lặp | Support agent | Tra cứu FAQ/case cũ để match câu hỏi khách | 8 phút/ticket → dưới 2 phút | Workflow | Cần data ticket thật để verify % lặp |
### Draft workflow — Đọc feedback tìm insight

```
CURRENT STATE — 60 phút

[1 Gom feedback 3 nguồn: 10']
→ [2 Đọc từng feedback: 30']  <-- bottleneck
→ [3 Phân loại thủ công: 15']  <-- bottleneck
→ [4 Tổng hợp report: 5']

FUTURE STATE — ~18 phút

[1 Auto-gom feedback (script/API): 2']  -- Rule
→ [2 AI phân loại theo chủ đề: 2']       -- Workflow step
→ [3 AI tóm tắt top insight: 2']         -- Workflow step
→ [4 PM review + xác nhận: 10']          -- Human boundary
→ [5 PM gửi report: 2']

Fallback: AI phân loại sai/gộp nhầm chủ đề → PM tự đọc lại nhóm nghi ngờ.
```

### Draft workflow — Support trả lời câu hỏi lặp

```
CURRENT STATE — ~11-14 phút/ticket

[1 Nhận ticket: 1']
→ [2 Đọc hiểu câu hỏi: 2']
→ [3 Tìm câu trả lời (tự tra): 5-8']  <-- bottleneck
→ [4 Soạn & gửi: 3']

FUTURE STATE — ~6-7 phút/ticket

[1 Nhận ticket: 1']
→ [2 AI match với FAQ/case cũ, gợi ý câu trả lời: 1']  -- Workflow step
→ [3 Agent review + chỉnh sửa: 3']                     -- Human boundary
→ [4 Gửi: 1']

Fallback: AI gợi ý sai/không match → Agent tự tra cứu thủ công như cũ.
```

