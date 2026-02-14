<!DOCTYPE html>
<html lang="az">
<head>
<meta charset="UTF-8">
<title>Nəşriyyatı</title>
<style>
body { font-family: Arial, sans-serif; background:#f4f4f4; text-align:center; }
.container { background:#fff; padding:25px; margin:50px auto; width:350px; border-radius:10px; box-shadow:0 0 10px rgba(0,0,0,0.1);}
h1 { color:#333; }
input, button { padding:10px; width:100%; margin-top:10px; border-radius:5px; border:1px solid #ccc; }
button { background:#4CAF50; color:white; border:none; cursor:pointer; }
button:hover { background:#45a049; }
#netice { margin-top:15px; font-weight:bold; }
</style>
</head>
<body>

<div class="container">
  <h1>Nəşriyyatı</h1>
  <p>İmtahan kodunu daxil edin və nəticənizə baxın:</p>
  <input id="kod" placeholder="İmtahan kodunu daxil edin">
  <button onclick="yoxla()">Nəticəyə bax</button>
  <div id="netice"></div>
</div>

<script>
const melumatlar = {
  "AZ01": {ad:"Ali Əliyev", bal:78, duzgun:39, sehv:11},
  "AZ02": {ad:"Aysel Məmmədova", bal:62, duzgun:31, sehv:19},
  "AZ03": {ad:"Elvin Həsənov", bal:85, duzgun:42, sehv:8},
  "AZ04": {ad:"Leyla Quliyeva", bal:70, duzgun:35, sehv:15},
  "AZ05": {ad:"Orxan Məmmədov", bal:90, duzgun:45, sehv:5},
  "AZ06": {ad:"Nərmin Əliyeva", bal:65, duzgun:33, sehv:17},
  "AZ07": {ad:"Rəşad İsmayılov", bal:80, duzgun:40, sehv:10},
  "AZ08": {ad:"Səbinə Hüseynova", bal:55, duzgun:27, sehv:23},
  "AZ09": {ad:"Tural Əliyev", bal:73, duzgun:37, sehv:13},
  "AZ10": {ad:"Zeynəb Məmmədova", bal:88, duzgun:44, sehv:6}
};

function yoxla() {
  const kod = document.getElementById("kod").value.toUpperCase();
  const n = melumatlar[kod];
  if(n){
    document.getElementById("netice").innerHTML =
      `Ad Soyad: ${n.ad}<br>Bal: ${n.bal}<br>Düzgün: ${n.duzgun}<br>Səhv: ${n.sehv}`;
  } else {
    document.getElementById("netice").innerHTML = "Bu koda uyğun nəticə tapılmadı";
  }
}
</script>

</body>
</html># Ne-riyyat-
