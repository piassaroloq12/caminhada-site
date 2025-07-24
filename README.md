<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Caminhada - Área de Lazer Castanheira</title>
  <style>
    body {
      background-color: #ffffff;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      margin: 0;
      padding: 0;
      color: #333;
    }
    header {
      background: linear-gradient(90deg, #27ae60, #2ecc71);
      color: white;
      padding: 30px 20px;
      text-align: center;
      box-shadow: 0 2px 10px rgba(0,0,0,0.1);
    }
    main {
      padding: 20px;
      max-width: 700px;
      margin: auto;
    }
    section {
      margin-bottom: 30px;
      background-color: #f9f9f9;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 1px 5px rgba(0,0,0,0.05);
    }
    h1, h2 {
      margin-bottom: 10px;
    }
    ul {
      padding-left: 20px;
      line-height: 1.6;
    }
    form input, form button {
      display: block;
      width: 100%;
      padding: 12px;
      margin: 10px 0;
      font-size: 1rem;
      border-radius: 6px;
      border: 1px solid #ccc;
    }
    form button {
      background: linear-gradient(90deg, #27ae60, #2ecc71);
      color: white;
      border: none;
      cursor: pointer;
      font-weight: bold;
      transition: background 0.3s ease;
    }
    form button:hover {
      background: linear-gradient(90deg, #219150, #27ae60);
    }
    .pix {
      background-color: #f4f4f4;
      padding: 15px;
      border-radius: 8px;
      text-align: center;
    }
    .pix-code {
      font-weight: bold;
      font-size: 1.1rem;
      color: #000;
    }
  </style>
</head>
<body>
  <header>
    <h1>Caminhada - Área de Lazer Castanheira</h1>
    <p>Participe de um dia de bem-estar, natureza e diversão!</p>
  </header>

  <main>
    <section>
      <h2>Informações do Evento</h2>
      <p><strong>📅 Data:</strong> 07 de setembro</p>
      <p><strong>💰 Valor:</strong> R$ 100,00 por pessoa</p>
      <p><strong>📝 Inscrições até:</strong> 10 de setembro</p>
    </section>

    <section>
      <h2>📌 Programação</h2>
      <ul>
        <li>☕ 7h - Café da manhã</li>
        <li>🚶 8h - Caminhada</li>
        <li>🍽️ 11h - Almoço</li>
        <li>🎵 12h - Música ao vivo</li>
        <li>🧘 15h - Yoga</li>
      </ul>
    </section>

    <section>
      <h2>✅ Inscrição ate o dia 01</h2>
      <form id="form-inscricao" onsubmit="enviarWhatsApp(); return false;">
        <input type="text" id="nome" placeholder="Nome completo" required>
        <input type="tel" id="telefone" placeholder="Telefone" required>
        <input type="email" id="email" placeholder="E-mail" required>
        <button type="submit">Desejo mais informações</button>
      </form>
    </section>
  </main>

  <script>
    function enviarWhatsApp() {
      const nome = document.getElementById('nome').value;
      const telefone = document.getElementById('telefone').value;
      const email = document.getElementById('email').value;

      const mensagem = `Olá! Desejo mais informações e o Pix para pagar a inscrição na caminhada.%0A%0ANome: ${nome}%0ATelefone: ${telefone}%0AEmail: ${email}`;
      const numero = "5528999402578";
      const url = `https://wa.me/${numero}?text=${mensagem}`;
      window.open(url, '_blank');
    }
  </script>
</body>
</html>
