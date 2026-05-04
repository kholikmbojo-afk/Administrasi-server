1.mengaktifkan instance
![alt text](image.png)
2. Lakukan Pathching OS

sudo apt-get update && sudo apt-get upgrade
![alt text](image-1.png)

3. Install MariaDB
sudo apt-get install mariadb-server 
![alt text](image-2.png)
sudo system start mariadb
sudo system status mariadb
![alt text](image-3.png)
coba apakah default setting yang berlaku (sudo mysql -u root -p)
cek apakah masih ada database dummy (show databases;)
![alt text](image-4.png)

4. lakukan Hardening Security
Masukan Command sudo mysql_secure_installation
Switch to unix_socket authentication : Y
Change the root password? : Y
Remove anonymous users? : Y
Disallow root login remotely? : Y
Remove test database and access to it? : Y
Reload privilege tables now? : Y
![alt text](image-5.png)
Cek kembali apakah masih bisa login tanpa pw
![alt text](image-6.png)
dan berhasil

5. Membuat database dan User

membuat database untuk web company profile (create database dbCompro;)
membuat user untuk web company profile (create user 'userCompro'@'localhost' identified by '*********';)
Memberikan Hak akses user untuk web company profile (grant all privileges on dbCompro.* to userCompro'@'localhost';)
flush privileges
![alt text](image-7.png)

6. Login menggunakan akun database yang sudah di buat

login menggunakan username (sudo mysql -u userCompro -p)
enter password yang sudah di buat (passwordCompro)
lihat database yang sudah dibuat (show databases;)
![alt text](image-10.png)