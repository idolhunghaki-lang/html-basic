<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<title>Responsive Homework</title>

<style>

/* ====== Mobile (mặc định) ====== */

body {
    margin: 0;
    font-family: Arial, sans-serif;
}

.container {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.item {
    width: 90%;
    margin: 10px 0;
    padding: 10px;
    border: 1px solid #ccc;
    text-align: center;
}

img {
    width: 100%;
    height: auto;
}


/* ====== Tablet View ====== */
@media screen and (min-width: 772px) {

    .container {
        flex-direction: row;
        flex-wrap: wrap;
        justify-content: space-around;
    }

    .item {
        width: 45%;
    }

    img {
        max-height: 30vh;
        object-fit: cover;
    }
}


/* ====== Large Screen View ====== */
@media screen and (min-width: 998px) {

    .item {
        width: 30%;
    }

}

</style>
</head>

<body>

<div class="container">

   <div class="item">
        <h2>Item 1</h2>
        <img src="https://picsum.photos/400/300?random=1">
        <p>Nội dung mô tả 1</p>
    </div>

  <div class="item">
        <h2>Item 2</h2>
        <img src="https://picsum.photos/400/300?random=2">
        <p>Nội dung mô tả 2</p>
    </div>

   <div class="item">
        <h2>Item 3</h2>
        <img src="https://picsum.photos/400/300?random=3">
        <p>Nội dung mô tả 3</p>
    </div>

</div>

</body>
</html>
