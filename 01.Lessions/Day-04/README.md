# Tìm hiểu Figma cơ bản

Trong bài học này các bạn cần nắm được một số khái niệm căn bản nhất về Figma bao gồm:

| Giai đoạn               | Nội dung                            |
| ----------------------- | ----------------------------------- |
| 1. Làm quen giao diện   | Frame, Shape, Text, Layer           |
| 2. Auto Layout          | Tạo button, card, header có co giãn |
| 3. Component & Instance | Dùng lại button, form               |
| 4. Variants             | Button nhiều trạng thái             |
| 5. Prototype            | Liên kết các màn hình               |
| 6. Style & System       | Font, màu, layout chuẩn             |
| 7. Libraries & Export   | Dùng lại giữa team, xuất code/dev   |

---

## 🎓 1. Làm quen giao diện

**Chủ đề: Frame, Shape, Text, và Layer**


### 🖥️ 1.1. GIỚI THIỆU GIAO DIỆN FIGMA

Khi bạn mở Figma (bản web hoặc app), bạn sẽ thấy:

| Khu vực                         | Chức năng                                                |
| ------------------------------- | -------------------------------------------------------- |
| **Thanh công cụ trên cùng**     | Chứa các công cụ: Frame, Move, Shape, Text...            |
| **Canvas (vùng trắng giữa)**    | Nơi bạn vẽ và thiết kế giao diện                         |
| **Layer Panel (bên trái)**      | Quản lý các đối tượng đã tạo                             |
| **Thanh thuộc tính (bên phải)** | Chỉnh màu, kích thước, font chữ... cho đối tượng đã chọn |

---

### 🔶 1.2. CÔNG CỤ **FRAME** – KHUNG LÀM VIỆC CHÍNH

#### ✅ Frame là gì?

* Là **khung nền** để bạn thiết kế giao diện
* Mỗi màn hình (ví dụ: màn hình điện thoại) được đặt trong một Frame

#### 📌 Cách tạo Frame:

1. Chọn công cụ **Frame (phím tắt: `F`)**
2. Ở panel bên phải, chọn mẫu có sẵn như:

   * iPhone 14, Desktop, Tablet...
3. Click vào Canvas để chèn Frame

#### 📘 Ví dụ:

* Tạo Frame có kích thước iPhone 14 Pro → đây là màn hình chính của app bạn đang thiết kế

---

### 🔷 1.3. CÔNG CỤ **SHAPE** – VẼ CÁC HÌNH CƠ BẢN

#### ✅ Shape là gì?

* Là các hình cơ bản như: hình chữ nhật, hình tròn, đường kẻ…
* Dùng để tạo nút, khung, thẻ, hình nền...

#### 📌 Cách tạo Shape:

1. Chọn công cụ `Rectangle (R)` hoặc click vào icon hình vuông trên thanh công cụ
2. Kéo chuột để vẽ lên canvas
3. Thay đổi kích thước, màu sắc ở bên phải

#### 📘 Ví dụ:

* Vẽ một hình chữ nhật 300x50px để làm nút "Bắt đầu"

---

### 🔤 1.4. CÔNG CỤ **TEXT** – THÊM CHỮ VÀO GIAO DIỆN

#### ✅ Text là gì?

* Là công cụ để bạn nhập nội dung chữ vào thiết kế như: tiêu đề, mô tả, nút...

#### 📌 Cách tạo Text:

1. Chọn công cụ **Text (`T`)**
2. Click lên canvas để gõ chữ
3. Chỉnh font, size, màu ở bảng bên phải

#### 📘 Ví dụ:

* Gõ dòng chữ "Chào mừng bạn đến với app" và đặt ở giữa màn hình

---

### 📚 1.5. **LAYER PANEL** – QUẢN LÝ CÁC ĐỐI TƯỢNG

#### ✅ Layer là gì?

* Mỗi đối tượng bạn tạo ra (Frame, Text, Shape…) là **một lớp (Layer)**
* Các lớp được sắp xếp theo thứ tự từ **dưới lên trên** (giống như xếp giấy)

#### 📌 Cách dùng:

* Xem danh sách Layer ở bên trái
* Kéo thả để sắp xếp thứ tự
* Click icon 👁 để ẩn/hiện, icon 🔒 để khóa layer

#### 📘 Ví dụ:

* Nếu Text nằm dưới hình chữ nhật → kéo nó lên trên trong Layer Panel để hiện ra

---

## 🎯 2. Auto Layout

### 2.1. **AUTO LAYOUT** LÀ GÌ?

> Là công cụ giúp bạn **bố trí và sắp xếp phần tử một cách tự động**, tương tự như **Flexbox** trong lập trình web.

✅ Khi nào nên dùng Auto Layout?

