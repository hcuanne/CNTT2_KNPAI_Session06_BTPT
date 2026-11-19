
# 1. Bối cảnh

Ứng dụng AI để giải thích kiến thức lập trình C bằng kỹ thuật Feynman và tự động chấm bài theo Rubric.

# 2. Yêu cầu đầu ra

- Đề xuất 2 giải pháp Prompting.
- So sánh ưu và nhược điểm.
- Chọn giải pháp tối ưu.
- Chạy thử và trình bày kết quả.

# 3. Bài làm

## Bước 1: Đề xuất 2 Prompt

**Giải pháp 1: Prompt đơn giản**

Bạn là gia sư AI. Hãy giải thích biến trong lập trình C theo kỹ thuật Feynman, sau đó chấm bài lập trình của sinh viên theo thang điểm 10 và nhận xét lỗi sai.

**Giải pháp 2: Prompt chi tiết**

Bạn là gia sư AI chuyên dạy lập trình C cho sinh viên năm nhất.

Yêu cầu:
1. Giải thích biến trong C bằng kỹ thuật Feynman, sử dụng ví dụ dễ hiểu.
2. Phân tích bài làm sinh viên.
3. Chấm điểm theo Rubric:
   - Hiểu kiến thức: 3 điểm.
   - Cú pháp: 3 điểm.
   - Sử dụng biến: 2 điểm.
   - Kết quả: 2 điểm.
4. Nhận xét và hướng dẫn sửa lỗi.
5. Nếu bài làm trống, yêu cầu bổ sung.
6. Nếu code sai, chỉ rõ lỗi.
7. Không tự suy đoán dữ liệu còn thiếu.
8. Nếu không chạy được code, chỉ đánh giá kết quả dự kiến.

Đầu ra: Giải thích, bảng điểm, nhận xét và kết luận.

## Bước 2: So sánh Trade-off

| Tiêu chí | Giải pháp 1 | Giải pháp 2 |
|---|---|---|
| Độ dễ hiểu | Cao | Trung bình |
| Tốn token | Ít | Nhiều hơn |
| Độ chính xác | Trung bình | Cao hơn |
| Chặn lỗi biên | Hạn chế | Tốt |
| Khả năng chấm điểm | Chưa rõ tiêu chí | Có Rubric cụ thể |
| Ưu điểm | Nhanh, dễ dùng | Chi tiết, dễ kiểm soát |
| Nhược điểm | Dễ bỏ sót lỗi | Prompt dài hơn |

## Bước 3: Lựa chọn và chạy thử

**Phương án lựa chọn: Giải pháp 2**

Lý do: Có tiêu chí chấm điểm rõ ràng, xử lý dữ liệu thiếu và giảm nguy cơ AI đưa ra kết quả sai.

**Dữ liệu chạy thử:**

#include <stdio.h>

int main() {
    int tuoi = 18;
    printf("%d", tuoi);
    return 0;
}

**Kết quả phản hồi AI:**

Giải thích Feynman: Biến giống như một chiếc hộp có tên, dùng để chứa dữ liệu. Ví dụ `tuoi` chứa giá trị 18.

| Tiêu chí | Điểm |
|---|---|
| Hiểu kiến thức | 3/3 |
| Cú pháp | 3/3 |
| Sử dụng biến | 2/2 |
| Kết quả dự kiến | 2/2 |
| **Tổng** | **10/10** |

Nhận xét: Code khai báo và sử dụng biến đúng, có đầy đủ thư viện. Kết quả dự kiến là 18.

**Thử trường hợp lỗi:**

Input: Bài làm để trống.

Output: "Chưa có bài làm. Vui lòng cung cấp code C để chấm điểm."


