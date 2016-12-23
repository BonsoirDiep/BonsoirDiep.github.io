---
layout: post
title: Trình điều khiển STM32F407
---

Phím điều khiển đơn giản:<br><br>
<script language="javascript" type="text/javascript">
  var wsUri = "wss://gepa14.herokuapp.com";
  function myAction(message){
      websocket = new WebSocket(wsUri);
      websocket.onopen = function(evt) { onOpen(evt) };
      websocket.onmessage = function(evt) { onMessage(evt) };
      /**/
      function onOpen(evt){
          websocket.send(message);
      }
      function onMessage(evt){
          console.log(evt.data);
          document.getElementById("output").innerHTML = evt.data;
          websocket.close();
      }
  }
</script>
<button class="btn btn-warning" onclick="myAction('orange')">Cam</button><br>
<button class="btn btn-success" onclick="myAction('green')">Xanh</button>
<button class="btn btn-danger" onclick="myAction('red')">Đỏ</button><br>
<button class="btn btn-info" onclick="myAction('blue')">Lục</button>
<br><div id="output">null</div>
