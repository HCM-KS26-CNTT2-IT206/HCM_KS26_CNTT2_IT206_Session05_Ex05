# BÀI THỰC HÀNH 5

## XÂY DỰNG CHIẾN DỊCH TRUYỀN THÔNG TUYỂN SINH KHÓA HỌC PYTHON CƠ BẢN

## 1\. Giới thiệu

Trong bài thực hành này, em sử dụng kỹ thuật **Prompt Chaining** để xây dựng một chiến dịch truyền thông tuyển sinh khóa học Python cơ bản dành cho sinh viên năm nhất.

Thay vì yêu cầu AI làm tất cả trong một lần, em chia công việc thành nhiều prompt. Kết quả của bước trước được dùng làm dữ liệu đầu vào cho bước tiếp theo. Cách làm này giúp nội dung có sự liên kết và hạn chế việc AI tự thay đổi thông tin khóa học.

### Thông tin khóa học được sử dụng

|Nội dung|Thông tin|
|-|-|
|Khóa học|Python cơ bản|
|Đối tượng|Sinh viên năm nhất|
|Độ tuổi|18–20|
|Thời lượng|8 tuần|
|Mục tiêu chiến dịch|Thu hút 100 lượt đăng ký tư vấn|
|Kênh truyền thông|Facebook và TikTok|

**Lưu ý:** Đề bài chưa cung cấp học phí, lịch học, hình thức học hoặc ưu đãi. Vì vậy, chiến dịch không tự đưa ra những thông tin này.

\---

## 2\. Sơ đồ chuỗi Prompt

```text
PROMPT 1
Phân tích khách hàng mục tiêu
        |
        v
Đầu ra: Chân dung sinh viên năm nhất
        |
        v
PROMPT 2
Xây dựng thông điệp truyền thông
        |
        v
Đầu ra: Một thông điệp chính và các ý hỗ trợ
        |
        v
PROMPT 3
Lập kế hoạch nội dung trong 7 ngày
        |
        v
Đầu ra: Lịch đăng Facebook và TikTok
        |
        v
PROMPT 4
Viết bài Facebook và kịch bản TikTok
        |
        v
Đầu ra: 2 bài Facebook + 2 kịch bản TikTok
        |
        v
PROMPT 5
Kiểm tra tính thống nhất chiến dịch
        |
        v
Đầu ra: Báo cáo kiểm tra và đề xuất chỉnh sửa
```

Chuỗi gồm 5 prompt liên tiếp. Kết quả của mỗi bước được chuyển sang bước tiếp theo để tiếp tục xử lý.

\---

## 3\. Xây dựng chuỗi Prompt và kết quả

### 3.1. Prompt 1 – Phân tích chân dung khách hàng mục tiêu

**Mục đích:** Tìm hiểu đối tượng mà chiến dịch muốn tiếp cận trước khi viết nội dung quảng cáo.

**Prompt sử dụng:**

```text
Bạn là người hỗ trợ lập kế hoạch truyền thông cho một trung tâm đào tạo lập trình.
Hãy phân tích chân dung khách hàng mục tiêu cho khóa học Python cơ bản.

Thông tin cố định:
- Đối tượng: Sinh viên năm nhất.
- Độ tuổi: 18–20.
- Thời lượng khóa học: 8 tuần.
- Mục tiêu chiến dịch: 100 lượt đăng ký tư vấn.
- Kênh truyền thông: Facebook và TikTok.

Hãy trình bày đơn giản, gồm: đặc điểm, nhu cầu, khó khăn,
động lực học tập và thói quen sử dụng mạng xã hội.
Không tự thêm học phí, lịch học, ưu đãi hoặc cam kết đầu ra.
```

**Kết quả đầu ra – Chân dung khách hàng mục tiêu:**

