<script type='text/javascript' src='https://code.jquery.com/jquery-3.2.1.min.js'></script>


<script type="text/javascript">
function changeImage() {
  var Value = document.getElementById("display").value;
  document.getElementById("selectimg").src = "https://raw.githubusercontent.com/sarah862024/bookandeat/master/" + Value + ".png";}
  function changeImage2() {
  var Value2 = document.getElementById("display2").value;
  document.getElementById("selectimg2").src = "https://raw.githubusercontent.com/sarah862024/bookandeat/master/" + Value2 + ".png";}
  function changeImage3() {
  var Value3 = document.getElementById("display3").value;
  document.getElementById("selectimg3").src = "https://raw.githubusercontent.com/sarah862024/bookandeat/master/" + Value3 + ".png";}
  function changeImage4() {
  var Value4 = document.getElementById("display4").value;
  document.getElementById("selectimg4").src = "https://raw.githubusercontent.com/sarah862024/bookandeat/master/" + Value4 + ".png";}
  function changeImage5() {
  var Value5 = document.getElementById("display5").value;
  document.getElementById("selectimg5").src = "https://raw.githubusercontent.com/sarah862024/bookandeat/master/" + Value5 + ".png";}
  function changeImage6() {
  var Value6 = document.getElementById("display6").value;
  document.getElementById("selectimg6").src = "https://raw.githubusercontent.com/sarah862024/bookandeat/master/" + Value6 + ".png";}
  function changeImage7() {
  var Value7 = document.getElementById("display7").value;
  document.getElementById("selectimg7").src = "https://raw.githubusercontent.com/sarah862024/bookandeat/master/" + Value7 + ".png";}
  function changeImage8() {
  var Value8 = document.getElementById("display8").value;
  document.getElementById("selectimg8").src = "https://raw.githubusercontent.com/sarah862024/bookandeat/master/" + Value8 + ".png";}

</script>

<style>
 
body{
 
background-color:#CEFFCE;
 
weight:900px;
 
height:100%;
 
}
.main{
weight:900px;
 
height:100%;
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
.announcement{
weight:900px;
height:900px;
font-family:Microsoft JhengHei;
}
#discount{
cursor:pointer;
position:fixed;
bottom:0;
 right:0; 
background-color:transparent;	
}
.ination:hover{
color:green;
cursor:pointer;
}
.information{
font-size:20px;
font-family:Microsoft JhengHei; 
position:relative; 
top:8px;
}
#regtitle{
font-size:30px;
color:green;
text-align:center;
}
.a1{
position:relative;
left:250px;
font-size:25px;
}
/* 已連結過 */
.a1:link{
color: #808000;
}
/* 未連結 */
.a1:visited{
color: #8FBC8F;
}
/* 滑鼠移至連結 */
.a1:hover{
color: #FFFFFF;
background-color:#8FBC8F;
}
/* 選擇的連結 */
.a1:active{
color: orange;
}
.single{
weight:900px;
height:500px;
}
.singleseat{
weight:500px;
height:500px;
float:left;
position:relative;
}
.select{
weight:400px;
height:500px;
position:relative;
left:50px;
}
.s{
weight:125px;
height:125px;
text-align:center;
padding:50px 62px 62px 62px;
}
#s1{
background-color:	#bfd8e3;
border: 3px solid gray;
border-radius:10px;
display:inline;
}
#s2{
background-color:	#bfd8e3;
border: 3px solid gray;
border-radius:10px;
display:inline;
}
#s3{
background-color:	#bfd8e3;
border: 3px solid gray;
border-radius:10px;
display:inline;
}
#s4{
background-color:	#bfd8e3;
border: 3px solid gray;
border-radius:10px;
display:inline;
}
#s5{
text-align:center;
background-color:	#f1f1b8;
padding:47px 62px 62px 62px;
border: 3px solid gray;
border-radius:10px;
position:relative;
top:70px;
}
#s6{
background-color:	#b8f1cc;
border: 3px solid gray;
border-radius:10px;
display:inline;
position:relative;
left:0px;
top:125px;
}
#s7{
background-color:	#b8f1cc;
border: 3px solid gray;
border-radius:10px;
display:inline;
position:relative;
left:2px;
top:125px;
}
#s8{
background-color:	#b8f1cc;
border: 3px solid gray;
border-radius:10px;
display:inline;
position:relative;
left:2px;
top:125px;
}
.s30{
weight:125px;
height:125px;
text-align:center;
}
#s9{
float:left;
padding: 130px 62px 140px 62px;
background-color:	#e4cde1;
border: 3px solid gray;
border-radius:10px;
position: relative;
left:465px;
top: 51px;
}
#s10{
float:left;
padding: 50px 60px 80px 53px;
background-color:	#b8f1cc;
border: 3px solid gray;
border-radius:10px;
display:inline;
position: relative;
left:-150px;
top: 192px;
}
#s11{
float:left;
padding: 50px 63px 80px 50px;
background-color:	#b8f1cc;
border: 3px solid gray;
border-radius:10px;
display:inline;
position: relative;
left:-143px;
top: 192px;
}
#s12{
padding: 50px 60px 60px 55px;
background-color:	#b8f1cc;
border: 3px solid gray;
border-radius:10px;
display:inline;
position: relative;
left:-137px;
top: 242px;
}
.foodimg{
float:left;
}
.bookfoodleft{
 float:left;
 weight:450px;
 height:450px;
 margin-left:180px;
 margin-top:32px;
  font-family:Microsoft JhengHei;
 }
 .bookfoodright{
 weight:450px;
 height:450px;
  margin-right:240px;
  font-family:Microsoft JhengHei;
  float:right;
 }
