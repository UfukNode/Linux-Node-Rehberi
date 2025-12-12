# 1- VPS Nereden Alınır?

VPS’i uzak sunucu olarak düşünebilirsiniz. Kendi bilgisayarınızı yormamak, donanımı yıpratmamak veya kesintisiz çalışmak istediğimiz zaman, node’ları bu sunucular üzerinde çalıştırırız. Node kurarken kullanılabilecek en temel araçtır.

Kullandığım VPS sağlayıcıları:

| Sıra | Sağlayıcı | Ödeme Yöntemi     | Açıklama                                                             |
| :--- | :-------- | :---------------- | :------------------------------------------------------------------- |
| 2    | [Contabo](https://contabo.com/en/vps/)  | Kredi kartı       | Uygun fiyatlı ancak bazı node’larda bant genişliği sorunları yaşadık |
| 3    | [Serverica](https://clients.servarica.com/)   | Kripto            | Fiyat/performans açısından dengeli                                   |
| 4    | [Netcup](https://www.netcup.com/en/server/vps)    | Kripto            | İyi performans, bazı ucuz paketler bulmak mümkün                     |

---

# 2- Hangi sistemi almalıyım?

* Bu kısım projeden projeye değişir.
* Her node projesinin minimum sistem gereksinimini kontrol edin.
* Rehberlerde genellikle hangi sunucunun uygun olduğu zaten yazıyor. (X hesabımı takip ederek güncellemeleri kaçırmazsınız.)
* Eğer proje GPU istiyorsa, ayrıca hazırladığım GPU rehberine bakabilirsiniz.

---

# 3- Örnek VPS Satın Alma

Mantığı anlamanız için herhangi bir sağlayıcı üzerinden örnek gösteriyorum.
Hangi sağlayıcıyı seçtiğiniz süreç açısından büyük bir fark yaratmaz.
Panel isimleri değişebilir ama mantık hep aynıdır.

Diyelim ki projede istenen sistem gereksinimleri şöyle olsun:

*(Buraya proje örneği ekleyebilirsiniz. Ben rehberlerde proje bazlı öneri ekliyorum.)*

---

# 4- VPS’e Nasıl Bağlanılır?

VPS’e SSH ile bağlanmak için bir istemci (MobaXterm, Termius vb.) kullanabilirsiniz. Ancak bilgisayarınızın kendi terminali (PowerShell) üzerinden de direkt bağlantı kurmanız mümkün.

Kolaylık sağlaması açısından daha sonra MobaXterm için ayrı bir rehber paylaşacağım, fakat önce terminal üzerinden bağlanmayı öğrenmeniz daha sağlıklı olacaktır.

---

### Terminal (PowerShell) ile bağlantı:

1. Windows’ta PowerShell’i açın.
2. Aşağıdaki formatta komutu yazın:

   ```bash
   ssh root@SUNUCU-IP-ADRESİ
   ```
3. Enter’a basın.
4. VPS sağlayıcısından mail ile gelen (veya panel üzerinden belirlediğiniz) şifreyi girin.
   *Şifre yazılırken görünmez, bu normaldir.*

---
