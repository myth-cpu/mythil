<!DOCTYPE html>
<html>
<head>
<title>Form Validation</title>
</head>
<body>
<form name="myForm" method="post" action="abc.jsp" onsubmit="return validateForm()">
  Name: <input type="text" name="name"><br/>
  Password: <input type="password" name="password"><br/>
  <input type="submit" value="Register">
</form>

<script>
function validateForm() {
  var name = document.myForm.name.value;
  var password = document.myForm.password.value;

  if (name == null || name == "") {
    alert("Name can't be blank");
    return false;
  } else if (password.length < 6) {
    alert("Password must be at least 6 characters long");
    return false;
  }
  return true; // Form is valid
}
</script>
</body>
</html>
