# Understanding Responsive Web Design

Tìm hiểu cơ chế hoạt động của một website có tính năng Responsive.

## 💛 What is Responsive User Interface Design ?

**Responsive User Interface Design** là một phương pháp thiết kế web trong đó giao diện thích ứng với bố cục của thiết bị để tăng cường khả năng sử dụng, điều hướng và tìm kiếm thông tin. Sự linh hoạt này có thể nhờ vào các `media queries`, cho phép thiết kế tự động điều chỉnh để phù hợp với không gian trình duyệt và đảm bảo tính nhất quán của nội dung trên các thiết bị, cũng như các yếu tố thiết kế được định kích cỡ bằng đơn vị tương đối (%).

### 💥 Lợi ích mang lại cho người dùng

- Điều hướng mượt mà
- Đọc dễ dàng, không bị mất nội dung
- Giảm thao tác cuộn, thu phóng
- Tăng trải nghiệm người dùng

---

## 💛 Cascading Style Sheets

Responsive Web Design (RWD) đã phát triển từ việc chỉ đơn giản điều chỉnh giao diện cho nhiều kích thước màn hình thành một phương pháp toàn diện tối ưu hóa trải nghiệm người dùng. Từ khi được giới thiệu vào năm 2010 bởi Ethan Marcotte, RWD đã áp dụng các công nghệ như **fluid grids**, **flexible images**, và **media queries**. 

Sau đó, nó tiến xa hơn với thiết kế **mobile-first**, **responsive images**, và **CSS Grid/Flexbox**, tập trung vào hiệu suất và trải nghiệm nhất quán. Hiện nay, RWD tích hợp các xu hướng như **PWAs**, **variable fonts**, **dark mode**, và tối ưu hóa hiệu suất với **Core Web Vitals**, trở thành nền tảng quan trọng của thiết kế web hiện đại.

## 💛 Fundamental Techniques for RWD ?

Các kỹ thuật triển khai

### 💥 CSS3 Media Queries and Screen Resolutions

```css
/* Màn hình tối thiểu 769px thì màu trắng */
@media only screen and (min-width: 769px) {
  body {
    background-color: #fff;
  }
}
/* Màn hình tối đa 768px thì màu lightblue */
@media only screen and (max-width: 768px) {
  body {
    background-color: lightblue;
  }
}
/* Màn hình tối đa 457px thì màu orange */
@media only screen and (max-width: 457px) {
  body {
    background-color: orange;
  }
}
```


Xem thêm: https://www.w3schools.com/css/css_rwd_mediaqueries.asp

### 💥 Flexible images

Đối với hình ảnh. Tùy vào từng trường hợp cụ thể.

Còn hẫu hết để hình ảnh tương thích được với các kích thước màn hình khác nhau thì bạn cần cho nó một thuộc tính

```css
img{
    max-width: 100%,
    height: auto
}
```
Xem thêm: https://www.w3schools.com/css/css_rwd_images.asp


### 💥 Fluid, Proportion-based Grids

Grids trong thiết kế website responsive là cách thức chia nội dung theo trục ngang thành các cột nhỏ thông thường là 12 cột (Column Grid).

Dựa vào các cột này. Người ta bố trí nội dung nằm ở đâu trong 12 cột đó.

Xem thêm: https://www.w3schools.com/css/css_rwd_grid.asp


Giới thiệu về 2 thư viện hỗ trợ phổ biến: 

#### Bootstrap 5

Doc: https://getbootstrap.com/

#### TailwindCss

Doc: https://tailwindcss.com/

---

## 💛 What is Progressive Enhancement?

- Giao diện người dùng có thể được cấu hình từ 3 lớp  (layer)

![layer](img/Progressive_enhancement_web_design_pyramid_(HTML,_CSS,_JS).svg)

- Base cơ bản dựa trên HTML, CSS là chủ yếu

- Ngoài ra chúng ta có thể sử dụng lớp JS để can thiệp vào kết quả hiển thị. Ví dụ: Thêm mới, Xóa, Cập nhật... dẫn đến thay đổi kết quả hiển thị.

Ví dụ 3 lớp:

Lớp HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Simple Form</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <form id="contactForm">
    <label for="name">Name:</label>
    <input type="text" id="name" name="name" required>
    
    <label for="email">Email:</label>
    <input type="email" id="email" name="email" required>
    
    <button type="submit">Submit</button>
  </form>
  <script src="script.js"></script>
