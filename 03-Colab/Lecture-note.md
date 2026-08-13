Trực quan hóa dữ liệu
==================

**Dr. Cuong Nguyen**
- CSO, LOBI Corp.
- [cuongnguyen@lobi.vn](mailto:cuongnguyen@lobi.vn) — 0916.110.333
- https://github.com/juhuvn
- 2026-08-18

----

# 1 Giới thiệu về Trực quan hóa Dữ liệu (Data Visualization)

## 1.1 Trực quan hóa dữ liệu
- Biểu diễn dữ liệu dưới dạng đồ thị, biểu đồ, bản đồ,...
- Một câu chuyện được truyền đạt qua hình ảnh
- Thể hiện các mô hình (patterns), xu hướng (trends), và sự bất thường (anomalies) trong dữ liệu

![Trực quan hóa dữ liệu](./imgs/introduction-to-data-visualization.png)

*Hình 1: Trực quan hóa dữ liệu*

## 1.2 Các loại biểu đồ
Có sáu loại biểu đồ chính:
- **So sánh (Comparisons)**: Các dạng trực quan để so sánh các danh mục, ví dụ như biểu đồ cột (bar charts), biểu đồ cột nhóm (grouped bars), biểu đồ bong bóng (bubble charts), biểu đồ radar, và biểu đồ cột ngang.
- **Xu hướng (Trends)**: Các biểu đồ hiển thị sự thay đổi theo thời gian hoặc trình tự, bao gồm biểu đồ đường (line charts), biểu đồ vùng (area charts), biểu đồ dòng chảy (stream graphs), biểu đồ tần suất (histograms), và biểu đồ hộp (box plots).
- **Thành phần trong Tổng thể (Part to Whole)**: Các biểu đồ minh họa cách từng thành phần đóng góp vào tổng thể, chẳng hạn như biểu đồ tròn (pie charts), biểu đồ cột xếp chồng (stacked bars), biểu đồ vùng xếp chồng (stacked areas), sơ đồ cây (tree maps), biểu đồ đo lường (gauges, meters), và biểu đồ dạng lưới (waffle plots).
- **Tương quan (Correlations)**: Trực quan hóa để khám phá mối quan hệ giữa các biến, bao gồm biểu đồ phân tán (scatterplots), bản đồ nhiệt (heatmaps), và tọa độ song song (parallel coordinates).
- **Mối quan hệ và Kết nối (Relationships and Connections)**: Các biểu đồ làm nổi bật các liên kết hoặc dòng chảy, chẳng hạn như biểu đồ dòng chảy (alluvial diagrams) và sơ đồ cây.
- **Bản đồ (Maps)**: Trực quan hóa dữ liệu không gian, bao gồm bản đồ nhiệt phân vùng (choropleth maps), bản đồ ký hiệu tỷ lệ (proportional symbol maps), và các đường kết nối.

![Các loại biểu đồ](./imgs/01-chart-types.png)
*Hình 2: Các loại biểu đồ*

## 1.3 Các công cụ Trực quan hóa Dữ liệu phổ biến
- Microsoft Excel
- Tableau
- Microsoft Power BI
- Google Looker Studio
- Python (Matplotlib, Seaborn)
- R (ggplot2 & Tidyverse)

## 1.4 R (ggplot2) so với Python (Matplotlib/Seaborn)
- **R**: Chuyên gia về Phân tích & Đồ họa
- **Python**: Con dao quân đội Thụy Sĩ đa năng

**Chọn R nếu:**
- Công việc hàng ngày của bạn chủ yếu là **phân tích dữ liệu thực nghiệm** (RNA-seq, proteomics, metabolomics, v.v.).
- Bạn cần tạo nhiều **đồ họa phức tạp, chất lượng cao cho các báo cáo và công bố khoa học**.
- Bạn muốn tận dụng hệ sinh thái **Bioconductor** khổng lồ và các phương pháp thống kê tiên tiến.
- Bạn đánh giá cao cách tiếp cận logic và có cấu trúc của **"Ngữ pháp Đồ họa" (Grammar of Graphics)**.

