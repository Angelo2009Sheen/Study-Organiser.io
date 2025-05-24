
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Student Dashboard</title>
  <style>
    :root {
      --bg-light: #fef6f3;
      --text-light: #333;
      --bg-dark: #121212;
      --text-dark: #f5f5f5;
      --accent: #94bbe9;
    }

    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background-color: var(--bg-light);
      color: var(--text-light);
      transition: background-color 0.3s, color 0.3s;
    }

    .dark-mode {
      background-color: var(--bg-dark);
      color: var(--text-dark);
    }

    header {
      padding: 1rem;
      background-color: var(--accent);
      color: white;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .verse {
      font-style: italic;
      font-size: 0.95rem;
    }

    nav {
      display: flex;
      flex-wrap: wrap;
      gap: 1rem;
      padding: 1rem;
    }

    nav a {
      text-decoration: none;
      background: var(--accent);
      padding: 0.8rem 1.2rem;
      border-radius: 8px;
      color: white;
      transition: background 0.3s;
    }

    nav a:hover {
      background: #7da9dc;
    }

    .toggle-btn {
      padding: 0.5rem 1rem;
      background: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      color: var(--accent);
      font-weight: bold;
    }

    .container {
      padding: 2rem;
      max-width: 800px;
      margin: auto;
      text-align: center;
    }
  </style>
</head>
<body>

<header>
  <div class="verse" id="bible-verse"></div>
  <button class="toggle-btn" onclick="toggleMode()">Toggle Dark/Light</button>
</header>

<main class="container">
  <h1>Welcome to Your Student Dashboard</h1>
  <p>Navigate through your academic tools:</p>
  <nav>
    <a href="https://angelo2009sheen.github.io/Subjects/">Subjects & Progress</a>
    <a href="calender.html">Calendar</a>
    <a href="textbooks.html">PDFs & Textbooks</a>
    <a href="To-do-list.html">To-Do / Assignments</a>
    <a href="Pomodoro.html">Pomodoro Timer</a>
    <a href="Exams.html">Exam Tracker</a>
    <a href="exercises.html">Exercise Uploads</a>
  </nav>
</main>

<script>
  const verses = [
    "I can do all things through Christ who strengthens me. — Philippians 4:13",
    "Trust in the Lord with all your heart and lean not on your own understanding. — Proverbs 3:5",
    "For I know the plans I have for you, declares the Lord. — Jeremiah 29:11",
    "The Lord is my shepherd; I shall not want. — Psalm 23:1",
    "Be strong and courageous. Do not be afraid. — Joshua 1:9"
  ];

  function getRandomVerse() {
    const index = Math.floor(Math.random() * verses.length);
    return verses[index];
  }

  document.getElementById("bible-verse").textContent = getRandomVerse();

  function toggleMode() {
    document.body.classList.toggle('dark-mode');
  }
</script>

</body>
</html>
