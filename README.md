<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Date misterioso</title>
    <style>

    body{
        background-color: red;
    }
    .painel{
        margin: auto;
        width: 500px;
        height: 500px;
        text-align: center;
        padding-top: 100px;
        font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;

    }

    .painel h1{
        color: white;
    }

    #sim{
        height: 40px;
        width: 60px;
        background-color: white;
        border: none;
        border-radius: 5px;
        margin-left: -80px;
    }

    #nao{
        position: absolute; 
        height: 40px;
        width: 60px;
        background-color: white;
        border: none;
        border-radius: 5px;
        margin-left: 20px;
    }
</style>
</head>

<body>
    
    <div class="painel">
        <h1>Namora comigo?</h1>

        <a href="https://www.youtube.com/watch?v=orWnzqBA63w&ab_channel=YusufScott"><button id="sim"> Sim! </button></a>
        <button onmouseover="fuja()" id="nao"> Não </button>
    </div>

    <script>

        function fuja(){
           var botaoNao = document.getElementById("nao")

           var larguraJanela = window.innerWidth;
           var alturaJanela = window.innerHeight;

           var maxX = larguraJanela - botaoNao.offsetWidth;
           var maxY = alturaJanela - botaoNao.offsetHeight;

           var aleatorioX = Math.floor(Math.random() * maxX);
           var aleatorioY = Math.floor(Math.random() * maxY);

           botaoNao.style.left = aleatorioX + "px";
           botaoNao.style.top = aleatorioY + "px";
        }


        
    </script>
</body>
</html>
