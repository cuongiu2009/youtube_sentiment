# Youtube Sentiment Analysis Portfolio

## 1. Giới thiệu dự án
Phân tích cảm xúc bình luận Youtube bằng các mô hình tự động (VADER, transformers, underthesea) để đánh giá xu hướng tích cực/tiêu cực của cộng đồng. Dự án phù hợp cho Data Analyst fresher muốn thực hành quy trình xử lý dữ liệu thực tế.

## 2. Quy trình thực hiện
- **Lấy dữ liệu:** Sử dụng Youtube API để thu thập bình luận từ video.
- **Tiền xử lý:** Làm sạch bình luận, loại bỏ thẻ HTML, link, giữ nguyên tiếng Việt.
- **Phân tích cảm xúc:** Áp dụng 3 mô hình:
  - VADER (tiếng Anh)
  - Transformers (rating star, chuyển sang nhãn cảm xúc)
  - Underthesea (tiếng Việt)
- **Tổng hợp & trực quan hóa:** So sánh số lượng nhãn, vẽ biểu đồ cột, wordcloud cho từng nhóm cảm xúc.

## 3. Đánh giá mô hình
- So sánh trực quan kết quả giữa các mô hình.
- Phân tích các trường hợp nhãn sai, minh họa bằng wordcloud.
- Nếu có dữ liệu gán nhãn thủ công, có thể tính các chỉ số đánh giá (accuracy, F1, v.v.).

## 4. Kết quả & nhận xét
- Mô hình VADER phù hợp cho tiếng Anh, transformers đa ngôn ngữ, underthesea cho tiếng Việt.
- Kết quả phụ thuộc vào chất lượng dữ liệu đầu vào và đặc thù ngôn ngữ.
- Trực quan hóa giúp kiểm tra nhanh độ hợp lý của nhãn.

## 5. Hướng dẫn sử dụng
1. Cài đặt các thư viện cần thiết:
   ```bash
   pip install google-api-python-client underthesea vaderSentiment transformers wordcloud matplotlib pandas
   ```
2. Chạy từng file Python theo thứ tự:
   - get_youtube_comments.py
   - preprocess_comments.py
   - analyze_sentiment.py
   - analyze_sentiment_vader.py
   - analyze_sentiment_transformers.py
3. Mở notebook `youtube_sentiment.ipynb` để tổng hợp, trực quan hóa và phân tích kết quả.

## 6. Đề xuất phát triển
- Kết hợp nhiều mô hình, bổ sung dữ liệu gán nhãn thủ công để đánh giá chính xác hơn.
- Tích hợp dashboard hoặc webapp để trình bày kết quả trực quan.
