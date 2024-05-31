# 4-ExplicarCodigo

Considere o trecho abaixo, e responda:

<html><head><script src="jquery.min.js"></script>
<script>
$(main);
function main(){
    $('button').click(foo);
}
function foo(){
    bar([10,20,30,40,50,60,70,80,90,100]);
}

function bar(v){
    var arrf = [];
    arrf[0] = function (x) { return 2*x; };
    arrf[1] = function (x) { return x-20; };
    arrf[2] = function (x) { if (x%3==0) return true; else return false; };
    arrf[3] = function (x,y) { return x+y+1; };
    arrf[4] = function (x) { return x+10; };
    
    alert(v.map(arrf[0]).map(arrf[1]). filter(arrf[2]).map(arrf[4]).reduce(arrf[3],0));
}
</script></head>
<body>
<button>OK</button>
</body>
</html>

a) Explique com detalhes o que faz a linha 20 (do alert)
b) Qual o valor mostrado pelo alert? qual o seu tipo?
