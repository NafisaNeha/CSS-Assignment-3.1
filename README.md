# CSS-Assignment-3.1
body{
    text-align: center;   
}
h1{
    font-size: 40px;
    font-weight: 300;
    margin-bottom: 0px;
}
h2{
    font-size: 18px;
    font-weight: 300;
}
p{
    font-size: 16px;
    color: #BDBDBD;
}

.container{
	
	width: 50%;
	margin: 0px auto;
	overflow: hidden;
	border: 1px solid;
    background-color: #C3C3C3;

	
}
.s_file{
	float: left;
	width: 25%;
	/* border: 1px solid red; */
	margin-top: 20px;
    margin-bottom: 20px;  
    margin-left: 45px;
    background-color: white;
	
}
.s_file img{
	width: 100%;
    
}









table {
    margin-left: 25%;
  }
  h2{
    text-align: left;
    margin-left: 10%;
  }

  
  th,
  td {
    padding: 8px;
    text-align: center;
    border: 1px solid rgb(216, 129, 129);
  }
  .prime {
    background-color: rgb(228, 132, 132);
  }

  
  
  
  
  
  <!DOCTYPE html>
<html>
<head>
  <title>Prime Numbers</title>
  <link rel="stylesheet" href="css/style.css">
</head>
<body>
   
  <?php
  function isPrime($num) {
    if ($num < 2) {
      return false;
    }
    for ($i = 2; $i <= sqrt($num); $i++) {
      if ($num % $i === 0) {
        return false;
      }
    }
    return true;
  }

  $start = 1; 
  $end = 100; 

  echo "<h2> Prime Numbers : </h2>";
  echo "<table>";
  echo "<tr><th>Number</th><th>Prime?</th></tr>";

  for ($num = $start; $num <= $end; $num++) {
    $primeClass = isPrime($num) ? 'prime' : '';
    echo "<tr><td>$num</td><td class='$primeClass'>" . (isPrime($num) ? 'YES' : 'No') . "</td></tr>";
  }

  echo "</table>";
  ?>
 
</body>
</html>
