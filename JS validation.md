# Validation form
* VD:
```
<script>
    function validateform() {
        var name = document.myform.name.value;
        var password = document.myform.password.value;
 
        if (name == null || name == "") {
            alert("Name can't be blank");
            return false;
        } else if (password.length < 6) {
            alert("Password must be at least 6 characters long.");
            return false;
        }
    }
</script>
<body>
  <form name="myform" method="post" action="welcome1.php"
        onsubmit="return validateform()">
    Name: <input type="text" name="name"><br> 
    Password: <input type="password" name="password"><br>
    <input type="submit" value="register">
  </form>
</body>
```
* Nhập lại mật khẩu bằng JS
```
<script type="text/javascript">
    function matchpass() {
        var firstpassword = document.form1.password.value;
        var secondpassword = document.form1.password2.value;
 
        if (firstpassword == secondpassword) {
            return true;
        } else {
            alert("password must be same!");
            return false;
        }
    }
</script>
<body>
<form name="form1" action="welcome1.php" onsubmit="return matchpass()">
  <table>
  <tr>
    <td> Password: </td>
    <td> <input type="password" name="password" /></td>
  </tr>
  <tr>
    <td>Re-enter Password: </td> 
    <td><input type="password" name="password2" /></td>
  <tr>
  <tr>
    <td> <input type="submit" value="Submit"> </td>
    <td></td>
</form>
</body>
```
* Validate số bằng JS
```
<script>
    function validate() {
        var num = document.myform.num.value;
        if (isNaN(num)) {
            document.getElementById("numloc").innerHTML = "Chỉ nhập giá trị số.";
            return false;
        } else {
            return true;
        }
    }
</script>
<form name="myform" onsubmit="return validate()">
  Number: <input type="text" name="num"><span id="numloc"></span><br> 
  <input type="submit" value="submit">
</form>
```
* Hiện hình ảnh khi validate form bằng JS
```
<script>
    function validate() {
        var name = document.myform.name.value;
        var password = document.myform.password.value;
        var status = false;
 
        if (name.length < 1) {
            document.getElementById("nameloc").innerHTML = 
                " <img src='unchecked.gif'/> Please enter your name";
            status = false;
        } else {
            document.getElementById("nameloc").innerHTML = 
                " <img src='checked.gif'/>";
            status = true;
        }
        if (password.length < 6) {
            document.getElementById("passwordloc").innerHTML = 
                " <img src='unchecked.gif'/> Password must be at least 6 char long";
            status = false;
        } else {
            document.getElementById("passwordloc").innerHTML = 
                " <img src='checked.gif'/>";
        }
        return status;
    }
</script>
 
<form name="myform" action="#" onsubmit="return validate()">
  <table>
    <tr>
      <td>Enter Name:</td>
      <td><input type="text" name="name" /> <span id="nameloc"></span></td>
    </tr>
    <tr>
      <td>Enter Password:</td>
      <td>
          <input type="password" name="password" /> 
          <span id="passwordloc"></span>
      </td>
    </tr>
    <tr>
      <td colspan="2"><input type="submit" value="register" /></td>
    </tr>
  </table>
</form>
```
 