</body>
</html>

```

Lớp CSS

```css
/* styles.css */
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
  background-color: #f9f9f9;
}

form {
  background: #ffffff;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

label {
  display: block;
  margin: 10px 0 5px;
}

input {
  width: 100%;
  padding: 8px;
  margin-bottom: 10px;
  border: 1px solid #ddd;
  border-radius: 4px;
}

button {
  background-color: #007BFF;
  color: #ffffff;
  padding: 10px 15px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

button:hover {
  background-color: #0056b3;
}

```

Lớp Javascaript

```js
// script.js
document.getElementById('contactForm').addEventListener('submit', function (e) {
  e.preventDefault();
  
  const name = document.getElementById('name').value;
  const email = document.getElementById('email').value;
  
  if (name && email) {
    alert(`Thank you, ${name}! We will contact you at ${email}.`);
  } else {
    alert('Please fill out all fields.');
  }
});
```

---

## 💛 Difference Between Graceful Degradation and Progressive Enhancement



![Enhancement-vs-Degradation](img/Enhancement-vs-Degradation.png)

### 💥 Graceful Degradation

**Graceful Degradation** là một triết lý thiết kế tập trung vào việc xây dựng một website/ứng dụng tập trung vào các thiết bị màn hình lớn (Desktop) làm cốt lõi.

Nhưng khi người dùng sử dụng các thiết bị có kích thước màn hình nhỏ hơn (Tablet, Mobile) thì vẫn hỗ trợ bằng cách hiển thị đáp ứng (repsonsive).  Mục tiêu là đảm bảo rằng người dùng cuối cùng vẫn có thể truy cập và sử dụng nội dung hoặc chức năng cốt lõi, mặc dù họ có thể không nhận được trải nghiệm tốt nhất như trên Desktop

### 💥 Progressive Enhancement

Đơn giản bạn chỉ cần hiểu nó ngược lại.

---

Nhưng trên thực tế người ta sử dụng song song 2 phương pháp. Để nó bổ sung cho nhau. Suy cho cùng thì Mục tiêu là phải tăng tính trải nghiệm người dùng.

---

## 💛 **Quy trình triển khai thiết kế Responsive**  

Responsive Design Workflow được chia thành bốn giai đoạn chính, mỗi giai đoạn có vai trò cụ thể để đảm bảo sản phẩm thiết kế thân thiện với mọi thiết bị.


### **💥 1. Discover (Khám phá)**  

Giai đoạn này tập trung vào việc hiểu nhu cầu của dự án, người dùng, và mục tiêu kinh doanh.  

#### **Kick-off and Project Charter** 

- Khởi động dự án
- Hỗ trợ thiết lập các giao thức truyền thông
- Thiết lập các quy tắc, mục tiêu, mốc thời gian hoàn thành, phạm vi và vai trò cũng như kết quả kỳ vọng.

#### **Project Analysis - Phân tích dự án** 

- Giúp xác định các yêu cầu của dự án, từ góc độ kỹ thuật, sáng tạo và tổ chức

#### **Content and Search Strategy - Nội dung và Chiến lược tìm kiếm**

- Giúp tạo sơ đồ trang web cho một dự án và hiển thị vị trí của mọi thứ. 
- Nó cũng giúp phát triển một tài liệu tóm tắt các phương pháp hay nhất cho Tối ưu hóa công cụ tìm kiếm

#### **Strategic Direction and Planning - Định hướng và Kế hoạch Chiến lược**

Giúp tổng hợp tất cả thông tin tìm thấy trong giai đoạn khám phá thành một tài liệu ngắn gọn nêu rõ các chiến lược tìm kiếm, nội dung, kỹ thuật và sáng tạo

### **💥 2. Designer (Thiết kế)**  

Tập trung vào tạo ra thiết kế linh hoạt, thân thiện với thiết bị. Đây là giai đoạn sáng tạo giao diện người dùng.  

#### UX Planning and Design - Lập Kế Hoạch và Thiết Kế UX

Giai đoạn này tập trung vào trải nghiệm người dùng (UX) khi họ tương tác với trang web. Mục tiêu là đảm bảo rằng trang web dễ sử dụng, trực quan và mang lại giá trị cho người dùng. Các yếu tố quan trọng bao gồm:

- **Nghiên cứu người dùng**: Hiểu đối tượng mục tiêu, nhu cầu của họ và cách họ sẽ tương tác với trang web.
- **Vẽ bản đồ hành trình người dùng**: Lập bản đồ các bước tương tác, từ việc truy cập trang đến thực hiện các hành động quan trọng (như mua hàng, đăng ký, v.v.).
- **Vẽ khung (Wireframing)**: Thiết kế với độ phân giải thấp thể hiện cấu trúc cơ bản của trang và nội dung. Các wireframe tập trung vào cấu trúc hơn là thẩm mỹ và là bước quan trọng để lên kế hoạch cách thiết kế sẽ điều chỉnh với các kích thước màn hình khác nhau.
- **Prototyping (Xây dựng nguyên mẫu)**: Tạo nguyên mẫu có thể tương tác để kiểm tra và cải thiện luồng người dùng, đảm bảo trang web đáp ứng nhu cầu của người dùng ở mọi bước.

####  Page Table - Bảng Trang

Bảng trang là một tài liệu hoặc công cụ liệt kê các thành phần và cấu trúc chính của từng trang trong trang web. Nó giúp tổ chức nội dung và các yếu tố thiết kế cho các điểm dừng (breakpoints) khác nhau (di động, máy tính bảng, máy tính để bàn). Các yếu tố trong bảng trang có thể bao gồm:

- **Bố cục trang**: Đối với mỗi kích thước màn hình (di động, máy tính bảng, máy tính để bàn), bạn sẽ xác định cách sắp xếp nội dung.
- **Nội dung**: Các văn bản, hình ảnh, biểu mẫu và yếu tố tương tác có mặt trên mỗi trang.
- **Breakpoints**: Xác định các điểm mà bố cục thay đổi cho các kích thước màn hình khác nhau (ví dụ: 320px, 768px, 1024px, v.v.).
- **Hành vi**: Cách các yếu tố như menu điều hướng, nút bấm và hình ảnh hoạt động trên các thiết bị khác nhau (ví dụ: menu xổ xuống trên máy tính để bàn, menu thu gọn trên di động).

#### Interaction Design - Thiết Kế Tương Tác

Thiết kế tương tác (IxD) tập trung vào cách người dùng tương tác với trang web hoặc ứng dụng. Điều này bao gồm thiết kế các yếu tố tương tác và đảm bảo rằng trang web cảm thấy trực quan và phản hồi nhanh khi người dùng chạm hoặc click. Các yếu tố quan trọng bao gồm:

- **Các yếu tố có thể nhấp**: Các nút, liên kết, thanh trượt và các yếu tố tương tác khác cần được thiết kế để hoạt động hiệu quả trên tất cả các thiết bị.
- **Chuyển động và hoạt ảnh**: Định nghĩa các chuyển động mượt mà và bắt mắt, đặc biệt là khi các yếu tố thay đổi kích thước hoặc vị trí trong quá trình tương tác (ví dụ: mở modal, mở rộng menu).
- **Trạng thái Hover và Touch**: Đảm bảo các yếu tố tương tác cung cấp phản hồi trực quan khi hover (trên máy tính để bàn) hoặc chạm (trên di động).
- **Khả năng tiếp cận (Accessibility)**: Thiết kế các tương tác sao cho mọi người, kể cả người khuyết tật, đều có thể sử dụng, với các trạng thái focus, điều hướng bằng bàn phím và vai trò ARIA.

#### Visual Design- Thiết Kế trực quan

Thiết kế hình ảnh đảm bảo tính thẩm mỹ của trang web là đồng bộ, hấp dẫn và phù hợp với nhận diện thương hiệu. Trong bối cảnh RWD, thiết kế hình ảnh cũng cần tính đến sự thích ứng trên các kích thước màn hình khác nhau. Các yếu tố chính bao gồm:

- **Typography (Kiểu chữ)**: Đảm bảo font chữ dễ đọc trên tất cả các thiết bị, điều chỉnh kích thước và khoảng cách dòng tùy theo kích thước màn hình.
- **Bảng màu**: Sử dụng màu sắc phù hợp với thương hiệu và dễ tiếp cận cho người khiếm thị.
- **Hình ảnh và Biểu tượng**: Tối ưu hóa hình ảnh cho các kích thước màn hình và độ phân giải khác nhau (ví dụ: màn hình retina), sử dụng biểu tượng dạng vector có thể mở rộng mượt mà trên các thiết bị.
- **Hệ thống lưới (Grid Systems)**: Tạo các bố cục lưới linh hoạt có thể thay đổi theo kích thước màn hình, đảm bảo nội dung được căn chỉnh đẹp mắt và cân đối trên mọi thiết bị.

#### Guidelines and Documentation - Hướng Dẫn và Tài Liệu

Sau khi thiết kế được hoàn thiện, việc tài liệu hóa hệ thống thiết kế và các hướng dẫn là rất quan trọng để đảm bảo tính nhất quán và khả năng mở rộng. Tài liệu này sẽ là tài liệu tham khảo cho các nhà phát triển và nhà thiết kế trong suốt quá trình dự án. Các yếu tố trong hướng dẫn và tài liệu bao gồm:

- **Hệ thống thiết kế (Design System)**: Một bộ quy tắc và thành phần đầy đủ (màu sắc, kiểu chữ, nút bấm, v.v.) đảm bảo tính nhất quán trong toàn bộ thiết kế.
- **Responsive Breakpoints**: Xác định các điểm dừng cụ thể và các điều chỉnh tương ứng cho nội dung và các yếu tố thiết kế.
- **Hướng dẫn về khả năng tiếp cận**: Đảm bảo trang web có thể sử dụng được bởi mọi người, bao gồm điều hướng bằng bàn phím, hỗ trợ màn hình đọc và độ tương phản phù hợp.
- **Thư viện thành phần (Component Libraries)**: Bộ sưu tập các thành phần có thể tái sử dụng mà các nhà phát triển có thể sử dụng để triển khai thiết kế một cách hiệu quả.
- **Đảm bảo chất lượng (Quality Assurance)**: Các hướng dẫn kiểm tra thiết kế trên các thiết bị và kích thước màn hình khác nhau để đảm bảo hành vi responsive hoạt động như mong đợi.

Bằng cách tuân thủ các giai đoạn này, bạn đảm bảo rằng quy trình thiết kế cho RWD của mình được thực hiện toàn diện, tập trung vào người dùng và có khả năng thích ứng, tạo ra trải nghiệm mượt mà trên tất cả các thiết bị.

---

### **💥 3. Develop (Phát triển)**  

Chuyển thiết kế sang mã nguồn thực tế và kiểm tra tính tương thích trên các thiết bị.  

**Hoạt động chính:**  
- **HTML, CSS, JavaScript:** Sử dụng các công nghệ này để xây dựng giao diện responsive.  
- **Frameworks:** Áp dụng framework như Bootstrap hoặc Tailwind CSS để tăng tốc độ phát triển.  
- **Media Queries:** Thêm các quy tắc CSS `@media` để xử lý các kích thước màn hình khác nhau.  
- **Kiểm tra trên thiết bị thật:** Đảm bảo sản phẩm chạy tốt trên các thiết bị khác nhau (mobile, tablet, desktop).  
- **Hiệu suất:** Tối ưu hóa hiệu suất tải trang (lazy loading, tối ưu hình ảnh, và giảm tài nguyên).  

**Kết quả đầu ra:**  
- Giao diện hoạt động đầy đủ.  
- Kiểm tra chất lượng và sửa lỗi.  

---

### **💥 4. Deploy (Triển khai)**  

Đưa sản phẩm lên môi trường thực tế và tiếp tục theo dõi hiệu quả hoạt động.  

- Nâng cấp nội dung: Giúp khách hàng tạo và duy trì nội dung hữu ích và có thể sử dụng được.

- Kiểm tra chấp nhận của người dùng: Giúp xác nhận rằng một trang web mới đáp ứng các mục tiêu và yêu cầu được xác định sớm trong dự án.

- Tài liệu và đào tạo: Giúp chuẩn bị tài liệu văn bản và video để giúp hiểu và sử dụng CMS và trang web mới.

- Kế hoạch ra mắt và phát hành: Giúp tạo kế hoạch ra mắt để lưu trữ Trang web hiện tại và phát hành Trang web mới cho công chúng cũng như danh sách kiểm tra chất lượng để đảm bảo rằng tất cả các yêu cầu của dự án đều được đáp ứng.

- Bắt đầu Kế hoạch vận hành: Giúp đạt được cột mốc thay đổi Trang web khi cần phát triển.


