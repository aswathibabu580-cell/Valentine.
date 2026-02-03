<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Will you be my Valentine?</title>

<style>
body{
    margin:0;
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    background:#ffeef2;
    font-family:'Comic Sans MS', cursive;
    overflow:hidden;
}

.container{
    text-align:center;
}

img{
    width:180px;
    transition:transform 0.5s;
}

h1{
    margin:20px 0;
}

.buttons{
    margin-top:20px;
}

button{
    padding:12px 25px;
    font-size:18px;
    border:none;
    border-radius:10px;
    cursor:pointer;
    margin:10px;
}

#yes{
    background:#2ecc71;
    color:#fff;
}

#no{
    background:#e74c3c;
    color:#fff;
    position:absolute;
}

.jump{
    animation: jump 0.5s infinite alternate;
}

@keyframes jump{
    from{ transform:translateY(0); }
    to{ transform:translateY(-30px); }
}
</style>
</head>

<body>

<div class="container">
    <img id="teddy" src="https://i.imgur.com/1Xn0z0k.png">
    <h1 id="text">Shynu...Will you be my Valentine? 💖</h1>

    <div class="buttons">
        <button id="yes">Yes</button>
        <button id="no">No</button>
    </div>
</div>

<script>
const yesBtn = document.getElementById("yes");
const noBtn = document.getElementById("no");
const text = document.getElementById("text");
const teddy = document.getElementById("teddy");

yesBtn.onclick = () => {
    text.innerHTML = "I knew it! 😍💖";
    teddy.classList.add("jump");
};

noBtn.onmouseover = () => {
    const x = Math.random() * (window.innerWidth - 100);
    const y = Math.random() * (window.innerHeight - 100);
    noBtn.style.left = x + "px";
    noBtn.style.top = y + "px";
};
</script>

</body>
</html>
