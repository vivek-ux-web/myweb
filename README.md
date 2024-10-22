<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cyber Awareness</title>
    <style>
        body {
            background-color: black;
            color: lime;
            font-family: Arial, sans-serif;
            overflow: hidden;
        }
        .container {
            text-align: center;
            padding: 50px;
            position: relative;
        }
        #popup {
            display: none;
            position: fixed;
            left: 50%;
            top: 50%;
            transform: translate(-50%, -50%);
            background: rgba(0, 0, 0, 0.8);
            border: 2px solid lime;
            padding: 20px;
            z-index: 1000;
            animation: fadeIn 0.5s;
        }
        #overlay {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
            z-index: 999;
        }
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        .moving-text {
            animation: moveText 5s infinite;
            white-space: nowrap;
            font-size: 1.5em;
        }
        @keyframes moveText {
            from { transform: translateX(100%); }
            to { transform: translateX(-100%); }
        }
    </style>
</head>
<body>

<div class="container">
    <h1>Welcome to the Cyber Awareness Portal</h1>
    <button onclick="showPopup()">Check Your Security</button>
</div>

<div id="overlay"></div>
<div id="popup">
    <h2>YOU HAVE BEEN HACKED!</h2>
    <p class="moving-text">Bank Account: 1234-5678-9101 | Balance: $0.00 | Transaction: Unauthorized Access</p>
    <p>Be aware of your digital security!</p>
    <button onclick="closePopup()">Close</button>
</div>

<script>
    function showPopup() {
        document.getElementById('popup').style.display = 'block';
        document.getElementById('overlay').style.display = 'block';
    }

    function closePopup() {
        document.getElementById('popup').style.display = 'none';
        document.getElementById('overlay').style.display = 'none';
        alert("SATARK RAHE! Stay aware of cyber crimes.");
    }
</script>

</body>
</html>