|Tiêu chí|Phân tích|
|-|-|
|Độ tuổi|18–20 tuổi|
|Đối tượng|Sinh viên năm nhất, có thể đang học các ngành liên quan đến công nghệ hoặc muốn tìm hiểu lập trình|
|Nhu cầu|Muốn làm quen với lập trình, có thêm kiến thức và kỹ năng phục vụ việc học|
|Khó khăn|Chưa biết bắt đầu từ đâu, chưa quen với cú pháp lập trình và có thể lo ngại kiến thức khó|
|Động lực|Muốn thử sức với lĩnh vực công nghệ, học thêm kỹ năng mới và tự tin hơn khi tiếp cận môn học liên quan|
|Thói quen mạng xã hội|Thường xem video ngắn trên TikTok, theo dõi các trang và nhóm sinh viên trên Facebook|
|Nội dung dễ thu hút|Video ngắn, ví dụ gần gũi, cách giải thích dễ hiểu và thông tin khóa học rõ ràng|

**Nhận xét:** Đối tượng này thường mới tiếp xúc với lập trình nên nội dung cần gần gũi, dễ hiểu, tránh dùng quá nhiều thuật ngữ chuyên môn.

\---

### 3.2. Prompt 2 – Xác định thông điệp truyền thông

**Đầu vào:** Sử dụng chân dung khách hàng mục tiêu ở Prompt 1.

**Prompt sử dụng:**

```text
Dựa trên chân dung khách hàng mục tiêu sau:
\[Chèn toàn bộ kết quả Prompt 1 vào đây]

Hãy đề xuất 3 thông điệp truyền thông cho khóa học Python cơ bản.
Sau đó chọn 1 thông điệp phù hợp nhất với sinh viên năm nhất.

Yêu cầu:
- Ngắn gọn, dễ nhớ và gần gũi.
- Tạo cảm giác người mới cũng có thể bắt đầu học.
- Không hứa hẹn việc làm, thu nhập hoặc cam kết đầu ra.
- Giữ nguyên thời lượng khóa học là 8 tuần.
- Không tự thêm thông tin chưa được cung cấp.
Giải thích ngắn gọn lý do chọn thông điệp.
```

**Kết quả đầu ra:**

Một số thông điệp được đề xuất:

1. Bắt đầu với Python – Từng bước làm quen với lập trình.
2. Chưa biết lập trình? Hãy bắt đầu từ những dòng code đầu tiên.
3. 8 tuần làm quen Python – Mở đầu hành trình khám phá công nghệ.

**Thông điệp chính được chọn:**

<blockquote>
\*\*“Chưa biết lập trình? Hãy bắt đầu từ những dòng code Python đầu tiên!”\*\*
</blockquote>

**Lý do lựa chọn:** Thông điệp sử dụng cách nói gần gũi, đánh đúng tâm lý của sinh viên mới bắt đầu và không tạo cảm giác khóa học quá khó. Nội dung cũng không đưa ra cam kết vượt quá thông tin được cung cấp.

\---

### 3.3. Prompt 3 – Xây dựng kế hoạch nội dung trong 7 ngày

**Đầu vào:** Chân dung khách hàng từ Prompt 1 và thông điệp chính từ Prompt 2.

**Prompt sử dụng:**

```text
Dựa trên chân dung khách hàng mục tiêu:
\[Chèn kết quả Prompt 1]

Và thông điệp truyền thông chính:
“Chưa biết lập trình? Hãy bắt đầu từ những dòng code Python đầu tiên!”

Hãy xây dựng lịch đăng nội dung trong 7 ngày trên Facebook và TikTok
để quảng bá khóa học Python cơ bản.

Thông tin cố định:
- Đối tượng: Sinh viên năm nhất, 18–20 tuổi.
- Thời lượng: 8 tuần.
- Mục tiêu: 100 lượt đăng ký tư vấn.

Yêu cầu:
- Mỗi ngày có chủ đề, nội dung chính, định dạng và kênh đăng.
- Nội dung đi từ thu hút sự chú ý, cung cấp thông tin đến kêu gọi đăng ký tư vấn.
- Giữ thông điệp chính xuyên suốt.
- Không tự thêm học phí, lịch học, ưu đãi hoặc cam kết đầu ra.
```

