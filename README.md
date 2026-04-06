<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Gerador Sensi FF</title>

<style>
body{
background:#0b0b0b;
color:white;
font-family:Arial;
text-align:center;
padding:20px;
}

select,button{
padding:12px;
margin:10px;
border:none;
border-radius:8px;
font-size:16px;
}

button{
background:red;
color:white;
}

#ativar{
display:none;
background:#00ff88;
color:black;
}
</style>

</head>

<body>

<h2>Gerador Sensibilidade Free Fire</h2>

<select id="modelo">
<option>Galaxy A10</option>
<option>Redmi Note 11</option>
<option>Moto G20</option>
</select>

<br>

<button onclick="gerar()">Gerar Sensibilidade</button>

<div id="resultado"></div>

<br>

<button id="ativar" onclick="ativar()">ATIVAR SENSIBILIDADE</button>

<script>

function gerar(){

let modelo = document.getElementById("modelo").value

let sensi = {
"Galaxy A10": {geral:92, red:88, x2:80, x4:72, awm:50, dpi:520},
"Redmi Note 11": {geral:95, red:90, x2:85, x4:75, awm:55, dpi:480},
"Moto G20": {geral:94, red:89, x2:83, x4:74, awm:53, dpi:500}
}

let s = sensi[modelo]

document.getElementById("resultado").innerHTML =
"Geral: "+s.geral+"<br>"+
"Red Dot: "+s.red+"<br>"+
"2x: "+s.x2+"<br>"+
"4x: "+s.x4+"<br>"+
"AWM: "+s.awm+"<br>"+
"DPI: "+s.dpi

document.getElementById("ativar").style.display = "inline-block"

}

function ativar(){
alert("Sensibilidade ativada com sucesso!")
}

</script>

</body>
</html>
