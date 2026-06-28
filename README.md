<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>AJAX Travel Destination Explorer</title>

<script src="https://code.jquery.com/jquery-3.7.1.min.js"></script>

<style>

body{
    margin:0;
    font-family:Arial, Helvetica, sans-serif;
    background:linear-gradient(135deg,#4facfe,#00f2fe);
}

.container{
    width:85%;
    margin:40px auto;
    background:white;
    border-radius:15px;
    padding:30px;
    box-shadow:0 0 20px rgba(0,0,0,.3);
}

h1{
    text-align:center;
    color:#0d6efd;
}

.subtitle{
    text-align:center;
    color:#666;
    margin-bottom:30px;
}

.buttons{
    text-align:center;
}

button{
    padding:12px 22px;
    margin:10px;
    border:none;
    border-radius:8px;
    cursor:pointer;
    color:white;
    font-size:16px;
    transition:.3s;
}

button:hover{
    transform:scale(1.05);
}

#paris{
    background:#e63946;
}

#tokyo{
    background:#6f42c1;
}

#kenya{
    background:#198754;
}

#content{
    margin-top:30px;
    padding:25px;
    border-radius:10px;
    background:#f8f9fa;
    border-left:8px solid #0d6efd;
    line-height:1.8;
    min-height:220px;
}

footer{
    text-align:center;
    margin-top:30px;
    color:#666;
}

</style>

<script>

$(document).ready(function(){

    // Load Paris information
    $("#paris").click(function(){

        $("#content").load("paris.txt");

    });

    // Load Tokyo information
    $("#tokyo").click(function(){

        $("#content").load("tokyo.txt");

    });

    // Load Kenya information
    $("#kenya").click(function(){

        $("#content").load("kenya.txt");

    });

});

</script>

</head>

<body>

<div class="container">

<h1>🌍 AJAX Travel Destination Explorer</h1>

<p class="subtitle">
Explore exciting travel destinations. Information is loaded using AJAX without refreshing the webpage.
</p>

<!--
AJAX Demonstration

This application uses jQuery's .load() method to retrieve information
from external text files.

When a destination button is clicked:

• An AJAX request is sent.
• Only the information panel is updated.
• The webpage does not reload.
• This creates a smoother user experience.

-->

<div class="buttons">

<button id="paris">🇫🇷 Paris</button>

<button id="tokyo">🇯🇵 Tokyo</button>

<button id="kenya">🇰🇪 Kenya</button>

</div>

<div id="content">

<h2>Welcome!</h2>

<p>

Click any destination above to discover interesting facts about it.

Notice that only this section changes while the rest of the webpage stays exactly the same. This is the power of AJAX.

</p>

</div>

<footer>

Created as an AJAX demonstration using jQuery.

</footer>

</div>

</body>
</html>
