<?php
mysql_connect("localhost","root","webproject");//連結伺服器
mysql_select_db("webproject");//選擇資料庫
mysql_query("set names utf8");//以utf8讀取資料，讓資料可以讀取中文
$data=mysql_query("select * from webproject");//從contact資料庫中選擇所有的資料表
?>
<?php
require_once("connMysql.php");
session_start();
//檢查是否經過登入，若有登入則重新導向
if(isset($_SESSION["loginMember"]) && ($_SESSION["loginMember"]!="")){
	//若帳號等級為 member 則導向會員中心
	if($_SESSION["memberLevel"]=="member"){
		header("Location: member_center.php");
	//否則則導向管理中心
	}else{
		header("Location: member_admin.php");	
	}
}
//執行會員登入
if(isset($_POST["username"]) && isset($_POST["passwd"])){
	//繫結登入會員資料
	$query_RecLogin = "SELECT id, password FROM login WHERE id=?";
	$stmt=$db_link->prepare($query_RecLogin);
	$stmt->bind_param("s", $_POST["username"]);
	$stmt->execute();
	//取出帳號密碼的值綁定結果
	$stmt->bind_result($username, $passwd);	
	$stmt->fetch();
	$stmt->close();
	//比對密碼，若登入成功則呈現登入狀態
	if(password_verify($_POST["passwd"],$passwd)){
		//計算登入次數及更新登入時間
		$query_RecLoginUpdate = "UPDATE login SET logintime=NOW(),state==”預約” WHERE id=?";
		$stmt=$db_link->prepare($query_RecLoginUpdate);
	    $stmt->bind_param("s", $username);
	    $stmt->execute();	
	header("Location: 預約系統");	
	    $stmt->close();
    }else{
		header("Location: index.php?errMsg=1");
	}
}
?>
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
         setInterval("sequentialImage()",4000);
         function sequentialImage(){ 
             document.getElementById("fbad_div").innerHTML  = "<img src='"+fbImg[j]+"' width=900 height=300>";        
                 j++;
                 if(j>=fbImg_len)  j=0;
         }
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
 margin-left:20px;
 }
 #news-title{
 font-size:20px;
 color:green;
 font-family:Microsoft JhengHei;
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
 height:170px;
 background-color:#C4E1FF;
 }
 #discount{
 cursor:pointer;
 position: fixed;
 bottom: 0;
 right: 0;
 background-color:transparent;	
 z-index:20;
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
 background-size：cover
 position:absolute;
 z-index:-1;
 }
 #my_div{
 position:absolute;
 z-index:5;
 margin-left:20px;
 }
 #announcement{
 position:relative;
 left:200px;
 }
 #fbad_div{
 position:absolute;
 z-index:5;
 margin-left:40px;
 }
 #fbad-left{
 float:left;
 }
 #fbad-right{
 float:right;
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
    <a href="https://sarah862024.github.io/bookandeat/about-us" target="_self" style="text-decoration:none;color:black;">
    <nobr class="information" id="know us">&nbsp;&emsp;&emsp;認識我們&nbsp;&emsp;</nobr></a> 
    <nobr class="information" id="book seat">&nbsp;&emsp;&emsp;預約座位&nbsp;&emsp;</nobr>
    <a href="https://sarah862024.github.io/bookandeat/traffic" target="_self" style="text-decoration:none;color:black;">
    <nobr class="information" id="traffic">&nbsp;&emsp;&emsp;交通位置&nbsp;&emsp;</nobr></a>
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
                  <p id="news-title"><strong>最新動態</strong></p>
                  <a href="https://sarah862024.github.io/bookandeat/端午不營業"> 5/30端午節公休一天</a><br/><br/>
                  <a href="https://sarah862024.github.io/bookandeat/暑假搶先訂位">7/1~8/31暑假搶先訂位大特惠</a><br/><br/>
                  <a href="https://sarah862024.github.io/bookandeat/教師節訂書打75折">9/28慶祝教師節，預訂參考書打75折</a><br/><br/>
                  <a href="https://sarah862024.github.io/bookandeat/國慶營業時間">10/10國慶日早上不營業，下午1點開始營業</a><br/><br/>
                  <a href="https://sarah862024.github.io/bookandeat/萬聖節活動">10/31萬聖節來就送美味小糖果</a><br/><br/>
                  <a href="https://sarah862024.github.io/bookandeat/聖誕節活動">12/25聖誕節交換禮物活動</a><br/><br/>
                  <a href="https://sarah862024.github.io/bookandeat/跨年不營業">12/31~1/1跨年放假兩天</a><br/>
                  <a id="announcement" href="https://sarah862024.github.io/bookandeat/公告列表">更多公告</a>
              </div>
              <div class="good">
                 <p><strong>傑出動態</strong></p>
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
      <input type="button" id="ysignup" value="    註     冊   "/>
      </div>
 </body>
