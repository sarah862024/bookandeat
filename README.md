<script type='text/javascript' src='https://code.jquery.com/jquery-3.2.1.min.js'></script>
<script type='text/javascript'>
$(document).ready(function() {
    $("#login_button1").css("color", "green");
    $("#login_button1").css("background", "white");
    $("#login_button1").mouseenter(function(){
        $("#login_button1").css("color", "white");
        $("#login_button1").css("background", "green");
    });
    $("#login_button1").mouseout(function(){
        $("#login_button1").css("color", "green");
        $("#login_button1").css("background", "white");
    });
   $("#login_button2").css("color", "green");
   $("#login_button2").css("background", "white");
   $("#login_button2").mouseenter(function(){
        $("#login_button2").css("color", "white");
        $("#login_button2").css("background", "green");
   });
   $("#login_button2").mouseout(function(){
        $("#login_button2").css("color", "green");
        $("#login_button2").css("background", "white");
   });
   /*開啟登入框loginframe*/
   $("#login_button1").click(function(){
       $(".main").css({opacity:'0.5'});
        $(".loginframe").fadeIn("fast");
        $(".signupframe").fadeOut("fast");
   });
   $("#loginclose").click(function(){
        $(".loginframe").fadeOut("fast");
        $(".main").animate({opacity:'1'});
   });
   /*確定登入*/
   $("#ylogin").mouseenter(function(){
        $("#ylogin").css("color", "green");
        $("#ylogin").css("background", "white");
   });
   $("#ylogin").mouseout(function(){
        $("#ylogin").css("color", "white");
        $("#ylogin").css("background", "green");
   });
   /*開起註冊框signupframe*/
   $("#login_button2").click(function(){
       $(".main").css({opacity:'0.5'});
        $(".signupframe").fadeIn("fast");
        $(".loginframe").fadeOut("fast");
   });
   $("#signupclose").click(function(){
        $(".signupframe").fadeOut("fast");
        $(".main").animate({opacity:'1'});
   });
   /*確定註冊*/
   $("#ysignup").mouseenter(function(){
        $("#ysignup").css("color", "green");
        $("#ysignup").css("background", "white");
   });
   $("#ysignup").mouseout(function(){
        $("#ysignup").css("color", "white");
        $("#ysignup").css("background", "green");
   });

});

var jsImg = new Array(7);
jsImg[0] = 'https://raw.githubusercontent.com/sarah862024/bookandeat/master/Web%20k%E4%B8%AD%E5%BB%A3%E5%91%8A1.png';
jsImg[1] = 'https://raw.githubusercontent.com/sarah862024/bookandeat/master/Web%20k%E4%B8%AD%E5%BB%A3%E5%91%8A2.png';
jsImg[2] = 'https://raw.githubusercontent.com/sarah862024/bookandeat/master/Web%20k%E4%B8%AD%E5%BB%A3%E5%91%8A3.png';
jsImg[3] = 'https://raw.githubusercontent.com/sarah862024/bookandeat/master/Web%20k%E4%B8%AD%E5%BB%A3%E5%91%8A4.png';
jsImg[4] = 'https://raw.githubusercontent.com/sarah862024/bookandeat/master/Web%20k%E4%B8%AD%E5%BB%A3%E5%91%8A5.png';
jsImg[5] = 'https://raw.githubusercontent.com/sarah862024/bookandeat/master/Web%20k%E4%B8%AD%E5%BB%A3%E5%91%8A6.png';
jsImg[6] = 'https://raw.githubusercontent.com/sarah862024/bookandeat/master/Web%20k%E4%B8%AD%E5%BB%A3%E5%91%8A7.png';
        var jsImg_len = jsImg.length; 
        var i=0;
        setInterval("sequentialImg()",4000);
        function sequentialImg(){   
            document.getElementById("my_div").innerHTML  = "<img src='"+jsImg[i]+"' width=700 height=250>";        
                i++;
                if(i>=jsImg_len)  i=0;
        }
        
        
