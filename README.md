<!DOCTYPE html>
<html>
<head>
<title>Gold AI Dashboard</title>
<meta name="viewport" content="width=device-width, initial-scale=1">

<style>
body{
font-family:Arial;
background:#111;
color:white;
padding:20px;
}

.box{
background:#1f1f1f;
padding:15px;
border-radius:10px;
margin-top:10px;
}
</style>
</head>

<body>

<h2>Gold AI Trading Dashboard</h2>

<div class="box" id="gold">
Loading Gold Data...
</div>

<script>

async function updateData(){

let goldPrice = Math.floor(Math.random()*200)+72000;

let result = `
MARKET BIAS : BUY

ENTRY : ${goldPrice}

STOP LOSS : ${goldPrice-200}

TARGET 1 : ${goldPrice+300}

TARGET 2 : ${goldPrice+500}

Updated : ${new Date().toLocaleTimeString()}
`;

document.getElementById("gold").innerHTML = result;

}

updateData();

setInterval(updateData,900000);

</script>

</body>
</html>
