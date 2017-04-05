<html>
<head>
  <meta charset="UTF-8">
  <title>Rosa</title>
  <link rel="stylesheet" type="text/css" href="styles/style.css">
  <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.1.1/jquery.min.js"></script>
  <script src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/2542/jquery.scrollie.min_1.js"></script>
 
</head>
<body>

<div class="Row">
  <div class="Column" id="Video-button"><button onclick="scroll1()"><span>Video</span></button></div>
  <div class="Column" id="Data-button"><button onclick="scroll2()"><span>Data</span></button></div>
  <div class="Column" id="Threesixty-button"><button onclick="scroll3()"><span>360</span></button></div>
  <div class="Column" id="Video2-button"><button onclick="scroll4()"><span>Video 2</span></button></div>
</div>
<div class="boxes" id="first">
  <iframe src="https://player.vimeo.com/video/210800050" width="100%" height="100%" frameborder="0" webkitallowfullscreen="" mozallowfullscreen="" allowfullscreen=""></iframe>
</div>
<div class="boxes" id="second"><h1 id="progress-second">DATA VIZ</h1></div>
<div class="boxes" id="third"><h1 id="progress-third">360</h1></div>
<div class="boxes" id="fourth"><h1 id="progress-fourth">VIDEO 2</h1></div>


  <script>
// PROGRESS BAR GETS YELLOW WHILE SCROLLING

 $('#first').scrollie({
    direction : 'both',
    scrollOffset : 0,
    scrollRatio : 2,
    scrollingInView : function(){
    $('#Video-button').css("background", "yellow");
    },
  });

 $('#progress-second').scrollie({
    direction : 'both',
    scrollOffset : -500,
    scrollRatio : 2,
    scrollingInView : function(){
    $('#Data-button').css("background", "yellow");
    },
  });

  $('#progress-third').scrollie({
    direction : 'both',
    scrollOffset : -500,
    scrollRatio : 2,
    scrollingInView : function(){
    $('#Threesixty-button').css("background", "yellow");
    },
  });

   $('#progress-fourth').scrollie({
    direction : 'both',
    scrollOffset : -500,
    scrollRatio : 2,
    scrollingInView : function(){
    $('#Video2-button').css("background", "yellow");
    },
  });

 // PROGRESS BAR GETS YELLOW ON CLICK

  function scroll1() {
$('html, body').animate({
    scrollTop: $("#first").offset().top
}, 1000);
$('#Video-button').css("background", "yellow");
}

function scroll2() {
$('html, body').animate({
    scrollTop: $("#second").offset().top
}, 1000);
$('#Data-button').css("background", "yellow");
}

function scroll3() {
$('html, body').animate({
    scrollTop: $("#third").offset().top
}, 1000);
$('#Threesixty-button').css("background", "yellow");
}

function scroll4() {
$('html, body').animate({
    scrollTop: $("#fourth").offset().top
}, 1000);
$('#Video2-button').css("background", "yellow");
}

  </script>


</body>
</html>
