<!DOCTYPE html>
<html>
<head>
	<title>Registration Form</title>
	<link rel="stylesheet" type="text/css" href="styl.css">
</head>
<body class="body-class">
	<h1 align="center" style="color:DodgerBlue;">Registration Form</h1>
		<form name="myform" onsubmit="return(validateForm())">
			<table border="0" align="center">
				<tr>
				
					<td align="right">
						<label for="userid">Userid:</label>
					</td>
					<td>
						<input type="text" name="id" id="userid" placeholder="minimum5-maximum12" required />
					</td>
				</tr>
				<tr>
					<td align="right">
						<label for="password">Password:</label>
					</td>
					<td>
						<input type="password" name="pass" id="password" placeholder="minimum7-maximum12" required />
					</td>
				</tr>
				<tr>
					<td align="right">
						<label for="name">Name:</label>
					</td> 
					<td>
						<input type="text" name="nam" id="name" placeholder="Only Alphabates" required />
					</td>
				</tr>
				<tr>
					<td align="right">
						<label for="address">Address:</label>
					</td>
					<td>
						<input type="text" id="address" placeholder="Optional" />
					</td>
				</tr>
				<tr>
					<td align="right">
						<label for="country">Country:</label>
					</td>
					<td>
						<select name="country">
							<option selected>America</option>
							<option>Belgium</option>
							<option>Canada</option>
							<option>Denmark</option>
							<option>England</option>
							<option>France</option>
							<option>Germany</option>
							<option>Hungary</option>
							<option>India</option>
						</select>
					</td>
				</tr>
				<tr>
					<td align="right">
						<label  for="zip code">ZIP code:</label>
					</td>
					<td>
						<input type="text" name="numb" id="zip code" placeholder="Only Numbers" required />
					</td>
				</tr>
				<tr>
					<td align="right">
						<label for="email">Email:</label>
					</td>
					<td>
						<input type="text" id="email" placeholder="example01@gmail.com" required />
					</td>
				</tr>
				<tr>
					<td align="right">
						<label for="sex">Sex:</label>
					</td>
					<td>
						<label>
						<input name="sex" type="radio" value="Male" />Male<br><input name="sex" type="radio" value="Female" />Female</label>
					</td>
				</tr>
				<tr>
					<td align="right">
						<label for="language">Language:</label>
					</td>
					<td>
						<input type="checkbox" name="language" value="English">English</input><input type="checkbox" name="language" value="Non English">Non English</input>
					</td>
				</tr>
				<tr>
					<td align="right">
						<label for="textarea">About:</label>
					</td>
					<td>
						<textarea placeholder="Optional" rows="5" cols="19">
						</textarea>
					</td>
				</tr>
					<td colspan="2" align="center">
							<input type="Submit" name="submit" value="Register" class="button-class"> 
					</td>
				</tr>
			</table>
		</form>
	<script type="text/javascript">
		function validateForm() {
			if (document.myform.id.value.length > 4 && document.myform.id.value.length < 13) {
			}else{
				alert("Enter required length..");
			}
			if (document.myform.pass.value.length > 7 && document.myform.pass.value.length < 13) {

			}else{
				alert("Enter required length..");
			}
			var letter1=document.myform.nam.value;
			var letter2=/^[a-zA-Z]+$/;
			if (letter1.match(letter2))  {

			}else{
				alert("Enter only alphabets..");
			}
			var number1=document.myform.numb.value;
			var number2=/^[0-9]+$/;
			if (number1.match(number2)) {

			}else{
				alert("Enter only numbers..");
			}
			return(true);
			window.alert("Registration succesfully completed..!");
		}
	</script>
</body>
</html>
