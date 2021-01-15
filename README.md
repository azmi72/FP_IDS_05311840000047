## FP_IDS_05311840000047
### Final Project IDS - Deteksi jika ada seseorang memasukkan flashdisk ke sistem kita tanpa izin. <br>

Program Sederhana untuk mengirim email kepada pemilik sistem setiap kali seseorang memasukkan flashdisk ke dalam sistem.<br>

`mail.py` adalah file python di mana kita bisa mendapatkan email yang dimasukkan seseorang ke dalam flashdisk di perangkat kita setiap kali seseorang memasukkan perangkat usb ke sistem kita. <br>

`mailwithattachment.py` adalah file python setiap kali seseorang memasukkan perangkat USB ke sistem kita, foto pengguna akan diklik dari sistem kita, dan teks beserta foto itu akan dikirimkan kepada email kita.

1. Pergi ke pengaturan akun gmail kita:
- Dari Penerusan dan POP / IMAP.
- Aktifkan IMAP dari akses IMAP.
- Sekarang buka Accounts dan Import Tab.
- Klik Pengaturan Akun Google Lainnya.
- Sekarang dari keamanan klik panel kiri.
- Scroll ke bawah, Temukan Less secure app access dan access nya di on kan.
2. Instal modul smtplib untuk python
- `pip3 instal smtplib`
3. Masukkan <b>SENDER_EMAIL</b>, <b>RECIEVER_EMAIL</b> dan sandi email pengirim di variabel <b>PASSWORD</b>
4. Buka /etc/udev/rules.d/ dan buat syntax kita:
- vim /etc/udev/rules.d/10.rules
- Misalkan kode python kita adalah mymail.py di direktori /root
- Di file rules, tulis: `ACTION=="add", SUBSYSTEM=="usb" RUN=="/root/mymail.py"`
- Pastikan kita terhubung ke internet dan `mymail.py` kita memiliki izin yang dapat dijalankan.
5. Langkah yang sama berlaku untuk file lampiran yaitu `mailwithattachment.py`.
