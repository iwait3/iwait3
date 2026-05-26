<!doctype html>
<html lang="zh-CN">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>个人介绍 - 软件工程专业</title>
    <style>
      * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
      }

      body {
        font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
        line-height: 1.6;
        color: #333;
        background: #ffffff;
        min-height: 100vh;
      }

      .container {
        max-width: 700px;
        margin: 0 auto;
        padding: 40px 20px;
      }

      /* 头部区域 */
      header {
        text-align: center;
        padding: 40px 0;
        animation: fadeInDown 1s ease-out;
      }

      .avatar {
        width: 160px;
        height: 160px;
        border-radius: 50%;
        margin: 0 auto 20px;
        background: linear-gradient(135deg, #ffcdd2 0%, #f8bbd9 100%);
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 50px;
        box-shadow: 0 8px 30px rgba(255, 182, 193, 0.4);
        transition:
          transform 0.3s ease,
          box-shadow 0.3s ease;
      }

      .avatar:hover {
        transform: scale(1.05);
        box-shadow: 0 12px 40px rgba(255, 182, 193, 0.6);
      }

      h1 {
        font-size: 28px;
        color: #2d3436;
        margin-bottom: 8px;
        font-weight: 600;
      }

      .title {
        font-size: 16px;
        color: #636e72;
        letter-spacing: 2px;
      }

      .divider {
        width: 60px;
        height: 2px;
        background: linear-gradient(90deg, #ffcdd2, #f8bbd9);
        margin: 20px auto;
        border-radius: 1px;
      }

      /* 内容卡片 */
      .card {
        background: white;
        border-radius: 16px;
        padding: 30px;
        margin-bottom: 20px;
        box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
        animation: fadeInUp 0.8s ease-out backwards;
        transition:
          transform 0.3s ease,
          box-shadow 0.3s ease;
      }

      .card:nth-child(2) {
        animation-delay: 0.1s;
      }
      .card:nth-child(3) {
        animation-delay: 0.2s;
      }
      .card:nth-child(4) {
        animation-delay: 0.3s;
      }
      .card:nth-child(5) {
        animation-delay: 0.4s;
      }

      .card:hover {
        transform: translateY(-5px);
        box-shadow: 0 8px 30px rgba(0, 0, 0, 0.08);
      }

      .section-title {
        font-size: 18px;
        font-weight: 600;
        color: #2d3436;
        margin-bottom: 18px;
        display: flex;
        align-items: center;
        gap: 12px;
      }

      .section-title::before {
        content: "";
        width: 10px;
        height: 24px;
        background: linear-gradient(180deg, #667eea 0%, #764ba2 100%);
        border-radius: 4px;
      }

      /* 关于我 */
      .about-text {
        font-size: 15px;
        color: #636e72;
        line-height: 1.8;
        text-align: justify;
      }

      /* 教育背景 */
      .education {
        background: #fff5f8;
        padding: 20px;
        border-radius: 12px;
      }

      .education-title {
        font-weight: 600;
        color: #2d3436;
        font-size: 16px;
      }

      .education-detail {
        color: #636e72;
        font-size: 14px;
        margin-top: 6px;
      }

      /* 技能网格 */
      .skills-grid {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        gap: 15px;
      }

      .skill-card {
        background: #fff5f8;
        padding: 20px;
        border-radius: 12px;
        text-align: center;
        transition: all 0.3s ease;
        border: 1px solid transparent;
      }

      .skill-card:hover {
        background: #ffebee;
        border-color: #ffcdd2;
        transform: scale(1.02);
      }

      .skill-icon {
        font-size: 28px;
        margin-bottom: 10px;
      }

      .skill-name {
        font-weight: 600;
        color: #2d3436;
        font-size: 14px;
      }

      .skill-level {
        font-size: 12px;
        color: #95a5a6;
        margin-top: 4px;
      }

      /* 联系方式 */
      .contact-info {
        display: flex;
        flex-wrap: wrap;
        gap: 15px;
      }

      .contact-item {
        flex: 1;
        min-width: 200px;
        display: flex;
        align-items: center;
        gap: 12px;
        background: #fff5f8;
        padding: 15px 20px;
        border-radius: 12px;
        transition: all 0.3s ease;
      }

      .contact-item:hover {
        background: #ffebee;
        transform: translateY(-3px);
      }

      .contact-icon {
        font-size: 22px;
        color: #e91e63;
      }

      .contact-link {
        text-decoration: none;
        color: #2d3436;
        font-weight: 500;
        font-size: 14px;
      }

      .contact-link:hover {
        color: #e91e63;
      }

      /* 页脚 */
      footer {
        text-align: center;
        padding: 30px 0;
        color: #95a5a6;
        font-size: 13px;
        animation: fadeIn 1s ease-out 0.5s backwards;
      }

      /* 动画 */
      @keyframes fadeInDown {
        from {
          opacity: 0;
          transform: translateY(-20px);
        }
        to {
          opacity: 1;
          transform: translateY(0);
        }
      }

      @keyframes fadeInUp {
        from {
          opacity: 0;
          transform: translateY(20px);
        }
        to {
          opacity: 1;
          transform: translateY(0);
        }
      }

      @keyframes fadeIn {
        from {
          opacity: 0;
        }
        to {
          opacity: 1;
        }
      }

      /* 响应式 */
      @media (max-width: 500px) {
        .container {
          padding: 25px 15px;
        }

        .avatar {
          width: 130px;
          height: 130px;
          font-size: 40px;
        }

        h1 {
          font-size: 24px;
        }

        .card {
          padding: 22px;
        }

        .skills-grid {
          grid-template-columns: 1fr;
        }

        .contact-info {
          flex-direction: column;
        }
      }
    </style>
  </head>
  <body>
    <div class="container">
      <!-- 头部 -->
      <header>
        <div class="avatar">👩‍</div>
        <h1>黄工</h1>
        <p class="title">软件工程专业 · 本科在读 · 重庆</p>
        <div class="divider"></div>
      </header>

      <!-- 关于我 -->
      <div class="card">
        <h2 class="section-title">关于我</h2>
        <p class="about-text">
          我是一名热爱技术的软件工程专业学生，目前就读于重庆某高校。我对软件开发充满热情，擅长将复杂的技术问题转化为优雅的解决方案。在学习过程中，我不仅掌握了扎实的理论基础，更注重实践能力的培养。我相信技术的力量可以改变世界，致力于通过代码创造有价值的产品。
        </p>
      </div>

      <!-- 教育背景 -->
      <div class="card">
        <h2 class="section-title">教育背景</h2>
        <div class="education">
          <div class="education-title">重庆某高校 - 软件工程专业</div>
          <div class="education-detail">本科 · 2023年9月 - 至今</div>
        </div>
      </div>

      <!-- 专业技能 -->
      <div class="card">
        <h2 class="section-title">专业技能</h2>
        <div class="skills-grid">
          <div class="skill-card">
            <div class="skill-icon">🌐</div>
            <div class="skill-name">前端开发</div>
            <div class="skill-level">HTML/CSS/JS/Vue/React</div>
          </div>
          <div class="skill-card">
            <div class="skill-icon">⚙️</div>
            <div class="skill-name">后端开发</div>
            <div class="skill-level">Node.js/Python/Java</div>
          </div>
          <div class="skill-card">
            <div class="skill-icon">🗄️</div>
            <div class="skill-name">数据库</div>
            <div class="skill-level">MySQL/PostgreSQL/MongoDB</div>
          </div>
          <div class="skill-card">
            <div class="skill-icon">📱</div>
            <div class="skill-name">鸿蒙开发</div>
            <div class="skill-level">HarmonyOS应用开发</div>
          </div>
        </div>
      </div>

      <!-- 联系方式 -->
      <div class="card">
        <h2 class="section-title">联系方式</h2>
        <div class="contact-info">
          <a
            href="https://github.com/yourusername"
            class="contact-item"
            target="_blank"
          >
            <span class="contact-icon">🐙</span>
            <span class="contact-link">GitHub</span>
          </a>
          <a href="mailto:3577723170@qq.com" class="contact-item">
            <span class="contact-icon">📧</span>
            <span class="contact-link">3577723170@qq.com</span>
          </a>
        </div>
      </div>

      <!-- 页脚 -->
      <footer>
        <p>© 2026 黄工 | 热爱技术，追求卓越</p>
      </footer>
    </div>
  </body>
</html>
