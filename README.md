<!DOCTYPE html>
<html lang="vi">

<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Website Wireframe Design</title>

<style>

body{
font-family: Arial, sans-serif;
margin:40px;
background:#f5f5f5;
line-height:1.6;
}

.container{
max-width:900px;
margin:auto;
background:white;
padding:30px;
border-radius:10px;
}

h1{
text-align:center;
}

.section{
margin-top:40px;
}

.wireframe{
border:2px solid black;
padding:20px;
margin-top:20px;
}

.box{
border:2px solid black;
text-align:center;
padding:20px;
margin:10px 0;
}

.grid{
display:grid;
grid-template-columns:1fr 1fr;
gap:10px;
}

</style>

</head>


<body>

<div class="container">

<h1>Responsive Website Wireframe</h1>

<p>
Before building my responsive website, I created wireframes to plan the layout and structure.
Wireframes help organize content and show how the website will appear on different devices.
This design includes two viewing modes: mobile view and large screen view.
</p>

<p>
The mobile layout uses a single column to make the content easy to read on smaller screens.
The larger screen layout uses multiple columns to better use the available space and display
images and text more efficiently.
</p>

<div class="section">

<h2>Mobile View Wireframe</h2>

<div class="wireframe">

<div class="box">HEADER</div>

<div class="box">IMAGE</div>
<div class="box">TEXT</div>

<div class="box">IMAGE</div>
<div class="box">TEXT</div>

<div class="box">IMAGE</div>
<div class="box">TEXT</div>

</div>

</div>


<div class="section">

<h2>Large Screen View Wireframe</h2>

<div class="wireframe">

<div class="box">HEADER</div>

<div class="grid">
<div class="box">IMAGE</div>
<div class="box">IMAGE</div>
</div>

<div class="grid">
<div class="box">TEXT</div>
<div class="box">TEXT</div>
</div>

<div class="grid">
<div class="box">IMAGE</div>
<div class="box">IMAGE</div>
</div>

</div>

</div>

</div>

</body>
</html>
