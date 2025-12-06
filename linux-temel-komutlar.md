# Linux-Sık-Kullanılan-Komutlar.md

Node kurarken en çok ihtiyacın olacak temel Linux komutları.
Her komut tek satırda ve kısa açıklamalı.

---

## 1- Sunucuya Bağlanma:

```bash
ssh user@ip   #Sunucuya bağlan
```

```bash
whoami        #Hangi kullanıcıdayım
```

```bash
passwd        #Şifre değiştir
```

---

## 2- Sistem Güncelleme:

```bash
sudo apt update && sudo apt upgrade -y   #Tüm paketleri güncelle
```

```bash
reboot        #Sunucuyu yeniden başlat
```

```bash
shutdown now  #Sunucuyu kapat
```

---

## 3- Dosya ve Klasör:

```bash
ls           #Bulunduğun dizindeki dosyalar
```

```bash
pwd          #Şu anki dizin
```

```bash
cd klasör    #Klasöre git
```

```bash
mkdir test   #Klasör oluştur
```

```bash
rm -rf test  #Klasör + içini sil (tehlikeli)
```

```bash
nano text.txt #Dosyayı düzenle
```

---

## 4- Servis & Log:

```bash
systemctl status servis   #Servis durumu
```

```bash
systemctl restart servis  #Servisi yeniden başlat
```

```bash
journalctl -xe            #Hata loglarına bak
```

```bash
tail -f /var/log/syslog   #Canlı log oku
```

---

## 5- Process Yönetimi:

```bash
ps aux         #Çalışan işlemler
```

```bash
kill PID       #Süreç sonlandır
```

```bash
top            #CPU kullanan işlemler
```

---

## 6- Port & Ağ:

```bash
lsof -i         #Açık portları gör
```

```bash
lsof -i :80     #80 portu kimde
```

```bash
ufw allow 3000  #Port aç
```

```bash
ping google.com #İnternet var mı
```

```bash
curl ifconfig.me #IP adresini öğren
```

---

## 7- Docker:

```bash
docker ps                     #Çalışan container’lar
```

```bash
docker logs -f container      #Canlı log
```

```bash
docker restart container      #Container’ı yeniden başlat
```

```bash
docker stop container         #Container’ı durdur
```

```bash
docker exec -it container bash #Container içine gir
```

---

## 8- Sistem & Kaynak:

```bash
free -h     #RAM kullanımını gör
```

```bash
df -h       #Disk kullanımını gör
```

```bash
htop        #CPU RAM canlı izleme
```

```bash
ncdu        #Hangi klasör yer kaplıyor
```

---

## 9- Temizlik:

```bash
clear       #Ekranı temizle
```

```bash
history     #Geçmiş komutlar
```