**Kết quả đầu ra – Lịch nội dung 7 ngày:**

|Ngày|Chủ đề|Nội dung chính|Kênh và định dạng|
|-|-|-|-|
|Ngày 1|Bạn có muốn học lập trình?|Giới thiệu việc bắt đầu học Python dành cho người mới|TikTok – Video ngắn|
|Ngày 2|Python là gì?|Giải thích đơn giản Python là ngôn ngữ lập trình và có thể bắt đầu tìm hiểu từ cơ bản|Facebook – Bài đăng|
|Ngày 3|Người mới học lập trình thường gặp gì?|Chia sẻ những khó khăn như chưa biết viết code, chưa hiểu cú pháp|TikTok – Video ngắn|
|Ngày 4|Giới thiệu khóa học|Giới thiệu khóa Python cơ bản dành cho sinh viên năm nhất, thời lượng 8 tuần|Facebook – Bài đăng|
|Ngày 5|Đừng ngại bắt đầu|Khuyến khích người mới tìm hiểu lập trình từ những kiến thức cơ bản|TikTok – Video ngắn|
|Ngày 6|Giải đáp thắc mắc|Tổng hợp một số câu hỏi thường gặp về việc bắt đầu học Python|Facebook – Bài đăng|
|Ngày 7|Kêu gọi đăng ký tư vấn|Nhắc lại thông tin khóa học và mời người quan tâm đăng ký tư vấn|Facebook và TikTok – Bài đăng/video|

**Nhận xét:** Lịch nội dung được sắp xếp theo trình tự: thu hút sự chú ý, giúp người xem hiểu thêm về Python, giới thiệu khóa học và cuối cùng là kêu gọi đăng ký tư vấn.

\---

### 3.4. Prompt 4 – Viết bài Facebook và kịch bản TikTok

**Đầu vào:** Chân dung khách hàng, thông điệp chính và lịch nội dung 7 ngày từ các bước trước.

**Prompt sử dụng:**

```text
Dựa trên các nội dung sau:
1. Chân dung khách hàng mục tiêu: \[Chèn kết quả Prompt 1]
2. Thông điệp chính: \[Chèn kết quả Prompt 2]
3. Lịch nội dung 7 ngày: \[Chèn kết quả Prompt 3]

Hãy viết:
- 2 bài đăng quảng cáo Facebook.
- 2 kịch bản video TikTok, mỗi video dài 30–45 giây.

Yêu cầu:
- Viết tự nhiên, gần gũi với sinh viên năm nhất.
- Bài Facebook có tiêu đề, nội dung và lời kêu gọi đăng ký tư vấn.
- Kịch bản TikTok có phân cảnh, lời thoại và gợi ý chữ trên màn hình.
- Các nội dung phải cùng hướng đến thông điệp chính.
- Chỉ sử dụng thông tin khóa học đã cho: Python cơ bản,
  sinh viên năm nhất, độ tuổi 18–20, thời lượng 8 tuần.
- Không tự tạo học phí, lịch học, ưu đãi hay cam kết đầu ra.
```

#### A. Hai bài đăng Facebook

**Bài đăng 1 – Dành cho người chưa biết lập trình**

**BẠN MUỐN HỌC LẬP TRÌNH NHƯNG CHƯA BIẾT BẮT ĐẦU TỪ ĐÂU?**

Là sinh viên năm nhất, có thể bạn đã từng nghe đến lập trình Python nhưng vẫn còn khá bỡ ngỡ. Bạn không biết phải học từ đâu, bắt đầu như thế nào hoặc liệu mình có theo kịp hay không.

Đừng quá lo lắng! Việc học một kiến thức mới luôn cần có thời gian để làm quen. Điều quan trọng là bạn dám bắt đầu và kiên trì tìm hiểu từng bước.

Trung tâm hiện tổ chức khóa học **Python cơ bản** dành cho sinh viên năm nhất, độ tuổi 18–20, với thời lượng **8 tuần**.

