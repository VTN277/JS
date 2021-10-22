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
