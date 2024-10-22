# clock
#index.html
clock.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>case study</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="clock">
        <div id="hours"></div>
        <div id="minutes"></div>
        <div id="seconds"></div>
    </div>
    <img src="image.svg" class="logo"/>
<script src="script.js"></script>
</body>
</html>
#styles.css
.clock{
  height: 40vw;
  width: 40vw;
  margin: auto;
  background-image:url("pngwing.com.png");
  background-size: 100%;
  position: relative;
}
#hours,#minutes,#seconds{
  position: absolute;

  border-radius: 10px;
  transform-origin: bottom;
}
#hours{
  width: 1.8%;
  height: 25%;
  top: 25%;
  left: 49%;
  opacity: 0.65;
  background-color: black;
}
#minutes{
 width: 1.6%;
 height:35% ;
 top: 15%;
 left: 49%;
 opacity: 0.65;
 background-color: blueviolet;
}
#seconds{
  width: 1%;
  height:45% ;
  top: 6%;
  left: 49%;
  opacity: 0.65;
  background-color: red;
}
#script.js
setInterval(()=> {
    d=new Date();
    htime=d.getHours();
    mtime=d.getMinutes();
    stime=d.getSeconds();
    hrotation=30 * htime + mtime / 2;
    mrotation=6 * mtime;
    srotation=6 * stime;
     hours.style.transform=`rotate(${hrotation}deg)`;
    minutes.style.transform=`rotate(${mrotation}deg)`;
    seconds.style.transform=`rotate(${srotation}deg)`;
},1000);
#image.svg
<svg height="2500" width="2183" src="https://commons.wikimedia.org/wiki/File:Analogue_clock_face.svg"></svg>