</style>
 
<body> 

<div class="main">
    
<div class="logo"><img src="http://lily0714.github.io/book-eat/bookandeat.png" weight="160" height="120"></div>
    
<div class="menu"> <strong>
    <a href="https://sarah862024.github.io/bookandeat/" target="_self" style="text-decoration:none;color:black;">
    <nobr class="information" id="homepage">&emsp;&emsp;首  頁&nbsp;&emsp;</nobr></a>
    <a href="https://sarah862024.github.io/bookandeat/about-us" target="_self" style="text-decoration:none;color:black;">
    <nobr class="information" id="know us">&nbsp;&emsp;&emsp;認識我們&nbsp;&emsp;</nobr></a> 
    <a href="https://sarah862024.github.io/bookandeat/bookseat" target="_self" style="text-decoration:none;color:black;">
    <nobr class="information" id="book seat">&nbsp;&emsp;&emsp;預約座位&nbsp;&emsp;</nobr></a>
    <a href="https://sarah862024.github.io/bookandeat/traffic" target="_self" style="text-decoration:none;color:black;">
    <nobr class="information" id="traffic">&nbsp;&emsp;&emsp;交通位置&nbsp;&emsp;</nobr></a>
    <a href="https://sarah862024.github.io/bookandeat/QA" target="_self" style="text-decoration:none;color:black;">
    <nobr class="information" id="QA">&nbsp;&emsp;&emsp;常見問題&nbsp;&emsp;</nobr></a>
    <a href="https://docs.google.com/a/gapp.fju.edu.tw/forms/d/e/1FAIpQLScVx-888W9pXGgX6TcoDJVicpdhJxE-g-Y2SBGr3MaosCAJ_g/viewform?usp=sf_link" target="_blank" style="text-decoration:none;color:black;">
    <nobr class="information" id="comment">&nbsp;&emsp;&emsp;意見回饋&nbsp;&emsp;</nobr></a><br> </strong> 
</div>
<div class = "bigback">
<div class="announcement">
<br/>
<strong>
<p id="regtitle">預約座位</p><br/><br/><br/><br/></strong>
  <div class="single">
     <div class="singleseat ">
        <div class="s" id="s1">A1</div>    
        <div class="s" id="s2">A2</div>
        <div class="s" id="s3">A3</div>
        <div class="s" id="s4">A4</div>
     <div class="row">
     <div id="s5">B5</div>
     <div class="s" id="s6">A6</div>
     <div class="s" id="s7">A7</div>
     <div class="s" id="s8">A8</div></div>
     <div class="row">
     <div class="s30" id="s9">C9</div>
     <div class="s30" id="s10">A10</div>
     <div class="s30" id="s11">A11</div>
     <div class="s30" id="s12">A12</div></div>
     <div class="row">
     <div id="s13"></div>
     <div class="s" id="s14"></div>
     <div class="s" id="s15"></div>
     <div class="s" id="s16"></div></div>
     </div>
     <div class="select">
              座位選擇區
     <form>
       <select style="width:150px" name="Yourseat">
       <optgroup label="單人區">
　     <option value="A1">單人區A1</option>
　     <option value="A2">單人區A2</option>
　     <option value="A3">單人區A3</option>
　     <option value="A4">單人區A4</option>
       <option value="A6">單人區A6</option>
       <option value="A7">單人區A7</option>
       <option value="A8">單人區A8</option>
       <option value="A10">單人區A10</option>
       <option value="A11">單人區A11</option>
       <option value="A12">單人區A12</option>
       <optgroup label="多人區">
       <option value="B5">多人區B5</option>
       <optgroup label="討論室">
       <option value="C9">討論室C9</option>
       </select>
       </form>
       </div>
       <input type="submit" value="預約">
       <br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/>
       <div>
       <strong>
