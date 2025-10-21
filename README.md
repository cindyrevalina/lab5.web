# 🌐 Praktikum 5 – JavaScript
🏫 **Universitas Pelita Bangsa**

🧑 **Nama:** Cindy Revalina Simanullang

🆔 **NIM:** 312410417

💻 **Kelas:** TI.24.A3

👨‍💻 **Mata Kuliah:** Pemrograman Web

📅 **Dosen Pengampu:** Agung Nugroho, S.Kom., M.Kom

---
## ⚙️ Langkah-Langkah Praktikum

---

### 🧾 **1️⃣ Pengenalan JavaScript**

**File:** `latihan1_hello.html`

```html
<script>
  document.write("Hello World<br>");
  console.log("Hello World dari console browser");
</script>
```

📘 **Penjelasan:**

* `document.write()` menampilkan teks langsung di halaman web.
* `console.log()` menampilkan pesan di konsol pengembang (untuk debugging).

📸 **Screenshot Hasil:**
<img src="picture/La5_javascript.png">

---

### 🔔 **2️⃣ Alert**

**File:** `latihan2_alert.html`

```html
<script>
  window.alert("Selamat datang di Praktikum JavaScript!");
</script>
```

📘 **Penjelasan:**
`alert()` menampilkan jendela popup berisi pesan kepada pengguna.

📸 **Screenshot Hasil:**

> <img src="picture/alert1.png">
><img src="picture/alert2.png">
> ---

---

### 💬 **3️⃣ Prompt Input**

**File:** `latihan3_prompt.html`

```html
<script>
  var nama = prompt("Masukkan nama Anda:");
  document.write("Halo, " + nama);
</script>
```

📘 **Penjelasan:**

* `prompt()` meminta input dari pengguna.
* Hasil input disimpan dalam variabel `nama`.
* Ditampilkan kembali ke halaman dengan `document.write()`.

📸 **Screenshot Hasil:**

> <img src="picture/prompt1.png">
><img src="picture/prompt2.png">
> ---

---

### ⚙️ **4️⃣ Fungsi JavaScript**

**File:** `latihan4_fungsi.html`

```html
<script>
  function sapa() {
    alert("Halo! Ini fungsi JavaScript dipanggil dari tombol.");
  }
</script>

<button onclick="sapa()">Klik Saya</button>
```

📘 **Penjelasan:**
Fungsi `sapa()` dibuat menggunakan keyword `function` dan dijalankan lewat event `onclick`.

📸 **Screenshot Hasil:**

> <img src="picture/fungsi.png">
> ---

---

### ➗ **5️⃣ Operasi Aritmatika**

**File:** `latihan5_aritmatika.html`

```html
<script>
  let a = 10, b = 5;
  document.write("Penjumlahan: " + (a + b) + "<br>");
  document.write("Pengurangan: " + (a - b) + "<br>");
  document.write("Perkalian: " + (a * b) + "<br>");
  document.write("Pembagian: " + (a / b) + "<br>");
</script>
```

📘 **Penjelasan:**
Menampilkan operasi matematika dasar dengan dua variabel `a` dan `b`.

📸 **Screenshot Hasil:**

> <img src="picture/aritmatika.png">
> ---

---

### ⚖️ **6️⃣ Seleksi Kondisi (If...Else)**

**File:** `latihan6_if_else.html`

```html
<script>
  let nilai = prompt("Masukkan nilai Anda:");
  if (nilai >= 70) {
    alert("Selamat, Anda Lulus!");
  } else {
    alert("Maaf, Anda Belum Lulus.");
  }
</script>
```

📘 **Penjelasan:**
`if...else` digunakan untuk pengambilan keputusan berdasarkan kondisi logika.

📸 **Screenshot Hasil:**

> <img src="picture/if_else1.png">
> <img src="picture/if_else2.png">
> ---

---

### 🔄 **7️⃣ Switch Case**

**File:** `latihan7_switch.html`

```html
<script>
  let hari = prompt("Masukkan nama hari:");
  switch (hari.toLowerCase()) {
    case "senin": alert("Hari kerja pertama!"); break;
    case "sabtu": alert("Akhir pekan!"); break;
    case "minggu": alert("Hari libur!"); break;
    default: alert("Hari tidak dikenali!");
  }
</script>
```

📘 **Penjelasan:**
`switch` digunakan untuk memeriksa beberapa kondisi sekaligus dengan lebih efisien daripada `if...else`.

📸 **Screenshot Hasil:**

> <img src="picture/switch.png">
> <img src="picture/switch2.png">
> ---

---

### 🧍‍♂️ **8️⃣ Tugas Akhir – Validasi Form**

