<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Gourav Flex Journey</title>
  <style>
    html {
      scroll-behavior: smooth;
    }
    body {
      font-family: 'Poppins', sans-serif;
      margin: 0;
      padding: 0;
      background: linear-gradient(180deg, #0a0a0a, #1a1a1a);
      color: #fff;
      text-align: center;
      overflow-x: hidden;
    }
    /* Loader Screen */
    #loader {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: #0a0a0a;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      z-index: 9999;
    }
    #loader h1 {
      font-size: 2.2em;
      background: linear-gradient(90deg, #ff5733, #ff914d);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      animation: pulse 1.5s infinite;
    }
    @keyframes pulse {
      0%, 100% { opacity: 1; }
      50% { opacity: 0.5; }
    }
    #loader .bar {
      width: 150px;
      height: 8px;
      background: #333;
      border-radius: 5px;
      overflow: hidden;
      margin-top: 20px;
    }
    #loader .bar::before {
      content: '';
      display: block;
      height: 100%;
      width: 0;
      background: linear-gradient(90deg, #ff5733, #ff914d);
      animation: loading 2.5s forwards;
    }
    @keyframes loading {
      from { width: 0; }
      to { width: 100%; }
    }

    header {
      background: linear-gradient(90deg, #ff5733, #ff914d);
      padding: 25px;
      font-size: 2em;
      font-weight: bold;
      letter-spacing: 1px;
      animation: slideDown 1s ease;
    }
    @keyframes slideDown {
      from {transform: translateY(-100%); opacity: 0;}
      to {transform: translateY(0); opacity: 1;}
    }
    nav {
      margin-top: 10px;
      animation: fadeIn 2s ease;
    }
    nav a {
      text-decoration: none;
      color: #fff;
      margin: 0 15px;
      font-weight: 600;
      transition: color 0.3s, transform 0.3s;
    }
    nav a:hover {
      color: #ff914d;
      transform: scale(1.1);
    }
    section {
      padding: 40px 20px;
      max-width: 900px;
      margin: auto;
      animation: fadeInUp 1s ease;
      transition: transform 0.5s;
    }
    section.pulse {
      transform: scale(1.02);
      box-shadow: 0 0 30px rgba(255,145,77,0.5);
    }
    @keyframes fadeInUp {
      from {opacity: 0; transform: translateY(40px);}
      to {opacity: 1; transform: translateY(0);}
    }
    h2 {
      color: #ff914d;
      margin-bottom: 15px;
    }
    .exercise, .nutrition {
      text-align: left;
      background: #111;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 0 15px rgba(255,145,77,0.5);
      margin-bottom: 30px;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }
    .exercise:hover, .nutrition:hover {
      transform: translateY(-5px);
      box-shadow: 0 0 25px rgba(255,145,77,0.7);
    }
    button {
      background: #ff914d;
      border: none;
      color: white;
      padding: 15px 30px;
      font-size: 1em;
      border-radius: 30px;
      cursor: pointer;
      transition: 0.3s;
    }
    button:hover {
      background: #ff5733;
      transform: scale(1.05);
      box-shadow: 0 0 20px rgba(255,145,77,0.6);
    }
    footer {
      background: #111;
      padding: 20px;
      font-size: 0.9em;
      color: #bbb;
      animation: fadeIn 2s ease;
    }
    @keyframes fadeIn {
      from {opacity: 0;}
      to {opacity: 1;}
    }
    /* Music Control */
    #musicControl {
      position: fixed;
      bottom: 20px;
      right: 20px;
      background: rgba(255,145,77,0.8);
      border: none;
      color: #111;
      padding: 12px 18px;
      font-weight: bold;
      border-radius: 30px;
      cursor: pointer;
      z-index: 10000;
      transition: transform 0.3s, background 0.3s;
    }
    #musicControl:hover {
      transform: scale(1.1);
      background: rgba(255,87,51,0.9);
    }
  </style>