<p id="regtitle">預約食物及參考書</p></strong>
<div class = "bookfoodleft">
 <p class="fdtitle">主食類</p>
   <form >
   <select id="display" onchange="changeImage()">
    <option>請選擇 </option>
  <option value="%E7%BE%A9%E5%A4%A7%E5%88%A9%E9%BA%B5">奶油香蒜墨魚義大利麵</option>
  <option value="%E7%95%AA%E8%8C%84%E9%86%AC%E7%82%92%E9%A3%AF">番茄炒飯</option>
  <option value="%E5%A5%B6%E6%B2%B9%E7%81%AB%E8%85%BF%E5%AF%AC%E9%BA%B5">奶油火腿寬麵</option>
   </select><br/><br/>
   <img class="game-picture"  id="selectimg">
   </form><br/>
    <p class="fdtitle">速食類</p>
   <form >
   <select id="display2" onchange="changeImage2()">
    <option>請選擇 </option>
  <option value="%E7%82%B8%E7%89%A9%E6%8B%BC%E7%9B%A4">炸物拼盤</option>
  <option value="%E8%B5%B7%E5%8F%B8%E7%89%9B%E8%82%89%E6%BC%A2%E5%A0%A1">起司牛肉漢堡</option>
  <option value="%E6%8A%AB%E8%96%A9">墨西哥辣味蘑菇披薩</option>
   </select><br/><br/>
   <img class="game-picture"  id="selectimg2">
   </form>
    <p class="fdtitle">輕食類</p>
   <form >
   <select id="display3" onchange="changeImage3()">
    <option>請選擇 </option>
  <option value="%E8%8A%B1%E7%94%9F%E9%86%AC%E4%B8%89%E6%98%8E%E6%B2%BB">花生醬火腿三明治</option>
  <option value="%E8%94%AC%E8%8F%9C%E4%B8%89%E6%98%8E%E6%B2%BB">蔬菜火腿三明治</option>
  <option value="%E8%94%AC%E8%8F%9C%E6%B2%99%E6%8B%89">新鮮蔬菜沙拉</option>
   </select><br/><br/>
   <img class="game-picture"  id="selectimg3">
   </form>
    <p class="fdtitle">水果類</p>
   <form >
   <select id="display4" onchange="changeImage4()">
    <option>請選擇 </option>
  <option value="%E5%A0%85%E6%9E%9C%E6%B0%B4%E6%9E%9C%E6%8B%BC%E7%9B%A4">堅果水果拼盤</option>
  <option value="%E6%B0%B4%E6%9E%9C%E6%8B%BC%E7%9B%A4">水果拼盤</option>
  <option value="%E6%B0%B4%E6%9E%9C%E9%BA%A5%E7%89%87%E5%84%AA%E6%A0%BC">水果麥片優格</option>
   </select><br/><br/>
   <img class="game-picture"  id="selectimg4">
   </form>
   </div>
   <div class="bookfoodright">
    <p class="fdtitle">飲料類</p>
   <form >
   <select id="display5" onchange="changeImage5()">
    <option>請選擇 </option>
  <option value="%E7%89%9B%E5%A5%B6">牛奶</option>
  <option value="%E9%A3%B2%E6%96%99">果昔</option>
  <option value="%E7%B2%BE%E5%8A%9B%E8%94%AC%E6%9E%9C%E6%B1%81">精力蔬果汁</option>
   </select><br/><br/>
   <img class="game-picture"  id="selectimg5">
   </form>
    <p class="fdtitle">點心類</p>
   <form >
   <select id="display6" onchange="changeImage6()">
    <option>請選擇 </option>
  <option value="%E8%9B%8B%E7%B3%95">提拉米蘇蛋糕</option>
  <option value="%E9%A4%85%E4%B9%BE">巧克力餅乾</option>
  <option value="%E9%AC%86%E9%A4%85">鬆餅</option>
  <option value="%E9%BA%B5%E5%8C%85">麵包</option>
   </select><br/><br/>
   <img class="game-picture"  id="selectimg6">
   </form>
    <p class="fdtitle">提神專區</p>
   <form >
   <select id="display7" onchange="changeImage7()">
    <option>請選擇 </option>
  <option value="%E8%8A%B1%E8%8C%B6">花茶</option>
  <option value="%E5%8F%A3%E9%A6%99%E7%B3%96">口香糖</option>
  <option value="%E5%92%96%E5%95%A1">咖啡</option>
  <option value="%E7%B6%A0%E8%8C%B6">綠茶</option>
   </select><br/><br/>
   <img class="game-picture"  id="selectimg7">
   </form>
    <p class="fdtitle">書籍專區與3C</p>
   <form >
   <select id="display8" onchange="changeImage8()">
    <option>請選擇 </option>
  <option value="%E9%87%8D%E9%BB%9E%E6%95%B4%E7%90%86">重點整理</option>
  <option value="%E6%9C%80%E6%96%B0%E6%9B%B8%E7%B1%8D">最新書籍</option>
  <option value="%E6%AD%B7%E5%B1%86%E8%80%83%E9%A1%8C">歷屆考題</option>
  <option value="%E7%A0%94%E7%A9%B6%E6%96%87%E7%8D%BB">研究文獻</option>
  <option value="%E7%B6%93%E5%85%B8%E5%8F%A4%E7%B1%8D">經典古籍</option>
  <option value="%E8%80%B3%E6%A9%9F">耳機</option>
  <option value="%E9%9B%BB%E8%85%A6">電腦</option>
   </select><br/><br/>
   <img class="game-picture"  id="selectimg8">
   </form>
   <br/><br/>
   <input type="submit" value="預約">
   <br/><br/>
   </div>
    </div>
<img id="discount" src="https://lily0714.github.io/book-eat/包月打八折正式.png" weight="130" height="160">

