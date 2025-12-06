# En Çok Kullanılan Linux Komutları (Node & VPS İçin)

Bu liste tamamen “node çalıştıran kullanıcılar” için hazırlanmıtır.
Her komut **tek cümle ile ne işe yarar** şeklinde açıklanmıştır.

---

## 1- Klasör & Dosya İşlemleri:

```bash
ls
```

- Bulunduğun klasördeki dosyaları listeler.

```bash
pwd
```

- Bulunduğun klasörün tam yolunu gösterir.

```bash
cd klasör
```

Bir klasöre girmeni sağlar.

```bash
mkdir klasör
```

Yeni klasör oluşturur.

```bash
rm -rf klasör
```

Klasörü içindekilerle birlikte siler (dikkat!).

```bash
touch dosya.txt
```

- Yeni boş dosya oluşturur.

```bash
nano dosya.txt
```

- Dosyayı düzenlemeni sağlar.

---

## 2- Paket Yönetimi

```bash
apt update
apt upgrade -y
```

- Sistemi günceller (her zaman ilk yapılır).

```bash
apt install paket
```

- Bir program/paket yükler.

```bash
apt remove paket
```

- Kurulu programı siler.

---

## 3- Sistem & Kullanıcı:

```bash
sudo komut
```

- Komutu yönetici olarak çalıştırır.

```bash
whoami
```

- Şu an hangi kullanıcı olduğunu gösterir.

```bash
htop
```

- CPU, RAM kullanımını canlı gösterir.

```bash
free -h
```

- RAM kullanımını gösterir.

```bash
df -h
```

- Disk kullanımını gösterir.

---

## 4- Servis & Log:

```bash
systemctl status servis
```

- Servisin çalışıp çalışmadığını gösterir.

```bash
systemctl restart servis
```

- Servisi yeniden başlatır.

```bash
journalctl -xe
```

- Hata loglarını gösterir.

```bash
tail -f /var/log/syslog
```

- Canlı log okumanızı sağlar.

---

## 6- Process / İşlem Yönetimi:

```bash
ps aux
```

- Açık olan tüm işlemleri gösterir.

```bash
top
```

- CPU kullanan işlemleri listeler.

```bash
kill PID
```

- Bir işlemi kapatır.

---

## 7- Port & Ağ

```bash
lsof -i -P -n
```

- Sistemdeki açık portları gösterir.

```bash
lsof -i :80
```

- 80 portunu hangi uygulama kullanıyor gösterir.

```bash
ufw allow 3000
```

- Port açar.

```bash
ping google.com
```

- İnternete çıkış var mı test eder.

```bash
curl site
```

- Bir URL’den veri çeker.

---

## 8- SSH & Kopyalama

```bash
ssh user@ip
```

- Sunucuya bağlanır.

```bash
scp dosya user@ip:/hedef
```

- Dosya kopyalar.

---

## 9- Docker

```bash
docker ps
```

- Çalışan container’ları gösterir.

```bash
docker logs -f container
```

- Container loglarını canlı gösterir.

```bash
docker restart container
```

- Container’ı yeniden başlatır.

```bash
docker stop container
```

- Çalışan container’ı durdurur.

```bash
docker exec -it container bash
```

- Container içine terminal açar.

---

## 10- Temizlik

```bash
clear
```

Terminal ekranını temizler.

```bash
reboot
```

- Sunucuyu yeniden başlatır.
