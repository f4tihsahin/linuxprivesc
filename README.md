# Linux Privilege Escalation Tools Collection

<p>
  <img src="https://img.shields.io/badge/platform-linux-0f62fe?style=for-the-badge&logo=linux&logoColor=white" alt="Platform Linux">
  <img src="https://img.shields.io/badge/shell-bash-121011?style=for-the-badge&logo=gnubash&logoColor=white" alt="Shell Bash">
  <img src="https://img.shields.io/badge/runtime-python3-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python 3">
</p>

Linux sistemlerde yetki yükseltme (privilege escalation) testleri için kullanılan popüler araçların tek yerde toplandığı sade ve pratik bir koleksiyon.

> [!WARNING]
> Bu araçları yalnızca **izinli** güvenlik testlerinde ve yasal kapsamda kullanın.

## 📚 İçindekiler

- [İçerik](#icerik)
- [Hızlı Başlangıç](#hizli-baslangic)
- [Araçları Tek Tek Çalıştırma](#araclari-tek-tek-calistirma)
- [Toplu Çalıştırma Senaryoları](#toplu-calistirma-senaryolari)
- [Arka Planda Çalıştırma](#arka-planda-calistirma)
- [Cron ile Zamanlama](#cron-ile-zamanlama)
- [Sadece LinPEAS (Minimal Kullanım)](#sadece-linpeas-minimal-kullanim)

<a id="icerik"></a>
## 📦 İçerik

| Dosya | Açıklama | Kısa Çalıştırma |
|---|---|---|
| `les.sh` | Linux Exploit Suggester — Kernel zafiyetlerini tespit eder | `./les.sh` |
| `linpeas.sh` | LinPEAS — Kapsamlı yetki yükseltme vektörü tarayıcısı | `./linpeas.sh` |
| `lse.sh` | Linux Smart Enumeration — Hızlı ve okunaklı sistem analizi | `./lse.sh -i` |
| `unix-privesc-check` | Unix yetki yükseltme denetleyicisi | `./unix-privesc-check standard` |
| `beroot.py` | BeRoot — Python ile yazılmış privesc aracı | `python3 beroot.py` |
| `LinEnum.sh` | Klasik Linux sistem enumürasyon aracı | `./LinEnum.sh` |

<a id="hizli-baslangic"></a>
## 🚀 Hızlı Başlangıç

### 1) Tüm araçları indir

```bash
cd /tmp
wget -q https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/les.sh -O les.sh
wget -q https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/linpeas.sh -O linpeas.sh
wget -q https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/lse.sh -O lse.sh
wget -q https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/unix-privesc-check -O unix-privesc-check
wget -q https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/beroot.py -O beroot.py
wget -q https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/LinEnum.sh -O LinEnum.sh
chmod +x *.sh *.py unix-privesc-check
echo "✅ Tüm araçlar indirildi."
```

### 2) Tüm taramaları sırayla çalıştır

```bash
cd /tmp
./les.sh > les.txt
./linpeas.sh > linpeas.txt
./lse.sh -i > lse.txt
./unix-privesc-check standard > unix_privesc.txt
python3 beroot.py > beroot.txt
./LinEnum.sh > linenum.txt
echo "✅ Tüm taramalar tamamlandı."
ls -lah *.txt
```

### 3) Tek komutla indir + çalıştır + kaydet

```bash
cd /tmp && \
wget -q https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/les.sh -O les.sh && \
wget -q https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/linpeas.sh -O linpeas.sh && \
wget -q https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/lse.sh -O lse.sh && \
wget -q https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/unix-privesc-check -O unix-privesc-check && \
wget -q https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/beroot.py -O beroot.py && \
wget -q https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/LinEnum.sh -O LinEnum.sh && \
chmod +x *.sh *.py unix-privesc-check && \
./les.sh > les.txt && \
./linpeas.sh > linpeas.txt && \
./lse.sh -i > lse.txt && \
./unix-privesc-check standard > unix_privesc.txt && \
python3 beroot.py > beroot.txt && \
./LinEnum.sh > linenum.txt && \
ls -lah *.txt
```

<a id="araclari-tek-tek-calistirma"></a>
## 🔧 Araçları Tek Tek Çalıştırma

<details>
<summary><strong>1) Linux Exploit Suggester (LES)</strong></summary>

```bash
wget https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/les.sh -O les.sh
chmod +x les.sh
./les.sh > les_output.txt
```
</details>

<details>
<summary><strong>2) LinPEAS</strong></summary>

```bash
wget https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/linpeas.sh -O linpeas.sh
chmod +x linpeas.sh
./linpeas.sh > linpeas_output.txt
```
</details>

<details>
<summary><strong>3) Linux Smart Enumeration (LSE)</strong></summary>

```bash
wget https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/lse.sh -O lse.sh
chmod +x lse.sh
./lse.sh -i > lse_output.txt
```
</details>

<details>
<summary><strong>4) Unix Privesc Check</strong></summary>

```bash
wget https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/unix-privesc-check -O unix-privesc-check
chmod +x unix-privesc-check
./unix-privesc-check standard > unix_privesc_output.txt
```
</details>

<details>
<summary><strong>5) BeRoot</strong></summary>

```bash
wget https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/beroot.py -O beroot.py
chmod +x beroot.py
python3 beroot.py > beroot_output.txt
```
</details>

<details>
<summary><strong>6) LinEnum</strong></summary>

```bash
wget https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/LinEnum.sh -O LinEnum.sh
chmod +x LinEnum.sh
./LinEnum.sh > linenum_output.txt
```
</details>

<a id="toplu-calistirma-senaryolari"></a>
## 📊 Toplu Çalıştırma Senaryoları

### Yöntem 1: Tarih damgalı ayrı dosyalar

```bash
DATE=$(date +%Y%m%d_%H%M%S)

./les.sh > les_${DATE}.txt
./linpeas.sh > linpeas_${DATE}.txt
./lse.sh -i > lse_${DATE}.txt
./unix-privesc-check standard > unix_privesc_${DATE}.txt
python3 beroot.py > beroot_${DATE}.txt
./LinEnum.sh > linenum_${DATE}.txt

echo "✅ Çıktılar kaydedildi: ${DATE}"
ls -lah *_${DATE}.txt
```

### Yöntem 2: Tüm çıktıları tek dosyada toplama

```bash
{
  echo "==================== LES ===================="
  ./les.sh
  echo -e "\n\n==================== LINPEAS ===================="
  ./linpeas.sh
  echo -e "\n\n==================== LSE ===================="
  ./lse.sh -i
  echo -e "\n\n==================== UNIX PRIVESC CHECK ===================="
  ./unix-privesc-check standard
  echo -e "\n\n==================== BEROOT ===================="
  python3 beroot.py
  echo -e "\n\n==================== LINENUM ===================="
  ./LinEnum.sh
} > all_scans_$(date +%Y%m%d_%H%M%S).txt

ls -lah all_scans_*.txt
```

<a id="arka-planda-calistirma"></a>
## 🚀 Arka Planda Çalıştırma

### Tüm araçları arka planda başlat

```bash
nohup ./les.sh > les_output.txt 2>&1 &
nohup ./linpeas.sh > linpeas_output.txt 2>&1 &
nohup ./lse.sh -i > lse_output.txt 2>&1 &
nohup ./unix-privesc-check standard > unix_privesc_output.txt 2>&1 &
nohup python3 beroot.py > beroot_output.txt 2>&1 &
nohup ./LinEnum.sh > linenum_output.txt 2>&1 &

echo "✅ Tüm araçlar arka planda çalışıyor."
jobs
```

### Durum kontrolü

```bash
jobs
ps aux | grep -E "les.sh|linpeas.sh|lse.sh|unix-privesc-check|beroot.py|LinEnum.sh" | grep -v grep
```

### Canlı çıktı izleme

```bash
tail -f les_output.txt linpeas_output.txt lse_output.txt unix_privesc_output.txt beroot_output.txt linenum_output.txt
```

### Tüm işlemleri durdurma

```bash
pkill -f "les.sh|linpeas.sh|lse.sh|unix-privesc-check|beroot.py|LinEnum.sh"
```

<a id="cron-ile-zamanlama"></a>
## ⏱️ Cron ile Zamanlama

Her gün 02:00'de `linpeas.sh` çalıştırıp `/tmp` altına çıktı kaydeder:

```bash
(crontab -l 2>/dev/null; echo "0 2 * * * cd /tmp && ./linpeas.sh > /tmp/linpeas_daily_\$(date +\%Y\%m\%d).txt") | crontab -
```

<a id="sadece-linpeas-minimal-kullanim"></a>
## 🎯 Sadece LinPEAS (Minimal Kullanım)

```bash
cd /tmp
wget -q https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/linpeas.sh -O linpeas.sh
chmod +x linpeas.sh
nohup ./linpeas.sh > linpeas_$(date +%Y%m%d_%H%M%S).txt 2>&1 &
ps aux | grep linpeas | grep -v grep
```
