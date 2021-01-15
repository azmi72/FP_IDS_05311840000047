## FP_IDS_05311840000047
### Final Project IDS - Deteksi jika ada seseorang memasukkan flashdisk ke sistem kita tanpa izin. <br>

Program Sederhana untuk mengirim email kepada pemilik sistem setiap kali seseorang memasukkan flashdisk ke dalam sistem.<br>

`mail.py` adalah file python di mana kita bisa mendapatkan email yang dimasukkan seseorang ke dalam flashdisk di perangkat kita setiap kali seseorang memasukkan perangkat usb ke sistem kita. <br>

`mailwithattachment.py` adalah file python setiap kali seseorang memasukkan perangkat USB ke sistem kita, foto pengguna akan diklik dari sistem kita, dan teks beserta foto itu akan dikirimkan kepada email kita.

- Pergi ke pengaturan akun gmail kita:
1. Dari Penerusan dan POP / IMAP.
2. Aktifkan IMAP dari akses IMAP.
3. Sekarang buka Accounts dan Import Tab.
4. Klik Pengaturan Akun Google Lainnya.
5. Sekarang dari keamanan klik panel kiri.
6. Scroll ke bawah, Temukan Less secure app access dan access nya di on kan.
- Instal modul smtplib untuk python
1. `pip3 instal smtplib`
- Masukkan <b>SENDER_EMAIL</b>, <b>RECIEVER_EMAIL</b> dan sandi email pengirim di variabel <b>PASSWORD</b>
- Buka /etc/udev/rules.d/ dan buat syntax kita:
1. vim /etc/udev/rules.d/10.rules
2. Misalkan kode python kita adalah mymail.py di direktori /root
3. Di file rules, tulis: `ACTION=="add", SUBSYSTEM=="usb" RUN=="/root/mymail.py"`
4. Pastikan kita terhubung ke internet dan `mymail.py` kita memiliki izin yang dapat dijalankan.
- Langkah yang sama berlaku untuk file lampiran yaitu `mailwithattachment.py`.
