## Đối tượng trong JS
* Là một thực thể có thuộc tính và phương thức
* 3 cách tạo đối tượng:
  * Sử dụng chuỗi chữ
  * Tạo thể hiện của Object (sử dụng từ khóa new)
  * Sử dụng một hàm tạo đối tượng (sử dụng từ khóa new)
* Tạo đối tượng bằng chuỗi chữ
```
<script>
    emp = {
        id : 102,
        name : "David",
        salary : 40000
    }
    document.write(emp.id + " " + emp.name + " " + emp.salary);
</script> 

```
* Tạo đối tượng bằng thể hiện của object (sử dụng new)
```
<script>
    var emp = new Object();
    emp.id = 101;
    emp.name = "David";s
    emp.salary = 50000;
    document.write(emp.id + "" + emp.name + "" + emp.salary);
</script>
```
* Tạo đối tượng bằng cách sử dụng một hàm tạo đối tượng (sử dụng từ khóa new)
```
<script>
    function emp(id, name, salary) {
        this.id = id;
        this.name = name;
        this.salary = salary;
    }
    e = new emp(103, "David", 30000);
 
    document.write(e.id + " " + e.name + " " + e.salary);
</script>

```
* Định nghĩa phương thức tỏng đối tượng JS
  * cần thêm thuộc tính trong hàm cùng tên cới phương thức
  ```
  <script>
    function emp(id, name, salary) {
        this.id = id;
        this.name = name;
        this.salary = salary;
        
        //thuoc tinh nay trung ten phuong thuc
        this.changeSalary = changeSalary;
        function changeSalary(otherSalary) {
            this.salary = otherSalary;
        }
    }
    e = new emp(103, "David", 30000);
    document.write(e.id + " " + e.name + " " + e.salary);
    e.changeSalary(45000);
    document.write("<br>" + e.id + " " + e.name + " " + e.salary);
  </script>
  
  ```
