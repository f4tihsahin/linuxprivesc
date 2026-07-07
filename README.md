# Linux Privilege Escalation Tools Collection

Bu repo, Linux sistemlerde yetki yükseltme (Privilege Escalation) testleri için kullanılan en popüler araçların bir koleksiyonudur. Pentest ve güvenlik değerlendirmeleri sırasında hedef sistemleri taramak için hazırlanmıştır.

---

## 📦 **İçerik**

| Dosya | Açıklama |
|-------|----------|
| `les.sh` | Linux Exploit Suggester - Kernel zafiyetlerini tespit eder |
| `linpeas.sh` | LinPEAS - Kapsamlı yetki yükseltme vektörü tarayıcısı |
| `lse.sh` | Linux Smart Enumeration - Hızlı ve okunaklı sistem analizi |
| `unix-privesc-check` | Unix yetki yükseltme denetleyicisi |
| `beroot.py` | BeRoot - Python ile yazılmış privesc aracı |
| `LinEnum.sh` | Klasik Linux sistem enumürasyon aracı |

---

## 🚀 **Tek Bir Sunucuya Tüm Araçları İndirme**

### **Tek Komut (Hepsi)**
```bash
cd /tmp && \
wget https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/les.sh -O les.sh && \
wget https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/linpeas.sh -O linpeas.sh && \
wget https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/lse.sh -O lse.sh && \
wget https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/unix-privesc-check -O unix-privesc-check && \
wget https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/beroot.py -O beroot.py && \
wget https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/LinEnum.sh -O LinEnum.sh && \
chmod +x *.sh *.py && \
echo "✅ Tüm araçlar indirildi ve çalıştırılabilir yapıldı!"
🔧 Araçları Ayrı Ayrı İndirme ve Çalıştırma
1. Linux Exploit Suggester (LES)
bash
# İndir
wget https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/les.sh -O les.sh
chmod +x les.sh

# Çalıştır ve çıktıyı kaydet
./les.sh > les_output.txt

# Sadece çalıştır
./les.sh
2. LinPEAS
bash
# İndir
wget https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/linpeas.sh -O linpeas.sh
chmod +x linpeas.sh

# Çalıştır ve çıktıyı kaydet
./linpeas.sh > linpeas_output.txt

# Sadece çalıştır
./linpeas.sh
3. Linux Smart Enumeration (LSE)
bash
# İndir
wget https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/lse.sh -O lse.sh
chmod +x lse.sh

# Çalıştır ve çıktıyı kaydet (interaktif mod kapalı)
./lse.sh -i > lse_output.txt

# Sadece çalıştır (interaktif)
./lse.sh
4. Unix Privesc Check
bash
# İndir
wget https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/unix-privesc-check -O unix-privesc-check
chmod +x unix-privesc-check

# Çalıştır ve çıktıyı kaydet (standart mod)
./unix-privesc-check standard > unix_privesc_output.txt

# Sadece çalıştır
./unix-privesc-check standard
5. BeRoot
bash
# İndir
wget https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/beroot.py -O beroot.py
chmod +x beroot.py

# Çalıştır ve çıktıyı kaydet
python3 beroot.py > beroot_output.txt

# Sadece çalıştır
python3 beroot.py
6. LinEnum
bash
# İndir
wget https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/LinEnum.sh -O LinEnum.sh
chmod +x LinEnum.sh

# Çalıştır ve çıktıyı kaydet
./LinEnum.sh > linenum_output.txt

# Sadece çalıştır
./LinEnum.sh
📊 Tüm Araçları Toplu Çalıştır ve Çıktıları Kaydet
Yöntem 1: Manuel Sıralı Çalıştırma
bash
# Tüm araçları indir
cd /tmp
wget https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/les.sh -O les.sh && \
wget https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/linpeas.sh -O linpeas.sh && \
wget https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/lse.sh -O lse.sh && \
wget https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/unix-privesc-check -O unix-privesc-check && \
wget https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/beroot.py -O beroot.py && \
wget https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/LinEnum.sh -O LinEnum.sh && \
chmod +x *.sh *.py

# Tüm araçları sırayla çalıştır ve çıktıları kaydet
echo "=== LES ÇALIŞIYOR ===" && ./les.sh > les_output.txt && \
echo "=== LINPEAS ÇALIŞIYOR ===" && ./linpeas.sh > linpeas_output.txt && \
echo "=== LSE ÇALIŞIYOR ===" && ./lse.sh -i > lse_output.txt && \
echo "=== UNIX PRIVESC CHECK ÇALIŞIYOR ===" && ./unix-privesc-check standard > unix_privesc_output.txt && \
echo "=== BE ROOT ÇALIŞIYOR ===" && python3 beroot.py > beroot_output.txt && \
echo "=== LINENUM ÇALIŞIYOR ===" && ./LinEnum.sh > linenum_output.txt

# Tüm çıktıları listele
ls -la *_output.txt
Yöntem 2: Tarih Damgalı Çıktılar
bash
# Tarih damgası ile çıktı oluştur
DATE=$(date +%Y%m%d_%H%M%S)

./les.sh > les_${DATE}.txt
./linpeas.sh > linpeas_${DATE}.txt
./lse.sh -i > lse_${DATE}.txt
./unix-privesc-check standard > unix_privesc_${DATE}.txt
python3 beroot.py > beroot_${DATE}.txt
./LinEnum.sh > linenum_${DATE}.txt

echo "✅ Tüm çıktılar ${DATE} ile kaydedildi!"
ls -la *_${DATE}.txt
Yöntem 3: Tek Dosyada Topla
bash
# Tüm çıktıları tek bir dosyada topla
{
    echo "==================== LİNUX EXPLOIT SUGGESTER ===================="
    ./les.sh
    echo -e "\n\n==================== LİNPEAS ===================="
    ./linpeas.sh
    echo -e "\n\n==================== LSE ===================="
    ./lse.sh -i
    echo -e "\n\n==================== UNİX PRİVESC CHECK ===================="
    ./unix-privesc-check standard
    echo -e "\n\n==================== BE ROOT ===================="
    python3 beroot.py
    echo -e "\n\n==================== LİNENUM ===================="
    ./LinEnum.sh
} > all_scans_$(date +%Y%m%d_%H%M%S).txt

echo "✅ Tüm çıktılar tek dosyada toplandı!"
ls -la all_scans_*.txt
🎯 Hızlı Başlangıç Komutu (En Pratik)
bash
# Tüm araçları indir, çalıştır ve çıktıları kaydet
cd /tmp && \
wget -q https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/les.sh -O les.sh && \
wget -q https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/linpeas.sh -O linpeas.sh && \
wget -q https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/lse.sh -O lse.sh && \
wget -q https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/unix-privesc-check -O unix-privesc-check && \
wget -q https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/beroot.py -O beroot.py && \
wget -q https://raw.githubusercontent.com/f4tihsahin/privesc-tools/main/LinEnum.sh -O LinEnum.sh && \
chmod +x *.sh *.py && \
echo "✅ Tüm araçlar indirildi!" && \
./les.sh > les.txt && \
./linpeas.sh > linpeas.txt && \
./lse.sh -i > lse.txt && \
./unix-privesc-check standard > unix_privesc.txt && \
python3 beroot.py > beroot.txt && \
./LinEnum.sh > linenum.txt && \
echo "✅ Tüm taramalar tamamlandı!" && \
ls -la *.txt
