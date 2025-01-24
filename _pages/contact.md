---
title: "Kontak"
permalink: "/contact"
search: exclude
layout: page-about
comments: false
image: assets/img/about.avif
---

<form id="kontak" action="https://formspree.io/{{site.formspree}}" method="POST">    
<p class="mb-4">Silakan lengkapi form berikut untuk menghubungi kami.</p>
<div class="form-group row">
<div class="col-md-6">
<input class="form-control" type="text" name="name" placeholder="Nama *" required>
</div>
<div class="col-md-6">
<input class="form-control" type="email" name="email" placeholder="Alamat E-mail*" required>
</div>
</div>
<textarea rows="8" class="form-control mb-3" name="message" placeholder="Isi Pesan/pertanyaan*" required></textarea>    
<input class="btn btn-success" type="submit" value="Kirim">
</form>
<p id="kontak-status"></p>

<script>
  var form = document.getElementById("kontak");
  
  async function handleSubmit(event) {
    event.preventDefault();
    var status = document.getElementById("kontak-status");
    var ngumpet = document.getElementById("kontak");
    var data = new FormData(event.target);
    fetch(event.target.action, {
      method: form.method,
      body: data,
      headers: {
          'Accept': 'application/json'
      }
    }).then(response => {
      if (response.ok) {
        status.innerHTML = "<b>Terima kasih atas kiriman anda!</b><br>Kami akan memeriksanya dan mengirimkan tanggapan sesegera mungkin jika dibutuhkan.<br><br>Kembali ke <a href='/'>halaman depan</a>.";
        kontak.setAttribute('style', 'display:none !important');
        form.reset()
      } else {
        response.json().then(data => {
          if (Object.hasOwn(data, 'errors')) {
            status.innerHTML = data["errors"].map(error => error["message"]).join(", ")
          } else {
            status.innerHTML = "Ups! Ada masalah saat mengirim form.<br><br>Coba <a href='/contact'>ulangi lagi dengan isian yang lengkap dan benar</a>."
          }
        })
      }
    }).catch(error => {
      status.innerHTML = "Ups! Ada masalah saat mengirim form.<br><br>Coba <a href='/contact'>ulangi lagi dengan isian yang lengkap dan benar</a>."
    });
  }
  form.addEventListener("submit", handleSubmit)
</script>