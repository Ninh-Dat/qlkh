<!doctype html>
<html>
<head>
<meta charset="utf-8">
<title>Untitled Document</title>
</head>

<body>
	<?php
	$conn=mysqli_connect("localhost","root","12345678","qlts");
	mysqli_query($conn,"set names utf8");
	$mats=$_POST["ma"];
	$hoten=$_POST["hoten"];
	$khoi=$_POST["khoi"];
	$diemtoan=$_POST["diemtoan"];
	$diemvan=$_POST["diemvan"];
	$diemngoaingu=$_POST["diemngoaingu"];
	
	$sql=" INSERT INTO thisinh2020 VALUES('$mats','$hoten','$khoi','$diemtoan','$diemvan','$diemngoaingu')";
	$query= mysqli_query($conn, $sql);
	mysqli_close($conn);
	?>
<form action="" method="post">
<table border="1" >
	<tr>
		<td align="center" colspan="2">Thêm</td>
	</tr>
	<tr>
		<td>Mã TS
		<td><input type="text" name="ma"/></td>
	</tr>
	<tr>
		<td>Họ Tên</td>
		<td><input type="text" name="hoten"/></td>
	</tr>
	<tr>
		<td>Khối</td>
		<td><input type="text" name="khoi"/></td>
	</tr>
	<tr>
		<td>Điểm toán</td>
		<td><input type="text" name="diemtoan"/></td>
	</tr>
	<tr>
		<td>Điểm văn</td>
		<td><input type="text" name="diemvan"/></td>
	</tr>
		<tr>
		<td>Điểm ngoại ngữ</td>
		<td><input type="text" name="diemngoaingu"/></td>
	</tr>
	<tr>
		<td align="center" colspan="2"><input type="submit" value="Nhập"/></td>
	</tr>
</table>
</form>
</body>
</html>
