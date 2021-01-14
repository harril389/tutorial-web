<div align="center">
  <img height="100" src="img/logo1.png">
  <h1>Tips-js-css-reactjs</h1>

---

</div>

## Table of Contents

1. [ReactJS](#reactjs)
2. [JS](#js)
3. [CSS](#css)
4. [Regex](#regex)

## ReactJS

1. Item 1
2. Item 2
3. Item 3
   1. Item 3a
   2. Item 3b

## JS

1. <details><summary><b>Xử lý mảng trong JS<b></summary>
   <details><summary><b>Menu<b></summary>
     
    1. [Map](#map)
    2. [Filter](#filter)
    3. [Reduce](#reduce)
    4. [forEach()](#forEach)
    5. [find()](#find)
    6. [push()](#push)
    7. [pop()](#pop)
    8. [shift()](#shift)
    9. [unshift()](#unshift)
    10. [splice()](#splice)
    11. [sort()](#sort)
    12. [reverse()](#reverse)
    13. [concat()](#concat)
    14. [slice()](#slice)
    15. [join()](#join)
    
   </details>
     
   1. ## **Map**
      1. Xử lý từng biến trong một mảng theo cùng 1 cách, trả về các giá trị sau xử lý bằng đúng số lượng phần tử ban đầu
      2. Hàm `map()` nhận vào 3 tham số (theo thứ tự):
         - Phần tử hiện tại của mảng.
         - Chỉ số của phần tử hiện tại trong mảng.
         - Mảng ban đầu.
      3. ```javascript
         let animal_names = animals.map((animal, index, animals) => {
           return animal.name;
         });
         ```
   2. ## **Filter**

   1. Lấy các phần tử trong mảng theo một tiêu chuẩn nhất định
   2. Hàm `Filter()` nhận vào 3 tham số (theo thứ tự):
      - Phần tử hiện tại của mảng.
      - Chỉ số của phần tử hiện tại trong mảng.
      - Mảng ban đầu.
   3. ```javascript
      let small_animals = animals.filter((animal) => {
        return animal.size === "small";
      });
      ```

   4. ## **Reduce**

      1. Hàm `reduce` sẽ biến đổi một mảng thành một giá trị đơn giản.
      2. Hàm `reduce` sẽ thực hiện một hàm được cung cấp cho mỗi giá trị của mảng, từ trái qua phải.
      3. Hàm sẽ trả về một kết quả được lưu trữ( tổng số hoặc kết quả tính toàn).
      4. Hàm `reduce` sẽ không thực hiện hàm được cung cấp đối với các phần tử không có giá trị.
      5. Hàm `reduce()` nhận vào 3 tham số (theo thứ tự):
         - Tham số đầu tiên là giá trị khởi tạo. Ta cần set giá trị khởi tạo ở cuối hàm. Trong ví dụ dưới là `0`. Nó có thể là bất cứ giá trị nào.
         - Tham số thứ 2 là phần tử hiện tại trong mảng.
         - Tham số thứ 3 và 4 giống với 2 hàm kể trên.
      6. ```javascript
         let total_weight = animals.reduce((weight, animal, index, animals) => {
           return (weight += animal.weight);
         }, 0);
         ```

   5. ## **forEach()**

      1. Phương thức `forEach()` sẽ thực thi một hàm khi duyệt qua từng phần tử của mảng.
      2. ```javascript
         const arr = ["a", "b", "c"];
         arr.forEach((element) => console.log(element));
         // expected output: "a"
         // expected output: "b"
         // expected output: "c"
         ```

   6. ## **find()**

      1. Phương thức `find()` sẽ trả về giá trị đầu tiên tìm thấy ở trong mảng được cung cấp.
      2. ```javascript
         const arr = [5, 12, 8, 130, 44];
         const found = arr.find((element) => element > 10);
         console.log(found);
         // expected output: 12
         ```

   7. ## **push()**

      1. Thêm một phần tử vào cuối mảng.
      2. ```javascript
         var arr = ["Xử", "lý", "chuỗi", "trong"];
         arr.push("JS"); //["Xử", "lý", "chuỗi", "trong", "JS"]
         ```

   8. ## **pop()**

      1. Xóa đi phần tử cuối cùng trong mảng.
      2. ```javascript
         var arr = ["Xử", "lý", "chuỗi", "trong", "JS"];
         arr.pop("JS"); //["Xử", "lý", "chuỗi", "trong"]
         ```

   9. ## **shift()**

      1. Xóa phần tử đầu tiên của mảng, sau đó dồn các phần tử phía sau xuống một bậc.
      2. ```javascript
         var arr = ["Xử", "lý", "chuỗi", "trong", "JS"];
         arr.shift(); //["lý", "chuỗi", "trong", "JS"]
         ```

   10. ## **unshift()**

       1. Thêm một phần tử vào vị trí đầu tiên của mảng, đồng thời đẩy các phẩn từ phía sau lên một bậc.
       2. ```javascript
          var arr = ["lý", "chuỗi", "trong", "JS"];
          arr.unshift("Xử"); //["Xử", "lý", "chuỗi", "trong", "JS"]
          ```

   11. ## **splice()**

       1. Thêm hoặc xóa các phần tử.
       2. Hàm `splice()` có ba tham số truyền vào:
          - `position_add` là vị trí sẽ thêm (vị trí đầu tiên là 0).
          - `num_element_remove` là số phần tử sẽ xóa (bắt đầu từ `position_add`).
          - `value1,` `value2,` .. là danh sách các phần tử sẽ được thêm vào sau khi tại vị trí `position_add` và sau khi remove `num_element_remove` phần tử.
       3. ```javascript
          var arr = ["Xử", "lý", "chuỗi", "trong", "JS"];
          arr.splice(1, 2, "hihi"); //["Xử", "hihi", "trong", "JS"]
          ```

   12. ## **sort()**

       1. Hàm này dùng để sắp xếp các phần tử trong mảng theo thứ tự chữ cái `alpha`.
       2. ```javascript
          var arr = ["Xử", "lý", "chuỗi", "trong", "JS"];
          arr.sort(); //["JS", "Xử", "chuỗi","lý", "trong"]
          ```

   13. ## **reverse()**

       1. Hàm đảo ngược các phẩn tử lại. Vị trí đầu sẽ được chuyển xuống cuối mảng và vị trí cuối mảng sẽ được chuyển lên đầu mảng.
       2. ```javascript
          var arr = ["Xử", "lý", "chuỗi", "trong", "JS"];
          arr.reverse(); //["JS", "trong", "chuỗi","lý", "Xử"]
          ```

   14. ## **concat()**

       1. Hàm dùng để nối hai mảng với nhau và trả về một mảng gồm tổng số phần tử của hai mảng đó. (hàm này sẽ trả lại một bản sao của mảng sau khi đã thực hiện nối, không làm thay đổi mảng gọi nó).
       2. ```javascript
          var arr1 = ["Xử", "lý", "chuỗi"];
          var arr2 = ["trong", "JS"];
          var arr = arr1.concat(arr2); //["Xử", "lý", "chuỗi", "trong", "JS"]
          ```

   15. ## **slice()**

       1. Hàm dùng để lấy một số phần tử con trong mảng.
       2. ```javascript
          var arr = ["Xử", "lý", "chuỗi", "trong", "JS"];
          arr.slice(3, 5); //["trong", "JS"];
          //slice(start, end)
          //`start`: là vị trí bắt đầu
          //`end`: là vị trí kết thúc
          ```

   16. ## **join()**

       1. Tạo ra một chuỗi mới bằng cách nối tất cả các phần tử của mảng.
       2. ```javascript
          var arr = ["Xử", "lý", "chuỗi", "trong", "JS"];
          arr.join(); //"Xử,lý,chuỗi,trong,JS"
          arr.join(""); //"XửlýchuỗitrongJS"
          arr.join("-"); //Xử-lý-chuỗi-trong-JS"
          ```

</details>

2. <details><summary><b>Xử lý chuỗi trong JS<b></summary>
   <details><summary><b>Menu<b></summary>
     
    1. [length](#length)
    2. [indexOf()](#indexOf)
    3. [lastIndexOf()](#lastIndexOf)
    4. [Search()](#Search)
    5. [slice()](#slice-1)
    6. [substring()](#substring)
    7. [substr()](#substr)
    8. [replace()](#replace)
    9. [toUpperCase()](#toUpperCase)
    10. [toLowerCase()](#toLowerCase)
    11. [split()](#split)
    
   </details>

   1. ## **length**
      1. Để lấy độ dài chuỗi.
      2. ```javascript
         string.length;
         //`string` là tên biến chứa chuỗi.
         var a = "harrii";
         a.length; //6
         ```
   2. ## **indexOf()**

      1. Phương thức này trả về vị trí của từ xuất hiện đầu tiên trong chuỗi, nếu trong chuỗi không có từ cần tìm thì nó sẽ trả về `-1`.
      2. ```javascript
         string.indexOf(keyword);
         //`keyword` là từ khóa cần tìm trong chuỗi.
         var a = "harrii";
         a.indexOf("toidicode"); //2
         ```

   3. ## **lastIndexOf()**

      1. Phương thức này cũng giống với phương thức `indexOf()` là tìm kiếm vị trí của chuỗi, nhưng hàm này sẽ trả về **vị trí cuối cùng của chuỗi xuất hiện** trong chuỗi cần tìm.
      2. ```javascript
         string.lastIndexOf(keyword);
         //`keyword` là từ khóa cần tìm trong chuỗi.
         var a = "harrii";
         a.lastIndexOf("toidicode"); //3
         ```

   4. ## **Search()**

      1. Hàm này giống như hàm `indexOf`.

   5. ## **slice()**

      1. Hàm này có tác dụng cắt ra một chuỗi con từ một chuỗi cha.
      2. Vị trí của chuỗi được tính từ `0`.
      3. Cắt chuỗi từ cuối về đầu. bằng việc thêm dấu `trừ` vào trước vị trí (tính từ cuối về đầu).
      4. ```javascript
         string.slice(begin, end);
         //`begin` là vị trí bắt đầu cắt chuỗi
         //`end` là vị trí kết thúc cắt chuỗi (nếu không điền thì là cắt đến hết chuỗi).
         var a = "harrii";
         a.slice(0, 3); //har
         ```

   6. ## **substring()**

      1. Hàm này cũng tương tự như hàm `slice()`, nhưng hàm này không cho phép truyền vào số âm.

   7. ## **substr()**

      1. Phương thức này cũng có tác dụng là cắt chuỗi nhưng tham số thứ 2 của phương thức này có phần khác với 2 phương thức còn lại.
      2. Vị trí của chuỗi được tính từ `0`.
      3. ```javascript
         string.substr(begin, length);
         //`begin` là vị trí bắt đầu cắt chuỗi
         //`length` là độ dài của chuỗi muốn cắt (tính từ điểm bắt đầu cắt).
         ```

   8. ## **replace()**

      1. Phương thức này cho phép tìm kiếm và thay thế chuỗi.
      2. ```javascript
         string.replace(chuoicantim, chuoithaythe);
         //`chuoicantim` là chuỗi cần tìm để thay thế.
         //`chuoithaythe` là chuỗi thay thế.
         var a = "harriwon";
         a.replace("won", "i"); //harrii
         ```

   9. ## **toUpperCase()**

      1. Phương thức này có tác dụng chuyển đổi chuỗi thành chữ in hoa.
      2. ```javascript
         string.toUppercase();
         var a = "harrii";
         a.toUpperCase(); //HARRII
         ```

   10. ## **toLowerCase()**

       1. Phương thức này có tác dụng chuyển đổi chuỗi thành chuỗi thường.
       2. ```javascript
          string.toLowerCase();
          var a = "HARRII";
          a.toLowerCase(); //harrii
          ```

   11. ## **split()**
       1. Phương thức `string.split()` sẽ phân tách một chuỗi thành một mảng dữ liệu dựa vào các kí tự phân cách trong chuỗi. Phương thức sẽ trả về một mảng mới.
       2. Nếu kí tự phân cách là một chuỗi rỗng, mỗi kí tự trong chuỗi sẽ được phân tách thành một phần tử của mảng.
       3. Phương thức `string.split()` sẽ không làm thay đổi chuỗi gốc ban đầu.
       4. ```javascript
          string.split(separator, limit);
          //`separator` là kí tự phân cách trong chuỗi, phương thức sẽ dựa vào kí tự này để phân tách chuỗi. Nếu không truyền vào, mảng trả về sẽ có một phần tử duy nhất có giá trị bằng chuỗi ban đầu. Nếu truyền vào một chuỗi rỗng, mỗi kí tự trong chuỗi sẽ là một phần tử của mảng trả về.
          //`limit` là tham số quy định số phần tử tối đa của mảng trả về. Nếu không được truyền vào thì phương thức sẽ lấy tất cả các phần tử có thể.
          var str = "Xử lý chuỗi trong JS";
          str.split(" "); //["Xử", "lý", "chuỗi", "trong", "JS"]
          ```

</details>

3. Item 3
   1. Item 3a
   2. Item 3b

## CSS

1. <details><summary><b>Phân biệt: display inline, block, inline-block<b></summary>

   1. **Inline**
      1. Với kiểu này thì các item sẽ nằm trên cùng một dòng, ví dụ như `<span>` . Nếu các items vượt quá độ dài của dòng thì item sẽ xuống dòng mới
      2. Các item có kiểu display này không thể set `width` và `height`.
      3. Các inline item sẽ chỉ có thể điều chỉnh `margin` và `padding` `left` và `right` (`top` và `bottom` thì không thể).
   2. **Block**
      1. Luôn được xuống dòng và chiếm toàn bộ `width` nếu width không được set.
   3. **Inline-block**
      1. Sẽ được sắp xếp giống với kiểu `display: inline` nghĩa là các items sẽ được xếp cùng nhau trên một dòng . Tuy nhiên các items sẽ có thuộc tính của `display: block` như là có set `width, height, margin, padding` đủ 4 hướng.

</details>

2. <details><summary><b>Có bao nhiêu cách để ẩn 1 phần tử<b></summary>

   1. `clip-path: circle(0)`
   2. `visibility: hidden`
   3. `display: none`
   4. `opacity: 0`
   5. `position: absolute; top: -9999px; left: -9999px`

</details>

3. <details><summary><b>Phân biệt margin và padding<b></summary>

   1. `Margin` là khoảng trống nằm giữa viền và phần tử tiếp theo
   2. `Padding` là khoảng trống nằm giữa nội dung và viền

</details>

4. <details><summary><b>Phân biệt: min-width, width, max-width<b></summary>

   1. `Min-width` được sử dụng để thiết lập chiều rộng nhỏ nhất cho một phần tử. Nó ngăn chặn chiều rộng của phần tử nhỏ hơn một giá trị được chỉ định.
   2. `Width` thiết lập chiều rộng cho thành phần.
   3. `Max-width` được sử dụng để thiết lập chiều rộng lớn nhất cho một phần tử. Nó ngăn chặn chiều rộng của phần tử vượt quá một giá trị được chỉ định.

</details>

5. <details><summary><b>Phân biệt: ul và ol<b></summary>

   1. Thẻ `\<ul>` tạo danh sách không có thứ tự
   2. Thẻ `\<ol>` tạo danh sách có thứ tự

</details>

6. <details><summary><b>Phân biệt các giá trị của Position<b></summary>

   1. **Static**
      1. Là giá trị mặc định của position
   2. **Relative**
      1. Vị trí mới của một element tương quan/ liên hệ tới vị trí mặc định của nó.
      2. Với các giá trị khác ngoài static, chúng ta có thể dễ dàng thay đổi vị trí của chúng bằng các thuộc tính helper `top | right | bottom | left | z-index`.
   3. **Absolute**
      1. Sẽ dịch chuyển vị trí của nó tương ứng với thẻ cha của nó.
      2. Một element được khai báo với thuộc tính position: absolute sẽ được loại bỏ khỏi luồng document (document flow). Vị trí mặc định của element sẽ là điểm bắt đầu (top-left) của element cha. Nếu nó không có bất cứ thẻ cha nào thì thẻ document `<html>` sẽ là cha của nó.
   4. **Fixed**
      1. Sẽ được loại bỏ khỏi document flow
      2. Vị trí của chúng **CHỈ** tương quan với thẻ `<html>`
      3. Chúng không bị ảnh hưởng bới scroll
   5. **Sticky**
      1. Là sự kết hợp của `position: relative` và `position: fixed`.
      2. Khi scroll đến vị trí của nó sẽ giống hệt như `fixed` và khi scroll ra khỏi nó thì nó sẽ quay lại vị trí ban đầu dưới dạng `relative`.

</details>

7. <details><summary><b>Nếu ảnh và text đang ở cùng 1 vị trí thì làm thế nào để chữ hiển thị lên ảnh. (ảnh và chữ là 2 phần tử khác nhau)<b></summary>
   1. Sử dụng thuộc tính `z-index` để set cho giá trị `z-index` của text lớn hơn giá trị `z-index` của ảnh

</details>

8. <details><summary><b>Overflow <b></summary>

   1. **Text-overflow**
      1. `text-overflow: clip` đoạn văn bản overflow sẽ bị ẩn đi.
      2. `text-overflow: ellipsis` phần bị ẩn đi sẽ được thay thế bằng dấu '3 chấm'
   2. **Overflow**
      1. `overflow: visible` phần nội dung bị tràn không bị cắt đi và nội dung bị tràn ra sẽ ghi đè lên các phần tử khác.
      2. `overflow: hidden` phần nội dung bị tràn ra bị cắt đi và phần nội dung đó sẽ bị ẩn đi.
      3. `overflow: scroll` phần nội dung bị tràn ra vẫn bị cắt đi, tuy nhiên trình duyệt sẽ có thêm thanh `scroll`, mình có thể kéo xem phần nội dung bị ẩn đi. Thanh `scroll` này được thêm vào cho cả chiều dọc và chiều ngang của phần tử.
      4. `overflow: auto` cũng giống như giá trị `scroll`, tuy nhiên thanh `scroll` sẽ được thêm vào khi cần thiết.
   3. **Overflow-x**
      1. Thuộc tính cho phép điều khiển nội dung bị tràn theo chiều ngang (nghĩa là bên trái `left` và bên phải `right` của phần tử). Tương tự thuộc tính `overflow`, thuộc tính `overflow-x` cũng có giá trị như `visible, hidden, auto, scroll`.
   4. **Overflow-y**
      1. Thuộc tính cho phép điều khiển nội dung bị tràn theo chiều dọc (nghĩa là bên trên `top` và bên dưới `bottom` của phần tử). Tương tự thuộc tính `overflow`, thuộc tính `overflow-y` cũng có giá trị như `visible, hidden, auto, scroll`.

</details>

## Regex

1. <details><summary><b>Các ký tự biểu diễn<b></summary>

   | Flag   |                             Detail                              |
   | ------ | :-------------------------------------------------------------: |
   | .      |      Biểu diễn bất kỳ ký tự nào ngoại trừ ký tự xuống dòng      |
   | []     |   Tập hợp ký tự. Phù hợp nếu có bất kỳ ký tự nào trong dấu []   |
   | [^ ]   | Tập hợp ký tự phủ định. Phù hợp nếu không có ký tự nào trong [] |
   | \*     |                     Lặp lại 0 đến nhiều lần                     |
   | +      |                    Lặp lại 1 hoặc nhiều lần                     |
   | ?      |            Tùy chọn có hay không cho mẫu phía trước             |
   | {n,m}  |                Độ dài tối thiểu là n tối đa là m                |
   | (xyz)  |                     Biểu diễn một nhóm mẫu                      |
   | &#124; |               Biểu diễn thay thế, phép toán `or`                |
   | \      |   Biểu diễn ký tự đặc biệt [ ] ( ) { } . \* + ? ^ $ \ &#124;    |
   | ^      |                      Điểm bắt đầu của dòng                      |
   | $      |                     Điểm kết thúc của dòng                      |

</details>

2. <details><summary><b>Ký hiệu tắt cho tập hợp<b></summary>

   | Flag |                        Detail                         |
   | ---- | :---------------------------------------------------: |
   | .    | Biểu diễn bất kỳ ký tự nào ngoại trừ ký tự xuống dòng |
   | \w   |   Chữ,số, và &#8212;, tương đương với: [a-zA-Z0-9_]   |
   | \W   |      Ngoài bảng chữ cái, tương đương với: [^\w]       |
   | \d   |                     Các số: [0-9]                     |
   | \D   |               Lặp lại 1 hoặc nhiều lần                |
   | ?    |                 Không phải số: [^\d]                  |
   | \s   |   Là ký tự trắng, tương đương với: [\t\n\f\r\p{Z}]    |
   | \S   |             Không phải ký tự trắng: [^\s]             |

</details>
