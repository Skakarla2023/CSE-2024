# 


### Write a HTML Code to create a form.

Code:

```
<html>
<head>
<title>Admission form NCERT Junction</title>
</head>
<body>

<h2>ONLINE CLASSES FOR XII,XI</h2>

<form action="\submit.php" method="post" name="form">
  <label for="fname">Full name:</label>
  <input type="text" id="fname" name="fname"><br>
  <label for="dob">Date of birth:</label>
  <input type="date" id="dob" name="dob"><br>
  <label for="mname">Mother name:</label>
  <input type="text" id="mname" name="mname"><br>
  <label for="faname">Father name:</label>
  <input type="text" id="faname" name="faname"><br>
  <p>Have You(Yes/No):</p>
  <input type="radio" id="computer" name="devices" value="COMPUTER">
  <label for="computer">COMPUTER</label>
  <input type="radio" id="mobile" name="devices" value="MOBILE">
  <label for="mobile">MOBILE</label>
  <input type="radio" id="zoom/g-meet" name="devices" value="ZOOM/G-MEET">
  <label for="zoom/g-meet">ZOOM/G-MEET</label><br>
  <label for="sname">School name:</label>
  <input type="text" id="sname" name="sname"><br>
  <label for="cname">Class:</label>
  <input type="text" id="cname" name="cname"><br>
  <p>Courses Applied:</p>
  <input type="checkbox" id="ec" name="ec" value="ECONOMICS">
  <label for="ec">ECONOMICS</label>
  <input type="checkbox" id="ps" name="ps" value="POLITICAL SCIENCE">
  <label for="ps">POLITICAL SCIENCE</label>
  <input type="checkbox" id="geo" name="geo" value="GEOGRAPHY">
  <label for="geo">GEOGRAPHY</label>
  <input type="checkbox" id="hi" name="hi" value="HISTORY">
  <label for="hi">HISTORY</label>
  <input type="checkbox" id="ls" name="ls" value="LEGAL STUDIES">
  <label for="ls">LEGAL STUDIES</label><br>
  <label for="mno">Mobile Number:</label>
  <input type="number" id="mno" name="mno"><br>
  <label for="wno">Whatsapp Number:</label>
  <input type="number" id="wno" name="wno"><br>
  <label for="email">Email:</label>
  <input type="mail" id="email" name="email"><br>
  <p>Gender:</p>
  <input type="radio" id="male" name="gender" value="MALE">
  <label for="male">MALE</label>
  <input type="radio" id="female" name="gender" value="FEMALE">
  <label for="female">FEMALE</label><br>
  <label for="add">Permanent Address:</label>
  <input type="text" id="add" name="add"><br>
  <label for="city">City/District</label>
  <input type="text" id="city" name="city"><br>
  <p>How you know us?</p>
  <input type="radio" id="internet" name="how" value="INTERNET">
  <label for="internet">INTERNET</label>
  <input type="radio" id="friend/relative" name="how" value="FRIEND/RELATIVE">
  <label for="friend/relative">FRIEND/RELATIVE</label>
  <input type="radio" id="ourstudent" name="how" value="OURSTUDENT">
  <label for="ourstudent">OURSTUDENT</label><br>
  <label for="addate">Admission Date:</label>
  <input type="date" id="addate" name="addate"><br>
  <label for="sign">Signature</label>
  <input type="text" id="sign" name="sign"><br>

  <input type="button" onclick="alert('Details Submitted')" value="submit">
</form>

</body>
</html>
```

Output:

![image](https://github.com/user-attachments/assets/a0e7e1cd-35e5-47fc-8684-1e7f18b71f07)
