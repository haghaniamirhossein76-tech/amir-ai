# amir-ai<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Amir AI</title>
<style>
body {
  margin: 0;
  font-family: Tahoma, Arial, sans-serif;
  background: #100b20;
  color: white;
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
}
.box {
  width: 90%;
  max-width: 500px;
  background: #211638;
  border: 1px solid #7652a8;
  border-radius: 20px;
  padding: 20px;
  box-sizing: border-box;
}
h1 { color: #d5aaff; text-align: center; }
#messages {
  height: 300px;
  overflow-y: auto;
  background: #140e24;
  border-radius: 12px;
  padding: 12px;
  margin: 15px 0;
}
.msg { margin: 10px 0; line-height: 1.8; }
input {
  width: 100%;
  padding: 13px;
  box-sizing: border-box;
  border-radius: 10px;
  border: 1px solid #7652a8;
  background: #140e24;
  color: white;
  font-size: 16px;
}
button {
  width: 100%;
  padding: 13px;
  margin-top: 10px;
  border: 0;
  border-radius: 10px;
  background: #a56bdf;
  color: white;
  font-size: 16px;
}
.note { color: #c9b9df; font-size: 12px; text-align: center; }
</style>
</head>
<body>
<div class="box">
  <h1>💜 Amir AI</h1>
  <p style="text-align:center">دستیار هوشمند تو</p>
  <div id="messages">
    <div class="msg">🤖 سلام! من Amir AI هستم. برای شروع، پیامت رو بنویس.</div>
  </div>
  <input id="question" placeholder="پیامت رو بنویس..." />
  <button onclick="sendMessage()">ارسال پیام</button>
  <p class="note">نسخه اولیه چت — اتصال هوش مصنوعی هنوز راه‌اندازی نشده است.</p>
</div>
<script>
function sendMessage() {
  const input = document.getElementById('question');
  const text = input.value.trim();
  if (!text) return;
  const messages = document.getElementById('messages');
  const user = document.createElement('div');
  user.className = 'msg';
  user.textContent = '👤 تو: ' + text;
  messages.appendChild(user);
  const reply = document.createElement('div');
  reply.className = 'msg';
  reply.textContent = '🤖 Amir AI: ظاهر چت آماده است؛ برای پاسخ هوشمند باید موتور هوش مصنوعی را هم متصل کنیم.';
  messages.appendChild(reply);
  input.value = '';
  messages.scrollTop = messages.scrollHeight;
}
</script>
</body>
</html>