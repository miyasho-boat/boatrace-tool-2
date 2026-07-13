<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>厳選ボートレースツール Ver.2</title>

<style>
body{
    margin:0;
    background:#f5f5f5;
    font-family:sans-serif;
}

header{
    background:#0077cc;
    color:white;
    text-align:center;
    padding:15px;
    font-size:24px;
    font-weight:bold;
}

main{
    max-width:900px;
    margin:auto;
    padding:20px;
}

.box{
    background:white;
    border-radius:10px;
    padding:20px;
    box-shadow:0 0 10px rgba(0,0,0,.15);
}

input[type=file]{
    width:100%;
    font-size:18px;
    margin-bottom:15px;
}

button{
    padding:12px 20px;
    font-size:18px;
    cursor:pointer;
}

#preview{
    margin-top:20px;
    text-align:center;
}

#preview img{
    max-width:100%;
    border:1px solid #ccc;
}

#result{
    margin-top:20px;
    background:#eee;
    padding:15px;
    min-height:120px;
    white-space:pre-line;
    font-size:20px;
}
</style>

</head>
<body>

<header>
厳選ボートレースツール Ver.2
</header>

<main>

<div class="box">

<input type="file" id="imageFile" accept="image/*">

<button disabled id="ocrButton">
OCRは次回実装
</button>

<div id="preview"></div>

<div id="result">
ここにOCR結果が表示されます。
</div>

</div>

</main>

<script>

const file=document.getElementById("imageFile");
const preview=document.getElementById("preview");
const button=document.getElementById("ocrButton");

file.addEventListener("change",function(){

const img=new Image();

img.src=URL.createObjectURL(file.files[0]);

preview.innerHTML="";
preview.appendChild(img);

button.disabled=false;

});

</script>

</body>
</html># boatrace-tool-2