| Trường hợp            | Lợi ích                        |
| --------------------- | ------------------------------ |
| Nút co giãn theo text | Không cần chỉnh tay chiều rộng |
| Căn giữa icon + text  | Tự động căn và cách đều        |
| Form, danh sách       | Khoảng cách đều, dễ canh chỉnh |

---

### 2.2. CÁCH THÊM AUTO LAYOUT

#### 📌 Cách thực hiện:

1. Chọn phần tử (hoặc nhóm nhiều phần tử)
2. Nhấn tổ hợp phím: `Shift + A` hoặc click nút “+” trong thanh bên phải (Auto Layout)
3. Figma sẽ bao lại phần tử trong một **Auto Layout Frame**

---

### 2.3. THUỘC TÍNH CỦA AUTO LAYOUT

| Thuộc tính                | Ý nghĩa                                                   | Ví dụ                            |
| ------------------------- | --------------------------------------------------------- | -------------------------------- |
| **Direction**             | Chiều sắp xếp: ngang (`horizontal`) hoặc dọc (`vertical`) | Nút = ngang, danh sách = dọc     |
| **Spacing between items** | Khoảng cách giữa các phần tử con                          | 8px, 16px, v.v                   |
| **Padding**               | Khoảng cách từ viền ngoài vào trong                       | 12px, 20px...                    |
| **Alignment**             | Căn giữa, trái, phải, trên, dưới                          | Nút: Center                      |
| **Resizing**              | Cố định hoặc co giãn phần tử                              | Fill container hoặc Hug contents |

---

### 2.4. VÍ DỤ 

#### TẠO BUTTON CO GIÃN THEO TEXT

👣 Các bước:

1. Chọn công cụ `Text` → Nhập chữ: “Mua ngay”
2. Chọn và nhấn `Shift + A` hoặc click phải chọn `Add to Auto Layout` để bật Auto Layout
3. Thêm padding: `8px (top/bottom), 16px (left/right)`
4. Chỉnh màu nền + căn giữa → hoàn thành button chuẩn

#### TẠO DANH SÁCH SẢN PHẨM

👣 Các bước:

1. Tạo 1 khối gồm: ảnh sản phẩm, tiêu đề, giá
2. Chọn các phần tử → Shift + A → sắp xếp dọc
3. Đặt spacing between items = 8px
4. Nhân bản ra nhiều dòng → gói lại bằng Auto Layout cha → danh sách sản phẩm hoàn chỉnh

---



## 3. 🎯 Component & Instance

### 3.1. COMPONENT LÀ GÌ?

> **Component** là một phần tử thiết kế có thể **tái sử dụng nhiều lần** trong toàn bộ dự án.
> Khi bạn thay đổi **Component gốc**, các bản sao (**Instance**) cũng thay đổi theo.

📌 Tưởng tượng thực tế:

| Thực tế                 | Trong Figma   |
| ----------------------- | ------------- |
| Khuôn bánh              | Component gốc |
| Những cái bánh đã nướng | Instance      |

---

### 3.2. LỢI ÍCH KHI DÙNG COMPONENT

| Lợi ích                   | Giải thích                                |
| ------------------------- | ----------------------------------------- |
| ⏱ Tiết kiệm thời gian     | Tạo 1 lần, dùng nhiều lần                 |
| 🎯 Đồng bộ thiết kế       | Chỉnh sửa 1 nơi → cập nhật toàn bộ        |
| 👥 Dễ làm việc nhóm       | Component rõ ràng, dễ chia sẻ             |
| 🧩 Xây dựng design system | Là nền tảng của hệ thống UI chuyên nghiệp |

---

### 3.3. TẠO COMPONENT TRONG FIGMA

👣 Cách thực hiện: Tạo một `Button`

1. Chọn công cụ Text → Nhập chữ: "Button"
2. Chọn toàn bộ phần tử đó → nhấn `Shift + A` để tạo `Auto layout`
3. Điều chỉnh padding, size chữ, màu nền, màu chữ...
4. Nhấn tổ hợp phím: `Ctrl + Alt + K` (Windows) hoặc `Cmd + Option + K` (Mac)
   Hoặc: `Right click` → **"Create component"**
5. Figma sẽ hiển thị khung màu **tím + icon kim cương** – đó là component gốc

---

### 3.4. INSTANCE LÀ GÌ?

> **Instance** là bản sao từ Component gốc. Bạn có thể thay nội dung như text, icon... nhưng vẫn giữ liên kết.

Hay nói một cách dễ hiểu:

- Component Button bạn vừa tạo ở trên được xem là main component (component gốc)
- Bạn sao chép nó ra một phiên bản thứ 2 --> thì nó được gọi là `Instance`
- Khi bạn thay đổi componen gốc -> tất cả các `Instance` sẽ tự động thay đổi theo component gốc.