</head>
<body>
  <!-- Loader Screen -->
  <div id="loader">
    <h1>Welcome to Gourav Flex Journey</h1>
    <div class="bar"></div>
  </div>

  <header>Gourav Flex Journey</header>
  <nav>
    <a href="#home">Home</a>
    <a href="#exercises">Exercises</a>
    <a href="#nutrition">Nutrition</a>
    <a href="#contact">Contact</a>
  </nav>

  <section id="home">
    <h2>Welcome to Gourav Flex Journey</h2>
    <p>Join Gourav, a passionate 16-year-old fitness enthusiast from India, on his path to becoming a professional bodybuilder. This website shares his workouts, routines, and diet insights to help you build strength, muscle, and confidence.</p>
  </section>

  <section id="exercises">
    <h2>Gym & Home Exercises</h2>
    <div class="exercise">
      <h3>🏋️‍♂️ Chest</h3>
      <ul>
        <li>Bench Press – Builds overall chest strength and size.</li>
        <li>Incline Dumbbell Press – Focuses on the upper chest.</li>
        <li>Push-ups – A great home workout for chest and arms.</li>
      </ul>
    </div>

    <div class="exercise">
      <h3>💪 Biceps & Triceps</h3>
      <ul>
        <li>Bicep Curls – Perfect for arm thickness and definition.</li>
        <li>Hammer Curls – Focuses on forearm development.</li>
        <li>Tricep Dips – Builds triceps and chest strength.</li>
      </ul>
    </div>

    <div class="exercise">
      <h3>🦵 Legs</h3>
      <ul>
        <li>Squats – The king of leg exercises for muscle growth.</li>
        <li>Lunges – Great for balance and glute development.</li>
        <li>Leg Press – Strengthens quadriceps and hamstrings.</li>
      </ul>
    </div>

    <div class="exercise">
      <h3>🔥 Abs & Core</h3>
      <ul>
        <li>Crunches – Builds the upper abdominal muscles.</li>
        <li>Plank – Increases stability and strengthens the core.</li>
        <li>Leg Raises – Targets lower abs and builds endurance.</li>
      </ul>
    </div>
  </section>

  <section id="nutrition">
    <h2>Diet & Nutrition for Muscle Growth</h2>
    <div class="nutrition">
      <h3>🥩 High Protein Foods</h3>
      <ul>
        <li>Chicken breast, eggs, paneer, fish, and lentils.</li>
        <li>Whey protein shakes for easy protein intake.</li>
      </ul>
      <h3>🍚 Carbohydrates</h3>
      <ul>
        <li>Brown rice, oats, whole wheat bread, and sweet potatoes.</li>
        <li>Fuel your workouts and maintain energy throughout the day.</li>
      </ul>
      <h3>🥑 Healthy Fats</h3>
      <ul>
        <li>Avocados, nuts, olive oil, and seeds for hormone balance.</li>
      </ul>
      <h3>🍎 Vitamins & Minerals</h3>
      <ul>
        <li>Eat fruits like bananas, oranges, and apples daily.</li>
        <li>Include green vegetables for fiber and micronutrients.</li>
      </ul>
    </div>
  </section>

  <section id="contact">
    <h2>Follow Gourav on Instagram</h2>
    <p>Stay updated with daily workouts, tips, and motivation!</p>
    <button onclick="window.open('https://www.instagram.com/gourav_flexjourney','_blank')">Visit Instagram Page</button>
  </section>

  <footer>
    <p>© 2025 Gourav Flex Journey | Built with passion for fitness.</p>
  </footer>

  <audio id="bgMusic" loop src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" preload="auto"></audio>
  <button id="musicControl">Mute</button>

  <script>
    const loader = document.getElementById('loader');
    const music = document.getElementById('bgMusic');
    const musicControl = document.getElementById('musicControl');
    const sections = document.querySelectorAll('section');
    let musicPlaying = true;

    window.addEventListener('load', () => {
      loader.style.opacity = '0';
      setTimeout(() => loader.style.display = 'none', 1000);
      music.volume = 0;
      music.play();
      fadeInAudio(music, 0.3, 3000);
    });

    musicControl.addEventListener('click', () => {
      if(musicPlaying){
        fadeOutAudio(music, 3000);
        musicControl.innerText = 'Unmute';
      } else {
        music.play();
        fadeInAudio(music, 0.3, 3000);
        musicControl.innerText = 'Mute';
      }
      musicPlaying = !musicPlaying;
    });

    function fadeInAudio(audio, targetVolume, duration){
      let step = targetVolume / (duration / 50);
      let vol = 0;
      const fade = setInterval(()=>{
        if(vol < targetVolume){
          vol += step;
          audio.volume = Math.min(vol, targetVolume);
        } else clearInterval(fade);
      }, 50);
    }

    function fadeOutAudio(audio, duration){
      let step = audio.volume / (duration / 50);
      const fade = setInterval(()=>{
        if(audio.volume > 0){
          audio.volume -= step;
        } else { audio.pause(); clearInterval(fade); }
      }, 50);
    }

    // Pulse effect synced with soft beat
    setInterval(()=>{
      sections.forEach(sec => sec.classList.toggle('pulse'));
    }, 2000);
  </script>
</body>
</html>
