<!DOCTYPE html>
<html>
	<head>
		<style>
			table, th, td {
				background-color: #2b2b2b;
				border: 1px solid #ff4040;
				color: #ffe8d1;
			}
			input {
				color: #ffe8d1;
			}
			button {
				background-color: #ffffff00;
				border: 3px solid #ff4040;
				color: #ffe8d1;
  				cursor: pointer;
			}
			.container {
				width: 12.67%;
				height: 16px;
			}

			.container .btn {
				width: 100%;
  				background-color: #55555500;
  				color: #ffffff00;
  				font-size: 16px;
  				border: 5px solid #000000;
				border-radius: 5px;
			}


			.container img {
				width: 4.2%;
				height: 22px;
			}

			.divflex {
				display: flex;
				width: 100%;
			}

			.images {
				width: 12.5%;
				height: fit-content;
			}

			.images img {
				width: 100%;
				height: 100%;
			}
			.images .ibtn {
				width: 100%;
				height: fit-content;
				transform: translate(0px, -100%);
				background-color: #40404000;
				border: 3px solid #404040;
				color: #40404000;
			}
		</style>
	</head>
	<body style="background-color:#404040;">
		<center>
			<font face = "Cherry Cream Soda, Bahnschrift Semibold Condensed">
				<h1 style="color: #ffe8d1;">The <a style="color: #ffe8d1;" href="https://chesscraft.ca">ChessCraft</a> Piece Library!</h1>
				<table style="width:53.125%;margin-bottom:3px">
					<tr>
						<th style="width:25%">Strength</th>
						<th style="width:25%">Rook</th>
						<th style="width:25%">Bishop</th>
						<th>Knight</th>
					</tr>
				</table>
				<div class="container" style="transform: translate(-159%, -2px)">
					<img id="strengthimg" src="images/slider.png" style="transform: translate(0%, 4px)">
					<button id="strength" class="btn" onmousedown = "funStrength(event)" onmousemove = "funMouse(event)" onclick = "funUp(event)" onmouseout = "funUp(event)" onmouseup = "funMouse(event)" style="transform: translate(0px, -22px)">50</button>
				</div>
				<div class="container" style="transform: translate(-53%, -18px)">
					<img id="rookimg" src="images/slider.png" style="transform: translate(-356%, 4px)">
					<button id="rook" class="btn" onmousedown = "funRook(event)" onmousemove = "funMouse(event)" onclick = "funUp(event)" onmouseout = "funUp(event)" onmouseup = "funMouse(event)" style="transform: translate(0px, -22px)">33</button>
				</div>
				<div class="container" style="transform: translate(53%, -34px)">
					<img id="bishopimg" src="images/slider.png" style="transform: translate(-356%, 4px)">
					<button id="bishop" class="btn" onmousedown = "funBishop(event)" onmousemove = "funMouse(event)" onclick = "funUp(event)" onmouseout = "funUp(event)" onmouseup = "funMouse(event)" style="transform: translate(0px, -22px)">33</button>
				</div>
				<div class="container" style="transform: translate(159%, -50px)">
					<img id="knightimg" src="images/slider.png" style="transform: translate(-356%, 4px)">
					<button id="knight" class="btn" onmousedown = "funKnight(event)" onmousemove = "funMouse(event)" onclick = "funUp(event)" onmouseout = "funUp(event)" onmouseup = "funMouse(event)" style="transform: translate(0px, -22px)">33</button>
				</div>
				<table style="width:53.125%;margin-bottom:3px">		
					<tr>
						<th style="width:25%">Forwardness</th>
						<th style="width:25%">Wideness</th>
						<th style="width:25%">Move/Capture</th>
						<th style="width:25%">Left/Right</th>
					</tr>
				</table>
				<div class="container" style="transform: translate(-159%, -2px)">
					<img id="forwardimg" src="images/slider.png" style="transform: translate(0%, 4px)">
					<button id="forwardness" class="btn" onmousedown = "funForward(event)" onmousemove = "funMouse(event)" onclick = "funUp(event)" onmouseout = "funUp(event)" onmouseup = "funMouse(event)" style="transform: translate(0px, -22px)">50</button>
				</div>
				<div class="container" style="transform: translate(-53%, -18px)">
					<img id="wideimg" src="images/slider.png" style="transform: translate(0%, 4px)">
					<button id="wideness" class="btn" onmousedown = "funWide(event)" onmousemove = "funMouse(event)" onclick = "funUp(event)" onmouseout = "funUp(event)" onmouseup = "funMouse(event)" style="transform: translate(0px, -22px)">50</button>
				</div>
				<div class="container" style="transform: translate(53%, -34px)">
					<img id="moveimg" src="images/slider.png" style="transform: translate(0%, 4px)">
					<button id="move/captr" class="btn" onmousedown = "funMove(event)" onmousemove = "funMouse(event)" onclick = "funUp(event)" onmouseout = "funUp(event)" onmouseup = "funMouse(event)" style="transform: translate(0px, -22px)">50</button>
				</div>
				<div class="container"style="transform: translate(159%, -50px)">
					<img id="sideimg" src="images/slider.png" style="transform: translate(0%, 4px)">
					<button id="left/right" class="btn" onmousedown = "funSide(event)" onmousemove = "funMouse(event)" onclick = "funUp(event)" onmouseout = "funUp(event)" onmouseup = "funMouse(event)" style="transform: translate(0px, -22px)">50</button>
				</div>
				<button id="sort" onclick=" return funSort(event)" style="color:#ffe8d1">Sort!</button>
				<h1 style = "color:#ffe8d1" id="piece1"></h1>
				<h1 style = "color:#ffe8d1" id="piece2"></h1>
				<h1 style = "color:#ffe8d1" id="piece3"></h1>
				<h1 style = "color:#ffe8d1" id="piece4"></h1>
				<h1 style = "color:#ffe8d1" id="piece5"></h1>
				<h2 style="color:#ffe8d1">The Rules</h2>
				<div class="divflex">
					<div class="images">
						<img src="images/2-pawn.png" alt="double advance">
						<button id="button2" class="ibtn" onclick=" return func2(event)">0</button>
					</div>
					<div class="images">
						<img src="images/3-pawn.png" alt="triple advance">
						<button id="button3" class="ibtn" onclick=" return func2(event)">0</button>
					</div>
					<div class="images">
						<img src="images/4-pawn.png" alt="quadruple advance">
						<button id="button4" class="ibtn" onclick=" return func2(event)">0</button>
					</div>
					<div class="images">
						<img src="images/en-passant.png" alt="en passant">
						<button id="buttone" class="ibtn" onclick=" return func2(event)">0</button>
					</div>
					<div class="images">
						<img src="images/kingcastle.png" alt="king castle">
						<button id="buttonk" class="ibtn" onclick=" return func2(event)">0</button>
					</div>
					<div class="images">
						<img src="images/rookcastle.png" alt="rook castle">
						<button id="buttonr" class="ibtn" onclick=" return func2(event)">0</button>
					</div>
					<div class="images">
						<img src="images/check.png" alt="check">
						<button id="buttonc" class="ibtn" onclick=" return func2(event)">0</button>
					</div>
					<div class="images">
						<img src="images/iron.png" alt="iron">
						<button id="buttoni" class="ibtn" onclick=" return func2(event)">0</button>
					</div>
				</div>
				<div id="botrow" class="divflex" style="margin-top: -192px">
					<div class="images">
						<img src="images/range.png" alt="range">
						<button id="buttonra" class="ibtn" onclick=" return func2(event)">0</button>
					</div>
					<div class="images">
						<img src="images/pacifism.png" alt="pacifism">
						<button id="buttonp" class="ibtn" onclick=" return func2(event)">0</button>
					</div>
					<div class="images">
						<img src="images/anchor.png" alt="anchor">
						<button id="buttona" class="ibtn" onclick=" return func2(event)">0</button>
					</div>
					<div class="images">
						<img src="images/trojan.png" alt="trojan">
						<button id="buttont" class="ibtn" onclick=" return func2(event)">0</button>
					</div>
					<div class="images">
						<img src="images/medusa.png" alt="medusa">
						<button id="buttonm" class="ibtn" onclick=" return func2(event)">0</button>
					</div>
					<div class="images">
						<img src="images/angel.png" alt="angel">
						<button id="buttonan" class="ibtn" onclick=" return func2(event)">0</button>
					</div>
					<div class="images">
						<img src="images/ahimsa.png" alt="ahimsa">
						<button id="buttonah" class="ibtn" onclick=" return func2(event)">0</button>
					</div>
					<div class="images">
						<img src="images/cannon.png" alt="cannon">
						<button id="buttonca" class="ibtn" onclick=" return func2(event)">0</button>
					</div>
				</div>
			</font>
		</center>
		<script type="text/javascript">
			function func2 (event) {
				element = document.activeElement.innerHTML;
				if (element == "0") {
					document.activeElement.innerHTML = "1000";
					document.activeElement.style.border = "3px solid #ff4040";
				}
				else {
					document.activeElement.innerHTML = "0";
					document.activeElement.style.border = "3px solid #404040";
				}
			}
			var varclick = 0;
			var pox;
			function funStrength() {
				corimage = strengthimg;
				varclick = 1;
			}
			function funRook() {
				corimage = rookimg;
				varclick = 1;
			}
			function funBishop() {
				corimage = bishopimg;
				varclick = 1;
			}
			function funKnight() {
				corimage = knightimg;
				varclick = 1;
			}
			function funForward() {
				corimage = forwardimg;
				varclick = 1;
			}
			function funWide() {
				corimage = wideimg;
				varclick = 1;
			}
			function funMove() {
				corimage = moveimg;
				varclick = 1;
			}
			function funSide() {
				corimage = sideimg;
				varclick = 1;
			}
			function funUp(e) {
				if (varclick == 1) {
					varclick = 0;
				}
			}
			function funMouse(e) {
				if (varclick == 1) {
					outwidth = window.innerWidth;
					pox = e.offsetX + 8;
					if ((Math.round((((pox / (outwidth / 1536)) / 2 - 50) * 1.19) + 50)) <= 100 & (Math.round((((pox / (outwidth / 1536)) / 2 - 50) * 1.19) + 50)) >= 0) {
						document.activeElement.innerHTML = Math.round((((pox / (outwidth / 1536)) / 2 - 50) * 1.19) + 50);
						corimage.style.transform = "translate(" + Math.round((((pox) / (outwidth / 1536)) / 2 - 50) * 25) + "%, 4px)";
						if (document.activeElement == rook) {
							var bishnum = Number(document.getElementById('bishop').innerHTML);
							var knignum = Number(document.getElementById('knight').innerHTML);
							var bishopmul = (bishnum + knignum) / bishnum;
							var knightmul = (bishnum + knignum) / knignum;
							if (bishopmul > 0 & knightmul > 0) {
								document.getElementById('bishop').innerHTML = Math.round((100 - Math.round((((pox / (outwidth / 1536)) / 2 - 50) * 1.19) + 50)) / bishopmul);
								document.getElementById('knight').innerHTML = Math.round((100 - Math.round((((pox / (outwidth / 1536)) / 2 - 50) * 1.19) + 50)) / knightmul);
								bishnum = Number(document.getElementById('bishop').innerHTML);
								knignum = Number(document.getElementById('knight').innerHTML);
								document.getElementById('bishopimg').style.transform = "translate(" + Math.round(bishnum * 21 - 1050) + "%, 4px)";
								document.getElementById('knightimg').style.transform = "translate(" + Math.round(knignum * 21 - 1050) + "%, 4px)";
							}
						}
						if (document.activeElement == bishop) {
							var rooknum = Number(document.getElementById('rook').innerHTML);
							var knignum = Number(document.getElementById('knight').innerHTML);
							var rookmul = (rooknum + knignum) / rooknum;
							var knightmul = (rooknum + knignum) / knignum;
							if (rookmul > 0 & knightmul > 0) {
								document.getElementById('rook').innerHTML = Math.round((100 - Math.round((((pox / (outwidth / 1536)) / 2 - 50) * 1.19) + 50)) / rookmul);
								document.getElementById('knight').innerHTML = Math.round((100 - Math.round((((pox / (outwidth / 1536)) / 2 - 50) * 1.19) + 50)) / knightmul);
								rooknum = Number(document.getElementById('rook').innerHTML);
								knignum = Number(document.getElementById('knight').innerHTML);
								document.getElementById('rookimg').style.transform = "translate(" + Math.round(rooknum * 21 - 1050) + "%, 4px)";
								document.getElementById('knightimg').style.transform = "translate(" + Math.round(knignum * 21 - 1050) + "%, 4px)";
							}
						}
						if (document.activeElement == knight) {
							var bishnum = Number(document.getElementById('bishop').innerHTML);
							var rooknum = Number(document.getElementById('rook').innerHTML);
							var bishopmul = (bishnum + rooknum) / bishnum;
							var rookmul = (bishnum + rooknum) / rooknum;
							if (bishopmul > 0 & rookmul > 0) {
								document.getElementById('bishop').innerHTML = Math.round((100 - Math.round((((pox / (outwidth / 1536)) / 2 - 50) * 1.19) + 50)) / bishopmul);
								document.getElementById('rook').innerHTML = Math.round((100 - Math.round((((pox / (outwidth / 1536)) / 2 - 50) * 1.19) + 50)) / rookmul);
								bishnum = Number(document.getElementById('bishop').innerHTML);
								rooknum = Number(document.getElementById('rook').innerHTML);
								document.getElementById('bishopimg').style.transform = "translate(" + Math.round(bishnum * 21 - 1050) + "%, 4px)";
								document.getElementById('rookimg').style.transform = "translate(" + Math.round(rooknum * 21 - 1050) + "%, 4px)";
							}
						}
					}
				}
			}
			function funSort(e) {
				var rules = [document.getElementById('button2').innerHTML, document.getElementById('button3').innerHTML, document.getElementById('button4').innerHTML, document.getElementById('buttone').innerHTML, document.getElementById('buttonk').innerHTML, document.getElementById('buttonr').innerHTML, document.getElementById('buttonc').innerHTML, document.getElementById('buttoni').innerHTML, document.getElementById('buttonra').innerHTML, document.getElementById('buttonp').innerHTML, document.getElementById('buttona').innerHTML, document.getElementById('buttont').innerHTML, document.getElementById('buttonm').innerHTML, document.getElementById('buttonan').innerHTML, document.getElementById('buttonah').innerHTML, document.getElementById('buttonca').innerHTML];
				var Alfil = [3, 0, 0, 100, 50, 50, 50, 50, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0];
				var Alibaba = [8, 0, 0, 100, 50, 50, 50, 50, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0];
				var Archbishop = [38, 0, 50, 50, 50, 50, 50, 50, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0];
				var Armed_Treasury = [14, 65, 12, 23, 87, 80, 50, 50, 0, 0, 0, 0, 0, 0, 1000, 0, 0, 0, 0, 0, 0, 0, 0, 0];
				var Axeman = [4, 100, 0, 0, 67, 67, 50, 50, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0];
				var Bandmaster = [23, 0, 0, 100, 50, 50, 50, 50, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0];
				var Bear = [40, 13, 13, 74, 50, 50, 50, 50, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0];
				var Chancellor = [44, 50, 0, 50, 50, 50, 50, 50, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0];
				var Dababba = [4, 0, 0, 100, 50, 50, 50, 50, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0];
				var Dolphin = [11, 33, 33, 34, 50, 50, 45, 50, 0, 0, 0, 0, 0, 0, 0, 0, 1000, 0, 0, 0, 0, 0, 0, 0];
				var Earth_Centaur = [13, 33, 0, 67, 50, 75, 50, 50, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0];
				var Ferz = [5, 0, 100, 0, 50, 50, 50, 50, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0];
				var Fire_Centaur = [13, 0, 33, 67, 50, 25, 50, 50, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0];
				var Horizontal_Mover = [10, 100, 0, 0, 50, 89, 50, 50, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0];
				var Kirin = [9, 0, 33, 67, 50, 50, 50, 50, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0];
				var Lance = [2, 100, 0, 0, 100, 0, 50, 50, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0];
				var Man = [11, 50, 50, 0, 50, 50, 50, 50, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0];
				var Overpreparer = [2, 0, 100, 0, 100, 50, 50, 50, 0, 0, 0, 0, 0, 0, 0, 1000, 0, 0, 0, 0, 0, 0, 0, 0];
				var Paladin = [20, 0, 0, 100, 50, 50, 50, 50, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0];
				var Phoenix = [12, 33, 0, 67, 50, 50, 50, 50, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0];
				var Prince = [60, 0, 0, 100, 50, 50, 50, 50, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0];
				var Silver_King = [7, 20, 80, 0, 60, 40, 50, 50, 0, 0, 0, 0, 0, 0, 1000, 0, 0, 0, 0, 0, 0, 0, 0, 0];
				var Spearman = [10, 75, 25, 0, 75, 25, 50, 50, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0];
				var Spider = [4, 50, 50, 0, 75, 75, 50, 50, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0];
				var Wasir = [6, 100, 0, 0, 50, 50, 50, 50, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0];
				var Vertical_Mover = [10, 100, 0, 0, 50, 11, 50, 50, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0];
				var Vortex = [5, 33, 0, 67, 50, 50, 40, 50, 0, 0, 0, 0, 0, 0, 0, 0, 1000, 0, 0, 0, 0, 0, 0, 0];
				var Xeawn = [8, 25, 25, 50, 50, 50, 27, 50, 0, 0, 0, 0, 0, 0, 0, 0, 1000, 0, 0, 0, 0, 0, 0, 0];
				Alfil = Math.abs(Alfil[0] - document.getElementById('strength').innerHTML) + Math.abs(Alfil[1] - document.getElementById('rook').innerHTML) + Math.abs(Alfil[2] - document.getElementById('bishop').innerHTML) + Math.abs(Alfil[3] - document.getElementById('knight').innerHTML) + Math.abs(Alfil[4] - document.getElementById('forwardness').innerHTML) + Math.abs(Alfil[5] - document.getElementById('wideness').innerHTML) + Math.abs(Alfil[6] - document.getElementById('move/captr').innerHTML) + Math.abs(Alfil[7] - document.getElementById('left/right').innerHTML + Math.abs(Alfil[8] - rules[0]) + Math.abs(Alfil[9] - rules[1]) + Math.abs(Alfil[10] - rules[2]) + Math.abs(Alfil[11] - rules[3]) + Math.abs(Alfil[12] - rules[4]) + Math.abs(Alfil[13] - rules[5]) + Math.abs(Alfil[14] - rules[6]) + Math.abs(Alfil[15] - rules[7]) + Math.abs(Alfil[16] - rules[8]) + Math.abs(Alfil[17] - rules[9]) + Math.abs(Alfil[18] - rules[10]) + Math.abs(Alfil[19] - rules[11]) + Math.abs(Alfil[20] - rules[12]) + Math.abs(Alfil[21] - rules[13]) + Math.abs(Alfil[22] - rules[14]) + Math.abs(Alfil[23] - rules[15]));
				Alibaba = Math.abs(Alibaba[0] - document.getElementById('strength').innerHTML) + Math.abs(Alibaba[1] - document.getElementById('rook').innerHTML) + Math.abs(Alibaba[2] - document.getElementById('bishop').innerHTML) + Math.abs(Alibaba[3] - document.getElementById('knight').innerHTML) + Math.abs(Alibaba[4] - document.getElementById('forwardness').innerHTML) + Math.abs(Alibaba[5] - document.getElementById('wideness').innerHTML) + Math.abs(Alibaba[6] - document.getElementById('move/captr').innerHTML) + Math.abs(Alibaba[7] - document.getElementById('left/right').innerHTML + Math.abs(Alibaba[8] - rules[0]) + Math.abs(Alibaba[9] - rules[1]) + Math.abs(Alibaba[10] - rules[2]) + Math.abs(Alibaba[11] - rules[3]) + Math.abs(Alibaba[12] - rules[4]) + Math.abs(Alibaba[13] - rules[5]) + Math.abs(Alibaba[14] - rules[6]) + Math.abs(Alibaba[15] - rules[7]) + Math.abs(Alibaba[16] - rules[8]) + Math.abs(Alibaba[17] - rules[9]) + Math.abs(Alibaba[18] - rules[10]) + Math.abs(Alibaba[19] - rules[11]) + Math.abs(Alibaba[20] - rules[12]) + Math.abs(Alibaba[21] - rules[13]) + Math.abs(Alibaba[22] - rules[14]) + Math.abs(Alibaba[23] - rules[15]));
				Archbishop = Math.abs(Archbishop[0] - document.getElementById('strength').innerHTML) + Math.abs(Archbishop[1] - document.getElementById('rook').innerHTML) + Math.abs(Archbishop[2] - document.getElementById('bishop').innerHTML) + Math.abs(Archbishop[3] - document.getElementById('knight').innerHTML) + Math.abs(Archbishop[4] - document.getElementById('forwardness').innerHTML) + Math.abs(Archbishop[5] - document.getElementById('wideness').innerHTML) + Math.abs(Archbishop[6] - document.getElementById('move/captr').innerHTML) + Math.abs(Archbishop[7] - document.getElementById('left/right').innerHTML + Math.abs(Archbishop[8] - rules[0]) + Math.abs(Archbishop[9] - rules[1]) + Math.abs(Archbishop[10] - rules[2]) + Math.abs(Archbishop[11] - rules[3]) + Math.abs(Archbishop[12] - rules[4]) + Math.abs(Archbishop[13] - rules[5]) + Math.abs(Archbishop[14] - rules[6]) + Math.abs(Archbishop[15] - rules[7]) + Math.abs(Archbishop[16] - rules[8]) + Math.abs(Archbishop[17] - rules[9]) + Math.abs(Archbishop[18] - rules[10]) + Math.abs(Archbishop[19] - rules[11]) + Math.abs(Archbishop[20] - rules[12]) + Math.abs(Archbishop[21] - rules[13]) + Math.abs(Archbishop[22] - rules[14]) + Math.abs(Archbishop[23] - rules[15]));
				Armed_Treasury = Math.abs(Armed_Treasury[0] - document.getElementById('strength').innerHTML) + Math.abs(Armed_Treasury[1] - document.getElementById('rook').innerHTML) + Math.abs(Armed_Treasury[2] - document.getElementById('bishop').innerHTML) + Math.abs(Armed_Treasury[3] - document.getElementById('knight').innerHTML) + Math.abs(Armed_Treasury[4] - document.getElementById('forwardness').innerHTML) + Math.abs(Armed_Treasury[5] - document.getElementById('wideness').innerHTML) + Math.abs(Armed_Treasury[6] - document.getElementById('move/captr').innerHTML) + Math.abs(Armed_Treasury[7] - document.getElementById('left/right').innerHTML + Math.abs(Armed_Treasury[8] - rules[0]) + Math.abs(Armed_Treasury[9] - rules[1]) + Math.abs(Armed_Treasury[10] - rules[2]) + Math.abs(Armed_Treasury[11] - rules[3]) + Math.abs(Armed_Treasury[12] - rules[4]) + Math.abs(Armed_Treasury[13] - rules[5]) + Math.abs(Armed_Treasury[14] - rules[6]) + Math.abs(Armed_Treasury[15] - rules[7]) + Math.abs(Armed_Treasury[16] - rules[8]) + Math.abs(Armed_Treasury[17] - rules[9]) + Math.abs(Armed_Treasury[18] - rules[10]) + Math.abs(Armed_Treasury[19] - rules[11]) + Math.abs(Armed_Treasury[20] - rules[12]) + Math.abs(Armed_Treasury[21] - rules[13]) + Math.abs(Armed_Treasury[22] - rules[14]) + Math.abs(Armed_Treasury[23] - rules[15]));
				Axeman = Math.abs(Axeman[0] - document.getElementById('strength').innerHTML) + Math.abs(Axeman[1] - document.getElementById('rook').innerHTML) + Math.abs(Axeman[2] - document.getElementById('bishop').innerHTML) + Math.abs(Axeman[3] - document.getElementById('knight').innerHTML) + Math.abs(Axeman[4] - document.getElementById('forwardness').innerHTML) + Math.abs(Axeman[5] - document.getElementById('wideness').innerHTML) + Math.abs(Axeman[6] - document.getElementById('move/captr').innerHTML) + Math.abs(Axeman[7] - document.getElementById('left/right').innerHTML + Math.abs(Axeman[8] - rules[0]) + Math.abs(Axeman[9] - rules[1]) + Math.abs(Axeman[10] - rules[2]) + Math.abs(Axeman[11] - rules[3]) + Math.abs(Axeman[12] - rules[4]) + Math.abs(Axeman[13] - rules[5]) + Math.abs(Axeman[14] - rules[6]) + Math.abs(Axeman[15] - rules[7]) + Math.abs(Axeman[16] - rules[8]) + Math.abs(Axeman[17] - rules[9]) + Math.abs(Axeman[18] - rules[10]) + Math.abs(Axeman[19] - rules[11]) + Math.abs(Axeman[20] - rules[12]) + Math.abs(Axeman[21] - rules[13]) + Math.abs(Axeman[22] - rules[14]) + Math.abs(Axeman[23] - rules[15]));
				Bandmaster = Math.abs(Bandmaster[0] - document.getElementById('strength').innerHTML) + Math.abs(Bandmaster[1] - document.getElementById('rook').innerHTML) + Math.abs(Bandmaster[2] - document.getElementById('bishop').innerHTML) + Math.abs(Bandmaster[3] - document.getElementById('knight').innerHTML) + Math.abs(Bandmaster[4] - document.getElementById('forwardness').innerHTML) + Math.abs(Bandmaster[5] - document.getElementById('wideness').innerHTML) + Math.abs(Bandmaster[6] - document.getElementById('move/captr').innerHTML) + Math.abs(Bandmaster[7] - document.getElementById('left/right').innerHTML + Math.abs(Bandmaster[8] - rules[0]) + Math.abs(Bandmaster[9] - rules[1]) + Math.abs(Bandmaster[10] - rules[2]) + Math.abs(Bandmaster[11] - rules[3]) + Math.abs(Bandmaster[12] - rules[4]) + Math.abs(Bandmaster[13] - rules[5]) + Math.abs(Bandmaster[14] - rules[6]) + Math.abs(Bandmaster[15] - rules[7]) + Math.abs(Bandmaster[16] - rules[8]) + Math.abs(Bandmaster[17] - rules[9]) + Math.abs(Bandmaster[18] - rules[10]) + Math.abs(Bandmaster[19] - rules[11]) + Math.abs(Bandmaster[20] - rules[12]) + Math.abs(Bandmaster[21] - rules[13]) + Math.abs(Bandmaster[22] - rules[14]) + Math.abs(Bandmaster[23] - rules[15]));
				Bear = Math.abs(Bear[0] - document.getElementById('strength').innerHTML) + Math.abs(Bear[1] - document.getElementById('rook').innerHTML) + Math.abs(Bear[2] - document.getElementById('bishop').innerHTML) + Math.abs(Bear[3] - document.getElementById('knight').innerHTML) + Math.abs(Bear[4] - document.getElementById('forwardness').innerHTML) + Math.abs(Bear[5] - document.getElementById('wideness').innerHTML) + Math.abs(Bear[6] - document.getElementById('move/captr').innerHTML) + Math.abs(Bear[7] - document.getElementById('left/right').innerHTML + Math.abs(Bear[8] - rules[0]) + Math.abs(Bear[9] - rules[1]) + Math.abs(Bear[10] - rules[2]) + Math.abs(Bear[11] - rules[3]) + Math.abs(Bear[12] - rules[4]) + Math.abs(Bear[13] - rules[5]) + Math.abs(Bear[14] - rules[6]) + Math.abs(Bear[15] - rules[7]) + Math.abs(Bear[16] - rules[8]) + Math.abs(Bear[17] - rules[9]) + Math.abs(Bear[18] - rules[10]) + Math.abs(Bear[19] - rules[11]) + Math.abs(Bear[20] - rules[12]) + Math.abs(Bear[21] - rules[13]) + Math.abs(Bear[22] - rules[14]) + Math.abs(Bear[23] - rules[15]));
				Chancellor = Math.abs(Chancellor[0] - document.getElementById('strength').innerHTML) + Math.abs(Chancellor[1] - document.getElementById('rook').innerHTML) + Math.abs(Chancellor[2] - document.getElementById('bishop').innerHTML) + Math.abs(Chancellor[3] - document.getElementById('knight').innerHTML) + Math.abs(Chancellor[4] - document.getElementById('forwardness').innerHTML) + Math.abs(Chancellor[5] - document.getElementById('wideness').innerHTML) + Math.abs(Chancellor[6] - document.getElementById('move/captr').innerHTML) + Math.abs(Chancellor[7] - document.getElementById('left/right').innerHTML + Math.abs(Chancellor[8] - rules[0]) + Math.abs(Chancellor[9] - rules[1]) + Math.abs(Chancellor[10] - rules[2]) + Math.abs(Chancellor[11] - rules[3]) + Math.abs(Chancellor[12] - rules[4]) + Math.abs(Chancellor[13] - rules[5]) + Math.abs(Chancellor[14] - rules[6]) + Math.abs(Chancellor[15] - rules[7]) + Math.abs(Chancellor[16] - rules[8]) + Math.abs(Chancellor[17] - rules[9]) + Math.abs(Chancellor[18] - rules[10]) + Math.abs(Chancellor[19] - rules[11]) + Math.abs(Chancellor[20] - rules[12]) + Math.abs(Chancellor[21] - rules[13]) + Math.abs(Chancellor[22] - rules[14]) + Math.abs(Chancellor[23] - rules[15]));
				Dababba = Math.abs(Dababba[0] - document.getElementById('strength').innerHTML) + Math.abs(Dababba[1] - document.getElementById('rook').innerHTML) + Math.abs(Dababba[2] - document.getElementById('bishop').innerHTML) + Math.abs(Dababba[3] - document.getElementById('knight').innerHTML) + Math.abs(Dababba[4] - document.getElementById('forwardness').innerHTML) + Math.abs(Dababba[5] - document.getElementById('wideness').innerHTML) + Math.abs(Dababba[6] - document.getElementById('move/captr').innerHTML) + Math.abs(Dababba[7] - document.getElementById('left/right').innerHTML + Math.abs(Dababba[8] - rules[0]) + Math.abs(Dababba[9] - rules[1]) + Math.abs(Dababba[10] - rules[2]) + Math.abs(Dababba[11] - rules[3]) + Math.abs(Dababba[12] - rules[4]) + Math.abs(Dababba[13] - rules[5]) + Math.abs(Dababba[14] - rules[6]) + Math.abs(Dababba[15] - rules[7]) + Math.abs(Dababba[16] - rules[8]) + Math.abs(Dababba[17] - rules[9]) + Math.abs(Dababba[18] - rules[10]) + Math.abs(Dababba[19] - rules[11]) + Math.abs(Dababba[20] - rules[12]) + Math.abs(Dababba[21] - rules[13]) + Math.abs(Dababba[22] - rules[14]) + Math.abs(Dababba[23] - rules[15]));
				Dolphin = Math.abs(Dolphin[0] - document.getElementById('strength').innerHTML) + Math.abs(Dolphin[1] - document.getElementById('rook').innerHTML) + Math.abs(Dolphin[2] - document.getElementById('bishop').innerHTML) + Math.abs(Dolphin[3] - document.getElementById('knight').innerHTML) + Math.abs(Dolphin[4] - document.getElementById('forwardness').innerHTML) + Math.abs(Dolphin[5] - document.getElementById('wideness').innerHTML) + Math.abs(Dolphin[6] - document.getElementById('move/captr').innerHTML) + Math.abs(Dolphin[7] - document.getElementById('left/right').innerHTML + Math.abs(Dolphin[8] - rules[0]) + Math.abs(Dolphin[9] - rules[1]) + Math.abs(Dolphin[10] - rules[2]) + Math.abs(Dolphin[11] - rules[3]) + Math.abs(Dolphin[12] - rules[4]) + Math.abs(Dolphin[13] - rules[5]) + Math.abs(Dolphin[14] - rules[6]) + Math.abs(Dolphin[15] - rules[7]) + Math.abs(Dolphin[16] - rules[8]) + Math.abs(Dolphin[17] - rules[9]) + Math.abs(Dolphin[18] - rules[10]) + Math.abs(Dolphin[19] - rules[11]) + Math.abs(Dolphin[20] - rules[12]) + Math.abs(Dolphin[21] - rules[13]) + Math.abs(Dolphin[22] - rules[14]) + Math.abs(Dolphin[23] - rules[15]));
				Earth_Centaur = Math.abs(Earth_Centaur[0] - document.getElementById('strength').innerHTML) + Math.abs(Earth_Centaur[1] - document.getElementById('rook').innerHTML) + Math.abs(Earth_Centaur[2] - document.getElementById('bishop').innerHTML) + Math.abs(Earth_Centaur[3] - document.getElementById('knight').innerHTML) + Math.abs(Earth_Centaur[4] - document.getElementById('forwardness').innerHTML) + Math.abs(Earth_Centaur[5] - document.getElementById('wideness').innerHTML) + Math.abs(Earth_Centaur[6] - document.getElementById('move/captr').innerHTML) + Math.abs(Earth_Centaur[7] - document.getElementById('left/right').innerHTML + Math.abs(Earth_Centaur[8] - rules[0]) + Math.abs(Earth_Centaur[9] - rules[1]) + Math.abs(Earth_Centaur[10] - rules[2]) + Math.abs(Earth_Centaur[11] - rules[3]) + Math.abs(Earth_Centaur[12] - rules[4]) + Math.abs(Earth_Centaur[13] - rules[5]) + Math.abs(Earth_Centaur[14] - rules[6]) + Math.abs(Earth_Centaur[15] - rules[7]) + Math.abs(Earth_Centaur[16] - rules[8]) + Math.abs(Earth_Centaur[17] - rules[9]) + Math.abs(Earth_Centaur[18] - rules[10]) + Math.abs(Earth_Centaur[19] - rules[11]) + Math.abs(Earth_Centaur[20] - rules[12]) + Math.abs(Earth_Centaur[21] - rules[13]) + Math.abs(Earth_Centaur[22] - rules[14]) + Math.abs(Earth_Centaur[23] - rules[15]));
				Ferz = Math.abs(Ferz[0] - document.getElementById('strength').innerHTML) + Math.abs(Ferz[1] - document.getElementById('rook').innerHTML) + Math.abs(Ferz[2] - document.getElementById('bishop').innerHTML) + Math.abs(Ferz[3] - document.getElementById('knight').innerHTML) + Math.abs(Ferz[4] - document.getElementById('forwardness').innerHTML) + Math.abs(Ferz[5] - document.getElementById('wideness').innerHTML) + Math.abs(Ferz[6] - document.getElementById('move/captr').innerHTML) + Math.abs(Ferz[7] - document.getElementById('left/right').innerHTML + Math.abs(Ferz[8] - rules[0]) + Math.abs(Ferz[9] - rules[1]) + Math.abs(Ferz[10] - rules[2]) + Math.abs(Ferz[11] - rules[3]) + Math.abs(Ferz[12] - rules[4]) + Math.abs(Ferz[13] - rules[5]) + Math.abs(Ferz[14] - rules[6]) + Math.abs(Ferz[15] - rules[7]) + Math.abs(Ferz[16] - rules[8]) + Math.abs(Ferz[17] - rules[9]) + Math.abs(Ferz[18] - rules[10]) + Math.abs(Ferz[19] - rules[11]) + Math.abs(Ferz[20] - rules[12]) + Math.abs(Ferz[21] - rules[13]) + Math.abs(Ferz[22] - rules[14]) + Math.abs(Ferz[23] - rules[15]));
				Fire_Centaur = Math.abs(Fire_Centaur[0] - document.getElementById('strength').innerHTML) + Math.abs(Fire_Centaur[1] - document.getElementById('rook').innerHTML) + Math.abs(Fire_Centaur[2] - document.getElementById('bishop').innerHTML) + Math.abs(Fire_Centaur[3] - document.getElementById('knight').innerHTML) + Math.abs(Fire_Centaur[4] - document.getElementById('forwardness').innerHTML) + Math.abs(Fire_Centaur[5] - document.getElementById('wideness').innerHTML) + Math.abs(Fire_Centaur[6] - document.getElementById('move/captr').innerHTML) + Math.abs(Fire_Centaur[7] - document.getElementById('left/right').innerHTML + Math.abs(Fire_Centaur[8] - rules[0]) + Math.abs(Fire_Centaur[9] - rules[1]) + Math.abs(Fire_Centaur[10] - rules[2]) + Math.abs(Fire_Centaur[11] - rules[3]) + Math.abs(Fire_Centaur[12] - rules[4]) + Math.abs(Fire_Centaur[13] - rules[5]) + Math.abs(Fire_Centaur[14] - rules[6]) + Math.abs(Fire_Centaur[15] - rules[7]) + Math.abs(Fire_Centaur[16] - rules[8]) + Math.abs(Fire_Centaur[17] - rules[9]) + Math.abs(Fire_Centaur[18] - rules[10]) + Math.abs(Fire_Centaur[19] - rules[11]) + Math.abs(Fire_Centaur[20] - rules[12]) + Math.abs(Fire_Centaur[21] - rules[13]) + Math.abs(Fire_Centaur[22] - rules[14]) + Math.abs(Fire_Centaur[23] - rules[15]));
				Horizontal_Mover = Math.abs(Horizontal_Mover[0] - document.getElementById('strength').innerHTML) + Math.abs(Horizontal_Mover[1] - document.getElementById('rook').innerHTML) + Math.abs(Horizontal_Mover[2] - document.getElementById('bishop').innerHTML) + Math.abs(Horizontal_Mover[3] - document.getElementById('knight').innerHTML) + Math.abs(Horizontal_Mover[4] - document.getElementById('forwardness').innerHTML) + Math.abs(Horizontal_Mover[5] - document.getElementById('wideness').innerHTML) + Math.abs(Horizontal_Mover[6] - document.getElementById('move/captr').innerHTML) + Math.abs(Horizontal_Mover[7] - document.getElementById('left/right').innerHTML + Math.abs(Horizontal_Mover[8] - rules[0]) + Math.abs(Horizontal_Mover[9] - rules[1]) + Math.abs(Horizontal_Mover[10] - rules[2]) + Math.abs(Horizontal_Mover[11] - rules[3]) + Math.abs(Horizontal_Mover[12] - rules[4]) + Math.abs(Horizontal_Mover[13] - rules[5]) + Math.abs(Horizontal_Mover[14] - rules[6]) + Math.abs(Horizontal_Mover[15] - rules[7]) + Math.abs(Horizontal_Mover[16] - rules[8]) + Math.abs(Horizontal_Mover[17] - rules[9]) + Math.abs(Horizontal_Mover[18] - rules[10]) + Math.abs(Horizontal_Mover[19] - rules[11]) + Math.abs(Horizontal_Mover[20] - rules[12]) + Math.abs(Horizontal_Mover[21] - rules[13]) + Math.abs(Horizontal_Mover[22] - rules[14]) + Math.abs(Horizontal_Mover[23] - rules[15]));
				Kirin = Math.abs(Kirin[0] - document.getElementById('strength').innerHTML) + Math.abs(Kirin[1] - document.getElementById('rook').innerHTML) + Math.abs(Kirin[2] - document.getElementById('bishop').innerHTML) + Math.abs(Kirin[3] - document.getElementById('knight').innerHTML) + Math.abs(Kirin[4] - document.getElementById('forwardness').innerHTML) + Math.abs(Kirin[5] - document.getElementById('wideness').innerHTML) + Math.abs(Kirin[6] - document.getElementById('move/captr').innerHTML) + Math.abs(Kirin[7] - document.getElementById('left/right').innerHTML + Math.abs(Kirin[8] - rules[0]) + Math.abs(Kirin[9] - rules[1]) + Math.abs(Kirin[10] - rules[2]) + Math.abs(Kirin[11] - rules[3]) + Math.abs(Kirin[12] - rules[4]) + Math.abs(Kirin[13] - rules[5]) + Math.abs(Kirin[14] - rules[6]) + Math.abs(Kirin[15] - rules[7]) + Math.abs(Kirin[16] - rules[8]) + Math.abs(Kirin[17] - rules[9]) + Math.abs(Kirin[18] - rules[10]) + Math.abs(Kirin[19] - rules[11]) + Math.abs(Kirin[20] - rules[12]) + Math.abs(Kirin[21] - rules[13]) + Math.abs(Kirin[22] - rules[14]) + Math.abs(Kirin[23] - rules[15]));
				Lance = Math.abs(Lance[0] - document.getElementById('strength').innerHTML) + Math.abs(Lance[1] - document.getElementById('rook').innerHTML) + Math.abs(Lance[2] - document.getElementById('bishop').innerHTML) + Math.abs(Lance[3] - document.getElementById('knight').innerHTML) + Math.abs(Lance[4] - document.getElementById('forwardness').innerHTML) + Math.abs(Lance[5] - document.getElementById('wideness').innerHTML) + Math.abs(Lance[6] - document.getElementById('move/captr').innerHTML) + Math.abs(Lance[7] - document.getElementById('left/right').innerHTML + Math.abs(Lance[8] - rules[0]) + Math.abs(Lance[9] - rules[1]) + Math.abs(Lance[10] - rules[2]) + Math.abs(Lance[11] - rules[3]) + Math.abs(Lance[12] - rules[4]) + Math.abs(Lance[13] - rules[5]) + Math.abs(Lance[14] - rules[6]) + Math.abs(Lance[15] - rules[7]) + Math.abs(Lance[16] - rules[8]) + Math.abs(Lance[17] - rules[9]) + Math.abs(Lance[18] - rules[10]) + Math.abs(Lance[19] - rules[11]) + Math.abs(Lance[20] - rules[12]) + Math.abs(Lance[21] - rules[13]) + Math.abs(Lance[22] - rules[14]) + Math.abs(Lance[23] - rules[15]));
				Man = Math.abs(Man[0] - document.getElementById('strength').innerHTML) + Math.abs(Man[1] - document.getElementById('rook').innerHTML) + Math.abs(Man[2] - document.getElementById('bishop').innerHTML) + Math.abs(Man[3] - document.getElementById('knight').innerHTML) + Math.abs(Man[4] - document.getElementById('forwardness').innerHTML) + Math.abs(Man[5] - document.getElementById('wideness').innerHTML) + Math.abs(Man[6] - document.getElementById('move/captr').innerHTML) + Math.abs(Man[7] - document.getElementById('left/right').innerHTML + Math.abs(Man[8] - rules[0]) + Math.abs(Man[9] - rules[1]) + Math.abs(Man[10] - rules[2]) + Math.abs(Man[11] - rules[3]) + Math.abs(Man[12] - rules[4]) + Math.abs(Man[13] - rules[5]) + Math.abs(Man[14] - rules[6]) + Math.abs(Man[15] - rules[7]) + Math.abs(Man[16] - rules[8]) + Math.abs(Man[17] - rules[9]) + Math.abs(Man[18] - rules[10]) + Math.abs(Man[19] - rules[11]) + Math.abs(Man[20] - rules[12]) + Math.abs(Man[21] - rules[13]) + Math.abs(Man[22] - rules[14]) + Math.abs(Man[23] - rules[15]));
				Overpreparer = Math.abs(Overpreparer[0] - document.getElementById('strength').innerHTML) + Math.abs(Overpreparer[1] - document.getElementById('rook').innerHTML) + Math.abs(Overpreparer[2] - document.getElementById('bishop').innerHTML) + Math.abs(Overpreparer[3] - document.getElementById('knight').innerHTML) + Math.abs(Overpreparer[4] - document.getElementById('forwardness').innerHTML) + Math.abs(Overpreparer[5] - document.getElementById('wideness').innerHTML) + Math.abs(Overpreparer[6] - document.getElementById('move/captr').innerHTML) + Math.abs(Overpreparer[7] - document.getElementById('left/right').innerHTML + Math.abs(Overpreparer[8] - rules[0]) + Math.abs(Overpreparer[9] - rules[1]) + Math.abs(Overpreparer[10] - rules[2]) + Math.abs(Overpreparer[11] - rules[3]) + Math.abs(Overpreparer[12] - rules[4]) + Math.abs(Overpreparer[13] - rules[5]) + Math.abs(Overpreparer[14] - rules[6]) + Math.abs(Overpreparer[15] - rules[7]) + Math.abs(Overpreparer[16] - rules[8]) + Math.abs(Overpreparer[17] - rules[9]) + Math.abs(Overpreparer[18] - rules[10]) + Math.abs(Overpreparer[19] - rules[11]) + Math.abs(Overpreparer[20] - rules[12]) + Math.abs(Overpreparer[21] - rules[13]) + Math.abs(Overpreparer[22] - rules[14]) + Math.abs(Overpreparer[23] - rules[15]));
				Paladin = Math.abs(Paladin[0] - document.getElementById('strength').innerHTML) + Math.abs(Paladin[1] - document.getElementById('rook').innerHTML) + Math.abs(Paladin[2] - document.getElementById('bishop').innerHTML) + Math.abs(Paladin[3] - document.getElementById('knight').innerHTML) + Math.abs(Paladin[4] - document.getElementById('forwardness').innerHTML) + Math.abs(Paladin[5] - document.getElementById('wideness').innerHTML) + Math.abs(Paladin[6] - document.getElementById('move/captr').innerHTML) + Math.abs(Paladin[7] - document.getElementById('left/right').innerHTML + Math.abs(Paladin[8] - rules[0]) + Math.abs(Paladin[9] - rules[1]) + Math.abs(Paladin[10] - rules[2]) + Math.abs(Paladin[11] - rules[3]) + Math.abs(Paladin[12] - rules[4]) + Math.abs(Paladin[13] - rules[5]) + Math.abs(Paladin[14] - rules[6]) + Math.abs(Paladin[15] - rules[7]) + Math.abs(Paladin[16] - rules[8]) + Math.abs(Paladin[17] - rules[9]) + Math.abs(Paladin[18] - rules[10]) + Math.abs(Paladin[19] - rules[11]) + Math.abs(Paladin[20] - rules[12]) + Math.abs(Paladin[21] - rules[13]) + Math.abs(Paladin[22] - rules[14]) + Math.abs(Paladin[23] - rules[15]));
				Phoenix = Math.abs(Phoenix[0] - document.getElementById('strength').innerHTML) + Math.abs(Phoenix[1] - document.getElementById('rook').innerHTML) + Math.abs(Phoenix[2] - document.getElementById('bishop').innerHTML) + Math.abs(Phoenix[3] - document.getElementById('knight').innerHTML) + Math.abs(Phoenix[4] - document.getElementById('forwardness').innerHTML) + Math.abs(Phoenix[5] - document.getElementById('wideness').innerHTML) + Math.abs(Phoenix[6] - document.getElementById('move/captr').innerHTML) + Math.abs(Phoenix[7] - document.getElementById('left/right').innerHTML + Math.abs(Phoenix[8] - rules[0]) + Math.abs(Phoenix[9] - rules[1]) + Math.abs(Phoenix[10] - rules[2]) + Math.abs(Phoenix[11] - rules[3]) + Math.abs(Phoenix[12] - rules[4]) + Math.abs(Phoenix[13] - rules[5]) + Math.abs(Phoenix[14] - rules[6]) + Math.abs(Phoenix[15] - rules[7]) + Math.abs(Phoenix[16] - rules[8]) + Math.abs(Phoenix[17] - rules[9]) + Math.abs(Phoenix[18] - rules[10]) + Math.abs(Phoenix[19] - rules[11]) + Math.abs(Phoenix[20] - rules[12]) + Math.abs(Phoenix[21] - rules[13]) + Math.abs(Phoenix[22] - rules[14]) + Math.abs(Phoenix[23] - rules[15]));
				Prince = Math.abs(Prince[0] - document.getElementById('strength').innerHTML) + Math.abs(Prince[1] - document.getElementById('rook').innerHTML) + Math.abs(Prince[2] - document.getElementById('bishop').innerHTML) + Math.abs(Prince[3] - document.getElementById('knight').innerHTML) + Math.abs(Prince[4] - document.getElementById('forwardness').innerHTML) + Math.abs(Prince[5] - document.getElementById('wideness').innerHTML) + Math.abs(Prince[6] - document.getElementById('move/captr').innerHTML) + Math.abs(Prince[7] - document.getElementById('left/right').innerHTML + Math.abs(Prince[8] - rules[0]) + Math.abs(Prince[9] - rules[1]) + Math.abs(Prince[10] - rules[2]) + Math.abs(Prince[11] - rules[3]) + Math.abs(Prince[12] - rules[4]) + Math.abs(Prince[13] - rules[5]) + Math.abs(Prince[14] - rules[6]) + Math.abs(Prince[15] - rules[7]) + Math.abs(Prince[16] - rules[8]) + Math.abs(Prince[17] - rules[9]) + Math.abs(Prince[18] - rules[10]) + Math.abs(Prince[19] - rules[11]) + Math.abs(Prince[20] - rules[12]) + Math.abs(Prince[21] - rules[13]) + Math.abs(Prince[22] - rules[14]) + Math.abs(Prince[23] - rules[15]));
				Silver_King = Math.abs(Silver_King[0] - document.getElementById('strength').innerHTML) + Math.abs(Silver_King[1] - document.getElementById('rook').innerHTML) + Math.abs(Silver_King[2] - document.getElementById('bishop').innerHTML) + Math.abs(Silver_King[3] - document.getElementById('knight').innerHTML) + Math.abs(Silver_King[4] - document.getElementById('forwardness').innerHTML) + Math.abs(Silver_King[5] - document.getElementById('wideness').innerHTML) + Math.abs(Silver_King[6] - document.getElementById('move/captr').innerHTML) + Math.abs(Silver_King[7] - document.getElementById('left/right').innerHTML + Math.abs(Silver_King[8] - rules[0]) + Math.abs(Silver_King[9] - rules[1]) + Math.abs(Silver_King[10] - rules[2]) + Math.abs(Silver_King[11] - rules[3]) + Math.abs(Silver_King[12] - rules[4]) + Math.abs(Silver_King[13] - rules[5]) + Math.abs(Silver_King[14] - rules[6]) + Math.abs(Silver_King[15] - rules[7]) + Math.abs(Silver_King[16] - rules[8]) + Math.abs(Silver_King[17] - rules[9]) + Math.abs(Silver_King[18] - rules[10]) + Math.abs(Silver_King[19] - rules[11]) + Math.abs(Silver_King[20] - rules[12]) + Math.abs(Silver_King[21] - rules[13]) + Math.abs(Silver_King[22] - rules[14]) + Math.abs(Silver_King[23] - rules[15]));
				Spearman = Math.abs(Spearman[0] - document.getElementById('strength').innerHTML) + Math.abs(Spearman[1] - document.getElementById('rook').innerHTML) + Math.abs(Spearman[2] - document.getElementById('bishop').innerHTML) + Math.abs(Spearman[3] - document.getElementById('knight').innerHTML) + Math.abs(Spearman[4] - document.getElementById('forwardness').innerHTML) + Math.abs(Spearman[5] - document.getElementById('wideness').innerHTML) + Math.abs(Spearman[6] - document.getElementById('move/captr').innerHTML) + Math.abs(Spearman[7] - document.getElementById('left/right').innerHTML + Math.abs(Spearman[8] - rules[0]) + Math.abs(Spearman[9] - rules[1]) + Math.abs(Spearman[10] - rules[2]) + Math.abs(Spearman[11] - rules[3]) + Math.abs(Spearman[12] - rules[4]) + Math.abs(Spearman[13] - rules[5]) + Math.abs(Spearman[14] - rules[6]) + Math.abs(Spearman[15] - rules[7]) + Math.abs(Spearman[16] - rules[8]) + Math.abs(Spearman[17] - rules[9]) + Math.abs(Spearman[18] - rules[10]) + Math.abs(Spearman[19] - rules[11]) + Math.abs(Spearman[20] - rules[12]) + Math.abs(Spearman[21] - rules[13]) + Math.abs(Spearman[22] - rules[14]) + Math.abs(Spearman[23] - rules[15]));
				Spider = Math.abs(Spider[0] - document.getElementById('strength').innerHTML) + Math.abs(Spider[1] - document.getElementById('rook').innerHTML) + Math.abs(Spider[2] - document.getElementById('bishop').innerHTML) + Math.abs(Spider[3] - document.getElementById('knight').innerHTML) + Math.abs(Spider[4] - document.getElementById('forwardness').innerHTML) + Math.abs(Spider[5] - document.getElementById('wideness').innerHTML) + Math.abs(Spider[6] - document.getElementById('move/captr').innerHTML) + Math.abs(Spider[7] - document.getElementById('left/right').innerHTML + Math.abs(Spider[8] - rules[0]) + Math.abs(Spider[9] - rules[1]) + Math.abs(Spider[10] - rules[2]) + Math.abs(Spider[11] - rules[3]) + Math.abs(Spider[12] - rules[4]) + Math.abs(Spider[13] - rules[5]) + Math.abs(Spider[14] - rules[6]) + Math.abs(Spider[15] - rules[7]) + Math.abs(Spider[16] - rules[8]) + Math.abs(Spider[17] - rules[9]) + Math.abs(Spider[18] - rules[10]) + Math.abs(Spider[19] - rules[11]) + Math.abs(Spider[20] - rules[12]) + Math.abs(Spider[21] - rules[13]) + Math.abs(Spider[22] - rules[14]) + Math.abs(Spider[23] - rules[15]));
				Wasir = Math.abs(Wasir[0] - document.getElementById('strength').innerHTML) + Math.abs(Wasir[1] - document.getElementById('rook').innerHTML) + Math.abs(Wasir[2] - document.getElementById('bishop').innerHTML) + Math.abs(Wasir[3] - document.getElementById('knight').innerHTML) + Math.abs(Wasir[4] - document.getElementById('forwardness').innerHTML) + Math.abs(Wasir[5] - document.getElementById('wideness').innerHTML) + Math.abs(Wasir[6] - document.getElementById('move/captr').innerHTML) + Math.abs(Wasir[7] - document.getElementById('left/right').innerHTML + Math.abs(Wasir[8] - rules[0]) + Math.abs(Wasir[9] - rules[1]) + Math.abs(Wasir[10] - rules[2]) + Math.abs(Wasir[11] - rules[3]) + Math.abs(Wasir[12] - rules[4]) + Math.abs(Wasir[13] - rules[5]) + Math.abs(Wasir[14] - rules[6]) + Math.abs(Wasir[15] - rules[7]) + Math.abs(Wasir[16] - rules[8]) + Math.abs(Wasir[17] - rules[9]) + Math.abs(Wasir[18] - rules[10]) + Math.abs(Wasir[19] - rules[11]) + Math.abs(Wasir[20] - rules[12]) + Math.abs(Wasir[21] - rules[13]) + Math.abs(Wasir[22] - rules[14]) + Math.abs(Wasir[23] - rules[15]));
				Vertical_Mover = Math.abs(Vertical_Mover[0] - document.getElementById('strength').innerHTML) + Math.abs(Vertical_Mover[1] - document.getElementById('rook').innerHTML) + Math.abs(Vertical_Mover[2] - document.getElementById('bishop').innerHTML) + Math.abs(Vertical_Mover[3] - document.getElementById('knight').innerHTML) + Math.abs(Vertical_Mover[4] - document.getElementById('forwardness').innerHTML) + Math.abs(Vertical_Mover[5] - document.getElementById('wideness').innerHTML) + Math.abs(Vertical_Mover[6] - document.getElementById('move/captr').innerHTML) + Math.abs(Vertical_Mover[7] - document.getElementById('left/right').innerHTML + Math.abs(Vertical_Mover[8] - rules[0]) + Math.abs(Vertical_Mover[9] - rules[1]) + Math.abs(Vertical_Mover[10] - rules[2]) + Math.abs(Vertical_Mover[11] - rules[3]) + Math.abs(Vertical_Mover[12] - rules[4]) + Math.abs(Vertical_Mover[13] - rules[5]) + Math.abs(Vertical_Mover[14] - rules[6]) + Math.abs(Vertical_Mover[15] - rules[7]) + Math.abs(Vertical_Mover[16] - rules[8]) + Math.abs(Vertical_Mover[17] - rules[9]) + Math.abs(Vertical_Mover[18] - rules[10]) + Math.abs(Vertical_Mover[19] - rules[11]) + Math.abs(Vertical_Mover[20] - rules[12]) + Math.abs(Vertical_Mover[21] - rules[13]) + Math.abs(Vertical_Mover[22] - rules[14]) + Math.abs(Vertical_Mover[23] - rules[15]));
				Vortex = Math.abs(Vortex[0] - document.getElementById('strength').innerHTML) + Math.abs(Vortex[1] - document.getElementById('rook').innerHTML) + Math.abs(Vortex[2] - document.getElementById('bishop').innerHTML) + Math.abs(Vortex[3] - document.getElementById('knight').innerHTML) + Math.abs(Vortex[4] - document.getElementById('forwardness').innerHTML) + Math.abs(Vortex[5] - document.getElementById('wideness').innerHTML) + Math.abs(Vortex[6] - document.getElementById('move/captr').innerHTML) + Math.abs(Vortex[7] - document.getElementById('left/right').innerHTML + Math.abs(Vortex[8] - rules[0]) + Math.abs(Vortex[9] - rules[1]) + Math.abs(Vortex[10] - rules[2]) + Math.abs(Vortex[11] - rules[3]) + Math.abs(Vortex[12] - rules[4]) + Math.abs(Vortex[13] - rules[5]) + Math.abs(Vortex[14] - rules[6]) + Math.abs(Vortex[15] - rules[7]) + Math.abs(Vortex[16] - rules[8]) + Math.abs(Vortex[17] - rules[9]) + Math.abs(Vortex[18] - rules[10]) + Math.abs(Vortex[19] - rules[11]) + Math.abs(Vortex[20] - rules[12]) + Math.abs(Vortex[21] - rules[13]) + Math.abs(Vortex[22] - rules[14]) + Math.abs(Vortex[23] - rules[15]));
				Xeawn = Math.abs(Xeawn[0] - document.getElementById('strength').innerHTML) + Math.abs(Xeawn[1] - document.getElementById('rook').innerHTML) + Math.abs(Xeawn[2] - document.getElementById('bishop').innerHTML) + Math.abs(Xeawn[3] - document.getElementById('knight').innerHTML) + Math.abs(Xeawn[4] - document.getElementById('forwardness').innerHTML) + Math.abs(Xeawn[5] - document.getElementById('wideness').innerHTML) + Math.abs(Xeawn[6] - document.getElementById('move/captr').innerHTML) + Math.abs(Xeawn[7] - document.getElementById('left/right').innerHTML + Math.abs(Xeawn[8] - rules[0]) + Math.abs(Xeawn[9] - rules[1]) + Math.abs(Xeawn[10] - rules[2]) + Math.abs(Xeawn[11] - rules[3]) + Math.abs(Xeawn[12] - rules[4]) + Math.abs(Xeawn[13] - rules[5]) + Math.abs(Xeawn[14] - rules[6]) + Math.abs(Xeawn[15] - rules[7]) + Math.abs(Xeawn[16] - rules[8]) + Math.abs(Xeawn[17] - rules[9]) + Math.abs(Xeawn[18] - rules[10]) + Math.abs(Xeawn[19] - rules[11]) + Math.abs(Xeawn[20] - rules[12]) + Math.abs(Xeawn[21] - rules[13]) + Math.abs(Xeawn[22] - rules[14]) + Math.abs(Xeawn[23] - rules[15]));
				var array = [Alfil + "_Alfil_JIT", Alibaba + "_Alibaba_4SU", Archbishop + "_Archbishop_1I1", Armed_Treasury + "_Armed Treasury_N8R", Axeman + "_Axeman_EWN", Bandmaster + "_Bandmaster_43P", Bear + "_Bear_43V", Chancellor + "_Chancellor_1I0", Dababba + "_Dababba_JJ0", Dolphin + "_Dolphin_GGD", Earth_Centaur + "_Earth Centaur_4SY", Ferz + "_Ferz_4TB", Fire_Centaur + "_Fire Centaur_4SW", Horizontal_Mover + "_Horizontal Mover_EZE", Kirin + "_Kirin/Jewels_4T5", Lance + "_Lance_EYK", Man + "_Man_71J", Overpreparer + "_Overpreparer_225", Paladin + "_Paladin_227", Phoenix + "_Phoenix/Incense_4T4", Prince + "_Prince_443", Silver_King + "_Silver King_N8S", Spearman + "_Spearman_229", Spider + "_Spider_EWK", Wasir + "_Wasir_4TD", Vertical_Mover + "_Vertical Mover_EZK", Vortex + "_Vortex_MRZ", Xeawn + "_Xeawn_GF6"];
				var collator = new Intl.Collator([], {numeric: true});
				array.sort((a, b) => collator.compare(a, b));
				var piece1 = array[0].split("_");
				var piece2 = array[1].split("_");
				var piece3 = array[2].split("_");
				var piece4 = array[3].split("_");
				var piece5 = array[4].split("_");
				document.getElementById('piece1').innerHTML = piece1[1] + ' <a style="color: #ffe8d1" href="https://chesscraft.ca/design?id=' + piece1[2] + '" target="_blank">' + piece1[2] + '</a>'
				document.getElementById('piece2').innerHTML = piece2[1] + ' <a style="color: #ffe8d1" href="https://chesscraft.ca/design?id=' + piece2[2] + '" target="_blank">' + piece2[2] + '</a>'
				document.getElementById('piece3').innerHTML = piece3[1] + ' <a style="color: #ffe8d1" href="https://chesscraft.ca/design?id=' + piece3[2] + '" target="_blank">' + piece3[2] + '</a>'
				document.getElementById('piece4').innerHTML = piece4[1] + ' <a style="color: #ffe8d1" href="https://chesscraft.ca/design?id=' + piece4[2] + '" target="_blank">' + piece4[2] + '</a>'
				document.getElementById('piece5').innerHTML = piece5[1] + ' <a style="color: #ffe8d1" href="https://chesscraft.ca/design?id=' + piece5[2] + '" target="_blank">' + piece5[2] + '</a>'
			}
			setInterval(function() {
				outwidth = window.innerWidth;
				var btnloop = document.getElementsByClassName('ibtn');
				var i;
				for (i = 0; i<btnloop.length; i++) {
    				btnloop[i].style.height = outwidth / 8;
				}
				document.getElementById('botrow').style.marginTop = outwidth / 8 - outwidth / 4
			}, 1);
		</script>
	</body>
</html>