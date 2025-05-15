
<!DOCTYPE html>
<html>
<head>
  <title>XSS Test</title>
</head>
<body>
  <h2>Tinggalkan Pesan:</h2>
  <form method="GET">
    <input type="text" name="pesan" placeholder="Tulis sesuatu...">
    <button type="submit">Kirim</button>
  </form>

  <p>Pesan Anda:</p>
  <div id="hasil"></div>

  <script>
    const params = new URLSearchParams(window.location.search);
    document.getElementById("hasil").innerHTML = params.get("pesan");
  </script>
</body>
</html>