var fbImg = new Array(13);
fbImg[0] = 'https://raw.githubusercontent.com/sarah862024/bookandeat/master/K%E4%B8%AD%E9%A3%9F%E7%89%A91.png';
fbImg[1] = 'https://raw.githubusercontent.com/sarah862024/bookandeat/master/K%E4%B8%AD%E9%A3%9F%E7%89%A92.png';
fbImg[2] = 'https://raw.githubusercontent.com/sarah862024/bookandeat/master/K%E4%B8%AD%E9%A3%9F%E7%89%A93.png';
fbImg[3] = 'https://raw.githubusercontent.com/sarah862024/bookandeat/master/K%E4%B8%AD%E9%A3%9F%E7%89%A94.png';
fbImg[4] = 'https://raw.githubusercontent.com/sarah862024/bookandeat/master/K%E4%B8%AD%E9%A3%9F%E7%89%A95.png';
fbImg[5] = 'https://raw.githubusercontent.com/sarah862024/bookandeat/master/K%E4%B8%AD%E9%A3%9F%E7%89%A96.png';
fbImg[6] = 'https://raw.githubusercontent.com/sarah862024/bookandeat/master/K%E4%B8%AD%E9%A3%9F%E7%89%A97.png';
fbImg[7] = 'https://raw.githubusercontent.com/sarah862024/bookandeat/master/K%E4%B8%AD%E5%8F%83%E8%80%83%E6%9B%B81.png';
fbImg[8] = 'https://raw.githubusercontent.com/sarah862024/bookandeat/master/K%E4%B8%AD%E5%8F%83%E8%80%83%E6%9B%B82.png';
fbImg[9] = 'https://raw.githubusercontent.com/sarah862024/bookandeat/master/K%E4%B8%AD%E5%8F%83%E8%80%83%E6%9B%B83.png';
fbImg[10] = 'https://raw.githubusercontent.com/sarah862024/bookandeat/master/K%E4%B8%AD%E5%8F%83%E8%80%83%E6%9B%B84.png';
fbImg[11] = 'https://raw.githubusercontent.com/sarah862024/bookandeat/master/K%E4%B8%AD%E5%8F%83%E8%80%83%E6%9B%B85.png';
fbImg[12] = 'https://raw.githubusercontent.com/sarah862024/bookandeat/master/K%E4%B8%AD%E5%8F%83%E8%80%83%E6%9B%B86.png';
        var fbImg_len = fbImg.length; 
        var j=0;
        var $next=$('#fbad-left');
        var $fbaddiv =$block.find('#fbad_div');
        var isHover = false; 
        var timer=4000,speed=2000;
        //點擊下一個
        //滑鼠移入廣告框時click換mouseover
        $next.click(function(){
            document.getElementById("fbad_div").innerHTML  = "<img src='"+fbImg[j]+"' width=900 height=300>";        
            j++;
            if(j>=fbImg_len)  j=0;
            if(!isHover){
            //啟動計時器
            timer = setTimeout("sequentialImage()",4000);
            }
        });
        $fbaddiv.hover(function(){
            isHover = true ;
            //停止計時器
            clearTimeout(timer);
        }, function(){
              isHover = false;
              //啟動計時器
              timer=setTimeout("sequentialImage()",2000);
        })
       //自動下一個
       function sequentialImage(){ 
           if(isHover)return;
            document.getElementById("fbad_div").innerHTML  = "<img src='"+fbImg[j]+"' width=900 height=300>";        
                j++;
                if(j>=fbImg_len)  j=0;
        }
        //啟動計時器
         timer=setTimeout("sequentialImage()",2000);

