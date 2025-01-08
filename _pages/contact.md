---
title: "Kontak"
permalink: "/contact.html"
---

<form id="kontak" action="https://formspree.io/{{site.formspree}}" method="POST">    
<p class="mb-4">Silakan lengkapi form berikut untuk menghubungi kami.</p>
<div class="form-group row">
<div class="col-md-6">
<input class="form-control" type="text" name="name" placeholder="Nama *" required>
</div>
<div class="col-md-6">
<input class="form-control" type="email" name="_replyto" placeholder="Alamat E-mail*" required>
</div>
</div>
<textarea rows="8" class="form-control mb-3" name="message" placeholder="Isi Pesan/pertanyaan*" required></textarea>    
<input class="btn btn-success" type="submit" value="Kirim">
<p id="my-form-status"></p>
</form>

<script>
  var form = document.getElementById("kontak");
  
  async function handleSubmit(event) {
    event.preventDefault();
    var status = document.getElementById("kontak-status");
    var data = new FormData(event.target);
    fetch(event.target.action, {
      method: form.method,
      body: data,
      headers: {
          'Accept': 'application/json'
      }
    }).then(response => {
      if (response.ok) {
        status.innerHTML = "Terima kasih atas kiriman anda!";
        form.reset()
      } else {
        response.json().then(data => {
          if (Object.hasOwn(data, 'errors')) {
            status.innerHTML = data["errors"].map(error => error["message"]).join(", ")
          } else {
            status.innerHTML = "Ups! Ada masalah saat mengirim form"
          }
        })
      }
    }).catch(error => {
      status.innerHTML = "Ups! Ada masalah saat mengirim  form"
    });
  }
  form.addEventListener("submit", handleSubmit)
</script>