---

Ví dụ: 

- Sau khi tạo component ở ví dụ trên
- Bạn sao chép ra một bản
- Khi bạn thay đổi màu hoặc padding của Component gốc, **mọi Instance sẽ cập nhật theo**.

---

### 3.5 KHI NÀO NÊN DÙNG COMPONENT?

| Tình huống           | Lý do                           |
| -------------------- | ------------------------------- |
| Nút bấm, input, icon | Lặp lại nhiều lần               |
| Thẻ sản phẩm         | Dễ chỉnh toàn bộ nếu cần update |
| Menu, navbar, header | Xuất hiện ở nhiều màn hình      |

---

### 3.6. BÀI TẬP THỰC HÀNH

#### 📝 Mục tiêu:

Tạo một Component nút bấm có thể tái sử dụng

**Yêu cầu:**

| Thành phần | Chi tiết                                                    |
| ---------- | ----------------------------------------------------------- |
| Nút        | Text = "Mua ngay", màu nền xanh, bo góc, padding 8x16      |
| Component  | Đặt tên là `Button / Primary`                               |
| Instance   | Tạo 3 bản sao: "Đăng nhập", "Thêm vào giỏ", "Đặt hàng ngay" |

**👣 Thực hiện:**

1. Tạo nút với Auto Layout
2. Biến thành Component
3. Tạo Instance và thay đổi nội dung từng nút

---


## 🎯 4. Variants - Biến thể

### 4.1. VARIANTS LÀ GÌ?

> **Variants** là một tính năng trong Figma cho phép bạn gộp **nhiều phiên bản của cùng một Component** (nút, thẻ, input…) thành một **Component set duy nhất**.

| Trước đây               | Với Variants                  |
| ----------------------- | ----------------------------- |
| Tạo từng nút riêng biệt | Gộp các nút vào 1 nhóm có tên |
| Khó quản lý             | Gọn gàng, dễ dùng             |

---

### 4.2. KHI NÀO NÊN DÙNG VARIANTS?

| Tình huống                 | Biến thể cần                      |
| -------------------------- | --------------------------------- |
| Button có nhiều trạng thái | Default, Hover, Disabled, Loading |
| Button có nhiều kiểu       | Primary, Secondary, Outline       |
| Icon có trạng thái         | On/Off, Active/Inactive           |
| Form field                 | Focused, Error, Filled, Empty     |

---

### 4.3. CÁCH TẠO VARIANTS TRONG FIGMA

👣 Các bước:

1. Tạo một Component gốc (VD: Button)
2. Duplicate (copy) ra nhều `instances` và thay đổi để có các trạng thái khác nhau
3. Biến tất cả các `instances` thành component.

    Lưu ý: Trong panel phải, đặt tên các Property:

   * `Type = Primary / Secondary / Outline`
   * `State = Default / Hover / Disabled`

4. Chọn tất cả các Component → click **Combine as Variants** (nút ở góc phải thanh công cụ)
5. Figma sẽ gộp lại thành **1 Component set có nhiều Variants**


---

### 4.4 GIẢI THÍCH KHÁI NIỆM

| Khái niệm     | Giải thích                         |
| ------------- | ---------------------------------- |
| Component Set | Nhóm chứa nhiều biến thể           |
| Variant       | Mỗi biến thể là 1 Component nhỏ    |
| Property      | Tên thuộc tính phân loại biến thể  |
| Value         | Giá trị cụ thể (VD: State = Hover) |

---

### 4.5. VÍ DỤ: BUTTON VỚI BIẾN THỂ

| Property | Value                    |
| -------- | ------------------------ |
| Type     | Primary, Secondary       |
| State    | Default, Hover, Disabled |

📌 Tổng cộng: 2 Type × 3 State = **6 biến thể**

---

### 4.6. QUY TẮC ĐẶT TÊN PROPERTY

* Nên viết theo cặp: `Property = Value`
* Tên rõ ràng, dễ hiểu

| Đúng           | Sai                                |
| -------------- | ---------------------------------- |
| Type = Primary | "primary" (không rõ thuộc tính gì) |
| State = Hover  | "hovered" (không nhất quán)        |

---

### 4.7. CÁCH SỬ DỤNG VARIANTS TRONG FILE KHÁC

1. Vào `Assets` → Kéo Component vào màn hình
2. Chọn instance → nhìn panel phải sẽ có dropdown để đổi:

   * `Type` → Chọn Primary, Secondary...
   * `State` → Chọn Hover, Disabled...

👉 Bạn chỉ cần kéo 1 nút vào → đổi qua lại các biến thể nhanh chóng.

---

