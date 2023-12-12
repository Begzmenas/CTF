<!DOCTYPE html>
<html>
<head>
    <title>CTF Site</title>
    <style>
        /* Add your site's CSS here */
    </style>
</head>
<body>
    <h1>Welcome to the CTF Site!</h1>
    <p>Here are some challenges you can try:</p>

    <!DOCTYPE html>
<html>
<head>
    <title>Simple CTF Site</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }

        .challenge {
            border: 1px solid #ccc;
            border-radius: 4px;
            padding: 15px;
            margin-bottom: 10px;
        }

        .challenge h3 {
            margin-top: 0;
        }
    </style>
</head>
<body>
    <h1>Welcome to the Simple CTF Site!</h1>
    <p>Below are 5 challenges. Solve them and enter the flag in the corresponding input box to get the flag.</p>

    <div class="challenge">
        <h3>Challenge 1</h3>
        <p>What is the first letter of the alphabet?</p>
        <input type="text" id="flag1" name="flag1" placeholder="Enter the flag">
        <button onclick="checkFlag1()">Submit</button>
        <script>
            function checkFlag1() {
                var flag1 = document.getElementById('flag1').value.toLowerCase();
                if (flag1 === 'o') {
                    alert('Correct!');
                } else {
                    alert('Incorrect. Try again.');
                }
            }
        </script>
    </div>

    <!DOCTYPE html>
<html>
<head>
    <title>CTF Challenge</title>
    <style>
        /* Add your challenge's CSS here */
    </style>
</head>
<body>
    <!DOCTYPE html>
<html>
<head>
    <title>Challenge 2</title>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
</head>
<body>
    <h1>Challenge 2</h1>
    <p>The flag is hidden within the HTML comments. Good luck!</p>

    <script>
        function submitFlag() {
            var flag = document.getElementById('flag').value;
            var xhr = new XMLHttpRequest();
            xhr.open('POST', '/submit', true);
            xhr.setRequestHeader('Content-Type', 'application/json');
            xhr.onreadystatechange = function () {
                if (xhr.readyState === 4 && xhr.status === 200) {
                    var result = JSON.parse(xhr.responseText);
                    if (result.correct) {
                        alert('Congratulations! The flag is correct.');
                    } else {
                        alert('Sorry, the flag you submitted is incorrect. Please try again.');
                    }
                }
            };
            xhr.send(JSON.stringify({ 'flag': flag }));
        }
    </script>

    <label for="flag">Enter the flag:</label>
    <input type="text" id="flag" name="flag">
    <button onclick="submitFlag()">Submit</button>
</body>
</html>

    <!-- 
        Hidden Flag: {your flag here}
    -->
</body>
</html>

</body>
</html>

   <!DOCTYPE html>
<html>
<head>
 <title>Basic CTF Challenge</title>
 <style>
    #password { display: none; }
 </style>
</head>
<body>
 <h1>Challenge 3</h1>
 <p>The hidden password is: <span id="password">SuperSecretPassword123</span></p>

 <h2>Enter the password to continue:</h2>
 <form>
    <input type="text" id="user_password" required>
    <button type="submit">Submit</button>
 </form>

 <script>
    const form = document.querySelector('form');
    const password = document.getElementById('password').textContent;
    const user_password = document.getElementById('user_password');

    form.addEventListener('submit', (event) => {
      event.preventDefault();
      if (user_password.value === password) {
        alert('Congratulations! You found the password.');
      } else {
        alert('Incorrect password. Please try again.');
      }
    });
 </script>
</body>
</html>

</body>
</html>
