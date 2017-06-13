<html>
<head>
  <title>Bootstrap Example</title>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" />
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
  <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>

  <link rel="stylesheet" href="//maxcdn.bootstrapcdn.com/font-awesome/4.5.0/css/font-awesome.min.css" />

<link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css" />
<link href='http://fonts.googleapis.com/css?family=Oleo+Script' rel='stylesheet' type='text/css'>
<link href='http://fonts.googleapis.com/css?family=Pacifico' rel='stylesheet' type='text/css'>
<link href='http://fonts.googleapis.com/css?family=Great+Vibes' rel='stylesheet' type='text/css'>
<link rel="stylesheet" href="//maxcdn.bootstrapcdn.com/bootstrap/3.3.1/css/bootstrap.min.css" />
<style>
#heading{
  font-family: 'Pacifico';
  text-decoration: underline;
  font-style: normal;
  font-size: 500%;
  text-align: center;
  margin-bottom: 20px;
  color: white;
  text-shadow: 5px 5px #000;

}
.butn{
  background-color: darkorchid;
  padding: 10px;
  color: white;
  font-family: 'Great Vibes', cursive, monospace;
  font-size: 40px;
  margin : 20px;
  margin-left: 80px;
  transition: all 1s;
}
.butn:hover{
  background-color: red;
}
#my_canvas{
    background: #fff;
    border : saddlebrown 5px solid;
    margin-left: 40px;
    margin-top: 50px;
  box-shadow: 5px 5px 5px yellow;
    border-radius: 0% 30% 0% 30%;
  }
.tweet{
    background-color: blue;  
  padding: 10px;
  color: white;
  font-size: 40px;
  margin : 20px;
}
.tweet:hover{
  background:magenta;
  transition: all 1s;
}
</style>
  <body id="h">
  <header>
    <h1 id="heading">Random Quote Machine</h1>
  </header>
  <div class="container-fluid">
  <div class="row">
    <div class="col-xs-9">
      <button id="btn" class="butn" onclick="changeBG()">A new Quote</button>
    </div>
    
    <div class="col-xs-3">
      <a class="twitter" href="https://twitter.com/share" target="_blank"><button type="button" class="tweet"><i class="fa fa-twitter" aria-hidden="true"></i></button>
      </a>
    </div>
    <div class="col-xs-8"  id="quotes" >      
    </div>
  </div>    
  </div>
    <canvas id="my_canvas" width="1220px" height="300px"></canvas>
  <div id="write"></div>
  <script>
var col=["khaki","fuschia","chocolate","crimson","lawngreen","olive","red","dimgray","navy","rosybrown","purple","aqua","indigo","forestgreen","orchid","tan","gold","tomato","wheat","greenyellow","yellowgreen","darkmagenta","indianred","mediumorchid","hotpink","limegreen","darkcyan","goldenrod","palevioletred","violet","palegreen","thistle","orangered","coral","lightseagreen","chartreuse","olivedrab","springgreen","burlywood"];
function changeBG(){
  var elem=document.getElementById('h');
  elem.style.transition="background 1s linear 0s";
  elem.style.background=col[Math.floor(Math.random()*col.length)];
}
var i=0;
var comma = new Image();
comma.src =
  "http://pix.iemoji.com/images/emoji/apple/ios-9/256/sans-serif-heavy-double-turned-comma-quotation-mark-ornament.png";
var ctx;
var cw;
var ch;
var btn;
var riuquotes=[];
function initCanvas() {
  ctx = document.getElementById('my_canvas').getContext("2d");
  cw = ctx.canvas.width;
  ch = ctx.canvas.height;
  ctx.drawImage(
    comma,
    0,
    0,
    comma.width,
    comma.height,
    0,
    0,
    comma.width,
    comma.height
  );
  riuquotes = [
    {
      quote: "Arise, awake and stop not till the goal is reached.",
      person: " –Swami Vivekananda"
    },
    {
      quote:
        "Death is not extinguishing the light; it is only putting out the lamp because the dawn has come.",
      person: " –Rabindranath Tagore"
    },
    {
      quote: "Don't cry because it's over, smile because it happened.",
      person: " –Dr. Seuss"
    },
    {
      quote: "He who can become mad with an idea, he alone sees light.",
      person: " –Swami Vivekananda"
    },
    {
      quote: "Either you run the day, or the day runs you.",
      person: " –Jim Rohn"
    },
    {
      quote: "The best revenge is massive success.",
      person: " –Frank Sinatra"
    },
    {
      quote:
        "Instinct is like ice, reason is the water, and inspiration is the subtlest form of vapour.",
      person: " –Swami Vivekananda"
    },
    {
      quote:
        "When I hear somebody sigh, ‘Life is hard,’ I am always tempted to ask, ‘Compared to what?’",
      person: " –Sydney Harris"
    },
    {
      quote: "When I let go of what I am, I become what I might be.",
      person: " –Lao Tzu"
    },
    {
      quote: "If not us, who? If not now, when?",
      person: " –John Kennedy"
    },
    {
      quote:
        "The world is the great gymnasium where we come to make ourselves strong.",
      person: " –Swami Vivekananda"
    },
    {
      quote: "When the flower blooms, the bees come uninvited.",
      person: " –Ramakrishna Parmahamsa"
    },
    {
      quote:
        "The first principle of true teaching is that nothing can be taught!",
      person: " –Sir Aurobindo Ghosh"
    },
    {
      quote:
        "By plucking her petals you do not gather the beauty of the flower.",
      person: " –Rabindranath Tagore"
    },
    {
      quote: "The greatest religion is to be true to your own future.",
      person: " –Swami Vivekananda"
    },
    {
      quote:
        "Smile...it will either warm their heart or piss them off...either way you win!",
      person: " –Keep smiling!"
    },
    {
      quote: "The things I used to trip on, I walk over now!",
      person: " –GOAL SHOULD BE!"
    },
    {
      quote:
        "If you love someone,set them free. If they come back, they're yours; if they don't, they never were!",
      person: " –Richard Bach"
    },
    {
      quote:
        "Character is repeated habits, and repeated habits alone can reform character.",
      person: " –Swami Vivekananda"
    },
    {
      quote: "Stay Hungry, Stay Foolish!",
      person: " –Steve Jobs"
    },
    {
      quote:
        "The biggest changes in a women's nature are brought by love; in man, by ambition",
      person: " –Rabindranath Tagore"
    },
    {
      quote:
        "In order to see, you have to stop being in the middle of the picture.",
      person: " –Sir Aurobindo Ghosh"
    }
  ];
  
  btn = document.getElementById("btn");
  btn.addEventListener("mousedown", function(event) {    i=Math.floor(Math.random()*riuquotes.length);
    ctx.clearRect(comma.width, 0, cw - comma.width, ch);
    ctx.clearRect(0, comma.height, cw, ch - comma.height);
    ctx.fillStyle = "green";
    ctx.font = "bold 25px Oleo Script,Arial";
    ctx.fillText(riuquotes[i].quote, 10 + comma.width, 100);
    ctx.fillStyle = "#3364FF";
    ctx.font = "bold 40px Lobster,sans-serif";
    ctx.fillText(riuquotes[i].person, 300 + comma.width, 250);
  });
  $(".twitter").click(function(){
        $(this).attr("href", 'https://twitter.com/intent/tweet?text=' + riuquotes[i].quote);
      });
}
window.onload = initCanvas;

  </script>
</body>
</head>
</html>
