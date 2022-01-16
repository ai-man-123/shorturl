<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Short - URL</title>
<link rel="stylesheet" href="/css/style.css">
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous">
<link rel="stylesheet" href="https://pro.fontawesome.com/releases/v5.10.0/css/all.css" integrity="sha384-AYmEC3Yw5cVb3ZcuHtOA93w35dYTsvhLPVnYs9eStHfGJvOvKxVfELGroGkvsg+p" crossorigin="anonymous" />
</head>
<body class="">
<div class="d-flex justify-content-center">
<div class="card">
<div class="card-body">
<form action="short" method="POST">
<div class="form-group">
<label><i class="fas fa-link"></i> Long URL</label>
<input type="url" name="url" class="form-control" placeholder="Your URL *" required>
<small class="form-text text-muted">Later there will be rules that users must obey if they want to add a new URL!<br>We don't allow you to use this for NSFW stuff...</small>
</div>
<label><i class="fas fa-pencil-alt"></i> Customize URL</label>
<div class="form-group form-inline" id="app-6">
<input type="text" class="form-control col-md-4" placeholder="clph.pw" style="color: white;cursor: not-allowed;" readonly>
<input class="form-control" type="text" name="short" maxlength="16" placeholder="alias" v-model="pesan" id="alias">
<small class="text-muted text-left col-lg-6 d-none d-lg-block">Your URL will be: <strong>{{ location.protocol }}//{{window.location.host}}/{{ pesan }}</strong></small>
</div>
<button type="submit" class="btn btn-primary mb-2">Submit</button>
</form>
<a href="/remove"><button class="btn btn-primary">Remove URL?</button></a>
</div>
</div>
</div>
<script src="https://cdn.jsdelivr.net/npm/vue"></script>
<script>
          var app6 = new Vue({
  el: '#app-6',
  data: {
    pesan: ''
  }
})</script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/limonte-sweetalert2/7.28.2/sweetalert2.all.min.js"></script>
</body>
</html>
