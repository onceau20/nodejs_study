const express = require('express');
const body = require('body-parser');
const { response } = require('express');
const app = express();
const port = 3000;
var db = [];
app.use(express.static('./'));
app.use(express.urlencoded({extended:true}));

app.post('/home', (req, res) => {
    res.redirect(`http://localhost:${port}`);
  });

app.get('/home', (req, res) => {
    const title = req.query.title;
    const description = req.query.description;
    console.log(req.query.title);
    db.push({title,description});
    
    res.redirect(`/`);
});

app.get('/data', (req, res) => {
    const number = req.query.number;
    res.send(db[number]);
});

app.listen(port, () => {
    console.log(`Example app listening at http://localhost:${port}`);
   
});

