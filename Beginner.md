## Biến
* local: bên trong block code
* gloabl: khai báo bên ngoài hàm hoặc cùng đối tượng window (window.a)
  * khi khai báo một đối tượng bên ngoài hàm nó được thêm vào trong đối tượng window
  ```
  <script>
    var value = 50;
    function a() {
        alert(window.value); //truy cập biến toàn cầu
    }
  </script>
  ```
## Kiểu dữ liệu
* kiểu nguyên thủy (primitive) và tham chiếu (reference)
  * Nguyên thủy: String, Number, Boolean, Undefined, Null 
  * Thamc chiếu: Object, Array, RegExp
* JS là ngôn ngữ kiểu động => không cần chỉ định loại biến
## Toán tử
Toán tử | Mô tả
------------ | -------------
(?:) | toán tử điều kiện dựa trên điều kiện
, | cho phép nhiều biểu thức được đánh giá như một câu lệnh đơn
delete | xóa một thuộc tính của đối tượng
in | kiểm tra đối tượng đã có thuộc tính đã cho
instance of | Kiểm tra nếu đối tượng là một thể hiện của kiểu dữ liệu đã cho
new | tạo một thể hiện của đối tượng
typeof | kiểm tra đối tượng
void | loại bỏ giá trị trả về của biểu thức
yeild | kiểm tra những gì được trả về trong một trình tạo bởi trình lặp của trình tạo
## Hàm
* Là một chương trình con được thiết kế để thực hiện một công việc cụ thể
* Hàm trong JS luôn trả về một giá trị, nếu không định nghĩa giá trị cụ thể, hàm sẽ trả về undefined
## Sự kiện (event)
* là sự tương tác của JS với HTML xảy ra khi người dùng hoặc trình duyệt thao tác với một trang web (onclick, onmouseover, onmouseout ...)
