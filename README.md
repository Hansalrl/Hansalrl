<!-- Skill Menu -->
<div align="center">
  <h2>Skill</h2>
  <p>Select a skill category:</p>
  <nav>
    <a href="#frontend" class="menu-item">Frontend</a>
    <a href="#backend" class="menu-item">Backend</a>
    <a href="#database" class="menu-item">Database</a>
  </nav>
</div>

<!-- About Me Menu -->
<div align="center">
  <h2>About Me</h2>
  <p>Select a topic:</p>
  <nav>
    <a href="#bio" class="menu-item">Bio</a>
    <a href="#education" class="menu-item">Education</a>
    <a href="#hobbies" class="menu-item">Hobbies</a>
  </nav>
</div>

<!-- Styling for the menu -->
<style>
  .menu-item {
    display: inline-block;
    margin: 0 10px;
    padding: 10px 20px;
    background-color: #6c63ff;
    color: white;
    border-radius: 5px;
    cursor: pointer;
    transition: all 0.3s ease-in-out;
  }

  .menu-item:hover {
    transform: scale(1.1);
    background-color: #ff5e5e;
  }

  nav {
    display: inline-block;
    margin-top: 10px;
    position: relative;
  }

  nav::before {
    content: "";
    position: absolute;
    width: 0;
    height: 0;
    border-top: 10px solid transparent;
    border-bottom: 10px solid transparent;
    border-right: 10px solid #6c63ff;
    left: -15px;
    top: 10px;
    transition: all 0.3s ease-in-out;
  }

  nav:hover::before {
    border-right: 10px solid #ff5e5e;
  }
</style>

<!-- JavaScript for the random arrow colors -->
<script>
  // Select all the menu items
  const menuItems = document.querySelectorAll(".menu-item");

  // Define the colors to choose from
  const colors = [
    "#6c63ff",
    "#ff5e5e",
    "#2cb67d",
    "#f6c85f",
    "#9b59b6",
    "#e74c3c",
    "#3498db",
    "#1abc9c",
    "#f1c40f",
    "#95a5a6"
  ];

  // Loop through the menu items and assign a random color to each arrow
  menuItems.forEach(item => {
    const arrow = item.parentNode.parentNode.querySelector("nav::before");
    const color = colors[Math.floor(Math.random() * colors.length)];
    arrow.style.borderRightColor = color;
    item.style.backgroundColor = color;
  });
</script>

<!-- Last updated: yyyy-mm-dd -->
<p align="right"><em>Last updated: 2023-03-27</em></p>

