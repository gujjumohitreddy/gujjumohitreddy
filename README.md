<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Gujju Mohit | Developer Portfolio</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: #0d1117;
      color: #c9d1d9;
      text-align: center;
      padding: 2rem;
    }
    a {
      color: #58a6ff;
      text-decoration: none;
    }
    h1 {
      color: #58a6ff;
    }
    .socials img {
      width: 32px;
      margin: 0.5rem;
    }
    .badges img {
      margin: 0.5rem;
    }
    button.resume {
      padding: 0.7rem 1.5rem;
      background-color: #238636;
      color: white;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      font-size: 1rem;
      margin-top: 1rem;
    }
    #repos {
      margin-top: 2rem;
    }
    .repo {
      margin: 0.5rem 0;
      background-color: #161b22;
      padding: 1rem;
      border-radius: 8px;
      width: 80%;
      max-width: 600px;
      margin-left: auto;
      margin-right: auto;
    }
  </style>
</head>

<body>
  <h1>👋 Hello, I'm Gujju Mohit</h1>
  <p>Python Developer | Web Enthusiast | Tech Explorer</p>

  <p>
    💻 I love creating clean, simple, and useful tools with Python & web technologies.<br />
    🤝 Let's collaborate on open-source projects!
  </p>

  <!-- ✅ Resume Button -->
  <a href="assets/gujju_mohit_resume.pdf" download>
    <button class="resume">📄 Download My Resume</button>
  </a>

  <!-- ✅ Social Links -->
  <div class="socials">
    <a href="https://linkedin.com/in/gmohitreddy"><img src="https://skillicons.dev/icons?i=linkedin" /></a>
    <a href="https://x.com/gmohitreddy"><img src="https://skillicons.dev/icons?i=twitter" /></a>
    <a href="https://instagram.com/gmohitreddy"><img src="https://skillicons.dev/icons?i=instagram" /></a>
    <a href="https://github.com/gujjumohitreddy"><img src="https://skillicons.dev/icons?i=github" /></a>
  </div>

  <!-- ✅ Tech News Section -->
  <h2>📰 Live Tech Updates</h2>
  <p>
    🚀 <a href="https://techcrunch.com/">TechCrunch</a> &nbsp;|&nbsp;
    🧠 <a href="https://openai.com/blog/">OpenAI Blog</a> &nbsp;|&nbsp;
    🌐 <a href="https://github.blog/">GitHub Blog</a> &nbsp;|&nbsp;
    📈 <a href="https://ai.googleblog.com/">Google AI Blog</a>
  </p>

  <div class="badges">
    <a href="https://techcrunch.com/"><img src="https://img.shields.io/badge/TechCrunch-News-green?style=for-the-badge&logo=techcrunch&logoColor=white" /></a>
    <a href="https://openai.com/blog/"><img src="https://img.shields.io/badge/OpenAI-Blog-8a2be2?style=for-the-badge&logo=openai&logoColor=white" /></a>
    <a href="https://github.blog/"><img src="https://img.shields.io/badge/GitHub-Blog-black?style=for-the-badge&logo=github&logoColor=white" /></a>
    <a href="https://ai.googleblog.com/"><img src="https://img.shields.io/badge/Google%20AI-Blog-blue?style=for-the-badge&logo=google&logoColor=white" /></a>
  </div>

  <!-- ✅ Auto GitHub Repos -->
  <h2>📦 Latest Projects</h2>
  <div id="repos">Loading projects...</div>

  <script>
    fetch("https://api.github.com/users/gujjumohitreddy/repos?sort=updated")
      .then(res => res.json())
      .then(data => {
        const container = document.getElementById("repos");
        container.innerHTML = "";
        data.slice(0, 5).forEach(repo => {
          const div = document.createElement("div");
          div.className = "repo";
          div.innerHTML = `<strong><a href="${repo.html_url}" target="_blank">${repo.name}</a></strong><br/>${repo.description || 'No description'}<br/>⭐ ${repo.stargazers_count} | 🔄 ${repo.forks_count}`;
          container.appendChild(div);
        });
      });
  </script>

  <!-- ✅ Visitor Counter (No setup needed) -->
  <h2 style="margin-top: 3rem;">👀 Visitors</h2>
  <img src="https://hits.sh/gujjumohitreddy.github.io.svg?style=for-the-badge&label=Profile+Views&color=purple" alt="hit counter" />

  <!-- Footer -->
  <footer style="margin-top: 3rem;">
    <p>Made with ❤️ by Gujju Mohit | Powered by GitHub Pages</p>
  </footer>
</body>
</html>