**Chọn Python nếu:**
- Trực quan hóa chỉ là **một bước trong một quy trình lớn hơn** liên quan đến xử lý hình ảnh, học máy, tự động hóa hoặc phát triển phần mềm.
- Bạn cần **tích hợp các phân tích của mình vào một trang web hoặc ứng dụng**.
- Bạn đã quen thuộc với Python và muốn **giữ mọi thứ trong một môi trường**.
- Bạn làm việc nhiều với các mô hình học sâu cho các vấn đề sinh học (ví dụ: AlphaFold).

**Lời khuyên:** Một nhà tin sinh học giỏi thường biết cả hai. Họ có thể sử dụng **R để khám phá, phân tích thống kê và vẽ biểu đồ nhanh**, sau đó chuyển sang **Python để xây dựng các quy trình tự động hoặc các mô hình phức tạp**.

# 2. Matplotlib và Seaborn là gì?

## 2.1 Matplotlib
- Là thư viện cốt lõi (low-level) để vẽ biểu đồ 2D trong Python.
- Cung cấp khả năng kiểm soát chi tiết đến từng yếu tố của biểu đồ (trục, nhãn, màu sắc, chú giải, v.v.).
- Rất mạnh mẽ và linh hoạt nhưng đôi khi cần viết nhiều mã (code) để tạo ra một biểu đồ phức tạp hoặc có tính thẩm mỹ cao.
- Thường được sử dụng làm nền tảng (backend) cho các thư viện đồ họa cấp cao hơn.

## 2.2 Seaborn
- Là thư viện trực quan hóa dữ liệu cấp cao (high-level) được xây dựng dựa trên nền tảng của Matplotlib.
- Cung cấp giao diện lập trình (API) trực quan và dễ sử dụng hơn để vẽ các đồ thị thống kê.
- Tích hợp chặt chẽ và tương tác rất tốt với cấu trúc dữ liệu `DataFrame` của thư viện Pandas.
- Cung cấp sẵn các chủ đề (themes) mặc định và bảng màu (color palettes) đẹp mắt, giúp tạo đồ thị chuẩn xuất bản chỉ với một vài dòng mã.
- Có khả năng tự động thực hiện một số phép tính toán thống kê (ví dụ: vẽ đường hồi quy, tính khoảng tin cậy) trong quá trình vẽ đồ thị.

## 2.3 Khi nào dùng thư viện nào?
- **Ưu tiên sử dụng Seaborn** khi bạn muốn nhanh chóng khám phá dữ liệu, vẽ các đồ thị thống kê phức tạp (ví dụ: phân phối, quan hệ tương quan, so sánh nhóm) từ dữ liệu dạng bảng (DataFrame) một cách dễ dàng và thẩm mỹ.
- **Sử dụng Matplotlib** khi bạn cần can thiệp sâu, tinh chỉnh các chi tiết cụ thể của đồ thị (ví dụ: kích thước hình ảnh, phông chữ, vị trí chính xác của các chú giải), hoặc khi bạn muốn tạo ra những biểu đồ đặc thù, bố cục phức tạp không được hỗ trợ sẵn trong Seaborn.
- **Trong thực tế:** Các nhà phân tích thường kết hợp cả hai. Họ dùng Seaborn để dựng khung đồ thị chính cho nhanh và đẹp, sau đó gọi các hàm của Matplotlib (thông qua đối tượng `Axes` hoặc `Figure`) để tinh chỉnh lại đồ thị cho đúng ý muốn.

# 3 Giới thiệu về Vibe Coding trong Trực quan hóa Dữ liệu

## 3.1 Vibe Coding là gì?
- **Vibe coding** là phong cách lập trình hiện đại, nơi người lập trình sử dụng Trí tuệ Nhân tạo (các trợ lý AI/LLM như Gemini, ChatGPT, Claude, Antigravity, Cursor,...) để tự động sinh mã nguồn thông qua các câu lệnh bằng ngôn ngữ tự nhiên (prompts).
- Thay vì phải ghi nhớ từng cú pháp (syntax) phức tạp của Matplotlib hay Seaborn, bạn tập trung vào việc mô tả **ý đồ phân tích (intent)** và **kết quả mong muốn**.
- Người làm phân tích dữ liệu chuyển vai trò từ người gõ từng dòng code sang **người điều phối (director)** và **người kiểm định (reviewer)**.

