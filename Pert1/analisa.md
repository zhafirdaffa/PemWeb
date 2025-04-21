

### **Analisis Docker Compose & Nginx pakai 5W 1H**

1. #What (Apa sih ini?)   
   Ini adalah konfigurasi buat ngejalanin **Nginx** di dalam Docker container. Ada file (docker-compose.yml) yang nge-setup layanan **web** pakai image **nginx:latest**. Trus ada file (.env) buat ngasih nama proyek dan repository, dan file (nginx.conf) buat konfigurasi web server.

2. #Who  (Siapa yang pakai ini?)
  
   Biasanya sih yang pakai ini **developer** atau **mahasiswa teknik informatika** yang lagi belajar **web server**, **Docker**, dan **deployment aplikasi web**. Bisa juga buat tim yang mau gampang nge-deploy website tanpa harus install Nginx secara manual.

3. #Where (Dimana ini berjalan?)
   
   Ini dijalankan di **Docker**. Jadi selama ada **Docker & Docker Compose** di komputer bisa di Linux, macOS, atau Windows, bisa langsung dijalankan. Kalau mau akses web-nya, tinggal buka **localhost** di browser.

4. #When (Kapan ini dipakai?)
   
   Dipakai pas butuh **web server cepat & gampang dikonfigurasi**. Misalnya buat **belajar Nginx**, **ngetes website statis**, atau **nge-deploy latihan pemrograman web** tanpa ribet setting server manual.

5. #Why  (Kenapa Pakai ini?)
   - **Lebih praktis** → Gak perlu install Nginx satu-satu, cukup jalanin (docker-compose up -d).  
   - **Portable** → Bisa jalan di mana aja selama ada Docker.  
   - **Mudah dikonfigurasi** → Tinggal edit (nginx.conf) kalau mau ubah aturan routingnya.  
   - **Isolasi lingkungan** → Nginx dan websitenya jalan di dalam container, jadi gak ganggu sistem utama.

6. #How  (Gimana Cara Kerjanya?)
   - (docker-compose.yml) nge-define service **web** yang pakai image **nginx:latest**.  
   - Nginx bakal **listen di port 80**, trus ngeload file HTML dari folder (src dan latihan).  
   - (nginx.conf) ngatur biar akses ke [/] buka file dari (/usr/share/nginx/html, dan akses ke /latihan) buka dari (/usr/share/nginx/latihan/).  
   - Jadi, kalau ada file **index.html** di (src), bisa diakses di (localhost). Kalau ada file **home.html** di (latihan), bisa diakses di (localhost/latihan).  
