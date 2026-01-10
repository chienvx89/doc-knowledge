# Giới thiệu GitHub Copilot cho DEV Team

---


## 🎤 1 – Giới thiệu

**GitHub Copilot**  
**Pair Programmer cho DEV Team**

*Code nhanh hơn – Ít lặp hơn – Đỡ mệt hơn*

---


## 😵 2 – Vấn đề quen thuộc khi lập trình

### Nội dung
- Viết nhiều code lặp lại (CRUD, DTO, mapping)
- Đọc code cũ / code người khác
- Ngại viết unit test
- Refactor rất tốn thời gian

---


## 🎯 3 – Mục tiêu buổi chia sẻ

### Nội dung

- **Hiểu GitHub Copilot làm được gì**
  1. Gợi ý code theo ngữ cảnh
  2. Sinh code lặp & boilerplate rất tốt (các mẫu hiện tại của dự án)
  3. Viết unittest hoặc test case
  4. Đọc & giải thích code
  5. Refactor Code

- **Biết dùng Copilot cho C# hiệu quả**
  - Copilot tốt hay dở phụ thuộc vào cách ae "nói chuyện" với nó

  1. **Comment càng rõ → code càng đúng** (https://prnt.sc/SrocDYiIsf_b)
     - ❌ Comment mơ hồ:
       ```csharp
       // get data
       ```
     - ✅ Comment tốt: (càng chi tiết càng tốt)
       ```csharp
       // get latest by organizationId, ignore deleted records
       ```

  2. **Đặt tên hàm & biến có ý nghĩa** (https://prnt.sc/ZWRN5ZVjM-tG)
     - Copilot học rất nhiều từ tên
     - ❌ `var d; var tmp`
     - ✅ `var latestProduct;`

  3. **Dùng Copilot cho đúng loại việc**
     - ✅ NÊN dùng:
       - Controller / Service boilerplate
       - LINQ / SQL query
       - DTO / mapping
       - Unit test
       - Refactor code
       - Write document

  4. **Luôn review code Copilot sinh**
     - Checklist luôn phải đặt ra:
       - Có đúng yêu cầu không?
       - Có xử lý null / edge case không?
       - Có tối ưu performance không?
       - Có vi phạm security không?
     - 👉 Xem Copilot như dev junior

- **Tránh được các hiểu lầm nguy hiểm**

  1. **Hiểu lầm #1: "Copilot lúc nào cũng đúng"**
     - ❌ SAI
     - Copilot có thể:
       - Sinh SQL không tối ưu
       - Quên index
       - Quên filter quan trọng
       - Viết LINQ tốn memory...
     - ⇒ Dev phải review

  2. **Hiểu lầm #2: "Copy là xong"**
     - Copy code mà:
       - Không hiểu logic
       - Không test
       - Không benchmark
     - ⇒ Dễ sinh bug & tech debt

  3. **Hiểu lầm #3: "Copilot thay dev senior"**
     - Hiện tại thì chưa
     - Copilot:
       - Không hiểu hệ thống tổng thể
       - Không chịu trách nhiệm
     - ⇒ Nó tăng tốc, không thay thế

  4. **Hiểu lầm #4: "Copilot viết gì cũng an toàn"**
     - ❌ Sai
     - Có thể sinh code:
       - Không thread-safe
       - Không kiểm soát input
       - Không tối ưu DB
     - ⇒ Security & performance vẫn là việc của dev

---

## 💡 4 – Kinh nghiệm thực tế

### Nội dung

**Công cụ & môi trường**
- Dùng VS Code + extension GitHub Copilot ⇒ ngon hơn Visual Studio (nhẹ, nhanh, ít lỗi)
- Sử dụng model hợp lý cho từng loại công việc

**Bảng chọn model theo loại công việc** (https://prnt.sc/6MR6qLtOe-5r)

| Nhiệm vụ               | Model nên dùng   | Ghi chú              |
| ---------------------- | ---------------- | -------------------- |
| Inline code completion | Miễn phí / nhẹ   | Nhanh, đủ dùng       |
| CRUD / DTO / mapping   | Miễn phí / nhẹ   | Không cần model mạnh |
| Explain code           | Trung cấp (paid) | Dùng nhiều nhất      |
| Refactor code          | Trung → Cao      | Tùy độ phức tạp      |
| Unit test              | Trung cấp        | Sinh skeleton        |
| SQL / LINQ phức tạp    | Cao cấp          | Luôn review          |
| Debug lỗi khó          | Cao cấp          | Đáng tiền            |

**Cách tương tác hiệu quả**
- Kiên nhẫn luyện tập & tìm cách tương tác với Copilot
- Nếu vấn đề phức tạp, cần chia nhỏ ra từng phần để Copilot dễ hiểu hơn

**Cấu hình MCP Server**
- Kết nối: VS Code → MCP Server → API → Cơ sở dữ liệu (https://prnt.sc/wWIaQqLwacuG)
- Cấu hình file JSON trong VS Code (https://prnt.sc/NS3eflhmcg-e)
- Ví dụ: MCP kết nối với SQL (https://prnt.sc/5IVgoVQ8kPuW)

---


## 📚 5 – Các khái niệm hay ho

### Nội dung
- **AI pair programming**: Lập trình cùng AI
- **Large Language Model (LLM)**: Mô hình ngôn ngữ lớn
- **Training data**: Dữ liệu huấn luyện
- **Context window**: Cửa sổ ngữ cảnh
- **Prompt**: Lời nhắc
- **Prompt engineering**: Kỹ thuật tạo lời nhắc hiệu quả
- **MCP server**: Máy chủ Model Context Protocol
- **Token**: Đơn vị ngôn ngữ nhỏ nhất
- **Fine-tuning**: Tinh chỉnh mô hình
- **Agent**: Đại lý AI

---


## 🎯 Kết luận

### Nội dung

**"GitHub Copilot giống một dev junior code rất nhanh. Dùng tốt thì tiết kiệm thời gian ⇒ dùng ẩu thì tạo thêm việc, tốn chi phí"**
