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
    $("#know us").click(function(){
        $(".content").fadeOut("fast");
       $(".about").fadeIn("fast");
    });
});
</script>
<style>
body{
background-color:#CEFFCE;
weight:900px;
height:100%;
}
.about{
display:none;
weight:900px;
height:300px;
align:center;
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
/*background-color:#0080FF;*/
border: 5px ridge green; 
margin-top:10px; 
margin-left:20px; 
margin-right:20px; 
margin-bottom:10px; 
padding-right:60px;
padding-bottom:-20px;
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
background-color:#9D9D9D;
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
</style>
<body>
<div class="main">
   <div class="logo">
   <img src="http://lily0714.github.io/book-eat/bookandeat.png" weight="160" height="120">
   </div>
   <div class="menu">
   <p><nobr class="information" id="know us">: 認識我們 :</nobr><nobr class="information" id="book seat">: 預約座位 :</nobr></p> 
   </div>
   <div class="content">
       <div class="ad-login">
           <div class="k-ad">
             <p>k中廣告1</p>
           </div>
           <div class="login">
             <p>登入</p>
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
           <p>食物跟參考書的廣告</p>
       </div>
      
       <div class="link">
         <p>重要連結</p>
       </div>
       
   /*主要內容外的東西*/
   <img id="discount" src="https://lily0714.github.io/book-eat/包月打八折正式.png" weight="130" height="160">
   /*彈出視窗在這*/
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
     </div>
     <div class="about">
           我們創立這個K書中心( 博客來一客 Book and Eat )是為了讓每個需要<br>
           讀書空間的人有既安靜又整潔的地方能夠使用。很多人常常讀書讀著讀著<br>
           肚子就餓了，又或著讀著讀著就開始恍神、打瞌睡、精神不濟。但是平常<br>
           在圖書館、公用的讀書空間之類的場所都是不準飲食的，讓很多人覺得很<br>
           困擾，甚至導致有人會在以上場所刻意違規偷偷吃東西喝飲料。如果您也<br>
           是這樣覺得，那博客來一客就是您的最佳選擇了，博客來一客提供大家安<br>
           靜整潔的舒適空間，另外也提供各式各樣的食物及飲品，讓你在認真讀書<br>
           的同時也能邊享用美食提振您的精神。<br>
     </div>
</body>

