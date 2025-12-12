## GPU Kiralayabileceğiniz Servisler

Aşağıdaki sağlayıcılar node topluluklarında en çok kullanılan GPU kiralama platformlarıdır. Ödeme yöntemleri ve fiyatlar değişebilir ancak SSH bağlanma mantığı tümünde aynıdır.

| Sağlayıcı   | Ödeme Yöntemi        | Açıklama                                                  |
| ----------- | -------------------- | --------------------------------------------------------- |
| [Vast.ai](https://cloud.vast.ai/?ref_id=222215)    | Kredi kartı / Kripto | En çok kullanılan; fiyat/performans açısından iyi seçenek |
| [RunPod](https://runpod.io?ref=5j0m7csw)      | Kredi kartı / Kripto | Hızlı kurulum, çok sayıda template                        |

Bu sağlayıcıların tamamında aşağıdaki adımlar neredeyse aynıdır:

* SSH key ekleme
* Template seçme
* GPU modeli seçme
* Depolama ayarlama
* Terminalden bağlanma

Şimdi Vast.ai ile örnek anlatıma geçiyoruz.

---

## 1- Vast.ai'e SSH Key Ekleme:

Node için GPU sunucularına bağlanırken SSH key kullanmak hem güvenlik açısından zorunludur hem de şifresiz bağlanmanı sağlar. Aynı yaklaşım **Paperspace, TensorDock, RunPod, Lambda vb. GPU sağlayıcılarının tamamında aynıdır.**

1. Bilgisayarında **Terminal** (veya PowerShell) aç.
2. Aşağıdaki komutu gir:

```bash
ssh-keygen
```

3. Gelen 3 soruya da sadece **Enter** yaparak geç.
4. SSH key dosyan oluşturulacak ve bilgisayarındaki key yolunu verecek. Bu yolu kopyala.

![kopyala](https://github.com/user-attachments/assets/d6da34b4-a93b-4db7-a755-5eeb644545ec)

6. Verilen yolu kopyala ve aşağıdaki gibi başına `cat` ekleyerek terminale gir:

```bash
cat ~/.ssh/id_rsa.pub
```

![Adsız tasarım](https://github.com/user-attachments/assets/a2da6842-94dd-42ef-9fe8-971474780f37)

6. Vast.ai’e gir → soldan **Keys** sekmesine git.
7. Sağ üstten `new` deyip kopyaladığın satırı yapıştır ve kaydet.

Bu işlem sayesinde terminalden sunucularına şifresiz bağlanabilirsin. Aynı yöntem diğer tüm GPU sağlayıcılarında da kullanılmaktadır.

---

## 2- Vast.ai Template Seçimi ve Sunucu Kiralama

Boundless veya benzeri GPU gerektiren node’lar için uygun konfigürasyona sahip bir sunucu kiralaman gerekiyor. Bu adımlar çoğu GPU sağlayıcısında aynı mantıkla çalışır.

1. Vast paneline gir ve sol üstten **“Templates”** sekmesine tıkla.
2. Açılan listeden **“Ubuntu 22.04 VM”** template’ini seç (aşağıdaki görsel).

![Adsız tasarım](https://github.com/user-attachments/assets/452408df-df90-481d-8999-abdec53de3e7)

3. Görseldeki gibi filtreleyip, işine uygun cihazı seçip **Rent** butonuna bas.

![1](https://github.com/user-attachments/assets/29c2df12-340e-4aa9-adf9-d684398945a8)

---

## 3- Sunucuya Giriş

1. Soldan **Instances** kısmına git.
2. Cihazının üzerinde bulunan terminal butonuna bas, **SSH** ile başlayan komutu kopyala.
3. Powershell veya terminaline yapıştırarak sunucuna giriş yap.

![Adsız tasarım](https://github.com/user-attachments/assets/dc14064a-63f0-43a9-b31e-81a2ca2a4bbd)

---

✅ Bu bağlantı yöntemi; RunPod, TensorDock, Paperspace, Lambda vb. tüm GPU sağlayıcılarında benzer şekilde kullanılır. Mantık basit: SSH key oluştur, panele ekle ve terminalden bağlan.
