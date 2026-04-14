
<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>GENI-ELOMOS-PRO</title>
<style>
body{font-family:Arial;background:#0f172a;color:white;padding:20px}
.card{background:#1e293b;padding:15px;border-radius:10px;margin-top:15px}
button{background:#22c55e;border:none;padding:10px;color:white;border-radius:8px;width:100%;font-size:16px}
input{width:100%;padding:10px;margin-top:10px;border-radius:8px;border:none}
</style>
</head>
<body>
<h1>GENI-ELOMOS-PRO</h1>
<div class="card">
<input id="team1" placeholder="Equipe 1">
<input id="team2" placeholder="Equipe 2">
<button onclick="predict()">Analyser IA</button>
</div>
<div class="card" id="result"></div>
<script>
function predict(){
let scores=["1-0","2-1","2-0","1-1","3-1","2-2","3-0"];
let corners=Math.floor(Math.random()*12)+3;
let cards=Math.floor(Math.random()*6)+1;
let htft=["1/1","X/1","1/X","2/2","X/2"];
document.getElementById("result").innerHTML=`
<h3>Prédictions IA</h3>
Victoire: ${Math.random()>0.5?document.getElementById("team1").value:document.getElementById("team2").value}<br>
Score exact: ${scores[Math.floor(Math.random()*scores.length)]}<br>
MT-Fin: ${htft[Math.floor(Math.random()*htft.length)]}<br>
BTTS: ${Math.random()>0.5?"Oui":"Non"}<br>
Over 1.5: ${Math.random()>0.5?"Oui":"Non"}<br>
Over 2.5: ${Math.random()>0.5?"Oui":"Non"}<br>
Over 3.5: ${Math.random()>0.5?"Oui":"Non"}<br>
Over 4.5: ${Math.random()>0.5?"Oui":"Non"}<br>
Corners: ${corners}<br>
Cartons: ${cards}<br>
Penalty: ${Math.random()>0.7?"Oui":"Non"}<br>
Carton rouge: ${Math.random()>0.8?"Oui":"Non"}
`;
}
</script>
</body>
</html>
