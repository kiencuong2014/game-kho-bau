<!DOCTYPE html>

<html lang="vi">
<head>
<meta charset="UTF-8">
<title>Game Kho Báu</title>
<style>
body { margin:0; overflow:hidden; background:#0f172a; }
#game {
    width:100vw; height:100vh;
    background:url('https://picsum.photos/800/600?jungle') center/cover;
    position:relative;
}
#player {
    width:60px; height:60px;
    position:absolute;
    background:url('https://cdn-icons-png.flaticon.com/512/194/194938.png') center/cover;
    left:50px; top:50px;
}
#treasure {
    width:60px; height:60px;
    position:absolute;
    background:url('https://cdn-icons-png.flaticon.com/512/2331/2331943.png') center/cover;
    right:80px; bottom:80px;
}
#text {
    position:absolute;
    top:20px; left:50%;
    transform:translateX(-50%);
    color:white; font-size:24px;
}
</style>
</head>
<body>

<div id="game">
<div id="text">Di chuyển bằng WASD hoặc phím mũi tên 🎮</div>
<div id="player"></div>
<div id="treasure"></div>
</div>

<script>
let p=document.getElementById("player");
let t=document.getElementById("treasure");
let txt=document.getElementById("text");

let x=50,y=50,s=10;

document.addEventListener("keydown",e=>{
if(e.key=="d"||e.key=="ArrowRight")x+=s;
if(e.key=="a"||e.key=="ArrowLeft")x-=s;
if(e.key=="w"||e.key=="ArrowUp")y-=s;
if(e.key=="s"||e.key=="ArrowDown")y+=s;

x=Math.max(0,Math.min(window.innerWidth-60,x));
y=Math.max(0,Math.min(window.innerHeight-60,y));

p.style.left=x+"px";
p.style.top=y+"px";

let pr=p.getBoundingClientRect();
let tr=t.getBoundingClientRect();

if(pr.left<tr.right&&pr.right>tr.left&&pr.top<tr.bottom&&pr.bottom>tr.top){
txt.innerText="🎉 Bạn thắng!";
t.style.display="none";
}
});
</script>

</body>
</html>
