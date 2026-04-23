# Day 16 Submission — Vu Quang Phuc

## Members
- Vũ Quang Phuc

---

## 1. Idea reframed

Original idea:
> AI Agent hỗ trợ sinh viên và người đi làm đánh giá kỹ năng và định hướng nghề nghiệp.

Reframed as a product opportunity:
> Sinh viên IT mới ra trường và người chuyển việc thiếu năng lực tự phân tích thị trường lao động. Các giải pháp tìm việc hiện tại (TopCV, VietnamWorks) chỉ dừng ở mức gợi ý việc làm, thiếu chiều sâu phân tích về "skill gap" và xu hướng kỹ năng dài hạn. Chúng ta có cơ hội dùng AI Agent tự động hóa việc thu thập, phân tích hàng nghìn JD thực tế để cung cấp cho họ bức tranh thị trường và lộ trình học tập tối ưu, giúp họ không bị chệch hướng đầu tư kỹ năng.

---

## 2. Customer / Segment Card

- **Segment name:** Sinh viên IT năm cuối / Sinh viên mới ra trường (Freshers)
- **Operational context:** Đang chuẩn bị CV để xin thực tập hoặc công việc chính thức đầu tiên.
- **Recurring workflow:** Duyệt CV → Lướt thị trường (TopCV/ITviec) → Search Job → Tự phân tích yêu cầu JD → Rút ra insight → Cập nhật lộ trình học/CV → Nộp đơn.
- **Pain moment:** Điểm nghẽn lớn nhất nằm ở bước "Tự phân tích yêu cầu JD" và "Rút ra insight": mất quá nhiều thời gian lướt đọc JD thủ công nhưng vẫn mơ hồ, không biết mình đang thiếu kỹ năng gì trọng yếu nhất so với mặt bằng chung.
- **Why now:** Sự bùng nổ của LLM cho phép đọc hiểu, trích xuất (parse metadata) và phân tích ngôn ngữ tự nhiên từ dữ liệu unstructured (JD) với chi phí rẻ và tốc độ mà con người không thể làm bằng tay.
- **Access path:** Qua các CLB học thuật IT, phòng công tác sinh viên các trường Đại học kỹ thuật, hoặc cộng đồng sinh viên IT trên Facebook/Discord.

One-sentence description:
> Sinh viên IT sắp ra trường đang loay hoay mất định hướng vì không biết chính xác kỹ năng hiện tại của mình còn thiếu những gì so với yêu cầu thực tế của các công ty công nghệ.

---

## 3. Need Map (2–3 needs)

### Need #1 (priority)
- **Statement (JTBD):** When chuẩn bị CV để xin việc, I want biết chính xác khoảng cách kỹ năng (skill gap) giữa tôi và nhu cầu của thị trường, so I can ưu tiên học đúng những kỹ năng đang được săn đón thay vì học dàn trải.
- **Current workaround:** Rải CV cầu may, lên các group Facebook IT hỏi "Năm 4 rồi nên học gì tiếp theo", hoặc tự đọc từng JD trên TopCV rồi ghi chú ra giấy/Excel.
- **Pain signal:** Tốn hàng tuần liền để tự research nhưng vẫn mông lung; rải nhiều CV nhưng tỷ lệ phản hồi thấp vì không match keyword kỹ năng của nhà tuyển dụng.
- **Evidence / proxy evidence:** Số lượng lớn các bài post hỏi xin định hướng nghề nghiệp trên các diễn đàn IT; Các tính năng AI check CV / Career Map của các nền tảng quốc tế (như Kickresume) thu hút lượng lớn traffic.
- **Why underserved:** Các trang tìm việc ở VN tập trung vào việc "khớp lệnh" (job matching) ngay lập tức cho doanh nghiệp, chứ không tập trung vào việc "phân tích và giáo dục" định hướng dài hạn cho ứng viên.

### Need #2
- **Statement (JTBD):** When phải lựa chọn một ngách chuyên sâu (VD: Frontend, AI, Data), I want nhìn thấy bức tranh xu hướng dài hạn về mức lương và tần suất tuyển dụng, so I can đầu tư thời gian vào một lộ trình an toàn và sinh lời.
- **Current workaround:** Đọc các "IT Market Report" được phát hành hàng năm (Vietnam IT Market Report).
- **Pain signal:** Báo cáo ngành thường có độ trễ cao (1 năm 1 lần), chung chung, không real-time và không mang tính cá nhân hóa.
- **Evidence / proxy evidence:** Làn sóng sa thải (layoff) và sự phát triển của AI gây ra tâm lý hoang mang, FOMO mạnh mẽ trong cộng đồng dev.
- **Why underserved:** Việc tổng hợp dữ liệu real-time thành dashboard xu hướng cho người dùng cuối đòi hỏi pipeline dữ liệu lớn (cào dữ liệu liên tục) mà các nền tảng truyền thống không chia sẻ public.

---