### 4.8. BÀI TẬP THỰC HÀNH

📝 Mục tiêu:

Tạo một nút `Button` có 2 loại và 3 trạng thái bằng **Variants**

| Property | Value                    |
| -------- | ------------------------ |
| Type     | Primary, Outline         |
| State    | Default, Hover, Disabled |

👣 Gợi ý thực hiện:

1. Tạo 6 nút bằng Auto Layout
2. Đặt tên rõ ràng (VD: Primary / Hover)
3. Chọn tất cả → Combine as Variants
4. Tạo Property trong panel phải:

   * Property 1: Type
   * Property 2: State

---

## 🎯 5. Prototype


### 5.1. PROTOTYPE LÀ GÌ?

> **Prototype** là tính năng giúp bạn mô phỏng lại **trải nghiệm người dùng** khi họ thao tác với sản phẩm như click, chuyển màn hình, vuốt, mở popup…

👉 Giúp bạn **trình bày ý tưởng**, **kiểm thử giao diện**, và **trình diễn với khách hàng hoặc lập trình viên**.

---

### 5.2 TẠI SAO CẦN PROTOTYPE?

| Lý do                     | Lợi ích                          |
| ------------------------- | -------------------------------- |
| 🎯 Trực quan hóa ý tưởng  | Người xem hiểu ngay luồng UX     |
| 🧪 Thử nghiệm sớm         | Kiểm tra trước khi lập trình     |
| 👥 Giao tiếp tốt với team | Dev hiểu đúng logic luồng chuyển |

---

### 5.3. GIAO DIỆN PROTOTYPE

Chuyển sang tab **Prototype** (ở thanh phải) sẽ có:

| Thành phần  | Ý nghĩa                                         |
| ----------- | ----------------------------------------------- |
| Interaction | Chọn hành động (On Click, Hover, Key press...)  |
| Navigation  | Chọn kiểu chuyển (Navigate to, Open Overlay...) |
| Animation   | Hiệu ứng (Instant, Dissolve, Smart Animate...)  |
| Trigger     | Sự kiện xảy ra (Click, Hover, Drag...)          |

---

### 5.4. CÁCH TẠO PROTOTYPE CƠ BẢN

👣 Các bước:

1. **Tạo 2 Frame** (VD: Trang Đăng nhập & Trang Chủ)
2. Chọn nút “Đăng nhập” → vào tab `Prototype`
3. Kéo mũi tên xanh **nối đến frame kế tiếp (Trang Chủ)**
4. Cấu hình:

   * **Trigger:** On Click
   * **Action:** Navigate to
   * **Animation:** Smart Animate (hoặc Instant)

---

VÍ DỤ THỰC TẾ – ỨNG DỤNG ĐĂNG NHẬP

| Frame   | Nội dung                                |
| ------- | --------------------------------------- |
| Trang 1 | Giao diện đăng nhập với nút “Đăng nhập” |
| Trang 2 | Trang chủ với tiêu đề “Chào bạn!”       |

👉 Khi click vào nút → chuyển từ Trang 1 → Trang 2 với hiệu ứng mượt.

---

### 5.6. LOẠI TƯƠNG TÁC THƯỜNG DÙNG

| Tương tác              | Ứng dụng                            |
| ---------------------- | ----------------------------------- |
| On Click → Navigate to | Chuyển màn hình                     |
| On Hover               | Đổi trạng thái nút                  |
| Open Overlay           | Mở popup (VD: modal giỏ hàng)       |
| Swap with              | Chuyển giữa 2 frame nhanh (VD: tab) |
| Scroll to              | Cuộn tới vị trí trong cùng 1 frame  |

---

### 5.7 CÁCH XEM PROTOTYPE

* Nhấn nút ▶️ **“Present”** ở góc trên phải để xem thử
* Bạn có thể **click thử, chuyển cảnh, test logic**
* Dùng phím **← / →** để chuyển frame theo thứ tự

---

### 5.8 BÀI TẬP THỰC HÀNH

📝 Mục tiêu: Tạo mô phỏng ứng dụng chuyển màn hình

| Frame | Nội dung                                         |
| ----- | ------------------------------------------------ |
| 1     | Trang Đăng nhập (form + nút “Đăng nhập”)         |
| 2     | Trang Chủ (chữ “Chào mừng”)                      |
| 3     | Popup thông báo “Đăng nhập thành công” (Overlay) |

👣 Hướng dẫn:

1. Tạo 3 Frame
2. Dùng **On Click → Navigate to** để chuyển từ Trang 1 → Trang 2
3. Thêm 1 frame nhỏ làm popup → dùng **Open overlay**
4. Trình diễn bằng nút **Present**

---

## 🎯 6. Style & System

## 🎯 7. Libraries & Export