</script>
<style>
body{
background-color:#CEFFCE;
weight:900px;
height:100%;
}
.login_button{
border-radius:2px;
width:150px;
height:50px;
font-size:20px;
font-family:Microsoft JhengHei;
cursor:pointer;
position:relative;
left:30px;
z-index:1;
}
.logo{
weight:160px;
height:120px;

}
.menu{
weight:900px;
height:50px;
background-color:#FFFFFF;
}
.ad-login{
weight:900px;
height:250px;
}
.k-ad{
float:left;
weight:700px;  
height:250px;
/*background-color:#424200;*/
}
.login{
float:right;
weight:200px;
height:250px;
background-image:url("https://lily0714.github.io/book-eat/登入面板1.png");
background-repeat:no-repeat;
background-size：contain contain;
border: 5px ridge green; 
margin-top:0px; 
margin-left:633px; 
margin-right:20px; 
margin-bottom:10px; 
padding-right:60px;
padding-bottom:-20px;
padding-top:60px;
z-index:1;
}
.loginframe{
weight:450px;
height:250px;
background-color:#FFFFFF;
border-radius:1px;
border-style:solid;
border-color:green;
position:fixed;
top:20%;
left:30%;
z-index:3;
display:none;
opacity:1;
}
.signupframe{
weight:450px;
height:250px;
background-color:#FFFFFF;
border-radius:1px;
border-style:solid;
border-color:green;
position:fixed;
top:20%;
left:30%;
z-index:3;
display:none;
opacity:1;
}
#logintitle{
float:left;
position:relative;
left:1px;
}
#loginclose{
cursor:pointer;
float:right;
position:relative;
right:1px;
}
#ylogin{
float:right;
position:relative;
right:50px;
bottom:-10px;
color:white;
background:green;
weight:110px;
height:110px;
font-family:Microsoft JhengHei;
font-size:20px;
border-radius:2px;
cursor:pointer;
}
#signuptitle{
float:left;
position:relative;
left:1px;
}
#signupclose{
cursor:pointer;
float:right;
position:relative;
right:1px;
}
#ysignup{
float:right;
position:relative;
right:50px;
bottom:-10px;
color:white;
background:green;
weight:110px;
height:110px;
font-family:Microsoft JhengHei;
font-size:20px;
border-radius:2px;
cursor:pointer;
}
.form1{
float:left;
position:relative;
left:50px;
}
.news-good{
weight:900px;
height:450px;
}
.news{
float:left;
weight:450px;
height:450px;
/*background-color:#0080FF;*/
}
.good{
weight:450px;
height:450px;
/*background-color:#9D9D9D;*/
}
.fbad{
weight:900px;
height:300px;
}
.link{
weight:900px;
height:100px;
background-color:#FF00FF;
}
#discount{
cursor:pointer;
position: fixed;
bottom: 0;
right: 0;
background-color:transparent;	
}
.information:hover{
color:green;
cursor:pointer;
}
.information{
font-size:20px;
font-family:Microsoft JhengHei;
position:relative;
top: 8px;
}
.bigback{
weight:1000px;
height:1200px;
background-image:url("https://lily0714.github.io/book-eat/全底圖1.png");
background-repeat:no-repeat;
background-color:transparent;
position:absolute;
z-index:-1;
}
#my_div{
position:absolute;
z-index:5;
margin-left:20px;
}
#fbad_div{
position:absolute;
z-index:5;
margin-left:40px;
}
#fbad-left{
float:left;
cursor:pointer;
}
#fbad-right{
float:right;
cursor:pointer;
}
</style>
<body onload="sequentialImg();">
<div class="main">
   <div class="logo">
   <img src="http://lily0714.github.io/book-eat/bookandeat.png" weight="160" height="120">
   </div>
   <div class="menu">
   <strong>
   <a href="https://sarah862024.github.io/bookandeat/" target="_self" style="text-decoration:none;color:black;">
   <nobr class="information" id="homepage">&emsp;&emsp;首  頁&nbsp;&emsp;</nobr></a>
   <a href="https://zx85010442.github.io/book-eat-About-Us/" target="_self" style="text-decoration:none;color:black;">
   <nobr class="information" id="know us">&nbsp;&emsp;&emsp;認識我們&nbsp;&emsp;</nobr></a> 
   <nobr class="information" id="book seat">&nbsp;&emsp;&emsp;預約座位&nbsp;&emsp;</nobr>
   <nobr class="information" id="traffic">&nbsp;&emsp;&emsp;交通位置&nbsp;&emsp;</nobr>
   <nobr class="information" id="QA">&nbsp;&emsp;&emsp;常見問題&nbsp;&emsp;</nobr>
   <nobr class="information" id="comment">&nbsp;&emsp;&emsp;意見回饋&nbsp;&emsp;</nobr><br> </strong>
   </div>
   <div class = "bigback">
   <div class="ad-login">
       <div class="k-ad">    
           <div id="my_div" ></div>
       </div>
       <div class="login">
           <p></p>
<b>
<input type="button" id="login_button1" class = "login_button" value=" 登 入 " />
<br>
<br>
<input type="button" id="login_button2" class = "login_button" value=" 註 冊 "/>
</b>
       </div>
  </div>
   <p></p>
       <div class="news-good">
            <div class="news">
                <p>最新動態</p>
            </div>
            <div class="good">
                <p>傑出動態</p>
            </div>
       </div>
   <p></p>
       <div class="fbad">
<img id="fbad-left" src="https://sarah862024.github.io/bookandeat/左.png" weight="50" height="300"><div id="fbad_div" ></div><img id="fbad-right" src="https://sarah862024.github.io/bookandeat/右.png" weight="50" height="300"> 
       </div>
      
       <div class="link">
         <p>重要連結</p>
       </div>
       </div>
</div>       

   <img id="discount" src="https://lily0714.github.io/book-eat/包月打八折正式.png" weight="130" height="160">

    <div class="loginframe">
<img id="logintitle" src="http://lily0714.github.io/book-eat/登入框頭1.png" weight="400" height="50"><img src="http://lily0714.github.io/book-eat/登入框關閉.png" id="loginclose" weight="50" height="50">
<br>
     <form class = "form1">
     <br>
     帳號:<input type="text" placeholder="請輸入帳號"><br><br>
     密碼:<input type="text" placeholder="請輸入密碼"><br>
     </form>
     <input type="button" id="ylogin" value="    登     入   "/>
     </div>
    <div class="signupframe">
<img id="signuptitle" src="http://lily0714.github.io/book-eat/註冊框頭.png" weight="400" height="50"><img src="http://lily0714.github.io/book-eat/登入框關閉.png" id="signupclose" weight="50" height="50">
<br>
     <form class = "form1">
     <br>
     帳號:<input type="text" placeholder="請輸入新帳號"><br><br>
     密碼:<input type="text" placeholder="請輸入新密碼"><br>
     </form>
     <input type="button" id="ysignup" value="    註     冊   "/>
     </div>
</body>