**File:** `form_validasi.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Validasi Form dengan JavaScript</title>
</head>
<body>
  <h2>Form Validasi JavaScript</h2>

  <form id="formData" onsubmit="return validasiForm()">
    <label>Nama:</label><br>
    <input type="text" id="nama" placeholder="Masukkan nama Anda"><br><br>

    <label>Email:</label><br>
    <input type="email" id="email" placeholder="contoh@email.com"><br><br>

    <label>Umur:</label><br>
    <input type="number" id="umur" placeholder="Masukkan umur Anda"><br><br>

    <button type="submit">Kirim</button>
  </form>

  <script>
    function validasiForm() {
      let nama = document.getElementById("nama").value.trim();
      let email = document.getElementById("email").value.trim();
      let umur = document.getElementById("umur").value.trim();

      if (nama === "" || email === "" || umur === "") {
        alert("❌ Semua field wajib diisi!");
        return false;
      }

      let emailPattern = /^[^ ]+@[^ ]+\.[a-z]{2,3}$/;
      if (!email.match(emailPattern)) {
        alert("⚠️ Format email tidak valid!");
        return false;
      }

      if (umur < 18) {
        alert("🚫 Umur minimal adalah 18 tahun!");
        return false;
      }

      alert("✅ Data berhasil dikirim! Terima kasih, " + nama + ".");
      return true;
    }
  </script>
</body>
</html>
```

📘 **Penjelasan Tugas:**

| Elemen                             | Fungsi                                                      |
| ---------------------------------- | ----------------------------------------------------------- |
| `onsubmit="return validasiForm()"` | Menjalankan fungsi sebelum data dikirim.                    |
| `trim()`                           | Menghapus spasi kosong agar input tidak dianggap isi palsu. |
| `emailPattern`                     | Regex untuk validasi format email.                          |
| `if (umur < 18)`                   | Menolak data jika umur di bawah 18 tahun.                   |
| `alert()`                          | Menampilkan hasil validasi (salah atau benar).              |

📸 **Screenshot Hasil:**

> <img src="picture/validasi.png">
> <img src="picture/validasi1.png">
> ---

### 🧮 **9️⃣ HTML DOM – CheckBox Otomatis**

**File:** `latihan9_checkbox.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>CheckBox Otomatis</title>
</head>
<body>
  <h2>Pilih Makanan Favorit:</h2>

  <input type="checkbox" name="makanan" value="Nasi Goreng" onclick="hitungTotal()"> pecel lele <br>
  <input type="checkbox" name="makanan" value="Bakso" onclick="hitungTotal()"> Bakso <br>
  <input type="checkbox" name="makanan" value="Sate" onclick="hitungTotal()"> Sate <br>
  <input type="checkbox" name="makanan" value="Mie Ayam" onclick="hitungTotal()"> Mie Ayam <br><br>

  <p>Total item dipilih: <span id="total">0</span></p>

  <script>
    function hitungTotal() {
      let checkbox = document.querySelectorAll('input[name="makanan"]:checked');
      document.getElementById("total").innerText = checkbox.length;
    }
  </script>
</body>
</html>
```

📘 **Penjelasan:**

* Menggunakan **HTML DOM** untuk menghitung jumlah checkbox yang dicentang.
* `querySelectorAll('input[name="makanan"]:checked')` mengambil semua checkbox yang dipilih.
* Nilai total ditampilkan langsung melalui elemen `<span id="total">`.

📸 **Screenshot Hasil:**

> <img src="picture/checkbox.png">
> ---

---

### 📂 **10️⃣ Eksternal JavaScript**

**File:** `eksternal.js`

```javascript
document.write("Hello World dari file eksternal.js<br>");
console.log("Pesan dari eksternal JavaScript!");
```

**File HTML yang memanggil eksternal.js:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Eksternal JavaScript</title>
  <script src="eksternal.js"></script>
</head>
<body>
  <h2>Contoh JavaScript Eksternal</h2>
</body>
</html>
```

📘 **Penjelasan:**

* File `.js` eksternal memungkinkan kita memisahkan logika JavaScript dari struktur HTML.
* Kelebihan:

  * 📁 Kode lebih rapi dan mudah dikelola.
  * ⚡ Loading halaman lebih cepat karena cache browser.
  * 🔁 Dapat digunakan ulang di beberapa halaman.

---

### ✅ Setelah itu lanjutkan ke bagian:

👉 **11️⃣ Tugas Akhir – Validasi Form**

---![alt text](image.png)

## 📚 **Struktur Folder**

```
lab5_javascript/
│
├── latihan1_hello.html
├── latihan2_alert.html
├── latihan3_prompt.html
├── latihan4_fungsi.html
├── latihan5_aritmatika.html
├── latihan6_if_else.html
├── latihan7_switch.html
├── form_validasi.html
└── README.md
```

---

## 🧾 **Laporan Praktikum**

1. 📂 Buat repository **Lab5Web** di GitHub.
2. 💾 Upload seluruh file latihan dan tugas.
3. 📸 Masukkan screenshot hasil di README.md sesuai ruang kosong di atas.
4. 📝 Commit dan Push hasilnya ke GitHub.
5. 🔗 Kirimkan URL repository ke e-learning Universitas Pelita Bangsa.

---
