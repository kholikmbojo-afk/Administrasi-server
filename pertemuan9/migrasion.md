#Melakukan uploading web apps dynamic ke EC2 AWS
1. Pastikan Web Apps Dynamic tidak error di localhost

2. Jika sudah tanpa error, membuat folder build
npm run build
pastikan menghasilkan folder .next/standlone didalam tersedia folder static
![alt text](image-4.png)
![alt text](image-5.png)

3. Proses Upload File Folder Standalone
Lakukan Proses Acchive pada folder .next/standalone dan folder public
Running Instance -> Connect Open SSH -> Connect FileZilla
upload file hasil archive ke EC2 AWS menggunakan FileZilla
![alt text](image-6.png)
ekstrak file hasil archive
Install tools Unzip di EC2
sudo apt install unzip -y

cd /var/www/html
command ls untuk cek
Ekstrak file hasil archive
unzip nama_file.zip
![alt text](image-7.png)

4. Export dbcompro dari localhost dari database phpmyadmin dalam bentuk sql

masuk ke user compro (command sudo mysql -u userCompro -p)
masukan password
Cek database dbComrpo (show databases;)
command (use dbCompro)
paste isi database sql (hilangkan ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci) dulu
![alt text](image-8.png)
![alt text](image-9.png)
![alt text](image-10.png)

5. Seseuaikan isi file .env di file zilla 
![alt text](image-11.png)

6. di Terminal SSH cd ke folder standalone run apps
exit database
cd standalone
pm2 start server.js 
![alt text](image-12.png)

7. Buka port di security group EC2

Klik nama security di instance scroll sampe ada link
edit inbound rules
add rule
port 3000
save rule
![alt text](image-13.png)

8. dan berhasil
![alt text](image-14.png)
