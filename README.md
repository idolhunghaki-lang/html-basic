<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Portfolio của tôi</title>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial;
    }

    body {
      background: white;
      color: black;
      transition: 0.3s;
    }

    .dark {
      background: #111;
      color: white;
    }

    /* NAV */
    nav {
      display: flex;
      justify-content: space-between;
      padding: 15px;
      background: #333;
      color: white;
    }

    ul {
      display: flex;
      gap: 15px;
      list-style: none;
    }

    a {
      color: white;
      text-decoration: none;
    }

    button {
      cursor: pointer;
      padding: 5px 10px;
    }

    /* SECTIONS */
    section {
      padding: 60px;
      text-align: center;
    }

    /* PROJECT */
    .card {
      background: #eee;
      margin: 10px;
      padding: 20px;
      border-radius: 10px;
      display: inline-block;
    }

    .dark .card {
      background: #222;
    }

    /* FORM */
    input, button {
      margin: 10px;
      padding: 10px;
    }

    /* ANIMATION */
    section {
      opacity: 0;
      transform: translateY(30px);
      transition: 0.6s;
    }

    section.show {
      opacity: 1;
      transform: translateY(0);
    }

    /* RESPONSIVE */
    @media (max-width: 600px) {
      ul {
        flex-direction: column;
      }
    }
  </style>
</head>

<body>

  <!-- NAVBAR -->
  <nav>
    <h1>My Portfolio</h1>
    <ul>
      <li><a href="#home">Trang chủ</a></li>
      <li><a href="#about">Giới thiệu</a></li>
      <li><a href="#projects">Dự án</a></li>
      <li><a href="#contact">Liên hệ</a></li>
    </ul>
    <button id="toggle">🌙</button>
  </nav>

  <!-- HOME -->
  <section id="home">
    <h2>Xin chào 👋</h2>
    <p>Tôi là sinh viên IT</p>
  </section>

  <!-- ABOUT -->
  <section id="about">
    <h2>Giới thiệu</h2>
    <p>Tôi biết HTML, CSS, JavaScript</p>
  </section>

  <!-- PROJECTS -->
  <section id="projects">
    <h2>Dự án</h2>
    <div class="card">Website 1</div>
    <div class="card">Website 2</div>
  </section>

  <!-- CONTACT -->
  <section id="contact">
    <h2>Liên hệ</h2>
    <form id="form">
      <input type="text" id="name" placeholder="Tên của bạn">
      <input type="email" id="email" placeholder="Email">
      <br>
      <button type="submit">Gửi</button>
    </form>
    <p id="msg"></p>
  </section>

  <script>
    // DARK MODE
    const toggle = document.getElementById("toggle");
    toggle.onclick = () => {
      document.body.classList.toggle("dark");
    };

    // FORM VALIDATION
    const form = document.getElementById("form");
    const msg = document.getElementById("msg");

    form.addEventListener("submit", function(e) {
      e.preventDefault();

      let name = document.getElementById("name").value;
      let email = document.getElementById("email").value;

      if (name === "" || email === "") {
        msg.textContent = "Vui lòng nhập đầy đủ!";
        msg.style.color = "red";
      } else {
        msg.textContent = "Gửi thành công!";
        msg.style.color = "green";
      }
    });

    // SCROLL ANIMATION
    const sections = document.querySelectorAll("section");

    window.addEventListener("scroll", () => {
      sections.forEach(sec => {
        const top = sec.getBoundingClientRect().top;
        if (top < window.innerHeight - 50) {
          sec.classList.add("show");
        }
      });
    });
  </script>

</body>
</html>
