1. Start instances AWS
2. Paching OS -> sudo apt-get update && sudo apt-get upgrade
3. Hapus Layanan nginx -> sudo systemctl stop apache2 && sudo systemctl disable apache2 -> sudo apt remove apache2
- docker ps -la
4. Hapus layanan Mariadb dan uninstall -> sudo systemctl stop mariadb && suddo systemctl desable mariadb
- sudo apt auto-remove mariadb-server -> systemctl status mariadb mariadb-client mariadb-common
5. esting Next.JS + db menggunakan user bukan root pada local environment
![alt text](image.png)
- Klik user yang sudah di buat -> pilih database -> pilih dbcompro -> terus klik all -> go
![alt text](image-1.png)
- sesuaikan file .env
- open terminal -> cd web-dinamis
- npm i
- npm run dev -> cek website localhost
![alt text](image-2.png)
