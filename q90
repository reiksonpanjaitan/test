let minutes = 90;
let seconds = 0;
let countdown = setInterval(function() {
  if (seconds > 0) {
    seconds--;
  } else if (seconds == 0 && minutes > 0) {
    minutes--;
    seconds = 59;
  }
  let timerElem = document.getElementById("timer90");
  timerElem.innerHTML = `${minutes} menit ${seconds} detik`;
  if (minutes == 0 && seconds == 0) {
    clearInterval(countdown);
    checkAnswers90();
  }
}, 1000);

function checkAnswers90() {
  clearInterval(countdown);
  let score = 0;
  const answers = document.querySelectorAll(".question input:checked");
  answers.forEach(function(answer) {
    if (answer.value === "correct") {
      score++;
      answer.parentNode.style.color = "blue";
    } else {
      answer.parentNode.style.color = "red";
    }
  });
  var nama=document.getElementById("namasiswa").value;
  var tanggallengkap = new String();
  var namahari = ("Minggu Senin Selasa Rabu Kamis Jumat Sabtu"); namahari = namahari.split(" ");
  var namabulan = ("Januari Februari Maret April Mei Juni Juli Agustus September Oktober November Desember"); namabulan = namabulan.split(" ");
  var tgl = new Date();
  var hari = tgl.getDay();
  var tanggal = tgl.getDate();
  var bulan = tgl.getMonth();
  var tahun = tgl.getFullYear();
  tanggallengkap = namahari[hari] + ", " +tanggal + " " + namabulan[bulan] + " " + tahun;
  var waktu = new Date();
  waktulengkap = waktu.getHours().toString().padStart(2, '0')+":"+waktu.getMinutes().toString().padStart(2, '0')+":"+waktu.getSeconds().toString().padStart(2, '0');
  
  document.getElementById("submit-btn").disabled = true;
  result.style="color:black; background:-webkit-linear-gradient(45deg, #cffc05, #5EEE66); textAlign:left; fontSize:40px; border-radius:10px; -moz-border-radius:10px; -webkit-border-radius:10px; border: 5px solid #000000; padding: 5px; max-width:100%;";
  document.getElementById("result").innerHTML = 
  "<center><table>"+
  "<tr><td>Nama Peserta</td><td>:</td><td>"+nama+"</td></tr>"+
  "<tr><td>Tanggal Ujian</td><td>:</td><td>"+tanggallengkap+"</td></tr>"+
  "<tr><td>Hasil Ujian</td><td>:</td><td>"+score+" soal benar</td></tr>"+
  "<tr><td>Selesai Pukul</td><td>:</td><td>"+waktulengkap+"</td></tr>"+
  "<tr><td>Sisa Waktu</td><td>:</td><td>"+minutes+" menit</td></tr>"+
  "</table>"+"<input type='button' value='COBA LAGI' onClick='document.location.reload(true)'>"+"<hr>"+
  "Terima kasih, telah berlatih di website <b>ayoberlatih.com</b><br><img alt='Ayo Berlatih' height='50' width='50' src='https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgBXCv7G30VrFft5iABUI4mxXF07A-ZMC-Tx17y5lXNcSypfWvlVkPtwyi5iZN_K38uVQQNTyhpVUqWuuQm84MBjAHKCF4_bj8Q55L6c1kTcku49sYqJ502jD1qv05Q4exsgnmLIrFpEOcZeWDEiLQJj2s9fEgA4P9365Wgtpyk126XY2hilRL8hXBl/s1600/Logo%20Ayo%20Berlatih.png'/><br>Follow Us on:<br><button><a href='https://www.youtube.com/ayoberlatih?sub_confirmation=1'>Youtube</a></button> - <button><a href='https://www.facebook.com/ayoberlatih'>Facebook</a></button></center>";
  
}
