# Sudarshan-Das
index.html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Sudarshan Das Portfolio</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header>
    <h1>Welcome to Sudarshan Das' Portfolio</h1>
  </header>
  <section id="about">
    <h2>About Me</h2>
    <p>Experienced in sales, freelance work, and skilled in mobile electronics and design.</p>
  </section>
  <section id="portfolio">
    <h2>Portfolio</h2>
    <!-- Add your work examples here -->
  </section>
  <section id="experience">
    <h2>Experience</h2>
    <p>Sage Ayurveda, Bajaj Allianz,...</p>
  </section>

  <section id="contact">
    <h2>Contact</h2>
    <form action="https://formspree.io/your-email" method="POST">
      <input type="email" name="email" placeholder="Your Email">
      <textarea name="message" placeholder="Your Message"></textarea>
      <button type="submit">Send</button>
    </form>
  </section>
  <script src="script.js"></script>
</body>
</html>
styles.css
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background: linear-gradient(120deg, #fdfbfb 0%, #ebedee 100%);
}

header {
  text-align: center;
  padding: 50px;
  background-color: #282c34;
  color: white;
  font-size: 2rem;
}

section {
  padding: 40px;
}

#about, #portfolio, #experience, #contact {
  background: #fff;
  box-shadow: 0 10px 20px rgba(0,0,0,0.1);
  margin: 20px;
  border-radius: 10px;
  text-align: center;
}
<canvas id="canvas"></canvas>
<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
<script>
  const scene = new THREE.Scene();
  const camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);

  const renderer = new THREE.WebGLRenderer({ canvas: document.querySelector("#canvas") });
  renderer.setSize(window.innerWidth, window.innerHeight);
  
  const geometry = new THREE.BoxGeometry();
  const material = new THREE.MeshBasicMaterial({ color: 0x00ff00 });
  const cube = new THREE.Mesh(geometry, material);
  
  scene.add(cube);
  camera.position.z = 5;

  function animate() {
    requestAnimationFrame(animate);
    cube.rotation.x += 0.01;
    cube.rotation.y += 0.01;
    renderer.render(scene, camera);
  }
  
  animate();
</script>
