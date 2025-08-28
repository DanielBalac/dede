<!doctype html>
<html lang="pt-BR">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width,initial-scale=1" />
    <title>rafael hechtman</title>
    <meta name="description" content="Site pessoal de Rafael Hechtman — portfólio, contato e sobre." />
    <style>
      :root{
        --bg:#0f1724;
        --card:#0b1220;
        --accent1:#7c3aed;
        --accent2:#06b6d4;
        --muted:#9aa4b2;
      }
      *{box-sizing:border-box}
      html,body{height:100%}
      body{
        margin:0;
        font-family:Inter, system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;
        background:linear-gradient(180deg,var(--bg),#071021 120%);
        color:#e6eef6;
        -webkit-font-smoothing:antialiased;
        -moz-osx-font-smoothing:grayscale;
        line-height:1.4;
      }
      .container{max-width:980px;margin:48px auto;padding:24px}
      header{display:flex;align-items:center;gap:18px}
      .avatar{
        width:110px;height:110px;border-radius:18px;flex:0 0 110px;
        background:linear-gradient(135deg,var(--accent1),var(--accent2));
        display:flex;align-items:center;justify-content:center;font-weight:700;font-size:28px;color:rgba(255,255,255,0.95);
        box-shadow:0 8px 30px rgba(2,6,23,0.6);
      }
      h1{margin:0;font-size:32px;letter-spacing:0.2px}
      p.lead{margin:6px 0 0;color:var(--muted)}
      nav{margin-top:18px;display:flex;gap:10px}
      a.btn{padding:10px 14px;border-radius:12px;background:rgba(255,255,255,0.03);text-decoration:none;color:inherit;font-weight:600;border:1px solid rgba(255,255,255,0.03)}
      main{margin-top:28px;display:grid;grid-template-columns:1fr 320px;gap:22px}
      .card{background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));padding:18px;border-radius:14px;border:1px solid rgba(255,255,255,0.03);box-shadow:0 6px 24px rgba(2,6,23,0.5)}
      .about h2{margin-top:0}
      .skills{display:flex;flex-wrap:wrap;gap:8px;margin-top:8px}
      .tag{background:rgba(255,255,255,0.03);padding:8px 10px;border-radius:999px;font-size:13px}
      .contact-list{display:flex;flex-direction:column;gap:10px}
      footer{margin-top:28px;text-align:center;color:var(--muted);font-size:14px}
      @media(max-width:880px){main{grid-template-columns:1fr} .avatar{width:86px;height:86px;border-radius:12px}}
    </style>
  </head>
  <body>
    <div class="container">
      <header>
        <div class="avatar">RH</div>
        <div>
          <h1>rafael hechtman</h1>
          <p class="lead">Portfólio pessoal • Desenvolvedor &amp; Criador</p>
          <nav>
            <a class="btn" href="#sobre">Sobre</a>
            <a class="btn" href="#trabalhos">Trabalhos</a>
            <a class="btn" href="#contato">Contato</a>
          </nav>
        </div>
      </header>

      <main>
        <section class="card about" id="sobre">
          <h2>Sobre mim</h2>
          <p>Olá — eu sou Rafael Hechtman. Aqui está um resumo rápido: gosto de construir produtos digitais com atenção ao detalhe, experiência do usuário e bom design. Trabalho com desenvolvimento web, automações e projetos criativos.</p>

          <h3 style="margin-top:16px">Habilidades</h3>
          <div class="skills">
            <span class="tag">HTML &amp; CSS</span>
            <span class="tag">JavaScript</span>
            <span class="tag">React</span>
            <span class="tag">Node.js</span>
            <span class="tag">UX/UI</span>
            <span class="tag">Design System</span>
          </div>

          <h3 style="margin-top:16px">Resumo</h3>
          <p class="lead">Tenho experiência em projetos front-end e back-end, gosto de trabalhar em times pequenos e iterar rápido. Tento sempre equilibrar código limpo com interfaces agradáveis.</p>
        </section>

        <aside class="card" id="trabalhos">
          <h3>Projetos</h3>
          <ul style="padding-left:18px;margin-top:6px">
            <li><strong>Projeto A</strong> — landing interativa e SPA.</li>
            <li><strong>Projeto B</strong> — automação de processos e dashboard.</li>
            <li><strong>Projeto C</strong> — pequena biblioteca de componentes.</li>
          </ul>

          <h3 style="margin-top:14px">Contato</h3>
          <div class="contact-list" id="contato">
            <div>Email: <a href="mailto:rafael@example.com">rafael@example.com</a></div>
            <div>LinkedIn: <a href="#">linkedin.com/in/rafael-hechtman</a></div>
            <div>GitHub: <a href="#">github.com/rafaelhechtman</a></div>
          </div>

          <div style="margin-top:16px;text-align:center">
            <a class="btn" href="#contato">Entrar em contato</a>
          </div>
        </aside>
      </main>

      <footer>
        © <span id="year"></span> rafael hechtman — feito com ❤️
      </footer>
    </div>

    <script>
      // seta o ano automaticamente
      document.getElementById('year').textContent = new Date().getFullYear();

      // Simples melhoria: scroll suave para links
      document.querySelectorAll('a[href^="#"]').forEach(a=>{
        a.addEventListener('click',e=>{
          e.preventDefault();
          const t=document.querySelector(a.getAttribute('href'));
          if(t) t.scrollIntoView({behavior:'smooth',block:'start'});
        });
      });
    </script>
  </body>
</html>
