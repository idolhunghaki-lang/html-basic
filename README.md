<html lang="vi">

<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Responsive Final Project</title>

<style>

body{
font-family: Arial, sans-serif;
margin:0;
text-align:center;
}

header{
padding:20px;
}

.gallery{
display:grid;
grid-template-columns:1fr;
gap:10px;
padding:10px;
}

.item{
border:2px solid #ccc;
padding:10px;
}

img{
width:100%;
height:auto;
}


/* TABLET VIEW */

@media (min-width:772px){

.gallery{
grid-template-columns:1fr 1fr;
}

img{
border-radius:50%;
}

.item:last-child{
grid-column:span 2;
}

}


/* LARGE SCREEN */

@media (min-width:992px){

.item:nth-child(3n){
grid-column:span 2;
}

img{
border-radius:0;
}

}


/* REDUCED MOTION */

@media (prefers-reduced-motion: reduce){

*{
scroll-behavior:auto;
animation:none;
transition:none;
}

}


/* DARK MODE */

@media (prefers-color-scheme: dark){

body{
background:#111;
color:#eee;
}

.item{
background:#333;
border-color:black;
}

img{
background:#222;
}

}

</style>

</head>

<body>

<header>
<h1>My Photo Gallery</h1>
<p>Responsive Web Design Project</p>
</header>

<main class="gallery">

<div class="item">
<img src="img1.jpg" alt="Mountain landscape">
<p>Beautiful mountain landscape.</p>
</div>

<div class="item">
<img src="img2.jpg" alt="Ocean beach">
<p>Relaxing beach view.</p>
</div>

<div class="item">
<img src="img3.jpg" alt="Forest trees">
<p>Peaceful forest scenery.</p>
</div>

<div class="item">
<img src="img4.jpg" alt="City skyline">
<p>Modern city skyline.</p>
</div>

<div class="item">
<img src="img5.jpg" alt="Desert dunes">
<p>Golden desert dunes.</p>
</div>

<div class="item">
<img src="img6.jpg" alt="Snow mountains">
<p>Snow covered mountains.</p>
</div>

</main>

</body>
</html>