Nếu bạn đang quan tâm đến lập trình và muốn tìm hiểu thêm về khóa học, hãy đăng ký tư vấn ngay nhé!

**Chưa biết lập trình? Hãy bắt đầu từ những dòng code Python đầu tiên!**

\#PythonCoBan #HocLapTrinh #SinhVienNamNhat

\---

**Bài đăng 2 – Giới thiệu khóa học**

**SINH VIÊN NĂM NHẤT – ĐỪNG NGẠI THỬ SỨC VỚI PYTHON!**

Bạn muốn tìm hiểu về công nghệ? Bạn muốn biết một chương trình máy tính được viết như thế nào?

Python là một lựa chọn để bạn bắt đầu làm quen với lập trình. Với khóa học Python cơ bản có thời lượng **8 tuần**, trung tâm hướng đến những bạn sinh viên năm nhất đang muốn tìm hiểu kiến thức lập trình từ đầu.

Bạn không cần phải biết tất cả ngay từ đầu. Hãy bắt đầu bằng việc tìm hiểu những kiến thức cơ bản và từng bước làm quen với Python.

**Đối tượng:** Sinh viên năm nhất, từ 18–20 tuổi.  
**Khóa học:** Python cơ bản.  
**Thời lượng:** 8 tuần.

Bạn muốn biết thêm thông tin? Hãy để lại đăng ký để được tư vấn về khóa học nhé!

\#Python #LapTrinhCoBan #SinhVien

#### B. Hai kịch bản video TikTok

**Video 1 – Chủ đề: Chưa biết lập trình có học Python được không?**

<text>Thời lượng dự kiến: 35–40 giây</text>

|Thời gian|Hình ảnh / Phân cảnh|Lời thoại|Chữ trên màn hình|
|-|-|-|-|
|0–5 giây|Một sinh viên ngồi trước laptop, nhìn màn hình code|“Bạn muốn học lập trình nhưng lại không biết bắt đầu từ đâu?”|Muốn học lập trình nhưng chưa biết bắt đầu?|
|5–12 giây|Cảnh sinh viên tìm hiểu về Python trên máy tính|“Nếu bạn là sinh viên năm nhất và đang muốn làm quen với lập trình, Python là một lựa chọn để bắt đầu tìm hiểu.”|Làm quen với Python|
|12–25 giây|Hiển thị tên khóa học và hình ảnh học tập|“Trung tâm có khóa học Python cơ bản dành cho sinh viên từ 18 đến 20 tuổi, với thời lượng 8 tuần.”|Python cơ bản – 8 tuần|
|25–38 giây|Sinh viên nhìn vào camera, xuất hiện thông tin đăng ký|“Đừng ngại khi mình chưa biết gì. Hãy bắt đầu từ những dòng code đầu tiên và đăng ký tư vấn để tìm hiểu thêm nhé!”|Đăng ký tư vấn ngay!|

**Video 2 – Chủ đề: Giới thiệu khóa học Python cơ bản**

<text>Thời lượng dự kiến: 35–40 giây</text>

|Thời gian|Hình ảnh / Phân cảnh|Lời thoại|Chữ trên màn hình|
|-|-|-|-|
|0–5 giây|Cảnh sinh viên sử dụng laptop|“Sinh viên năm nhất muốn tìm hiểu về công nghệ nhưng chưa biết học lập trình từ đâu?”|Bạn muốn tìm hiểu lập trình?|
|5–13 giây|Hiển thị chữ Python trên màn hình|“Hãy thử bắt đầu với Python – một ngôn ngữ lập trình mà bạn có thể tìm hiểu từ những kiến thức cơ bản.”|Bắt đầu với Python|
|13–25 giây|Hiển thị thông tin khóa học|“Khóa học Python cơ bản dành cho sinh viên năm nhất từ 18 đến 20 tuổi, thời lượng 8 tuần.”|Đối tượng: 18–20 tuổi / Thời lượng: 8 tuần|
|25–40 giây|Hình ảnh sinh viên học tập, kết thúc bằng lời kêu gọi|“Nếu bạn đang quan tâm, hãy đăng ký tư vấn để được tìm hiểu thêm về khóa học nhé!”|Đăng ký tư vấn ngay hôm nay!|

