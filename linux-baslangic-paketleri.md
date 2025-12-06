# Bir Node Kurmak İçin Gerekli Paketler ve Araçlar.

Kurduğumuz node'lar için gerekli tüm paketlerin kurulumunu buradaki komutlar ile gerçekleştirebilirsiniz.

---

## 1- Sistem Güncellemesi:

```bash
sudo apt-get update && sudo apt-get upgrade -y
```

---

## 2- Temel Paketler:

Yazılım derlemek, dosya indirmek ve sistem izlemek için. Bu araçlar çoğu projede eğer sıfır bir sunucudaysanız kurmalısınız.

```bash
sudo apt install -y curl screen iptables build-essential git wget lz4 jq make gcc nano \
automake autoconf tmux htop nvme-cli pkg-config libssl-dev libleveldb-dev \
tar clang bsdmainutils ncdu unzip ca-certificates net-tools iputils-ping
```

---

## 3- Python 3:

Script ve bot çalıştırmak için.

```bash
sudo apt install -y python3-pip python3-dev build-essential libssl-dev libffi-dev
```

---

## 3- Go 1.23.5:

Çoğu blockchain node'u Go ile yazılmıştır.

```bash
sudo rm -rf /usr/local/go
curl -L https://go.dev/dl/go1.23.5.linux-amd64.tar.gz | sudo tar -xzf - -C /usr/local
echo 'export PATH=$PATH:/usr/local/go/bin:$HOME/go/bin' >> $HOME/.bash_profile
echo 'export PATH=$PATH:/usr/local/go/bin:$HOME/go/bin' >> $HOME/.bashrc
source $HOME/.bashrc
go version
```

---

## 4- Node.js 24 LTS:

Web3 araçları için gerekli.

```bash
sudo apt-get remove -y nodejs
sudo apt-get purge -y nodejs
sudo apt-get autoremove -y
sudo rm -f /etc/apt/keyrings/nodesource.gpg
sudo rm -f /etc/apt/sources.list.d/nodesource.list

sudo apt-get update
curl -fsSL https://deb.nodesource.com/setup_24.x | sudo -E bash -
sudo apt install -y nodejs

node -v
npm -v

sudo npm install -g yarn
yarn -v
```

---

## 5- Docker + Docker Compose:

Node'ları konteyner içinde çalıştırmak için.

```bash
sudo apt update -y && sudo apt upgrade -y

for pkg in docker.io docker-doc docker-compose docker-compose-v2 podman-docker containerd runc; do 
  sudo apt-get remove -y $pkg
done

sudo apt-get install -y ca-certificates curl gnupg
sudo install -m 0755 -d /etc/apt/keyrings

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg

echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt update -y
sudo apt-get install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

sudo usermod -aG docker $USER
newgrp docker

docker --version
docker compose version
```

---

## 6- Port ve Firewall:

Port açmak ve kontrol etmek için.

```bash
sudo apt install -y lsof ufw
```

```bash
# Açık portları görmek için:
sudo lsof -i -P -n | grep LISTEN

# Port açmak için (örnek):
sudo ufw allow 3000
```

---

## 7- Sistem İzleme:

CPU, RAM ve disk kullanımını görmek için.

```bash
sudo apt install -y htop ncd
```

```bash
htop        # CPU/RAM izle
ncdu /      # Disk kullanımı
```

---

## 8- Ek Ayarlar (Opsiyonel):

### Swap Oluşturma (RAM az ise).

```bash
sudo fallocate -l 8G /swapfile
sudo chmod 600 /swapfile
sudo mkswap /swapfile
sudo swapon /swapfile
echo '/swapfile none swap sw 0 0' | sudo tee -a /etc/fstab
```

## Paketler Güncel ve Yüklü mü Kontrol Et:

```bash
python3 --version
go version
node -v
docker --version
git --version
```