## 3.2 Lợi ích của Vibe Coding khi Trực quan hóa Dữ liệu
- **Tốc độ thử nghiệm cực nhanh (Rapid Prototyping)**: Nhanh chóng tạo ra nhiều dạng biểu đồ khác nhau để tìm ra cách truyền đạt dữ liệu tối ưu nhất.
- **Giảm rào cản cú pháp**: Không cần mất thời gian tra cứu tài liệu (documentation) cho các tham số tinh chỉnh giao diện phức tạp (như tùy biến trục, bảng màu, chú thích, font chữ,...).
- **Tập trung vào Tư duy Phân tích (Data Storytelling)**: Dành nhiều thời gian hơn để đọc hiểu ý nghĩa dữ liệu và rút ra tri thức (insights) thay vì sửa lỗi cú pháp.

## 3.3 Quy trình Vibe Coding hiệu quả
1. **Cung cấp ngữ cảnh dữ liệu**: Mô tả cho AI biết cấu trúc dữ liệu của bạn (tên cột, kiểu dữ liệu, một vài dòng mẫu).
2. **Mô tả mục tiêu trực quan hóa**: Nêu rõ bạn muốn xem xét mối quan hệ nào (xu hướng, so sánh, thành phần, tương quan,...).
3. **Thực thi và quan sát**: Chạy đoạn mã do AI tạo ra trong Google Colab / Jupyter Notebook để xem biểu đồ kết quả.
4. **Tinh chỉnh tinh tế (Iterative Prompting)**: Yêu cầu AI chỉnh sửa các chi tiết cụ thể (ví dụ: *"Đổi màu dải phân bố sang xanh lam, xoay nhãn trục X 45 độ và thêm đường kẻ lưới nét đứt"*).
5. **Lưu ý quan trọng**: Biểu đồ AI vẽ ra có thể rất đẹp nhưng vẫn có nguy cơ sai lệch giá trị hoặc nhầm lẫn logic phân tích. Người làm phân tích **luôn phải đối chiếu và kiểm tra tính chính xác của dữ liệu**.

## 3.4 Làm gì khi chưa có ý đồ phân tích?
Khi đứng trước một tập dữ liệu mới mà chưa biết bắt đầu từ đâu hoặc chưa có sẵn câu hỏi/giả thuyết cụ thể, bạn có thể tận dụng AI theo các bước sau để tìm kiếm ý tưởng:

1. **Yêu cầu AI tóm tắt và khám phá tổng quan (EDA - Exploratory Data Analysis)**:
   - Cung cấp cho AI kết quả của `df.info()`, `df.describe()` hoặc 5 dòng đầu `df.head()`.
   - Đặt câu lệnh: *"Hãy tóm tắt đặc điểm tập dữ liệu này, chỉ ra các biến quan trọng, giá trị thiếu (missing values) và gợi ý các hướng khám phá ban đầu."*
2. **Nhờ AI đề xuất các câu hỏi và giả thuyết phân tích**:
   - Đặt câu lệnh: *"Dựa vào cấu trúc dữ liệu trên, hãy gợi ý cho tôi 5 câu hỏi phân tích có giá trị nhất hoặc các giả thuyết có thể kiểm định."*
3. **Tạo đồ thị tổng quan tự động (Overview Dashboard / Quick Scan)**:
   - Yêu cầu AI sinh code vẽ biểu đồ Ma trận Tương quan (Correlation Heatmap) cho các biến số, hoặc Ma trận Phân tán (Pairplot) để nhìn nhanh mối liên hệ giữa các cặp biến.
   - Yêu cầu AI gợi ý và vẽ 3-4 biểu đồ cơ bản nhất đại diện cho các khía cạnh khác nhau của dữ liệu.
4. **Đào sâu theo vệt phát hiện (Drill-down)**:
   - Khi nhìn thấy điểm bất thường (outlier), sự lệch phân bố (skewness) hoặc một xu hướng lạ từ biểu đồ tổng quan, hãy chụp hình hoặc mô tả lại điểm đó cho AI và yêu cầu đào sâu: *"Tôi thấy cột X có phân bố bị lệch phải rất mạnh, hãy gợi ý biểu đồ phân rã hoặc phân nhóm cột X theo cột Y để giải thích nguyên nhân."*



