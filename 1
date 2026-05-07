const express = require('express');
const cors = require('cors');

const app = express();
app.use(cors());
app.use(express.json());

const keys = new Map();

app.get('/generate', (req, res) => {
  const code = 'MT-' + Math.random().toString(36).substring(2, 10).toUpperCase();
  keys.set(code, { used: false });
  res.send(`<h2>✅ Nuovo codice generato:</h2><h1 style="color:green">${code}</h1>`);
});

app.post('/api/verify', (req, res) => {
  const { code } = req.body;
  if (!code) return res.json({ status: "error", message: "Codice mancante" });

  const clean = code.toUpperCase().trim();
  const record = keys.get(clean);

  if (!record) return res.json({ status: "error", message: "Codice non valido" });
  if (record.used) return res.json({ status: "error", message: "Codice già utilizzato" });

  record.used = true;
  record.usedAt = new Date();

  res.json({ status: "success", message: "✅ Attivazione completata!" });
});

const PORT = process.env.PORT || 3000;
app.listen(PORT, () => console.log(`Server attivo su ${PORT}`));
