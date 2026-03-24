<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Portfolio</title>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial;
    }

    body {
      background: #f5f5f5;
      color: #333;
      transition: 0.3s;
    }

    .dark {
      background: #121212;
      color: #fff;
    }

    /* NAV */
    nav {
      display: flex;
      justify-content: space-between;
      padding: 15px 30px;
      background: #222;
      color: white;
      position: sticky;
      top: 0;
    }

    nav ul {
      display: flex;
      gap: 20px;
      list-style: none;
    }

    nav a {
      color: white;
      text-decoration: none;
    }

    button {
      cursor: pointer;
      padding: 5px 10px;
    }

    /* HERO */
    #home {
      height: 90vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
    }

    #home h1 {
      font-size: 40px;
    }

    /* SECTIONS */
    section {
      padding: 60px 20px;
      text-align: center;
      opacity: 0;
      transform: translateY(30px);
      transition: 0.6s;
    }

    section.show {
      opacity: 1;
      transform: translateY(0);
    }

    /* PROJECTS */
    .projects {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
    }

    .card {
      background: white;
      padding: 20px;
      margin: 10px;
      border-radius: 10px;
      width: 200px;
      box-shadow: 0 5px 10px rgba(0,0,0,0.1);
    }

    .dark .card {
      background: #1e1e1e;
    }

    /* FORM */
    input, button {
      padding: 10px;
      margin: 10px;
    }

    /* RESPONSIVE */
    @media (max-width: 600px) {
      nav ul {
        flex-direction: column;
      }
    }
  </style>
</head>

<body>

  <!-- NAV -->
  <nav>
    <h2>Portfolio</h2>
    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
    <button id="toggle">🌙</button>
  </nav>

  <!-- HOME -->
  <section id="home" class="show">
    <h1>Xin chào 👋</h1>
    <p>Tôi là Web Developer</p>
  </section>

  <!-- ABOUT -->
  <section id="about">
    <h2>Giới thiệu</h2>
    <p>Tôi có kỹ năng HTML, CSS, JavaScript và xây dựng website responsive.</p>
  </section>

  <!-- PROJECTS -->
  <section id="projects">
    <h2>Dự án</h2>
    <div class="projects">
      <div class="card">Website bán hàng</div>
      <div class="card">Portfolio cá nhân</div>
      <div class="card">Landing page</div>
    </div>
  </section>

  <!-- CONTACT -->
  <section id="contact">
    <h2>Liên hệ</h2>
    <form id="form">
      <input type="text" id="name" placeholder="Tên">
      <input type="email" id="email" placeholder="Email">
      <br>
      <button type="submit">Gửi</button>
    </form>
    <p id="msg"></p>
  </section>

  <script>
    // DARK MODE
    document.getElementById("toggle").onclick = () => {
      document.body.classList.toggle("dark");
    };

    // FORM VALIDATION
    document.getElementById("form").addEventListener("submit", function(e){
      e.preventDefault();

      let name = document.getElementById("name").value;
      let email = document.getElementById("email").value;
      let msg = document.getElementById("msg");

      if(name === "" || email === ""){
        msg.innerText = "Vui lòng nhập đầy đủ!";
        msg.style.color = "red";
      } else {
        msg.innerText = "Gửi thành công!";
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
