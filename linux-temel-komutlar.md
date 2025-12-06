# Node Kurarken Sık Kullanılan Komutlar:

Node kurarken en çok ihtiyacın olacak temel Linux komutları.
Her komut tek satırda ve kısa açıklamalı.

---

## 1- Sunucuya Bağlanma:

Sunucuya bağlantı ve kullanıcı işlemleri.

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

Sistemi güncel tutmak ve yeniden başlatma işlemleri.

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

Klasör oluşturma, içine girme, silme ve düzenleme.

```bash
ls           #Bulunduğun dizindeki dosyalar
```

```bash
mkdir ufuk   #Klasör oluştur
```

```bash
cd ufuk    #Klasöre git
```

```bash
rm -rf ufuk  #Klasör + içini sil (tehlikeli)
```

```bash
nano ufuk #Dosyayı düzenle
```

---

## 4- Servis & Log:

Servis durumunu kontrol etmek ve log okumak.

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

Çalışan süreçleri görüntüleme ve sonlandırma.

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

Portları, bağlantıları ve internet erişimini kontrol etmek.

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

Container yönetimi, log ve silme işlemleri.

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
docker rm container           #Container sil
```

```bash
docker exec -it container bash #Container içine gir
```

---

## 8- Sistem & Kaynak:

RAM, disk kullanımı ve sistem yükünü görmek.

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

Terminal ekranını temizlemek ve önceki komutlara bakmak.

```bash
clear       #Ekranı temizle
```

```bash
history     #Geçmiş komutlar
```

---

## 10- Screen:

Node’ları kapatmadan terminalden çıkmak.

```bash
screen -S ufuk     #Yeni screen başlat
```

```bash
screen -ls         #Açık screenleri listele
```

```bash
screen -r ufuk     #Screen'e geri bağlan
```

```bash
CTRL + A + D       #Screen'den çık (arka planda çalışsın)
```

```bash
screen -X -S ufuk quit   #Screen'i kapat
```

- screen → işlemleri arka planda çalıştırır
- terminal kapanınca işlem durmaz
- node kurulumlarında şarttır

---

## ✅ Ek Kaynak:

- Popüler Komutlara Buradan Ulaşabilirsiniz:
[https://www.digitalocean.com/community/tutorials/linux-commands](https://www.digitalocean.com/community/tutorials/linux-commands)
