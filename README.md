<!-- GitHub绿墙比例Banner (宽度自适应) -->
<div align="center">
  <img src="https://github.com/Geekstrange/Geekstrange/blob/main/img/wow.jpg?raw=true" alt="Banner" width="100%" height="100%" style="object-fit: cover;">
</div>

<!-- 今日诗词标题区域 -->
<div align="center" style="margin: 2rem 0;">
  <div id="poem-container" style="font-size: 1.8rem; font-weight: 600; color: #333; line-height: 1.8; min-height: 60px;">
    加载中...
  </div>
  <div id="poem-author" style="margin-top: 0.8rem; font-size: 1.2rem; color: #666; font-style: italic;"></div>
</div>

<!-- GitHub统计卡片 -->
<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Geekstrange&show_icons=true&theme=github_dark" height="160">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Geekstrange&layout=compact&theme=github_dark" height="160">
</div>

<!-- 技术栈 -->
<h3>🛠️ Tech Stack</h3>
<p>
  <img src="https://img.shields.io/badge/Go-00ADD8?logo=go&logoColor=white" alt="Go">
  <img src="https://img.shields.io/badge/Rust-CC4729?logo=rust&logoColor=white" alt="Rust">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black">
  <img src="https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white">
  <img src="https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white">
</p>

<!-- 社交链接 -->
<h3>🌐 Connect with Me</h3>
<p>
  <a href="https://codepen.io/Geekstrange">
    <img src="https://img.shields.io/badge/CodePen-5E616D?logo=codepen" alt="CodePen">
  </a>
  <a href="https://www.linkedin.com/in/eric-zhang-b1682920b/">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?logo=linkedin" alt="LinkedIn">
  </a>
  <a href="https://www.instagram.com/be.wind/">
    <img src="https://img.shields.io/badge/Instagram-E4405F?logo=instagram" alt="Instagram">
  </a>
  <a href="https://space.bilibili.com/100030354">
    <img src="https://img.shields.io/badge/Bilibili-FF69B4?logo=bilibili" alt="Bilibili">
  </a>
  <a href="https://www.coolapk.com/u/3791216">
    <img src="https://img.shields.io/badge/Coolapk-11B5F6?logo=android&logoColor=white&color=32CD32" alt="Coolapk">
  </a>
</p>

<script>
// 调用今日诗词API获取随机诗句
fetch('https://v1.jinrishici.com/all.json')
  .then(response => response.json())
  .then(data => {
    const poemContainer = document.getElementById('poem-container');
    const authorContainer = document.getElementById('poem-author');

    // 显示诗句和作者
    poemContainer.textContent = data.content;
    authorContainer.textContent = `—— ${data.author}《${data.origin}》`;
  })
  .catch(error => {
    document.getElementById('poem-container').textContent = "海内存知己，天涯若比邻";
    document.getElementById('poem-author').textContent = "—— 王勃《送杜少府之任蜀州》";
  });
</script>