## 4. Strategy Statement

For **sinh viên IT mới ra trường**
who struggle with **việc thiếu góc nhìn tổng quan và mơ hồ về khoảng cách kỹ năng (skill gap)**,
our product helps them **phát hiện lỗ hổng kỹ năng và định hướng lộ trình học tập**
through **việc tự động hóa phân tích hàng ngàn JD thực tế để rút ra Aggregate Insights**,
unlike **các nền tảng việc làm truyền thống chỉ dừng lại ở mức gợi ý việc làm (job matching)**,
because we can leverage **hệ thống AI Agent tự động crawl, trích xuất và phân tích dữ liệu tuyển dụng một cách liên tục**.

---

## 5. Moat Hypothesis

**Moat mechanism:** Data compounding & Workflow embedding

If we deploy 10,000 times in the IT career vertical, the following improve:
1. Pipeline dữ liệu (JD metadata, top skills, salary range) ngày càng dày và mang tính lịch sử, giúp insight/trend dự đoán càng chính xác hơn (Data compounding).
2. Hệ thống chuẩn hóa (normalize) từ khóa kỹ năng (ví dụ: nhận diện "React", "ReactJS", "React.js" là một) ngày càng thông minh.
3. Sinh viên tin tưởng vào hệ thống tư vấn này hơn vì nó dựa trên data thực tế real-time chứ không phải cảm tính, từ đó biến tool thành bước bắt buộc (workflow embedding) trước khi nộp CV.

Why competitors cannot easily replicate this:
> Việc xây dựng một pipeline thu thập JD liên tục, sạch, tuân thủ pháp lý (chỉ lấy metadata/aggregate data - ADR-10) và xử lý qua LLM tốn nhiều công sức setup. Đối thủ mới có thể copy giao diện, nhưng không thể có ngay lập tức khối lượng dữ liệu lịch sử về xu hướng kỹ năng mà chúng ta đã tích lũy qua thời gian dài.

---

## 6. Initial TAM / SAM / SOM view

| Layer | Estimate | Key assumptions | Confidence |
|---|---|---|---|
| TAM | $5M/year | Tổng nhân sự ngành IT VN (~500,000 người) * $10/year (giá trị insight) | Low |
| SAM | $500k - $700k/year | Sinh viên IT ra trường hàng năm (~50,000 - 70,000) * $10/year | Med |
| SOM | 10,000 active users | Chiếm 10-20% sinh viên từ top các trường ĐH công nghệ trong 12-24 tháng (Freemium model) | Med |

**Top 3 unknowns requiring further research:**
1. Mức độ sẵn sàng chi trả (Willingness to pay) của sinh viên cho một báo cáo phân tích skill gap cá nhân hóa là bao nhiêu?
2. Có thể pivot mô hình sang B2B (bán nền tảng cho Phòng Công tác sinh viên các trường Đại học) để tăng doanh thu thay vì thu tiền lẻ từ sinh viên không?
3. Chi phí vận hành (token LLM cho việc trích xuất skill, server lưu trữ/crawling) có tối ưu khi scale lên 10,000 JD/tuần không?

**Judgment:**
- [x] Worth pursuing now
- [ ] Worth pursuing but not now (need to validate [...] first)
- [ ] Not worth pursuing as currently framed

---

## 7. Positioning Note (2 sentences)

**What we are:**
> Chúng tôi là một Trợ lý AI Hướng nghiệp (AI Career Counselor) giúp tự động hóa quá trình phân tích thị trường lao động và lỗ hổng kỹ năng cá nhân dựa trên dữ liệu JD thực tế.

**What we are not / not yet:**
> Chúng tôi không phải là một sàn giao dịch việc làm (job board) như TopCV hay VietnamWorks, nơi cố gắng khớp lệnh ứng viên và doanh nghiệp ngay lập tức.

---

## 8. Self-assessment before Day 17

Trong 6 mắt xích (Idea → Customer → Need → Strategy → Moat → Market Size), mắt xích nào team đang yếu nhất?

> Market Size & Moat. Chúng tôi chưa rõ ràng về Pricing Model để biến lượng User thành doanh thu ổn định (sinh viên thường ít có khả năng chi trả). Ngoài ra, Moat về Data Compounding đòi hỏi phải có Pipeline Crawl cực kỳ ổn định, điều này dễ gặp rủi ro bị các trang job block IP.

Open questions chúng tôi muốn khám phá thêm ở Day 17:
1. Mô hình doanh thu nào là khả thi nhất cho MVP này (Freemium, Freemium kèm quảng cáo, hay pivot B2B)?
2. Minimum Viable Data (Lượng dữ liệu tối thiểu) bao nhiêu JD là đủ để thuật toán đưa ra insight có giá trị thuyết phục user trong buổi demo?
3. Làm thế nào để xây dựng vòng lặp phản hồi (Feedback loop) với user mà không làm phức tạp hóa MVP ban đầu?