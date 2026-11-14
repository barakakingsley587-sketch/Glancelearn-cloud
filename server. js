const express = require('express');
const cors = require('cors');
const app = express();
app.use(cors());
app.use(express.json({limit:'50mb'}));

let savedDb = null;

app.get('/', (req,res)=>res.send('GlanceLearn Cloud OK'));
app.post('/save', (req,res)=>{
  savedDb = req.body.db;
  res.json({success:true});
});
app.get('/load', (req,res)=>{
  res.json({db: savedDb});
});
app.get('/db', (req,res)=>{
  res.json({db: savedDb});
});

const PORT = process.env.PORT || 10000;
app.listen(PORT, ()=>console.log('Running on '+PORT));