1.patikan udah instal putty
![alt text](image-10.png)

 konversi file key
![alt text](image-11.png)

2.konversi file public key dari .pem menjadi .ppk di putty

buka puttyGen
load file .pem
save as .ppk
![alt text](image-12.png)

3.set up putty untuk remote ssh
buka apps putty
isi ip public sesuai
isi port untuk ssh sesuai security group di instance
isi nama sessiom
load file .ppk (klik ssh > auth > credentials > load file .ppk)
![alt text](image-13.png)
![alt text](image-14.png)

4.sudo apt-get update terus sudo apt-get upgrade
![alt text](image-15.png)

5.pembuktian remote ssh secara visual
copy public address instance paste ke browse
![alt text](image-16.png)

6.install web server seperti apache
sudo apt install apache2
reload browser
![alt text](image-17.png)

7.matikan instance agar tidak kena tagihan
sudo shutdown now
![alt text](image-18.png)