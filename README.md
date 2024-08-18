<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login Page</title>
    <link rel="stylesheet" href="asignment.css">
</head>
<body>
    <div class="container">
        <h1>Login Page</h1>

        <!-- Login Form -->
        <form id="login-form">
            <input type="email" id="email" placeholder="Email" required>
            <input type="password" id="password" placeholder="Password" required>
            <button type="submit" id="submit-btn">Submit</button>
            <button type="button" id="register-btn">Register</button>
        </form>

        <!-- Registration Form -->
        <div id="registration-form" style="display: none;">
            <h2>Registration Form</h2>
            <form id="register-form">
                <label for="name">Name:</label>
                <input type="text" id="name" name="name" placeholder="Name" required>
                
                <label for="contact">Contact:</label>
                <input type="number" id="contact" name="contact" placeholder="Contact" required>
                
                <label for="dob">Date of Birth:</label>
                <input type="date" id="dob" name="dob" required>
                
                <label for="address">Address:</label>
                <textarea id="address" name="address" placeholder="Address" required></textarea>
                
                <label for="email">Email:</label>
                <input type="email" id="register-email" name="email" placeholder="Email" required>
                
                <label for="gender">Gender:</label>
                <div id="gender-group">
                    <input type="radio" id="male" name="gender" value="male" required>
                    <label for="male">Male</label>
                    <input type="radio" id="female" name="gender" value="female" required>
                    <label for="female">Female</label>
                </div>
                
                <label for="stream">Stream:</label>
                <select id="stream" name="stream" required>
                    <option value="b.tech">B.Tech</option>
                    <option value="m.tech">M.Tech</option>
                    <option value="b.voc">B.Voc</option>
                </select>

                <button type="submit" id="register-submit-btn">Submit</button>
            </form>
        </div>
    </div>

    <script>
        // Toggle between login and registration forms
        document.getElementById('register-btn').addEventListener('click', function() {
            document.getElementById('login-form').style.display = 'none';
            document.getElementById('registration-form').style.display = 'block';
        });

        // Handle form submission
        document.getElementById('register-form').addEventListener('submit', function(event) {
            event.preventDefault(); // Prevent actual form submission

            // Get form data
            const formData = new FormData(this);

            // Perform form submission (e.g., via AJAX)
            console.log('Form submitted:', Object.fromEntries(formData));

            // Optionally reset the form
            this.reset();
        });
    </script>
</body>
</html>
