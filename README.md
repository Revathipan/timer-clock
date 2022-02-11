# timer-clock
//html----<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Wikipedia Viewer</title>
    <link rel="stylesheet" type="text/css" href="style.css">
</head>
<body>
    <img id="image1" src=https://tse1.mm.bing.net/th?id=OIP.uETeqvrS4lpzaSgza4B0hgHaEB&pid=Api&P=0&w=343&h=186>
    <button id="toggleButton">Dark mode</button>
    <div id="clock-container">
        <div id="clock">
            <div id="center-point"></div>
            <div id="second"></div>
            <div id="minute"></div>
            <div id="hour"></div>
        </div>
        <div id="time">5:20 PM</div>
        <div id="date">TUESDAY, JAN 18</div>
    </div>
    <script type="text/javascript" src="app.js"></script>
</body>
</html>

css----*{
    color: red;
}
#image1{
    height: 40%;
    width: 60%;
    position: relative;
}
#toggleButton{
    position: absolute;
    top: 60px;
    left: 25%;
}
#time{
    position: absolute;
    top: 350px;
    left: 25%;
    display: block;
    font-size: 500;
    font-weight: 900;
}
#date{
    position: absolute;
    top: 400px;
    left: 25%;
    display: block;
    font-weight: 500;
}
#center-point{
    position: absolute;
    border-radius: 50%;
    height: 10px;
    width: 10px;
    top: 65px;
    left: 45%;
    background-color: red;
}
#clock{
    height: 150px;
    width: 150px;
    position: absolute;
    top: 150px;
    left: 25%;
    border-color: 2px solid red;
    /*background-color:white;*/
    border-radius: 50%;
}

#hour {
    width: 1.8%;
    height: 25%;
    top: 25%;
    left: 48.85%;
    opacity: 0.8;
}
  
#minute {
    width: 1.6%;
    height: 30%;
    top: 19%;
    left: 48.9%;
    opacity: 0.8;
}
  
#second {
    width: 1%;
    height: 40%;
    top: 9%;
    left: 49.25%;
    opacity: 0.8;
}

 
#hour,
#minute,
#second {
    position: absolute;
    background: rgb(233, 228, 228);
    border-radius: 10px;
    transform-origin: bottom;
}
js---setInterval(() => {
	d = new Date(); //object of date()
	hr = d.getHours();
	min = d.getMinutes();
	sec = d.getSeconds();
	hr_rotation = 30 * hr + min / 2; //converting current time
	min_rotation = 6 * min;
	sec_rotation = 6 * sec;

	hour.style.transform = `rotate(${hr_rotation}deg)`;
	minute.style.transform = `rotate(${min_rotation}deg)`;
	second.style.transform = `rotate(${sec_rotation}deg)`;
}, 1000);
