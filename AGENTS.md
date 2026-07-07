## Cursor Cloud specific instructions

Bu repo bir “uygulama” değil; tek tek çalıştırılan Linux privesc enum script koleksiyonu. Standart servis/DB yok. Komut örnekleri için `README.md` yeterli. (`README.md`.)

- **Çalıştırma (bulut VM doğrulama / hello-world)**: Çıktıları VM içinde `/tmp/privesc_out/` gibi bir klasöre yönlendirmek pratik. Örnek:
  - `./les.sh > les.txt 2>&1`
  - `./lse.sh -i > lse.txt 2>&1`
  - `./LinEnum.sh > linenum.txt 2>&1`
  - `./linpeas.sh > linpeas.txt 2>&1`

- **Bilinen repo durumu (kod değiştirmeden not)**:
  - `unix-privesc-check` dosyası bu repoda **shell script değil**, `pentestmonkey` sitesinden gelen **HTML içerik** gibi görünüyor; bu haliyle `./unix-privesc-check standard` beklenen şekilde çalışmayabilir.
  - `beroot.py` `from beroot.run import run` import ediyor ama repoda `beroot/` Python paketi yok; bu nedenle `python3 beroot.py` `ModuleNotFoundError` ile fail olabilir.

- **İşlem durdurma**: `README.md` içinde `pkill -f ...` örneği var; Cloud Agent oturumlarında bunun yerine PID bazlı kill tercih edin (yanlış process öldürme riskini azaltır).
