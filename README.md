# 🌐 Chaos Web Playground

> Một **game** trên GitHub: điều gì sẽ xảy ra nếu mọi người cùng nhau "đóng góp" vào một trang web mà **không ai quản lý**?

Xem kết quả trực tiếp tại: [https://openchaosweb.github.io/](https://openchaosweb.github.io/)

GitHub Pages sẽ tự động cập nhật sau mỗi lần **merge PR**.

---

## 🎮 Luật chơi

Bạn có thể **fork → thêm thứ gì đó → gửi pull request**.  

Nếu PR của bạn **không conflict**, nó sẽ được merge — **dù xấu hay đẹp, đúng hay sai**.

1. Toàn bộ trang web chỉ có **một file duy nhất: `index.html`**.  
2. Bên trong có **100 slot** (từ `#slot-001` đến `#slot-100`).  
3. Mỗi người có thể thêm hoặc sửa **một slot bất kỳ**.  
4. **Nếu PR conflict**, PR đó bị bỏ qua (người khác nhanh tay hơn 😎).  
5. Không có ai “quản lý nội dung” — chỉ cần không quá bậy, code hợp lệ, không phá trang hoàn toàn.

---

## 🧱 Cách tham gia

1. Fork repo này.  
2. Chọn một slot trống trong `index.html`, ví dụ `slot-042`.  
3. Thêm nội dung của bạn vào các slot:
   ```html
   <!-- == SLOT 41 == -->
   <div id="slot-042" class="slot">
     <style>
       /* Mọi CSS phải được scope theo ID của slot */
       #slot-042 { background:#111; color:#0f0; padding:12px; }
       #slot-042 h3 { margin:0; font-size:18px; }
     </style>

     <h3>Xin chào từ slot 42!</h3>
     <p>Đây là phần của tôi 😎</p>
     <button onclick="alert('Hi from slot 42')">Bấm tôi</button>
   </div>
   ```
4. Commit & Push → Gửi Pull Request về repo chính.
5. Nếu PR không conflict, tôi sẽ merge, trang web sẽ tự động cập nhật trên GitHub Pages. 🎉

# 📜 Quy Tắc Tham Gia

## 🎨 Quy tắc CSS

Để trang không bị sập trong 3 phút đầu:

* **🔒 BẮT BUỘC:** Mọi **selector** phải bắt đầu bằng **ID slot** của bạn.
    * *(Ví dụ: `#slot-042 h1 { ... }`)*.
* **🚫 CẤM:** Sử dụng selector **toàn cục** (`body`, `html`, `*`, `.slot`, `:root`, …).
* **🚫 CẤM:** Làm biến mất **layout chính** (`display:none` trên `#slot-id` hoặc `body`).
* **⚡ ĐƯỢC PHÉP:** **Inline style** hoặc thẻ `<style>` trong slot.
* **💡 GỢI Ý:** Nếu muốn tách biệt hoàn toàn, bạn có thể **nhúng `<iframe>`** riêng trong slot.

***

## 🧩 Quy tắc JavaScript

JS được phép, nhưng **đừng phá trình duyệt** người khác.

* Dùng `console.log()` thay vì `alert()` nếu bạn muốn lịch sự 😆.
* Mọi **biến** nên được đặt tên riêng để tránh đụng nhau (*`slot42Counter`, `slot99Timer`, ...*).

***

## 🧠 Mục Tiêu

* Xem cộng đồng tạo ra một trang web **ngẫu nhiên, điên rồ** nhưng **đẹp** đến mức nào.
* Thử nghiệm xem một dự án **không có quản lý** sẽ **tiến hóa** ra sao.
* **Vui là chính**. 🎉

***

## ❤️ Cảm Ơn

Nếu bạn tham gia, bạn đã góp phần vào một **thí nghiệm hỗn loạn vĩ đại** của web.

Cảm ơn vì đã phá — à không, đã **đóng góp** 😁

***

## 📜 Giấy Phép

**MIT** — vì ngay cả hỗn loạn cũng cần tự do.
