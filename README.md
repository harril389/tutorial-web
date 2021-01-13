<div align="center">
  <img height="100" src="img/logo1.png">
  <h1>Tips-js-css-reactjs</h1>

---

</div>

## Table of Contents

1. [ReactJS](#reactjs)
2. [JS](#js)
3. [CSS](#css)

## ReactJS

1. Item 1
2. Item 2
3. Item 3
   1. Item 3a
   2. Item 3b

## JS

1. Item 1
2. Item 2
3. Item 3
   1. Item 3a
   2. Item 3b

## CSS

1. <details><summary><b>Phân biệt: display inline, block, inline-block<b></summary>

   1. **inline**
      1. Với kiểu này thì các item sẽ nằm trên cùng một dòng, ví dụ như \<span> . Nếu các items vượt quá độ dài của dòng thì item sẽ xuống dòng mới
      2. Các item có kiểu display này không thể set width và height.
      3. Các inline item sẽ chỉ có thể điều chỉnh margin và padding left and right (top và bottom thì không thể).
   2. **block**
      1. luôn được xuống dòng và chiếm toàn bộ width nếu width không được set.
   3. **inline-block**
      1. sẽ được sắp xếp giống với kiểu display: inline, nghĩa là các items sẽ được xếp cùng nhau trên một dòng . Tuy nhiên các items sẽ có thuộc tính của display: block như là có set width, height, margin, padding đủ 4 hướng.

</details>

2. <details><summary><b>Có bao nhiêu cách để ẩn 1 phần tử<b></summary>

   1. clip-path: circle(0);
   2. visibility: hidden;
   3. display: none;
   4. opacity: 0;
   5. position: absolute; top: -9999px; left: -9999px;

</details>

3. <details><summary><b>Phân biệt margin và padding<b></summary>

   1. **Margin** là khoảng trống nằm giữa viền và phần tử tiếp theo
   2. **Padding**là khoảng trống nằm giữa nội dung và viền

</details>

4. <details><summary><b>Phân biệt: min-width, width, max-width<b></summary>

   1. **min-width** được sử dụng để thiết lập chiều rộng nhỏ nhất cho một phần tử. Nó ngăn chặn chiều rộng của phần tử nhỏ hơn một giá trị được chỉ định.
   2. **width** thiết lập chiều rộng cho thành phần.
   3. **max-width** được sử dụng để thiết lập chiều rộng lớn nhất cho một phần tử. Nó ngăn chặn chiều rộng của phần tử vượt quá một giá trị được chỉ định.

</details>

5. <details><summary><b>Phân biệt: ul và ol<b></summary>

   1. Thẻ `\<ul>` tạo danh sách không có thứ tự
   2. Thẻ `\<ol>` tạo danh sách có thứ tự

</details>

6. <details><summary><b>Phân biệt các giá trị của Position<b></summary>
   1. **static**
      1. Là giá trị mặc định của position
   2. **Relative**
      1. Vị trí mới của một element tương quan/ liên hệ tới vị trí mặc định của nó.
      2. Với các giá trị khác ngoài static, chúng ta có thể dễ dàng thay đổi vị trí của chúng bằng các thuộc tính helper `top | right | bottom | left | z-index`.
   3. **Absolute**
      1. Sẽ dịch chuyển vị trí của nó tương ứng với thẻ cha của nó.
      2. Một element được khai báo với thuộc tính position: absolute sẽ được loại bỏ khỏi luồng document (document flow). Vị trí mặc định của element sẽ là điểm bắt đầu (top-left) của element cha. Nếu nó không có bất cứ thẻ cha nào thì thẻ document `\<html>` sẽ là cha của nó.
   4. **Fixed**
      1. Sẽ được loại bỏ khỏi document flow
      2. Vị trí của chúng **CHỈ** tương quan với thẻ `\<html>`
      3. Chúng không bị ảnh hưởng bới scroll
   5. **Sticky**
      1. Là sự kết hợp của `position: relative` và `position: fixed`.
      2. Khi scroll đến vị trí của nó sẽ giống hệt như `fixed` và khi scroll ra khỏi nó thì nó sẽ quay lại vị trí ban đầu dưới dạng `relative`.

</details>

7. <details><summary><b>nếu ảnh và text đang ở cùng 1 vị trí thì làm thế nào để chữ hiển thị lên ảnh. (ảnh và chữ là 2 phần tử khác nhau)<b></summary>
   1. sử dụng thuộc tính z-index để set cho giá trị z-index của text lớn hơn giá trị z-index của ảnh

</details>

8. <details><summary><b>Overflow <b></summary>
   1. **text-overflow**
      1. `text-overflow: clip` đoạn văn bản overflow sẽ bị ẩn đi.
      2. `text-overflow: ellipsis` phần bị ẩn đi sẽ được thay thế bằng dấu '3 chấm'
   2. **overflow**
      1. `overflow: visible`  phần nội dung bị tràn không bị cắt đi và nội dung bị tràn ra sẽ ghi đè lên các phần tử khác.
      2. `overflow: hidden` phần nội dung bị tràn ra bị cắt đi và phần nội dung đó sẽ bị ẩn đi.
      3. `overflow: scroll` phần nội dung bị tràn ra vẫn bị cắt đi, tuy nhiên trình duyệt sẽ có thêm thanh `scroll`, mình có thể kéo xem phần nội dung bị ẩn đi. Thanh `scroll` này được thêm vào cho cả chiều dọc và chiều ngang của phần tử.
      4. `overflow: auto` cũng giống như giá trị `scroll`, tuy nhiên thanh `scroll` sẽ được thêm vào khi cần thiết.
   3. **overflow-x**
      1. Thuộc tính cho phép điều khiển nội dung bị tràn theo chiều ngang (nghĩa là bên trái `left` và bên phải `right` của phần tử). Tương tự thuộc tính `overflow`, thuộc tính `overflow-x` cũng có giá trị như `visible, hidden, auto, scroll`.
   4. **overflow-y**
      1. Thuộc tính cho phép điều khiển nội dung bị tràn theo chiều dọc (nghĩa là bên trên `top` và bên dưới `bottom` của phần tử). Tương tự thuộc tính `overflow`, thuộc tính `overflow-y` cũng có giá trị như `visible, hidden, auto, scroll`.

</details>