\---

### 3.5. Prompt 5 – Kiểm tra tính thống nhất của chiến dịch

**Đầu vào:** Toàn bộ kết quả từ Prompt 1 đến Prompt 4.

**Prompt sử dụng:**

```text
Bạn là người kiểm tra nội dung truyền thông.
Hãy kiểm tra toàn bộ chiến dịch dựa trên các kết quả sau:
- Chân dung khách hàng mục tiêu: \[Chèn kết quả Prompt 1]
- Thông điệp chính: \[Chèn kết quả Prompt 2]
- Lịch nội dung 7 ngày: \[Chèn kết quả Prompt 3]
- Hai bài Facebook và hai kịch bản TikTok: \[Chèn kết quả Prompt 4]

Hãy kiểm tra:
1. Các nội dung có đúng đối tượng sinh viên năm nhất 18–20 tuổi không?
2. Thông điệp chính có được giữ thống nhất không?
3. Thông tin khóa học có bị thay đổi không?
4. Nội dung có phù hợp với Facebook và TikTok không?
5. Các bài đăng và video có lời kêu gọi đăng ký tư vấn không?

Trình bày kết quả theo bảng gồm: tiêu chí, kết quả kiểm tra và nhận xét.
Nếu có lỗi, hãy nêu cách chỉnh sửa. Không tự thêm thông tin mới cho khóa học.
```

**Kết quả đầu ra – Báo cáo kiểm tra tính nhất quán:**

|Tiêu chí kiểm tra|Kết quả|Nhận xét|
|-|-|-|
|Đúng đối tượng|Đạt|Nội dung tập trung vào sinh viên năm nhất từ 18–20 tuổi|
|Thông điệp chính|Đạt|Các nội dung đều hướng đến việc bắt đầu học Python từ cơ bản|
|Thông tin khóa học|Đạt|Giữ đúng tên khóa học Python cơ bản và thời lượng 8 tuần|
|Kênh truyền thông|Đạt|Facebook sử dụng bài viết, TikTok sử dụng video ngắn|
|Lời kêu gọi đăng ký|Đạt|Các bài đăng và video đều hướng người xem đến đăng ký tư vấn|
|Tính liên kết|Đạt|Lịch nội dung đi từ giới thiệu vấn đề đến giới thiệu khóa học và kêu gọi tư vấn|

**Một số điểm cần lưu ý khi triển khai thực tế:**

* Trung tâm cần bổ sung thông tin liên hệ hoặc đường dẫn đăng ký tư vấn chính thức trước khi đăng bài.
* Không nên tự ghi học phí, lịch học hoặc ưu đãi khi chưa có thông tin xác nhận.
* Nên theo dõi số lượt đăng ký tư vấn để đánh giá tiến độ hướng đến mục tiêu 100 lượt.

\---

## 4\. Tổng kết

Qua bài thực hành, em đã sử dụng kỹ thuật Prompt Chaining để chia quá trình xây dựng chiến dịch truyền thông thành 5 bước: phân tích khách hàng mục tiêu, xác định thông điệp, lập kế hoạch nội dung, viết nội dung quảng cáo và kiểm tra tính thống nhất.

Điểm quan trọng của cách làm này là kết quả ở mỗi bước được sử dụng làm đầu vào cho bước tiếp theo. Nhờ vậy, các nội dung trong chiến dịch có sự liên kết với nhau và hạn chế tình trạng AI tự thay đổi thông tin ban đầu.

Qua bài tập, em hiểu thêm cách sử dụng AI để hỗ trợ công việc truyền thông. Tuy nhiên, kết quả do AI tạo ra vẫn cần được đọc và kiểm tra lại trước khi sử dụng thực tế.

\---

**HẾT**

