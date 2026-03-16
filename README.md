<!DOCTYPE html>
<html>
<head>
<title>Student Registration Form</title>

<style>

body{
    font-family: Arial, sans-serif;
    background: linear-gradient(to right, #6a11cb, #2575fc);
}

.container{
    width: 400px;
    background: white;
    margin: 50px auto;
    padding: 25px;
    border-radius: 10px;
    box-shadow: 0px 0px 10px gray;
}

h2{
    text-align: center;
}

label{
    font-weight: bold;
}

input, select, textarea{
    width: 100%;
    padding: 8px;
    margin-top: 5px;
    margin-bottom: 15px;
    border-radius: 5px;
    border: 1px solid gray;
}

.gender{
    width: auto;
}

button{
    width: 48%;
    padding: 10px;
    border: none;
    border-radius: 5px;
    background: #2575fc;
    color: white;
    font-size: 16px;
    cursor: pointer;
}

button:hover{
    background: #1a5ad7;
}

.reset{
    background: #ff4d4d;
}

.reset:hover{
    background: #cc0000;
}

.btns{
    display: flex;
    justify-content: space-between;
}

</style>
</head>

<body>

<div class="container">

<h2>Student Registration</h2>

<form id="studentForm">

<label>First Name</label>
<input type="text" id="fname" required>

<label>Last Name</label>
<input type="text" id="lname" required>

<label>Email</label>
<input type="email" id="email" required>

<label>Password</label>
<input type="password" id="password" required>

<label>Gender</label><br>
<input type="radio" name="gender" value="Male" class="gender"> Male
<input type="radio" name="gender" value="Female" class="gender"> Female
<input type="radio" name="gender" value="Other" class="gender"> Other
<br><br>

<label>Date of Birth</label>
<input type="date" id="dob">

<label>Course</label>
<select id="course">
<option>BCA</option>
<option>BBA</option>
<option>B.Tech</option>
<option>MBA</option>
</select>

<label>Address</label>
<textarea id="address" rows="3"></textarea>

<div class="btns">
<button type="submit">Register</button>
<button type="reset" class="reset">Reset</button>
</div>

</form>

</div>

<script>

document.getElementById("studentForm").addEventListener("submit", function(event){

    event.preventDefault(); // stop page refresh

    let fname = document.getElementById("fname").value;
    let lname = document.getElementById("lname").value;
    let email = document.getElementById("email").value;
    let password = document.getElementById("password").value;
    let dob = document.getElementById("dob").value;
    let course = document.getElementById("course").value;
    let address = document.getElementById("address").value;

    let gender = document.querySelector('input[name="gender"]:checked');

    console.log("Student Registration Data");
    console.log("First Name:", fname);
    console.log("Last Name:", lname);
    console.log("Email:", email);
    console.log("Password:", password);
    console.log("Gender:", gender ? gender.value : "Not selected");
    console.log("Date of Birth:", dob);
    console.log("Course:", course);
    console.log("Address:", address);

});

</script>

</body>
</html>
