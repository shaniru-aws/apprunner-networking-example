const express = require('express');
const app = express();
const port = 3000;
const axios = require('axios');

app.get('/', (req, res) => {
  res.send('Hello World!');
});

app.get('/ip/:ipAddress', async (req, res) => {
  const ipAddress = req.params.ipAddress;

  try {
    const response = await axios.get(`http://ipinfo.io/${ipAddress}`);
    res.json(response.data);
  } catch (error) {
    console.error(error);
    res.status(500).send('Error fetching IP information');
  }
});

app.listen(port, () => {
  console.log(`Example app listening at http://localhost:${port}`);
});
